---
description: Hämtar information om en användare. Använd e-postadressen och lösenordet för en systemanvändare som autentiseringsuppgifter för att godkänna begäran. Annars hämtar åtgärden information om standardanvändaren.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

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
| `*`userHandle`*` | `xsd:string` | Nej | Hantera användaren vars information du vill returnera. |
| `*`e-post`*` | `xsd:string` | Nej | Användarens e-postadress. |

**Utdata (getUserInfoReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | Ja | Användarens förnamn, efternamn, e-postadress och roll, samt om användaren är giltig och när användarens lösenord upphör att gälla. |

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
