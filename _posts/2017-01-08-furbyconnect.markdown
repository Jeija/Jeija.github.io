---
layout: single
title:  "Reverse Engineering Furby Connect's Bluetooth Protocol"
date:   2017-01-08 18:00:00 +0100
categories: wireless Furby
---

Some of my earlist memories from being a toddler was my cousin having a Furby, so naturally I also really wanted to have one.
When most children finally get one of these little monsters, feeding and petting Furby keeps them busy for a week or so until they get bored and move on to something new.
For me, however, the fascination never really faded.

So last Christmas, I gifted myself with Hasbro's new "Furby Connect" that comes with a Bluetooth Low Energy (BLE) interface.
Smart toys equipped with BLE just ask to be hacked, so I was quite surprised when I found out that there are no security checks whatsoever in place to protect Furby against someone uploading and playing arbitrary audio.
But see for yourself:

<div style="margin-bottom: 1em">
	<iframe src="https://www.youtube-nocookie.com/embed/FkblA_CxHgU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

You can find more information about this project on [its GitHub page](https://github.com/Jeija/bluefluff).
