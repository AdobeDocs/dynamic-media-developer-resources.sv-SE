---
description: Returnerar alla mappar och undermappar med början i mappsökvägen. Svaret getFolders returnerar maximalt 100 000 mappar.
seo-description: Returnerar alla mappar och undermappar med början i mappsökvägen. Svaret getFolders returnerar maximalt 100 000 mappar.
seo-title: getFolders
solution: Experience Manager
title: getFolders
topic: Scene7 Image Production System API
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# getFolders{#getfolders}

Returnerar alla mappar och undermappar med början i mappsökvägen. Svaret getFolders returnerar maximalt 100 000 mappar.

## Syfte med mappar {#section-66e344d5333f42f1b060a0cba25935c3}

Med en mapp kan du ordna undermappar och resurser. Alla mapp- och resursnamn måste vara unika. Mappar och resurser som delar samma namn orsakar en namnområdeskonflikt, även om de finns i olika mapphierarkier.
Syntax

## Auktoriserade användartyper {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läsåtkomst till mappen för att kunna returnera data om den.

## Parametrar {#section-0c1976503eaa418a9226b51667901176}

**Indata (getFoldersParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| ` *`accessUserHandle`*` | `xsd:string` | Nej | Används av administratörer för att personifiera en viss användare. |
| ` *`accessGroupHandle`*` | `xsd:string` | Nej | Filtrera efter en viss grupp. |
| ` *`folderPath`*` | `xsd:string` | Nej | Rotmappen som ska hämta mappar och alla undermappar till lövnivån. Om detta utelämnas används företagsroten. |
| ` *`assetTypeArray`*` | `types:StringArray` | Nej | Returnerar mappar som bara innehåller angivna resurstyper. |
| ` *`responseFieldArray`*` | `types:StringArray` | Nej | Innehåller en lista med fält som du vill inkludera i svaret. |
| ` *`excludeFieldArray`*` | `types:StringArray` | Nej | Innehåller en lista med fält som du vill utesluta från svaret. |

**Utdata (getFoldersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`folderArray`*` | `types:FolderArray` | Nej | En matris med mappar som matchar filtervillkoren. Svaret är begränsat till max 100 000 mappar. |
| ` *`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Exempel {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Detta kodexempel returnerar en array som innehåller alla företagets mappar tillsammans med specifik information om varje mapp.

**Begäran**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Svar**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

