# AI-Alisher — Alisher Isaev "miyasi"

Alisher Isaevning YouTube'dagi **"Biznes razborlar to'plami"** pleylistidagi videolar asosida qurilgan bilim bazasi va tizim prompti.
Maqsad: tadbirkorlarga Alisher uslubida **razbor** qiladigan AI-maslahatchi. U savol beradi, raqamga aylantiradi, biznesni bo'laklarga bo'ladi, ildiz muammoni topadi, qadamlar beradi va majburiyat oladi.

> ⚠️ Bu — Alisher Isaevning ochiq videolari asosidagi **AI modeli**, uning o'zi emas. AI o'zini shunday tanishtiradi va yangi "esdaliklar" to'qimaydi.

## Qanday ishlatish

**Claude Projects / ChatGPT Custom GPT / Gemini Gem:**
1. `SYSTEM_PROMPT.md` matnini to'liq "Instructions / System prompt" maydoniga qo'ying.
2. Quyidagi fayllarni "Knowledge / Project files"ga yuklang: `01_…` – `08_…` va `04_mavzular/` ichidagi fayllar (eng muhimlari). Joy bo'lsa — `cases/` papkasini ham.
3. Birinchi xabar: biznesingiz, raqamlaringiz va bitta zaprosingiz.

**API orqali:** `SYSTEM_PROMPT.md` — system prompt. Qolgan fayllar RAG uchun manba (har bir fayl `##` bo'limlarga bo'lingan, yozuvlarda `[NN mm:ss]` manba havolasi bor). `extracts/*.json` — strukturalangan ma'lumot (freymvorklar, savollar, raqamlar, iboralar, Q&A juftliklari).

## Fayllar xaritasi

