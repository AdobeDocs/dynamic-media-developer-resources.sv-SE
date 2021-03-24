---
description: Returnerar information om ett företags struktur (antal filer osv.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# getDiskUsage{#getdiskusage}

Returnerar information om ett företags struktur (antal filer osv.).

## Auktoriserade användartyper {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Indata (getDiskUsageParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars diskanvändning du vill erhålla. |

**Utdata (getDiskUsageReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`discUsageArray`*` | `types:DiskUsageArray` | Ja | Matris med företagsdiskanvändning. |

## Exempel {#section-cb16a97badc94076ad5da277db5ed16a}

Namnet på denna begäran är vilseledande. I stället för att bara returnera ett skalärvärde som återspeglar hur mycket diskutrymme ett företag använder, får det även annan information om ett företags struktur.

**Begäran**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Svar**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

