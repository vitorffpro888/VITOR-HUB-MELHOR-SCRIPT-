-- vitor hub
local VitorHub = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local AutoFarmToggle = Instance.new("TextButton")
local AutoQuestToggle = Instance.new("TextButton")
local AutoRaidToggle = Instance.new("TextButton")
local TeleportButton = Instance.new("TextButton")
-- Adicione mais botões para outras funções aqui

-- Configurações da GUI
VitorHub.Name = "VitorHub"
VitorHub.Parent = game.CoreGui
VitorHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = VitorHub
MainFrame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
MainFrame.Position = UDim2.new(0.5, -150, 0.5, -200)
MainFrame.Size = UDim2.new(0, 300, 0, 400)
MainFrame.Draggable = true

Title.Name = "Title"
Title.Parent = MainFrame
Title.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
Title.Size = UDim2.new(1, 0, 0.1, 0)
Title.Font = Enum.Font.SourceSansBold
Title.Text = "Vitor Hub"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true

-- Botão Auto Farm
AutoFarmToggle.Name = "AutoFarmToggle"
AutoFarmToggle.Parent = MainFrame
AutoFarmToggle.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
AutoFarmToggle.Position = UDim2.new(0.05, 0, 0.15, 0)
AutoFarmToggle.Size = UDim2.new(0.9, 0, 0.1, 0)
AutoFarmToggle.Font = Enum.Font.SourceSans
AutoFarmToggle.Text = "Auto Farm: Off"
AutoFarmToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
AutoFarmToggle.TextScaled = true

-- Botão Auto Quest
AutoQuestToggle.Name = "AutoQuestToggle"
AutoQuestToggle.Parent = MainFrame
AutoQuestToggle.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
AutoQuestToggle.Position = UDim2.new(0.05, 0, 0.3, 0)
AutoQuestToggle.Size = UDim2.new(0.9, 0, 0.1, 0)
AutoQuestToggle.Font = Enum.Font.SourceSans
AutoQuestToggle.Text = "Auto Quest: Off"
AutoQuestToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
-- Script de Auto Raid para Blox Fruits no Roblox

local AutoRaidHub = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local AutoRaidToggle = Instance.new("TextButton")

-- Configurações da GUI
AutoRaidHub.Name = "AutoRaidHub"
AutoRaidHub.Parent = game.CoreGui
AutoRaidHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = AutoRaidHub
MainFrame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
MainFrame.Position = UDim2.new(0.5, -150, 0.5, -100)
MainFrame.Size = UDim2.new(0, 300, 0, 200)
MainFrame.Draggable = true

Title.Name = "Title"
Title.Parent = MainFrame
Title.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
Title.Size = UDim2.new(1, 0, 0.2, 0)
Title.Font = Enum.Font.SourceSansBold
Title.Text = "Auto Raid Hub"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true

-- Botão Auto Raid
AutoRaidToggle.Name = "AutoRaidToggle"
AutoRaidToggle.Parent = MainFrame
AutoRaidToggle.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
AutoRaidToggle.Position = UDim2.new(0.1, 0, 0.4, 0)
AutoRaidToggle.Size = UDim2.new(0.8, 0, 0.2, 0)
AutoRaidToggle.Font = Enum.Font.SourceSans
AutoRaidToggle.Text = "Auto Raid: Off"
AutoRaidToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
AutoRaidToggle.TextScaled = true

-- Função de Auto Raid
local autoRaidEnabled = false
AutoRaidToggle.MouseButton1Click:Connect(function()
autoRaidEnabled = not autoRaidEnabled
AutoRaidToggle.Text = "Auto Raid: " .. (autoRaidEnabled and "On" or "Off")

if autoRaidEnabled then
while autoRaidEnabled do
wait(1)
-- Código de Auto Raid
for _, raid in pairs(game.Workspace.Raids:GetChildren()) do
if raid:FindFirstChild("Humanoid") and raid.Humanoid.Health > 0 then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = raid.HumanoidRootPart.CFrame
wait(0.5)
game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool"):Activate()
end
end
end
end
end)

return AutoRaidHub
-- alto elite hunter

local AutoEliteHunterHub = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local AutoEliteHunterToggle = Instance.new("TextButton")

-- Configurações da GUI
AutoEliteHunterHub.Name = "AutoEliteHunterHub"
AutoEliteHunterHub.Parent = game.CoreGui
AutoEliteHunterHub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = AutoEliteHunterHub
MainFrame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
MainFrame.Position = UDim2.new(0.5, -150, 0.5, -100)
MainFrame.Size = UDim2.new(0, 300, 0, 200)
MainFrame.Draggable = true

Title.Name = "Title"
Title.Parent = MainFrame
Title.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
Title.Size = UDim2.new(1, 0, 0.2, 0)
Title.Font = Enum.Font.SourceSansBold
Title.Text = "Auto Elite Hunter Hub"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true

-- Botão Auto Elite Hunter
AutoEliteHunterToggle.Name = "AutoEliteHunterToggle"
AutoEliteHunterToggle.Parent = MainFrame
AutoEliteHunterToggle.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
AutoEliteHunterToggle.Position = UDim2.new(0.1, 0, 0.4, 0)
AutoEliteHunterToggle.Size = UDim2.new(0.8, 0, 0.2, 0)
AutoEliteHunterToggle.Font = Enum.Font.SourceSans
AutoEliteHunterToggle.Text = "Auto Elite Hunter: Off"
AutoEliteHunterToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
AutoEliteHunterToggle.TextScaled = true

-- Função de Auto Elite Hunter
local autoEliteHunterEnabled = true
AutoEliteHunterToggle.MouseButton1Click:Connect(function()
autoEliteHunterEnabled = not autoEliteHunterEnabled
AutoEliteHunterToggle.Text = "Auto Elite Hunter: " .. (autoEliteHunterEnabled and "On" or "Off")

if autoEliteHunterEnabled then
while autoEliteHunterEnabled do
wait(1)
-- Código de Auto Elite Hunter
for _, elite in pairs(game.Workspace.Elites:GetChildren()) do
if elite:FindFirstChild("Humanoid") and elite.Humanoid.Health > 0 then
