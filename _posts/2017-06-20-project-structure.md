---
published: false
date: 2017-06-20T00:00:00.000Z
---
## A Little Planning

The new project will look like this:

## Models

Users can:

- Create an account.
- Log in to an account.
- Log out.
- Update profile fields: location

First name: string
Last name: string
Email Address: string

Logged-in users can:

- Create a mailbox using the oAuth redirect flow.
- Delete a mailbox.
- View all mailboxes belonging to that user.

User ID: foreign key
Name: string
Email Address: string
Provider: string
Hostname: string
Refresh Token: string
Last Checked: datetime
Default: boolean

Logged-in users with mailboxes can:

- Create a new email. This may be either stored as a local copy or, perhaps better, created as a draft in the user's mailbox using the mail APIs.
- Edit an existing email. 
- Delete an email.
- View all emails belonging to the user.

Mailbox ID: foreign key
Message ID: string (Google or Microsoft message ID)
Send At: datetime (UTC)
Status: string, default "draft"
Meta: json (includes subject, reply-to, to, snippet of body - enough to provide a summary for the index page)

## System notifications

Users will receive an email from the system when:

- They request a "forgot password" reset.
- To confirm account creation.
- To confirm an email received from outside the app.
- To alert them to errors with the email received from outside the app.
- Optionally, to alert them that an email has been sent.

## oAuth

- Users will use oAuth to request API permissions from Gmail and Microsoft APIs. 
- oAuth can also be used to register or sign in, and increased permissions requested when a mailbox is added.

## Scheduled jobs

- The system will check periodically for emails that are due to be sent using the user's mailbox.

## User emails

- The system will use the Gmail and Outlook APIs to create drafts with labels, and send them.