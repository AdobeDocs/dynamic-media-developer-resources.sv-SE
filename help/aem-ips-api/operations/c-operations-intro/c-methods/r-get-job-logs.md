---
description: Hämtar angivna jobbloggar för det valda företaget. Du kan sortera efter tecken, riktning, start- och slutdatum samt antal rader.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# getJobLogs{#getjoblogs}

Hämtar angivna jobbloggar för det valda företaget. Du kan sortera efter tecken, riktning, start- och slutdatum samt antal rader.

Syntax

## Auktoriserade användartyper {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-8cfdc7994da24678a45edcb37e9a2166}

**Indata (getJobLogsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Nej | Företagets handtag. |
| userHandle | `xsd:string` | Nej | Hämtar loggar för jobb som skickats av en viss användare. |
| sortBy | `xsd:string` | Nej | Här kan du välja sorteringsfält. |
| sortDirection | `xsd:string` | Nej | Sorteringsordning (stigande eller fallande). |
| startDate | `xsd:dateTime` | Nej | Datum och tid då jobbloggen startades. Ange tidszonen med begäran för det här fältet. |
| endDate | `xsd:dateTime` | Nej | Datum och tid för slutet av jobbloggen. Ange tidszonen med begäran för det här fältet. |
| numRows | `xsd:int` | Nej | Maximalt antal rader som ska returneras. |

**Utdata (getJobLogsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Ja | Matris med jobbloggar. |

## Exempel {#section-35871c94b4a44559912577efddbc46a6}

Detta kodexempel returnerar IPS-jobbloggar för ett visst företag. Du kan också använda den för att returnera jobbloggar för en viss användare eller företag och användare.

**Begäran**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Svar**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
