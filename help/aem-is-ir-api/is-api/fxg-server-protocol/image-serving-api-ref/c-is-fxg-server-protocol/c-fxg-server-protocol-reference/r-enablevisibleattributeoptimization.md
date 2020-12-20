---
description: Aktiverar optimering av FXG.
seo-description: Aktiverar optimering av FXG.
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

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
