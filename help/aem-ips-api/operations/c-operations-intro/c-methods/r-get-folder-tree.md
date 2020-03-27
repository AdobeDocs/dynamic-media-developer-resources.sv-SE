---
description: Returnerar mappar och undermappar i en hierarkisk trädstruktur. Svaret getFolderTree är begränsat till högst 100 000 mappar
seo-description: Returnerar mappar och undermappar i en hierarkisk trädstruktur. Svaret getFolderTree är begränsat till högst 100 000 mappar
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Scene7 Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getFolderTree{#getfoldertree}

Returnerar mappar och undermappar i en hierarkisk trädstruktur. Svaret getFolderTree är begränsat till högst 100 000 mappar

Syntax

## Auktoriserade användartyper {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läsåtkomst till mappen för att kunna returnera data om den.

## Parametrar {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Indata (getFolderTreeParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| ` *`accessUserHandle`*` | `xsd:string` | Nej | Används endast av administratörer för att personifiera en viss användare. |
| ` *`accessGroupHandle`*` | `xsd:string` | Nej | Används för att filtrera efter en viss grupp, inklusive någon av dem som företaget tillhör. |
| ` *`folderPath`*` | `xsd:string` | Nej | Rotmappen som ska hämta mappar och alla undermappar till lövnivån. Om detta utelämnas används företagsroten. |
| ` *`djup`*` | `xsd:int` | Ja | Värdet noll hämtar mappen på den översta nivån. Alla andra värden anger djupet som ska nedbrytas i trädet. |
| ` *`assetTypeArray`*` | `types:StringArray` | Nej | Returnerar mappar som bara innehåller angivna resurstyper. |
| ` *`responseFieldArray`*` | `types:StringArray` | Nej | Innehåller en lista med fält som du vill inkludera i svaret. |
| ` *`excludeFieldArray`*` | `types:StringArray` | Nej | Innehåller en lista med fält som du vill utesluta i svaret. |

**Utdata (getFolderTreeReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`mappar`*` | `types:folders` | Nej | Hierarkin för mappar i en trädstruktur. Svaret är begränsat till högst 100 000 mappar. |
| ` *`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Exempel {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

I det här kodexemplet används ett företagshandtag och en djupparameter för att avgöra hur mycket av djupet som svaret ska returnera. Svaret innehåller mappar och undermappsmatriser med relaterade. Ställ in djupvärdet till ett mindre tal för att söka djupare i mappträdet.

**Begäran**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Svar**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

