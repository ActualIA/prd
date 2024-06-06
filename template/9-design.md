# Design and Implementation

## Frontend

*List the key libraries, languages, components used by the MVP.*

*If applicable, describe essential screens.*

The main design language of the application comes in the adoption of Google's massively popular Material Design 3 design specification, which is not only considered a standard in Android app UI design, but is also strongly adaptable to the iOS design language, as Google themselves has admitted [*in the past*](https://www.theverge.com/2021/10/12/22722130/google-ios-app-material-design-components-uikit). We are able to cross these beams thanks to our usage of the [*Flutter*](https://flutter.dev/) development framework and the Dart programming language.

A Figma board is used to keep the design uniform throughout development, and it would be advisable to work out a true visual identity of the app (color palette, main font pairings and design elements) in order to keep communication around the app (advertisement and presentation) consistent. 

## Backend

*Decompose the MVP into functional blocks.*

`/** I DONT KNOW */`

## Data Model

*What data are you collecting / managing?*

*How is it organised?*

*Where is it stored?*

*How is it shared/copied/cached?*

Our data model is split between a backend and a front end. We store most of the soft state on device, and it is only committed to the Supabase DB on form validation. Hard state is kept on the DB.

The Supabase database is organized in 5 **tables**, which contain all of the users and their relative settings, as relations on the User ID. They look like The **user** table mostly contains just enough data to discriminate users and greet them (display names, email), if they want to use a Google account, or nothing, if they login anonymously. Their User ID ties them to their chosen **news settings**, stored as lists of text options, **news providers**, containing their chosen sources, **alarms**, containing the informati

| Table   |            Contents               |
|---------|-----------------------------------|
| `users` | Contains information to discriminate users: UID, as well as display name and email if Google login | 
| `news_settings`  | Contains one list of preferences per UID (as text) |
| `news_providers` | Contains one list of providers per UID (as text) |
| `alarms` | Contains the list of alarm settings for every user that has set an alarm |
| `news` | Contains every generated transcript for every user UID |


## Security Considerations

_See previous question about security for a more in-depth answer._

## Infrastructure and Deployment

*How is the application developed, tested and deployed?*

*Any special infrastructure requirements.*

## Test Plan

*How is the application developed, tested and deployed?*

*Any special infrastructure requirements.*

