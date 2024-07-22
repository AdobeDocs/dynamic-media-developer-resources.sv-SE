---
title: createFolder
description: Skapar en mapp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# [!DNL createFolder]{#createfolder}

Skapar en mapp.

>[!NOTE]
>
>Den nya mappen är underordnad mappen Images, även om du anger en `/` som anger roten för företaget.

Syntax

## Auktoriserade användartyper {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till den överordnade mappen.

## Parametrar {#section-c00d8d89cf114886a535056f2a1bf892}

**Indata (createFolder)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget |
| folderPath | `xsd:string` | Ja | Rotmappen som används för att hämta mappar och alla undermappar till lövnivån. Om detta utelämnas används företagsroten. |

**Utdata (createFolderParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| folderHandle | `xsd:string` | Ja | Hantera den nya mappen. |

## Exempel {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Den här exempelkoden skapar en mapp i roten av ett företag. Svaret returnerar referensen för den nyligen skapade mappen.

**Begäran**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Svar**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
