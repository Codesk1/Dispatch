# Codesk Dispatch
Dispatch System made by Codesk for ESX and QB 

# Installation

- Download the resource (Make sure to download the one for your framework, either ESX or QBCore)
- Add the resource to your resources folder
- Check the config to modify something you might wanna modify
- Add `ensure codesk_dispatch` to your server.cfg

Thats all you need for the installation.

# Usage

Here we will expain the main usage of the resource.

*Jobs*

To add more jobs, go to `configs/config.lua` and you can add as much jobs as you want

```lua
Config.AllowedJobs = {
    {job = 'police', label = 'LSPD'},
    {job = 'ambulance', label = 'LSFD'},
    {job = 'mechanic', label = 'LSC'},
}
```

*Commands*

By default, the resource uses the alert UI, but if you want to use commands instead, go to `configs/config.lua` and set `Config.useCommands` as true, if you want to add more commands just do the next steps:

```lua
Config.Commands = {
    ['entorno'] = { -- name of the command
        target = 'police', -- the job you want to be alerted when users use this command
        deftitle = '911 Alert', -- the title that the alert will have
        sound = true -- do you want sound when getting the alert?
    },
}```

