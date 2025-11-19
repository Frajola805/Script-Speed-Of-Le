local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "AutoFluenx - Speed Legends",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Loading...",
   LoadingSubtitle = "by Rchard",
   ShowText = "AutoFluenx", -- for mobile users to unhide rayfield, change if you'd like
   Theme = "DarkBlue", -- Check https://docs.sirius.menu/rayfield/configuration/themes
   ToggleUIKeybind = "K", -- The keybind to toggle the UI visibility (string like "K" or Enum.KeyCode)
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   }
})

--local
local teleporteAtivo = false
local velocidadeTeleporte = 0.1
local farmAtivo = false
local teleporteAtivo = false

--Tab Info
local SzTab = Window:CreateTab("Logs Info", 7734075797) -- Title, Image

--Paragrafor Info
local Paragraph = SzTab:CreateParagraph(
    {Title = "📜 Logs Info", 
    Content = [[

Versão: 2.1.0
Desenvolvedor: Rchard
Última atualização: 19/11/2024

🔧 CONFIGURAÇÃO:
• Tema: Amethyst
• Toggle key: K
• Save config: Ativado

🔒 Segurança:
• Anti-detection ativo
• Sem keyloggers

📝 Idiomas:
• Português BR
> English - Em Breve...

📞 SUPORTE:
Contato: Discord
    ]]
})

--Toggle Discord

--Tab Farm
local SzTab = Window:CreateTab("Main", 6026568198) -- Title, Image

