# [Nintendo Music Notifications](https://github.com/dootskyre/NintendoMusicNotifications/releases/latest)

<img width="348" height="110" alt="Screenshot 1879" src="https://github.com/user-attachments/assets/cbaeb301-d9e0-410b-8c46-40138feef8ac" />

This Shortcut checks for Nintendo Music notifications at a specified time, and if one is detected, gives you a notification or sends a message via webhook with all the information about the update.

Specifically, when run, the Shortcut will send a notification/webhook if tracks have been added in the past 10 minutes, otherwise it will give an information popup if the user is actively in the Shortcuts app.

The Shortcut supports all types of news from the Nintendo Music app. This includes new games, new playlists, and new home sections. When a playlist or game is added, a link to the playlist (or All Tracks in the case of games) and the image associated with it will be included in the notification/message.

## Installation & Setup
To install, click **[here](https://github.com/dootskyre/NintendoMusicNotifications/releases/latest)** to go to the releases page, then click the installation link or download the shortcut ZIP to install the shortcut.

The Shortcut should be run once prior to adding the Automation because it will ensure permissions are set up correctly, and will tell you what local time to set the Automation to. 

Typically, updates happen weekly on Mondays or Thursdays at 5:00PM PST, but sometimes they are moved to a later day in the week for cases such as Special Releases. As a result, it's usually best to set the shortcut to run **daily** at 5:00PM PST. If nothing updates, you won't recieve any notifications.

There are also a few settings you can configure within the Shortcut editor, listed below.

## Settings

### News Recency
When run, the Shortcut will check the release time of news compared to the current time to decide whether to send a notification. 
This defaults to 10 minutes, meaning if news was released in the past 10 minutes when the Shortcut is run, it will send a notification.

You can decrease the time to make checking stricter (eg. setting to 3 minutes and running this multiple times at 5:00 and 5:05 to ensure something isn’t missed) or increase the time to make checking more loose (eg. setting to 60 minutes and running it outside of automations).

### Playlist Update Image
By default, this Shortcut will use the game/playlist icon for notifications. You can configure this to show the highlights banner instead, which may have imagery more relevant to the update, but won't scale properly to notifications. If using the webhook, the highlights banner is preferred as it takes up the message width.

### Webhooks 
The Shortcut uses a Dictionary to store various Webhook URLs.
The `key` is the webhook URL you get from Discord. You can also put a label beforehand if you want, eg. `My Server https://…`.
The `value` can be any text you want added to the message sent from the shortcut. `<@&role-id>` can be used to ping a specific role. You can also leave it blank.

You can add multiple channel webhooks by adding items to the list. Each webhook will only use the additional text assigned to it.

If you set the webhook up and are running the Shortcut on multiple devices, it’s best to duplicate the Shortcut and edit it to create a version for your other devices that does *not* have the webhook settings.
Running the webhook on a Mac is ideal as it can use the webhook while the device is asleep. If you have to use a device other than a Mac, the shortcut can still send messages over the webhook, but only while the device is unlocked.

Here's an example of how a webhook message may look:

<img width="412" height="363" alt="Screenshot 1878" src="https://github.com/user-attachments/assets/6ed71c39-08a3-447e-865b-c85b8f39cb6f" />
