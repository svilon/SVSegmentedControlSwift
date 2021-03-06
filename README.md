# SVSegmentedControlSwift

[![Version](https://img.shields.io/cocoapods/v/SVSegmentedControlSwift.svg?style=flat)](http://cocoapods.org/pods/SVSegmentedControlSwift)
[![License](https://img.shields.io/cocoapods/l/SVSegmentedControlSwift.svg?style=flat)](http://cocoapods.org/pods/SVSegmentedControlSwift)
[![Platform](https://img.shields.io/cocoapods/p/SVSegmentedControlSwift.svg?style=flat)](http://cocoapods.org/pods/SVSegmentedControlSwift)

This control was created to solve issue, that native UISegmentedControl has. Reffer to SVSegmentedControl for obj-c version.
UISegmentedControl has issue with apportionsSegmentWidthsByContent setting (adjust segments width proportionally to content). Often, it appears that control bounds are wider, than actual segments width. See screenshot bellow - I put yellow color as layer background.

![UISegmentedControl](https://github.com/svilon/SVSegmentedControlSwift/blob/master/Screens/UISegmentedControl.png)

With SVSegmentedControl issue is fixed and same segmented control will look like:

![SVSegmentedControl](https://github.com/svilon/SVSegmentedControlSwift/blob/master/Screens/SVSegmentedControl.png)

Also, SVSegmentedControl introduces “smart” mode, where, if there is enough room, every segment, that needs to be wider than average width, gets enough room to display content (which is usually less then in proportional mode). If there is no enough room for all content - segments width is distributed proportionally (fixed, of course :) ).

NOTE. SVSegmentedControl is designed and test only to work with segments with titles, not with images.

## Usage
SVSegmentedControl provides two new properties to adjust it's behaviour:
* @IBInspectable public var fixNativeProportionalSizing: Bool = false
* @IBInspectable public var smartAdjustment: Bool = false

As you can see, you can change them in runtime, or configure in IB.

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

## Installation

SVSegmentedControlSwift is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SVSegmentedControlSwift"
```

## Author

Eugene Shevtsov, i.i.shevtsov@gmail.com

## License

SVSegmentedControlSwift is available under the MIT license. See the LICENSE file for more info.
