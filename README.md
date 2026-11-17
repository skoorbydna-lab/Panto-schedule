# Puss in Boots – Rehearsal Planner

Rehearsal scheduler for the Peakland Players panto (Monday nights until opening on 29 January 2027).

- Plans every scene at least twice, grouping scenes so people get nights off
- Mark who's away each night and tap **Re-plan**
- **Send to WhatsApp** button for each night's call sheet

The schedule is saved in the director's browser. Use **Setup → Copy backup** now and then.

## Live mode (everyone sees updates, only the director edits)

1. In the [Firebase console](https://console.firebase.google.com), add a project (or use an existing one).
2. **Build → Authentication → Sign-in method:** turn on **Email/Password**. On the **Users** tab, add a user with the email `director@peaklandplayers.panto` and the director's password. (The email is made up; the director only ever types the password.)
3. **Build → Firestore Database:** create a database. On the **Rules** tab, paste in `firestore.rules` and publish.
4. **Project settings → Your apps:** add a web app and copy its `firebaseConfig`.
5. In `index.html`, paste that config into `FIREBASE_CONFIG`.

Until step 5 is done, the page works as before and saves only on the device it's used on.
