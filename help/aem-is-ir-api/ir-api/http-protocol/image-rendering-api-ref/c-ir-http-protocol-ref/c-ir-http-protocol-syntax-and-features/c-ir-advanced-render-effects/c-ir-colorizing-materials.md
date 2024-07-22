---
title: Färglägga material
description: De flesta material kan färgas dynamiskt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Färglägga material{#colorizing-materials}

De flesta material kan färgas dynamiskt.

Färgningsalgoritmen är enkel och fungerar bäst för materialbilder som har ett begränsat nyansintervall. Om du vill färglägga ett material subtraherar renderaren bara värdet `bgc=` och lägger till värdet `color=` för varje pixelvärde.

Färgläggning är inaktiverat om `color=` inte anges. Attributet `bgc=` ignoreras av kabinettmaterial. Basfärgvärdet som är inbäddat i filen [!DNL vnc] används i stället.
