---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral  </span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. </p> <p> När den anges till <span class="codeph"> upp </span>, <span class="codeph"> ned </span>, <span class="codeph"> vänster </span> eller <span class="codeph"> höger </span>, rullas panelen ut i en angiven riktning utan någon ytterligare gränskontroll. Det här beteendet kan leda till att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> fit-vertical </span> flyttar komponenten först baspanelens position till botten av SocialShare och försöker att rulla ut panelen antingen från nederkanten, höger eller vänster, från den här basplatsen. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepa utrullningsförsöken från överkanten, höger och vänster riktning. </p> <p>När den är inställd på <span class="codeph"> fit-lateral </span> använder komponenten en liknande logik som med fit-vertikal, men flyttar i stället basen till höger, som först provar åt höger, nedåt och uppåt, och flyttar sedan basen till vänster och försöker åt vänster, nedåt och uppåt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-8e843b967237426e9a8b3cd0f27b9820}

Valfritt.

## Standard {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Exempel {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
