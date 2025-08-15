---
title: Textplacering
description: renderaren text= placerar text som skiljer sig i grunden från renderaren textPs= när den används på lager med redan storlek (d.v.s. när size= även anges).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Textplacering{#text-positioning}

Återgivaren `text=` placerar text som skiljer sig i grunden från renderaren textPs= när den används på lager med redan storlek (d.v.s. när size= även anges).

Självstorleksändringslager för `text=` och `textPs=` har liknande utseende och placering.

`textPs=` justerar den övre delen av teckencellen mot textrutans övre del (förutsatt att `\vertalt` används), även om det resulterar i att delar av de återgivna texttecknen delvis sträcker sig utanför textrutans gräns. Återgivna specialtecken för vissa teckensnitt kan också skjuta ut något utanför textrutans vänstra och högra kant. För program som kräver att all återgiven text ska finnas i lagerrektangeln kan RTF-kommandona `\marg*` eller `textFlowPath=` användas för att justera textåtergivningsområdet.

`text=` flyttar däremot den återgivna texten efter behov och ser till att alla återgivna tecken ryms helt i den angivna textrutan.

`text=` kan vara något enklare att använda för enkla program, men `textPs=` erbjuder exakt positionering oberoende av teckensnittets ytor och texteffekter.

## Exempel {#section-1b6bdf2ea34447528188ae4e1430ee71}

Följande exempel är för text i förstorlek. Beteendet för text som ändrar storlek automatiskt är annorlunda.

** `Text=` har alltid en smal marginal överst:**

![Exempel på textplacering är en bild](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` återger text som är tätt justerad mot textrutans överkant, vilket resulterar i en viss urklippning, även för vanliga teckensnitt som Arial®:**

![Exempel på textplacering är två bilder](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` förskjuter automatiskt återgiven text nedåt för att undvika urklipp:**

![Exempel på textplacering är tre bilder](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` flyttar inte text som innehåller upphöjda delar, vilket resulterar i betydande bortfall om texten finns i lager 0:**

![Exempel på textplacering är fyra bilder](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**En marginal på 10 pt (200 twip) längst upp återger texten utan bortfall:**

![Exempel på textplacering är fem bilder](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Återgivna tecken för vissa skriptteckensnitt kan sträcka sig utanför textrutan avsevärt:**

![Exempel på textplacering är sex bilder](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
