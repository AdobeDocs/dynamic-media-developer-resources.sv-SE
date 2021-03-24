---
description: Hämtar egenskapsuppsättningstyperna som är associerade med det angivna företaget eller globala egenskapsuppsättningstyper om inget företag anges.
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# getPropertySetTypes{#getpropertysettypes}

Hämtar egenskapsuppsättningstyperna som är associerade med det angivna företaget eller globala egenskapsuppsättningstyper om inget företag anges.

Syntax

## Auktoriserade användartyper {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Indata (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4">Referensen till företaget som egenskapsuppsättningstyperna är associerade med. <p>Utelämna om du vill returnera globala egenskapsuppsättningstyper. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (getPropertySetTypesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Ja | En array med egenskapsuppsättningstyper som är associerade med det angivna företaget, eller globala egenskapsuppsättningstyper om inget företag har angetts. |

## Exempel {#section-280c406a90864409856aee44d4069a52}

**Begäran**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Svar**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

