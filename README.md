# UXPasscodeField

[![CI Status](http://img.shields.io/travis/Eddie Lau/UXPasscodeField.svg?style=flat)](https://travis-ci.org/Eddie Lau/UXPasscodeField)
[![Version](https://img.shields.io/cocoapods/v/UXPasscodeField.svg?style=flat)](http://cocoapods.org/pods/UXPasscodeField)
[![License](https://img.shields.io/cocoapods/l/UXPasscodeField.svg?style=flat)](http://cocoapods.org/pods/UXPasscodeField)
[![Platform](https://img.shields.io/cocoapods/p/UXPasscodeField.svg?style=flat)](http://cocoapods.org/pods/UXPasscodeField)

## Screenshot

![Screenshot](./Screenshot.gif)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

```swift
import UIKit
import UXPasscodeField

class ViewController: UIViewController {

    @IBOutlet weak var passcodeField: UXPasscodeField!

    override func viewDidLoad() {
        super.viewDidLoad()

        passcodeField.becomeFirstResponder()

        // Optional, default is 6
        passcodeField.numberOfDigits = 6

        // Optional, default is false
        passcodeField.isSecureTextEntry = false

        passcodeField.addTarget(
          self,
          action: #selector(ViewController.passcodeFieldDidChangeValue),
          for: .valueChanged)

    }

    @IBAction func passcodeFieldDidChangeValue() {
        print(passcodeField.passcode)
    }

}
```

## Requirements

## Installation

UXPasscodeField is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "UXPasscodeField"
```

## Author

Eddie Lau, eddie@touchutility.com

## License

UXPasscodeField is available under the MIT license. See the LICENSE file for more info.
