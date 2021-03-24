---
description: Skapar ett nytt lösenord.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---


# generatePassword{#generatepassword}

Skapar ett nytt lösenord.

Syntax

## Auktoriserade användartyper {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
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
| `*`lösenord`*` | `xsd:string` | Ja | Ett nytt lösenord. |

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

