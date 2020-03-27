---
description: Byter namn på en resurs.
seo-description: Byter namn på en resurs.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

Byter namn på en resurs.

>[!NOTE]
>
>Parametern `renameFiles` har tagits bort för tidigare versioner och tagits bort från `renameAsset`. Sökvägen för den virtuella filen ändras så att den matchar det nya resursnamnet (med filtillägget bevarat), medan sökvägarna för fysiska filer inte påverkas. API-klienter måste ta bort referenser till den här parametern när de uppdaterar till den nya API-versionen.

## Auktoriserade användartyper {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-ef95a994106841e0ab346dd4cf672258}

**Indata (renameAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som tillgången tillhör. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Referensen till resursen som du vill byta namn på. |
| ` *`newName`*` | `xsd:string` | Ja | Resursens nya namn. |
| ` *`validateName`*` | `xsd:boolean` | Ja | Om resurstypen `validateName` är `true` och resurstypen kräver ett unikt IPS-ID kontrolleras det nya namnet för global unicitet och `renameAsset` ett fel genereras om den inte är unik. |

**Utdata (renameAssetReturn)**

IPS API returnerar inget svar för den här åtgärden. Se beskrivningen av elementet för `<ns1:validateName>` att få information om det här elementet.

## Exempel {#section-a0ddffd62bec42e09069f22ceb486f8a}

Det här kodexemplet byter namn på en resurs

**Begäran**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Svar**

Ingen.
