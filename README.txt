FLOWLINE - Android app (taiyaar project)

Is folder mein pura Android project ("android" folder) pehle se bana hua hai.
Game ki file: www/index.html. App ka naam Flowline, icon bhi laga hua hai.

--------------------------------------------------
RASTA 1: Bina Android Studio ke (GitHub se APK)
--------------------------------------------------
1. github.com par free account banao, ek naya repository banao.
2. Is poore folder ki saari files us repository mein upload karo
   (".github" folder bhi - wo hidden hota hai, isliye folder ko drag karke upload karo).
3. Repository ke "Actions" tab mein "Build APK" apne aap chalega (5-10 minute).
   Na chale to "Build APK" > "Run workflow" dabao.
4. Khatam hone par us run ko kholo, neeche "Artifacts" mein "flowline-apk" download karo.
5. Zip kholo, andar app-debug.apk hai. Phone mein bhej kar install karo
   (Settings mein "Install unknown apps" allow karna padega).

--------------------------------------------------
RASTA 2: Android Studio se
--------------------------------------------------
1. Node.js aur Android Studio install karo.
2. Is folder mein terminal kholo:
     npm install
     npx cap sync android
     npx cap open android
3. Gradle sync poora hone do. Phir:
   Build > Build Bundle(s) / APK(s) > Build APK(s)
   APK: android/app/build/outputs/apk/debug/app-debug.apk

--------------------------------------------------
Play Store ke liye
--------------------------------------------------
Android Studio mein Build > Generate Signed Bundle / APK > Android App Bundle (.aab).
Apni keystore (signing key) sambhal kar rakhna, kho gayi to app update nahi hoga.
Debug APK sirf testing ke liye hai. Package naam com.flowline.game ko apne unique naam se badal sakte ho.

--------------------------------------------------
Badlav karne hain?
--------------------------------------------------
- www/index.html edit karo, phir:  npx cap sync android
- Share button ka link: www/index.html mein  const LINK=  dhundh kar apni website / Play Store link daal do.
- App ka naam: android/app/src/main/res/values/strings.xml
