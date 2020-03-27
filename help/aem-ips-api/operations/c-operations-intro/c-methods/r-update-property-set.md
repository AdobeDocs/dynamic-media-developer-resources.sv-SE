---
description: Använder en egenskapsarray för att uppdatera en egenskapsuppsättning.
seo-description: Använder en egenskapsarray för att uppdatera en egenskapsuppsättning.
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
topic: Scene7 Image Production System API
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`setHandle`*` | `xsd:string` | Ja | Hantera till egenskapsuppsättningen. |
| ` *`replaceProperties`*` | `xsd:string` | Nej | Ange som `true` ska ersätta egenskaper. |
| ` *`propertyArray`*` | `types:PropertyArray` | Ja | Array med uppdaterade egenskaper för egenskapsuppsättningen. |

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
