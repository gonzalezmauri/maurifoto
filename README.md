
























Readme · MD
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
If the token box just below Availability is empty, paste your GitHub token in there (I emailed it to you, subject "Github Token", this is what lets the site save photos back to the repo (see SETUP.md for how to create one). You only have to do this once per browser. Once it's in, that browser remembers it for every future visit, you won't need to paste it again unless you clear your browser's data, switch to a different browser or device, or the token expires. If you ever do need a new one, the "Forget saved token" button clears the old one out first.
In the Photos section, pick the category you want from the dropdown (Family, Engagement, Street, Maternity, Editorial, or Graduation).
Click the file picker and choose one or more photos from your device. You can select several at once.
Click Upload.
That's it, uploads save automatically. No need to hit Save changes afterward, the moment you click Upload, the photos are on their way to the repo. Give it a few minutes and they'll be live on the site. The photos you've uploaded for each category also show up in a small thumbnail list right below the upload button, so you can see what's already there.

To remove a photo, click the small remove button on its thumbnail in that list, then click Save changes at the bottom of the admin panel to make the removal stick (removals, unlike uploads, need that extra Save step).

Visitors will see these photos when they tap that category's tile on the Portfolio tab, cycling through with the arrows if there's more than one.

Editing the text on any screen
Nearly everything you see on the site, headlines, button labels, the bio, descriptions, form placeholders, is plain text sitting right inside index.html. You don't need the admin panel or a token for this, it's the same process as changing the passcode: open index.html on github.com, click the pencil icon to edit, use your browser's find (Ctrl+F or Cmd+F) to search for the exact wording you see on the live site, edit the text, and commit. The live site updates within a minute or two.

Two things to watch for: only change the words themselves, not the <...> tags around them, changing those can break the page's layout. And the pricing menu on the Packages tab is a photo, not text, so it can't be edited this way, that one needs a new image (ask me if you want help swapping it in).

Here's where to find the wording for each part of the site:

Header, top of the page The username ("mauri.foto"), the three bio lines below the stats ("Just a witness in ATX with a camera," "Based in Austin, TX," and so on), and the "Text me," "E-mail me," and "Instagram" labels.

Payment row The Zelle, Venmo, and Cashapp labels, and the phone number, handle, or username shown underneath each one.

Portfolio tab The caption on each of the 6 tiles (Family, Engagement, Street, Maternity, Editorial, Graduation), and the note underneath the grid, "Tap a category to see more from that kind of session."

Packages tab The "Packages" heading, the paragraph describing how sessions work, and the "View pricing" button.

Book tab The "Request a Session" heading, the intro paragraph, the "No open sessions this month" message, the form's field labels and placeholder text, and the "Send request" button.

Admin panel All the labels and hint text down here (under Requests, Availability, and Photos) follow the same rule, though you're the only one who ever sees these.

Since most of this wording is a short, unique phrase, searching for the exact words as they appear on the live site (like "Just a witness in ATX" or "View pricing") is the fastest way to land right on the line you need.



