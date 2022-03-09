---
description: Tar bort ett företags metadatafält.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# deleteMetadataField{#deletemetadatafield}

Tar bort ett företags metadatafält.

Syntax

## Auktoriserade användartyper {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-73f12a30cc4340b6b32dd11effd5195e}

**Indata (deleteMetadataFieldParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Referensen till företaget som innehåller metadatafältet som ska tas bort. |
| fieldHandle | `xsd:string` | Ja | Referensen till metadatafältet som ska tas bort. |

**Utdata (deleteMetadataFieldParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Det här kodexemplet tar bort ett företags metadatafält. Det använder företagshandtaget och metadatahandtaget som fält i `deleteMetadataFieldParam` skickas till IPS Web Services-servern för att utföra den här åtgärden.

**Begäran**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Svar**

Ingen.0
