---
description: Konfigurationsattribut för Interactive Video Viewer.
seo-description: Konfigurationsattribut för Interactive Video Viewer.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut för Interactive Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral</span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. När den anges till <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> vänster</span> eller <span class="codeph"> höger</span>, rullas panelen ut i den angivna riktningen utan någon ytterligare kontroll av gränserna, vilket kan leda till att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> fit-vertical</span> flyttar komponenten först baspanelspositionen till botten av SocialShare och försöker att rulla ut panelen i någon av följande riktningar från en sådan basplats: nerifrån, höger, vänster. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepar utrullningsförsöken från översta, högra och vänstra riktningen. </p> <p>När den är inställd på <span class="codeph"> fit-ateral</span>, använder komponenten en liknande logik, men flyttar basen till höger först, och försöker till höger, nedåt och uppåt. Sedan flyttas basen till vänster och leder fram till vänster, nedåt och uppåt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

