---
description: Returnerar information om ett företags struktur (antal filer osv.).
seo-description: Returnerar information om ett företags struktur (antal filer osv.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag vars diskanvändning du vill erhålla. |

**Utdata (getDiskUsageReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`discUsageArray`*` | `types:DiskUsageArray` | Ja | Matris med företagsdiskanvändning. |

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

