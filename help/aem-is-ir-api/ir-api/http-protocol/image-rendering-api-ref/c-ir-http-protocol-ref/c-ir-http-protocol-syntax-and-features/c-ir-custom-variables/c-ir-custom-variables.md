---
description: Frågedelen av begäranden och vinjettmodifieringssträngar kan innehålla användardefinierade variabler.
solution: Experience Manager
title: Egna variabler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Egna variabler{#custom-variables}

Frågedelen av begäranden och vinjett::Modifierarsträngar kan innehålla användardefinierade variabler.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variabelnamn. Kan bestå av en kombination av alfa-, siffra- och säkra tecken, med undantag för &#39;$&#39;.

** *[!DNL value]* ** Värde som variabeln ska anges till (sträng).

Variabler definieras på liknande sätt som andra serverkommandon, med syntaxen ovan. Variabler måste definieras innan de kan refereras. Variabler som definieras i `vignette::Modifier` kan refereras i URL-begäran och vice versa.

>[!NOTE]
>
>*[!DNL value]* måste vara URL-kodad med ett-pass för säker HTTP-överföring. Dubbel kodning krävs om *[!DNL value]* överförs på nytt via HTTP. Detta är fallet när *[!DNL value]* ersätts till en kapslad extern begäran.

Variabler refereras genom att du bäddar in variabelnamnet (omges av ett radavstånd och ett efterföljande $) var som helst i kommandovärden. Till exempel mellan &quot;=&quot; efter kommandonamnet och efterföljande &quot;&amp;&quot; eller slutet av begäran. Servern ersätter varje sådan förekomst av $ *[!DNL name]*$ med *[!DNL string]*. Inga substitutioner kommer att förekomma på förekomster av $ *[!DNL name]*$ i kommandonamn (före likhetstecknet för ett kommando) och i sökvägsdelen av begäran.

Anpassade variabler får inte kapslas. Förekomster av $ *[!DNL name]*$ inom *[!DNL string]* ersätts inte. Begärandefragmentet `$var2=apple&$var1=my$var2$tree&text=$var1$` matchar till `text=my$var2$tree`.

$ är inte ett reserverat tecken; det kan inträffa på annat sätt i begäran. `src=my$texture$file.tif` är till exempel ett giltigt kommando (förutsatt att det finns en materialkatalogpost eller texturfil med namnet [!DNL my$texture$file.tif]), medan `wid=$number$` inte är det, eftersom `wid=` kräver ett numeriskt argument.
