---
description: I det här exemplet används Bildrutefunktion för att färglägga ett objekt och använda en dekal som innehåller anpassad text i en av vinjettuppsättningarna.
seo-description: I det här exemplet används Bildrutefunktion för att färglägga ett objekt och använda en dekal som innehåller anpassad text i en av vinjettuppsättningarna.
seo-title: Exempel
solution: Experience Manager
title: Exempel
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Exempel{#examples}

I det här exemplet används Bildrutefunktion för att färglägga ett objekt och använda en dekal som innehåller anpassad text i en av vinjettuppsättningarna.

IR-variabler används för att identifiera vinjett, logotypbild och anpassad text.

Fältet `vignette::Modifier` i posten *template* i vinjettkartan för materialkatalogen `myCat` innehåller följande:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alla vinjetteringar som ska användas visas i vinjetteringskartan för materialkatalogen `myCat`.

Klienten kan nu göra följande begäran för att hämta standardbilden (då används de variabler som definierats i början av mallen):

[!DNL `https://server/myCat/template`]

Följande begäran anger visst innehåll som ska återges:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Mer information om kommandot Image Serving `text=` finns i dokumentationen om bildservrar.
