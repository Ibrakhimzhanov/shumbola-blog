---
title: "1 plugin o'rnatdim. Claude Code o'zi ishladi."
date: 2026-02-15
tags: ["claude-code", "AI", "vibe-coding", "tools"]
description: "Superpowers plugini Claude Code ni avtonom agentga aylantiradi. O'rnatish 1 daqiqa. Agent savol beradi, rejalashtiradi, o'zi yozadi."
draft: false
---

Kecha men Claude Code ga "yangi blog post yoz" dedim. U darhol yozishga kirishmadi. Avval so'radi: "Kim uchun? Qanday ohangda? Asosiy xulosa nima?" Men javob berdim. U reja tuzdi. 5 bosqichli pipeline qurdi. Keyin yozdi. Men faqat tekshirdim.

Bir oy oldin bunday bo'lmas edi. Har bir qadamni men aytishim kerak edi. Nima o'zgardi? Bitta plugin o'rnatdim.

## Superpowers nima?

Jesse Vincent yaratgan open-source plugin. Claude Code uchun "skill" lar to'plami. [GitHub da 52,000 dan ortiq yulduz](https://github.com/obra/superpowers) yig'gan.

Oddiy qilib aytsam og'alar: bu plugin Claude Code ga ishlash usulini o'rgatadi. Agent avval savol beradi, keyin reja tuzadi, keyin yozadi. Siz boshqarasiz, u ishlaydi.

Jesse Vincent [blogida](https://blog.fsck.com/2025/10/09/superpowers/) asosiy g'oyani tushuntiradi: agent kod yozish usulini biladi, siz faqat nima qurish kerakligini aytasiz. Qolganini u o'zi tashkil qiladi.

## Qanday ishlaydi?

Pluginni o'rnatganingizdan keyin Claude Code ning xulq-atvori o'zgaradi. Qaraymiz og'alar:

```
Oddiy Claude Code:              Superpowers bilan:

"Nima qilishim kerak?"          "Nima qurmoqchisiz?"
  ↓                               ↓
Siz hamma narsani               Sizga savollar beradi
aytasiz                           ↓
  ↓                             Dizayn taklif qiladi
U yozadi                          ↓
  ↓                             Siz tasdiqlaysiz
Xato bo'lsa qayta                 ↓
tushuntirasiz                   Reja yozadi (tasklar bilan)
                                  ↓
                                Har bir taskni alohida bajaradi
                                  ↓
                                Test yozadi, tekshiradi
                                  ↓
                                Kod tayyor
```

Farqni ko'ryapsizmi? Chap tomonda siz bosh. O'ng tomonda agent bosh, siz nazoratchi.

## Men qanday ishlataman

Mana 3 ta real misol.

**Blog yozish.** Bu blogni yozayotganda Claude Code menga avval 4 ta savol berdi. Auditoriya kim? Ohang qanday? Asosiy xulosa nima? Men javob berdim, u research qildi, qoralama yozdi, 4 ta parallel critic orqali tekshirdi. Men faqat natijani ko'rdim va tuzatdim.

**Bot yangilash.** SoliqBot ni yangilayotganda agent reja yaratdi. Har bir qismni alohida task qilib bo'ldi. Birinchi test yozdi (RED deyiladi, ya'ni xato chiqadigan test). Keyin kodni yozdi (GREEN, test o'tadi). Keyin tozaladi (REFACTOR). Bu professional dasturlashda TDD deyiladi. Men buni qo'lda qilmayman, agent o'zi majburiy qiladi.

**Debugging.** Bitta botda xato bor edi, 2 kun topa olmadim. Superpowers bilan Claude Code 4 bosqichli tizimdan o'tkazdi: simptom, sabab, tuzatish, tekshirish. 20 daqiqada topdi. Men 2 kun sarfladim, agent 20 daqiqa.

## Asosiy skilllar

Superpowers ichida bir nechta "skill" bor. Har biri agentga bitta ishni to'g'ri qilishni o'rgatadi:

| Skill | Nima qiladi | Qachon ishlaydi |
|-------|------------|-----------------|
| Brainstorm | Savollar beradi, dizayn taklif qiladi | Yangi loyiha boshlaganda |
| Write Plan | Reja yozadi, har bir task 2-5 daqiqalik | Dizayn tasdiqlanganda |
| Execute Plan | Rejani task bo'yicha bajaradi | Reja tayyor bo'lganda |
| TDD | Test yozadi, keyin kod yozadi | Har bir yangi funksiya uchun |
| Debugging | 4 bosqichli xato qidirish | Xato topilganda |
| Code Review | Kodni tekshiradi, fikr bildiradi | Merge oldidan |

Men eng ko'p brainstorm va execute plan ishlataman. Chunki men muammoni tushuntiraman, agent reja qiladi va bajaradi.

## O'rnatish

O'rnatish 1 daqiqa. Claude Code terminalni oching:

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

Tamom. Keyingi safar Claude Code ni ishlatganingizda u boshqacha ishlaydi. Avval savol beradi, keyin reja tuzadi, keyin yozadi.

## Nima yoqdi, nima yoqmadi

**Yoqdi:**
- Eng katta farq: agent avval o'ylaydi, keyin yozadi. Oldin teskari edi.
- Kod sifati sezilarli oshdi, chunki TDD majburiy qilinadi. Test yozmay turib kod yozolmaydi.
- Agar bir nechta mustaqil task bo'lsa, subagentlar parallel ishlaydi. Vaqt tejaydi.
- Plugin o'zi 2000 tokendan kam. Context window ni deyarli iste'mol qilmaydi.

**Yoqmadi:**
- Ba'zan ortiqcha savol beradi. "Bitta qator o'zgartir" desam ham 5 bosqichli plan tuzmoqchi bo'ladi.
- 10 dan kam taskli kichik ishlar uchun og'ir. Oddiy Claude Code tezroq.

Menimcha, 10+ taskli katta loyihalar uchun juda yaxshi. Kichik tuzatishlar uchun oddiy Claude Code yetarli.

## Nima o'zgardi

Bir oy oldin men Claude Code ga har bir qadamni aytardim. "Bu faylni o'qi. Bu funksiyani o'zgartir. Bu testni yoz." Hozir men faqat muammoni aytaman. Agent o'zi qadamlarni aniqlaydi, reja tuzadi, bajaradi.

Mana shu blogning o'zi ham superpowers pipeline dan o'tdi. Research, qoralama, 4 ta critic tekshiruvi, deploy. Men faqat natijani tekshirdim va tuzatdim.

GitHub da 52,000 yulduz. Men ham shu pluginni har kuni ishlataman.
