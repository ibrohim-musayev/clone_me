# Vazifa: Alisher Isaev "miyasi" — sintez bosqichi

## Kontekst
30 ta "Biznes Razbor" videosi (≈25 soat) to'liq tahlil qilindi. Har bir video uchun:
- `./brain/cases/NN_*.md` — batafsil razbor-tahlil (diagnostika oqimi, freymvorklar, iqtiboslar, vaqt belgilari);
- `./brain/extracts/NN.json` — strukturalangan ekstrakt;
- `./brain/_merged/<kalit>.md` — barcha videolar bo'yicha avtomatik birlashtirilgan ro'yxatlar
  (frameworks, principles, diagnostic_questions, recommendations, numbers, metaphors, phrases, beliefs, warnings,
  personal_facts, qa_pairs) va `_index.md` (videolar indeksi: NN, sarlavha, soha, mavzular).

Endi bu xom ashyodan **AI-Alisher "miyasi"ni** yig'amiz — bu fayllar AI-maslahatchiga bilim bazasi va tizim prompti bo'ladi.
U tadbirkorlarga Alisher uslubida razbor qiladi: savol beradi, raqamga aylantiradi, ildiz muammoni topadi, qadamlar beradi.

## Umumiy qoidalar (barcha sintez fayllari uchun)
1. **Til**: o'zbek (lotin). Alisherning ruscha/inglizcha biznes atamalari (zapros, CAC, LTV, KPI, operatsionka...) saqlansin.
2. **Takrorlarni birlashtiring**: bir xil g'oya bir necha videoda uchrasa — bitta yozuv, lekin barcha manbalar ko'rsatilsin.
   Ko'p videoda takrorlangan g'oya = yadro e'tiqod; buni "chastota" bilan belgilang (masalan `[5 video]`).
3. **Manba havolalari**: har bir freymvork/qoida/da'vo yonida `[NN mm:ss]` (video raqami — fayl prefiksi, vaqt).
4. **Faqat Alisherniki**: mehmonlar, boshqa ekspertlar, AI-yordamchi yoki reklama roliklari gaplari Alisherga yozilmasin.
   Montaj qo'yilmalari (teaser, "tizim — futbolchiga butsi" klipi, Full Contact/Biznes Davolash reklamasi, otzivlar) takroriy —
   ularni bir marta, "reklama/montaj" deb belgilang yoki tashlab keting.
5. **Noaniqlik**: avto-subtitr xatosi sababli noaniq raqam/nomlar `(?)` bilan qolsin, o'ylab topilmasin.
   Ziddiyatli fikrlar topilsa — ikkalasini ham manbasi bilan yozing va kontekst farqini tushuntiring.
6. **Amaliylik**: har bir qoida AI uni qo'llay oladigan shaklda bo'lsin — "qachon qo'llanadi", "qanday savol bilan boshlanadi",
   "nima tavsiya qilinadi", "qanday xatodan saqlaydi".
7. **Hajm**: qisqartirmang, lekin takrorlamang. Sifat > hajm. Har bir chiqish fayli boshida 10–20 qatorli "Eng muhimi" bloki bo'lsin.
8. Faqat o'zingizga biriktirilgan chiqish fayl(lar)ini yozing. Boshqa fayllarni o'zgartirmang.
9. Ish tugagach javobingiz qisqa bo'lsin: yozilgan fayllar, hajmi (so'z), asosiy tuzilma, topilgan ziddiyat/bo'shliqlar.
