### Hi there <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30">

<a href="https://twitter.com/xcoding_jb"  target="_blank" >
  <img align="left" alt="JB's | Twitter" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/twitter.svg" />
</a>
<a href="https://www.linkedin.com/in/jayveeballesteros/" target="_blank" >
  <img align="left" alt="JB's LinkedIn" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/linkedin.svg" />
</a>
<a href="https://github.com/jayveeballesteros" target="_blank" >
  <img align="left" alt="JB's Counter" src="https://visitor-badge.glitch.me/badge?page_id=jayveeballesteros.jayveeballesteros" />
</a>

<br>
<br>

```swift

import Foundation

struct Profile: CustomStringConvertible {

    let name = "Jayvee Ballesteros"
  
    var description: String {
        """
        \(name)\n
        BS Information Technology graduate with passion for iOS development and design. 
        Majority of the time I practice with native iOS applications using Swift, UIKit,
        and trying to explore future possibilities for SwiftUI, always open to learning 
        new technologies and frameworks.\n

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
