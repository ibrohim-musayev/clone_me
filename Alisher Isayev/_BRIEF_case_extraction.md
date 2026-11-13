# Vazifa: "Biznes Razbor" videosini to'liq tahlil qilish (Alisher Isaev "miyasi" uchun)

## Kontekst
Biz Alisher Isaevning (o'zbek tadbirkori, biznes-mentor, "Biznes Razbor", "Biznes Davolash", "Full Contact" loyihalari muallifi)
YouTube'dagi "Biznes razborlar to'plami" pleylistidagi 30 ta videoni to'liq ko'rib chiqib, uning **fikrlash tizimini**
("miyasi"ni) qayta tiklayapmiz: u qanday savol beradi, muammoni qanday diagnostika qiladi, qaysi qoida/freymvorklarga
tayanadi, qanday gapiradi, nimaga ishonadi. Natijada AI-maslahatchi yaratiladi, u Alisher uslubida tadbirkorlarga razbor qiladi.

Bu bosqichda sizning ishingiz: berilgan har bir video transkriptini **BOSHIDAN OXIRIGACHA, HAR BIR QATORINI** o'qib,
batafsil tahlil fayllarini yozish. Bu xulosa emas — bu "miya" uchun xom ashyo. Hech narsani tashlab ketmang:
har bir freymvork, qoida, savol, misol, raqam, metafora, hazil, iboralar muhim.

## Manbalar
- Transkriptlar: `./sources/transcripts/NN_<id>.txt` — YouTube avto-subtitrlari (o'zbekcha), `[MM:SS]` vaqt belgilari bilan,
  `>>` — gapiruvchi almashgani belgisi. **Avto-subtitr xatolari ko'p** (so'zlar noto'g'ri eshitilgan, ruscha so'zlar buzilgan).
  Kontekstdan aniq bo'lgan xatolarni tuzating (masalan "CEU" → "CEO", "shustriy" → "shustriy/chaqqon"), lekin hech narsani o'ylab topmang.
  Noaniq joylarni `(?)` bilan belgilang.
- Ba'zi transkriptlar uzstt (oflayn STT) orqali olingan: `./sources/transcripts/NN_<id>.txt` formatida, ichida
  `SPEAKER_00` kabi gapiruvchi belgilari bo'lishi mumkin (diarizatsiya avtomatik, xato bo'lishi mumkin).
- Video metama'lumotlari (sarlavha, sana, tavsif): `./sources/meta/NN_<id>.txt`
- Fayl katta bo'lsa Read tool'ni offset/limit bilan bo'lib-bo'lib o'qing — lekin **hammasini** o'qing.

## Gapiruvchilarni ajratish (juda muhim)
Videoda odatda: **Alisher Isaev** (ekspert, savol beradi, diagnostika qiladi), **mehmon tadbirkor(lar)** (muammosini aytadi),
ba'zan boshlovchi/moderator yoki boshqa ekspertlar, ba'zan zal tomoshabinlari. "Miya"ga faqat **Alisher**ning fikrlari kiradi.
Mehmon gaplari — kontekst. Boshqa ekspert fikri bo'lsa, alohida belgilang ("boshqa ekspert: ..."). Kim gapirayotgani noaniq bo'lsa, ayting.

## Har bir video uchun 2 ta fayl yozing

### 1) `./brain/cases/NN_<qisqa-slug>.md` — to'liq razbor-tahlil (o'zbek tilida, lotin yozuvida)
Bo'limlar (hammasi majburiy; ma'lumot bo'lmasa "—" yozing):

```
# NN. <Video sarlavhasi>
- URL: https://www.youtube.com/watch?v=<id>
- Sana / davomiylik:
- Mehmon(lar): ism, biznes, soha, shahar, biznes hajmi (aylanma, xodimlar soni, mijozlar, ... — videoda aytilgani)
- Boshqa ishtirokchilar:
- Mavzular (teglar): masalan #sotuv #HR #delegatsiya #eksport #restoran ...

## 1. Mehmonning so'rovi (u qanday muammo bilan keldi — o'z so'zlari bilan)
## 2. Diagnostika oqimi (ENG MUHIM QISM)
   Alisher qadamma-qadam qanday savollar berdi va har bir savol nimani ochdi. Xronologik tartibda, [vaqt] bilan.
   Format: `[MM:SS] Savol/harakat: "..." → Nima ochildi / nimaga bu savolni berdi (mantiq)`.
   Uning muammoni qanday qayta formulirovka qilgani ("asl muammo X emas, Y"), raqamlarga qanday aylantirgani,
   qanday qilib mehmonni o'zi javob topishga majburlagani — hammasini yozing.
## 3. Haqiqiy (ildiz) muammo — Alisher xulosasi
## 4. Yechim / harakat rejasi — aniq qadamlar, ketma-ketlik, muddatlar, KPI, "uy vazifasi", "jazo"/majburiyat, va'dalar
## 5. Freymvorklar, qoidalar, modellar
   Har biri: **Nomi** (Alisher qo'ygan nom bo'lsa o'sha, bo'lmasa siz qisqa nom bering) — mazmuni — qachon qo'llanadi — iqtibos [vaqt]
## 6. Raqamlar, benchmarklar, misollar (foizlar, summalar, muddatlar, nisbatlar — kontekst bilan)
## 7. Metaforalar, hikoyalar, hazillar, analogiyalar (iqtibos bilan)
## 8. Uslub va iboralar — Alisherning o'ziga xos so'zlari, tez-tez ishlatadigan iboralari, murojaat shakli, ritmi,
   ruscha/inglizcha so'zlar, intonatsiya (masalan "Qarang", "Zo'r", "Yashang", "To'xtang", "Tushuntira oldimmi?") — haqiqiy misollar bilan
## 9. E'tiqodlar, qadriyatlar, qarashlar (pul, xodim, oila, din, sog'liq, fokus, o'qish, risk...) — iqtibos bilan
## 10. Ogohlantirishlar / "hech qachon qilmang" lar
## 11. Alisher o'zi haqida aytganlari (bizneslari, tajribasi, maslahatchilari, odatlari, raqamlar) — faqat videoda aytilgani
## 12. Boshqa ishtirokchilar fikrlari (Alisherdan farqli bo'lsa)
## 13. Reklama/CTA (Full Contact, Biznes Davolash va h.k.) — 1-2 qator
## 14. Namunaviy dialoglar (few-shot uchun): 4–10 ta juftlik
   "Tadbirkor: ..." / "Alisher: ..." — originalga yaqin, lekin tozalangan o'zbek tilida; uning savol bilan javob berish uslubini saqlang.
## 15. Bu videodan "miya" uchun eng muhim 10 ta saboq (qisqa punktlar)
```

### 2) `./brain/extracts/NN.json` — mashina o'qiydigan ekstrakt (UTF-8, to'g'ri JSON)
```json
{
  "video": "NN", "id": "<youtube id>", "title": "...", "industry": "...", "guest_business": "...",
  "topics": ["..."],
  "frameworks": [{"name": "...", "description": "...", "when_to_use": "...", "quote": "...", "ts": "MM:SS"}],
  "principles": [{"text": "...", "quote": "...", "ts": "MM:SS", "theme": "hiring|sales|finance|strategy|focus|leadership|marketing|operations|mindset|personal|..."}],
  "diagnostic_questions": [{"question": "...", "purpose": "...", "ts": "MM:SS"}],
  "recommendations": [{"problem": "...", "advice": "...", "ts": "MM:SS"}],
  "numbers": [{"value": "...", "context": "...", "ts": "MM:SS"}],
  "metaphors": [{"text": "...", "meaning": "...", "ts": "MM:SS"}],
  "phrases": [{"phrase": "...", "usage": "..."}],
  "beliefs": [{"topic": "...", "belief": "...", "quote": "...", "ts": "MM:SS"}],
  "warnings": [{"text": "...", "ts": "MM:SS"}],
  "personal_facts": [{"fact": "...", "ts": "MM:SS"}],
  "qa_pairs": [{"entrepreneur": "...", "alisher": "..."}]
}
```
Iqtiboslar o'zbek tilida, Alisherning so'zlariga iloji boricha yaqin (avto-subtitr xatolari tuzatilgan holda).

## Sifat talablari
- To'liqlik: video davomidagi barcha muhim lahzalar qamrab olinsin (boshi, o'rtasi, oxiri). Tahlil oxirgi daqiqalarni ham qamrasin.
- Aniqlik: faqat transkriptda bor narsa. Taxmin bo'lsa — "(taxmin)" deb belgilang.
- Hajm: har bir case .md fayli odatda 1500–4000 so'z. Qisqartirmang.
- Hech qanday shaxsiy ma'lumotni (telefon raqamlar) case fayllarga ko'chirmang; mehmon ismi va biznesi — mayli.
- Ishni tugatgach, javobingizda faqat: yozilgan fayllar ro'yxati + har bir video bo'yicha 3–5 qatorli eng muhim topilmalar
  + transkript sifati bo'yicha muammolar (agar bo'lsa). Uzun javob qaytarmang — hamma narsa fayllarda bo'lsin.
