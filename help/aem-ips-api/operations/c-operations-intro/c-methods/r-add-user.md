---
description: Skapar ett användarkonto och lägger till det kontot till ett eller flera företag.
seo-description: Skapar ett användarkonto och lägger till det kontot till ett eller flera företag.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# addUser{#adduser}

Skapar ett användarkonto och lägger till det kontot till ett eller flera företag.

När du lägger till en användare till flera företag anger du de företagen efter deras företagshandtag i `companyHandleArray`. Den här åtgärden returnerar referensen till användaren som du just lade till.

## Auktoriserade användartyper {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-40390a512e314b8d80ecffbb7729f6fb}

**Indata (addUserParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Ja | Användarens förnamn. |
| ` *`lastName`*` | `xsd:string` | Ja | Användarens efternamn. |
| ` *`e-post`*` | `xsd:string` | Ja | Användarens e-postadress. |
| ` *`defaultRole`*` | `xsd:string` | Ja | Anger rollen för en användare i varje företag de tillhör. Observera dock att `IpsAdmin`-rollen åsidosätter andra inställningar per företag. |
| ` *`lösenord`*` | `xsd:string` | Ja | Anger användarens lösenord |
| ` *`passwordExpires`*` | `xsd:dateTime` | Nej | Anger lösenordets förfalloperiod. Ange tidszonen när begäran skickas. Tidszoner justeras till Central Time. |
| ` *`isValid`*` | `xsd:boolean` | Ja | Anger om användaren är giltig. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Ja | En array med företagshandtag. |

**Utdata (addUserParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Ja | Referensen till användaren. |

## Exempel {#section-2547cef622734b71919eef849960b5cb}

IPS API returnerar ett användarhandtagselement som anger den nya användaren.

**Begäran**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Svar**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

