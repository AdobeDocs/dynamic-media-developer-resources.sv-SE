---
description: Hämtar en array med medlemmar som finns i en bilduppsättning.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# getImageSetMembers{#getimagesetmembers}

Hämtar en array med medlemmar som finns i en bilduppsättning.

Syntax

## Auktoriserade användartyper {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Kräver läsåtkomst till bilden och medlemsuppsättningsresursen.

## Parametrar {#section-a67ba98095574533980997c83ceaa316}

**Indata (getImageSetMembersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget som innehåller bilduppsättningen. |
| assetHandle | `xsd:string` | Ja | Resurshandtaget för bilduppsättningen. |

**Utdata (getImageSetMembersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | Nej | Array med medlemmar i bilduppsättningen. |

## Exempel {#section-888a9a78033346f39b171229de93dfa0}

Detta kodexempel returnerar specifika bilduppsättningsmedlemmar. Svaret returnerar en tom array.

**Begäran**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Svar**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```
