NSM TECHNOLOGIES — WEBSITE
==========================

WHAT'S INCLUDED
- Home, About us, Our apps, Contact and app-specific privacy pages
- Responsive design for mobile and desktop
- Google Play links for Game Zone: Classic Games and My Talking Cat
- Contact page email: ludofuncontact@gmail.com
- Separate privacy policies for each app
- Supplied NSM Technologies logo and both supplied app icons in public/images/
- Subtle app-icon animations that respect reduced-motion settings
- Firebase Hosting configuration
- Unity LevelPlay app-ads.txt served at the hosting root from public/app-ads.txt

BEFORE YOU PUBLISH
1. Review the app descriptions and illustrative artwork against the current Google Play listings.
2. Review public/privacy-game-zone.html and public/privacy-my-talking-cat.html to confirm that the supplied disclosures match each app's actual data practices and current advertising SDK configuration.
3. Both app privacy policies use ludofuncontact@gmail.com as the contact address.
4. Compare every seller entry in public/app-ads.txt with the complete, authorized list in your Unity dashboard. Keep only entries authorized for your apps.
5. Configure the correct publisher domain in Google Play and Unity. If you add an ownerdomain field, use only your verified publisher domain.
6. After deployment, visit https://YOUR_DOMAIN/app-ads.txt and confirm the file is publicly accessible at the domain root and contains the final authorized seller list.

DEPLOYMENT FROM ANDROID
This is easiest if you can use Google Cloud Shell in Chrome. Desktop site mode may help.
1. Create a Firebase project at https://console.firebase.google.com/
2. Open https://shell.cloud.google.com/ and sign in.
3. Upload/extract this ZIP in Cloud Shell, or recreate the files there.
4. Ensure firebase.json is in the project root and website files are inside public/.
5. Run: firebase deploy --only hosting
6. Open the Hosting URL shown by Firebase and check /app-ads.txt.
7. For a custom domain, open Firebase Console > Hosting > Add custom domain and follow its DNS instructions. DNS changes can take time.
8. Check https://YOUR_DOMAIN/app-ads.txt after the custom domain is connected. Firebase's "public" folder is the website document root, so public/app-ads.txt is served as /app-ads.txt.

IMPORTANT ABOUT THE ZIP
The ZIP is the website source files; it does not deploy the site automatically.
Firebase hosting may ask you to initialize/select a project if setup has not been completed.
Unity verification will not succeed until the deployed file, domain, and authorized seller list match the values in your Unity dashboard.
