---
description: Med renderaren text= placeras text i grunden annorlunda än renderaren textPs= när den används på lager med redan storleksanpassad storlek (dvs när size= även anges).
seo-description: Med renderaren text= placeras text i grunden annorlunda än renderaren textPs= när den används på lager med redan storleksanpassad storlek (dvs när size= även anges).
seo-title: Textplacering
solution: Experience Manager
title: Textplacering
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Textplacering{#text-positioning}

Med renderaren text= placeras text i grunden annorlunda än renderaren textPs= när den används på lager med redan storleksanpassad storlek (dvs när size= även anges).

Självstorleksändring `text=`och `textPs=` lager har liknande utseende och placering.

`textPs=` justerar tecknets överkant mot textrutans överkant (förutsatt att `\vertalt`), även om detta leder till att delar av de återgivna texttecknen delvis sträcker sig utanför textrutans gränser. Återgivna specialtecken för vissa teckensnitt kan också skjuta ut något utanför textrutans vänstra och högra kant. För program som kräver att all återgiven text ska finnas i lagerrektangeln, kan RTF- `\marg*` kommandona eller - `textFlowPath=` användas för att justera textåtergivningsområdet.

I stället `text=` flyttas den återgivna texten efter behov och alla återgivna specialtecken garanteras att passa in helt i den angivna textrutan.

Även om det `text=` kan vara något enklare att använda för enkla program, `textPs=` erbjuder exakt positionering oberoende av teckensnitt och texteffekter.

## Exempel {#section-1b6bdf2ea34447528188ae4e1430ee71}

Följande exempel är för text i förstorlek. Beteendet för text som ändrar storlek automatiskt är annorlunda.

** `Text=` har alltid en smal marginal överst:**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` återger text som är tätt justerad mot textrutans överkant, vilket kan leda till en viss urklippning, även för vanliga teckensnitt som Arial:**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` förskjuter automatiskt återgiven text nedåt för att undvika urklipp:**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` flyttar inte text som innehåller upphöjda delar, vilket resulterar i betydande bortfall om texten finns i lager 0:**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**En marginal på 10 pt (200 twip) längst upp återger texten utan bortfall:**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Återgivna tecken för vissa skriptteckensnitt kan sträcka sig utanför textrutan:**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
