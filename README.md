# FaceVision — Yuz va His-tuyg'u Tahlili Tizimi

> Individual loyiha | Diplom ishi | Sun'iy intellekt | Kompyuter ko'rishi

---

## 📋 Loyiha haqida

**FaceVision** — bu veb-brauzerni ishlatib, real vaqtda yuzni aniqlash va his-tuyg'ularni tahlil qiluvchi dastur. Loyiha Sun'iy Intellekt va Kompyuter Ko'rishi (Computer Vision) sohalariga asoslangan.

### Asosiy imkoniyatlar
- ✅ Real vaqtda yuz aniqlash (Real-time Face Detection)
- ✅ 7 xil his-tuyg'uni tahlil qilish (Emotion Recognition)
- ✅ Yoshni taxminlash (Age Estimation)
- ✅ Jinsni aniqlash (Gender Detection)
- ✅ Bir vaqtda bir nechta yuzni aniqlash
- ✅ Snapshot (rasm olish) funksiyasi
- ✅ FPS va sessiya statistikasi

### Aniqlanadigan his-tuyg'ular
| Emotion | O'zbekcha | Emoji |
|---------|-----------|-------|
| neutral | Neytral | 😐 |
| happy | Xursand | 😄 |
| sad | G'amgin | 😢 |
| angry | G'azablangan | 😠 |
| fearful | Qo'rqqan | 😨 |
| disgusted | Jirkanch | 🤢 |
| surprised | Hayron | 😮 |

---

## 🛠 Texnologiyalar

| Texnologiya | Maqsadi |
|-------------|---------|
| **HTML5** | Sahifa tuzilmasi |
| **CSS3** | Dizayn va animatsiyalar |
| **JavaScript (ES6+)** | Dastur mantiqi |
| **face-api.js** | AI modellari (TensorFlow.js ustida) |
| **WebRTC (getUserMedia)** | Kameraga kirish |
| **Canvas API** | Yuz ustiga chizish |

### AI Modellari (face-api.js)
1. **SSD MobileNetV1** — Yuzni aniqlash uchun
2. **Face Landmark 68** — Yuz nuqtalarini aniqlash
3. **Face Expression Net** — His-tuyg'ularni tahlil qilish
4. **Age & Gender Net** — Yosh va jinsni aniqlash

---

## 🚀 Ishga tushirish

### Variant 1: To'g'ridan-to'g'ri ochish
```
index.html faylini Chrome/Firefox brauzerida oching
```
> ⚠️ Ba'zi brauzerlar mahalliy faylda kameraga ruxsat bermaydi

### Variant 2: Local server (tavsiya etiladi)
```bash
# Python bilan
python -m http.server 8000

# Brauzerda oching:
http://localhost:8000
```

### Variant 3: VS Code Live Server
VS Code'da "Live Server" extension o'rnating va `index.html` faylida o'ng tugma → "Open with Live Server"

---

## 📁 Loyiha tuzilmasi

```
face-emotion-project/
├── index.html          # Asosiy dastur (barcha kod shu yerda)
└── README.md           # Loyiha hujjati
```

> face-api.js modellari internet orqali CDN'dan yuklanadi (o'rnatish shart emas)

---

## 🎯 Loyiha arxitekturasi

```
Kamera (WebRTC)
    ↓
Video oqimi (HTML5 Video)
    ↓
face-api.js (TensorFlow.js)
    ├── SSD MobileNetV1 → Yuz joylashuvi
    ├── Landmark Net   → 68 ta yuz nuqtasi
    ├── Expression Net → 7 xil his-tuyg'u
    └── Age/Gender Net → Yosh + Jins
    ↓
Canvas API → Natijalarni ekranda ko'rsatish
    ↓
UI yangilanishi (real vaqt)
```

---

## 📊 Ishlash ko'rsatkichlari

- **FPS**: 15-30 kadr/sekund (qurilmaga qarab)
- **Yuz aniqlash aniqligi**: ~95% (SSD MobileNetV1)
- **His-tuyg'u aniqligi**: ~80-85%
- **Kechikish**: <100ms (real vaqt)

---

## 👨‍💻 Muallif

**Individual loyiha** — Diplom ishi  
Texnologiya: Sun'iy Intellekt, Kompyuter Ko'rishi  
Yil: 2024-2025

---

## 📚 Foydalanilgan manbalar

- [face-api.js](https://github.com/justadudewhohacks/face-api.js) — JavaScript Face Recognition Library
- [TensorFlow.js](https://www.tensorflow.org/js) — Machine Learning for JavaScript
- [MDN WebRTC](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API) — Real-time communication
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) — 2D Graphics
