---
description: Lägger till en användare i en array med grupper.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# addGroupMembership{#addgroupmembership}

Lägger till en användare i en array med grupper.

Syntax

## Auktoriserade användartyper {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-e250f6ddb13646808c6a8860b6442bc5}

**Indata (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Hantera användaren vars gruppmedlemskap du vill lägga till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>En array med referenser till de grupper som du vill att företaget ska tillhöra. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (addGroupMembershipParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-f7a1f40c3d7a40ea964b29056c734d81}

I det här exemplet läggs en grupp till i ett företag med groupHandleArray. I det här exemplet används endast en grupp.

**Begäran**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Svar**

Ingen.
