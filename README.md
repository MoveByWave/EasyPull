# EasyPull
Let pull-to-refresh Easy for any UIScrollView

You have the flexibility to set custom view with fantastic animation.(可以灵活的设置自定义效果，实现期望的动画)


## Usage

(see sample Xcode project in `/Demo`)

### Adding Drop Pull to Refresh

Only support Manual Mode(仅支持手动模式)

```Swift
 tableView.easy_addDropPull({
     // prepend data to dataSource, insert cells at top of table view
     // call tableView.easy_stopDropPull() when done
 })
```

### Adding Up Pull to Refresh and Load more

Manual Mode(手动模式)

```Swift
 tableView.easy_addUpPullManual({
     // prepend data to dataSource, insert cells at bottom of table view
     // call tableView.easy_stopUpPull() when done
 })
```

Automatic Mode(自动模式)

```Swift
 tableView.easy_addUpPullAutomatic({
     // prepend data to dataSource, insert cells at bottom of table view
     // call tableView.easy_stopUpPull() when done
 })
```

### Customization

The pull-to-refresh view can be customized using the following methods:

```Swift
 func easy_addDropPull(action: (() ->Void), customDropView: EasyViewManual? = nil)
 func easy_addUpPullManual(action: (() ->Void), customUpView: EasyViewManual? = nil)
 func easy_addUpPullAutomatic(action: (() ->Void), customUpView: EasyViewAutomatic? = nil)
```

Your custom views must implement the `EasyViewManual` protocol when you prefer the Manual mode 
Or implement the `EasyViewAutomatic` protocol when you prefer the Automatic mode.
(如果需要手动模式，你的自定义view必须实现EasyViewManual协议。如果需要自动模式，你的自定义view则必须实现EasyViewAutomatic协议。)

(see sample Xcode project in `/Demo/MyCusyomView.swift` or `/Demo/EasyPull/DefaultView.swift`)

## Installation

### From CocoaPods

### Source files


## License

This code is distributed under the terms and conditions of the [MIT license](LICENSE).