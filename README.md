# 🌟 Lrd Library

A modern, feature-rich UI library for Roblox with stunning animations and extensive functionality.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

- 🎨 Modern and sleek design
- 🌈 Customizable themes
- 🔄 Smooth animations
- 📱 Responsive layout
- 🛠️ Easy to use API
- 🎯 Multiple UI components
- 🎮 Controller support
- 🌓 Dark mode support

## 📥 Installation

### Method 1: Direct Download
Copy the `init.lua` file into your Roblox project.

### Method 2: Using Wally (Roblox Package Manager)
```toml
[dependencies]
StunningUI = "username/stunningui@1.0.0"
```

## 🚀 Quick Start

```lua
local StunningUI = require(path.to.StunningUI)

-- Create a new window
local window = StunningUI.new("My Cool GUI")

-- Add a button
window:AddButton("Click Me!", function()
    print("Button clicked!")
end)

-- Add a toggle
window:AddToggle("Enable Feature", false, function(enabled)
    print("Toggle state:", enabled)
end)

-- Add a slider
window:AddSlider("Speed", 0, 100, 50, function(value)
    print("Slider value:", value)
end)

-- Add a dropdown
window:AddDropdown("Select Option", {"Option 1", "Option 2", "Option 3"}, "Option 1", function(selected)
    print("Selected:", selected)
end)

-- Add a textbox
window:AddTextbox("Enter Name", "Type here...", function(text)
    print("Text entered:", text)
end)
```

## 🎨 Components

### Buttons
```lua
window:AddButton(text: string, callback: function)
```

### Toggles
```lua
window:AddToggle(text: string, default: boolean, callback: function)
```

### Sliders
```lua
window:AddSlider(text: string, min: number, max: number, default: number, callback: function)
```

### Dropdowns
```lua
window:AddDropdown(text: string, options: table, default: string, callback: function)
```

### Textboxes
```lua
window:AddTextbox(text: string, placeholder: string, callback: function)
```

## 🎨 Customization

You can customize the theme when creating a new window:

```lua
local customTheme = {
    Primary = Color3.fromRGB(65, 105, 225),
    Secondary = Color3.fromRGB(45, 45, 55),
    Background = Color3.fromRGB(30, 30, 35),
    Text = Color3.fromRGB(255, 255, 255),
    Accent = Color3.fromRGB(85, 125, 245),
    Success = Color3.fromRGB(46, 204, 113),
    Warning = Color3.fromRGB(241, 196, 15),
    Error = Color3.fromRGB(231, 76, 60)
}

local window = StunningUI.new("Custom Theme", customTheme)
```

## 📚 Examples

### Creating a Settings Menu
```lua
local window = StunningUI.new("Settings")

window:AddToggle("Enable Sound", true, function(enabled)
    -- Handle sound settings
end)

window:AddSlider("Volume", 0, 100, 50, function(volume)
    -- Handle volume change
end)

window:AddDropdown("Quality", {"Low", "Medium", "High"}, "Medium", function(quality)
    -- Handle quality change
end)
```

### Creating an Inventory
```lua
local window = StunningUI.new("Inventory")

for _, item in ipairs(inventory) do
    window:AddButton(item.name, function()
        -- Handle item selection
    end)
end
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

If you have any questions or need help, please open an issue on GitHub. 
