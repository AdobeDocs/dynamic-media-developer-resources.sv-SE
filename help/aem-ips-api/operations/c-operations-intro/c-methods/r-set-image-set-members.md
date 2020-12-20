---
description: Anger listan med resurser som är associerade med en bilduppsättning.
seo-description: Anger listan med resurser som är associerade med en bilduppsättning.
seo-title: setImageSetMembers
solution: Experience Manager
title: setImageSetMembers
topic: Scene7 Image Production System API
uuid: 84a73ff4-e93f-4764-80e8-e15f1fec1aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# setImageSetMembers{#setimagesetmembers}

Anger listan med resurser som är associerade med en bilduppsättning.

Den här åtgärden ignorerar parametern `pageReset` för `ImageSets` och `SpinSets` och tvingar värdet till true.

## Auktoriserade användartyper {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till bilduppsättningsresursen och läsåtkomst till varje medlemsresurs.

## Parametrar {#section-2f46efcd24c648aeacba738509426e46}

**Indata (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoriskt </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Företagshandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtag för bilduppsättning. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> En array med resursmedlemmar som tillhör bilduppsättningen. </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (setImageSetMembersReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-7b87219034464aa98524178ccee27738}

I det här kodexemplet används en medlemsarray för att ange medlemmarna i en bilduppsättning.

**Begäran**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Svar**

Ingen.
