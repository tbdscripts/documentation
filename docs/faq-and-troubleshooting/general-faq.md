---
id: general-faq
title: 💬 General FAQ
---

All general Documentation for configuration not mentioned in other sections

***

### Where can I find the icons? <a href="#12582c8d-dba8-47a4-83ac-24a5e56b2043" id="12582c8d-dba8-47a4-83ac-24a5e56b2043"></a>

You can find all of the Font Awesome icons [here](https://fontawesome.com/icons?d=gallery), Because we are awesome, you have access to all of the icons even including the PRO versions.

### How do I change the language?

To change the default language used by Cosmo, Please follow the outlined steps below:

- Check to see if your language is supported by Cosmo,
- Head into `config/app.php`
- You will find a `'locale'` Key, all you need to do is change the value associated with this key.

Your new value should look similar to this

`'locale' => 'fr',`  -- This is for a french default language

### How do I change the favicon? <a href="#8037fc9f-eb0d-4adc-989a-aadfdd3df29a" id="8037fc9f-eb0d-4adc-989a-aadfdd3df29a"></a>

Favicon is the little image located next to the title on the browser tab.

To change this simply navigate to `/public/img` you will then see an image named "logo.png".

all you have to do is replace this file with an image of your choice.

The image has to be:

* The same name (logo.png)
* 32px X 32px.

### How do I fix my other directories?

There are a few steps that you'll need to complete in order to get those directories to work again. It's very easy and will only take a few seconds.

Steps:
- Navigate to the directory that is not visible.

- Create a file within the directory called .htaccess.

- Open the file and paste the following code within the new file `RewriteEngine off`

- Save the file.

- Your directory should now be working.


**YOU WILL HAVE TO REPEAT STEPS 1-4 FOR EVERY DIRECTORY THAT IS NOT WORKING.**
