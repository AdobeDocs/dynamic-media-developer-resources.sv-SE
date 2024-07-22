---
description: Skapar en bild med flera lager som kan ha flera text- och bildlager.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# createTemplate{#createtemplate}

Skapar en bild med flera lager som kan ha flera text- och bildlager.

Parametern `urlModifier` anger de Image Server-protokollkommandon som lagras i Image Server-katalogen som används före eventuella användardefinierade kommandon på URL:en. Parametern `urlPostApplyModifier` anger protokollkommandon som används efter URL-kommandon, vilket åsidosätter eventuella inställningar som användaren anger.

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
| companyHandle | `xsd:string` | Ja | Företaget som mallen tillhör. |
| folderHandle | `xsd:string` | Ja | Mappreferensen som representerar mappen där mallen finns. |
| name | `xsd:string` | Ja | Mallnamn. |
| type | `xsd:string` | Ja | Malltyp. |
| urlModifier | `xsd:string` | Ja | Anger de Image Server-kommandon som lagras i IS-katalogen och som används före användarkommandon på URL:en. |
| urlPostApplyModifier | `xsd:string` | Nej | Anger protokollkommandon som används efter URL-kommandon, som åsidosätter eventuella inställningar som användaren anger står i konflikt med varandra. |

**Utdata (createTemplateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Referensen till mallen. |

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
