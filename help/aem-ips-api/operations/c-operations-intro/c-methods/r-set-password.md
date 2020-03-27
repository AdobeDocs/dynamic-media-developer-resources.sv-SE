---
description: Anger lösenordet för en viss användare eller standardanvändaren till ett visst värde, beroende på om du anger en användarreferens eller inte.
seo-description: Anger lösenordet för en viss användare eller standardanvändaren till ett visst värde, beroende på om du anger en användarreferens eller inte.
seo-title: setPassword
solution: Experience Manager
title: setPassword
topic: Scene7 Image Production System API
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setPassword{#setpassword}

Anger lösenordet för en viss användare eller standardanvändaren till ett visst värde, beroende på om du anger en användarreferens eller inte.

Lösenordets förfallodatum är valfritt. Om det utelämnas upphör aldrig lösenordet att gälla.

## Auktoriserade användartyper {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Endast* `IpsAdmin` användartypen har behörighet att köra setPassword-anrop mot andra användare.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parametrar {#section-0531294341f7483d89dacaa393dd659a}

**Indata (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Användarhandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> lösenord </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:sträng </span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Lösenord. </p> <p>Följande krav gäller för det valda lösenordet: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Lösenord är skiftlägeskänsliga. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">Lösenordet måste innehålla minst åtta tecken. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">Lösenordet måste innehålla ett eller flera tecken från följande teckenklasser: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Engelska gemener. Exempel: <span class="codeph"> a b c d e </span> o.s.v. </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Engelska versaler. Exempel: <span class="codeph"> A C D E </span> och så vidare. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Nummer. Exempel: <span class="codeph"> 1 2 3 4 5 </span> och så vidare. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Specialsymboltecken. Du kan till exempel använda något av följande: <span class="codeph"> ` ~! @ # $ % ^ * ( ) _ + - = { }| [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Bestämmer förfallodatum för lösenord. <p>Obs!  Ange tidszonen med begäran för det här fältet. Tidszoner justeras till Central Time. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (setPasswordReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-23a6fbabdb3c4c3180076057e47ae567}

I det här kodexemplet skapas ett användarlösenord. Lösenordet upphör aldrig att gälla eftersom det `passwordExpires` utelämnats.

**Begäran**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Svar**

Ingen.
