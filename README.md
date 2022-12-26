## Before start reading:
**IMPORTANT: ALL EXPLOIT STATUS ARE TAKEN FROM THE WEBSITE https://whatexploitsare.online/ BEFORE REPORTING A ERROR ABOUT STATUS, PLEASE, CHECK THE WEBSITE**
# ForLua: About
* Version: 0.1
* Dev: ss.spooky.ss#0003
## How it works
### Get Status
It uses the website https://whatexploitsare.online/ to get all the exploits status. The script send a request to the website, and the script uses the website JSON to find your script status.
### Get Download
It has a table with a lot of links for each exploit, when you use `:GetDownloadLink()` you are just asking for the script to return a specific value from the table.
## Programming Info
### Information about
|Information| Value |
|--------|---------|
|Lines | 96 |
|Functions | 3 |
|If | 6 |
|Return | 7 |
## Database
### Status Database

Everyhting inside https://whatexploitsare.online/ you can use it in `:GetStatus()`, example `:GetStatus("ROBLOX", false)`

### Download Database

|Exploit|Download Type|WRD|
|------|-------------|----|
|KRNL|Direct Link|Yes|
|Electron|Linkvertise|No|
|Oxygen|Direct Link|Yes|
|Fluxus|Linkvertise|Yes|
|Ro-Ware|Website Link|Yes|
|Celestial|Direct Link|No|
|Comet|Diret Link|Yes|

# ForLua: Documentation

## GetStatus

### Setup

First of all, insert this code into your script

```lua
local ForLua = loadstring(game:HttpGet(("https://raw.githubusercontent.com/spookysss/ForLua/main/forlua.lua"), true))()
```

### Requesting an exploit status

You should build something like this

```lua
ForLua:GetStatus()
```

The first value will be you exploit name, while the second value will be a boolean to determinate if you want to return two tables, a table with the exploit name and the information inside that table, for example

Input:
```lua
print(ForLua:GetStatus("KRNL", true))
```
Output:
```lua
{
  ["KRNL"] = {
    ["exploit_version"] = "2014Q",
    ["last_update"] = "2022-11-20",
    ["last_update_unix"] = 1668984122,
    ["roblox_version"] = "version-3b33190189084158",
    ["updated"] = true
  }
}
```

### Requesting an exploit download link

The first value means if you want to get the link from the WRD, or from the official download link, for example

Input:
```lua
print(lib:GetDownloadLink(true, "KRNL"))
```

Output:
```lua
-- WRD download link
```

