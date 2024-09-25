# Fire2023
A fire effect for LED strips, based on Fire2012 with some improvements

The Fire2012 effect is great, because it is easy to used and looks reasonably realistic.

I was not entirely happy with the effect and I wanted it to run on an Attiny. 
And while I tried to change details, it got worse.

So I had to whitebox the entire code: Now it is in controller-friendly form. I did not achieve that it runs on an Attiny, but I am happy with it now.

Main improvements: Detailed comments on what line does what, better fire-like color palette, softer animation and better control over the details of the fire.

I tried applying it on a 6-LED-lamp, it worked (albeit, the big code really is not necessary there), and I tried to apply it to a 100-pixel-torch, and it worked.

This variant here is the one applied to the 100-pixel-torch, running on an ESP32.


