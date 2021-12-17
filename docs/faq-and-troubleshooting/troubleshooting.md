---
id: troubleshooting
title: Troubleshooting
---

# ⁉ Troubleshooting

All issues we think you could run into are laid out below with the necessary steps to resolve the issue.

***

### I'm getting an HTML 406 Error, How do I fix this? <a href="#e1fa3327-bba8-45cb-a0c4-ad40a2c5ea91" id="e1fa3327-bba8-45cb-a0c4-ad40a2c5ea91"></a>

{% embed url="https://www.youtube.com/watch?v=83Jcj2lDxaA" %}

***

### My Discord Widget is causing Cosmo to error! <a href="#ad9bc274-32ac-4cb4-ae29-b66139b67e38" id="ad9bc274-32ac-4cb4-ae29-b66139b67e38"></a>

Please make sure that you have **enabled** the "[Discord Widget](https://blog.discord.com/add-the-discord-widget-to-your-site-d45ffcd718c6)" in your Discord server.

You can do this by following the steps outlined below:

1. Open Your Discord "Server Settings"
2. Navigate to the "Widget" tab located on the left
3. Check the "Enable Server Widget" slider on the top of the page.
4. Open your Management page on Cosmo.
5. Press "Clear Cache"
6. Refresh your page/browser
7. Enjoy

If for some reason you can't enter the management panel and need to remove the widget fo the following.

1. Open PHPMyAdmin (Or any other MySQL Database viewer)
2. Head into the database used for Cosmo.
3. find the "key" named "discord\_widget\_enbled".
4. Set the change the "value" from 1 to 0 and save.

***

### My Server isn't showing up \&or isn't showing the correct details! <a href="#0583f754-dab9-42a6-a136-7ab74e3408a3" id="0583f754-dab9-42a6-a136-7ab74e3408a3"></a>

Make sure you have the following requirements enabled for the steam stats to be grabbed. If you are unsure please contact your host Provider.

* GMP PHP Module \&or 64-bit PHP
* UDP Connections ENABLED

***

### "No Such File or Directory" / "File Get Contents" Errors. <a href="#0ef4b577-be65-4378-a6b4-e5ea29090318" id="0ef4b577-be65-4378-a6b4-e5ea29090318"></a>

This simply means that you have installed cosmo into the wrong working directory or that you need to clear your browser cache.

***

### CloudFlare SSL & Links <a href="#cac0c6d1-fd8f-4113-b431-f45bdd2b43e5" id="cac0c6d1-fd8f-4113-b431-f45bdd2b43e5"></a>

If you are using \&or want to use Cloudflare S:on your website follow the following steps to ensure everything runs smoothly.

* Make sure SSL/TLS is set to FULL SSL.
* Enable Always Use HTTPS.
* Enable Automatic HTTPS Reqrites

***

#### Existing Directory not working. <a href="#7cbb551b-6a6a-4d9b-86fc-5b928461ae62" id="7cbb551b-6a6a-4d9b-86fc-5b928461ae62"></a>

There are a few steps that you'll need to complete in order to get those directories to work again. It's very easy and will only take a few seconds.

**Steps:**

1. Navigate to the directory that is not visible.
2. create a file within the directory called `.htaccess`.
3. Open the file and paste the following code within the new file `RewriteEngine off`.
4. Save the file.
5. Your directory should now be working.

**YOU WILL HAVE TO REPEAT STEPS 1-4 FOR EVERY DIRECTORY THAT IS NOT WORKING.**

***

### My Steam API Key is invalid!

Please make sure that you have a valid [Steam API Key](https://steamcommunity.com/dev/apikey)

You can replace your old Steam API Key by following the steps outlined below:

1. Open your database for cosmo.
2. Go into the configurations table.
3. Look for a column with the name `steam_api_key`.
4. Change the value of the column to your new Steam API Key.
5. Go into your files for cosmo and delete the data folder in `storage/framework/cache`.
6. You should now be able to login.
