# Havo Pro — Android APK Yaratish Yo'riqnomasi

## Loyiha haqida
Bu loyiha **Havo Pro** HTML faylini Android ilovaga (APK) aylantirish uchun tayyorlangan.
Texnologiya: **WebView Wrapper** — HTML/CSS/JS ni Android ichiga o'rab ishlatadi.

---

## 1-USUL: Android Studio (Tavsiya etiladi)

### Talablar
- [Android Studio](https://developer.android.com/studio) o'rnatilgan bo'lishi kerak
- Java yoki Kotlin bilimi shart emas

### Qadamlar

**1. Loyihani oching:**
```
File → Open → HavoPro papkasini tanlang
```

**2. Sync qiling:**
Android Studio avtomatik Gradle sync so'raydi → "Sync Now" bosing

**3. APK yarating:**
```
Build → Build Bundle(s) / APK(s) → Build APK(s)
```

**4. APK joyi:**
```
app/build/outputs/apk/debug/app-debug.apk
```

---

## 2-USUL: Online (Android Studio o'rnatmasdan)

### AppsGeyser.com orqali (Eng oson)
1. https://appsgeyser.com ga kiring
2. "Create App" → "Website" tanlang
3. HTML faylni yuklang yoki localhost URL bering
4. APK yuklab oling — **bepul va imzosiz**

### WebIntoApp.com
1. https://webintoapp.com ga kiring
2. HTML faylni drag-and-drop qiling
3. APK yaratiladi

---

## 3-USUL: Capacitor (Professional)

```bash
npm install -g @ionic/cli
npm install @capacitor/core @capacitor/android
npx cap init HavoPro uz.havopro
npx cap add android
# index.html ni www/ papkaga qo'ying
npx cap sync
npx cap open android
```

---

## Loyiha tuzilmasi

```
HavoPro/
├── app/
│   ├── src/main/
│   │   ├── AndroidManifest.xml      ← Ruxsatlar va konfiguratsiya
│   │   ├── assets/
│   │   │   └── index.html           ← Sizning HTML faylingiz
│   │   ├── java/uz/havopro/
│   │   │   └── MainActivity.java    ← WebView sozlamalari
│   │   └── res/
│   │       ├── layout/activity_main.xml
│   │       ├── values/styles.xml
│   │       └── mipmap-hdpi/ic_launcher.png
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── gradle.properties
```

---

## APKni telefonga o'rnatish

1. APK faylni telefoningizga ko'chiring
2. Sozlamalar → Xavfsizlik → "Noma'lum manbalardan o'rnatish" — yoqing
3. APK faylga bosing → O'rnatish

---

## Muammolar va yechimlar

| Muammo | Yechim |
|--------|--------|
| Gradle sync xatosi | File → Invalidate Caches → Restart |
| SDK topilmadi | SDK Manager dan Android 34 yuklab oling |
| Build muvaffaqiyatsiz | `./gradlew clean` bajaring |

---

## Ikonka almashtirish

`app/src/main/res/mipmap-hdpi/ic_launcher.png` faylini
192×192 px PNG ikonkangiz bilan almashtiring.

---

Savollar uchun Claude.ai ga murojaat qiling! 🚀
