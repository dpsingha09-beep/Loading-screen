-- LocalScript inside StarterGui

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
gui.IgnoreGuiInset = true -- covers entire screen

-- Fullscreen black background
local bg = Instance.new("Frame")
bg.Size = UDim2.new(1, 0, 1, 0)
bg.Position = UDim2.new(0, 0, 0, 0)
bg.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
bg.BorderSizePixel = 0
bg.Parent = gui

-- Title text
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0.2, 0)
title.Position = UDim2.new(0, 0, 0.25, 0)
title.BackgroundTransparency = 1
title.TextColor3 = Color3.fromRGB(0, 255, 0)
title.Font = Enum.Font.Code
title.TextScaled = true
title.Text = "Your script is bypassing anti-cheat..."
title.Parent = bg

-- Progress bar background
local barBg = Instance.new("Frame")
barBg.Size = UDim2.new(0.6, 0, 0.05, 0)
barBg.Position = UDim2.new(0.2, 0, 0.55, 0)
barBg.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
barBg.BorderSizePixel = 0
barBg.Parent = bg

-- Progress bar fill
local barFill = Instance.new("Frame")
barFill.Size = UDim2.new(0, 0, 1, 0)
barFill.BackgroundColor3 = Color3.fromRGB(0, 200, 0)
barFill.BorderSizePixel = 0
barFill.Parent = barBg

-- Fake loading sequence
task.wait(2)
for i = 1, 99 do
	title.Text = "Bypassing anti-cheat... "..i.."%"
	barFill.Size = UDim2.new(i/100, 0, 1, 0)
	task.wait(0.05)
end

-- Stuck at 99%
title.Text = "Bypassing anti-cheat... 99%"
task.wait(5)

-- Final message
title.Text = "Almost ready..."
