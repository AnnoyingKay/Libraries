LIBRARIES v4

One page that holds Shelf, Musicbox and SavePoint. The libraries go round in a circle: after Games comes Books again, and Books back to Games. Swipe left or right on a phone or tablet, use the left and right arrow keys on a computer, or tap the Books, Vinyl, Games and Home tabs along the bottom. On a computer there are also arrow buttons at the sides.

Nothing needs to change in the Shelf, Musicbox or SavePoint repositories.

Files for a NEW repository (root): index.html, sw.js, manifest.webmanifest, icon-192.png, icon-512.png, firestore.rules

1. GitHub: create a new public repository called Libraries (same account as the others).
2. Add file > Upload files, drop the six files above, commit.
3. Settings > Pages > Deploy from a branch > main, folder / (root), Save.
4. Open https://annoyingkay.github.io/Libraries/ and reload twice.
5. Add it to the home screen on the phone and tablet.

Sign in once. All three apps use the same Firebase project, so one sign in covers them. If a sign in window is blocked inside Libraries, open that app on its own address once, sign in there, then come back.

Links straight to one page: #books, #vinyl, #games, #home after the address. The page also remembers the last library you used.

If a repository is ever renamed, change the LIBS list at the top of the script in index.html.

Home page (new in v4)

The fourth page shows one card per library with item counts. Books: physical books and ebooks (audiobooks on a small extra line). Vinyl: records in the collection (wishlist not counted). Games: physical and digital.
Books come from the data already on the device. Vinyl and Games are counted from Firebase when you are signed in, then kept for offline use. Tap Refresh to update, or tap a card to open that library.
Games physical and digital show a dash until SavePoint stores a field called format on each game, with the exact lowercase values physical or digital. The total still shows.
No change to the Firestore rules is needed.

Optional: Shelf's sw.js deletes the offline copies kept by other apps on the same address, including this one. Offline use of Libraries is the only thing affected. See optional/Shelf-sw.js in the Musicbox files for the fix.

Firestore rules

firestore.rules is the one master set of rules for Shelf, Musicbox and SavePoint, because they share one Firebase project. Keep it here and nowhere else. The three app repositories must not carry their own copy.
To change the rules: edit firestore.rules here, then Firebase console > Firestore Database > Rules, paste the whole file, Publish. Use the Rules Playground to test first.
The two accounts allowed into Musicbox and SavePoint are listed once, in the pairUser function.
