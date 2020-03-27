---
description: Anger riktningen på bildruteanimeringen för knappbehållaren.
seo-description: Anger riktningen på bildruteanimeringen för knappbehållaren.
seo-title: FavoriterMenu.hållning
solution: Experience Manager
title: FavoriterMenu.hållning
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoriterMenu.hållning{#favoritesmenu-bearing}

Anger riktningen på bildruteanimeringen för knappbehållaren.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-ateral</span> </p> </td> 
   <td colname="col2"> <p> När den är inställd på <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> vänster</span>eller <span class="codeph"> höger</span>, rullas panelen ut i den angivna riktningen utan någon extra gränskontroll, vilket resulterar i att panelen klipps av en extern behållare. </p> <p>När den är inställd på <span class="codeph"> justerbart lodrätt</span>flyttar komponenten först baspanelspositionen till nederkanten av Favoriter-menyn och försöker att rulla ut panelen i någon av följande riktningar från den här basplatsen: nerifrån, höger, vänster. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till överkanten och upprepa utrullningsförsök från överkanten, höger och vänster riktning. </p> <p>När komponenten är inställd på <span class="codeph"> "fit-ateral</span>" använder den en liknande logik. Basen flyttas först åt höger och försöker åt höger, nedåt och uppåt. Sedan flyttas basen till vänster och leder genom att försöka vänster, ned och upp. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
