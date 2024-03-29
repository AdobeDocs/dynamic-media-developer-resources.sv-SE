---
description: Tar bort ett bildformat. Hämta bildformatshandtaget från saveImageFormat.
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# deleteImageFormat{#deleteimageformat}

Tar bort ett bildformat. Hämta bildformatshandtaget från saveImageFormat.

Syntax

## Auktoriserade användartyper {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-462c05d9aad746ee8d2be0656041b693}

**Indata (deleteImageFormatParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget som innehåller det bildformat som du vill ta bort. |
| imageFormatHandle | `xsd:string` | Ja | Handtaget till det bildformat som du vill ta bort. |

**Utdata (deleteImageFormatParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

Det här kodexemplet tar bort ett bildformat från ett företag. Hämta bildformatshandtaget från en annan åtgärd.

**Begäran**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**Svar**

Ingen.

**Relaterat ämne:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
