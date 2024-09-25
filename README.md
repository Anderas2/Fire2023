# Fire2023
A fire effect for LED strips, based on Fire2012 with some improvements.

The Fire2012 effect is great, because it is easy to used and looks reasonably realistic.

I was not entirely happy with the effect and I wanted it to run on an Attiny. 
And while I tried to change details, it got worse.

So I had to whitebox the entire code: Now it is in controller-friendly form. I did not achieve that it runs on an Attiny, but I am happy with it now.

Main improvements: Detailed comments on what line does what, better fire-like color palette, softer animation and better control over the details of the fire.

I tried applying it on a 6-LED-lamp, it worked (albeit, the big code really is not necessary there), and I tried to apply it to a 100-pixel-torch, and it worked.

## The physical project
This variant here is the one applied to the 100-pixel-torch, running on an ESP32.
You can watch it in action here 
[![Torch](https://img.youtube.com/vi/a_Wr0q9YQs4/0.jpg)](https://www.youtube.com/watch?v=a_Wr0q9YQs4)

Internally it looks like this

![Torch internal](https://github.com/Anderas2/Fire2023/blob/main/PXL_20240925_094213321.jpg)

## about the code
The "Fire" uses two layers of Perlin noise. 
Perlin is nice, as it is not totally random, but looks like a cloud. That's practical, because fire is just a glowing cloud that moves upwards.

So we have one perlin "cloud" that moves upwards and uses firery colors from a color palette while it "cools down".
Another perlin "cloud" moves in front of the fire and simulates smoke moving across the fire. 
Basically, that's all!

Many of the parameters in the code depend on your LED layout - a thin but long led layout needs other speed, "heat", cloud, everything than a wide but short LED layout. If you use few LED, the animation is barely visible, then you rather need a "blinky" style, if you have many and the movement becomes visible, you maybe prefer a "soft" style.
Just try until you find your ideal. 

Have fun!
Andreas
