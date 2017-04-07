## Programming Considerations
 
![RGButterfly Logo](images/RGButterfly_Logo.png) This section gives an overview of the program structure and development process.

### Platform

The App is currently implemented to run on ___iPhone___ devices ([_iOS_](https://en.m.wikipedia.org/wiki/IOS) v10.x) with development using the [_XCode_](https://developer.apple.com/xcode/) IDE. Consideration has been given to extending this App to other platforms and venturing into multi-platform environments such as [_Xamarin_](https://www.xamarin.com/) for future Apps development.

### Language

Work started on this application back in 2014, shortly after I got into iOS development. Though Apple was just switching to the [_Swift_](https://developer.apple.com/swift/) programming language, I decided to continue implementing in [_Objective-C_](https://en.m.wikipedia.org/wiki/Objective-C) since, at the time, Swift was still relatively untested and provided fewer online resources. Fortunately Apple was expected to continue supporting Objective-C into the forseeable future and, more importantly, the Swift design allowed its libraries to be easily integrated into Objective-C applications allowing for a gradual transition (I have since started going in this direction)

### XCode IDE

The experience of using XCode for App development has been largely positive and I have personally found this IDE to be superior to many of the others I have used in the past including Eclipse and IntelliJ. It took a while gettings used to Objective-C and the many IDE abstractions (such as XCode _groups_ used to structure the App components) especially coming from a Software Engineering background where much of my work was backend, often at the Linux OS level, and in many cases using scripting/interpretive languages.

### Structure

The main project (currently private) integrates a number of private GitHub repos as well as libraries from the [_IOS Utilities_](https://github.com/spineo/ios-utilities), [_IOS Algorithms_](https://github.com/spineo/ios-algorithms), [_IOS Custom Cells_](https://github.com/spineo/ios-custom-cells), and [_RGButterfly Tests (Swift)_]( https://github.com/spineo/rgbutterfly-tests) public repos. Over time, as I refactored the code, it made sense create these separate frameworks of potentially resuable code (the plan is to eventually make all repos public). The down side of this approach has been needing to now integrate more than one GitHub repo into the application (something that is fortunately automatically done in XCode) and tagging the many repos. Since I have been the only developer on this project, I have generally worked off of the _Master_ branch except for a few occasions earlier on.
