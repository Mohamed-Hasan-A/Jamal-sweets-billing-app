SNACKS SHOP BILLING APP - UPGRADED (Tamil + English)

Files:
- index.html: Billing app, language toggle, receipt print/share, optional Firebase sync
- manifest.json: installable PWA settings
- sw.js: offline cache
- firestore.rules: Firebase Firestore rules for the shop sync path

EXISTING FEATURES KEPT
- Billing, products add/edit/delete, bill history/search/date filter
- Shop details, CSV export, JSON backup/restore, print receipt
- Offline-first localStorage and installable PWA

NEW FEATURES
- Header-la Tamil / English toggle; language choice saved on device
- WhatsApp Share button: saves bill first, then shares bill text through WhatsApp
- Optional Firebase Firestore sync setup for two devices

A. GITHUB PAGES UPDATE (existing repository)
1. First current app data-ku Shop & Backup > Download Backup click panni JSON backup edunga.
2. ZIP extract pannunga.
3. Existing GitHub repository 'snacks-billing-app' open pannunga.
4. index.html, manifest.json, sw.js files-ai repository root-la replace/upload pannunga. firestore.rules and README_Tanglish.txt reference-ku vechukkonga; GitHub Pages root-la upload panninaalum app break aagathu.
5. GitHub Settings > Pages > Deploy from a branch > main > /(root) > Save.
6. Website refresh pannunga. Old cache irundha browser-la site data/cache clear pannitu reopen pannunga; backup eduthathukku apram mattum.
7. Android Chrome: site open > menu (⋮) > Install app / Add to Home screen. Computer Chrome/Edge-la same URL open pannunga.

B. TAMIL / ENGLISH
- Top-right-la 'தமிழ்' button press pannunga.
- English-ku thirumba 'English' press pannunga.
- Language choice device-la save aagum. Product names neenga type pannura maadhiriye irukkum.

C. FREE FIREBASE AUTOMATIC SYNC SETUP (one-time, internet required)
1. https://console.firebase.google.com open pannunga; Google account use panni project create pannunga.
2. Project Settings > General > Your apps > Web app (</>) add pannunga. App config-la irukkura apiKey, projectId, appId values eduthukkonga.
3. Build > Authentication > Get started > Sign-in method > Anonymous enable pannunga.
4. Build > Firestore Database > Create database pannunga.
5. Firestore Rules tab-la firestore.rules file content paste panni Publish pannunga.
6. Both devices-la same published website open pannunga. Shop & Backup tab-la Firebase API key, Project ID, App ID, and SAME private Shop Sync Code enter panni Save Sync Setup & Connect press pannunga.
7. Shop Sync Code unique and long-a create pannunga; rendu device-layum exact same code. Vera yaarukkum share panna vendam.
8. Sync status 'Connected' nu varanum. Test-ku device A-la sample product add pannunga; internet irukkumbodhu device B refresh/open pannina varudha check pannunga. Bills/products/settings changes internet return aagumbodhu sync queue-la pogum.

IMPORTANT SYNC / SECURITY NOTES
- Firebase free tier limits apply; no guarantee unlimited free usage.
- These starter rules allow any signed-in anonymous Firebase user to read/write a shop path if they know its Shop Sync Code. Keep code private; this is suitable only for a small personal prototype, not sensitive/high-security business data. Production use-ku proper user authentication and shop membership rules configure pannunga.
- Initial Firebase setup/connect-ku internet thevai. Offline billing still works locally; cloud sync happens only after internet returns.
- Existing local data will merge with cloud data by product ID and bill ID. Before first sync, backup both devices. If same bill IDs were independently created on two devices before syncing, conflicts may occur; best to configure sync on both devices before new billing.
- This is not GST-compliant accounting software. Check local tax/invoice requirements if applicable.

D. BILLING / RECEIPT
1. New Bill > product tap > quantity +/- adjust.
2. Customer details optional; discount/payment select pannunga.
3. Save & Print Bill press pannunga. Browser print dialog-la printer or Save as PDF select pannalaam.
4. WhatsApp Share button bill save aana piragu press pannunga; WhatsApp share message open aagum.
5. Old bill print panna Bill History > Print.

E. BACKUP
- Shop & Backup > Download Backup regularly.
- Browser data clear pannina local data pogalaam. Backup file safe-a vechukkonga.
