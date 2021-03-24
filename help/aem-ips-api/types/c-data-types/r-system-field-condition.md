---
description: Ett sökvillkor för systemfält för åtgärden searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# SystemFieldCondition{#systemfieldcondition}

Ett sökvillkor för systemfält för åtgärden searchAssets.

För unära jämförelser skickar du exakt ett värde ( `boolVal`, `longVal`, `doubleVal` eller `dateVal`) beroende på systemfältstypen. För sökintervall skickar du parametrarna `min<Type>` och `max<Type>` och skickar `op` värdet `Between` eller `NotBetween`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`fält`*` | `xsd:string` | Val av systemfält för resurssökning. |
| `*`op`*` | `xsd:string` | Välj mellan operatorer för strängjämförelse. |
| `*`value`*` | `xsd:string` | Värde att testa mot. |
| `*`boolVal`*` | `xsd:boolean` | Booleskt jämförelsevärde. |
| `*`longVal`*` | `xsd:long` | Långt jämförelsevärde. |
| `*`minLong`*` | `xsd:long` | Nedre gräns för långt intervall. |
| `*`maxLong`*` | `xsd:long` | Övre gräns för långt intervall. |
| `*`doubleVal`*` | `xsd:double` | Dubbelt jämförelsevärde. |
| `*`minDouble`*` | `xsd:double` | Nedre gräns för dubbelintervall. |
| `*`maxDouble`*` | `xsd:double` | Övre gräns för dubbelintervall. |
| `*`dateVal`*` | `xsd:dateTime` | Datumjämförelsevärde. |
| `*`minDate`*` | `xsd:dateTime` | Minsta datumintervall. |
| `*`maxDate`*` | `xsd:dateTime` | Högsta datumintervall. |

## Exempel {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

