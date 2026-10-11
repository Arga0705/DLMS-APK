# L-TRONIK DSP PRO - aplikasi Android

Bungkus Capacitor untuk UI BLE. Memakai plugin @capacitor-community/bluetooth-le (BLE native),
protokolnya sama dengan firmware v1.9.4.

## Syarat
- Node.js 20 atau lebih baru
- Android Studio (sudah termasuk JDK dan Android SDK)

## Bangun APK
    npm install
    npm run apk

Hasil: android/app/build/outputs/apk/debug/app-debug.apk (kirim ke HP, izinkan "install dari sumber tidak dikenal").

Atau lewat Android Studio:
    npm install
    npm run setup
    npx cap open android      (lalu Build > Build APK)

## Catatan
- Android 12 ke atas meminta izin "Perangkat di sekitar"; Android 11 ke bawah meminta izin lokasi (aturan Android untuk pemindaian BLE).
- Mengubah UI: edit index.html lalu jalankan npm run setup lagi.
- Ikon bawaan Capacitor; ganti lewat Android Studio (File > New > Image Asset).

## Bangun APK otomatis di GitHub (tanpa Android Studio)
1. Unggah isi folder ini ke repo GitHub.
2. Tab Actions > Build APK > Run workflow. APK muncul di bagian Artifacts.
3. Untuk tautan unduh tetap: buat tag, mis. `git tag v1.9.4 && git push --tags`. APK terlampir di Releases.
4. Isi `APK_URL` di index.html dengan
   https://github.com/NAMA/REPO/releases/latest/download/ltronik-dsp.apk
   agar tombol "Unduh APK" di versi web mengarah ke sana.
