# Free Fire Spinner — GitHub Build Ready

यह project एक generic Android app है जो bundled Python runner को app के अंदर चलाने के लिए Chaquopy का उपयोग करता है। इसमें किसी game bypass/cheat functionality को शामिल नहीं किया गया है।

## सबसे आसान APK तरीका — GitHub Actions

1. इस पूरे project folder की सभी files GitHub repository के root में upload करें।
2. GitHub में **Actions** tab खोलें।
3. **Build Free Fire Spinner APK** workflow चुनें।
4. **Run workflow** दबाएँ।
5. Build पूरा होने के बाद नीचे **Artifacts** में `FreeFireSpinner-debug-apk` मिलेगा।
6. उसे डाउनलोड करके ZIP खोलें और `app-debug.apk` install करें।

Workflow cloud runner पर JDK, Android SDK और Gradle तैयार करके `assembleDebug` चलाता है। इसलिए फोन में Android Studio/AndroidIDE/SDK लगाने की जरूरत नहीं है।

## App features

- Main dashboard सीधे खुलता है; normal user login नहीं।
- ऊपर Admin Login।
- Admin project files import कर सकता है।
- Bundled Python `runner.py` app के साथ आता है।
- START / STOP / RESTART।
- Live stdout/stderr log panel।
- Python `input()` के लिए input box + SEND।
- Android foreground service notification।
- Project और output files list।
- Text file viewer।
- Android Share / Save-As export।
- Android app sandbox में limited shell command box।
- Dark/cyber-style UI।

## Demo admin

Username: `admin`
Password: `Ravi@12345`

यह demo/local credential है। Production app में इसे बदलना जरूरी है।

## जरूरी ईमानदार limitation

यह source project cloud-build-ready है, लेकिन इस chat environment में Android SDK + Gradle + Chaquopy dependencies के साथ पूरा APK build/run करके verify नहीं किया गया है। इसलिए इसे पहले से "100% tested APK" कहना सही नहीं होगा। GitHub Actions build log किसी dependency/configuration error को सीधे दिखाएगा।

साथ ही Android app sandbox का shell Termux जैसा full Linux shell नहीं है। Arbitrary native Python packages भी हर बार Android पर compatible नहीं होते; pure-Python packages अधिक आसान होते हैं।
