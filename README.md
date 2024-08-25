# gamezens-library
Roblox drawing library inspired by the well known gamesense menu, strictly for educational purposes

Example:
```luau
local window = lib.create_window("gamesense",Enum.KeyCode.Insert) -- function create_window(theme,open_keycode)
local tab = window.create_tab("rbxassetid://10464044451") -- function create_tab(tab_image)
local tab2 = window.create_tab("rbxassetid://10464234466")

local sector = tab.create_sector("Mute lib") -- function create_sector(sector_header_text)

sector.error("Error text") -- function sector.error(text); function error.set(new_text)
sector.info("Information text") -- function sector.info(text)
local warning = sector.warning("Warning text"	); warning.set("Warning (overriden) text")  -- function sector.warning(text);  function warning.set(new_text)
sector.text("Text") -- function text(); function text.set(new_text)

local textbox = sector.textbox("Textbox","Default text",function(text) -- function sector.textbox(placeholder,default_text,callback(text))
	print(text)
end)
textbox.set("Textbox (overriden)") -- function textbox.set(new_text)

local button = sector.button("Button",function() -- function sector.button(text,callback())
	print("Button clicked")
end)
button.set("Button (overriden)") -- function button.set(new_text)

local dd = sector.dropdown("Dropdown",{"1","2","3","4","5","6"},"3",function(value) -- function sector.dropdown(text,options: {},default,callback(value))
	print(value)
end)
dd.set("2") -- function dropdown.set(value_from_dropdown)
dd.add("added after dec") -- function dropdown.add(new_element)
dd.remove("2") -- function dropdown.remove(element_to_be_removed)
dd.set_text("Dropdown with new text") -- function dropdown.set_text(new_text)

local toggle = sector.toggle("Toggle",true,function(value) -- function sector.toggle(text,default,callback(state))
	print(value)
end)
toggle.set_text("Toggle new text") -- function toggle.set_text(new_text)
toggle.add_color(Color3.fromRGB(255,0,255),function(value) -- function toggle.add_color(default,callback(color))
	print(value)
end)

local slider = sector.slider("Slider","px",0,500,250,function(value) -- function sector.slider(text,unit,min,max,default,callback(value))
	print(value)
end)
slider.set(0.5) -- function slider.set(value: 0.00-1.00)
slider.set_text("Slider overwritten") -- function slider.set_text(new_text)
```
