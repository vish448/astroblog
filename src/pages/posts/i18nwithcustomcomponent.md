---
layout: ../../layouts/MarkdownPostLayout.astro
title: How to add lang option in your custom components.
author: Vishang Soni
description: "How can you add basic language options for dialog fields in your custom components. "
image:
    url: "https://docs.astro.build/assets/arc.webp"
    alt: "Adding lang option with your custom component."
pubDate: '2024-03-14'
tags: ["astro", "blogging", "aem", "i18n", "D4"]
---


## How to add language option with custom component using CRXDE
***Scenario*** Adding three language option with your custome component. ***English***, ***Spanish*** and ***French***.

Create **i18n** folder in your component.
Create ***Subfolders*** for each languages within ***i18n***
**en**
**es**
**fr**
Component structure will look like this 👇

![i18n base folder structure](./images/i18nbasefolderstructure.png "i18n base folder structure")

Add Mixins.. to these folders with **type** ***mix:language***
![add mixins to lang folder](./images/addmixins.png "Add mixins to lang folder")

After adding mixins. Add a property called ***jcr:language*** with language ***iso code*** i.e **french it will be fr**

Within those folder **create node** with exect same name as an item in your component with ***primaryType: sling:MessageEntry***
Now add two properties
1. sling:key
2. sling:message
Sling:key is ***same*** for all language and change the ***sling:message*** properties with your desire custom value in each language.
![key and message property](./images/addkeyandmessageproperty.png "add key and message propeties")

**Test**
Change the prefered language from profile->prefrences and check in the component weather the lang is chages to your custom meesage attached to the lanaguage.