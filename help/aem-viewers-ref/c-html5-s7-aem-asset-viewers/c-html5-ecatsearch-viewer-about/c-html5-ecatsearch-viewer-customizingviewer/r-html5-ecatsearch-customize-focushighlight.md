---
description: Markering av indatafokus som visas runt det fokuserade elementet i användargränssnittet.
seo-description: Markering av indatafokus som visas runt det fokuserade elementet i användargränssnittet.
seo-title: Fokusmarkering
solution: Experience Manager
title: Fokusmarkering
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Fokusmarkering{#focus-highlight}

Markering av indatafokus som visas runt det fokuserade elementet i användargränssnittet.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

Fokusmarkeringens utseende styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer *:focus
```

**CSS-egenskaper för fokusmarkeringen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kontur  </span> </p> </td> 
   <td colname="col2"> <p> Fokusmarkeringsstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Om du vill inaktivera standardmarkeringen för webbläsarfokus för alla element i visningsprogrammets användargränssnitt lägger du till följande CSS-väljare i visningsprogrammets formatmall:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

