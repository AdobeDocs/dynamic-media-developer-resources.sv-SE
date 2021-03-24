---
description: Tar bort en egenskapsuppsättning och alla associerade egenskaper.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# deletePropertySet{#deletepropertyset}

Tar bort en egenskapsuppsättning och alla associerade egenskaper.

Syntax

## Auktoriserade användartyper {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-e5fc868f69494cf6858e03027db09101}

**Indata (deletePropertySetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | Referensen till egenskapsuppsättningen som ska tas bort. |

**Utdata (deletePropertySetParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-cf319fc8f86a40ab9cbd838b031973fe}

Det här kodexemplet använder uppsättningens referens som ett fält i `deletePropertySetParam` som skickas till IPS Web services-servern för att ta bort egenskapsuppsättningen.

**Begäran**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Svar**

Ingen.
