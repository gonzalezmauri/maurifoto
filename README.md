mauri.foto

The website for Mauricio Gonzalez's photography business, styled after an Instagram profile. Live at:

https://gonzalezmauri.github.io/maurifoto/

Everything the site needs lives in this repo: index.html (the whole site, one file) and a data folder holding availability.json, requests.json, and gallery.json, which the admin panel updates automatically when you hit Save.

First-time setup (creating the repo, turning on GitHub Pages, generating the access token the admin panel needs) is covered in SETUP.md. This file covers the two things you'll come back to most often once the site is up and running.

Opening the admin panel

Scroll to the very bottom of the site, past the booking section. Enter the passcode and hit Unlock. That reveals Requests, Availability, and Photos, along with the Save changes button at the bottom.

Changing the admin passcode

The passcode is just a line inside index.html, there's no separate settings screen for it.

Go to your repo on github.com and open index.html.
Click the pencil icon to edit it.
Use your browser's find (Ctrl+F or Cmd+F) and search for ADMIN_PASSCODE.
You'll land on a line that looks like:
js
   var ADMIN_PASSCODE = "yourpasscode";
Change the text between the quotes to your new passcode, then commit the change.

The live site picks it up within a minute or two. Note the line number shifts every time the file is updated, so search for ADMIN_PASSCODE rather than relying on a specific line number.

Adding photos to a portfolio gallery

Each of the 6 portfolio tiles (Family, Engagement, Street, Maternity, Editorial, Graduation) opens its own photo gallery when a visitor taps it. Here's how to add photos to one:

Open the admin panel (see above).
Scroll down to the Photos section.
If you haven't already, paste your GitHub token into the box just below Availability, this is what lets the site save photos back to the repo. You only need to do this once per browser/device (see SETUP.md for how to create a token).
In the Photos section, pick the category you want from the dropdown (Family, Engagement, Street, Maternity, Editorial, or Graduation).
Click the file picker and choose one or more photos from your device. You can select several at once.
Click Upload. Each photo is resized automatically and saved straight to the repo, no need to hit Save changes afterward for uploads, they're live within a minute or two.
The photos you've uploaded for each category show up in a small thumbnail list right below the upload button, so you can see what's already there.

To remove a photo, click the small remove button on its thumbnail in that list, then click Save changes at the bottom of the admin panel to make the removal stick (removals, unlike uploads, need that extra Save step).

Visitors will see these photos when they tap that category's tile on the Portfolio tab, cycling through with the arrows if there's more than one.
