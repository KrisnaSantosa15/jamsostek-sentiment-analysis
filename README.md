# Analisis Sentimen Aplikasi Jamsostek Mobile

![Jamsostek Mobile](https://play-lh.googleusercontent.com/ivLsnKV-iepAMvH3h71ViAKAA9hpYDE5TCV-1unGpeRbeyowlqYHLd64YIR6HbODvAKN=s48-rw)

## Latar Belakang

Jamsostek Mobile adalah aplikasi yang digunakan untuk memudahkan peserta Jamsostek dalam mengakses informasi BPJS. Aplikasi ini memiliki beberapa fitur, seperti cek saldo, cek iuran, klaim JHT, dan lain-lain. Dengan adanya aplikasi ini, peserta Jamsostek tidak perlu lagi datang ke kantor untuk mengecek informasi terkait program Jamsostek. Namun, tentu saja, aplikasi ini juga memiliki kekurangan dan kelebihan. Oleh karena itu, kita akan melakukan analisis sentimen terhadap aplikasi Jamsostek Mobile.

## Tujuan

Tujuan dari analisis ini adalah untuk mengetahui sentimen pengguna terhadap aplikasi Jamsostek Mobile. Dengan mengetahui sentimen pengguna, kita dapat mengetahui kelebihan dan kekurangan dari aplikasi ini. Dengan demikian, kita dapat menjadikan analisis ini sebagai bahan masukan untuk meningkatkan kualitas aplikasi Jamsostek Mobile atau aplikasi serupa di masa depan.

## Data

Data yang digunakan dalam analisis ini adalah data review aplikasi [Jamsostek Mobile (JMO)](https://play.google.com/store/apps/details?id=com.bpjstku) yang diambil dari Google Play Store. Data ini berisi review pengguna beserta rating yang diberikan oleh pengguna. Data ini diambil pada tanggal 17 Februari 2025 dengan total 108.000 review. Namun, agar dataset dataset seimbang, kita akan menggunakan teknik undersampling dengan library `imbalanced-learn` untuk membagi data berdasarkan jumlah minimum dari 3 kategori sentiment, yaitu positif, netral, dan negatif.

## Kualitas Data

Data yang digunakan dalam analisis ini adalah data review aplikasi Jamsostek Mobile yang diambil dari Google Play Store. Data ini memiliki 4 kolom, yaitu:
- `id`: ID review
- `content`: Isi review
- `score`: Rating yang diberikan oleh pengguna (1-5)
- `date`: Tanggal review
Dataset ini masih belum bersih, sehingga kita perlu mengolah data terlebih dahulu dengan melakukan beberapa tahapan, seperti menghapus baris data yang kosong, menghapus data duplikat, labeling dan lain-lain.

## Metode Labeling

Metode labelling yang digunakan dalam proyek analisis sentimen ini adalah dengan menggunakan lexicon-based. Lexicon-based adalah metode yang menggunakan kamus kata-kata yang sudah diberi label sentimen (positif, netral, negatif). Di mana sentimen teks ditentukan dengan mencocokkan kata-kata dalam teks dengan dua kamus lexicon (positif dan negatif) yang sudah memiliki skor sentimen. Skor sentimen dihitung dengan menjumlahkan nilai dari kata-kata yang ada di teks berdasarkan kamus tersebut. Sentimen akhir dikategorikan sebagai POSITIF, NEGATIF, atau NETRAL berdasarkan skor yang dihasilkan, dengan threshold -5 untuk negatif, 5 untuk positif, dan sisanya netral.

## Author

- Nama : Krisna Santosa
- Dicoding Profile : [Krisna Santosa](https://www.dicoding.com/users/krisna_santosa)