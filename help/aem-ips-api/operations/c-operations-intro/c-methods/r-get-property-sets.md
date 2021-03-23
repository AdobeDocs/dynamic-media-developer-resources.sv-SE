---
description: Hämtar egenskapsuppsättningar som är associerade med ett typhandtag.
seo-description: Hämtar egenskapsuppsättningar som är associerade med ett typhandtag.
seo-title: getPropertySets
solution: Experience Manager
title: getPropertySets
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# getPropertySets{#getpropertysets}

Hämtar egenskapsuppsättningar som är associerade med ett typhandtag.

Syntax

## Auktoriserade användartyper {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-d8da2847e77e4a95a4441d9848cac775}

**Indata (getPropertySetsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | Referensen till egenskapsuppsättningstypen. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Ja | Den primära ägaren av data som är bundna till databasobjektet. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | Nej | En valfri sekundär dataägare. |

**Utdata (getPropertySetsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`setArray`*` | `types:PropertySetArray` | Ja | Array med egenskapsuppsättningar. |

## Exempel {#section-1358af974eab4259864910337a6f0bd2}

Detta kodexempel returnerar egenskapsuppsättningar för sin primära ägare, som anges av ett typhandtag.

**Begäran**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Svar**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

