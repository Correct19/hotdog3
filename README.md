local player = game.Players.LocalPlayer
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = player.PlayerGui

local button = Instance.new("TextButton")
button.Size = UDim2.new(0, 200, 0, 50)
button.Position = UDim2.new(0.5, -100, 0.5, -25)
button.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
button.Text = "Parar Inimigos"
button.TextColor3 = Color3.fromRGB(0, 0, 0)
button.Font = Enum.Font.SourceSans
button.TextSize = 24
button.Parent = screenGui

local function pararInimigos()
    local inimigos = workspace:FindFirstChild("EnemyFolder")
    if inimigos then
        for _, inimigo in pairs(inimigos:GetChildren()) do
            if inimigo:FindFirstChild("Humanoid") then
                inimigo.Humanoid.WalkSpeed = 0
            end
        end
    else
   
  end    
end

button.Activated:Connect(pararInimigos)
