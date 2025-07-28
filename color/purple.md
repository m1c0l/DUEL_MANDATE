# Purple

Up until today, I had internalized the fact that red + blue = purple. Specifically, a dark purple:
![Columns of red, blue, purple](https://www.schemecolor.com/images/scheme/red-blue-purple.png)

I had learned this from elementary school art class, where we'd mix paints, crayons, markers, on and on, and mixing red and blue pigments results in purple.

But today I was reviewing the RGB colors that computers display, and in RGB, combining red and blue (each at 255, their max values) results in _magenta_:

![Magenta](https://www.computerhope.com/cdn/html-color-codes/magenta.png)

## Why the difference? Pigments vs pixels

First we need to ask, how do we see color? The light coming from the paint or screen enters our eyes and hits photoreceptor cells in the retina, which are attuned to different wavelengths of light: short cones for blue, medium cones for red, large cones for green. TODO: rods?

![Cones and rods](https://ars.els-cdn.com/content/image/3-s2.0-B9780128042540000077-f07-12-9780128042540.jpg)

Many screens consist of red, green, and blue subpixels which you can see with a magnifying glass, like LCDs:
![subpixels of the letter e](https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/Subpixel_rendering_LCD_photo_3e_composite.jpg/500px-Subpixel_rendering_LCD_photo_3e_composite.jpg)

The light (or lack thereof) coming from the 3 subpixels _adds up_ to the final color you see from that pixel: black if none are on, solid red if only the red is on, solid white if all 3 are on, or solid magenta if both the red and blue subpixels are on. You can also see that the subpixels also can be somewhat translucent, especially at the edges of the 'e.'

On the other hand, pigments like paint aren't directly emitting light; rather they're absorbing ambient light, and some fraction of it gets reflected back into your eye. A black paint coat absorbs all light, while a red paint absorbs all light _except_ the wavelength corresponding to red; the paint's color that you see has _subtracted_ from the ambient light.

When you mix two different paints (say red and blue), it's like doing 2 successive subtractions: the resulting paint absorbs both non-red and non-blue colors. It _absorbs more light wavelengths_ and so it reflects less light, appearing darker to your eye (plus the hue has shifted).
