---
description: Tar bort taggfältsvärden från ordlistan för ett taggfält.
seo-description: Tar bort taggfältsvärden från ordlistan för ett taggfält.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Tar bort taggfältsvärden från ordlistan för ett taggfält.

## Auktoriserade användartyper {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-5db64a6ae238426395bc760b83587260}

**Indata (deleteTagFieldValuesParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget för det företag som innehåller taggfältet. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Handtaget för det taggfält som ska ändras. |
| ` *`valueArray`*` | `types:StringArray` | Ja | En array med taggvärden som ska tas bort från fältets ordlista. |

**Utdata (deleteTagFieldValuesParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-92f9e575a6da491caa09e264b4d6ee55}

**Begäran**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Svar**

Ingen.
