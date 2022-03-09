---
description: Tar bort en egenskapsuppsättningstyp och dess associerade egenskapsuppsättning och egenskaper.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# deletePropertySetType{#deletepropertysettype}

Tar bort en egenskapsuppsättningstyp och dess associerade egenskapsuppsättning och egenskaper.

Syntax

## Auktoriserade användartyper {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-1c8973f5d35f44b4a6a483a41609e455}

**Indata (deletePropertySetTypeParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | Referensen till egenskapsuppsättningstypen som ska tas bort. |

**Utdata (deletePropertySetTypeParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-85faa2e3411a4e23aa6489037f7ce078}

I det här kodexemplet används typens handtag som ett fält i `deletePropertySetTypeParam` skickas till IPS-webbtjänstservern för att egenskapsuppsättningstypen ska kunna tas bort.

**Begäran**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Svar**

Ingen.
