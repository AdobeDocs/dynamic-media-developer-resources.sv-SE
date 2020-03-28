---
description: Konfigurationsattribut för Video360 Viewer.
seo-description: Konfigurationsattribut för Video360 Viewer.
seo-title: SocialShare.stånd
solution: Experience Manager
title: SocialShare.stånd
topic: Dynamic media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.stånd{#socialshare-bearing}

Konfigurationsattribut för Video360 Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral</span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. </p> <p> När den är inställd på <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> vänster</span>eller <span class="codeph"> höger</span>, rullas panelen ut i en viss riktning utan någon extra gränskontroll, vilket kan leda till att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> justerad lodrät</span>flyttar komponenten först baspanelens position till nederkanten av SocialShare och försöker att rulla ut panelen nedifrån, till höger eller till vänster från en sådan basplats. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepa utrullningsförsök i den övre, högra och vänstra riktningen. </p> <p>När komponenten är inställd på <span class="codeph"> "fit-ateral</span>" använder den en liknande logik. Basen flyttas dock först åt höger, och sedan visas riktningarna höger, ned och upp, och basen flyttas åt vänster, åt vänster, nedåt och uppåt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

