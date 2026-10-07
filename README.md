# AUSC Trials 2027 app

An installable phone app for trial coaches. The player data stays in the club's Google Sheet;
these files are only the app screens, and they talk to the Sheet through the Apps Script.

## Set up (once)

1. **Update the Apps Script.** In the Google Sheet: Extensions > Apps Script. Replace Code.gs
   with the new version, save, then Deploy > Manage deployments > pencil icon >
   Version: New version > Deploy. Copy the Web app URL (it ends in `/exec`).
2. **Edit `config.js`.** Paste that URL between the quotes.
3. **Put the files on GitHub Pages.**
   - On github.com, create a new **public** repository, e.g. `ausc-trials`.
   - Add file > Upload files, drag in every file from this folder (not the folder itself), Commit.
   - Settings > Pages > Source: Deploy from a branch > Branch: `main`, folder `/ (root)` > Save.
   - After a minute or two the app is at `https://<your-username>.github.io/ausc-trials/`.
4. **Install it on a phone.** Open that link, enter the passcode and your name, then
   - iPhone (Safari): Share > Add to Home Screen
   - Android (Chrome): tap Install in the blue bar, or menu > Install app

## Good to know

- No player details are in these files. Anyone can see the code and the web app URL, but the
  data only comes back with the passcode (Apps Script > Project Settings > Script Properties > PASSCODE).
- To change the passcode, edit that property. No redeploy needed; coaches re-enter it next time.
- To update the app, edit or re-upload files in the repository. Phones pick up the new version
  the next time the app is opened with signal.
- If you change Code.gs, redeploy as a **new version of the same deployment** so the URL in
  `config.js` keeps working.
