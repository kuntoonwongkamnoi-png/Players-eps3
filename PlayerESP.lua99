# Players-eps3
local Players = game:GetService("Players")
local me = Players.LocalPlayer

local function addESP(player)
    if player == me then return end

    local function setup(character)
        local old = character:FindFirstChild("PlayerESP")
        if old then old:Destroy() end

        local h = Instance.new("Highlight")
        h.Name = "PlayerESP"
        h.FillColor = Color3.fromRGB(255, 0, 0)
        h.OutlineColor = Color3.new(1, 1, 1)
        h.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
        h.Adornee = character
        h.Parent = character
    end

    if player.Character then setup(player.Character) end
    player.CharacterAdded:Connect(setup)
end

for _, p in ipairs(Players:GetPlayers()) do
    addESP(p)
end

Players.PlayerAdded:Connect(addESP)
