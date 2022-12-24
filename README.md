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

*Alert Commands*

By default, the resource uses the alert UI, but if you want to use commands instead, go to `configs/config.lua` and set `Config.useCommands` as true, if you want to add more commands just do the next steps:

```lua
Config.Commands = {
    ['entorno'] = { -- name of the command
        target = 'police', -- the job you want to be alerted when users use this command
        deftitle = '911 Alert', -- the title that the alert will have
        sound = true -- do you want sound when getting the alert?
    },
}
```
*Other Commands*

There are other commands like `/dispatch`, it opens the terminal where you can see the alerts and the interactive map, and `/panic` which will send an alert to all the polices in case a police officer needs help.

In case you want to change any of those commands, it's in the config file, you can change them whenever you want.

```lua
Config.UICommand = 'alertp' 

Config.TerminalCommand = 'dispatch' 

Config.PanicCommand = 'panic'
```

*How to send alerts from other scripts?*

If you want to link our dispatch with your robberys or any other resource, here's the trigger you might be looking for

```lua
    TriggerServerEvent('codesk_dispatch:send', target, text, coords, title, sound)
    --target: the job you want to alert
    --text: the text that the alert will have
    --coords: the coords of the alerts [You can use GetEntityCoords(PlayerPedId())]
    --title: the title of the alert
    --sound: true or false
```

