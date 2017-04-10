## The Reference Data and Match Methodology
 
[![RGButterfly Logo](images/RGButterfly_Logo.png)](https://spineo.github.io/RGButterflyDocs/) This experimental App (currently private) grew out of my interest in painting and aims to help users find acrylic color paint matches associated with selected areas of a photo. It does this by applying a selected _Match Algorithm_ against a database of reference paints and paint mixes.

### The Reference Data

The Paint Swatch Database is currently comprised of about 2,500 paint references and mixes each of them created manually (screenshots below show three sample sheets). For accuracy, 1 ml syringes were used to accurately measure/dispense the paint and cotton swabs to carefully mix them (for this version, only two-color mixes were created though the App functionality supports using a "mix" as reference for a three-way or multi-color mix)

![Sample Paint Swatches](images/ColorSheets.jpg)

The paint was applied on acid-free, triple-primed white canvas paper in generally thick layers or _Thick_ as set in the "Canvas Coverage" property. Paint coverage might also be specified as _Thin_ or _Sparse_ (these latter two categories usually the result of using less paint and/or transparent or translucent paints)

After the paint swatches sheets were created they were photographed. For lighting consistency, this was done with pre-dominantly artificial light, at the same time of day for each sheet, and in a way that eliminated reflection as much as possible. Photographed swatches were then entered manually using the app _Mix Association_ feature and the individual properties of each swatch set in the App _Paint Swatch Detail_ View (and example data capture session is shown __[here](DataCapture.md)__)

### The Match Methodology

The user may apply seven algorithms to find one or more potential matches. Each algorithm compares the tap area against the database of swatches to yield a difference (d). The smaller the _d_ value the better the match is assumed to be. The algorithms, based on RGB and/or HSB color properties, are shown below:

* RGB only or default:

   _d = sqrt((r2-r1)^2 + (g2-g1)^2 + (b2-b1)^2)_


* HSB only:

   _d = sqrt((h2-h1)^2 + (s2-s1)^2 + (b2-b1)^2)_


* RGB and Hue:

   _d = sqrt((r2-r1)^2 + (g2-g1)^2 + (b2-b1)^2 + (h2-h1)^2)_


* RGB + HSB:

   _d = sqrt((r2-r1)^2 + (g2-g1)^2 + (b2-b1)^2 + (h2-h1)^2 + (s2-s1)^2 + (b2-b1)^2)_


* Weighted RGB:

   _d = ((r2-r1)*0.30)^2 + ((g2-g1)*0.59)^2 + ((b2-b1)*0.11)^2_


* Weighted RGB + HSB:

   _d = ((r2-r1)*0.30)^2 + ((g2-g1)*0.59)^2 + ((b2-b1)*0.11)^2 + (h2-h1)^2 + (s2-s1)^2 + (b2-b1)^2_


* Hue only:

   _d = sqrt((h2-h1)^2)_


I found that though some of these algorithms (in particular the RGB method) consistently produced the best results others might perform slightly better at different RGB/HSB ranges. All algorithms do consistently produce better results matching darker colors than lighter ones so I am still working on improvements to the accuracy, in particular, relating to lighter values.

[![RGButterfly Logo](images/RGButterfly_Logo.png)](https://spineo.github.io/RGButterflyDocs/) For questions/comments about this App please email me at [svpineo@gmail.com](mailto:svpineo@gmail.com)
