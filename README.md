# Pertemuan 04 - Seleksi Multi-Kondisi dan Validasi Input

## Identitas

**Nama:** Arya Kusmana Anas
**NIM:** 2225250118
**Kelas:** 3 B 
**Mata Kuliah:** Algoritma dan Pemrograman  
**Program Studi:** S1 Pendidikan Matematika FKIP Untirta  

---

## Tujuan

Membangun program validasi dan klasifikasi dengan menggunakan struktur
`if-elif-else`.

Pada pertemuan ini dipelajari:
- Seleksi multi-kondisi dengan `if-elif-else`
- Klasifikasi berdasarkan rentang nilai
- Validasi tipe data
- Validasi rentang nilai
- Validasi domain
- Penggunaan `try-except ValueError`
- Penyusunan tabel keputusan dan test case

---

## Cara Menjalankan
python3 praktik/validasi_klasifikasi_nilai.py
Pastikan Python sudah terinstall.

## Tabel Keputusan Praktik 1
Kondisi	Syarat	Keluaran
Tipe input	Semua input berupa angka	Proses dilanjutkan
Nilai ujian	0 ≤ ujian ≤ 100	Proses dilanjutkan
Nilai tugas	0 ≤ tugas ≤ 100	Proses dilanjutkan
Kehadiran	0 ≤ hadir ≤ 100	Proses dilanjutkan
Kehadiran rendah	hadir < 80	Tidak memenuhi syarat kehadiran
Predikat A	nilai akhir ≥ 85	A
Predikat B	nilai akhir ≥ 70	B
Predikat C	nilai akhir ≥ 60	C
Predikat D	nilai akhir ≥ 50	D
Predikat E	selain kondisi di atas	E


## Tabel pengujian
Hasil Pengujian
No	| Ujian |  Tugas |	Kehadiran |	Nilai Akhir | Keluaran Diharapkan |	Keluaran Aktual	Status |
1 | 90 | 80 | 95 | 86.00	| Predikat A, Lulus		
2 |	75 | 70	| 85 | 73.00	| Predikat B, Lulus		
3 |	60 | 60	| 80 | 60.00	| Predikat C, Lulus		
4 |	55 | 50	| 90 | 53.00	| Predikat D, Belum lulus		
5 | 40 | 30	| 100| 36.00	| Predikat E, Belum lulus		
6 | 50 | 90	| 75 | 90.00	| Tidak memenuhi syarat kehadiran		
7 | 105| 80	| 90 | -	    | Penolakan rentang nilai ujian		
8 | 80 | -5	| 90 | -	    | Penolakan rentang nilai tugas		
9 | 80 | 80	| abc| -	    | Penolakan tipe input

## Refleksi
Salah satu input tidak valid yang perlu diperhatikan adalah input berupa teks ketika program mengharapkan angka.

Contohnya:

abc

Input tersebut dapat menyebabkan ValueError ketika dikonversi menggunakan float() atau int(). Oleh karena itu, digunakan try-except ValueError agar program dapat memberikan pesan penolakan yang sesuai.

## Kesimpulan
Pada Pertemuan 04 dipelajari penggunaan seleksi multi-kondisi dengan
if-elif-else serta validasi input.

Validasi dilakukan sebelum klasifikasi agar program hanya memproses data yang
valid. Pengujian dilakukan menggunakan berbagai test case, termasuk nilai
batas, nilai di luar rentang, dan input yang bukan angka.