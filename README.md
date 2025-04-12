imgui-console
---
A starting point for my own dear imgui console widget.
See [Inspiration](https://github.com/AaronAppel/imgui-console/edit/master/README.md#inspiration-and-credits) section for credits.

I am aiming to combine the awesome search and hints features of RedSkittleFox's [imgui-console](https://github.com/RedSkittleFox/imgui-console), with rmxbalanque's excellent UI and scripts execution [imgui-console](https://github.com/rmxbalanque/imgui-console) to get a powerful development console. Add in the genius registry edit from cstom4994's [imgui_lua_inspector](https://github.com/cstom4994/imgui_lua_inspector) and the result would be a more complete and super powerful devlopment console.

Each are a little dated and have some buggy or unintitive behaviour for me so I ouwld like to improve on that.
Afterwards I hope to add my own unique features, if I find the time.

## My Changes
- "//" Comment support in .script files

## Future Features Wishlist
#### Output Search CTRL + F:
- Character highlighting
- Navigation between results

#### Advanced Search:
- Case sensitivity
- Exact versus fuzzy find/matching
- Regex matching

#### Debugging:
- Option to output text buffer content to file
- Option to automatically dump to file periodically or using a callback

#### Display:
- Options for text wrapping, font (size, style, bold)
- Advanced text formatting to support font and color changes (html, .md, etc)
- Log line numbers
- Window options: Adjustable columns, collapsable headers, re-orderable tabs, etc

#### Tabs:
Registry Tab
- View registered variables and commands information
- Edit registery entries
- Execute registery entries
- Reload registry at runtime (hot reload support)

File Tab:
- Displays file content
- File content formatting with syntax highlighting for different languages
- Button or way to pop out into separate window to be used as a file viewer

Custom User Tab
- Add callback or expose user methods to add custom tabs of their own

Output/Log Tab:
- Where messages and log history lives

Execution/Run Tab:
- Where command execution history lives

## Inspiration and Credits  

Inspired by rmxbalanque's [imgui-console](https://github.com/rmxbalanque/imgui-console)

<img class="animated-gif" src="https://user-images.githubusercontent.com/46074377/85931741-7b756200-b87b-11ea-9112-89d7fca305a0.gif" width="200" height="150"></img>

and RedSkittleFox's [imgui-console](https://github.com/RedSkittleFox/imgui-console)

<img src="https://github.com/AaronAppel/imgui-console/blob/ReadMeAssets/RedSkittleFox_ImguiConsole.jpg" width=200 height=150 />

and cstom4994's [imgui_lua_inspector](https://github.com/cstom4994/imgui_lua_inspector)

<img class="animated-gif" src="https://github.com/cstom4994/imgui_lua_inspector/blob/master/demo.gif" width="200" height="150"></img>

and neuroeidos' [console-manager](https://github.com/neuroeidos/console-manager)

<img src="https://private-user-images.githubusercontent.com/69249846/430962649-f0d0942d-faf5-41b2-8d8d-a86e8cb90105.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDQ0NzUxMjEsIm5iZiI6MTc0NDQ3NDgyMSwicGF0aCI6Ii82OTI0OTg0Ni80MzA5NjI2NDktZjBkMDk0MmQtZmFmNS00MWIyLThkOGQtYTg2ZThjYjkwMTA1LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA0MTIlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNDEyVDE2MjAyMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTlmM2U0MmM1NmY4NzRhZjcxZjA2NGM1ZDQyZTk2Mjc1Y2M5NDI4NGM5NGM3ZDdjNmNkNDhjZDI4MWY0ZDE2ZmYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.2ljbpZm0vQdcItK9M69758kxSAkUmY4DxcZleYhN0kw" width=200 height=150 />

Make sure to check them out!
