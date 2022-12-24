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

To add more jobs, go to configs/config.lua and you can add as much jobs as you want

```lua
Config.AllowedJobs = {
    {job = 'police', label = 'LSPD'},
    {job = 'ambulance', label = 'LSFD'},
    {job = 'mechanic', label = 'LSC'},
}
```

