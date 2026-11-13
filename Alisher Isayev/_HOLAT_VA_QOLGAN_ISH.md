# Holat — 2026-11-13 (YANGILANDI): sintez 30/30 videoga yangilandi

- Barcha sintez fayllari (01–08, `04_mavzular/` 9 ta playbook) endi 30 video (01–30) asosida.
- Usul: qayta yozish o'rniga qo'shimcha bandlar (`adds`) birlashtirildi; asl mazmun tekshirilgan (hech bir asl qator yo'qolmagan).
- Sarlavha qatorlaridagi "21 video" hisobi yangilandi. Bo'lim ichidagi ba'zi "21 videoda" izohlari eski holatda qolgan.
- `SYSTEM_PROMPT.md` va `README.md` yangilanmagan (README'dagi "21 video" jumlalari qolgan).

---

# Holat — 2026-11-12, 20:00 (keyingi hafta shu yerdan davom etiladi)

## Tayyor
- **30/30 video to'liq tahlil qilingan:** `cases/` (≈172 ming so'z) + `extracts/*.json`. `_merged/` 30 video bo'yicha yangilangan.
- Barcha transkriptlar `../sources/transcripts/` da (21 ta YouTube subtitri, 9 ta uzstt).
- `SYSTEM_PROMPT.md` — 30 video bo'yicha yangilangan (33 ta tamoyil, jumladan 20–30-videolardan yangi qoidalar 28–33).
- `README.md` — tayyor.

## Qolgan ish: sintez fayllarini 30 videoga yangilash
Hozir quyidagi fayllar **21 video** (01–19, 26, 27) asosida yozilgan. Ularga 20, 21, 22, 23, 24, 25, 28, 29, 30-videolarni qo'shish kerak.
Har bir fayl boshida "yangilash qoidasi" bor.
- `01_shaxs_va_qadriyatlar.md`, `07_raqamlar_benchmarklar.md`
- `02_razbor_algoritmi.md`
- `03_freymvorklar.md`
- `04_mavzular/` — 9 ta playbook. ⚠️ `sotuv_va_b2b.md` yangilash jarayonida to'xtatilgan, qisman yangilangan bo'lishi mumkin: tekshirib, oxiriga yetkazish kerak.
- `05_sohalar_va_keyslar.md`
- `06_ovoz_va_uslub.md`, `08_dialog_namunalari.md`

Har bir fayl uchun yangilashda o'qiladigan manbalar:
- 9 ta yangi ekstrakt: `extracts/20.json` … `30.json`;
- tegishli case bo'limlari.

## Agar tokenni tejash kerak bo'lsa
Faqat `03_freymvorklar.md` va `02_razbor_algoritmi.md`ni yangilash yetarli.
SYSTEM_PROMPT allaqachon 30 videoni qamragan, case fayllar to'liq.
