---
description: Tar bort en egenskapsuppsättning och alla associerade egenskaper.
seo-description: Tar bort en egenskapsuppsättning och alla associerade egenskaper.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`setHandle`*` | `xsd:string` | Ja | Referensen till egenskapsuppsättningen som ska tas bort. |

**Utdata (deletePropertySetParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-cf319fc8f86a40ab9cbd838b031973fe}

I det här kodexemplet används uppsättningens handtag som ett fält i den `deletePropertySetParam` som skickas till IPS Web services-servern för att ta bort egenskapsuppsättningen.

**Begäran**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Svar**

Ingen.
