# Design and Implementation

## Frontend

The main design language of the application comes in the adoption of Google's massively popular Material Design 3 design specification, which is not only considered a standard in Android app UI design, but is also strongly adaptable to the iOS design language, as Google themselves has admitted [*in the past*](https://www.theverge.com/2021/10/12/22722130/google-ios-app-material-design-components-uikit). We are able to cross these beams thanks to our usage of the [*Flutter*](https://flutter.dev/) development framework and the Dart programming language.

A Figma board is used to keep the design uniform throughout development, and it would be advisable to work out a true visual identity of the app (color palette, main font pairings and design elements) in order to keep communication around the app (advertisement and presentation) consistent. 

## Backend

*Decompose the MVP into functional blocks.*

`/** I DONT KNOW */`

## Data Model

Our data model is split between a backend and a front end. We store most of the soft state on device, and it is only committed to the Supabase DB on form validation. Hard state is kept on the DB.

The Supabase database is organized in 5 **tables**, which contain all of the users and their relative settings, as relations on the User ID. They look like The **user** table mostly contains just enough data to discriminate users and greet them (display names, email), if they want to use a Google account, or nothing, if they login anonymously. Their User ID ties them to their chosen **news settings**, stored as lists of text options, **news providers**, containing their chosen sources, **alarms**, containing the information regarding their chosen alarm settings if any, and **news**, containing the generated transcripts for every user.

|      Table       |            Contents               |
|------------------|-----------------------------------|
|     `users`      | Contains information to discriminate users: UID, as well as display name and email if Google login | 
|  `news_settings` | Contains one list of preferences per UID (as text) |
| `news_providers` | Contains one list of providers per UID (as text) |
|     `alarms`     | Contains the list of alarm settings for every user that has set an alarm |
|      `news`      | Contains every generated transcript for every user UID |


## Security Considerations

_See previous question about security for a more in-depth answer._

## Infrastructure and Deployment

The backend is, in its POC/MVP state, deployed on Supabase directly, managed through its integrated dashboard. The compute nodes and storage are stored on the Supabase servers. 

Testing is done via manual testing of newly written components: we use the provided Flutter test suite, as well as the [`lcov`](https://github.com/linux-test-project/lcov) command line utility to ensure proper coverage. We define proper coverage as >80% line coverage, which is pretty standard in this kind of application. End-to-end testing is to be updated regularly as new user stories and interaction patterns emerge, to ensure no unintended behavior breaks our app, and proper usage results in the correct outcome. 

Using Flutter instead of other development environments, such as Kotlin or Java or others, comes with multiple benefits, but in this case the one that interests us the most is the possibility of using a single codebase for all platforms. This not only speeds up development, but it also makes testing much easier, since the same tests can be written for all platforms at once, drastically speeding up development and feature implementation.

Additionally, the Flutter developer environment is a lot more open than other Android development frameworks, allowing our developers to easily work in any environment, OS and editor they choose to, and to test their code even without launching heavy, resource-hungry emulators or needing an Android device. 

## Test Plan

As the project grows larger in scope, it could be interesting to have a dedicated test branch on the [*project's GitHub page*](https://github.com/ActualIA/app) to add an additional buffer preventing merges on main from applying unintended side effects, and to have a more structured release format. 
