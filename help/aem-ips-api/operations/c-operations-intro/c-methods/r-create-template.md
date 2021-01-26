---
description: Skapar en bild med flera lager som kan ha flera text- och bildlager.
seo-description: Skapar en bild med flera lager som kan ha flera text- och bildlager.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Dynamic Media Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# createTemplate{#createtemplate}

Skapar en bild med flera lager som kan ha flera text- och bildlager.

Parametern `urlModifier` anger de Image Server-protokollkommandon som lagras i Image Server-katalogen som används före eventuella kommandon som användaren anger på URL:en. Parametern `urlPostApplyModifier` anger protokollkommandon som används efter URL-kommandon, som åsidosätter eventuella inställningar som användaren anger.

## Auktoriserade användartyper {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Indata (createTemplateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företaget som mallen tillhör. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mappreferensen som representerar mappen där mallen finns. |
| `*`name`*` | `xsd:string` | Ja | Mallnamn. |
| `*`type`*` | `xsd:string` | Ja | Malltyp. |
| `*`urlModifier`*` | `xsd:string` | Ja | Anger de Image Server-kommandon som lagras i IS-katalogen och som används före användarkommandon på URL:en. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nej | Anger protokollkommandon som används efter URL-kommandon, som åsidosätter eventuella inställningar som användaren anger. |

**Utdata (createTemplateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | Referensen till mallen. |

## Exempel {#section-09adb4d2f0c944af875c4463a461f55d}

I det här kodexemplet skapas en mall i en mapp som anges av en referens, med namnet `APIcreateTemplate`, `urlModifier` och `urlPostApplyModifier`. Svaret returnerar referensen till den nya mallen.

**Begäran**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Svar**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```

