## Programming Considerations
 
![RGButterfly Logo](images/RGButterfly_Logo.png) This section gives an overview of the program structure and development process.

### Platform

The App is currently implemented to run on ___iPhone___ devices ([_iOS_](https://en.m.wikipedia.org/wiki/IOS) v10.x) with development using the [_XCode_](https://developer.apple.com/xcode/) IDE. Consideration has been given to extending this App to other platforms and venturing into multi-platform environments such as [_Xamarin_](https://www.xamarin.com/) for future Apps development.

### Language

Work started on this application back in 2014, shortly after I got into iOS development. Though Apple was just switching to the [_Swift_](https://developer.apple.com/swift/) programming language, I decided to continue implementing in [_Objective-C_](https://en.m.wikipedia.org/wiki/Objective-C) since, at the time, Swift was still relatively untested and provided fewer online resources. Fortunately Apple was expected to continue supporting Objective-C into the forseeable future and, more importantly, the Swift design allowed its libraries to be easily integrated into Objective-C applications allowing for a gradual transition (I have since started going in this direction)

### XCode IDE

The experience of using XCode for App development has been largely positive and I have personally found this IDE to be superior to many of the others I have used in the past including Eclipse, IntelliJ, and Visual Studio. It took a while getting used to Objective-C and the many IDE abstractions (such as XCode _groups_ used to structure the App components) especially coming from a Software Engineering background where much of my work was at the Linux OS level and often using scripting/interpretive languages.

A couple of notes about XCode. It can only be run on MacOS and is easier to use on a larger screen. That being said, while I prefer XCode development on my iMac I have found no significant hurdles to using it on my 13 inch MacBook Pro.

### GitHub Integration

The main project (currently private) integrates a number of private GitHub repos as well as libraries from the [_IOS Utilities_](https://github.com/spineo/ios-utilities), [_IOS Algorithms_](https://github.com/spineo/ios-algorithms), [_IOS Custom Cells_](https://github.com/spineo/ios-custom-cells), and [_RGButterfly Tests (Swift)_]( https://github.com/spineo/rgbutterfly-tests) public repos. Over time, as I refactored the code, it made sense create these separate frameworks of potentially resuable code (the plan is to eventually make all repos public). The down side of this approach has been needing to now integrate more than one GitHub repo into the application (something that is fortunately automatically done in XCode) and tagging the many repos. Since I have been the only developer on this project, I have generally worked off of the _Master_ branch except for a few occasions earlier on in the project.

### Issue Tracking

One of the first tasks I integrated into the development process was Issue tracking. Though in the past I have used many commercial/open source issue tracking systems any of which I would highly recommend for multi-developer environments, I felt that using such a system for this one-man project was overkill. The system I came up with uses a simple Excel Spreadsheet with five sheets (or tabs): _Active_, _Pre-Release_, _Post-Release_, _Completed_, and _Next Release_ issues.

### App Design

Several months were spend on the _App Design_. The process that followed is outlined below:

1. ___Design the initial Wire Diagram___: The 'Wire Diagram' was a schematic drawn on a large whiteboard. While the initial diagram did not take long to complete (maybe about an hour) it was the result of weeks of brainstorming and successfully outlined my vision. I would often tweak the drawing as I worked out my main features.

2. ___Detail the Main Features___: This step involved writting down in a spreadsheet the key features I wanted to implement. I often refered to this document (along with the _Issue Tracking Spreadsheet_) while implementing the _Proof-of-Concept_ outlined below.

2. ___Implement a Proof-of-Concept Prototype (POC)___: My first questions was _Can the key features be implemented and produce the expected results?_ The best way to find out was to implement a simple POC that integrated these features, among them the _Match Algorithms_. My target was an _iPad_ App and, despite a few bugs, it produced the results I hoped for and lay down the ground work for the next step. 

3. ___Create the Mockup Application Prototype (MAP)___: By now I just about knew exactly what I wanted but instead of diving into the implementation, I was hoping that creating a MAP would allow me to more easily set up the UI, Control, and Navigation for a "finished" App without the time expenditure generally involved in developing. For this I turned to [___AppCooker___](https://itunes.apple.com/us/app/appcooker-prototyping-mockup-studio-for-ios/id418861662?mt=8), a MAP tool for the iPad. The $20 I invested on this App was well worth the cost. The tool allowed me to lay out the various controllers and UI elements in a way similar to an XCode [_Storyboard_](https://developer.apple.com/library/content/documentation/General/Conceptual/Devpedia-CocoaApp/Storyboard.html) and simulate many of the real App interactive elements such as  _Actions_, [_Segues_](https://developer.apple.com/library/content/featuredarticles/ViewControllerPGforiPhoneOS/UsingSegues.html) and _Navigation_. Even though the MAP took several weeks to complete the finished framework served as an invaluable reference that helped, without a doubt, speed up the development process.

### Data Model
