# [Nintendo Music Updates](https://github.com/dootskyre/NintendoMusicNotifications/releases/latest)

This Shortcut checks for Nintendo Music notifications at a specified time, and if one is detected, gives you a notification or sends a message via webhook with all the information about the update.

Specifically, when run, the Shortcut will send a notification/webhook if tracks have been added in the past 10 minutes, otherwise it will give an information popup if the user is actively in the Shortcuts app.

The Shortcut supports all types of news from the Nintendo Music app. This includes new games, new playlists, and new home sections. When a playlist or game is added, a link to the playlist (or All Tracks in the case of games) and the image associated with it will be included in the notification/message.

## Automation details
Typically, updates happen weekly on Mondays at 5:00PM PST, but sometimes they are moved to a later day in the week for cases such as Special Releases. As a result, it's usually best to set the shortcut to **run daily at 5:00PM PST**, because if nothing happens, you won't recieve any sort of notification.

## Settings
There are a couple settings you can change within the Shortcut editor:

### Playlist Update Image
By default, this Shortcut will use the game/playlist icon for notifications. You can configure this to show the highlights banner instead, which may have imagery more relevant to the update, but won't scale properly to notifications. If using the webhook, the highlights banner is probably preferred as it takes up the message width.

### Webhooks 
This uses a Dictionary to store various Webhook URLs.
The “key” is the webhook URL you get from Discord. You can also put a label beforehand if you want, eg. “My Server https://…”
The “value” is any text you want added to the message sent from the shortcut. <@&role-id> can be used to ping a specific role. You can leave it blank if you want. 
You can add multiple channel webhooks by adding items to the list. Each webhook will only use the additional text assigned to it.

If you set the webhook up and are running the Shortcut on multiple devices, it’s best to duplicate the Shortcut and edit it to create a version for your other devices that does *not* have these webhook settings.
Running this on a Mac is ideal as it can use the webhook while the device is asleep. If you have to use a device other than a Mac, the shortcut can still send messages over the webhook, but only while the device is unlocked.
