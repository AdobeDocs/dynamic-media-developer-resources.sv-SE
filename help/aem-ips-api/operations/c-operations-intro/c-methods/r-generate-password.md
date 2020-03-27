---
description: Skapar ett nytt lösenord.
seo-description: Skapar ett nytt lösenord.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Scene7 Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# generatePassword{#generatepassword}

Skapar ett nytt lösenord.

Syntax

## Auktoriserade användartyper {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-d516615c906240819a284786efb19863}

**Indata (generatePasswordParam)**

Ingen.

**Utdata (generatePasswordParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`lösenord`*` | `xsd:string` | Ja | Ett nytt lösenord. |

## Exempel {#section-f580fefdccec46fe95359e3aef0ed17f}

Detta kodexempel genererar ett lösenord. Det är ovanligt eftersom begäran bara är en parameter utan några omslutna element eller värden. IPS returnerar ett starkt lösenord.

**Begäran**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Svar**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

