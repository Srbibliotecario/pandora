if game.PlaceId == 120853645603939 then
    -- Load
    local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

    -- Main
    local Window = OrionLib:MakeWindow({Name = "Pandora", HidePremium = false, SaveConfig = true, ConfigFolder = "Pandora"})

    -- Valor auto-click
    local AutoFarm = {
        autock = false,
        autoreb = false,
        rebirthValue = 0, -- Valor inicial padrão
        rebirth1t = false,
        rebirth10t = false,
        rebirth100t = false,
        rebirth1qd = false,
        rebirth10qd = false,
        rebirth100qd = false,
        rebirth1qn = false,
        rebirth10qn = false,
        rebirth100qn = false,
        rebirth1sx = false,
        rebirth10sx = false,
        rebirth100sx = false,
        automastery = false,
        autoopBasic = false,
        autoopUncommon = false,
        autoopsamurai = false,
        autoopAncient = false,
        autoopcyber = false,
        autooptiki = false,
        autoopvolcanic = false,
        autoopmagic = false,
        autoopheaven = false,
        autoopheaven25 = false,
        autoopspooky = false,
        autoworldspawn = false,
        autoworldsamurai = false,
        autoworldsavanna = false,
        autoworldcyber = false,
        autoworldtiki = false,
        autoworldvulcan = false,
        autoworldmagic = false,
        autoworldheaven = false,
        autoworldspooky = false,
        autousepotionclick = false,
        autousepotiongem = false,
        autousepotionluck = false,
        autousepotionrebirth = false

    }

    function autock()
        while AutoFarm.autock do
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Click"):FireServer()
            wait(0.05)
        end
    end

    -- Função para auto-rebirth
    function autoreb()
        while AutoFarm.autoreb do
            local args = {
                [1] = AutoFarm.rebirthValue -- Usa o valor dinâmico atualizado
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end
    
    -- Função para formatar números
    local function formatarNumero(valor)
        if valor >= 1e21 then
            return string.format("%.1fSx", valor / 1e21) -- Sextalhões
        elseif valor >= 1e18 then
            return string.format("%.1fQn", valor / 1e18) -- Quintilhões
        elseif valor >= 1e15 then
            return string.format("%.1fQd", valor / 1e15) -- Quadrilhões
        elseif valor >= 1e12 then
            return string.format("%.1fT", valor / 1e12) -- Trilhões
        elseif valor >= 1e9 then
            return string.format("%.1fB", valor / 1e9) -- Bilhões
        elseif valor >= 1e6 then
            return string.format("%.1fM", valor / 1e6) -- Milhões
        elseif valor >= 1e3 then
            return string.format("%.1fk", valor / 1e3) -- Milhares
        else
            return tostring(valor) -- Menor que 1k
        end
    end


    function automastery()
        while AutoFarm.automastery do
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("IncreaseMastery"):InvokeServer()
           wait(1)
         end
    end

    function rebirth10t()
        while AutoFarm.rebirth10t do
            local args = {
                [1] = 10000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth100t()
        while AutoFarm.rebirth100t do
            local args = {
                [1] = 100000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth1qd()
        while AutoFarm.rebirth1qd do
            local args = {
                [1] = 1000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth10qd()
        while AutoFarm.rebirth10qd do
            local args = {
                [1] = 10000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth100qd()
        while AutoFarm.rebirth100qd do
            local args = {
                [1] = 100000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth1qn()
        while AutoFarm.rebirth1qn do
            local args = {
                [1] = 1000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth10qn()
        while AutoFarm.rebirth10qn do
            local args = {
                [1] = 10000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth100qn()
        while AutoFarm.rebirth100qn do
            local args = {
                [1] = 100000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth1sx()
        while AutoFarm.rebirth1sx do
            local args = {
                [1] = 1000000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth10sx()
        while AutoFarm.rebirth10sx do
            local args = {
                [1] = 10000000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    function rebirth100sx()
        while AutoFarm.rebirth100sx do
            local args = {
                [1] = 10000000000000000000000
            }
            
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
            wait(1)
        end
    end

    


    -- Valor auto-open
    function autoopBasic()
        while AutoFarm.autoopBasic do
            local args = {
                [1] = "Basic",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopUncommon()
        while AutoFarm.autoopUncommon do
            local args = {
                [1] = "Uncommon",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopsamurai()
        while AutoFarm.autoopsamurai do
            local args = {
                [1] = "Samurai",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopAncient()
        while AutoFarm.autoopAncient do
            local args = {
                [1] = "Ancient",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopcyber()
        while AutoFarm.autoopcyber do
            local args = {
                [1] = "Cyber",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autooptiki()
        while AutoFarm.autooptiki do
            local args = {
                [1] = "Tiki",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopvolcanic()
        while AutoFarm.autoopvolcanic do
            local args = {
                [1] = "Volcanic",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopmagic()
        while AutoFarm.autoopmagic do
            local args = {
                [1] = "Magic",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopheaven()
        while AutoFarm.autoopheaven do
            local args = {
                [1] = "Heaven",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end 

    -- Valor auto-open
    function autoopheaven25()
        while AutoFarm.autoopheaven25 do
            local args = {
                [1] = "Heaven [25% Luck]",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

    -- Valor auto-open
    function autoopspooky()
        while AutoFarm.autoopspooky do
            local args = {
                [1] = "Spooky",
                [2] = "Triple"
            }
            game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("Hatch"):InvokeServer(unpack(args))
            wait(0.1)
        end
    end

     -- Valor auto-rebirth
      function autoreb()
          while AutoFarm.autoreb do
              local args = {
                [1] = AutoFarm.rebirthValue -- Usa o valor dinâmico atualizado
               }
                game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
                wait(3)
           end
       end




       function autoreb1b()
          while AutoFarm.autoreb1b do
             local args = {
                [1] = 1000000000
             }
            
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("Rebirth"):FireServer(unpack(args))
             wait(3)
           end
       end

       function automastery()
          while AutoFarm.automastery do
             game:GetService("ReplicatedStorage"):WaitForChild("Functions"):WaitForChild("IncreaseMastery"):InvokeServer()
              wait(1)
           end
       end

       function autoworldspawn()
         while AutoFarm.autoworldspawn do
             local args = {
                [1] = "Spawn"
             }
            
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
              wait(1)
           end
       end

       function autoworldsamurai()
        while AutoFarm.autoworldsamurai do
            local args = {
               [1] = "Samurai Land"
            }
           
            game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
             wait(1)
          end
      end

      function autoworldsavanna()
         while AutoFarm.autoworldsavanna do
             local args = {
               [1] = "Ancient Ruins"
             }
           
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
             wait(1)
          end
      end

      function autoworldcyber()
         while AutoFarm.autoworldcyber do
             local args = {
              [1] = "Cyber City"
             }
          
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
             wait(1)
          end
      end

      function autoworldtiki()
         while AutoFarm.autoworldtiki do
            local args = {
             [1] = "Tiki Island"
             }
         
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
              wait(1)
           end
       end

       function autoworldvulcan()
         while AutoFarm.autoworldvulcan do
             local args = {
             [1] = "Corrupted Volcano"
             }
        
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
              wait(1)
          end
      end

      function autoworldmagic()
         while AutoFarm.autoworldmagic do
             local args = {
             [1] = "Magic"
              }
       
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
              wait(1)
          end
      end

      function autoworldheaven()
         while AutoFarm.autoworldheaven do
             local args = {
             [1] = "Heaven"
             }
      
             game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
              wait(1)
          end
       end

       function autoworldspooky()
        while AutoFarm.autoworldspooky do
           local args = {
              [1] = "Spooky"
              }
     
              game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("SetWorldBoost"):FireServer(unpack(args))
               wait(1)
          end
      end



     function autousepotionclick()
          while AutoFarm.autousepotionclick do
             local args = {
                [1] = "Click"
              }
            
              game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("UsePotion"):FireServer(unpack(args))
              wait(1)
           end
       end

       function autousepotionluck()
          while AutoFarm.autousepotionluck do
             local args = {
              [1] = "Luck"
              }
          
              game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("UsePotion"):FireServer(unpack(args))
               wait(1)
           end
       end

     function autousepotiongem()
          while AutoFarm.autousepotiongem do
              local args = {
                [1] = "Gem"
              }
            
              game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("UsePotion"):FireServer(unpack(args))
               wait(1)
           end
       end

     function autousepotionrebirth()
           while AutoFarm.autousepotionrebirth do
              local args = {
                [1] = "Rebirth"
              }
            
              game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("UsePotion"):FireServer(unpack(args))
               wait(1)
           end
       end




    -- Jogador
    local panTab = Window:MakeTab({
        Name = "auto-farm",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })

    local Section = panTab:AddSection({
        Name = "auto-farm"
    })

    panTab:AddToggle({
        Name = "auto-click",
        Default = false,
        Callback = function(Value)
            AutoFarm.autock = Value
            if AutoFarm.autock then
                spawn(autock)
            end
        end
    })

    
    -- Indicador de Rebirth
    local rebirthIndicator = panTab:AddParagraph("Indicador de Rebirth", "Rebirth atual: " .. formatarNumero(AutoFarm.rebirthValue))

    -- Textbox para alterar o valor do Rebirth
    panTab:AddTextbox({
        Name = "Rebirth Value",
        Default = tostring(AutoFarm.rebirthValue),
        TextDisappear = false,
        Callback = function(Value)
            local number = tonumber(Value) -- Converte para número
            if number then
                AutoFarm.rebirthValue = number -- Atualiza o valor dinâmico
                rebirthIndicator:Set("Rebirth atual: " .. formatarNumero(AutoFarm.rebirthValue)) -- Atualiza o texto na interface
                print("Valor de Rebirth atualizado para:", AutoFarm.rebirthValue)
            else
                print("Por favor, insira um número válido.")
            end
        end
    })

    -- Toggle para auto-rebirth
    panTab:AddToggle({
        Name = "auto-rebirth",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoreb = Value
            if AutoFarm.autoreb then
                spawn(autoreb)
            end
        end
    })

    panTab:AddToggle({
        Name = "auto mastery",
        Default = false,
        Callback = function(Value)
            AutoFarm.automastery = Value
            if AutoFarm.automastery then
                spawn(automastery)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth10t",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth10t = Value
            if AutoFarm.rebirth10t then
                spawn(rebirth10t)
            end
        end
    })
    
    panTab:AddToggle({
        Name = " rebirth100t",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth100t = Value
            if AutoFarm.rebirth100t then
                spawn(rebirth100t)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth1qd",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth1qd = Value
            if AutoFarm.rebirth1qd then
                spawn(rebirth1qd)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth10qd",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth10qd = Value
            if AutoFarm.rebirth10qd then
                spawn(rebirth10qd)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth100qd",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth100qd = Value
            if AutoFarm.rebirth100qd then
                spawn(rebirth100qd)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth1qn",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth1qn = Value
            if AutoFarm.rebirth1qn then
                spawn(rebirth1qn)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth10qn",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth10qn = Value
            if AutoFarm.rebirth10qn then
                spawn(rebirth10qn)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth100qn",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth100qn = Value
            if AutoFarm.rebirth100qn then
                spawn(rebirth100qn)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth1sx",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth1sx = Value
            if AutoFarm.rebirth1sx then
                spawn(rebirth1sx)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth10sx",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth10sx = Value
            if AutoFarm.rebirth10sx then
                spawn(rebirth10sx)
            end
        end
    })

    panTab:AddToggle({
        Name = " rebirth100sx",
        Default = false,
        Callback = function(Value)
            AutoFarm.rebirth100sx = Value
            if AutoFarm.rebirth100sx then
                spawn(rebirth100sx)
            end
        end
    })



    local panTab = Window:MakeTab({
        Name = "egg"
    })
    
    
    panTab:AddToggle({
        Name = "egg-Basic",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopBasic = Value
            if AutoFarm.autoopBasic then
                spawn(autoopBasic)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Uncomon",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopUncommon = Value
            if AutoFarm.autoopUncommon then
                spawn(autoopUncommon)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Samurai",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopsamurai = Value
            if AutoFarm.autoopsamurai then
                spawn(autoopsamurai)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Ancient",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopAncient = Value
            if AutoFarm.autoopAncient then
                spawn(autoopAncient)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Cyber",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopcyber = Value
            if AutoFarm.autoopcyber then
                spawn(autoopcyber)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Tiki",
        Default = false,
        Callback = function(Value)
            AutoFarm.autooptiki = Value
            if AutoFarm.autooptiki then
                spawn(autooptiki)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Volcanic",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopvolcanic = Value
            if AutoFarm.autoopvolcanic then
                spawn(autoopvolcanic)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Magic",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopmagic = Value
            if AutoFarm.autoopmagic then
                spawn(autoopmagic)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-heaven",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopheaven = Value
            if AutoFarm.autoopheaven then
                spawn(autoopheaven)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Heaven25",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopheaven25 = Value
            if AutoFarm.autoopheaven25 then
                spawn(autoopheaven25)
            end
        end
    })

    panTab:AddToggle({
        Name = "egg-Spooky",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoopspooky = Value
            if AutoFarm.autoopspooky then
                spawn(autoopspooky)
            end
        end
    })

    local panTab = Window:MakeTab({
        Name = "Set-world"
    })

    panTab:AddToggle({
        Name = "1x(0 Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldspawn = Value
            if AutoFarm.autoworldspawn then
                spawn(autoworldspawn)
            end
        end
    })

    panTab:AddToggle({
        Name = "1.5x(1k Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldsamurai = Value
            if AutoFarm.autoworldsamurai then
                spawn(autoworldsamurai)
            end
        end
    })

    panTab:AddToggle({
        Name = "2x(25k Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldsavanna = Value
            if AutoFarm.autoworldsavanna then
                spawn(autoworldsavanna)
            end
        end
    })


    panTab:AddToggle({
        Name = "3x(250k Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldcyber = Value
            if AutoFarm.autoworldcyber then
                spawn(autoworldcyber)
            end
        end
    })
    panTab:AddToggle({
        Name = "5x(5m Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldtiki = Value
            if AutoFarm.autoworldtiki then
                spawn(autoworldtiki)
            end
        end
    })

    panTab:AddToggle({
        Name = "8x(250M Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldvulcan = Value
            if AutoFarm.autoworldvulcan then
                spawn(autoworldvulcan)
            end
        end
    })

    panTab:AddToggle({
        Name = "10x(25b Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldmagic = Value
            if AutoFarm.autoworldmagic then
                spawn(autoworldmagic)
            end
        end
    })

    panTab:AddToggle({
        Name = "15x(10t Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldheaven = Value
            if AutoFarm.autoworldheaven then
                spawn(autoworldheaven)
            end
        end
    })

    

    panTab:AddToggle({
        Name = "25x(2.5Qd Rebirth)",
        Default = false,
        Callback = function(Value)
            AutoFarm.autoworldspooky = Value
            if AutoFarm.autoworldspooky then
                spawn(autoworldspooky)
            end
        end
    })
    
    
    local panTab = Window:MakeTab({
        Name = "Misc"
    })
    
    panTab:AddToggle({
        Name = "potion-click",
        Default = false,
        Callback = function(Value)
            AutoFarm.autousepotionclick = Value
            if AutoFarm.autousepotionclick then
                spawn(autousepotionclick)
            end
        end
    })

    panTab:AddToggle({
        Name = "potion-luck",
        Default = false,
        Callback = function(Value)
            AutoFarm.autousepotionluck = Value
            if AutoFarm.autousepotionluck then
                spawn(autousepotionluck)
            end
        end
    })

    panTab:AddToggle({
        Name = "potion-gem",
        Default = false,
        Callback = function(Value)
            AutoFarm.autousepotiongem = Value
            if AutoFarm.autousepotiongem then
                spawn(autousepotiongem)
            end
        end
    })

    panTab:AddToggle({
        Name = "potion-rebirth",
        Default = false,
        Callback = function(Value)
            AutoFarm.autousepotionrebirth = Value
            if AutoFarm.autousepotionrebirth then
                spawn(autousepotionrebirth)
            end
        end
    })

    -- Adicionando Anti AFK
   local isAntiAfkActive = false
   local virtualUser = game:GetService("VirtualUser")

 panTab:AddToggle({
    Name = "Anti AFK",
    Default = false,
  Callback = function(Value)
        isAntiAfkActive = Value
        if isAntiAfkActive then
            game:GetService("Players").LocalPlayer.Idled:Connect(function()
                if isAntiAfkActive then
                    virtualUser:CaptureController()
                    virtualUser:ClickButton2(Vector2.new())
                end
            end)
        end
   end
})
















end

