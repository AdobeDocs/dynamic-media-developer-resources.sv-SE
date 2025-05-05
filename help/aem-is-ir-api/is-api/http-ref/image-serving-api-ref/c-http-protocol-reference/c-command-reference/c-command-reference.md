---
title: Kommandoreferens
description: I det här avsnittet beskrivs HTTP-protokollkommandona.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Kommandoreferens{#command-reference}

I det här avsnittet beskrivs HTTP-protokollkommandona.

>[!TIP]
>
>Prova och upptäck fördelarna med Dynamic Media bildmodifierare och Smart Imaging med Dynamic Media [_Snapshot_](https://snapshot.scene7.com/).
>
> Ögonblicksbild är ett visuellt demonstrationsverktyg som är utformat för att illustrera styrkan hos Dynamic Media för optimerad och dynamisk bildleverans. Experimentera med testbilder eller Dynamic Media-URL:er för att visuellt se resultatet av olika bildmodifierare i Dynamic Media och optimera smarta bilder för följande:
>* Filstorlek (med WebP- och AVIF-leverans)
>* Nätverksbandbredd
>* DPR (Device Pixel Ratio)
>
>Om du vill lära dig hur enkelt det är att använda ögonblicksbild kan du spela upp utbildningsvideon [för ögonblicksbild](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=sv-SE) (3 minuter och 17 sekunder).


**Endast för Dynamic Media i Adobe Experience Manager** - Förutom de grundläggande bildinställningarna som är tillgängliga i användargränssnittet har [!DNL Dynamic Media] i AEM ( [!DNL Adobe Experience Manager]) stöd för många avancerade bildändringar som du kan ange i fältet **Bildmodifierare** . Dessa parametrar definieras nedan. Tänk dock på att följande funktioner inte stöds i Dynamic Media i AEM.

* Färgkorrigeringskommandon: `icc=` och `iccEmbed=`.
* Grundläggande mallnings- och textrenderingskommandon: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` och `textPs=`.
* Localization commands: `locale=` and `req=xlate`.
* `req=set` är inte tillgängligt för allmän användning.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Icke-kärnbaserade Dynamic Media-tjänster: SVG, bildåtergivning och web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Se även Dynamic Media [Alternativ för bildförinställningar](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=sv-SE#dynamic) i dokumentationen till AEM 6.5.

* [justera](r-align.md)
* [ankare](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [färg](r-color-commandref.md)
* [beskära](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [effekt](r-effect.md)
* [effectMask](r-effectmask.md)
* [utöka](r-extend.md)
* [anpassa](r-fit.md)
* [vända](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [hide](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [lager](r-layer.md)
* [locale](r-locale.md)
* [map](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
* [nätverk](r-network.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_growth](r-op-grow.md)
* [op_growthMask](r-op-growmask.md)
* [op_growthMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [ursprung](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspektiv](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [kvantifiera](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [gradera](r-rgn.md)
* [rotera](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [size](r-size-reference.md)
* [src](r-src.md)
* [mall](r-template.md)
* [text](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
