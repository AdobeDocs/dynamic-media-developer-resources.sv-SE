---
description: Tar bort ett bildschema.
seo-description: Tar bort ett bildschema.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
topic: Scene7 Image Production System API
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteImageMap{#deleteimagemap}

Tar bort ett bildschema.

Syntax

## Auktoriserade användartyper {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-28de12bab79045a5977c68855e37ae3d}

**Indata (deleteImageMapParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget som innehåller bildschemat som ska tas bort. |
| ` *`imageMapHandle`*` | `xsd:string` | Ja | Handtaget till bildschemat som ska tas bort. |

**Utdata (deleteImageMapParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Det här kodexemplet tar bort ett bildschema från ett företag. Du måste hämta handtaget för bildschemat från en annan åtgärd.

**Begäran**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Svar**

Ingen
