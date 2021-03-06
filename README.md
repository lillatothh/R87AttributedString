# R87AttributedString

[![Version](https://img.shields.io/cocoapods/v/R87AttributedString.svg?style=flat)](http://cocoadocs.org/docsets/R87AttributedString)
[![License](https://img.shields.io/cocoapods/l/R87AttributedString.svg?style=flat)](http://cocoadocs.org/docsets/R87AttributedString)
[![Platform](https://img.shields.io/cocoapods/p/R87AttributedString.svg?style=flat)](http://cocoadocs.org/docsets/R87AttributedString)

## Introduction

With the help of R87AttributedString you can format attributed texts easily.

For example you can add the thext #like this# or *like this* and you can specify from code how the text inside the # and * characters should look like.

![Screenshot](/Screenshots/Screenshot-01.png)

## Installation

R87AttributedString is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'R87AttributedString'
```

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

You can use the librarly like this:

```obj-c
NSString *textString = @"*CocoaPods Events*\n\n#Code of Conduct#\nAll attendees, speakers, sponsors and volunteers...";
NSDictionary *defaultTextAttributes = @{
	NSForegroundColorAttributeName: [UIColor blackColor],
	NSFontAttributeName: [UIFont systemFontOfSize:14.0],
};
NSMutableAttributedString *text = [[NSMutableAttributedString alloc] initWithString:textString attributes:defaultTextAttributes];

[text r87_addAttributes:@{
	NSFontAttributeName: [UIFont boldSystemFontOfSize:24.0],
} betweenCharacters:@"#"];

[text r87_addAttributes:@{
	NSForegroundColorAttributeName: [UIColor redColor],
	NSFontAttributeName: [UIFont systemFontOfSize:35.0],
} betweenCharacters:@"*"];

self.textView.attributedText = text;
```

## Compatibility

iOS 4.3+

## License

R87AttributedString is available under the MIT license. See the LICENSE file for more info.
