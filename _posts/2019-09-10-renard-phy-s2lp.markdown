---
layout: single
title:  "Open Sigfox Stack for STMicroelectronics S2-LP"
date:   2019-09-10 9:00:00 +0200
categories: wireless sigfox
---

Late last year I published [`librenard`](https://github.com/Jeija/librenard), an open-source Sigfox stack implementation based [on my reverse engineered Sigfox specifications](/sigfox). In the meantime, [Sigfox have also officially opened their specs](https://build.sigfox.com/sigfox-device-radio-specifications), confirming my own research.

`librenard` was written with portability in mind, making it possible to run it both as part of a tool such as [`renard`](https://github.com/Jeija/renard) (CLI encoder / decoder for Sigfox) as well as part of microcontroller applications. However, there have not been any attempts to actually use `librenard` on a microcontroller together with a dedicated RF transceiver IC so far (at least that I am aware of).

This is changing now with the release of [`renard-phy-s2lp`](https://github.com/jeija/renard-phy-s2lp), which integrates `librenard` with a driver for the STMicroelectronics S2-LP ultra-low power RF transceiver. Thanks to interchangeable hardware abstraction layers, `renard-phy-s2lp` is independent of the microcontroller platform. So far, it has been tested with an STM32L0 development board ([STEVAL-FKI868V2](https://www.st.com/en/evaluation-tools/steval-fki868v2.html)) and Espressif's ESP32.

`renard-phy-s2lp`, the hardware abstraction layers and demo applications are all permissively licensed, so feel free to embed them in your IoT application. I'd still be happy to merge any improvements you make upstream!
