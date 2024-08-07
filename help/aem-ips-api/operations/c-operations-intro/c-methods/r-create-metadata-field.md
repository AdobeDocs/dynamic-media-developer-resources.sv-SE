---
title: createMetadataField
description: Det gör att administratörer kan skapa metadatafält som kan koordineras med content management-system eller för mallåtgärder. Exempel på skapade metadatafält är nyckelord, information om författaren till bilden eller information om upphovsrättsinnehavare.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# createMetadataField{#createmetadatafield}

Det gör att administratörer kan skapa metadatafält som kan koordineras med content management-system eller för mallåtgärder. Exempel på skapade metadatafält är nyckelord, information om författaren till bilden eller information om upphovsrättsinnehavare.

Syntax

## Auktoriserade användartyper {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parametrar {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Indata (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namnet på det företag som metadatafältet tillhör. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Resurstyp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namnet på metadatafältet som du skapar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Fälttyp för metadata. <p>Metadatafältstyperna definierar de tillgängliga typerna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Standardvärdet för metadatafältet som ska skapas (till exempel <span class="codeph"> Scen 7</span>). </p> <p>Standardvärden stöds inte för taggfältstyper och måste utelämnas. Om ett icke-tomt standardvärde anges för en taggfältstyp returneras ett fel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Dölj eller visa systemspecifika IPS-metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>En boolesk flagga som anger om metadatafältet används (valideras) när värdet ställs in. </p> <p>Om värdet är true genereras ett fel om ett ogiltigt värde anges i <span class="codeph"> setAssetMetadata </span> /<span class="codeph"> batchSetAssetMetadata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Du kan skapa en uppsättning delade specifika värden som markerade taggar kan peka på. </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (createMetadataFieldReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| fieldHandle | `xsd:string` | Ja | Referensen till det nya metadatafältet. |

## Exempel {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Detta kodexempel skapar ett metadatafält för strängtyp med namnet `createMetadataField`. Svaret returnerar referensen till det nya metadatafältet.

**Begäran**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Svar**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```
