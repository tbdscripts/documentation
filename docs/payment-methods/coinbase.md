---
id: coinbase
title: 🪙 Coinbase
---

[Coinbase](https://www.coinbase.com/) is a crypto trading platform, it allows you to buy/sell/trade your crypto. Cosmo has an integration with it, it allows people to purchase packages from your store with crypto. 

Crypto in general however has a couple downsides: the coins fluctuate in value and a payment can take a while to process.

## Setting up Coinbase

### Getting the required credentials
* Head to the [Coinbase Commerce Dashboard](https://commerce.coinbase.com/dashboard)
* Sign in (or create an account)
* Once in the dashboard, go to the `Settings` tab (button located on the left side of the page)
* Scroll all the way down until you get to a section called `API Keys`
    * Click `Create an API key`
    * Once created, click the copy icon to copy the API key.
    * Copy the API key to place where you can retrieve it later.
* Scroll down to the `Webhook Subscriptions` section (it should be below the `API keys` section)
    * Click `Add an endpoint`
    * The endpoint **must** be `your domain + /api/coinbase`, so for example `https://demo.tbdscripts.com/api/coinbase`
    * Hit the `Save` button
    * Click `Show shared secret` in the section and a popup should open
    * Copy the shared secret by clicking the copy icon and copy it somewhere so you can retrieve it later.

### Setting up in Cosmo
* Head to your Cosmo instance's management panel
* Go to the `Settings` page and go to the `Store` tab
* Open up the `Coinbase` section
    * Paste ur API key into the `Coinbase API Key` input
    * Paste ur shared secret into the `Coinbase Shared Webhook Secret` input
    * Enable the gateway by checking the checkbox

You are now able to accept crypto payments within your Cosmo donation store.