sample-ios-ChildView
===================

This example shows you how to __embed__ a CoronaView into an existing view hierarchy. 

# Code Overview

## CoronaView setup (Obj-C)

The CoronaView is instantiated just like any normal UIView. A `CoronaView` is paired with an instance of `CoronaViewController`.

This example sets up the `CoronaViewController` as a child of `ViewController` which is the root view controller for the app. This enables the `CoronaView` to be inserted anywhere in the view hierachy of the app.

## CoronaView contents (Lua)

The contents of the `CoronaView` are determined via Lua. In this project, the `CoronaView` is told to look for Lua files in the `Corona` subfolder of the .app bundle. 

NOTE: The Xcode project is setup to automatically copy the contents of `ChildView/Corona` to a `Corona` subfolder in the destination .app bundle, so you are free to modify/add/delete the Lua files as well as other asset files.


# Setup

The sample expects `CoronaKit.framework` to be installed at `/Users/Shared/CoronaLabs/ios/CoronaKit.framework`. 


# Requirements

* Xcode 5
* Mac OS X 10.8 or higher


# Version Notes

If you are using an older version of CoronaKit (2014.2174 and earlier), you will need to modify the Xcode project with the following settings:

* Dead Code Stripping: `NO`
* Other Linker Flags: `-ObjC -all_load -lobjc -lsqlite3`
