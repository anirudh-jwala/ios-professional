# Code Snippets

## Active constraints array

```swift
NSLayoutConstraint.activate([
        
])
```

## New View

```swift
import Foundation
import UIKit

class NewView: UIView {
    
    override init(frame: CGRect) {
        super.init(frame: frame)
        
        style()
        layout()
    }
    
    required init?(coder: NSCoder) {
        fatalError("init(coder:) has not been implemented")
    }
    
    override var intrinsicContentSize: CGSize {
        return CGSize(width: 200, height: 200)
    }
}

extension NewView {
    
    func style() {
        translatesAutoresizingMaskIntoConstraints = false
    }
    
    func layout() {
        
    }
}
```

## No Storyboards

```swift
var window: UIWindow?
    
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]?) -> Bool {
        
        window = UIWindow(frame: UIScreen.main.bounds)
        window?.makeKeyAndVisible()
        window?.backgroundColor = .systemBackground
        window?.rootViewController = ViewController()
        
        return true
    }
```


## Unit Tests

```swift
import XCTest

@testable import Bankey

class Test: XCTestCase {
    var vc: ViewController!
    
    override func setUp() {
        super.setUp()
        vc = ViewController()
        vc.loadViewIfNeeded()
    }
    
    func testShouldBeVisible() throw {
        let isViewLoaded = vs.isViewLoaded
        XCTAssert(isViewLoaded)
    }
}
```
