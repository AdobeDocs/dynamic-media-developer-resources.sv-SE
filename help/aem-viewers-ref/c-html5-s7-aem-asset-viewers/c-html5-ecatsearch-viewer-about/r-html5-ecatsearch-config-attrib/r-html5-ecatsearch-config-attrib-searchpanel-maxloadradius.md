---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
uuid: 37d58c88-3d45-44d9-9f2c-d616d1077906
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> förinläsare</span></span> </p> </td> 
   <td colname="col2"> <p>Anger beteende för komponentförinläsning. </p> <p>När värdet är <span class="codeph"> -1</span> läses alla miniatyrbilder in samtidigt när komponenten initieras eller resursen ändras. </p> <p> Om <span class="codeph"> 0</span> anges läses endast synliga miniatyrer in. </p> <p>Ange <span class="codeph"><span class="varname"> förinläsare</span></span> för att definiera hur många osynliga rader runt det synliga området som ska förinläsas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-4b7952997f9240e581d21bcdb173f9af}

Valfritt.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Exempel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
