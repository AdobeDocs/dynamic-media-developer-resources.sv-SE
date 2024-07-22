---
description: Hämtar en användares medlemskap i en företagsmatris.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# getCompanyMembership{#getcompanymembership}

Hämtar en användares medlemskap i en företagsmatris.

Syntax

## Auktoriserade användartyper {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Indata (getCompanyMembershipParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| userHandle | `xsd:string` | Nej | Handtaget till den användare vars medlemskap du vill få. |

**Utdata (getCompanyMembershipReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | Ja | En matris med företagsmedlemskap. |

## Exempel {#section-e4958d104ea344a4a79f57d07b46eba7}

Det här kodexemplet tar en användarreferens och hämtar alla användarens företagsmedlemskap i en array. Svaret har trunkerats av kortfattade skäl.

**Begäran**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Svar**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
