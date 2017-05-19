# [RGButterflyDocs](http://rgbutterfly.com/)

## Overview

[![RGButterfly Logo](images/RGButterfly_Logo.png)](http://rgbutterfly.com) The main purpose of this iPhone App is to suggest Acrylic paints associated with tapped areas in a photo. It does this by applying a selected _Match Algorithm_ against a database of reference paints, paint mixes, and generic paint references. A key word is _attempt_
as there is much variability in the process and the results obtained will often be far from what you might expect (please review the [__Reference Data and Methodology__](About.md) and [__Disclaimer__](Disclaimer.md) sections to learn more)

The three main tasks this App performs are __Reference & Search__, __Image Area(s) Match__ against a reference database, and the __Paints Data Capture__.

### Reference & Search

The Initial View allows a user to switch between the five types of displays (shown in the screenshots that follow):
* __Color Associations__: An ordered list of collections each representing a _Mix, Coverage, or Generic Association_
* __Match Associations__: An ordered list of collections each representing a _Match Association_
* __Individual Colors__: An ordered list of individual colors (mainly reference and mix paint swatches)
* __Keywords Listing__: An alphabetized list of keywords and their associated reference or paint mixes
* __Subjective Colors__: A list of color categories and their associated reference or paint mixes

For each of the associations (first two screenshots below), scrolling right to left exposes remaining elements of the collection view and clicking on any of the rows reveals the [__Association Detail__](Associations.md). For the [__Individual Colors__](Individual.md) listing (third screenshot), clicking on a row takes you directly to the [__Detailed View__](Detail.md) for that _Mix_ or _Reference_ swatch.

![Assoc, Match, and All Views](images/Assoc_Match_and_AllViews.jpg)

Rotating to landcape, as shown below, makes it easier to read the full names. Something especially useful for mixes, which use a longer display name that includes the two references and mix ratio.

![All Portrait and Landscape](images/All_Port_and_LandView.jpg)

The _Keywords Listing_ (first two screenshots below) allows users to search for keywords and find their associated references and/or mixes. The _Subjective Colors_ listing (third screenshot) categorizes colors into groups (similar to a _Color Wheel_). In this view, the elements of one or more groups can be revealed/hidden by clicking on the corresponding down/up arrow widgets (as shown below) or, alternatively, all groups can be revealed/hidden by clicking on the arrow widget on the top Navigation Toolbar.

![Keyw and Subj Views](images/Keyw_and_SubjViews.jpg)

All listings, with the exception of _Subjective Colors_ are alphabetized and include the top-right magnifier __Search__ button (search rules are somewhat different for each type of listing). In addition, the _Individual Colors_ and _Keywords Listing_ also provide an __Alphabetical Index__ widget for quick access.

### Image Area(s) Match

A new photo can be taken or and existing image used for the Image Match. The screenshots below show the general sequence of events for this type of data capture. More detailed examples of this functionalithy can be found __[here](ImageMatch.md)__.

![MatchViews](images/MatchViews.jpg)


### Paints Data Capture

Photographed paint swatch areas can be tapped and integrated into a _Mix Association_ as shown in the screenshots below. The _Add Color Mix_ feature (screenshots 2 & 3) allows users to add existing reference colors to the mix. A more detailed session used for this type of data capture can be found __[here](DataCapture.md)__.

![DataCapture](images/ManualDataCapture.jpg)

### Settings

The Settings Controller, accessible from the gear button (bottom right on most views), allows a number of global App customizations. Other "Non-Settings" features embedded in this controller include the _About this App_ and _Disclaimer_ pages, Links to the _Web Documentation_ (GitHub Pages), Email _Provide Feedback_ link, and documentation _Share_ buttons which enable distribution using any share-able App (such as Facebook, Twitter, Messenger, and Email) that user has access to. More on this controller, including screenshots, can be found [__here__](Settings.md). 


### Privacy, Access and Alerts

This App does not store user or location information. Specific privacy settings must be enabled in order to access the Camera or Photo Library. Alerts cover a variety of use cases (though most alerts are informational). More content related to _Access and Alerts_ can be found __[here](AccessAndAlerts.md)__.  

### Programming Considerations

[__This__](Programming.md) section gives a mostly high-level overview of the program structure and development process.

### Future Directions

Though App has not been released, there are a number of new features that I am looking to implement as well as existing ones that I plan to revisit sometime down the road. Some of the main ones include:

* __Continue Improving the Data Capture__
* __Extend the Dataset__ by adding Paints and additional Keywords associations
* Continue __Improving the Match Algorithms__ and perhaps even look into data derivation formulas
* Consider __Deployment to Other Platforms and/or Device Types__
* Address __Internationalization/Localization__ issues
* __Improve Usability__ (covers things like improvements to the UI/Graphics and new User Settings, such as Fonts and Thumbnail sizes)
* __Revisit the Current Data Storage Model__ (perhaps consider centralized data storage and queries)
* In some ways similar to the preceding point, __make it easy to share swatch data__

For questions/comments about this App please email me at [svpineo@gmail.com](mailto:svpineo@gmail.com)

_Note: Clicking on this ![RGButterfly Logo](images/RGButterfly_Logo.png) logo will get you back to this main page_.

