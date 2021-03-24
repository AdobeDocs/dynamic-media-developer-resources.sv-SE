---
description: Typ av begäran. Anger typen av begäran.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '98'
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
