game:GetService("StarterGui"):SetCore("SendNotification", { 
    Title = "Spotify do this cuz i like it";
    Text = "Enjoy i damage my finger 2 times xD";
    Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150";
    Duration = 5;
})

local TweenService = game:GetService("TweenService")
local RunService = game:GetService("RunService")

local SpotifyGUI = Instance.new("ScreenGui")
local Everything = Instance.new("Frame")
local Right = Instance.new("Frame")
local Left = Instance.new("Frame")
local Spotify = Instance.new("ImageButton")
local Title = Instance.new("TextLabel")
local Artist = Instance.new("TextLabel")
local Bar = Instance.new("Frame")
local Progress = Instance.new("Frame")
local Current = Instance.new("TextLabel")
local Maximum = Instance.new("TextLabel")
local Premuim = Instance.new("Folder")
local Previous = Instance.new("ImageButton")
local Skip = Instance.new("ImageButton")
local Resume = Instance.new("ImageButton")
local Update = Instance.new("TextButton")
local Token = Instance.new("TextBox")
local Credit = Instance.new("TextLabel")

Premuim.Name = 'Premuim'
SpotifyGUI.Name = "SpotifyGUI"
SpotifyGUI.Parent = game.CoreGui

Everything.Name = "Everything"
Everything.Parent = SpotifyGUI
Everything.BackgroundColor3 = Color3.fromRGB(52, 52, 52)
Everything.BackgroundTransparency = 1.000
Everything.BorderSizePixel = 0
Everything.Position = UDim2.new(0.336979181, 0, 0.0666666701, 0)
Everything.Size = UDim2.new(0, 625, 0, 99)

Right.Name = "Right"
Right.Parent = Everything
Right.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
Right.BorderSizePixel = 0
Right.Position = UDim2.new(0.498807102, 0, -0.00751272682, 0)
Right.Size = UDim2.new(0, 313, 0, 63)

Left.Name = "Left"
Left.Parent = Everything
Left.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
Left.BorderSizePixel = 0
Left.Position = UDim2.new(0.000307112932, 0, -0.00751272682, 0)
Left.Size = UDim2.new(0, 312, 0, 63)

Spotify.Name = "Spotify"
Spotify.Parent = Everything
Spotify.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Spotify.BackgroundTransparency = 1.000
Spotify.BorderSizePixel = 0
Spotify.Position = UDim2.new(0.449566096, 0, -0.644637704, 0)
Spotify.Size = UDim2.new(0, 63, 0, 63)
Spotify.ZIndex = 2
Spotify.Image = "http://www.roblox.com/asset/?id=4526758789"

Title.Name = "Title"
Title.Parent = Everything
Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Title.BackgroundTransparency = 1.000
Title.Position = UDim2.new(0.0208000001, 0, 0, 0)
Title.Size = UDim2.new(0, 525, 0, 33)
Title.Font = Enum.Font.Cartoon
Title.Text = "The Title Of The Song Playing"
Title.TextColor3 = Color3.fromRGB(0, 81, 255)
Title.TextSize = 26.000
Title.TextStrokeTransparency = 0.000
Title.TextWrapped = true
Title.TextXAlignment = Enum.TextXAlignment.Left

Artist.Name = "Artist"
Artist.Parent = Everything
Artist.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Artist.BackgroundTransparency = 1.000
Artist.Position = UDim2.new(0.0192000009, 0, 0.292929292, 0)
Artist.Size = UDim2.new(0, 310, 0, 20)
Artist.Font = Enum.Font.Cartoon
Artist.Text = "Artist"
Artist.TextColor3 = Color3.fromRGB(0, 243, 255)
Artist.TextSize = 25.000
Artist.TextStrokeTransparency = 0.000
Artist.TextWrapped = true
Artist.TextXAlignment = Enum.TextXAlignment.Left

Bar.Name = "Bar"
Bar.Parent = Everything
Bar.BackgroundColor3 = Color3.fromRGB(64, 64, 64)
Bar.BorderSizePixel = 0
Bar.Position = UDim2.new(0.0192000009, 0, 0.696969688, 0)
Bar.Size = UDim2.new(0, 601, 0, 3)

