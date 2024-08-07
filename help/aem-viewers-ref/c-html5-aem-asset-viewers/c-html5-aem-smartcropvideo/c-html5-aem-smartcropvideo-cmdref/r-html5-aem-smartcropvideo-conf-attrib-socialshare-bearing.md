---
title: SocialShare.bearing
description: Konfigurationsattribut för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut för visningsprogrammet för smart beskärning.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> upp|ned|vänster|höger|anpassa-vertikalt|anpassa-lateralt</span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. </p> <p> När den är inställd på <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> left</span> eller <span class="codeph"> right</span> rullas panelen ut i en angiven riktning utan en extra gränskontroll, vilket kan leda till att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> fit-vertical</span> flyttar komponenten först baspanelspositionen till nederkanten av SocialShare och försöker att rulla ut panelen nedifrån, till höger eller till vänster från den här basplatsen. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepa rullningsförsök i den övre, högra och vänstra riktningen. </p> <p>När den är inställd på <span class="codeph"> fit-ateral</span> använder komponenten en liknande logik. Basen flyttas dock först åt höger, och sedan visas riktningarna höger, ned och upp, och basen flyttas åt vänster, åt vänster, nedåt och uppåt. </p> </td> 
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
