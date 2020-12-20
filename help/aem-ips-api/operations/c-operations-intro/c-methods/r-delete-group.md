---
description: Tar bort en grupp.
seo-description: Tar bort en grupp.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# deleteGroup{#deletegroup}

Tar bort en grupp.

Syntax

## Auktoriserade användartyper {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-42775102ec724c36ae5241eea1a00b8e}

**Indata (deleteGroupParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som tillhör gruppen som du vill ta bort. |
| ` *`groupHandle`*` | `xsd:string` | Ja | Referensen till gruppen som du vill ta bort. |

**Utdata (deleteGroupParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Den här exempelkoden tar bort en grupp från ett företag. Den kräver en gruppreferens som du måste hämta från en annan åtgärd.

**Begäran**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Svar**

Ingen.
