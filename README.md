local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Fluent " .. Fluent.Version,
    SubTitle = "by dawid",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true,
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl
})

local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

local Options = Fluent.Options

do
    Fluent:Notify({
        Title = "Notification",
        Content = "This is a notification",
        SubContent = "SubContent",
        Duration = 5
    })

    Tabs.Main:AddParagraph({
        Title = "AutoFarm",
        Content = "Sistema automático para defesa e teleporte aos mobs."
    })

    -- Variáveis de Controle (já estão dentro do Fluent.Options)
    local DefenseToggle = Tabs.Main:AddToggle("DefenseToggle", { Title = "Defesa Automática", Default = false })
    local TpMobsToggle = Tabs.Main:AddToggle("TpMobsToggle", { Title = "Teleportar para Mobs", Default = false })

    -- Função da Defesa Automática
    DefenseToggle:OnChanged(function(Value)
        if Value then
            task.spawn(function()
                while Options.DefenseToggle.Value do
                    local args = {
                        [1] = "startDefense",
                        [2] = {
                            ["privacy"] = "private",
                            ["difficult"] = "easy"
                        }
                    }
                    game:GetService("ReplicatedStorage"):WaitForChild("Shared"):WaitForChild("events"):WaitForChild("RemoteEvent"):FireServer(unpack(args))
                    Fluent:Notify({
                        Title = "Defesa",
                        Content = "Defesa iniciada automaticamente!",
                        Duration = 3
                    })
                    task.wait(5)
                end
            end)
        else
            Fluent:Notify({
                Title = "Defesa",
                Content = "Defesa automática desativada.",
                Duration = 3
            })
        end
    end)

    -- Função do TP para Mobs
    TpMobsToggle:OnChanged(function(Value)
        if Value then
            task.spawn(function()
                local mobsFolder = workspace:WaitForChild("tempEnemies") -- Trocar aqui se a pasta tiver outro nome
                local player = game.Players.LocalPlayer
                local character = player.Character or player.CharacterAdded:Wait()
                local hrp = character:WaitForChild("HumanoidRootPart")

                while Options.TpMobsToggle.Value do
                    for _, mob in ipairs(mobsFolder:GetChildren()) do
                        if mob:IsA("Model") and mob:FindFirstChild("HumanoidRootPart") then
                            hrp.CFrame = mob.HumanoidRootPart.CFrame
                            task.wait(1)
                        elseif mob:IsA("Part") then
                            hrp.CFrame = mob.CFrame
                            task.wait(1)
                        end
                    end
                    task.wait(0.1)
                end
            end)
        else
            Fluent:Notify({
                Title = "Teleporte",
                Content = "Teleporte para mobs desativado.",
                Duration = 3
            })
        end
    end)
end

-- SaveManager e InterfaceManager Setup
SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)

SaveManager:IgnoreThemeSettings()
SaveManager:SetIgnoreIndexes({})

InterfaceManager:SetFolder("FluentScriptHub")
SaveManager:SetFolder("FluentScriptHub/specific-game")

InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)

Window:SelectTab(1)

Fluent:Notify({
    Title = "Fluent",
    Content = "Script carregado com sucesso!",
    Duration = 8
})

SaveManager:LoadAutoloadConfig()
