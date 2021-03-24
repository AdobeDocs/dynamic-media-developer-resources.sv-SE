---
description: Aktiverar optimering av FXG.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

Aktiverar optimering av FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Tar bort de element vars synlighet anges som false i FXG när denna FXG skickas, vilket i sin tur minskar bearbetningstiden för FXG. Även om det bara tar bort de element som visas med synlighet som false som inte påverkar något annat element i FXG. Om det till exempel finns text på `Path` och synligheten för `Path` är inställd på false tas den inte bort från FXG även om den här modifieraren är aktiverad eftersom texten måste ritas på den här sökvägen.

Standardvärdet är 1.
