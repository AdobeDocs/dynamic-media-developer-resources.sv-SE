---
description: Skapa ett nytt bildschema eller redigera ett befintligt.
seo-description: Skapa ett nytt bildschema eller redigera ett befintligt.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# saveImageMap{#saveimagemap}

Skapa ett nytt bildschema eller redigera ett befintligt.

Syntax

## Auktoriserade användartyper {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Indata (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtaget till företaget med den bildschema som du vill spara. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtaget till den bildresurs som bildschemat tillhör. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Handtaget till bildschemat. Skapar ett bildschema om NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namnet på det bildschema som skapas eller sparas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Val av regionsform. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> En kommaavgränsad lista med punkter som definierar regionen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> åtgärd  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Det <span class="codeph"> href </span>-värde som är associerat med bildschemat enligt specifikationen i IPS-gränssnittet. </p> <p>Om du vill hämta <span class="codeph"> href </span>-värdet klickar du på bilden i IPS-gränssnittet, kopierar och klistrar in URL:en i det här elementet och formaterar sedan IPS-URL:en som en korrekt URL. Till exempel blir <span class="codeph"> &amp; </span> <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Ordningen i listan med bildscheman (Z-axeln). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> aktiverad  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Utdata (saveImageMapReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Ja | Handtaget till det nya eller redigerade bildschemat. |

## Exempel {#section-fdac488b640f427c8aa3d549c5032851}

I det här kodexemplet skapas ett nytt bildschema för en resurs. Den använder en formtyp som bestäms av en konstant för en områdesformsträng och returnerar ett handtag till det nya bildschemat.

**Begäran**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Svar**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```

