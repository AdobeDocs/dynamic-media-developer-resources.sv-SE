---
description: Hämtar egenskapsuppsättningstyperna som är associerade med det angivna företaget eller globala egenskapsuppsättningstyper om inget företag anges.
seo-description: Hämtar egenskapsuppsättningstyperna som är associerade med det angivna företaget eller globala egenskapsuppsättningstyper om inget företag anges.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
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
| ` *`typeArray`*` | `types:PropertySetTypeArray` | Ja | En array med egenskapsuppsättningstyper som är associerade med det angivna företaget, eller globala egenskapsuppsättningstyper om inget företag har angetts. |

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

