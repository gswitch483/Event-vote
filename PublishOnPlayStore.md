# How to Publish Your Android GPT-4 Vision App on the Google Play Store

## 1. Prepare Your App for Release

### a. App Icon & Branding
- Replace the default app icon (`ic_launcher`) with your unique icon in `res/mipmap-*/`.
- Update `app_name` in `res/values/strings.xml`.

### b. Remove Test Data & Debug Code
- Make sure no test data, logs, or debug code is left.
- Clean up sensitive info: **Never ship your OpenAI API key!**
    - For production, use a backend proxy for OpenAI requests.

### c. Versioning
- In `build.gradle`:
    - Increment `versionCode` and update `versionName`.

### d. Release Build
- In Android Studio:  
  `Build > Generate Signed Bundle / APK > Android App Bundle`
- Follow prompts to create a keystore (save this securely!) and sign your bundle.

---

## 2. Create a Google Play Developer Account

- Go to [Google Play Console](https://play.google.com/console)
- Pay the one-time registration fee (~$25 USD)
- Fill out your developer profile

---

## 3. Prepare Store Listing

- **App name**: Up to 50 characters  
- **Short description**: Up to 80 characters  
- **Full description**: Up to 4000 characters  
- **Screenshots**: At least 2 for phone (1080x1920px recommended), optionally for tablet, 7-inch, 10-inch, etc.  
- **High-res icon**: 512x512px, 32-bit PNG  
- **Feature graphic**: 1024x500px, JPG or 24-bit PNG  
- **Privacy policy URL**: Required if using network/internet, especially with AI  
    - You can use a privacy policy generator or GitHub Pages for hosting

---

## 4. Upload Your App

1. In Play Console, click **Create app**
2. Fill out required info, select app category
3. Upload your signed **App Bundle (.aab)**
4. Add screenshots, icon, feature graphic, descriptions
5. Fill out **Content Rating**, **Data Safety**, and **Privacy Policy**

---

## 5. Set Up App Content

- **Target Audience**: Specify if app is for children
- **Permissions**: Clarify what your app uses and why (e.g., storage, internet, camera if handling images)
- **Sensitive permissions**: Explain why you need them, if applicable

---

## 6. Review & Rollout

- Click **Publish** (or **Submit for review**)
- Google will review (may take hours to a few days)
- You’ll be notified via email if approved or if you need to fix something

---

## 7. Post-Publish

- Share your Play Store link!
- Monitor reviews, crash reports, and analytics in the Play Console

---

## Additional Tips

- **Testing:** Use the Play Console’s closed, open, or internal testing tracks before public release.
- **API Key Security:** Never ship your OpenAI API key. Use a backend for production.
- **Updates:** To update, increment `versionCode` and `versionName`, upload a new `.aab` in Play Console.

---

**References:**
- [Play Console Help](https://support.google.com/googleplay/android-developer)
- [Preparing your app for release](https://developer.android.com/studio/publish/preparing)
- [Launch checklist](https://developer.android.com/distribute/best-practices/launch/launch-checklist)
