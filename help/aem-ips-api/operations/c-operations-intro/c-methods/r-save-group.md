---
description: Skapa eller redigera en grupp.
seo-description: Skapa eller redigera en grupp.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveGroup{#savegroup}

Skapa eller redigera en grupp.

Syntax

## Auktoriserade användartyper {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-743610e98dd5494baffcbad6401038eb}

**Indata (saveGroupParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget med gruppen som du vill spara. |
| ` *`groupHandle`*` | `xsd:string` | Nej | Referensen till gruppen. |
| ` *`name`*` | `xsd:string` | Ja | Gruppnamn. |
| ` *`isSystemDefined`*` | `xsd:boolean` | Ja | `false` är standard. |

**Utdata (saveGroupReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Ja | Gruppreferens. |

## Exempel {#section-26eee227ff1f4edabb7fa1240b4d9999}

Det här kodexemplet skapar en grupp som tillhör ett visst företag. Om gruppen redan finns sparas den med de parametervärden som du anger.

**Begäran**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Svar**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```

