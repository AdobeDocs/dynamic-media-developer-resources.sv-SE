---
description: Skapar en mapp.
seo-description: Skapar en mapp.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createFolder{#createfolder}

Skapar en mapp.

>[!NOTE]
>
>Den nya mappen är underordnad mappen Images, även om du anger en `/` som anger företagets rot.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget |
| ` *`folderPath`*` | `xsd:string` | Ja | Rotmappen som används för att hämta mappar och alla undermappar till lövnivån. Om detta utelämnas används företagsroten. |

**Utdata (createFolderParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ja | Hantering av den nya mappen. |

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

