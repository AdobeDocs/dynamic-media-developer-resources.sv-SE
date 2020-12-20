---
description: Typ av begäran. Anger typen av begäran.
seo-description: Typ av begäran. Anger typen av begäran.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# req{#req}

Typ av begäran. Anger typen av begäran.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`alternativ`*]`

* [katalogprops](r-catalogprops.md)
* [exists](r-exists.md)
* [imageprops](r-imageprops.md)
* [bilduppsättning](r-imageset-req.md)
* [img](r-img.md)
* [loadCache](r-loadcache.md)
* [map](r-map-req.md)
* [mask](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [proppar](r-props.md)
* [lös](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [mål](r-targets.md)
* [tmb](r-tmb.md)
* [användardata](r-userdata.md)
* [validera](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Om inget annat anges i de detaljerade beskrivningarna returnerar servern `text` svar med MIME-typen `text/plain`. I många typer av förfrågningar kan du ange en svarstyp, till exempel `text`, som vanligtvis är standard, `javascript`, `xml` eller `json`. De associerade MIME-svarstyperna är `text/plain`, `text/javascript`, `text/xml` och `text/javascript`.

Om inget annat anges formaterar svaren som en uppsättning `name=value`-par.

Se [Egenskaper](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
