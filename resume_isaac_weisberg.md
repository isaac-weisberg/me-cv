# Isaac Weisberg
London, United Kingdom  
net.caroline.weisberg@gmail.com  
## Summary

A systems programmer is looking for a product that is nowhere near its decline. Eagerness of a 4 year old. Interest in a wide range of development stacks.

## Employment History

### **Disrapp, Saint Petersburg, Russian Federation**
*iOS Developer April 2019 - Present*

Native iOS/UIKit development in a one year old "rich client" project.  

Clean architecture with coordinator-tree-based navigation and RxSwift based MVVM.

Heavy isolated chunks of functionality  
Incredible emphasis on the UX  
Regular feature based code-review  
Schedule independent refactoring  
gRPC based server interoperation  
CoreData based waste of time and patience  
Establishing architectural conventions in coop  
A/B experiments and analytics grind  
Developer intreviews

Pushed 4 sizable chunks of functionality into production, outputting high-quality low-maintainance-cost code.

### **Magora Systems, Novosibirsk, Russian Federation**  
*iOS Developer October 2018 - April 2019*

Native iOS with Swift in an outsourcing company.

Clean architecture with coordinator-tree-based navigation and RxSwift based MVVM (*note how I copy-pasted it from the section above*).  

Participated in a 2k+ hours project.  
Periodical teammate code reviews.  
Interviewed 15+ candidates for upper and lower tier iOS developers positions.  
Pre-sale and limited scope estimation.  
Presented a modernization and unification of project-wise error handling and propagation.  
Participated in productivity optimization of networking API design standards.  
Introduced the team to RxDataSources and RxKeyboard, which lead to a general codebase improval.

### **RDSTeam, Novosibirsk, Russian Federation**
*iOS Developer April 2017 - October 2018*

Native iOS with Swift, RxSwift and GRDB. Strong maintainability accent. Custom-written app content versioning and caching systems. SceneKit, SpriteKit, ARKit. Promises, RxDataSources, RxKeyboard. SwiftyStoreKit, SwiftSoup, PocketSVG. CoreData, APNS. Design and implementation of REST API's client side. Inevitably Alamofire.

6+ apps on App Store. Integrated a lot of development solutions that simplified and enhanced the development process.

## Professional Skills

- Software development.  
Preferred domain: system programming.  
Primary commercial experience: native iOS.  
- Wide interest in multiple other native and managed development stacks.
- Application and presentation layer architecture, Clean.
- Languages and runtimes, low-level implementation.
- Common CS.

## Programming practices accross carreer

Web frontend development:
- Typescript, Babel, Webpack bundling
- React.js/Redux, a couple of training projects
- Vue.js/vuex/vue-router, a couple of training projects
- RxJS 7.x
- Electron.js, a single training project

Backend development:
- Node.js, Express.js, Koa.js, several practice projects
- Mongo.db, PostreSQL, Facebook Graph API
- Go, Gin-Gonic eco-system, a practice project

Native frontend development:
- Windows Presentation Foundation, commercial practice
- Unity Engine, commercial practice
- Androind Platform, understanding of concepts, no notable practice

Other:
- Kotlin, knowing the language by docs, no notable practice
- C, practice projects: implementation of OOP, closures, macro-based generic type system, usage of aio and standard library

## Interesting commercial problem solving cases

*Disrapp, Summer-Fall 2019*: the architecture of a couple of view controllers was tightly coupled, MVVM broken multiple times, in other words legacy code. Also there was a case of literally lazy business modeling. There would be a view model with a lot of fields and a few initializers. Only one of the initializers would be accepting a legitimate data storage object, while the other initializers would ignore the fields they could ignore and initialize the others with default values. It would store a type, determined by an initializer used. If a view found that the view model was built using a real database object, it would initialize itself accordingly, it used the fields and reactive getters and subjects to bind the event propagation. Alternatively, if, for instance, you used another initializer, the view would ignore some Rx events, it bound its own events only to particular subjects, its visualization depended on the the viewmodel's state. 

Obviously, it's the abundance of segregation, and state leakage. A lot of the bugs were supported by this approach. So, as we started to implement a new type of this view model what I did is I replaced all of the usages with an intermediate model, an enumerator with associated values that brought a legacy view model in one case and a completely new, light view model specifically for this new case. The view that ate the new view model was also new. Paid off in a long run, implemented a couple more cases and corresponding views, refactored a lot of code and event propagation on 3 screens, eliminated a few of out of place navigation. Great stuff, I enjoy working at this company because of this habit of packing refactoring into the tasks while we can, stealth mode. Really improves the maintainability costs.

*Magora Systems, Winter 2019*: the client application boasted zero native funcionality yet was sold as 2 separate native clients anyway. One of the requirements was to have a video player with customized playback widgets. The catch was that it was necessary that all the content was hosted at Youtube. I've been in charge of building a web view coated with native widgets, scrollable playback progress bar, timestamps, navigation. Interopped with Javascript that exposed the Youtube player API, have writter Reactive wrappers for events coming in a out of the web view's Javascript context.

Nothing could save the player though: the UX was terrible, Youtube embedded player would totally break on screen rotation, the players own widgets rendered in web view just wouldn't go away without reliance on DOM's structure and manual removal, also Youtube strictly prohibits custom overlays and widgets threatening with a ban. Fun times. Client was flattered.

## Hobbies & Interests

Bikeriding was one of my biggest passions until I discovered electric scooters. Also I am totally into autosport, currently studying at a driving school and hoping one day I won't procrastinate just enough to enter a karting league as an amateur driver.

## Notable activity

GitHub open source projects  
Medium articles in FRP and architecture  
Functional and reactive state systems research  
Public speech and technical writing  
Education strategies and human resource crisis  

## Links

More links at my personal website http://caroline-weisberg.net/
