---
description: Hämtar information om en användare. Använd e-postadressen och lösenordet för en systemanvändare som autentiseringsuppgifter för att godkänna begäran. Annars hämtar åtgärden information om standardanvändaren.
seo-description: Hämtar information om en användare. Använd e-postadressen och lösenordet för en systemanvändare som autentiseringsuppgifter för att godkänna begäran. Annars hämtar åtgärden information om standardanvändaren.
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
topic: Scene7 Image Production System API
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUserInfo{#getuserinfo}

Hämtar information om en användare. Använd e-postadressen och lösenordet för en systemanvändare som autentiseringsuppgifter för att godkänna begäran. Annars hämtar åtgärden information om standardanvändaren.

Syntax

## Auktoriserade användartyper {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-e87b3cb743494719925c9458eed433b6}

**Indata (getUserInfoParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Nej | Hantera användaren vars information du vill returnera. |
| ` *`e-post`*` | `xsd:string` | Nej | Användarens e-postadress. |

**Utdata (getUserInfoReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`userInfo`*` | `types:User` | Ja | Användarens förnamn, efternamn, e-postadress och roll, samt om användaren är giltig och när användarens lösenord upphör att gälla. |

## Exempel {#section-98d77a2e360a438dbe240099bea26a65}

Detta kodexempel returnerar information för standard-IPS-användaren.

**Begäran**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Svar**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```

