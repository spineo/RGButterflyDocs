## Programming Considerations
 
![RGButterfly Logo](images/RGButterfly_Logo.png) This section gives an overview of the program structure and development process.

### Platform

The App is currently implemented to run on ___iPhone___ devices ([_iOS_](https://en.m.wikipedia.org/wiki/IOS) v10.x). The experience of developing using [_XCode_](https://developer.apple.com/xcode/) has been largely positive and have found this IDE to be superior to many of the others I have used in the past including Eclipse and IntelliJ. Consideration has been given to extending this App to other platforms and venturing into multi-platform environments such as [_Xamarin_](https://www.xamarin.com/) for future Apps development.

### Language

Work started on this application back in 2014, shortly after I got into iOS development. Though Apple was just switching to  the [_Swift_](https://developer.apple.com/swift/) programming language, I decided to continue implementing in [_Objective-C_](https://en.m.wikipedia.org/wiki/Objective-C) as, at the time, Swift was still relatively untested and provided fewer online resources. Apple was also expected to continue support for Objective-C into the forseeable future and, more importantly, Swift design allowed its libraries to be easily integrated into Objective-C applications making postponing such transition to a later date easier (a move that I have already started doing)

### Structure

The main project (currently private) integrates a number of private GitHub repos as well as libraries from the [_IOS Utilities_](https://github.com/spineo/ios-utilities), [_IOS Algorithms_](https://github.com/spineo/ios-algorithms), [_IOS Custom Cells_](https://github.com/spineo/ios-custom-cells), and [_RGButterfly Tests (Swift)_]( https://github.com/spineo/rgbutterfly-tests) public repos. Over time, as I refactored the code, it made sense create these separate frameworks of potentially resuable code (the plan is to eventually make all repos public)
