LIBRARIES v2

One page that holds Shelf, Musicbox and SavePoint. The libraries go round in a circle: after Games comes Books again, and Books back to Games. Swipe left or right on a phone or tablet, use the left and right arrow keys on a computer, or tap the Books, Vinyl and Games tabs along the bottom. On a computer there are also arrow buttons at the sides.

Nothing needs to change in the Shelf, Musicbox or SavePoint repositories.

Files for a NEW repository (root): index.html, sw.js, manifest.webmanifest, icon-192.png, icon-512.png

1. GitHub: create a new public repository called Libraries (same account as the others).
2. Add file > Upload files, drop the five files above, commit.
3. Settings > Pages > Deploy from a branch > main, folder / (root), Save.
4. Open https://annoyingkay.github.io/Libraries/ and reload twice.
5. Add it to the home screen on the phone and tablet.

Sign in once. All three apps use the same Firebase project, so one sign in covers them. If a sign in window is blocked inside Libraries, open that app on its own address once, sign in there, then come back.

Links straight to one library: #books, #vinyl, #games after the address. The page also remembers the last library you used.

If a repository is ever renamed, change the LIBS list at the top of the script in index.html.

Optional: Shelf's sw.js deletes the offline copies kept by other apps on the same address, including this one. Offline use of Libraries is the only thing affected. See optional/Shelf-sw.js in the Musicbox files for the fix.
