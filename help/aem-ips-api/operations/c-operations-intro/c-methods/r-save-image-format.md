---
description: Skapar ett bildformat.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# saveImageFormat{#saveimageformat}

Skapar ett bildformat.

>[!NOTE]
>
>Fältvärdet `urlModifier` måste bestå av giltig XML. Ändra till exempel `&` till `&`. Hämta värdet `urlModfier` från IPS-användargränssnittet.

## Auktoriserade användartyper {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Indata (saveImageFormatParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget med det bildformat som du vill arbeta med. |
| imageFormatHandle | `xsd:string` | Nej | Bildformatshandtag som du vill spara. |
| name | `xsd:string` | Ja | Bildformatsnamn. |
| urlModifier | `xsd:string` | Ja | Detta kan vara vilken frågesträng som helst för IPS-protokoll. Det enklaste sättet att generera en URL-modifierare är att skapa en med IPS-användargränssnittet och sedan klippa ut och klistra in frågesträngen. |

**Utdata (saveImageFormatReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Ja | Hantera bildformatet. |

## Exempel {#section-c7bd733212ef494297a97093f3af193f}

I det här kodexemplet skapas ett bildformat. I det här exemplet bestämdes `urlModifier` av dess värde i IPS-användargränssnittet med ett giltigt HTML-format.

**Begäran**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Svar**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
