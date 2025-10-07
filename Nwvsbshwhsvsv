local player = game.Players.LocalPlayer

-- HumanoidRootPartを取得する関数
local function getHumanoidRootPart()
    local character = player.Character or player.CharacterAdded:Wait()
    return character:FindFirstChild("HumanoidRootPart")
end

-- Lavaを1秒ごとに削除するループ
local function removeLava()
    while true do
        local map = game.Workspace:FindFirstChild("Map")
        if map then
            local ghostShipInterior = map:FindFirstChild("GhostShipInterior")
            if ghostShipInterior then
                local lavaParts = ghostShipInterior:FindFirstChild("LavaParts")
                if lavaParts then
                    local lava = lavaParts:FindFirstChild("Lava")
                    if lava then
                        lava:Destroy()
                        print("Lava を削除しました。")
                    end
                end
            end
        end
        task.wait(1)
    end
end

task.spawn(removeLava)

-- すでにGUIがある場合は削除
if player.PlayerGui:FindFirstChild("TeleportGui") then
    player.PlayerGui.TeleportGui:Destroy()
end

-- GUI作成
local screenGui = 
