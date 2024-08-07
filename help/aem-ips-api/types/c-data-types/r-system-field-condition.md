---
description: Ett sökvillkor för systemfält för åtgärden searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Ett sökvillkor för systemfält för åtgärden searchAssets.

För unära jämförelser skickar du exakt ett värde ( `boolVal`, `longVal`, `doubleVal` eller `dateVal`) beroende på systemfältstypen. För sökintervall skickar du parametrarna `min<Type>` och `max<Type>` och skickar värdet `op` `Between` eller `NotBetween`.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| fält | `xsd:string` | Val av systemfält för resurssökning. |
| op | `xsd:string` | Välj mellan operatorer för strängjämförelse. |
| value | `xsd:string` | Värde att testa mot. |
| boolVal | `xsd:boolean` | Boolesk jämförelse. |
| longVal | `xsd:long` | Long comparison value. |
| minLong | `xsd:long` | Nedre gräns för långt intervall. |
| maxLong | `xsd:long` | Övre gräns för långt intervall. |
| doubleVal | `xsd:double` | Dubbel jämförelse. |
| minDouble | `xsd:double` | Nedre gräns för dubbelintervall. |
| maxDouble | `xsd:double` | Övre gräns för dubbelintervall. |
| dateVal | `xsd:dateTime` | Datumjämförelse. |
| minDate | `xsd:dateTime` | Minsta datumintervall. |
| maxDate | `xsd:dateTime` | Maximalt datumintervall. |

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
