Read in English: [README.md](README.md)

# Kantor Virtual — Muse AI

Template kantor virtual yang dijalankan oleh **Muse** — manajer kantor AI Anda. Tujuh meja, satu papan tugas, dan pustaka 26 skill manajer. Pakai untuk menjalankan pekerjaan Anda seperti sebuah kantor: tugas masuk sebagai surat, meja-meja mengerjakannya, dan hasil kerja kembali ke Anda untuk disetujui.

> **Jujur dulu:** kantor yang live berjalan di dalam Muse sebagai aplikasi fullstack, dan tidak bisa dibagikan lewat tautan publik (datanya terikat akun pemiliknya). Repo ini adalah versi template yang mandiri: aplikasi kantor di `office/` berjalan offline dari satu file HTML dan menyimpan datanya di `localStorage` peramban. Ini demo dan titik awal — bukan kantor live.

## Screenshot

![Denah 2D](docs/screenshots/denah-2d.png)
*Denah 2D animasi — avatar Anda plus lima rekan berjalan antar meja, meja rapat, dan pojok kopi; jam lokal berjalan.*

> **Demo satu pemain:** denah ini bermain seperti Gather.town untuk satu pemain — jalan dengan WASD, tombol panah, atau klik-di-lantai. Multiplayer live (orang lain berjalan bersama Anda secara real-time) butuh server dan di luar cakupan halaman statis ini.

![Papan tugas](docs/screenshots/papan-tugas.png)
*Papan tugas — Antre → Dikerjakan → Menunggu Pemilik → Selesai.*

![Panel Rekrut](docs/screenshots/panel-rekrut.png)
*Panel Rekrut — skill yang terpasang dan cara kerja perekrutan.*

## Tujuh meja (contoh — ganti namanya sesuai pekerjaan Anda)

| Meja | Lingkup |
|------|---------|
| 💰 **GRANTS** | Hibah & pendanaan |
| 🛡️ **COMPLIANCE** | Aturan & kepatuhan |
| 📚 **MENTORING** | Pendampingan & bimbingan |
| 🧑‍🏫 **TEACHING** | Pengajaran & kelas |
| 🔬 **RESEARCH** | Riset & bacaan |
| 🎬 **CONTENT** | Konten & media |
| 📊 **REVIEW** | Evaluasi & data |

Meja-meja di atas hanya contoh. Ganti nama, lingkup, atau tambah meja baru di `office/index.html` (`UNITS`) dan di `docs/brain.md`.

## Cara kerja papan tugas

Setiap pekerjaan masuk sebagai *surat tugas* dan bergerak melalui empat kolom:

**Antre → Dikerjakan → Menunggu Pemilik → Selesai**

- Prosesor kantor mengerjakan tugas berstatus **Dikerjakan**.
- Hasil kerja diantar ke chat utama pemilik dan tugas pindah ke **Menunggu Pemilik** — tidak pernah otomatis **Selesai**.
- **Hanya pemilik yang menandai Selesai.**

### Otonomi manajer (template, opt-in)

Otonomi mati secara default. Nyalakan hanya untuk jenis tugas yang Anda percaya, dan hanya setelah pemilik menyetujuinya:

- Tugas yang pemilik tulis sendiri dengan penanda `auto=true` dikerjakan otomatis, tanpa menekan "Mulai kerjakan".
- Otonomi hanya untuk pekerjaan internal: draf, dokumen, riset, persiapan.
- Apa pun yang butuh mengirim pesan/email, posting, membayar/berlangganan, generate video atau paket konten, atau menyentuh isi kasus sensitif dipindah ke **Menunggu Pemilik** dengan catatan kenapa butuh pemilik.
- Pengingat tenggat untuk tugas penting/mendesak: maks 1x per tugas per hari.
- Manajer boleh hire skill/agen **gratis** sendiri dan melaporkan tiap hire; hire berbayar tetap kandidat sampai pemilik menyetujui.

### Aturan keras — COMPLIANCE

Kantor **tidak pernah memproses isi kasus sensitif** (nama/inisial pihak, berita acara, rekomendasi, pemanggilan). Pekerjaan kasus hanya di obrolan kepatuhan khusus. Yang boleh dikerjakan di kantor: administrasi umum — daftar hadir, template, jadwal, penomoran surat.

## ⭐ Sorotan utama: 26 skill manajer

