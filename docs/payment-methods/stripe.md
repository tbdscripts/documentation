---
id: stripe
title: Stripe
---

# 💳 Stripe

Cosmo supports [Stripe](https://stripe.com) as a payment method. While we don't promote it as our primary payment method, we highly recommend using it over PayPal. The setup is similar to PayPal's but involves a few different steps. Let's get at it!

## Setting up Stripe
Setting up Stripe is fairly easy, and only involves a couple steps. 

### Stripe Dashboard Setup
:::info
We will not be giving help with setting up your account. This includes signing up, activating your account, etc.
On the other hand, we do ofcourse give support with failing webhooks and packages not being delivered.
:::

* Head over to the [Stripe Dashboard](https://dashboard.stripe.com)
* Log in or create an account
* Stripe will prompt you to make a merchant account, if you do not already have one
* Optional: switch to live data if you are not testing the integration (top right)
* Head to the developer dashboard (button top right of the dashboard)
* Head to the `API keys` tab
* Copy the publishable key and the secret key (you have to reveal the secret key first by clicking it) to a location where you can retrieve it later.
    * The publishable key starts with `pk_`
    * The secret key starts with `sk_`
* Head to the `Webhooks` tab
* Click `Add endpoint` on the top right of the page
    * As Endpoint URL you will use `your domain + /api/stripe` so for example `https://demo.tbdscripts.com/api/stripe` **THIS IS A VITAL PART**
    * If you wish you can add a description, it's optional however
    * Leave the version as default
    * As for the events, you'd want to select these: `checkout.session.completed` and `charge.dispute.created`
    * Create the endpoint by clicking `Add endpoint`
* Click on the webhook/endpoint you've just created, it will take you to its details
    * Reveal the signing secret and copy it to a place where you can retrieve it later.

You've now gotten all the details you need from the Stripe Dashboard.
If you wish you can take a look around the dashboard, it has quite some nice statistics which you can later use to track payments, monthly revenue, etc.
But for now let's get it setup into Cosmo!

### Cosmo Setup
* Head to your Cosmo instance's Management Panel
* Go to the `Settings` page
* Click on the `Store` tab and open the `STRIPE` category
    * Fill in the `Stripe Secret Key`, this is the one starting with `sk_`
    * Fill in the `Stripe Public Key`, this is the one starting with `pk_`
    * Fill in the `Stripe Webhook Secret`, this one starts with `whsec_`
* Enable the gateway by checking the checkbox
* Enable the payments methods you want

:::caution
You can not blindly add payment methods as you go, they need to be enabled and setup in your Stripe dashboard.
:::