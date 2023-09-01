---
title: saveMetadataField
description: Skapa eller redigera ett metadatafält. Utelämna den valfria fältreferensen för att skapa ett metadatafält.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# saveMetadataField{#savemetadatafield}

Skapa eller redigera ett metadatafält. Utelämna den valfria fältreferensen för att skapa ett metadatafält.

>[!NOTE]
>
>Den här metoden är föråldrad.

## Auktoriserade användartyper {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-ec6827d485a143f4a059a92b18e40f4e}

**Indata (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameternamn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtaget till företaget. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Fälthandtag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Val av resurstyper som metadata ska sparas från. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Fältnamn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Val av metadatafälttyper. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Standardvärde för fälten för alla resurser. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Dölj eller visa systemspecifika IPS-metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>En boolesk flagga som anger om metadatafältet används (valideras) när värdet ställs in. </p> <p>Om värdet är true genereras ett fel om ett ogiltigt värde anges i <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (saveMetadataFieldReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Hantera det nya metadatafältet. |

## Exempel {#section-4441c26d1f41466ba972b43dd5189e89}

I det här kodexemplet skapas ett metadatafält som begränsas av strängkonstanterna Resurstyp och Metadatafälttyper. Om `fieldHandle` -elementet har ett giltigt fältreferensvärde, ändrar metadatavärdena och får samma fältreferens som du angav i begäran.

**Begäran**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Svar**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
