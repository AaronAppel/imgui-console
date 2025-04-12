For full example project see : https://github.com/rmxbalanque/imgui-console/blob/master/example/src/example_main.cpp

## Creating The Console
#include "imgui_console.h"
ImGuiConsole console;

## Registering Variables
console.System().RegisterVariable("background_color", clear_color, imvec4_setter);

## Registering Commands
console.System().RegisterCommand("random_background_color", "Assigns a random color to the background application",
     [&clear_color]()
     {
         clear_color.x = (rand() % 256) / 256.f;
         clear_color.y = (rand() % 256) / 256.f;
         clear_color.z = (rand() % 256) / 256.f;
         clear_color.w = (rand() % 256) / 256.f;
     });
console.System().RegisterCommand("reset_background_color", "Reset background color to its original value",
     [&clear_color, val = clear_color]()
     {
         clear_color = val;
     });

## Commands
help - information. Can be used with other commands like "help filter" or "help reset_background_color"
clear - clears text buffer contents
filter - adds following arguments to top filter bar field
get - prints value of registered variable
set - assigns value of registered variable
run - executes script by name

## Logging Output
// Log example information:
console.System().Log(csys::ItemType::INFO) << "George enjoys swinging" << csys::endl;
console.System().Log(csys::ItemType::WARNING) << "Look out for that tree!" << csys::endl;
console.System().Log(csys::ItemType::SEVERE) << "Ouch!" << csys::endl;

## Rendering Console imgui Window
while (appRunning)
... // imgui begin draw
ImGuiConsole console.Draw();
... // imgui end draw

## Custom Scripting
A script file contains commands, the same as if you entered them manually in the console.

Example console.script:
```
// Comment
clear
help filter
get background_color
set background_color [255 0 0 255]
get background_color
```

The convenience and power of scripts comes from executing several custom commands quickly and easily.
When testing a system, or developing a feature, setup up a runtime environment to a specific state with a single command, or even automatically.

## Registering Custom Scripts
console.System().RegisterScript("script_command_name", "./filename.script");
Registered scripts will be listed in the "Scripts" tab as buttons.
Use the "Reload Scripts" button to update contents at runtime.
