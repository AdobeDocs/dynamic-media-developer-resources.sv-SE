---
description: Tar bort en mapp.
seo-description: Tar bort en mapp.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
topic: Scene7 Image Production System API
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# deleteFolder{#deletefolder}

Tar bort en mapp.

Syntax

## Auktoriserade användartyper {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och borttagningsåtkomst till mappen och alla dess underordnade objekt.

## Parametrar {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Indata (deleteFolderParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som mappen tillhör. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Referensen till mappen som ska tas bort. |

**Utdata (deleteFolderParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-9d4617b322e8442d80e59be0f8714841}

Den här exempelkoden tar bort en mapp från företagets rot. Den kräver en mappreferens som du måste hämta från en annan åtgärd.

**Begäran**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Ingen.
