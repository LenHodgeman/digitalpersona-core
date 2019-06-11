---
layout: default
title: Usage
has_toc: false
has_children: true
permalink: /usage  
nav_order: 2
---
###### [DigitalPersona Access Management API ](https://lenhodgeman.github.io/digitalpersona-access-management-api/)/ Core Components / Usage / Overview  

![](../../docs/assets/HID-DPAM-Core.png)
### Usage

DigitalPersona Device Access (DP DA) is a Windows service and a user agent application running
locally on a user device and providing access to authentication devices like fingerprint readers,
smarrtcard readers etc. These devices are not directly accessible from Javascript running in a browser.
The `device-access.js` library communicates with the DP DA agent via a secure message channel,
allowing to implement composite authentication in web pages.

* [Details](details.md)
* [Tutorial](tutorial.md)
* [Examples](examples.md)
* [How-to](how-to.md)
* [Reference](reference.md)

Draft C17
