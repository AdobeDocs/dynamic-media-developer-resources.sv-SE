---
description: Skapa eller redigera en grupp.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

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
| companyHandle | `xsd:string` | Ja | Referensen till företaget med gruppen som du vill spara. |
| groupHandle | `xsd:string` | Nej | Referensen till gruppen. |
| name | `xsd:string` | Ja | Gruppnamn. |
| isSystemDefined | `xsd:boolean` | Ja | `false` är standard. |

**Utdata (saveGroupReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| groupHandle | `xsd:string` | Ja | Grupphandtag. |

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
