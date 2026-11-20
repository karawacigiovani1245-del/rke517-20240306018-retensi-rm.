# Mini-PRD: RetensiRM Mampang (one page)

**User and setting:** Petugas rekam medis di ruang rekam medis Puskesmas Mampang Prapatan.
**The routine today:** <3–4 lines: how it works on paper / in WhatsApp now.>
**The routine today:** Petugas rekam medis mendata berkas yang masuk tahap retensi ke dalam catatan/daftar berkas di ruang rekam medis. Karena pendataan dan pengecekan dilakukan secara bertahap dengan perangkat terbatas, pemantauan berkas yang sudah waktunya diretensi berjalan lebih lambat.
Photo of an EMPTY form, or one with every name and number covered: `docs/form_photo.jpg`

**The problem:** Petugas rekam medis di Puskesmas Mampang Prapatan memproses retensi berkas lebih lambat karena pendataan berkas yang masuk tahap retensi hanya mengandalkan satu komputer bersama tanpa pencatatan daftar retensi yang terstruktur, sehingga status berkas yang harus diretensi berisiko tertunda.

**The user's routine (answer from what you saw):**
- What does the user look for most? Status retensi berkas dan berkas yang sudah jatuh tempo/siap diretensi.
- What do they write every time? Nomor rekam medis (fiktif), tanggal kunjungan terakhir, tanggal jatuh tempo retensi, dan status retensi.
- What goes wrong now? Pencatatan dan pelacakan status retensi berjalan lambat serta berisiko tertunda.
- What do they count at the end of the month? Rekap jumlah berkas yang diretensi dan daftar berkas yang jatuh tempo/terlambat diretensi pada bulan tersebut.

**The user (one role):** Petugas rekam medis, mencatat dan memperbarui status retensi berkas rekam medis serta memeriksa rekap bulanan secara rutin pada jam kerja/jadwal retensi.

## In v1.0 (3–5 user stories)
- US-1: As a medical records officer, I want to record a medical record's retention entry with fictional data so that its retention status is tracked in one place.
- US-2: As a medical records officer, I want to search and update a record's retention status so that I can quickly see what is waiting, ready, or completed.
- US-3: As a medical records officer, I want to view a monthly retention summary and due/overdue list so that I know what to process this month.

## Out of scope (at least 3)
- Pemindaian (scanning) dokumen fisik maupun pengubahan tata ruang rak filing atau pembelian perangkat keras.
- Integrasi langsung ke sistem rekam medis nasional atau pencatatan lintas unit lain (seperti pendaftaran atau farmasi).
- Pengelolaan hak akses multi-pengguna atau fitur lanjutan di luar pencatatan dan rekap status retensi.

## Data list
| Field | Type | Required? | Rule |
|---|---|---|---|
| No. RM (fiktif) | text | required | format kode fiktif unik, tidak boleh kosong |
| Tanggal Kunjungan Terakhir | date | required | tidak boleh di masa depan |
| Tanggal Jatuh Tempo Retensi | date | required | tidak boleh lebih awal dari Tanggal Kunjungan Terakhir |
| Status Retensi | choice | required | salah satu dari: Menunggu, Siap Retensi, Selesai Retensi |

## Checks for v1.0 (Situation → Action → Result)
- C-1: Situation: fictional record RM-0001 with last visit 2020-01-10, due date 2025-01-10, status Siap Retensi -> Action: save entry and reload page -> Result: record stays saved with all fields intact.
- C-2: Situation: due date is entered earlier than last visit date -> Action: attempt to save entry -> Result: save is blocked with a clear validation message.
- C-3: Situation: 10 fictional test records exist and 3 have status Siap Retensi this month -> Action: open monthly retention report -> Result: exactly those 3 records appear in the summary/list.

**How I will know it helped:** Petugas dapat mengecek status retensi berkas dan menyusun rekap bulanan lebih cepat dan terstruktur dibandingkan menelusuri catatan secara manual satu per satu.
