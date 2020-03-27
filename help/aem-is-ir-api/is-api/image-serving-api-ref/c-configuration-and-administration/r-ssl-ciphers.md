---
description: Taggen Connector i server.xml har stöd för ett ciphers-attribut som begränsar antalet ciphers som kan väljas för en SSL-anslutning.
seo-description: Taggen Connector i server.xml har stöd för ett ciphers-attribut som begränsar antalet ciphers som kan väljas för en SSL-anslutning.
seo-title: Definiera SSL-ciphers
solution: Experience Manager
title: Definiera SSL-ciphers
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Definiera SSL-ciphers{#defining-ssl-ciphers}

Taggen Connector i server.xml har stöd för ett ciphers-attribut som begränsar antalet ciphers som kan väljas för en SSL-anslutning.

Som standard är alla ciphers tillgängliga. Listan är kommaavgränsad och kan innehålla något av följande värden:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Om något av värdena är fel aktiverar Tomcat alla klipp. Därför är det viktigt att du kontrollerar med ett externt verktyg efter konfigurationen för att se vilka utbildare som är aktiverade.

Som ett exempel aktiverar följande konfiguration endast chiffersviterna &quot;128 bitar&quot; och högre:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
