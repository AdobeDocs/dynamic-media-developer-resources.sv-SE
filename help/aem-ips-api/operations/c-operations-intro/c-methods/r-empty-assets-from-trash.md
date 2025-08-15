---
title: emptyAssetsFromTrash
description: Tömmer resurser från IPS-papperskorgen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Tömmer resurser från IPS-papperskorgen.

Assets bor i papperskorgen tills de töms manuellt eller tills de tippar ut ur papperskorgen. Om de töms manuellt bor de i papperskorgen till nästa rensningsjobb (normalt på kvällen) när de till slut tömts från systemet. Om de kommer ut i papperskorgen rensas resurserna bort som en del av samma rensningsaktivitet. Timeout-värdet kan konfigureras (standardvärdet är 7 dagar).

## Auktoriserade användartyper {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-8e1fb0ee3aae453581e99ef76e298569}

**Indata (emptyAssetsFromTrashParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | xsd:string | Ja | Handtaget till det företag som äger tillgångarna. |
| assetHandleArray | typer:HandleArray | Ja | Arrayen med handtag som representerar objekt som ska tömmas från papperskorgen. |

**Utdata (emptyAssetsFromTrashParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| successCount | xsd:Int | Ja | Antalet resurser som tömts från papperskorgen. |
| warningCount | xsd:Int | Ja | Antalet varningar som genereras när åtgärden försökte tömma resurser från papperskorgen. |
| errorCount | xsd:Int | Ja | Antalet fel som genererades när åtgärden försökte tömma resurser från papperskorgen. |
| warningDetailArray | typer:AssetOperationFaultArray | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tömma dem från papperskorgen. |
| errorDetailArray | typer:AssetOperationFaultArray | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tömma dem från papperskorgen. |

## Exempel {#section-6154a873b6c342bf92e2036280cafdcf}

I det här kodexemplet används företagets handtag och en tillgångshandtag som innehåller handtag till de tillgångar som ska tömmas från papperskorgen.

**Begäran**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Svar**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
