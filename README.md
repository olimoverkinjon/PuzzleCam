# PuzzleCam

**Qo‘l harakatlari bilan boshqariladigan brauzer fotobutkasi va suratli boshqotirma.**

**A gesture-controlled browser photobooth and photo puzzle.**

[O‘zbekcha](#o‘zbekcha) · [English](#english)

---

## O‘zbekcha

Kamera qarshisida qo‘llaringiz bilan ramka yasang, suratga tushing va uni 3×3 boshqotirma qilib yig‘ing. Tayyor suratlar albomga qo‘shiladi va bitta PNG fayl sifatida yuklab olinadi. Ilova interfeysini **UZ / EN** tugmalari bilan almashtirish mumkin.

### Imkoniyatlar

- Qo‘l harakatlari orqali suratga olish va boshqotirma o‘ynash
- Uchta suratgacha albomga yig‘ish va PNG qilib yuklab olish
- O‘zbekcha va inglizcha interfeysi
- Mobil va kompyuter ekranlariga moslashuvchan ko‘rinish
- Suratlar brauzerdan chiqmaydi; sahifani yangilaganda albom tozalanadi

### Ishga tushirish

Kamera brauzerda ishlashi uchun loyiha lokal HTTP server orqali ochilishi kerak. Loyiha papkasida terminal oching:

```powershell
python -m http.server 5500
```

Brauzerda [http://localhost:5500](http://localhost:5500) manzilini ochib, kamera ruxsatini bering. VS Code’dagi Live Server kengaytmasidan ham foydalanish mumkin.

**Talablar:** kamera, zamonaviy brauzer (Chrome yoki Edge tavsiya etiladi) va MediaPipe modelini ilk marta yuklash uchun internet.

### Boshqaruv

1. Ikki qo‘l ko‘rsatkich barmog‘i bilan surat ramkasining ikki chetini belgilang.
2. Ikkala qo‘lda bosh barmoq va ko‘rsatkich barmoq uchini yaqinlashtirib, qisqa ushlab turing. Uch soniyalik hisobdan keyin surat olinadi.
3. Bo‘lakni chimdib ushlab, kerakli katakka olib boring.
4. Boshqotirma yig‘ilgach, mushtni qisqa ushlab suratni albomga saqlang.
5. Albomdagi suratlarni **Suratlarni yuklab olish** tugmasi orqali bitta PNG fayl qilib yuklab oling.

> Musht qilish boshqotirma yechilgandan so‘ng suratni saqlaydi. Yechilmagan bo‘lsa, boshqotirma yangidan boshlanadi.

### Texnologiyalar

- [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) — qo‘l nuqtalarini aniqlash
- Canvas 2D — kamera tasviri va boshqotirma bo‘laklarini chizish
- JavaScript ES modullari va CSS
- Tashqi kutubxonalar CDN orqali yuklanadi; alohida o‘rnatish talab qilinmaydi

### Muammolarni bartaraf etish

- **Kamera yoqilmayapti:** saytga kamera ruxsati berilganini va kamera boshqa ilovada ishlamayotganini tekshiring.
- **Model yuklanmayapti:** internet aloqasini tekshiring; MediaPipe jsDelivr’dan, qo‘l modeli Google Storage’dan yuklanadi.
- **Sahifa bo‘sh ko‘rinmoqda:** HTML faylni bevosita ochmang, lokal server orqali ishga tushiring.
- **Chimdib ushlash aniqlanmayapti:** yorug‘ joyda turing va ikkala qo‘lni kameraga to‘liq ko‘rsating.

---

## English

Frame a shot with your hands, take a photo, then solve it as a 3×3 puzzle. Completed photos are added to an album and can be downloaded together as a single PNG. Switch the app language with the **UZ / EN** buttons.

### Features

- Take photos and solve puzzles using hand gestures
- Collect up to three photos and download them as a PNG
- Uzbek and English interface
- Responsive layout for desktop and mobile
- Photos stay in the browser and are cleared when the page is refreshed

### Run locally

The camera requires the app to be served over a local HTTP server. Open a terminal in the project folder and run:

```powershell
python -m http.server 5500
```

Open [http://localhost:5500](http://localhost:5500) in your browser and grant camera access. You can also use the Live Server extension in VS Code.

**Requirements:** a camera, a modern browser (Chrome or Edge recommended), and an internet connection to download the MediaPipe model on first launch.

### Controls

1. Frame the shot using the index fingers of both hands.
2. Pinch your thumb and index finger on both hands and hold briefly. A three-second countdown starts before the photo is taken.
3. Pinch a tile and move it to the correct cell.
4. Once the puzzle is solved, briefly make a fist to save the photo to the album.
5. Use **Download photos** to save the album as one PNG file.

> Making a fist saves a solved puzzle. If the puzzle is not solved, it starts over.

### Built with

- [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) for hand landmark detection
- Canvas 2D for the camera preview and puzzle rendering
- JavaScript ES modules and CSS
- External libraries are loaded from CDNs; no package installation is needed

### Troubleshooting

- **Camera does not start:** allow camera access for the site and make sure another app is not using it.
- **The model does not load:** check your internet connection. MediaPipe is loaded from jsDelivr and the hand model from Google Storage.
- **The page is blank:** serve the app locally instead of opening the HTML file directly.
- **Pinch gestures are not detected:** use good lighting and keep both hands fully in view.

---

## License

MIT
