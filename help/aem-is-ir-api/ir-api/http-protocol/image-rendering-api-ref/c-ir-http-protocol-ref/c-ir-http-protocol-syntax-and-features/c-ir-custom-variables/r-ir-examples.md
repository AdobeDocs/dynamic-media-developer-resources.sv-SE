---
title: Exempel
description: I det här exemplet används Bildrutefunktion för att färglägga ett objekt och använda en dekal som innehåller anpassad text i en av vinjettuppsättningarna.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Exempel{#examples}

I det här exemplet används Bildrutefunktion för att färglägga ett objekt och använda en dekal som innehåller anpassad text i en av vinjettuppsättningarna.

IR-variabler används för att identifiera vinjett, logotypbild och anpassad text.

Fältet `vignette::Modifier` i posten med namnet *template* i vinjetteringskartan för materialkatalogen `myCat` innehåller följande:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alla använda vinjetter visas i vinjetteringskartan för materialkatalogen `myCat`.

Klienten kan nu göra följande begäran för att hämta standardbilden (använder variablerna som definieras i början av mallen):

[!DNL `https://server/myCat/template`]

Följande begäran anger visst innehåll som ska återges:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Mer information om kommandot Bildserver `text=` finns i dokumentationen om bildservrar.
