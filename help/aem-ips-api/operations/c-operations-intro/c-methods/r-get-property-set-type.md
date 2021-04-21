---
description: Hämtar en egenskapsuppsättningstyp med hjälp av ett handtag för ett företag och namnet på egenskapsuppsättningstypen. Den får en typstruktur med handtaget till typen samt egenskapstypen.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# getPropertySetType{#getpropertysettype}

Hämtar en egenskapsuppsättningstyp med hjälp av ett handtag för ett företag och namnet på egenskapsuppsättningstypen. Den får en typstruktur med handtaget till typen samt egenskapstypen.

Syntax

## Auktoriserade användartyper {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-c9a53400c44744668bd7915f72d2bf3d}

**Indata (getPropertySetTypeParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nej | Handtaget till företaget. Valfritt eftersom en egenskapsuppsättningstyp kan tillhöra flera företag. |
| `*`name`*` | `xsd:string` | Ja | Typnamn för egenskapsuppsättning. |

**Utdata (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PropertySetType</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Typstrukturen som innehåller en: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Handtag. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Typnamn. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Egenskapstyp. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Värde som anger om typen tillåter flera egenskapstyper. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-1b57199415e34a8fa449f864f8895b14}

Detta kodexempel returnerar en egenskapsuppsättningstyp efter namn.

**Begäran**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Svar**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