--Toggle Auto Orb
local Toggle = SzTab:CreateToggle({
   Name = "Auto Farm Orb",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
            farmAtivo = Value
            while farmAtivo do
                local args = {
	"collectOrb",
	"Red Orb",
	"City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Blue Orb",
	"City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Orange Orb",
	"City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Yellow Orb",
	"City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Red Orb",
	"Snow City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Blue Orb",
	"Snow City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Orange Orb",
	"Snow City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Yellow Orb",
	"Snow City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Red Orb",
	"Magma City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Blue Orb",
	"Magma City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Orange Orb",
	"Magma City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))

                local args = {
	"collectOrb",
	"Yellow Orb",
	"Magma City"
}
game:GetService("ReplicatedStorage"):WaitForChild("rEvents"):WaitForChild("orbEvent"):FireServer(unpack(args))
            wait(velocidadeFarm)
        end
   end,
})

--Toggle Auto Hoop
local Toggle = SzTab:CreateToggle({
   Name = "Auto Hoop",
   CurrentValue = false,
   Callback = function(Value)
      teleporteAtivo = Value
      
      while teleporteAtivo do
         -- 🎯 TODAS AS SUAS POSIÇÕES!
         local posicoes = {
            CFrame.new(-11096.9756, 200.85762, 4465.38623, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(-13140.8779, 200.85762, 4465.38623, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(-12993.0518, 200.85762, 5222.70654, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(-13254.3594, 222.457626, 4891.59521, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(3980.02271, 159.935181, 5589.11572, 0, -1, -0, -1, 0, -0, 0, 0, -1),
            CFrame.new(4650.22803, 221.242523, 5608.65186, -4.30345535e-05, -0.984805167, 0.173663586, -1.00000012, 4.27365303e-05, -3.75509262e-06, -3.75509262e-06, -0.173663586, -0.984805346),
            CFrame.new(5392.49902, 297.850708, 5885.29834, -4.94718552e-05, -0.819112599, 0.573632717, -0.99999994, 4.94718552e-05, -1.55866146e-05, -1.55866146e-05, -0.573632717, -0.819112539),
            CFrame.new(5666.27734, 326.553741, 6494.69971, -5.96046448e-07, 0.0871878564, 0.996191859, -1, -5.96046448e-07, -5.66244125e-07, 5.66244125e-07, -0.996191859, 0.0871878266),
            CFrame.new(3806.31958, 299.433289, 7225.60938, 4.76837158e-05, -0.996190667, -0.0872024298, -1, -4.76837158e-05, -2.08243728e-06, -2.08243728e-06, 0.0872024298, -0.996190667),
            CFrame.new(4516.79004, 221.241058, 7181.66162, 4.76837158e-05, -0.996190667, -0.0872024298, -1, -4.76837158e-05, -2.08243728e-06, -2.08243728e-06, 0.0872024298, -0.996190667),
            CFrame.new(5361.84033, 297.850372, 7025.4126, -2.06232071e-05, -0.866040051, -0.499974549, -0.99999994, 2.06232071e-05, 5.5283308e-06, 5.5283308e-06, 0.499974549, -0.866039991),
            CFrame.new(2094.12817, 252.005325, 12877.9062, -1.50203705e-05, -0.615643799, 0.788024604, -1, 1.49607658e-05, -7.33137131e-06, -7.33137131e-06, -0.788024604, -0.61564374),
            CFrame.new(1664.36707, 80.9162903, 12589.6143, -1.26361847e-05, -0.965938866, -0.258770198, -0.99999994, 1.2755394e-05, 1.66893005e-06, 1.66893005e-06, 0.258770198, -0.965938807),
            CFrame.new(1941.97888, 93.2132187, -2047.35083, 1.2755394e-05, 0.965938866, -0.258770198, -0.99999994, 1.2755394e-05, -1.66893005e-06, 1.66893005e-06, 0.258770198, 0.965938926),
            CFrame.new(-536.467285, 58.4536629, -133.109863, 2.07424164e-05, 0.57355696, -0.819165647, -0.99999994, 2.07424164e-05, -1.07884407e-05, 1.07884407e-05, 0.819165647, 0.573557019),
            CFrame.new(1173.29761, 92.0464401, -6024.1543, -0.0154292583, 0.998328567, -0.0556953251, -0.999880552, -0.015357852, 0.00171039067, 0.000852169469, 0.0557150617, 0.998446345),
            CFrame.new(-489.536072, 98.2929382, 2502.04541, -0.00131225586, 0.707105696, 0.707106769, -0.999998391, -0.00182616711, -2.96533108e-05, 0.00127029419, -0.707105637, 0.707106829),
            CFrame.new(137.719437, 75.417099, -5972.40283, 0, 1, -0, -1, 0, 0, 0, 0, 1),
            CFrame.new(-350.591919, 66.0969849, -8732.12598, -0.0153386593, 0.989664674, -0.142578512, -0.999882221, -0.0152513981, 0.00170488656, -0.00048726052, 0.142587885, 0.989782035),
            CFrame.new(230.099228, 94.2061768, 80.8283539, 0, 1, -0, -1, 0, 0, 0, 0, 1),
            CFrame.new(-85.5007935, 116.006203, -107.871613, -1.03712082e-05, 0.93968749, 0.34203434, -1, -1.03712082e-05, -1.81794167e-06, 1.81794167e-06, -0.34203434, 0.939687431),
            CFrame.new(1805.65564, 90.9715958, 4617.18018, 2.07424164e-05, 0.57355696, -0.819165647, -0.99999994, 2.07424164e-05, -1.07884407e-05, 1.07884407e-05, 0.819165647, 0.573557019),
            CFrame.new(2061.9834, 159.914078, 4374.27637, -2.07424164e-05, -0.57355696, 0.819165647, -0.99999994, 2.07424164e-05, -1.07884407e-05, -1.07884407e-05, -0.819165647, -0.5735569),
            CFrame.new(-533.456421, 58.4536629, 209.88414, 1.54972076e-06, -0.422563195, -0.906333447, -1, -1.54972076e-06, -9.83476639e-07, -9.83476639e-07, 0.906333447, -0.422563195),
            CFrame.new(473.226654, 66.0969849, -10867.7471, -0.0150305033, 0.992836952, 0.118527696, -0.999880791, -0.0153421164, 0.00171688572, 0.00352305174, -0.11848776, 0.992949247),
            CFrame.new(-1746.42273, 150.61377, 5372.56934, 5.68628311e-05, -0.481334239, 0.876537085, -1, -5.68628311e-05, 3.3646822e-05, 3.3646822e-05, -0.876537085, -0.481334209),
            CFrame.new(2485.43457, 135.569199, 12384.5459, 7.56978989e-06, -0.681969762, 0.731380403, -1, -7.62939453e-06, 3.27825546e-06, 3.27825546e-06, -0.731380403, -0.681969762),
            CFrame.new(-1645.2699, 69.0413895, 5337.91748, -1.00135803e-05, 0.342006564, 0.939697623, -1, -1.00135803e-05, -7.00354576e-06, 7.00354576e-06, -0.939697623, 0.342006564),
            CFrame.new(-278.891968, 66.0969849, -10946.5225, -0.0153386593, 0.989664674, -0.142578512, -0.999882221, -0.0152513981, 0.00170488656, -0.00048726052, 0.142587885, 0.989782035),
            CFrame.new(1769.68945, 80.9169006, 12879.6992, 0, -1, -0, -1, 0, -0, 0, 0, -1),
            CFrame.new(2333.35889, 161.676392, 13369.0215, 0, -1, -0, -1, 0, -0, 0, 0, -1),
            CFrame.new(355.429199, 111.786301, -10924.5957, -4.66108322e-05, 0.998628676, 0.0523534007, -1, -4.66108322e-05, -1.22189522e-06, 1.22189522e-06, -0.0523534007, 0.998628616),
            CFrame.new(-15167.4121, 382.212463, 4888.26465, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(-15376.3613, 412.314148, 4475.25928, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279),
            CFrame.new(-15156.4043, 355.120056, 4141.85889, 8.70227814e-06, 0.0200170279, 0.999799609, -1, 8.70227814e-06, 8.55326653e-06, -8.55326653e-06, -0.999799609, 0.0200170279)
         }
         
         -- 🎯 LOOP POR TODAS AS POSIÇÕES
         for i, pos in pairs(posicoes) do
            if not teleporteAtivo then break end  -- Para se desativado
            
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
            wait(velocidadeTeleporte)
         end
      end
   end,
})

--Tab Configuração
local SzTab = Window:CreateTab("Configuração", 7734053495) -- Title, Image

--Slide Auto Orb
local Slider = SzTab:CreateSlider({
   Name = "Velocidade Auto Orb",
   Range = {0.00001, 1},
   Increment = 0.1,
   Suffix = "Segundos",
   CurrentValue = 0.1,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
            velocidadeFarm = Value
   end,
})

--Slide Auto Hoop
local Slider = SzTab:CreateSlider({
   Name = "Velocidade Auto Hoop",
   Range = {0.00001, 1},
   Increment = 0.1,
   Suffix = "Segundos",
   CurrentValue = 0.1,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
            velocidadeFarm = Value
   end,
})

--Aviso
local Paragraph = SzTab:CreateParagraph({
   Title = "⚠️  Avisos Importantes:",
   Content = [[
   USE COM MODERAÇÃO!
• Não abuse para evitar ban
• Caso for usar em uma velocidade muito 
  alta, use em servidores com poucos players!

• USE POR SUA CONTA E RISCO!

💡  DICAS DE SEGURANÇA:
• Velocidade ideal: 0.05 a 0.1
   ]]
})
