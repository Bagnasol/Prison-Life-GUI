local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()

local Window = Library.CreateLib("Juna Official -Prison Life- V0.1", "Sentinel")
local Tab = Window:NewTab("Main")

local Section = Tab:NewSection("Player")

Section:NewSlider("WS", "Change Player WS", 500, 16, function(s) -- 500 (MaxValue) | 16 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

Section:NewSlider("Jump Power", "Change Player Jump Power", 500, 16, function(s) -- 500 (MaxValue) | 16 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)

local Tab = Window:NewTab("Other")


local Section = Tab:NewSection("Misc")

Section:NewButton("Remove Doors", "Remove Door in game", function()
    game.Workspace.Doors:Destroy()
end)
