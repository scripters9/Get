# Get
-- Crie uma GUI para o Hub
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TeleportButton = Instance.new("TextButton")
local ShopButton = Instance.new("TextButton")
local InventoryButton = Instance.new("TextButton")
local FlyButton = Instance.new("TextButton") -- Novo botão Fly

ScreenGui.Name = "HubGui"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

Frame.Name = "MainFrame"
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.Position = UDim2.new(0.3, 0, 0.3, 0)
Frame.Size = UDim2.new(0.4, 0, 0.4, 0)

TeleportButton.Name = "TeleportButton"
TeleportButton.Parent = Frame
TeleportButton.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
TeleportButton.Position = UDim2.new(0.1, 0, 0.1, 0)
TeleportButton.Size = UDim2.new(0.8, 0, 0.15, 0)
TeleportButton.Font = Enum.Font.SourceSans
TeleportButton.Text = "Teleport"
TeleportButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TeleportButton.TextSize = 24

ShopButton.Name = "ShopButton"
ShopButton.Parent = Frame
ShopButton.BackgroundColor3 = Color3.fromRGB(0, 170, 0)
ShopButton.Position = UDim2.new(0.1, 0, 0.3, 0)
ShopButton.Size = UDim2.new(0.8, 0, 0.15, 0)
ShopButton.Font = Enum.Font.SourceSans
ShopButton.Text = "Shop"
ShopButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ShopButton.TextSize = 24

InventoryButton.Name = "InventoryButton"
InventoryButton.Parent = Frame
InventoryButton.BackgroundColor3 = Color3.fromRGB(170, 0, 255)
InventoryButton.Position = UDim2.new(0.1, 0, 0.5, 0)
InventoryButton.Size = UDim2.new(0.8, 0, 0.15, 0)
InventoryButton.Font = Enum.Font.SourceSans
InventoryButton.Text = "Inventory"
InventoryButton.TextColor3 = Color3.fromRGB(255, 255, 255)
InventoryButton.TextSize = 24

FlyButton.Name = "FlyButton" -- Configurações do botão Fly
FlyButton.Parent = Frame
FlyButton.BackgroundColor3 = Color3.fromRGB(255, 170, 0)
FlyButton.Position = UDim2.new(0.1, 0, 0.7, 0)
FlyButton.Size = UDim2.new(0.8, 0, 0.15, 0)
FlyButton.Font = Enum.Font.SourceSans
FlyButton.Text = "Fly"
FlyButton.TextColor3 = Color3.fromRGB(255, 255, 255)
FlyButton.TextSize = 24

-- Função para teleportar o jogador
local function teleportarJogador()
    local player = game.Players.LocalPlayer
    if player and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
        player.Character.HumanoidRootPart.CFrame = CFrame.new(0, 10, 0) -- Coordenadas de teleporte
    end
end

-- Função para abrir a loja
local function abrirLoja()
    print("Loja aberta")
    -- Código 
