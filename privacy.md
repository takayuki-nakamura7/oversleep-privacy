---
title: Privacy Policy
permalink: /privacy/
---

# Oversleep Privacy Policy

*Last updated: 20 September 2026*

Oversleep is a calendar-aware alarm app for iPhone. This policy describes what
the app accesses, what it stores, and what it never does.

The short version: **Oversleep has no backend.** There is no Oversleep account,
no server that receives your data, no analytics SDK, and no advertising SDK.
Your calendar events are processed on your device.

## Calendar access

Oversleep reads calendar data in order to calculate a safe wake time before your
events. It reads **only the calendars you explicitly select**, and access is
**read-only** — Oversleep never creates, edits, or deletes calendar data.

**Apple Calendar.** The app requests full calendar event access because it needs
each event's title, start time, status, and participation to apply your rules and
calculate a wake time. No Oversleep account is involved.

**Google Calendar (optional).** You may connect a Google account directly. If you
do, Oversleep requests these scopes:

| Scope | Why |
|---|---|
| `openid`, `email` | To show which account is connected, in Settings |
| `calendar.calendarlist.readonly` | To list your calendars so you can choose which to use |
| `calendar.events.readonly` | To read events on the calendars you chose |

Requests go from the app directly to Google. No Oversleep server is involved at
any point.

## Limited use

Oversleep's use of information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements. Specifically, Google Calendar data is
used only to provide and improve the alarm features described here. It is never
transferred to anyone else, never used for advertising, and never used to train
generalized models. No human reads it.

## What is stored, and where

Everything Oversleep stores is stored **on your device**.

- **Google sign-in.** Sign-in uses the system authentication session with
  Authorization Code + PKCE. Oversleep never sees your Google password and
  contains no OAuth client secret. The refresh token, account identifier, and
  account email are held in the iPhone Keychain as this-device-only data.
- **Calendar events.** Access tokens, provider responses, event payloads, and raw
  Google calendar identifiers are not persisted.
- **Your account email** is displayed only in Settings → Calendar Sources.
- **Recent activity** about alarm scheduling is kept for 7 days, then removed
  automatically.

## What other parts of iOS receive

- **AlarmKit** receives the schedule metadata it needs to ring. Raw event titles
  are not copied into it.
- **Notifications** include an event title only when *Hide Event Titles* is off.
- **The Home Screen widget** shows tomorrow's alarm, and the event behind it when
  one applies. With *Hide Event Titles* on, titles do not appear there either.

## Your control

- Disconnecting Google Calendar deletes its stored credential from the Keychain.
- Removing a calendar source stops Oversleep reading it. Nothing in your calendar
  account is changed or deleted.
- Calendar and notification permissions can be revoked at any time in iOS
  Settings.
- You can revoke Oversleep's access to your Google account at
  [myaccount.google.com/permissions](https://myaccount.google.com/permissions).
- Deleting the app removes its stored data. Keychain removal on uninstall is
  controlled by iOS.

## Children

Oversleep is not directed at children and does not knowingly collect information
from them.

## Changes

If this policy changes, the date at the top of this page changes with it.

## Contact

[ktkr3335@yahoo.co.jp](mailto:ktkr3335@yahoo.co.jp)
