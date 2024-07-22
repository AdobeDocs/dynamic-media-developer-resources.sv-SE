---
title: Fokusmarkering
description: Markering av indatafokus som visas runt det fokuserade elementet i användargränssnittet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
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

**CSS-egenskaper för fokus**

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
