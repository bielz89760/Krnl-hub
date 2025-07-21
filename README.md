local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "Krnl Hub",
   Icon = nil, -- ou assetId válido em string
   LoadingTitle = "Krnl Hub",
   LoadingSubtitle = "by bzn",
   Theme = "Dark Blue",
   ToggleUIKeybind = "K",

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false,

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil,
      FileName = "Krnl Hub"
   },

   Discord = {
      Enabled = true,
      Invite = "53JypkeF",
      RememberJoins = true
   },

   KeySystem = true,
   KeySettings = {
      Title = "Krnl Keys",
      Subtitle = "Key System",
      Note = "Para conseguir a key, entre no discord do Krnl",
      FileName = "Key",
      SaveKey = true,
      GrabKeyFromSite = false,
      Key = {"Krnl", "Ore", "KrnlHub"}
   }
})

local KrnlHub = Window:CreateTab("Aura Hub", 4483362458)
local Farm = Window:CreateTab("Farm", 4483362458)
local Windows = Window:CreateTab("Windows", 4483362458)

local SectionMain = KrnlHub:CreateSection("Funções Principais")

local function MatarJogador()
   local player = game.Players.LocalPlayer
   if player and player.Character and player.Character:FindFirstChild("Humanoid") then
      player.Character.Humanoid.Health = 0
   end
end

local ButtonKill = Farm:CreateButton({
   Name = "Matar Jogador",
   Callback = MatarJogador
})

local Button = Windows:CreateButton({
   Name = "Infinite Jump",
   Callback = function()
  local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
local InfiniteJump = CreateButton("Infinite Jump: On", StuffFrame)
InfiniteJump.Position = UDim2.new(0,10,0,130)
InfiniteJump.Size = UDim2.new(0,150,0,30)
InfiniteJump.MouseButton1Click:connect(function()
	local state = InfiniteJump.Text:sub(string.len("Infinite Jump: ") + 1) --too lazy to count lol
	local new = state == "Off" and "On" or state == "On" and "Off"
	InfiniteJumpEnabled = new == "On"
	InfiniteJump.Text = "Infinite Jump: " .. new
end)
   end,
})

local Button = Windows:CreateButton({
   Name = "God mode",
   Callback = function()
   -- Improved God Mode Script

-- Constants
local MAX_HEALTH = 100 -- Adjust as needed

-- Get the player's character
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Function to enable god mode
local function enableGodMode()
    -- Get the humanoid of the character
    local humanoid = character:WaitForChild("Humanoid")
    
    -- Set max health and initial health
    humanoid.MaxHealth = MAX_HEALTH
    humanoid.Health = MAX_HEALTH
    
    -- Function to prevent character from taking damage
    local function preventDamage()
        humanoid:GetPropertyChangedSignal("Health"):Connect(function()
            humanoid.Health = MAX_HEALTH
        end)
    end
    
    -- Function to prevent character from dying
    local function preventDeath()
        humanoid.Died:Connect(function()
            wait(0.1) -- Wait a short delay to ensure proper health reset
            humanoid.Health = MAX_HEALTH
        end)
    end
    
    -- Connect the prevent functions
    preventDamage()
    preventDeath()
    
    -- Optional: Prevent status effects, such as debuffs or other harmful conditions
    humanoid:GetPropertyChangedSignal("WalkSpeed"):Connect(function()
        humanoid.WalkSpeed = 16 -- Example: Reset walk speed if affected
    end)
end

-- Call the function to enable god mode
enableGodMode()

   end,
})

local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "Krnl Hub",
   Icon = nil, -- ou assetId válido em string
   LoadingTitle = "Krnl Hub",
   LoadingSubtitle = "by bzn",
   Theme = "Dark Blue",
   ToggleUIKeybind = "K",

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false,

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil,
      FileName = "Krnl Hub"
   },

   Discord = {
      Enabled = true,
      Invite = "53JypkeF",
      RememberJoins = true
   },

   KeySystem = true,
   KeySettings = {
      Title = "Krnl Keys",
      Subtitle = "Key System",
      Note = "Para conseguir a key, entre no discord do Krnl",
      FileName = "Key",
      SaveKey = true,
      GrabKeyFromSite = false,
      Key = {"Krnl", "Ore", "KrnlHub"}
   }
})

local KrnlHub = Window:CreateTab("Aura Hub", 4483362458)
local Farm = Window:CreateTab("Farm", 4483362458)
local Windows = Window:CreateTab("Windows", 4483362458)

local SectionMain = KrnlHub:CreateSection("Funções Principais")

local function MatarJogador()
   local player = game.Players.LocalPlayer
   if player and player.Character and player.Character:FindFirstChild("Humanoid") then
      player.Character.Humanoid.Health = 0
   end
end

local ButtonKill = Farm:CreateButton({
   Name = "Matar Jogador",
   Callback = MatarJogador
})

local Button = Windows:CreateButton({
   Name = "Infinite Jump",
   Callback = function()
  local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
local InfiniteJump = CreateButton("Infinite Jump: On", StuffFrame)
InfiniteJump.Position = UDim2.new(0,10,0,130)
InfiniteJump.Size = UDim2.new(0,150,0,30)
InfiniteJump.MouseButton1Click:connect(function()
	local state = InfiniteJump.Text:sub(string.len("Infinite Jump: ") + 1) --too lazy to count lol
	local new = state == "Off" and "On" or state == "On" and "Off"
	InfiniteJumpEnabled = new == "On"
	InfiniteJump.Text = "Infinite Jump: " .. new
end)
   end,
})

