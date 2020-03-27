---
description: Hämtar en array med användare som anges av hanterare för företag, grupper och användarroller. Med den här åtgärden kan du sortera returnerade användare och filtrera efter tecken.
seo-description: Hämtar en array med användare som anges av hanterare för företag, grupper och användarroller. Med den här åtgärden kan du sortera returnerade användare och filtrera efter tecken.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUsers{#getusers}

Hämtar en array med användare som anges av hanterare för företag, grupper och användarroller. Med den här åtgärden kan du sortera returnerade användare och filtrera efter tecken.

## Auktoriserade användartyper {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`includeInactive`*` | `xsd:boolean` | Nej | Inkludera eller exkludera inaktiva användare. Användare av icke-IPS-administratörer måste vara en aktiv medlem i minst ett företag för att kunna auktoriseras att göra API-anrop. Ett auktoriseringsfel returneras om användaren inte har några aktiva företagsmedlemskap. |
| ` *`includeInvalid`*` | `xsd:boolean` | Nej | Gör att du kan inkludera/exkludera ogiltiga användare. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Nej | Filtrera resultat efter företag. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Nej | Filtrera resultat efter grupp. |
| ` *`userRoleArray`*` | `types:StringArray` | Nej | Filtrera resultat efter användarroll. |
| ` *`charFilterField`*` | `xsd:string` | Nej | Filtrera resultat efter fältets strängprefix (se [!DNL Trash State).] |
| ` *`charFilter`*` | `xsd:string` | Nej | Filtrera resultat efter ett visst tecken. |
| ` *`sortBy`*` | `xsd:string` | Nej | Val av användarsorteringsfält. |
| ` *`recordsPerPage`*` | `xsd:int` | Nej | Returnerar angivet antal poster per sida. |
| ` *`resultsPage`*` | `xsd:int` | Nej | Resultatsida. |

**Utdata (getUsersReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`userArray`*` | `types:UserArray` | Ja | En array med användare. |

## Exempel {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Detta kodexempel returnerar användararrayen för flera valfria parametrar. Användarroller, användarteckenfilterfält och användarsorteringsfält bestäms med hjälp av specifika strängkonstanter.

**Begäran**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Svar**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```

