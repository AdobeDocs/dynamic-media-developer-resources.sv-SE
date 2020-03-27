---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.stånd
solution: Experience Manager
title: SocialShare.stånd
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SocialShare.stånd{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral </span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. </p> <p> När den är inställd på <span class="codeph"> upp </span>, <span class="codeph"> ned </span>, <span class="codeph"> vänster </span>eller <span class="codeph"> </span>höger, rullas panelen ut i en viss riktning utan någon ytterligare gränskontroll. Det här beteendet kan leda till att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> justerad lodrät </span>flyttar komponenten först baspanelspositionen till nederkanten av SocialShare och försöker att rulla ut panelen antingen från nederkanten, höger eller vänster, från den här basplatsen. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepa utrullningsförsöken från överkanten, höger och vänster riktning. </p> <p>När komponenten är inställd på <span class="codeph"> "fit-ateral" </span>använder den en liknande logik som med"fit-vertical", men i stället flyttas basen till höger, nedåt och uppåt och nedåt, och sedan flyttas basen till vänster, vilket försöker vänster, nedåt och uppåt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-8e843b967237426e9a8b3cd0f27b9820}

Valfritt.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Exempel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
