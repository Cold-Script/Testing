local function Esp(child, name)
	local hi = Instance.new("Highlight")
	hi.Parent = child
	hi.Adornee = child
	hi.OutlineColor = Color3.new(1,1,1)
	hi.FillColor = Color3.fromRGB(255, 255, 255)
	hi.FillTransparency = 0.5
     hi.OutlineTransparency = 1
     hi.DepthMode = "AlwaysOnTop"
     hi.Name = "ESP"
task.spawn(function()
while wait() do
	if child:IsA("Part") then
		child.Color = Color3.new(1,1,1)
		child.Transparency = 0
	end
  end
end)
	spawn(function()
		while task.wait() do
			if hi then
				local hue = tick() % 5 / 5
				local color = Color3.new(1,1,1)
				hi.OutlineColor = color
				hi.FillColor = color
			end
		end
	end)
end


local function Esp1(child, name)
local function Esp(child, name)
	local billboard_gui = Instance.new("BillboardGui")
	billboard_gui.Active = false
	billboard_gui.AlwaysOnTop = true
	billboard_gui.ClipsDescendants = false
	billboard_gui.LightInfluence = 10
	billboard_gui.Size = UDim2.new(2, 0, 2, 0)
	billboard_gui.ResetOnSpawn = false
	billboard_gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	billboard_gui.Parent = child
	billboard_gui.Name = "ESP"
	local text_label = Instance.new("TextLabel")
	text_label.Font = Enum.Font.Oswald
	text_label.Text = name
	text_label.TextColor3 = Color3.new(1, 1, 1)
	text_label.TextScaled = false
	text_label.TextSize = 35
	text_label.TextWrapped = false
	text_label.BackgroundColor3 = Color3.new(1, 1, 1)
	text_label.BackgroundTransparency = 1
	text_label.BorderColor3 = Color3.new(0, 0, 0)
	text_label.BorderSizePixel = 0
	text_label.Size = UDim2.new(1, 0, 1, 0)
	text_label.Visible = true
	text_label.Parent = billboard_gui

	local uistroke = Instance.new("UIStroke")
	uistroke.Thickness = 0.5
	uistroke.Parent = text_label

	spawn(function()
		while task.wait() do
			local hue = tick() % 5 / 5
			local color = Color3.fromRGB(255,0,0)
			text_label.TextColor3 = color
		end
	end)
end

local function Esp2(child, name)
local function Esp(child, name)
	local billboard_gui = Instance.new("BillboardGui")
	billboard_gui.Active = false
	billboard_gui.AlwaysOnTop = true
	billboard_gui.ClipsDescendants = false
	billboard_gui.LightInfluence = 10
	billboard_gui.Size = UDim2.new(2, 0, 2, 0)
	billboard_gui.ResetOnSpawn = false
	billboard_gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	billboard_gui.Parent = child
	billboard_gui.Name = "ESP2"
	local text_label = Instance.new("TextLabel")
	text_label.Font = Enum.Font.Oswald
	text_label.Text = name
	text_label.TextColor3 = Color3.new(1, 1, 1)
	text_label.TextScaled = false
	text_label.TextSize = 35
	text_label.TextWrapped = false
	text_label.BackgroundColor3 = Color3.new(1, 1, 1)
	text_label.BackgroundTransparency = 1
	text_label.BorderColor3 = Color3.new(0, 0, 0)
	text_label.BorderSizePixel = 0
	text_label.Size = UDim2.new(1, 0, 1, 0)
	text_label.Visible = true
	text_label.Parent = billboard_gui

	local uistroke = Instance.new("UIStroke")
	uistroke.Thickness = 0.5
	uistroke.Parent = text_label

	spawn(function()
		while task.wait() do
			local hue = tick() % 5 / 5
			local color = Color3.fromRGB(255,0,0)
			text_label.TextColor3 = color
		end
	end)
end

