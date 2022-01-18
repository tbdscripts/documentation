---
id: rust
title: 🪨 Rust
---

Cosmo supports Rust for the automated store. You can use it by installing the official Rust plugin for Cosmo.

:::caution
This integration will be rewritten soon, due to the new integration endpoints update.
You can still use the plugin but be ready to update it soon
:::

:::caution
The only supported action type is Console Command
:::

## Installing the integration
* [Download the integration](https://github.com/tbdscripts/cosmo-rust/archive/refs/heads/master.zip)
* Place the `Cosmo.cs` file in your servers `plugins` folder
* Restart your server
* Edit the generated configuration file

:::danger
The database credentials must **match** the credentials of your web instance of Cosmo **exactly**
Also make sure Remote SQL is enabled, so that the plugin can connect to your database!
:::

* Restart your server