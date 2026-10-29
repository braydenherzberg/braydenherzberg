# Cheers

**Available on the App Store · Source code private**

[App Store](https://apps.apple.com/us/app/cheers-lockscreen-widgets/id6759501004)

iOS application for sending messages of up to 50 characters to friends' lock-screen and home-screen widgets. Users connect through friend codes.

## Contributions

- Developed the SwiftUI application and WidgetKit extension.
- Built Firebase-backed friend relationships and message storage.
- Implemented shared widget caching, preference synchronization, and push-update handling.

## Screenshots

![Cheers screens showing sample incoming messages and a message composer with an in-app widget preview.](../assets/cheers/workflow.png)

1. **Friends:** Review messages and select a recipient.
2. **Composer:** Write a message and review the widget preview.

Full-size screenshots: [friends](../assets/cheers/01-friends.png) · [composer](../assets/cheers/02-compose.png).

Screenshots are from the v1.1 simulator capture set and use fictional contacts and messages. The composer shows an in-app widget preview.

## Design decision

An App Group cache shares message content and preferences between the app and widget. Firebase stores friend relationships and messages. Cached content supports widget timelines, but requires synchronization when messages or privacy preferences change. Device-to-device delivery was not tested during this portfolio review.

**Technologies:** Swift, SwiftUI, WidgetKit, App Groups, Firebase Authentication, Cloud Firestore, Firebase Cloud Functions, APNs.

## Status

Version v1.1.1 is listed on the [App Store](https://apps.apple.com/us/app/cheers-lockscreen-widgets/id6759501004). The listing identifies Brayden Herzberg as the developer and Tributary Studios LLC as the seller. Source code is private.

[Back to profile](../README.md)