local function Esp3(child, name)
local function Esp(child, name)
	local billboard_gui = Instance.new("BillboardGui")
	billboard_gui.Active = false
	billboard_gui.AlwaysOnTop = true
	billboard_gui.ClipsDescendants = false
	billboard_gui.LightInfluence = 10
	billboard_gui.Size = UDim2.new(2, 0, 2, 0)
	billboard_gui.ResetOnSpawn = false
	billboard_gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	billboard_gui.Parent = child
	billboard_gui.Name = "ESP3"
	local text_label = Instance.new("TextLabel")
	text_label.Font = Enum.Font.Oswald
	text_label.Text = name
	text_label.TextColor3 = Color3.new(1, 1, 1)
	text_label.TextScaled = false
	text_label.TextSize = 35
	text_label.TextWrapped = false
	text_label.BackgroundColor3 = Color3.new(1, 1, 1)
	text_label.BackgroundTransparency = 1
	text_label.BorderColor3 = Color3.new(0, 0, 0)
	text_label.BorderSizePixel = 0
	text_label.Size = UDim2.new(1, 0, 1, 0)
	text_label.Visible = true
	text_label.Parent = billboard_gui

	local uistroke = Instance.new("UIStroke")
	uistroke.Thickness = 0.5
	uistroke.Parent = text_label

	spawn(function()
		while task.wait() do
			local hue = tick() % 5 / 5
			local color = Color3.fromRGB(255,0,0)
			text_label.TextColor3 = color
		end
	end)
end

local rep = 'https://raw.githubusercontent.com/mstudio45/LinoriaLib/main/'

local lib =   loadstring(game:HttpGet(rep.. 'Library.lua'))()
local save =  loadstring(game:HttpGet(rep.. 'addons/SaveManager.lua'))()
local theme = loadstring(game:HttpGet(rep.. 'addons/ThemeManager.lua'))()

local Options = getgenv().Options

local window = lib:CreateWindow({
    Title = 'ESP',
    Center = true,
    AutoShow = true,
    TabPadding = 8,
    MenuFadeTime = 0.2
})
Tab = window:AddTab("Main")
Tav = Tab:AddLeftGroupbox("ESP")
Tav:AddToggle("",{Text="ESP DOORS",Callback=function(Value)
if Value then
			for _, v in pairs(workspace:GetDescendants()) do
				if v.Name == "Door" and v.Parent.Name == "Door" then
					Esp(v, "DOOR")
				end
			end
			DOORESP = workspace.ChildAdded:Connect(function(child)
				task.wait(0.1)
				for _, v in pairs(child:GetDescendants()) do
					if v.Name == "Door" and v.Parent.Name == "Door" then
					Esp(v, "DOOR")
					end
				end
			end)
		else
			DOORESP:Disconnect()
			for _, v in pairs(workspace.CurrentRooms:GetDescendants()) do
				if v.Name == "ESP" then
					v:Destroy()
				end
			end
		end})
  Tav:AddToggle("",{Text="ESP DOORS",Callback=function(Value)
if Value then
			for _, v in pairs(workspace:GetDescendants()) do
				if v.Name == "Door" and v.Parent.Name == "Door" then
					Esp(v, "DOOR")
				end
			end
			DOORESP = workspace.ChildAdded:Connect(function(child)
				task.wait(0.1)
				for _, v in pairs(child:GetDescendants()) do
					if v.Name == "Door" and v.Parent.Name == "Door" then
					Esp(v, "DOOR")
					end
				end
			end)
		else
			DOORESP:Disconnect()
			for _, v in pairs(workspace.CurrentRooms:GetDescendants()) do
				if v.Name == "ESP" then
					v:Destroy()
				end
			end
		end})
  Tav:AddToggle("",{Text="ESP KEY & LEVER+",Callback=function(Value)
if Value then
			for _, v in pairs(workspace:GetDescendants()) do
				if v.Name == "KeyObtain" then
					Esp(v, "Key")
      elseif v.Name == "LeverForGate" then
					Esp(v, "Lever")
     elseif v.Name == "TimerLever" then
					Esp(v, "Timer Lever")
				end
			end
			KEYESP = workspace.ChildAdded:Connect(function(child)
				task.wait(0.1)
				for _, v in pairs(child:GetDescendants()) do
					if v.Name == "KeyObtain" then
					Esp(v, "Key")
         elseif v.Name == "LeverForGate" then
					Esp(v, "Lever")
        elseif v.Name == "TimerLever" then
					Esp(v, "Timer Lever")
					end
				end
			end)
		else
			KEYESP:Disconnect()
			for _, v in pairs(workspace.CurrentRooms:GetDescendants()) do
				if v.Name == "ESP2" then
					v:Destroy()
				end
			end
		end})
  
  
