---
description: Hämtar alla systemegenskaper i en enda begäran.
seo-description: Hämtar alla systemegenskaper i en enda begäran.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSystemProperties{#getsystemproperties}

Hämtar alla systemegenskaper i en enda begäran.

Syntax

## Auktoriserade användartyper {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parametrar {#section-b2a4fb7068424223aec87c50f0586d73}

**Indata (getSystemPropertiesParam)**

Ingen.

**Utdata (getSystemPropertiesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`propertyArray`*` | `types:PropertyArray` | Ja | En array med systemegenskaper. |

## Exempel {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Detta kodexempel returnerar en array med systemegenskaper. Svaret trunkeras för att vara kortfattat.

**Begäran**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Svar**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

