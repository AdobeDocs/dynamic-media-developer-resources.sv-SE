---
description: Använder en egenskapsarray för att uppdatera en egenskapsuppsättning.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# updatePropertySet{#updatepropertyset}

Använder en egenskapsarray för att uppdatera en egenskapsuppsättning.

Syntax

## Auktoriserade användartyper {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Indata (updatePropertySetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| setHandle | `xsd:string` | Ja | Hantera till egenskapsuppsättningen. |
| replaceProperties | `xsd:string` | Nej | Ange `true` om du vill ersätta egenskaper. |
| propertyArray | `types:PropertyArray` | Ja | Array med uppdaterade egenskaper för egenskapsuppsättningen. |

**Utdata (updatePropertySetReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Detta kodexempel uppdaterar en egenskapsuppsättning med egenskaper i egenskapsarrayen.

**Begäran**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Svar**

Ingen.