Progress.Name = "Bar"
Progress.Parent = Bar
Progress.BackgroundColor3 = Color3.fromRGB(29, 185, 84)
Progress.BorderSizePixel = 0
Progress.Size = UDim2.new(0, 1, 0, 3)

Current.Name = "Current"
Current.Parent = Everything
Current.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Current.BackgroundTransparency = 1.000
Current.BorderSizePixel = 0
Current.Position = UDim2.new(0, 0, 0.727272749, 0)
Current.Size = UDim2.new(0, 48, 0, 27)
Current.Font = Enum.Font.Cartoon
Current.Text = "0:00"
Current.TextColor3 = Color3.fromRGB(0, 0, 0)
Current.TextSize = 20.000
Current.TextWrapped = true

Maximum.Name = "Maximum"
Maximum.Parent = Everything
Maximum.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Maximum.BackgroundTransparency = 1.000
Maximum.BorderSizePixel = 0
Maximum.Position = UDim2.new(0.923200011, 0, 0.727272749, 0)
Maximum.Size = UDim2.new(0, 48, 0, 27)
Maximum.Font = Enum.Font.Cartoon
Maximum.Text = "0:00"
Maximum.TextColor3 = Color3.fromRGB(0, 0, 0)
Maximum.TextSize = 20.000
Maximum.TextWrapped = true

Premuim.Parent = Everything

Previous.Name = "Previous"
Previous.Parent = Premuim
Previous.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Previous.BackgroundTransparency = 1.000
Previous.BorderSizePixel = 0
Previous.Position = UDim2.new(0.43840006, 0, 0.709112108, 0)
Previous.Size = UDim2.new(0, 30, 0, 30)
Previous.ZIndex = 2
Previous.Image = "http://www.roblox.com/asset/?id=4458878865"

Skip.Name = "Skip"
Skip.Parent = Premuim
Skip.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Skip.BackgroundTransparency = 1.000
Skip.BorderSizePixel = 0
Skip.Position = UDim2.new(0.513600111, 0, 0.709112108, 0)
Skip.Size = UDim2.new(0, 30, 0, 30)
Skip.ZIndex = 2
Skip.Image = "http://www.roblox.com/asset/?id=4458877936"

Resume.Name = "Resume"
Resume.Parent = Premuim
Resume.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Resume.BackgroundTransparency = 1.000
Resume.BorderSizePixel = 0
Resume.Position = UDim2.new(0.476800054, 0, 0.709112108, 0)
Resume.Size = UDim2.new(0, 30, 0, 30)
Resume.ZIndex = 2
Resume.Image = "http://www.roblox.com/asset/?id=4458862490"

Update.Name = "Update"
Update.Parent = Everything
Update.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
Update.BackgroundTransparency = 1.000
Update.Position = UDim2.new(0.524800003, 0, 0.282828271, 0)
Update.Size = UDim2.new(0, 90, 0, 31)
Update.Font = Enum.Font.Cartoon
Update.Text = "Update Token"
Update.TextColor3 = Color3.fromRGB(255, 255, 255)
Update.TextScaled = true
Update.TextSize = 14.000
Update.TextStrokeTransparency = 0.000
Update.TextWrapped = true

Token.Name = "Token"
Token.Parent = Everything
Token.BackgroundColor3 = Color3.fromRGB(56, 56, 56)
Token.BorderSizePixel = 0
Token.Position = UDim2.new(0.680000007, 0, 0.303030312, 0)
Token.Size = UDim2.new(0, 190, 0, 26)
Token.Font = Enum.Font.SourceSans
Token.PlaceholderText = "Insert Token Here:D"
Token.Text = ""
Token.TextColor3 = Color3.fromRGB(0, 0, 0)
Token.TextSize = 14.000
Token.TextWrapped = true

