# Proses Penerbitan Dokumen

Ringkas. Penjelasan lengkap alur kerja ada di
[`pokja1-handbook/docs/02-alur-kerja.md`](https://github.com/idtc-id/pokja1-handbook/blob/main/docs/02-alur-kerja.md).

## Alur singkat

```
Usulan topik          → issue di pokja1-handbook
      ↓
Kajian awal           → ringkasan standar yang sudah ada
      ↓
Kelompok penyusun     → 3 unsur: pemerintah, industri, akademisi
      ↓
Draf 0.x              → PR ke repo ini, status "Draf"
      ↓
Tinjauan internal     → review 3 unsur
      ↓
Tinjauan publik       → Discussions, minimal 3 minggu
      ↓
Uji penerapan         → dipakai minimal 1 pilot Pokja 2
      ↓
Versi 1.0 "Berlaku"   → rilis (GitHub Release) + tabel di README diperbarui
```

## Membuat dokumen baru

1. Pastikan topik sudah disetujui lewat issue di `pokja1-handbook`.
2. Buat branch `dokumen/<kode>-<slug>`, misalnya `dokumen/DT-S-01-glosarium`.
3. Salin folder template yang sesuai dari [`template/`](template/).
4. Buat folder `standar/DT-S-01-glosarium/` (atau `panduan/`, `policy-brief/`).
5. Isi `README.md` di folder tersebut sebagai naskah utama.
6. Buka Pull Request berlabel `dokumentasi`.

## Aturan Pull Request

- Satu PR untuk satu dokumen. Jangan menggabung beberapa dokumen dalam satu PR.
- PR draf awal cukup disetujui **koordinator dokumen**.
- PR yang mengubah **ketentuan** pada dokumen berstatus *Berlaku* butuh persetujuan
  **minimal 2 peninjau dari unsur berbeda** + Ketua Pokja.
- Perbaikan redaksi (typo, tautan rusak) cukup 1 approval.

## Tinjauan publik

Saat dokumen masuk tinjauan publik:

1. Ubah status di halaman pertama menjadi **Tinjauan publik** dengan tanggal mulai dan berakhir.
2. Buka Discussion baru berjudul `[Tinjauan Publik] <kode> — <judul>`.
3. Umumkan lewat kanal IDTC dan situs komunitas.
4. Setiap masukan **dijawab tertulis** — diterima, ditolak beserta alasannya, atau ditunda.
5. Rekap masukan disimpan sebagai `lampiran-tinjauan-publik.md` di folder dokumen.

## Rilis versi

Setiap versi yang ditetapkan dibuat sebagai **GitHub Release**:

- Tag: `<kode>-v<versi>`, misalnya `DT-S-01-v1.0`.
- Judul: `<Kode> <Judul> versi <x.y>`.
- Catatan rilis: ringkasan perubahan dan tanggal berlaku.

Setelah rilis, perbarui tabel daftar dokumen di [README.md](README.md).

## Penomoran versi

| Perubahan | Contoh | Versi |
|---|---|---|
| Perbaikan redaksi, contoh tambahan, klarifikasi | Memperjelas definisi | 1.0 → 1.1 |
| Perubahan ketentuan yang membuat penerapan lama tidak sesuai | Mengubah skema wajib | 1.1 → 2.0 |

## Menarik dokumen

Dokumen **tidak dihapus**. Untuk menarik:

1. Ubah status menjadi **Ditarik**.
2. Tambahkan bagian *Alasan penarikan* dan, bila ada, penggantinya.
3. Biarkan file tetap di tempatnya supaya tautan lama tidak putus.
