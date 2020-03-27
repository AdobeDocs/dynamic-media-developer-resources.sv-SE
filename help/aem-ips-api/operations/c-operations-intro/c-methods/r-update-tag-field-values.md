---
description: Uppdaterar taggordlistevärden för ett taggfält.
seo-description: Uppdaterar taggordlistevärden för ett taggfält.
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
topic: Scene7 Image Production System API
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateTagFieldValues{#updatetagfieldvalues}

Uppdaterar taggordlistevärden för ett taggfält.

Syntax

## Auktoriserade användartyper {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-0a3a4bab026746238c9d4009caf42e94}

**Indata (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Företagshandtag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Fälthandtag för tagg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Array med taggfältsvärden som du vill uppdatera. <p>Obs!  Uppdaterar endast strängvärden för taggar. Påverkar inte resursassociationer. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (updateTagFieldValuesReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet uppdaterade taggfält. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genererades när åtgärden försökte uppdatera taggfält. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte uppdatera taggfält. |
| ` *`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte uppdatera taggfält. |
| ` *`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte uppdatera taggfält. |

## Exempel {#section-bb4dcf97044c4675974c9b8d27674001}

**Begäran**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Svar**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

