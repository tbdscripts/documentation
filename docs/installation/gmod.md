---
id: garrys-mod
title: Garry's Mod
---

# 🔫 Cosmo - Garry's Mod
Cosmo supports Garry's Mod for the automated store. You can use it by installing the official Garry's Mod addon for Cosmo.

## Installing the integration
* [Download the integration](https://github.com/tbdscripts/cosmo-gmod/archive/refs/heads/master.zip)
* Extract the .zip file 
* Place the addon folder in your server's `addons` folder
* Head into `lua/cosmo` and edit the `sh_config.lua` file
* Update `Cosmo.Config.InstanceUrl` to match your website's domain
* Close `sh_config.lua` and open `sv_config.lua`
* Update `Cosmo.Config.ServerToken` to match your server token

:::info
Your server token can be found in the **Management Panel** under **Components -> Server**.
Click on the **Edit** button of the corresponding server and click **Regenerate Token**
:::
* Update any other configuration values if you wish
* Restart your server

## Supported Action Types
* Console Command
* Usergroup
* Custom Lua
* DarkRP Money
* DarkRP Levels
* (Permanent) Weapons
* Pointshop 1 points
* Pointshop 2 standard and premium points

## Turning on debug mode
If staff requested you to turn on debug mode for support, please follow these steps.

* Go into `lua/cosmo` and edit the `sh_config.lua` file
* Set `Cosmo.Config.LogLevel` to `Cosmo.Log.LEVEL_DEBUG`
* Restart your server