Credit.Name = "Credit"
Credit.Parent = Everything
Credit.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Credit.BackgroundTransparency = 1.000
Credit.BorderSizePixel = 0
Credit.Position = UDim2.new(0.860387504, 0, -0.0141414106, 0)
Credit.Size = UDim2.new(0, 86, 0, 28)
Credit.Font = Enum.Font.Cartoon
Credit.Text = "Credits: ken:3"
Credit.TextColor3 = Color3.fromRGB(2, 208, 92)
Credit.TextScaled = true
Credit.TextSize = 14.000
Credit.TextWrapped = true


open = true
token = nil
premuim = nil
local spotify = function(url,method,token)
    local success, res = pcall(syn.request, {
            Url = url,
            Method = method,
            Headers = {
                ["Accept"] = "application/json",
                ["Authorization"] = 'Bearer ' .. token,
                ["Content-Type"] = "application/json"
            }
    })
    if success == true and type(res) == "table" and #res.Body > 0 then
        local parsed = game.HttpService:JSONDecode(res.Body)
        return {
            artist = parsed['item']['artists'][1]['name'],
            title = parsed['item']['name'],
			current = parsed['progress_ms'],
			maximum = parsed['item']['duration_ms'],
			playing = parsed['is_playing'],
        }
    else
        return {
            artist = 'Failed to get artist',
            title = 'Failed to get song name',
			current = 'nil',
			maximum = 'nil'
        }
    end
	end

	function Format(Int)
	return string.format("%02i", Int)
	end

	function convertToHMS(Seconds)
	local Minutes = (Seconds - Seconds%60)/60
	Seconds = Seconds - Minutes*60
	local Hours = (Minutes - Minutes%60)/60
	Minutes = Minutes - Hours*60
	return Format(Minutes)..":"..Format(Seconds)
	end

Spotify.MouseButton1Click:Connect(function()
	if open == true then
		open = false
Left:TweenSizeAndPosition(
	UDim2.new(0, 0,0, 63),
	UDim2.new(0.499, 0,-0.008, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
)
Right:TweenSizeAndPosition(
	UDim2.new(0, 0,0, 63),   
	UDim2.new(0.499, 0,-0.008, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
	)
Spotify:TweenPosition(
	UDim2.new(0.45, 0,-0.008, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
)
Artist.Visible = false
Title.Visible = false
Token.Visible = false
Update.Visible = false
Credit.Visible = false
	elseif open == false then
		open = true
Left:TweenSizeAndPosition(
	UDim2.new(0, 312,0, 63),   
	UDim2.new(0, 0,-0.008, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
)
Right:TweenSizeAndPosition(
	UDim2.new(0, 313,0, 63),
	UDim2.new(0.499, 0,-0.008, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
)
Spotify:TweenPosition(
	UDim2.new(0.45, 0,-0.645, 0),
	Enum.EasingDirection.In,
	Enum.EasingStyle.Sine,
	2,
	true
)
wait(2)
Artist.Visible = true
Title.Visible = true
Token.Visible = true
Update.Visible = true
Credit.Visible = true
end
end)

Update.MouseButton1Click:Connect(function()
	token = Token.Text
end)

while wait(.25) do
if token ~= nil or token ~= '' then
local comply2, returns = pcall(spotify,'https://api.spotify.com/v1/me/player/currently-playing','GET',token)
if comply2 == true then
Title.Text = returns.title
Artist.Text = returns.artist
local currentsec = math.floor(returns.current/1000)
local maximumsec = math.floor(returns.maximum/1000)
Current.Text = convertToHMS(currentsec)
Maximum.Text = convertToHMS(maximumsec)
if returns.playing == true then
	Resume.Image = 'http://www.roblox.com/asset/?id=4458862490'
			elseif returns.playing == false then
		Resume.Image = 'http://www.roblox.com/asset/?id=4458863290'
end

  if maximumsec ~= 0 or maximumsec ~= '' then
   if currentsec > 0 then
    Progress:TweenSize(UDim2.new(currentsec/maximumsec,0,1,0), Enum.EasingDirection.Out, Enum.EasingStyle.Quad, .25)
   else
    Progress.Size = UDim2.new(0,0,1,0)
   end
  end

end
	end
end