Fokus utama repo ini adalah **26 skill manajer** pilihan dari katalog [Awesome Muse Skills](https://github.com/aicodedecode/awesome-muse-skills) (MIT, 2.648 skill). Tiap skill disalin **verbatim** ke `skills/` beserta `SKILL.md`, `skill.yaml`, `INSTALL-NOTES.md`, dan `ATTRIBUTION.md`.

### Inti manajer (9)

| Skill | Fungsinya |
|-------|-----------|
| `agent-manager-skill` | Mengelola armada agen AI lokal — membuat, mengawasi, mengarahkan tugas, memantau progres, dan menutup pekerja dengan rapi. |
| `agent-management` | Mengelola armada agen AI lokal: siklus hidup, pemantauan, penugasan, dan kontrol sumber daya. |
| `agent-orchestration` | Mengorkestrasi agen saat berjalan — perutean tugas, penjadwalan, eksekusi paralel, penggabungan hasil. |
| `agent-messaging` | Mengoordinasi agen lewat pesan: mengirim, menerima, dan mengelola komunikasi antar agen. |
| `planning` | Merencanakan kerja agen multi-langkah: memecah tujuan, mengurutkan agen, menentukan serah terima, menangani kegagalan. |
| `memory-search` | Mencari memori agen: mengingat keputusan, fakta, dan konteks dari percakapan sebelumnya. |
| `docs-search` | Mencari dokumentasi secara efektif: mengindeks dokumen, mencari dengan tepat, dan mengutip sumber. |
| `skill-creator` | Merancang dan menulis skill agen berkualitas: penentuan lingkup, frontmatter, struktur, tinjauan keamanan. |
| `skill-curator` | Memeriksa dan mengimpor skill pihak ketiga dengan aman: clone read-only, validasi, pindai keamanan, hapus duplikat. |

### Operasional kantor (7)

| Skill | Fungsinya |
|-------|-----------|
| `daily-briefing` | Menyusun ritual briefing pagi: prioritas semalam, kalender hari ini, 3 fokus utama. |
| `task-manager` | Merancang sistem manajemen tugas pribadi yang benar-benar jalan: mencatat, mengklarifikasi, mengatur, meninjau. |
| `meeting-notes-ai` | Memakai AI untuk notulen rapat — ringkasan otomatis, ekstraksi action item. |
| `email-triage` | Mencapai dan mempertahankan inbox zero: alur triase, filter, template, batching. |
| `calendar-guardian` | Menjaga waktu Anda: time-blocking, waktu penyangga, audit kalender mingguan, melindungi fokus. |
| `scheduling-assistant` | Memperlancar penjadwalan — alur pemesanan, manajemen ketersediaan, pengingat. |
| `weekly-review` | Menjalankan tinjauan mingguan yang menjaga seluruh sistem tetap bisa dipercaya: mencatat, mengklarifikasi, check-in. |

### Dokumen (6)

| Skill | Fungsinya |
|-------|-----------|
| `document-parser` | Membangun ingestion dokumen yang tangguh — chunking, metadata, pipeline multi-format. |
| `docx-pro` | Otomasi dokumen Word — membuat, membuat template, dan membaca file .docx. |
| `pdf-pro` | Pekerjaan PDF secara programatik — membuat, membaca, menggabung, dan mengisi PDF. |
| `presentation-designer` | Merancang deck presentasi yang menarik dengan struktur narasi dan kejelasan visual. |
| `forms-pro` | Membuat formulir web yang baik: pola UX, validasi, aksesibilitas, alur multi-langkah. |
| `survey-designer` | Merancang survei yang efektif — penulisan pertanyaan, skala jawaban, sampling, pengurangan bias. |

### Riset & sitasi (1)

| Skill | Fungsinya |
|-------|-----------|
| `citation-manager` | Mengelola sitasi dan referensi — mengumpulkan sumber, mengatur pustaka, memformat bibliografi. |

### Konten (3)

| Skill | Fungsinya |
|-------|-----------|
| `content-strategist` | Merancang strategi konten — riset audiens, topik pilar, kalender editorial. |
| `social-media-manager` | Merencanakan, membuat, dan mengelola kehadiran media sosial — kalender, strategi, engagement. |
| `newsletter-pro` | Menjalankan buletin profesional — strategi konten, penulisan, pertumbuhan, deliverability. |

Detail, pengelompokan, pemetaan ke meja, dan apa yang sengaja *tidak* dipasang: lihat [skills/INSTALL-NOTES.md](skills/INSTALL-NOTES.md).

## Cara memakai di Muse

1. **Clone atau unduh repo ini** (atau salin folder `skills/` dan `docs/brain.md`).
2. **Salin skill yang Anda butuhkan** ke folder custom-skills Muse, `~/workspace/custom-skills/` — tiap skill sebagai foldernya sendiri (`agent-manager-skill/`, `task-manager/`, …). Ambil yang dibutuhkan saja; tidak harus 26-nya.
3. **Salin `docs/brain.md`** ke workspace Anda sebagai otak kantor, dan **isi semua `[BRACKET]`** dengan meja, nama, jam, dan aturan Anda sendiri.
4. **Buka `office/index.html` di peramban** — tanpa build step, tanpa server. Tugas Anda tersimpan di `localStorage` peramban itu.
5. **Minta Muse jadi manajer kantor Anda** mengikuti file brain: mengarahkan tugas ke meja yang tepat, mengerjakannya, mengantar hasil ke chat utama Anda, dan memindah tugas yang selesai ke "Menunggu Pemilik".
6. **Sesuaikan dengan Anda:** edit `UNITS` dan `SEED_TASKS` di `office/index.html` (nama meja, lingkup, contoh tugas) dan bagian per meja di `docs/brain.md`.
7. **Hire skill baru saat ada tugas yang butuh:** cari di katalog [Awesome Muse Skills](https://github.com/aicodedecode/awesome-muse-skills), lalu pasang dengan `skill-curator` / `skill-creator` (clone read-only, validasi frontmatter, pindai keamanan, jangan pernah menjalankan kode atau installer dari repo asal, hapus duplikat berdasarkan isi). Hire gratis langsung aktif dan dilaporkan; hire berbayar menunggu persetujuan Anda.

## Cara memakai tanpa Muse

Papannya jalan sendiri: buka `office/index.html` di peramban apa pun. Seret kartu tugas antar kolom, atau pakai menu pindah di tiap kartu (ramah sentuhan). Tombol "Reset example tasks" mengembalikan 7 tugas contoh. Tanpa akun, tanpa server, tanpa data yang keluar dari peramban Anda.

## Kustomisasi

- **Meja:** edit array `UNITS` di `office/index.html` (id, nama, peran, emoji, warna) dan bagian yang cocok di `docs/brain.md`.
- **Tugas contoh:** edit `SEED_TASKS` di `office/index.html`. Ganti contohnya dengan tugas Anda yang sebenarnya, atau kosongkan dan mulai dari nol.
- **Status:** empat kolomnya adalah `Backlog`, `In progress`, `Waiting for owner`, `Done` (`STATUSES` di file). Ganti namanya bila alur kerja Anda memakai kata lain.
- **Skill:** tambah atau hapus folder di bawah `skills/` dan perbarui daftar `SKILL_GROUPS` di `office/index.html` supaya panel Rekrut cocok.
- **Aturan:** semua yang diikuti kantor ada di `docs/brain.md` — edit dulu file itu, kantor mengikuti apa yang tertulis di sana.

## Struktur repo

```
.
├── README.md                  # Versi Bahasa Inggris
├── README.id.md               # File ini (Bahasa Indonesia)
├── LICENSE                    # MIT
├── office/
│   └── index.html             # Aplikasi kantor mandiri (satu file, offline)
├── skills/
│   ├── INSTALL-NOTES.md       # 26 skill: kelompok, pemetaan meja, yang dilewati
│   └── <26 folder skill>/     # Salinan verbatim: SKILL.md + skill.yaml + catatan
└── docs/
    ├── brain.md               # Template otak kantor: aturan per meja, otonomi, perekrutan
    └── screenshots/           # Denah 2D, papan tugas, panel Rekrut
```

## Aturan yang mengatur kantor ini

Aturan lengkap ada di [docs/brain.md](docs/brain.md). Versi singkatnya:

- Bekerja dalam bahasa pemilik; sapa pemilik sesuai yang disepakati di file brain.
- Jangan kirim pesan/email atas nama pemilik tanpa persetujuannya — draf dulu, pemilik yang menyetujui.
- Jangan mengarang data, angka, sitasi, atau nama. Kalau belum terverifikasi, tulis begitu.
- Hormati jam tenang pemilik: jangan jadwalkan pekerjaan di jam itu.
- Tugas tidak pernah auto-Selesai — hanya pemilik yang menandai Selesai.
- Hire gratis langsung aktif dan dilaporkan; hire berbayar menunggu persetujuan.

## Lisensi & atribusi

MIT — lihat [LICENSE](LICENSE). Skill-skill di `skills/` berlisensi MIT dari kontributor [Awesome Muse Skills](https://github.com/aicodedecode/awesome-muse-skills); tiap folder menyimpan `ATTRIBUTION.md`-nya sendiri.
