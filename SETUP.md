# Setting up mauri.foto on GitHub Pages

This folder has everything the site needs: `index.html` (the whole page) and a `data` folder with `availability.json` and `requests.json` (these hold the calendar and booking requests, and get updated automatically when you hit Save in the admin panel).

## 1. Get the files into your repo

Go to https://github.com/gonzalezmauri/maurifoto (create the repo first if it doesn't exist yet, keep it public).

Upload all three files, keeping the folder structure: `index.html` at the root, and `data/availability.json` plus `data/requests.json` inside a `data` folder. The easiest way is dragging the whole `index.html` file and the `data` folder onto the "Add file" > "Upload files" page on github.com, then committing.

## 2. Turn on GitHub Pages

In the repo, go to Settings > Pages. Under "Build and deployment", set Source to "Deploy from a branch", pick your main branch and the `/ (root)` folder, then Save. Give it a minute or two, then the site will be live at:

https://gonzalezmauri.github.io/maurifoto/

## 3. Create a token so the Save button works

The admin panel's Save button writes straight to the two files in `data/` using a GitHub access token. You only need to make this once.

1. Go to https://github.com/settings/personal-access-tokens/new
2. Give it a name, something like "mauri foto site"
3. Set an expiration you're comfortable with (a year is fine, GitHub will remind you before it expires)
4. Under "Repository access," choose "Only select repositories" and pick `maurifoto`
5. Under "Permissions," open "Repository permissions" and set **Contents** to **Read and write**. Leave everything else alone.
6. Click "Generate token" and copy it right away, GitHub only shows it once

## 4. Paste the token into the site

Open the live site, scroll to the bottom, enter the passcode, and paste the token into the box under Availability. Hit Save once to confirm it works, the browser remembers it after that so you won't need to paste it again on that device.

## Changing the passcode

The passcode isn't stored anywhere fancy, it's just a line in `index.html`. To change it, open the file on github.com, click the pencil icon to edit, find the line that says `var ADMIN_PASSCODE = "mauri2026";`, change the text between the quotes, and commit. The live site picks it up within a minute or two.
