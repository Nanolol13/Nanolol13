repeat task.wait() until game:IsLoaded()

-- Einstellungen
local USE_KEY_SYSTEM = true -- << Auf false setzen, um das Keysystem zu deaktivieren
local CORREKTER_KEY = "Nanolol13"

-- Lade UI
local Init = loadstring(game:HttpGet("https://raw.githubusercontent.com/BaconLords/Scripts/main/Key"))()

-- Fenster
local Window = Init:CreateWindow({
    Title = "Loader",
    SubTitle = "github.com/baconlords",
    TabSize = 100,
    LoadingTitle = "Loader",
    LoadingSubtitle = "by github.com/baconlords",
    ConfigurationSaving = {
        Enabled = false
    },
    Discord = {
        Enabled = false,
        Invite = "natives",
        RememberJoins = false
    },
    KeySystem = USE_KEY_SYSTEM,
    KeySettings = {
        Title = "Key benötigt",
        Subtitle = "Join Discord für Key",
        Note = "discord.gg/natives",
        FileName = "LoaderKey",
        SaveKey = true,
        GrabKeyFromSite = false,
        Key = {"Nanolol13"}
    }
})

-- Haupt-Tab
local MainTab = Window:CreateTab("Main", 123456)

MainTab:CreateButton({
    Name = "Script laden",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/BaconLords/Scripts/main/test.lua"))()
    end
})
