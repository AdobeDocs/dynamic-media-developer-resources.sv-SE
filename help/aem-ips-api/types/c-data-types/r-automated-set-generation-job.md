---
description: Gruppera filer i uppsättningar med hjälp av en listmatris för resurshandtag.
seo-description: Gruppera filer i uppsättningar med hjälp av en listmatris för resurshandtag.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
topic: Scene7 Image Production System API
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Gruppera filer i uppsättningar med hjälp av en listmatris för resurshandtag.

Syntax

## Parametrar {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:HandleArray</span> </td> 
   <td colname="col3">En array med resurshandtag som används för att skapa uppsättningen. <p>Som standard är 1000 det maximala antalet resurser som du kan ha i arrayen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Sökväg till den mapp där du vill spara uppsättningarna. Sparar som standard i företagets rotmapp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Anger en flagga som anger om resurserna ska publiceras eller inte. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutoSetCreationOptions</span> </td> 
   <td colname="col3">En array med angivna genereringsskript som du kan köra på de överförda filerna. Se <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Ställ in ett automatiskt e-postmeddelande för jobbet. </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting Options**

Parametern `emailSetting` innehåller följande alternativ:

| Alternativ | Returnerar |
|---|---|
| `All` | Alla jobbmeddelanden (fel, varningar, slutförande) till den angivna mottagaren. |
| `Error` | Jobbfel till angiven mottagare. |
| `ErrorAndWarning` | Jobbfel och varningar till angiven mottagare. |
| `JobCompletion` | Ett meddelande om slutförande av jobb till den angivna mottagaren. |
| `None` | Jobbet skickar inga jobbmeddelanden till den angivna mottagaren. |

## Exempel {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

