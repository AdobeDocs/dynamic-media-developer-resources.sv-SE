---
description: 'null'
seo-description: 'null'
seo-title: Innehållsförteckning.hållning
solution: Experience Manager
title: Innehållsförteckning.hållning
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# Innehållsförteckning.hållning{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-ateral|fit-vertikal</span> </p> </td> 
   <td> <p> Styr riktningen på den nedrullningsbara panelens utseende. </p> <p>När den är inställd på <span class="codeph"> justerad lodrät</span>flyttar komponenten först baspanelens position till nederkanten av dess knapp och försöker rulla ut panelen antingen till höger eller till vänster från basplatsen. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position uppåt och upprepa utrullningsförsök i höger och vänster riktning. </p> <p>När den är inställd på <span class="codeph"> "fit-ateral</span>" använder komponenten en liknande logik, men flyttar basen till höger först och försöker upp och ned i riktningen. Sedan flyttas basen åt vänster och leder nedåt och uppåt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Anger fördröjning i sekunder för den nedrullningsbara timer som döljer panelen när en användare är inaktiv. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-55436ddd78b04f538dbb9a7a8463feae}

Valfritt.

## Standard {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Exempel {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
