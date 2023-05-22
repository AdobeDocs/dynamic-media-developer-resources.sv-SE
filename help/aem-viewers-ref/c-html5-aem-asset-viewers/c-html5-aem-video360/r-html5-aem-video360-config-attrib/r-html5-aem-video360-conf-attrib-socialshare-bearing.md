---
title: SocialShare.bearing
description: Konfigurationsattribut för Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut för Video360 Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral</span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. </p> <p> När inställt på <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> vänster</span>, eller <span class="codeph"> höger</span>rullas panelen ut i en angiven riktning utan en extra gränskontroll, vilket kan leda till att panelen klipps av en extern behållare. </p> <p>När inställt på <span class="codeph"> anpassa lodrätt</span>, flyttar komponenten först baspanelens position till nederkanten av SocialShare och försöker att rulla ut panelen från nederkanten, höger eller vänster från den här basplatsen. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till överkanten och upprepa rullningsförsök i den övre, högra och vänstra riktningen. </p> <p>När inställt på <span class="codeph"> anpassa-lateralt</span>, använder komponenten en liknande logik. Basen flyttas dock först åt höger, och sedan visas riktningarna höger, ned och upp, och basen flyttas åt vänster, åt vänster, nedåt och uppåt. </p> </td> 
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
