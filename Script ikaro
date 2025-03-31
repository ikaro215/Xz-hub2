-- Serviços
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local GuiService = game:GetService("GuiService")
local TweenService = game:GetService("TweenService")

-- Configurações
local killAuraRange = 10
local killAuraSpeed = 0.1
local aimbotSpeed = 0.1
local teleportPosition = Vector3.new(0, 0, 0) -- Posição para teletransporte

-- Interface de Usuário
local playerGui = game.Players.LocalPlayer.PlayerGui
local mainFrame = Instance.new("Frame")
mainFrame.Name = "DeadRailsScript"
mainFrame.Size = UDim2.new(0, 200, 0, 150)
mainFrame.Position = UDim2.new(0.5, -100, 0.5, -75)
mainFrame.BackgroundTransparency = 1

local killAuraButton = Instance.new("TextButton")
killAuraButton.Parent = mainFrame
killAuraButton.Size = UDim2.new(0, 100, 0, 25)
killAuraButton.Position = UDim2.new(0.25, -50, 0.2, -12)
killAuraButton.Text = "Kill Aura"
killAuraButton.BackgroundTransparency = 0.5

local aimbotButton = Instance.new("TextButton")
aimbotButton.Parent = mainFrame
aimbotButton.Size = UDim2.new(0, 100, 0, 25)
aimbotButton.Position = UDim2.new(0.25, -50, 0.4, -12)
aimbotButton.Text = "Aimbot"
aimbotButton.BackgroundTransparency = 0.5

local teleportButton = Instance.new("TextButton")
teleportButton.Parent = mainFrame
teleportButton.Size = UDim2.new(0, 100, 0, 25)
teleportButton.Position = UDim2.new(0.25, -50, 0.6, -12)
teleportButton.Text = "Teleport"
teleportButton.BackgroundTransparency = 0.5

mainFrame.Parent = playerGui

-- Funções
local function detectEnemies()
    local character = game.Players.LocalPlayer.Character
    if character then
        local position = character.HumanoidRootPart.Position
        for _, player in pairs(Players:GetPlayers()) do
            if player ~= game.Players.LocalPlayer then
                local enemyCharacter = player.Character
                if enemyCharacter then
                    local enemyPosition = enemyCharacter.HumanoidRootPart.Position
                    local distance = (position - enemyPosition).Magnitude
                    if distance <= killAuraRange then
                        return enemyCharacter
                    end
                end
            end
        end
    end
    return nil
end

local function attackEnemy(enemyCharacter)
    -- Lógica para atacar o inimigo
    print("Atacando inimigo!")
end

local function aimbot()
    -- Lógica para o aimbot
    print("Aimbot ativado!")
end

local function teleport()
    local character = game.Players.LocalPlayer.Character
    if character then
        character.HumanoidRootPart.CFrame = CFrame.new(teleportPosition)
    end
end

-- Conexões
killAuraButton.MouseButton1Click:Connect(function()
    while true do
        local enemy = detectEnemies()
        if enemy then
            attackEnemy(enemy)
        end
        wait(killAuraSpeed)
    end
end)

aimbotButton.MouseButton1Click:Connect(function()
    while true do
        aimbot()
        wait(aimbotSpeed)
    end
end)

teleportButton.MouseButton1Click:Connect(function()
    teleport()
end)
