---
description: Skapar en bilduppsättning.
seo-description: Skapar en bilduppsättning.
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
topic: Scene7 Image Production System API
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# createImageSet{#createimageset}

Skapar en bilduppsättning.

Syntax

## Auktoriserade användartyper {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till målmappen.

## Parametrar {#section-03d22ba7d290477e91c25ca1d4439200}

**Indata (createImageSetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget som bilduppsättningen tillhör. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Referensen till mappen. |
| ` *`name`*` | `xsd:string` | Ja | Namn på bilduppsättning. |
| ` *`type`*` | `xsd:string` | Ja | Bilduppsättningstyp. |
| ` *`thumbAssetHandle`*` | `xsd:string` | Nej | Hantera den resurs som fungerar som miniatyrbild för den nya bilduppsättningen. Om inget anges försöker IPS använda den första bildresursen som uppsättningen refererar till. |

**Utdata**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Handtaget till den nya bilduppsättningen. |

## Exempel {#section-385fe3b0af8044b0a2451336ec137fc5}

I det här kodexemplet skapas en bilduppsättning som anges av företag, mapp, namn och typ. Svaret är en resurshandtag för den nya bilduppsättningen.

**Begäran**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Svar**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```

