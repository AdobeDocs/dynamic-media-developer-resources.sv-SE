---
description: Kontrollerar om en användare med ett visst företag (identifieras av referens), e-postadress och lösenord kan logga in.
seo-description: Kontrollerar om en användare med ett visst företag (identifieras av referens), e-postadress och lösenord kan logga in.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# checkLogin{#checklogin}

Kontrollerar om en användare med ett visst företag (identifieras av referens), e-postadress och lösenord kan logga in.

>[!NOTE]
>
>Om företagsreferensen utelämnas kontrollerar den här metoden standardanvändarens inloggning.

## Auktoriserade användartyper {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-1ad4c0b4803b4388aedd655030676cb3}

**Indata (checkLoginParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nej | Referensen till företaget som innehåller användaren. |
| ` *`e-post`*` | `xsd:string` | Ja | Användarens e-postadress. |
| ` *`lösenord`*` | `xsd:string` | Ja | Användarens lösenord. |

**Utdata (checkLoginParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | Ja | Användarens inloggningsstatus. |

## Exempel {#section-23f90100a9d94bc7b4045634cccd1b98}

I den här exempelkoden används en företagshanteringsparameter, e-postadress och ett lösenord för att avgöra om en användare kan logga in på IPS. Om användaren *kan* logga in returnerar metoden strängen `ValidLogin`. Om användaren *inte kan* logga in returnerar metoden strängen `InvalidLogin`.

**Begäran**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Svar**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

