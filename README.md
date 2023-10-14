```swift

import Foundation

struct Profile: CustomStringConvertible {

    let name = "Jayvee Ballesteros"
  
    var description: String {
        """
        \(name)
        I’m a Software Engineer that specializes in native iOS development using Swift
        with UIKit &/or SwiftUI. Building side-projects and helping aspiring developers
        is how I further my self-education outside of working hours.

        """
    }
  
    enum Skill: String, CaseIterable {
        case swift, swiftUI, uIKit, PHP, JavaScript, HTML5, CSS3
        case xCode, webStorm, sketch, photoshop, finalCutPro
    }
 
    func proficient(in skills: [Skill] = Skill.allCases) -> String {
        skills
            .lazy
            .map(\.rawValue)
            .map(\.capitalized)
            .map { "- " + $0 + "\n" }
            .reduce("Skills: \n", +)
    }
}

// Paste into a playground!
let profile = Profile()
print(profile.description)
print(profile.proficient())

```
<!-- # <img class="logo" src="Images/Icon.png" width="32"> StoiQuote

StoiQuote is a simple app that displays random quotes about Stoicism.

> SwiftUI, API Request

<img src="Images/screen2.gif" width="320">

<a href="https://github.com/jayveeballesteros/StoiQuote"><img src="Images/github.svg"></a>

<br>
 -->
