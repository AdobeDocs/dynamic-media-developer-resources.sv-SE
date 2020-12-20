---
description: Tar bort en egenskapsuppsättningstyp och dess associerade egenskapsuppsättning och egenskaper.
seo-description: Tar bort en egenskapsuppsättningstyp och dess associerade egenskapsuppsättning och egenskaper.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
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
| ` *`typeHandle`*` | `xsd:string` | Ja | Referensen till egenskapsuppsättningstypen som ska tas bort. |

**Utdata (deletePropertySetTypeParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-85faa2e3411a4e23aa6489037f7ce078}

I det här kodexemplet används typens referens som ett fält i `deletePropertySetTypeParam` som skickas till IPS Web services-servern för att ta bort egenskapsuppsättningstypen.

**Begäran**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Svar**

Ingen.
