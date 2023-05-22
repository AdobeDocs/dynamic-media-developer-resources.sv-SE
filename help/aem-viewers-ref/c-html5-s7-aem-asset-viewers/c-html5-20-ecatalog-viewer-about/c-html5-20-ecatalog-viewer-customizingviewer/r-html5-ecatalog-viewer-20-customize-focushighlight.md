---
title: Fokusmarkering
description: Markering av indatafokus som visas runt det fokuserade elementet i användargränssnittet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
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
   <td colname="col1"> <p> <span class="codeph"> kontur </span> </p> </td> 
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
