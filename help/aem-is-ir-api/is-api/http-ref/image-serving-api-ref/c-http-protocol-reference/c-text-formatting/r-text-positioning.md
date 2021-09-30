---
title: Textplacering
description: Med renderaren text= placeras text i grunden annorlunda än renderaren textPs= när den används på lager med redan storlek (dvs. när size= anges).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Textplacering{#text-positioning}

Med `text=`-renderaren placeras text som skiljer sig väsentligt från renderaren textPs= när den används på lager med redan storlek (d.v.s. när size= även anges).

Självstorleksändring av `text=`och `textPs=` lager har liknande utseende och placering.

Med `textPs=` justeras tecknets överkant mot textrutans överkant (om `\vertalt` används), även om det resulterar i delar av de återgivna texttecknen som delvis ligger utanför textrutans gränser. Återgivna specialtecken för vissa teckensnitt kan också skjuta ut något utanför textrutans vänstra och högra kant. För program där all återgiven text ska finnas i lagrets rektangel kan RTF-kommandona `\marg*` eller `textFlowPath=` användas för att justera textåtergivningsområdet.

Med `text=` flyttas den återgivna texten efter behov och det garanteras att alla återgivna tecken får plats helt i den angivna textrutan.

`text=` kan vara något enklare att använda för enkla program, men `textPs=` erbjuder exakt positionering oberoende av teckensnitt och texteffekter.

## Exempel {#section-1b6bdf2ea34447528188ae4e1430ee71}

Följande exempel är för text i förstorlek. Beteendet för text som ändrar storlek automatiskt är annorlunda.

** `Text=` har alltid en smal marginal överst:**

![Exempel på textplacering - en bild](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` återger text som är tätt justerad mot textrutans överkant, vilket resulterar i en viss urklippning, även för vanliga teckensnitt som Arial®:**

![Exempel på textplacering är två bilder](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` förskjuter automatiskt återgiven text nedåt för att undvika urklipp:**

![Exempel på textplacering - tre bilder](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` flyttar inte text som innehåller upphöjda delar, vilket resulterar i betydande bortfall om texten finns i lager 0:**

![Exempel på textplacering är fyra bilder](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**En marginal på 10 pt (200 twip) längst upp återger texten utan bortfall:**

![Exempel på textplacering fem bilder](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Återgivna tecken för vissa skriptteckensnitt kan sträcka sig utanför textrutan:**

![Exempel på textplacering är sex bilder](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
