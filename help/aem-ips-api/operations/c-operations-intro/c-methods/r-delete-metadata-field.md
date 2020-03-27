---
description: Tar bort ett företags metadatafält.
seo-description: Tar bort ett företags metadatafält.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som innehåller metadatafältet som ska tas bort. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Referensen till metadatafältet som ska tas bort. |

**Utdata (deleteMetadataFieldParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Det här kodexemplet tar bort ett företags metadatafält. Det använder företagshandtaget och metadatahandtaget som fält i den `deleteMetadataFieldParam` som skickas till IPS-webbtjänstservern för att utföra den här åtgärden.

**Begäran**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Svar**

Ingen.0
