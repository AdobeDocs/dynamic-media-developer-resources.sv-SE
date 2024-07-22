---
description: Anger riktningen på bildruteanimeringen för knappbehållaren.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Anger riktningen på bildruteanimeringen för knappbehållaren.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> upp|ned|vänster|höger|anpassa-vertikalt|anpassa-lateralt</span> </p> </td> 
   <td colname="col2"> <p> När den är inställd på <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> left</span> eller <span class="codeph"> right</span>, rullas panelen ut i angiven riktning utan någon ytterligare gränskontroll, vilket resulterar i att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> fit-vertical</span> flyttar komponenten först baspanelens position till nederkanten av Favoriter-menyn och försöker att rulla ut panelen i någon av följande riktningar från den här basplatsen: bottom, right, left. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till överkanten och upprepa utrullningsförsök från överkanten, höger och vänster riktning. </p> <p>När den är inställd på <span class="codeph"> fit-ateral</span> använder komponenten en liknande logik. Basen flyttas först åt höger och försöker åt höger, nedåt och uppåt. Sedan flyttas basen till vänster och leder genom att försöka vänster, ned och upp. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
