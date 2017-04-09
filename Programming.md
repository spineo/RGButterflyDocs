## Programming Considerations
 
![RGButterfly Logo](images/RGButterfly_Logo.png) This section gives an overview of the program structure and development process.

### Platform

The App is currently implemented to run on ___iPhone___ devices ([_iOS_](https://en.m.wikipedia.org/wiki/IOS) v10.x) with development using the [_XCode_](https://developer.apple.com/xcode/) IDE. Consideration has been given to extending this App to other platforms and venturing into multi-platform environments such as [_Xamarin_](https://www.xamarin.com/) for future Apps development.

### Language

Work started on this application back in 2014, shortly after I got into iOS development. Though Apple was just switching to the [_Swift_](https://developer.apple.com/swift/) programming language, I decided to continue implementing in [_Objective-C_](https://en.m.wikipedia.org/wiki/Objective-C) since, at the time, Swift was still relatively untested and provided fewer online resources. Fortunately Apple was expected to continue supporting Objective-C into the forseeable future and the Swift API allowed its libraries to be easily integrated into Objective-C applications making a gradual transition easier (I have since started going in this direction)

### XCode IDE

The experience of using XCode for App development has been largely positive and I have found this IDE to be superior to many of the others used in the past including Eclipse, IntelliJ, and Visual Studio. It took a while getting used to Objective-C and the many IDE abstractions (such as XCode _groups_ used to structure the project tree) especially coming from a Software Engineering background where much of my work was at the Linux OS level mostly using scripting/interpretive languages.

A couple of notes about XCode. It is better run on MacOS systems and is easier to use on a larger screen. That being said, while I prefer XCode development on my iMac it also works fine on my 13 inch MacBook Pro with a bit of juggling.

### GitHub Integration

The main project (currently private) integrates a number of private GitHub repos as well as libraries from the [_IOS Utilities_](https://github.com/spineo/ios-utilities), [_IOS Algorithms_](https://github.com/spineo/ios-algorithms), [_IOS Custom Cells_](https://github.com/spineo/ios-custom-cells), and [_RGButterfly Tests (Swift)_]( https://github.com/spineo/rgbutterfly-tests) public repos. Over time, as I refactored the code, it made sense create these separate frameworks of potentially resuable code (the plan is to eventually make all repos public). The down side of this approach has been needing to now integrate more than one GitHub repo into the application (something that is fortunately automatically done in XCode) and tagging the many repos. Since I have been the only developer on this project, I have generally worked off of the _Master_ branch except for a few occasions earlier on in the project.

### Issue Tracking

One of the first tasks was to integrate into the development process Issue tracking. __This is something I would highly recommend for any medium to large project__. Though in the past I have used many commercial/open source issue tracking systems any of which would do the trick in multi-user environments, I felt that using such a system for this one-man project was overkill. The system I came up with uses a simple but effective Excel Spreadsheet with five sheets named _Active_, _Pre-Release_, _Post-Release_, _Completed_, and _Next Release_.

For each sheet I included six columns:
* __Task ID__: A numeric id prefixed by _F_ (Feature) or _B_ (Bug) (the Task ID should also be reference in the Git commits)
* __Component__: Structural or functional component(s) the Feature or Bug affects
* __Description__: Brief description of the problem
* __Status__: Completions Status (i.e., PEND, IN PROG, DONE, or ABAND)
* __Priority__: Work priority starting at 20 with 1 assigned to DONE/ABAND (sheets are _desc_ sorted by this column ensuring that high priority items bubble to the top and DONE/ABAND ones to the bottom)
* __Comments__: Additional comments such as completion status or references

The workflow is simple: New issues are generally added to the _Active_ sheet and DONE/ABAND ones get transferred to _Completed_. Issues tied to the Pre/Post-Release time-frames or slated for a future release get moved to the appropritate sheet or added directly to those sheets. To enhance readability selected rows are also color coded (i.e., yellow IN PROG and gray DONE/ABAND).

### App Design

Several months were spend on the _App Design_. The process that followed is outlined below:

1. ___Design the initial Wire Diagram___: The 'Wire Diagram' was a schematic drawn on a large whiteboard. While the initial diagram did not take long to complete (maybe about an hour) it was the result of weeks of brainstorming and successfully outlined my vision. I would often tweak the drawing as I worked out my main features.

2. ___Detail the Main Features___: This step involved writting down in a spreadsheet the key features I wanted to implement. I often refered to this document (along with the _Issue Tracking Spreadsheet_) while implementing the _Proof-of-Concept_ outlined below.

2. ___Implement a Proof-of-Concept Prototype (POC)___: My first questions was _Can the key features be implemented and produce the expected results?_ The best way to find out was to implement a simple POC that integrated these features, among them the _Match Algorithms_. My target was an _iPad_ App and, despite a few bugs, it produced the results I hoped for and lay down the ground work for the next step. 

3. ___Create the Mockup Application Prototype (MAP)___: By now I just about knew exactly what I wanted but instead of diving into the implementation, I was hoping that creating a MAP would allow me to more easily set up the UI, Control, and Navigation for a "finished" App without the time expenditure generally involved in developing. For this I turned to [___AppCooker___](https://itunes.apple.com/us/app/appcooker-prototyping-mockup-studio-for-ios/id418861662?mt=8), a MAP tool for the iPad. The $20 I invested on this App was well worth the cost. The tool allowed me to lay out the various controllers and UI elements in a way similar to an XCode [_Storyboard_](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/Storyboard.html) and simulate many of the real App interactive elements such as  _Actions_, [_Segues_](https://developer.apple.com/library/content/featuredarticles/ViewControllerPGforiPhoneOS/UsingSegues.html) and _Navigation_. Even though the MAP took several weeks to complete the finished framework served as an invaluable reference that helped, without a doubt, speed up the development process.

### Data Model

_Data_ is key to this application and this App is built on [_Core Data_](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/CoreData/index.html?utm_source=iosstash.io). A significant amount of time was spent developing the data model (and the many interfacing [_NSManagedObject_](https://developer.apple.com/reference/coredata/nsmanagedobject) sub-classes) even before diving, at least to a significant extent, into the UI controllers and views.

The data model is currently at major version 63 and is composed of 20 entities (each mapping to a _table_ in the backend [_SQLite_](https://www.sqlite.org) store). The NSManagedObject classes provide many of the key operations (i.e., Object or NSSet get/set, add, remove) against the _Entities_, _Attributes_, and/or _Relations_. Additional custom methods were also implemented with a few  generic ones packaged in the [_CoreDataUtils_](https://github.com/spineo/ios-utilities/blob/master/CoreDataUtils.m) class but most currently private.

Since most of the controllers in this App are [_TableView_](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html) Controllers the [_NSFetchedResultsController_](https://developer.apple.com/reference/coredata/nsfetchedresultscontroller) API is used frequently as it provides the built-in callback methods to populate the _TableViews_.

The initial [_ER_](https://en.m.wikipedia.org/wiki/Entity–relationship_model) relations were captured using a graphing application. After the initial implementation, additions/modifications were implemented directly by using the CoreData built-in Data Modelling tool.
