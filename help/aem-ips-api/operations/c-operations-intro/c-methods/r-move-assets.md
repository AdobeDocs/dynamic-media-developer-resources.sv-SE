---
description: Flyttar flera resurser oberoende av varandra. Detta uppnås med hjälp av AssetMove-typen som finns i assetMoveArray. Varje AssetMove-fält innehåller en målmapp.
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# moveAssets{#moveassets}

Flyttar flera resurser oberoende av varandra. Detta uppnås med hjälp av AssetMove-typen som finns i assetMoveArray. Varje AssetMove-fält innehåller en målmapp.

Syntax

## Auktoriserade användartyper {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-7d47f663474b41cc83439288ac133cc5}

**Indata (moveAssetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget med resurser som ska flyttas. |
| assetMoveArray | `types:AssetMoveArray` | Ja | En objektflyttningsarray. Den innehåller en resurs och en målmapp för resursen. |

**Utdata (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Antal resurser har flyttats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Antal resurser som genererade varningar när åtgärden försökte flytta dem. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Antal resurser som genererade fel när åtgärden försökte flytta dem. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span> som innehåller: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets som utlöste varningarna. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Varningskoder. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Orsak till varningen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span> som innehåller: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets som orsakade felen. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Felkoder. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Orsak till felen. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Det här kodexemplet flyttar resurser till en specifik plats som anges av `assetMoveArray`. Arrayen innehåller tillgångshandtaget och dess mappreferens. Svaret anger att resurserna flyttades.

**Begäran**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Svar**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```
