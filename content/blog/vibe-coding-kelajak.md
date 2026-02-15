---
title: "6 oyda 4 loyiha yaratdim. Bitta qator kod yozmadim."
date: 2026-02-15
tags: ["vibe-coding", "AI", "kelajak", "dasturlash"]
description: "CallMind, SpeakQuest, SoliqBot, blog. Hammasini Claude Code yozdi. Men faqat muammoni tushuntirdim."
draft: false
---

O'tgan yili men bitta loyihani 2 haftada tugatdim. Undan oldingi loyiham 3 oy olgan edi. Farqi nima? Birinchisini men yozdim. Ikkinchisini AI yozdi, men faqat boshqardim.

## Vibe coding — bu nima?

2025 yil fevralda Andrej Karpathy — Tesla va OpenAI ning sobiq bosh muhandisi — yangi atama kiritdi: **vibe coding**. U [tweetida](https://x.com/karpathy/status/1886192184808149383?lang=en) shunday yozdi:

> "Yangi turdagi dasturlash bor — men uni vibe coding deb atayman. Siz LLM ga muammoni tushuntirasiz, u kod yozadi, siz natijani ko'rasiz. Kod borligini ham unutasiz."

Tweetni 4.5 million kishi ko'rdi. Men buni o'qiganimda tushundim: men allaqachon shunday ishlayman. CallMind, SpeakQuest, bir nechta Telegram bot — hammasi shu usulda yaratilgan. Men sintaksis yozmayman. Men muammoni tushuntiraman.

## Raqamlar

| Ko'rsatkich | Raqam | Manba |
|------------|-------|-------|
| AI yozgan kod ulushi (global) | 41% | [EliteBrains](https://www.elitebrains.com/blog/aI-generated-code-statistics-2025) |
| Microsoft kodining AI ulushi | 20-30% | [TechCrunch](https://techcrunch.com/2025/04/29/microsoft-ceo-says-up-to-30-of-the-companys-code-was-written-by-ai/) |
| iOS applar o'sishi (YoY) | 60% | [Business of Apps](https://www.businessofapps.com/news/agentic-coding-drives-number-ios-apps-highest-level-ever) |
| AI tool ishlatadigan dasturchilar | 65% haftalik | [Stack Overflow 2025](https://survey.stackoverflow.co/2025/ai) |
| Yosh dasturchilar (22-25) ish kamaymasi | -20% | [Stanford/TIME](https://time.com/7312205/ai-jobs-stanford/) |

Oxirgi qatorga e'tibor ber. Stanford tadqiqotchilari ADP payroll ma'lumotlarini tahlil qilishdi — millionlab ishchilar, minglab kompaniyalar. 22-25 yoshdagi dasturchilar orasida bandlik 2022 cho'qqisiga nisbatan [20% ga tushgan](https://www.finalroundai.com/blog/stanford-study-shows-young-software-developers-losing-jobs-to-ai).

30 yoshdan kattalar? Ularning bandligi 6-12% ga **o'sgan**.

Sababi oddiy. AI sintaksisni yaxshi biladi — universitetda o'rgatadigan narsani. Lekin muammoni tushunish, arxitektura qurish, foydalanuvchi ehtiyojini anglash — buni hali AI qila olmaydi. Menimcha, buning sababi shuki, tajribali dasturchi "nima qurish kerak" degan savolga javob bera oladi. Yosh dasturchi faqat "qanday qurish kerak" ni biladi — va aynan shu qismni AI o'z zimmasiga oldi.

## Men nima qildim

Men professional dasturchi emasman. Lekin 2025 yil avgustdan beri men to'rtta loyiha yaratdim:

- **CallMind** — ovozli AI yordamchi. 3 kun davomida Claude Code bilan yozdim. Eng qiyin joyi — ovoz tanish API ni to'g'ri ulash edi. 2 soat davomida AI ga turli yo'llarni sinab ko'rishni aytdim, oxiri Whisper API bilan ishladi.
- **SpeakQuest** — ingliz tili o'rganish ilovasi. Buni 5 kunda tugatdim. Bitta bug 4 soat vaqtimni oldi — AI noto'g'ri state management qilgan edi. O'zim kod o'qib tushunmadim, lekin muammoni tavsiflashni o'rgandim.
- **SoliqBot** — QQS hisoblash boti Telegramda. Eng tez loyiham — 1 kun. Telegram Bot API oddiy ekan, AI deyarli xatosiz yozdi.
- Bu blog — Hugo + PaperMod + Netlify. Deploy qilish 2 soat oldi.

Bularning birortasida men for loop yoki if statement yozmadim. Claude Code ga aytdim: "menga shunday narsa kerak" — u qildi. Ishlamasa, tuzatishni so'radim.

```
Eski usul:                    Yangi usul:

Muammo → Sintaksis o'rgan     Muammo → AI ga tushuntir
       → Kod yoz                     → Natijani tekshir
       → Debug qil                   → Yo'naltir
       → Qayta yoz                   → Deploy qil
       → Deploy qil

Vaqt: 3 oy                   Vaqt: 2 hafta
```

## "Bu haqiqiy dasturlash emas"

Bu gapni ko'p eshitaman. Excel formulasi yozgan odamga ham xuddi shunday deyishgan. HTML yozganlarga ham. Python yozganlarga ham. No-code ishlatganlarga ham.

"Haqiqiy dasturlash" chegarasi har 10 yilda siljiydi. Endi u yana siljidi.

Karpathy o'zi ham [2026 yil fevralda](https://thenewstack.io/vibe-coding-is-passe/) terminni yangiladi — endi **"Agentic Engineering"** deydi:

> "99% vaqt siz kod yozmaysiz, AI agentlarni boshqarasiz va nazorat qilasiz."

Menimcha, bu to'g'ri nom. Men ham 99% vaqt kod yozmayman — muammoni tushuntiraman, natijani tekshiraman, yo'nalish beraman.

## Kim yutadi, kim yutqazadi?

[Gartner bashorati](https://venturebeat.com/business/gartner-citizen-developers-will-soon-outnumber-professional-coders-4-to-1/): 2026 yilga kelib citizen developer lar professional dasturchilardan **4:1** nisbatda ko'p bo'ladi.

Misollar allaqachon bor. [Lovable platformasida](https://techcrunch.com/2025/11/10/lovable-says-its-nearing-8-million-users-as-the-year-old-ai-coding-startup-eyes-more-corporate-employees/) Lissabondagi 11 yoshli bola Facebook klonini yaratdi — CEO Anton Osika Web Summit da aytdi. Shvetsiyalik ikki kishi platformada 7 oyda startap qurdi va yiliga $700,000 topmoqda. Platformaning o'zi 8 million foydalanuvchiga yetdi.

Oldin loyiha yaratish 6 oy va $50,000 talab qilar edi. Endi — [1 hafta va $500 dan kam](https://www.ptolemay.com/post/can-ai-build-your-app-the-no-bs-guide-for-founders).

## Nima qilish kerak

Stanford tadqiqoti aniq ko'rsatdi — faqat sintaksis bilish ish bermayapti.

Men 6 oy davomida 4 ta loyiha qilib o'rgangan narsalarim:

1. **Muammoni aniq ifoda qilish.** SoliqBot da men "QQS hisoblash boti yoz" deganimda AI nima qilishni bilmadi. "Foydalanuvchi summa kiritadi, bot 12% QQS qo'shib javob beradi" deganimda — 20 daqiqada tayyor bo'ldi.
2. **Natijani tezda baholash.** SpeakQuest da AI yozgan kodni o'qib tushunmasdim. Lekin ilovani ishga tushirib, 30 soniyada "ishlayapti" yoki "ishlamayapti" ni bilardim.
3. **Qismlarni birlashtirish.** CallMind da ovoz tanish, AI javob, va audio output — uchta alohida qism. Har birini AI yozdi, lekin ularni qanday ulashni men o'ylab topdim.

Dasturlash tilini o'rganma. Muammoni tushunishni o'rgan. Qolganini AI qiladi.

Sinab ko'r.
