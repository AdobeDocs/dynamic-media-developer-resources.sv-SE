---
description: Hämtar en användares medlemskap i en företagsmatris.
seo-description: Hämtar en användares medlemskap i en företagsmatris.
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Scene7 Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | Nej | Handtaget till användaren vars medlemskap du vill få. |

**Utdata (getCompanyMembershipReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`membershipArray`*` | `types:CompanyMembershipArray` | Ja | En matris med företagsmedlemskap. |

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

