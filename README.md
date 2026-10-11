# Qarz daftari

Do'konlar uchun qarzlar hisobi dasturi. Ma'lumotlar qurilmaning o'zida (LocalStorage) saqlanadi.
Bu loyiha GitHub Actions yordamida avtomatik APK yig'adi, kompyuterda Android Studio kerak emas.

## APK olish (5 qadam)

1. github.com saytida yangi repository oching (masalan `qarz-daftari`).
2. Shu papkadagi hamma fayllarni repository ga yuklang. Papka tuzilishi quyidagicha bo'lishi shart:

   ```
   www/index.html
   .github/workflows/build-apk.yml
   package.json
   capacitor.config.json
   .gitignore
   README.md
   ```

3. Yuklangandan so'ng GitHub avtomatik ishga tushadi. **Actions** bo'limiga kiring va **Build APK** ishi tugashini kuting (taxminan 4-7 daqiqa). Qo'lda ishga tushirish uchun: Actions -> Build APK -> Run workflow.
4. Ish yashil belgi bilan tugagach, uni oching va pastdagi **Artifacts** qismidan `qarz-daftari-apk` ni yuklab oling.
5. Zip ichidagi `app-debug.apk` ni telefonga o'tkazib o'rnating (Sozlamalar ichida "noma'lum manbalardan o'rnatish" ruxsatini yoqish kerak bo'ladi).

## Dasturni o'zgartirish

Hamma narsa `www/index.html` faylida. Uni GitHub da tahrirlab saqlasangiz, yangi APK avtomatik yig'iladi.

## Eslatmalar

- Bu `debug` APK: telefonga o'rnatish uchun yetarli, lekin Google Play ga yuklash uchun imzolangan `release` versiya kerak.
- Shriftlar Google Fonts dan yuklanadi. Internet bo'lmasa, tizim shrifti ishlatiladi, dastur baribir ishlaydi.
- Ma'lumotlar telefonda saqlanadi. Dasturni o'chirsangiz yoki ma'lumotlarini tozalasangiz, daftar ham o'chadi.
