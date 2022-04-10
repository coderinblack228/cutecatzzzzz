local TweenService = game:GetService("TweenService") 
function library:Tween(...) TweenService:Create(...):Play() end 

local Notification = Instance.new("ScreenGui")
do
local OnHitFrame = Instance.new("Frame")
local UIListLayout = Instance.new("UIListLayout")
local SampleFrame = Instance.new("Frame")
local Grad = Instance.new("Frame")
local SampleLabel = Instance.new("TextLabel")
local UIGradient = Instance.new("UIGradient")

Notification.Name = "Notification"
Notification.Parent = game.CoreGui
Notification.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

OnHitFrame.Name = "OnHitFrame"
OnHitFrame.Parent = Notification
OnHitFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
OnHitFrame.BackgroundTransparency = 1.000
OnHitFrame.Position = UDim2.new(0, 52, 0, -15)
OnHitFrame.Size = UDim2.new(0, 300, 0, 500)

UIListLayout.Parent = OnHitFrame
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 6)

SampleFrame.Name = "SampleFrame"
SampleFrame.Parent = OnHitFrame
SampleFrame.AutomaticSize = Enum.AutomaticSize.XY
SampleFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SampleFrame.BackgroundTransparency = 1.000
SampleFrame.BorderColor3 = Color3.fromRGB(7, 0, 0)
SampleFrame.Size = UDim2.new(0, 0, 0, 24)

Grad.Name = "Grad"
Grad.Parent = SampleFrame
Grad.BackgroundColor3 = Color3.fromRGB(222, 232, 255)
Grad.BackgroundTransparency = 1.000
Grad.AutomaticSize = Enum.AutomaticSize.Y
Grad.BorderSizePixel = 0
Grad.Size = UDim2.new(0, 3, 0, 24)

SampleLabel.Name = "SampleLabel"
SampleLabel.Parent = Grad
SampleLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SampleLabel.BackgroundTransparency = 1.000
SampleLabel.BorderSizePixel = 0
SampleLabel.Position = UDim2.new(1.97835922, 0, 0, 0)
SampleLabel.Size = UDim2.new(0, 0, 0, 24)
SampleLabel.Font = Enum.Font.Ubuntu
SampleLabel.Text = "TEST"
SampleLabel.TextTruncate = Enum.TextTruncate.AtEnd
SampleLabel.AutomaticSize = Enum.AutomaticSize.XY
SampleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
SampleLabel.TextSize = 13.000
SampleLabel.TextStrokeTransparency = 0.000
SampleLabel.TextTransparency = 1.000
SampleLabel.TextXAlignment = Enum.TextXAlignment.Left

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(49, 49, 49)), ColorSequenceKeypoint.new(0.41, Color3.fromRGB(25, 25, 25)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(25, 25, 25))}
UIGradient.Rotation = 90
UIGradient.Parent = SampleFrame
end
 
local function CreateHitElement(text,col,time, size, size2, size3, size4)
    spawn(function()
		local Frame = Notification.OnHitFrame.SampleFrame:Clone()
		local Grad = Frame.Grad
        local Label = Grad.SampleLabel
		
		library:Tween(Frame, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {Size = UDim2.new(size, size2, size3, size4)}) 
		library:Tween(Label, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {Size = UDim2.new(size, size2, size3, size4)}) 	
		
		library:Tween(Frame, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 0.000})       
		library:Tween(Grad, TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 0.000})  
		library:Tween(Label, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {TextTransparency = 0.000}) 
		
		Frame.Parent = Notification.OnHitFrame
		Grad.Parent = Frame
		Label.Parent = Grad
		Label.TextColor3 = col
		Label.Text = text
		wait(time)
		library:Tween(Frame, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1.000})       
		library:Tween(Grad, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1.000})  
		library:Tween(Label, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {TextTransparency = 1.000})
		library:Tween(Label, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {TextStrokeTransparency = 1.000})
		
		library:Tween(Frame, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {Size = UDim2.new(0, 0, size3, size4)}) 
		library:Tween(Label, TweenInfo.new(0.8, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {Size = UDim2.new(0, 0, size3, size4)}) 
		
		wait(0.8)
		Frame:Destroy()
		Grad:Destroy()
        Label:Destroy()
    end)
end
