AGAPE MEDIA STUDIO — COMPLETE STATIC BUILD

MAIN FILE
- index.html contains the complete HTML, CSS, JavaScript, and your Firebase web configuration.

SEPARATE SUPPORT FILES
- manifest.webmanifest
- service-worker.js
- assets/icon.svg
- firestore.rules

FIREBASE
1. Authentication > Sign-in method: Email/Password enabled.
2. Firestore Database: Production mode.
3. Open Firestore Database > Rules, paste firestore.rules and Publish.
4. Create the first administrator in Authentication > Users.
5. Copy that user's UID.
6. In Firestore > Data, create collection users and a document whose ID is exactly that UID.
7. Add fields:
   uid: same UID (string)
   email: exact Auth email in lowercase (string)
   displayName: administrator's name (string)
   role: superAdmin (string)
   department: Media Director (string)
   status: active (string)
   createdAt: current timestamp (timestamp)
8. Deploy the package to GitHub Pages.
9. Add your GitHub Pages hostname under Authentication > Settings > Authorized domains.

GITHUB PAGES
Upload all files/folders to the repository root. In repository Settings > Pages, select Deploy from a branch, main, and /(root).

IMPORTANT LIMITS
- Only HTML, CSS, vanilla JavaScript, Firebase Authentication and Cloud Firestore are used.
- No Firebase Storage, Cloud Functions, Cloud Run, external backend or paid APIs.
- Video/image/audio files stay on each user's device. Firestore stores metadata only.
- Video Studio is local preview/project organization, not a professional multi-track renderer.
- Browser camera preview/local recording is not a public livestream. Use OBS separately for broadcasting.
- Publishing records are manual; no social platform APIs.
- Invitation redemption is client-side because there is no trusted backend. It has weaker guarantees than server-verified invitation redemption. Issue invitations only to known people and review team accounts.
- Never add Firebase service-account private keys or passwords to the website files.