| Fayl | Nima bor |
|---|---|
| `SYSTEM_PROMPT.md` | Yadro: kimligi, 33 ta tamoyil, 10 qadamli razbor sikli, "agar → unda" qoidalari, uslub, chegaralar |
| `01_shaxs_va_qadriyatlar.md` | Kimligi (faqat videolarda aytilgani), loyihalari, odatlari, dunyoqarashi, chegaralari |
| `02_razbor_algoritmi.md` | Razbor metodi: 9 faza, 35+ diagnostika texnikasi, savollar banki, 58+ qaror qoidasi |
| `03_freymvorklar.md` | 160+ qoida va freymvork (ID'lar bilan), "hech qachon" ro'yxati, ziddiyatlar va ularning sharti |
| `04_mavzular/` | 9 ta playbook: sotuv/B2B, marketing/kanal/brend, moliya/unit-ekonomika, strategiya/fokus, xodim/HR, delegatsiya/tizim/KPI, eksport/masshtab, investitsiya, tadbirkor mindseti |
| `05_sohalar_va_keyslar.md` | 30 ta razbor katalogi, soha playbooklari, "muammo → keys" indeksi |
| `06_ovoz_va_uslub.md` | Ohang, ritm, iboralar (chastota bilan), ruscha atamalar, metaforalar kutubxonasi, chat uchun uslub qoidalari |
| `07_raqamlar_benchmarklar.md` | Formulalar (savdo = trafik × konversiya × chek, CAC, LTV, NPS...), benchmarklar, keyslardagi real raqamlar |
| `08_dialog_namunalari.md` | 100 ta real dialog (few-shot uchun), mavzular bo'yicha |
| `cases/NN_*.md` | Har bir videoning to'liq tahlili: diagnostika oqimi [vaqt bilan], freymvorklar, iqtiboslar, namunaviy dialoglar |
| `extracts/NN.json` | Har video bo'yicha mashina o'qiydigan ekstrakt |
| `_merged/` | Ekstraktlarning avtomatik birlashmasi (mavzu bo'yicha) |
| `_BRIEF_*.md` | Tahlil va sintez uchun yo'riqnomalar (qayta ishlash uchun) |

Manba materiallar: `../sources/` (transkriptlar, metama'lumotlar, STT natijalari), skriptlar: `../tools/`.

## Qanday qurildi

1. Pleylist: 31 ta video. **Biri yopiq (private)**, unga kirish imkoni yo'q. **30 ta video, ≈25 soat** tahlil qilindi.
2. Transkriptlar:
   - 21 ta video — YouTube'ning o'zbekcha avto-subtitrlari;
   - 9 ta videoda (20–25, 28–30) subtitr yo'q edi. Ular oflayn **uzstt** (rubaiSTT v2) bilan transkripsiya qilindi.
3. Har bir transkript boshidan oxirigacha o'qilib, batafsil tahlil (`cases/`) va strukturalangan ekstrakt (`extracts/`) yozildi.
4. Ekstraktlar birlashtirilib, mavzular bo'yicha sintez fayllari (01–08) yozildi. Takrorlar birlashtirildi, chastota (`[N video]`) va manba (`[NN mm:ss]`) saqlandi.

## Cheklovlar

- Avto-subtitr va STT xatolari sabab ba'zi nomlar va raqamlar noaniq. Ular `(?)` bilan belgilangan, AI ularni fakt deb aytmasligi kerak.
- Videolarda gapiruvchi belgisi ishonchsiz. Alisherga tegishliligi noaniq gaplar `(taxmin)` deb belgilangan.
- Montaj qo'yilmalari va reklamalar (Full Contact, Biznes Davolash, "tizim — butsi" klipi, otzivlar) razbor metodi sifatida hisoblanmagan.
- Videolarda kam yoritilgan mavzular: pul oqimi va moliyaviy hisobot, narxlash metodikasi, franshiza, yuridik va soliq masalalari, sotuv skriptlari, raqamli marketing taktikasi. AI bu mavzularda ehtiyotkor bo'lishi kerak.

## Manba videolar

| # | Sarlavha | Sana | Davomiylik | Havola |
|---|---|---|---|---|
| 01 | Tadbirkorning tezligi — biznesning eng katta muammosi? | 2026-11-02 | 42:22 | https://youtu.be/WMwtLZxRTMo |
| 02 | $100,000 dan $500,000 ga o‘tish: Katta mijozlar oldidagi qo‘rquvni qanday yengish kerak? | 2026-10-05 | 39:39 | https://youtu.be/eUBLJXOf3eI |
| 03 | Savdo tushib ketganida biznes qaysi raqamlar bilan qutqariladi? | 2026-09-07 | 48:45 | https://youtu.be/-ziyqAD_tso |
| 04 | Katta maosh oladigan xodimlar nega o‘sishdan to‘xtaydi? | 2026-08-17 | 40:58 | https://youtu.be/wpi73kWmiQM |
| 05 | Kelajakda kimlar bozorda qoladi? | 2026-07-20 | 22:10 | https://youtu.be/e_NzE2NyFCQ |
| 06 | Eksportga chiqishda asosiy to'siq nima? | 2026-06-29 | 35:47 | https://youtu.be/kf5ioZYsk9s |
| 07 | Ishlab chiqaruvchilarning million dollarlik xatosi | 2026-05-18 | 34:01 | https://youtu.be/rZkTZxoD83s |
| 08 | Raqobatchilar bilan kurashmang, ularning o‘zidan pul ishlang! | 2026-05-04 | 35:01 | https://youtu.be/ONi8fLoWTC0 |
| 09 | Dubay ko'chmas mulkiga hozir investitsiya qilish kerakmi? | 2026-04-27 | 22:43 | https://youtu.be/xShz3oasI9o |
| 10 | O‘quv markazlar kelajagi nima bo‘ladi? — “Razbor” 22-soni | 2026-03-30 | 51:51 | https://youtu.be/PDVW8qi5Gmk |
| 11 | Xizmat ko‘rsatish sohasida mijoz sonini 10x oshirish yo‘li — “Razbor” 21-soni | 2026-03-23 | 33:08 | https://youtu.be/7sy-2e9Wt1c |
| 12 | 62 daqiqada restoran biznesining sotuvini 5 000 000 000 so‘mga oshirishni o‘rganing | 2026-02-23 | 1:01:46 | https://youtu.be/t-AnVRGYHlE |
| 13 | Andijonda $70 000 000 lik loyiha — “Razbor” 19-soni | 2026-01-26 | 32:26 | https://youtu.be/qJapnjO1sNw |
| 14 | B2B sotuvdagi eng KATTA xatolar — “Razbor” 18-soni | 2026-01-09 | 52:33 | https://youtu.be/HQ3Rr1Verho |
| 15 | $1 000 000 000 lik kompaniyadan xodim yollash — “Razbor” 17-soni | 2025-12-29 | 38:32 | https://youtu.be/1rTZgWcF3GI |
| 16 | №1 fast-food restorani bo‘lish siri nimada? — “Razbor” 16-soni | 2025-11-21 | 30:10 | https://youtu.be/kpcpcpYhh4s |
| 17 | “Razbor” 15-soni — $41 000 000 lik bozor | 2025-11-04 | 28:44 | https://youtu.be/o6hzvmE4UdM |
| 18 | “Razbor” 14-soni — Xodim qidirmang, natija qidiring! | 2025-10-13 | 58:15 | https://youtu.be/HHK_0cmqVFE |
| 19 | “Razbor” 13-soni — Hech qachon bir vaqtda ikkita biznes qilmang! | 2025-09-29 | 28:27 | https://youtu.be/56WvvSulYmU |
| 20 | “Razbor” 12-soni — Eksportga chiqmoqchi bo'lgan tadbirkorlar ko‘rishi shart! | 2025-09-01 | 36:38 | https://youtu.be/5yWPPfkN2Fg |
| 21 | “Razbor” 11-soni — Xodimlar sonini oshirmasdan x10 kengayish | 2025-08-25 | 45:47 | https://youtu.be/n6nU1gxbE64 |
| 22 | $100 000 lik onlayn do'kon — "Razbor" 10-soni | 2025-08-11 | 1:06:12 | https://youtu.be/-KDQ7npk3uM |
| 23 | “Razbor” 9-soni — B2B yo'nalishida o‘sish nuqtasi — Tibbiyot sohasi | 2025-07-28 | 1:00:03 | https://youtu.be/7aY8s8JaZaU |
| 24 | “Razbor” 8-soni — Distributsiyaning kelajagi yo‘qmi? | 2025-07-21 | 33:12 | https://youtu.be/xEcqDBA7Fb0 |
| 25 | "Бизнес Разбор" 7 - soni — O'rta segmentdan yuqori segmentga o'tish yo'llari | 2025-07-04 | 48:27 | https://youtu.be/hofkkKx4oME |
| 26 | IT-kompaniya “разбор” — Qanday qilib biznesda “risk” va xarajatlarni kamaytirish? — Razbor 6-soni | 2025-04-26 | 54:42 | https://youtu.be/WXqWWlcYYp8 |
| 27 | Qanday qilib lokatsiya omilini yutish va lidlarni xaridorlarga aylantirish? — "Biznes Разбор" 5-soni | 2025-03-14 | 33:58 | https://youtu.be/_l2Vha-Hj00 |
| 28 | Xodim yollash, oliy maqsad, sodiq va kuchli jamoa qurish, HR — "Biznes Разбор" 4-soni | 2025-02-22 | 1:08:21 | https://youtu.be/Q0t378W3OHM |
| 29 | Logistika sohasidagi inqirozi — Xojakbar Gulyamov — "Biznes Разбор"  2-soni | 2024-06-28 | 1:02:03 | https://youtu.be/W8c5rJedMbs |
| 30 | Alisher Isaev bilan "Biznes Разбор" 1-soni | 2024-05-17 | 2:28:35 | https://youtu.be/Pi1r_VO2L4E |
| 31 | (yopiq video — kirish imkoni yo'q) | — | — | https://youtu.be/oX8OKykK6wY |
