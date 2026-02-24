---
title: ".uz domen oldim. 27,000 so'm. 10 daqiqa."
date: 2026-02-24
tags: ["hosting", "domen", "uzbekiston", "deploy"]
description: "O'zbekistonda domen olish, hosting tanlash va saytni deploy qilish. Ahost, Netlify, Cloudflare. Narxlar va jarayon."
draft: false
---

Birinchi loyihamni deploy qilmoqchi bo'lganimda, men domen nima ekanini bilmas edim. DNS, nameserver, A-record — bular menga chet tildek edi. Keyin ahost.uz da .uz domen oldim. 27,000 so'm. 10 daqiqa. Shu maqolada jarayonni boshidan oxirigacha ko'rsataman.

## Domen nima?

Domen — bu saytingizning manzili. `google.com`, `kun.uz`, `shumbola-blog.netlify.app`. Odamlar brauzerga shu manzilni yozadi va saytingiz ochiladi.

`.uz` — O'zbekistonning milliy domeni. Uni [UZINFOCOM](https://cctld.uz) boshqaradi. 2026 yil fevral holatida 148,000 dan ortiq `.uz` domen ro'yxatdan o'tgan.

```
Domen tuzilishi:

shumbola.uz
   │       │
   │       └── TLD (Top Level Domain) — .uz, .com, .net
   │
   └── Domen nomi — siz tanlaysiz

blog.shumbola.uz
  │
  └── Subdomen — bepul, cheksiz yaratish mumkin
```

## .uz domen zonalari

Hammasi `.uz` bilan tugamaydi. Bir nechta zona bor:

| Zona | Kim uchun | Kim olishi mumkin |
|------|-----------|-------------------|
| .uz | Har kimga — shaxsiy, biznes, loyiha | Har kim, har qanday fuqarolik |
| .com.uz | Tijorat saytlari | Faqat O'zbekiston fuqarolari |
| .co.uz | Tijorat (alternativa) | Faqat O'zbekiston fuqarolari |
| .org.uz | Tashkilotlar | Faqat O'zbekiston fuqarolari |
| .net.uz | Tarmoq xizmatlari | Faqat O'zbekiston fuqarolari |

Menimcha, ko'pchilik uchun oddiy `.uz` yetarli. Chet ellik bo'lsangiz ham olishingiz mumkin. `.com.uz` va boshqalar faqat O'zbekiston pasporti bilan.

## Qayerdan domen olish?

O'zbekistonda 19 ta akkreditatsiyalangan registrator bor. Men narxlarni solishtirib ko'rdim:

