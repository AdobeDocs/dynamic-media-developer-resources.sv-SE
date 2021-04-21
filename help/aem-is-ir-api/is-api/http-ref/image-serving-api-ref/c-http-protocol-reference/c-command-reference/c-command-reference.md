---
description: I det här avsnittet beskrivs HTTP-protokollkommandona.
solution: Experience Manager
title: Kommandoreferens
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# Kommandoreferens{#command-reference}

I det här avsnittet beskrivs HTTP-protokollkommandona.

**Endast** för Dynamic Media i AEM: Förutom de grundläggande bildinställningarna som är tillgängliga i användargränssnittet har  [!DNL Dynamic Media] i AEM (  [!DNL Adobe Experience Manager]) stöd för många avancerade bildändringar som du kan ange i fältet  **Image** Modifiers. Dessa parametrar definieras nedan. Tänk dock på att följande funktioner inte stöds i Dynamic Media i AEM.

* Färgkorrigeringskommandon: `icc=` och `iccEmbed=`.
* Grundläggande kommandon för mallar och textåtergivning: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` och `textPs=`.
* Lokaliseringskommandon: `locale=` och `req=xlate`.
* `req=set` är inte tillgängligt för allmän användning.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Icke-kärntjänster från Dynamic Media: SVG, bildåtergivning och web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Se även Dynamic Media [Image Preset Options](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) i dokumentationen till AEM 6.5.

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
