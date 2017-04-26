## Association Types
 
[![RGButterfly Logo](images/RGButterfly_Logo.png)](https://spineo.github.io/RGButterflyDocs/) There are three types of associations created through the manual or bulk [__data capture__](DataCapture.md) methods:

* ___Coverage___ associations, as shown in the first screenshot below, are related paint _references_ with varying HSB/RGB values, each the result of a different paint application process (i.e., in a _thin_ application, if the underlying canvas shows through, it will yield different values than a _thick_ application that fully blocks the canvas)

* ___Mix___ associations (screenshot 2) are produced by mixing two _reference_ paints (first two rows). Each resulting mix (remaining rows) captures a unique representation of the two references (as defined by a _mix ratio_) which is based on the proportion of each reference used to create the mix.

* ___Generic___ associations (final screenshot) are related _named_ swatches that are not associated with a specific paint reference or mix. They are used as "fillers" to identify a color by name during the matching process in the absence of a close paint match. While most Generic associations group the colors by where they might fall in the color wheel, any association rule can be used when creating these assocations.

These assocations are implemented as collection views with no size limitations. Some are as small as 2 (typically Coverage assocations) or may contain well over 100 items as is the case with a few of the Generic assocations.

[Association Types](images/AssociationTypes.jpg)

[![RGButterfly Logo](images/RGButterfly_Logo.png)](https://spineo.github.io/RGButterflyDocs/)