local Button = Windows:CreateButton({
   Name = "God mode",
   Callback = function()
   -- Improved God Mode Script

-- Constants
local MAX_HEALTH = 100 -- Adjust as needed

-- Get the player's character
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Function to enable god mode
local function enableGodMode()
    -- Get the humanoid of the character
    local humanoid = character:WaitForChild("Humanoid")
    
    -- Set max health and initial health
    humanoid.MaxHealth = MAX_HEALTH
    humanoid.Health = MAX_HEALTH
    
    -- Function to prevent character from taking damage
    local function preventDamage()
        humanoid:GetPropertyChangedSignal("Health"):Connect(function()
            humanoid.Health = MAX_HEALTH
        end)
    end
    
    -- Function to prevent character from dying
    local function preventDeath()
        humanoid.Died:Connect(function()
            wait(0.1) -- Wait a short delay to ensure proper health reset
            humanoid.Health = MAX_HEALTH
        end)
    end
    
    -- Connect the prevent functions
    preventDamage()
    preventDeath()
    
    -- Optional: Prevent status effects, such as debuffs or other harmful conditions
    humanoid:GetPropertyChangedSignal("WalkSpeed"):Connect(function()
        humanoid.WalkSpeed = 16 -- Example: Reset walk speed if affected
    end)
end

-- Call the function to enable god mode
enableGodMode()

   end,
})

local Slider = Windows:CreateSlider({
   Name = "WalkSpeed",
   Range = {0, 300},
   Increment = 1,
   Suffix = "Speed",
   CurrentValue = 16,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        Game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (value)
   end,
})

Windows:CreateButton({
	Name = "Steal Menu",
	Callback = function()

loadstring(game:HttpGet("https://raw.githubusercontent.com/Youifpg/Steal-a-Brainrot-op/refs/heads/main/THXZ1N.lua"))()
	end
})

local ToggleFlash = AuraHub:CreateToggle({
   Name = "Flash",
   CurrentValue = false,
   Callback = function(Value)
      local player = game.Players.LocalPlayer
      if player and player.Character and player.Character:FindFirstChild("Humanoid") then
         if Value then
            player.Character.Humanoid.WalkSpeed = 50
         else
            player.Character.Humanoid.WalkSpeed = 16
         end
      end
   end
})

local SliderJump = Farm:CreateSlider({
   Name = "Pulo (JumpPower)",
   Range = {0, 100},
   Increment = 1,
   Suffix = "", -- sem '%'
   CurrentValue = 50,
   Callback = function(Value)
      local player = game.Players.LocalPlayer
      if player and player.Character and player.Character:FindFirstChild("Humanoid") then
         player.Character.Humanoid.JumpPower = Value
      end
   end
})

local SectionNPC = Farm:CreateSection("NPCs")

local InputNPC = Farm:CreateInput({
   Name = "Nome do NPC",
   PlaceholderText = "Digite um NPC...",
   RemoveTextAfterFocusLost = false,
   Callback = function(Text)
      -- aqui você pode adicionar ação para o texto digitado
   end
})

local DropdownNPC = Farm:CreateDropdown({
   Name = "Selecionar NPC",
   Options = {"Npc 1", "Npc 2", "Npc 3"},
   CurrentOption = "Npc 1",
   Callback = function(Option)
      -- ação para opção selecionada
   end
})

local SectionExtra = Farm:CreateSection("Extras")

local KeybindExample = Farm:CreateKeybind({
   Name = "Atalho de Teclado",
   CurrentKeybind = "F",
   HoldToInteract = false,
   Callback = function(Key)
      -- ação ao pressionar a tecla
   end
})

local ParagraphCreator = Farm:CreateParagraph({
   Title = "Criador",
   Content = "Krnl Hub by Bzn"
})

Rayfield:LoadConfiguration()

local ToggleFlash = AuraHub:CreateToggle({
   Name = "Flash",
   CurrentValue = false,
   Callback = function(Value)
      local player = game.Players.LocalPlayer
      if player and player.Character and player.Character:FindFirstChild("Humanoid") then
         if Value then
            player.Character.Humanoid.WalkSpeed = 50
         else
            player.Character.Humanoid.WalkSpeed = 16
         end
      end
   end
})

local SliderJump = Farm:CreateSlider({
   Name = "Pulo (JumpPower)",
   Range = {0, 100},
   Increment = 1,
   Suffix = "", -- sem '%'
   CurrentValue = 50,
   Callback = function(Value)
      local player = game.Players.LocalPlayer
      if player and player.Character and player.Character:FindFirstChild("Humanoid") then
         player.Character.Humanoid.JumpPower = Value
      end
   end
})

local SectionNPC = Farm:CreateSection("NPCs")

local InputNPC = Farm:CreateInput({
   Name = "Nome do NPC",
   PlaceholderText = "Digite um NPC...",
   RemoveTextAfterFocusLost = false,
   Callback = function(Text)
      -- aqui você pode adicionar ação para o texto digitado
   end
})

local DropdownNPC = Farm:CreateDropdown({
   Name = "Selecionar NPC",
   Options = {"Npc 1", "Npc 2", "Npc 3"},
   CurrentOption = "Npc 1",
   Callback = function(Option)
      -- ação para opção selecionada
   end
})

local SectionExtra = Farm:CreateSection("Extras")

local KeybindExample = Farm:CreateKeybind({
   Name = "Atalho de Teclado",
   CurrentKeybind = "F",
   HoldToInteract = false,
   Callback = function(Key)
      -- ação ao pressionar a tecla
   end
})

local ParagraphCreator = Farm:CreateParagraph({
   Title = "Criador",
   Content = "Krnl Hub by Bzn"
})

Rayfield:LoadConfiguration()