| Registrator | .uz narxi (yiliga) | O'ziga xosligi |
|-------------|-------------------|----------------|
| [Ahost.uz](https://ahost.uz) | 27,000 so'm | ICANN akkreditatsiya, eng katta (~58,000 domen) |
| [Airnet.uz](https://airnet.uz) | 27,000 so'm | TAS-IX DNS, 1 Gbps |
| [Eskiz.uz](https://eskiz.uz) | 29,000 so'm | 50,000+ domen, Payme qabul qiladi |
| [PSCloud.uz](https://pscloud.uz) | 30,500 so'm | 7 ta data center |
| [Hostmaster.uz](https://hostmaster.uz) | 34,000 so'm | Yillik to'lovda bepul .uz |
| [ITSG.uz](https://itsg.uz) | 35,000 so'm | Qo'lda aktivatsiya |

27,000 so'm — bu taxminan $2. Yiliga. `.com` domen xorijda $10-14 turadi. `.uz` ancha arzon.

**Muhim:** xorijiy registratorlarda (INWX, EuroDNS) `.uz` olish 10 barobar qimmat — $100+. Faqat mahalliy registratordan oling.

## Men qanday oldim

Ahost.uz ga kirib, "Domen ro'yxatdan o'tkazish" bo'limiga o'tdim. Nomni yozdim, tekshirdim — band emas, buyurtma berdim.

Kerak bo'lgan ma'lumotlar:
- Ism, familiya
- Pasport seriya va raqam
- PINFL (O'zbekiston fuqarolari uchun)
- Telefon va email
- DNS server manzillari

DNS serverni bilmasangiz — registratorning o'zinikini yozing, keyin o'zgartirish mumkin.

`.uz` domenlar qo'lda aktivatsiya qilinadi. Dam olish kunlari ishlamaydi. Men shanba kuni buyurtma berdim, dushanba kuni aktivatsiya bo'ldi. Shuning uchun shoshilsangiz — ish kunlari oling.

## Hosting nima va kerakmi?

Hosting — bu saytingiz fayllari turgan kompyuter. Ikki tur bor:

```
Klassik hosting:                 Bepul platformalar:

Siz to'laysiz                   Siz to'lamaysiz
Fayl serverda turadi             Fayl Git da turadi
cPanel bilan boshqarasiz         Git push bilan deploy
PHP, MySQL ishlaydi              Faqat statik saytlar (HTML, Hugo, Next.js)
Har oylik to'lov                 Bepul (limitlar bilan)

Kimga: WordPress, PHP saytlar    Kimga: blog, portfolio, landing
Narx: 20,000-50,000 so'm/oy     Narx: $0
```

Agar blog yoki portfolio qilayotgan bo'lsangiz — bepul platformalar yetarli. WordPress yoki PHP kerak bo'lsa — hosting kerak.

## O'zbek hostinglar solishtirish

| Provayder | Eng arzon tarif | Disk | cPanel | TAS-IX |
|-----------|----------------|------|--------|--------|
| [Ahost.uz](https://ahost.uz) | 33,000 so'm/oy | 500 MB | Ha | Ha |
| [Hostmaster.uz](https://hostmaster.uz) | 19,900 so'm/oy | 1 GB | Ha | Ha |
| [Eskiz.uz](https://eskiz.uz) | 16,700 so'm/oy | — | Ha | Ha |
| [Billur.com](https://billur.com) | 20,000 so'm/oy | — | Ha | Ha |

Hammasi TAS-IX da — ya'ni O'zbekiston ichida tez ishlaydi. [Ahost](https://ahost.uz/news/510) eng qimmat, lekin eng katta (38,000+ mijoz, 500+ davlat tashkiloti). Hostmaster eng arzon.

**TAS-IX nima?** Toshkentdagi internet almashish nuqtasi. Saytingiz TAS-IX dagi serverda tursa, O'zbekistondagi foydalanuvchilar uchun tez ochiladi — trafik chet elga chiqmaydi.

## Bepul alternativalar

Blog, portfolio yoki landing page uchun hosting sotib olish shart emas:

| Platforma | Trafik | Build | Kuchli tomoni |
|-----------|--------|-------|---------------|
| [Cloudflare Pages](https://pages.cloudflare.com) | Cheksiz | 500 build/oy | Eng tez, cheksiz trafik |
| [Netlify](https://netlify.com) | ~10 GB | 300 daqiqa/oy | Oson sozlash |
| [Vercel](https://vercel.com) | 100 GB | 6,000 daqiqa/oy | Next.js uchun ideal |
| [GitHub Pages](https://pages.github.com) | 100 GB | — | Eng oddiy |

Bu blogning o'zi Netlify da turadi. $0 to'layman. Hugo bilan yozaman, `git push` qilaman, Netlify o'zi build qiladi. Bepul SSL, bepul subdomen (`shumbola-blog.netlify.app`).

Menimcha, yangi boshlovchilar uchun Cloudflare Pages eng yaxshi — trafik cheksiz va tez.

## Domenni bepul hostingga ulash

Ahost da `.uz` domen oldingiz. Netlify yoki Cloudflare da sayt deploy qildingiz. Endi domenni ulash kerak.

**Netlify uchun:**

Registrator panelida (ahost.uz) DNS yozuvlarni o'zgartiring:

```
Turi    Nomi          Qiymati
─────   ──────────    ──────────────────────────
A       @             75.2.60.5
CNAME   www           sayt-nomi.netlify.app
```

**Cloudflare Pages uchun:**

Cloudflare nameserverlarini registratorda yozing:

```
NS1:  ada.ns.cloudflare.com
NS2:  bob.ns.cloudflare.com
```

Keyin Cloudflare panelida domenni qo'shing. SSL avtomatik beriladi.

DNS o'zgarishlar 24-48 soat ichida tarqaladi. Lekin odatda 1-2 soatda ishlaydi.

## SSL haqida

SSL — bu saytingiz manzili oldida `https://` ko'rinishi. Brauzer "xavfsiz" deb ko'rsatadi. Bunsiz Google saytingizni past reytingga tushiradi.

Bepul SSL hamma joyda bor:

- Netlify, Vercel, Cloudflare, GitHub Pages — avtomatik bepul SSL
- Ahost, Billur, Hostmaster — Let's Encrypt bepul SSL kiritilgan
- Pullik SSL (DigiCert, $218+/yil) — faqat banklar va katta do'konlarga kerak. Blogga kerak emas.

## Xulosa

`.uz` domen 27,000 so'm — yiliga $2. Uni ahost.uz dan 10 daqiqada olish mumkin. Blog uchun hosting sotib olish shart emas — Netlify yoki Cloudflare Pages bepul. DNS sozlab, domenni ulaysiz.

```
Minimal sayt chiqarish:

Domen (.uz):      27,000 so'm/yil  (~$2)
Hosting:          $0 (Netlify/Cloudflare)
SSL:              $0 (avtomatik)
─────────────────────────────────────────
Jami:             27,000 so'm/yil
```

Birinchi saytingizni deploy qilish uchun $2 va 1 soat vaqt yetarli.
