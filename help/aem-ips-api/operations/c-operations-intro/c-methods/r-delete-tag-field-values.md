---
description: Tar bort taggfältsvärden från ordlistan för ett taggfält.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
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
| companyHandle | `xsd:string` | Ja | Handtaget för det företag som innehåller taggfältet. |
| fieldHandle | `xsd:string` | Ja | Handtaget för det taggfält som ska ändras. |
| valueArray | `types:StringArray` | Ja | En array med taggvärden som ska tas bort från fältets ordlista. |

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
