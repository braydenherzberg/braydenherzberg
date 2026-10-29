# Cheers

**Released iOS app · Source code private**

[View on the App Store](https://apps.apple.com/us/app/cheers-lockscreen-widgets/id6759501004)

Cheers lets friends share short messages through lock-screen and home-screen widgets. Users exchange friend codes, write a message of up to 50 characters, and see incoming cheers in the app and widget experience.

## My contribution

I built the SwiftUI application, WidgetKit experience, and Firebase-backed friend and message workflows. The public App Store listing names me as the developer and Tributary Studios LLC as the seller.

## Workflow

![Two actual Cheers app views with fictional data: incoming messages from friends and a message composer with recipient widget preview.](../assets/cheers/workflow.png)

1. **Choose a friend.** Review incoming messages and select a recipient.
2. **Compose a cheer.** Write a short message and review the in-app widget preview.

Individual views: [friends](../assets/cheers/01-friends.png) · [composer](../assets/cheers/02-compose.png).

These are existing authentic v1.1 simulator captures using the app’s fictional screenshot fixtures, rather than fresh captures from this review. The composer contains the app's own widget preview; it is not evidence of a message delivered to a second device.

## Engineering decision

The app and widget share a local App Group cache, while Firebase stores friend relationships and messages. This separates widget rendering from the main app's interface and supports cached timeline content. It also creates a consistency problem: updates and privacy preferences must be mirrored between the app, cache, and widget. The implementation includes cache refreshes and push-update handling; a screenshot alone cannot verify end-to-end delivery.

**Technology:** Swift, SwiftUI, WidgetKit, App Groups, Firebase Authentication, Cloud Firestore, Firebase Cloud Functions, and APNs widget-update handling.

## Status and evidence

Cheers has a public App Store listing, including a **v1.1.1** version-history entry. The portfolio captures illustrate the native workflow; device-to-device message delivery is outside this capture session's verification.

Source code remains private.

[Back to profile](../README.md)
