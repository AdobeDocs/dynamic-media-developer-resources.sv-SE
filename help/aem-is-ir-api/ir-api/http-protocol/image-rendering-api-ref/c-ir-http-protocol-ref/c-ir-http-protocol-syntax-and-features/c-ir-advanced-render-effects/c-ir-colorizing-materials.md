---
description: De flesta material kan färgas dynamiskt.
solution: Experience Manager
title: Färga material
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Färga material{#colorizing-materials}

De flesta material kan färgas dynamiskt.

Färgningsalgoritmen är mycket enkel och fungerar bäst för materialbilder som har ett begränsat nyansintervall. Om du vill färglägga ett material subtraherar renderaren bara `bgc=`-värdet och lägger till `color=`-värdet till varje pixelvärde.

Färgläggning är inaktiverat om `color=` inte anges. `bgc=` ignoreras av kabinettmaterial, basfärgvärdet som är inbäddat i  [!DNL vnc] filen används i stället.
