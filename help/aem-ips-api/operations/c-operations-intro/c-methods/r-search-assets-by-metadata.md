---
description: Söker i metadataindexarkivet efter de angivna söktermerna. Returnerar resursdata som metoden searchAssets.
seo-description: Söker i metadataindexarkivet efter de angivna söktermerna. Returnerar resursdata som metoden searchAssets.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Söker i metadataindexarkivet efter de angivna söktermerna. Returnerar resursdata som metoden searchAssets.

Med `searchAssetsByMetadata` kan du söka efter användardefinierade metadatafält, men dessa fält returneras inte om de anges i `responseMetadataArray`. Följande kodexempel illustrerar detta:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

returnerar ett null-värde:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Du kan lösa det här problemet genom att använda `fieldHandles` för resurserna som returneras från sökningen för att köra `getAssets` (se även [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Den här metoden hämtar värden för användardefinierade fält för resurserna i fråga. Använd följande syntaxexempel för att söka mot användardefinierade metadatafält:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Auktoriserade användartyper {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Indata (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handtaget till företaget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filter</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> text:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Filter som hjälper dig att definiera sökvillkor. </p> <p>Se <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Villkor som definierar sökvillkor. Mer information finns nedan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Ytterligare fält som du vill ha ifyllda på svaret i resurssammanfattningen. Fälten måste anges i normaliserat format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Antalet resurser som returneras av svaret. Standardvärdet är 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Anger vilken resultatsida som ska returneras baserat på sidstorleken <span class="codeph"> recordsPerPage</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Sortera efter valt resursfält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Val av sorteringsriktning. Stigande är standard. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (searchAssetsByMetadataReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | Nej | Antal träffar. |
| ` *`assetArray`*` | `types:AssetArray` | Nej | Array med resurser som returneras av sökningen. |

## metadataConditionArray-information {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Objektstruktur**

`metadataConditionArray` strukturen är följande:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Värden**

`field_handle` är söknyckeln för metadata. Den kan innehålla punktnotation. Möjliga värden är:

* `asset_id` (utan prefix)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (samma som  `modified_at` (datum i formuläret: fr.o.m. 25 juli 2014 22:13:45 GMT-0500 (CDT))

* `created_by`

**Tillåtna operatorer**

[!DNL operator] definierar hur värdet ska jämföras och inkluderar:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

`comparison_value` är den term du ska söka efter.

## Exempel {#section-53a12b9c023e4e629eddf5719c955ad4}

Det här kodexemplet utför en sökning med följande metadatavillkor:

* `name` fältet innehåller  `1000801`.

* `dc.rights` är lika med  `Per Jessen Schmidt`.

**Begäran**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Svar**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

