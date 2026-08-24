# AI-Administrator — sotuv sahifasi

Statik sahifa, GitHub Pages uchun. Bitta fayl: `index.html`. Tashqi bog'liqlik faqat Google Fonts.

## Dizayn qarori

**Sahifa — kecha.** Mahsulot soat 21:00 dan keyin sodir bo'ladigan narsani hal qiladi,
shuning uchun zamin ham kecha: chuqur navy (`#0B1220`).

**Bitta urg'u rangi: amber (`#FFB765`) = "javob berildi".**
Jimlik alohida rang bilan emas, **amberning yo'qligi** bilan ko'rsatiladi. Qizil ishlatilmagan —
javobsizlik xavotirli emas, u shunchaki hech narsa. Sahifaning rang mantiqi sotuv dalilining o'zi.

**Signature — jimlik oralig'i.** Sahifa markazida ikkita chat: bir xil kecha, ikki natija.
Chapda xabarlardan keyin punktir chiziq ichida **"JAVOB YO'Q · 11 soat 32 daqiqa"** — u
sahifada jismonan baland joy egallaydi. O'ngda o'sha bo'shliq yo'q: bot 21:42 da javob beradi.
Dalil bezak orqali emas, ikki ustunning **balandlik farqi** orqali ko'rsatiladi.

**Shriftlar:**
- `Bricolage Grotesque` — sarlavhalar (xarakterli, o'ziga xos)
- `Instrument Sans` — matn
- `JetBrains Mono` — **faqat vaqt belgilari va yorliqlar**. Vaqtlar bezak emas, dalil bo'lib
  o'qilishi kerak — chatdagi 21:42 sotuv argumentining o'zi.

**Ataylab qilinmagan:** "01 / 02 / 03 — qanday ishlaydi" bloki yo'q. Tushuntirish namoyishning
o'z ichida, chat yonidagi mono izohlar sifatida ("narxni sizning bilim bazangizdan oldi").
Alohida qadamlar qatori shablon bo'lardi va chat allaqachon ketma-ketlikni ko'rsatib turibdi.

## Tuzilma

1. **Hero** — savol: "Bu xabarga kim javob beradi?"
2. **Ikki kecha** — signature blok (jimlik ↔ javob + lid kartochkasi)
3. **Statistika** — ⚠️ izohga olingan, pastga qarang
4. **Narx** — 500 000 / 700 000
5. **Yopish**

## Jonli manzil

**https://akmalzokirjonov.github.io/ai-administrator/**

Repo: `github.com/akmalzokirjonov/ai-administrator` (public, `main` / `(root)`, HTTPS majburiy).

## Yangilash

```
cd ai-administrator
git add -A
git commit -m "nima o'zgardi"
git push
```

1–2 daqiqada jonli bo'ladi.

## Lokal ko'rish

```
cd ai-administrator
python -m http.server 8765 --bind 127.0.0.1
```

Keyin `http://127.0.0.1:8765`.

## ⚠️ Statistika bloki

`index.html` ichida HTML izohi ostida turibdi. **Ochishdan oldin real raqamlar kerak.**

1. Javobsizlik testini o'tkazing (`docs/sotuv-rejasi.md`)
2. `python javobsizlik.py` natijasini oling
3. `__` o'rniga real raqamlarni qo'ying
4. Izoh belgilarini olib tashlang

**Raqamlarni o'ylab topmang.** Sahifaning butun vazifasi — ishonch.

## Nima yozilmagan (ataylab)

- **Pilot narxi (200–350 ming)** — sahifada yo'q. Sahifada 500 000 turadi, jonli suhbatda
  350 000 aytiladi; shundagina chegirma haqiqiy imtiyoz bo'lib his qilinadi.
- **Kalendar / qabulga yozish** — bot buni qilmaydi va va'da qilinmaydi. Narx ostida ochiq
  izohlangan (`CONTEXT.md`: "yozuv emas, lid").

## Texnik eslatmalar

- **JavaScript o'chirilsa ham hamma matn ko'rinadi.** Yashirish sinfi (`.js`) `<head>` dagi
  skript orqali qo'shiladi; skript ishlamasa hech narsa yashirilmaydi.
- Animatsiya `IntersectionObserver` bilan, lekin **1.8 soniyalik zaxira taymer** bor —
  observer ishlamasa ham kontent ko'rinadi. Sotuv sahifasi hech qachon bo'sh qolmasligi kerak.
- `prefers-reduced-motion` hurmat qilinadi.
- Klaviatura fokusi ko'rinadigan (`:focus-visible`, amber halqa).
- Mobil: 860px dan pastda ikki chat ustma-ust joylashadi.
