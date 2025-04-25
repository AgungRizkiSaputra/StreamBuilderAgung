Lanjutan dari GitHub sebelumnya : https://github.com/AgungRizkiSaputra/StreamAgung

# Praktikum 5 : Multiple Stream Subscription

### P5: Jawaban Soal 12

- Langkah 3, itu class NumberStream yang memiliki method getNumbers, yang mengembalikan sebuah Stream dari tipe int. Stream.periodic(Duration, callback) digunakan untuk menghasilkan data secara berkala (setiap 1 detik).
  Di tiap periode (setiap detik), sebuah angka acak dari 0 sampai 9 dihasilkan menggunakan Random().nextInt(10).
  yield\* digunakan untuk meneruskan stream hasil dari Stream.periodic keluar dari method getNumbers.

- Langkah 7, StreamBuilder digunakan untuk mendengarkan stream (numberStream) dan memperbarui UI setiap kali data baru masuk. initialData: 0 artinya data awal yang ditampilkan sebelum stream mulai memancarkan data adalah 0.

snapshot berisi status dan data terbaru dari stream:

- snapshot.hasData: mengecek apakah ada data yang tersedia.

- snapshot.data: adalah angka acak yang dihasilkan dari stream.

Jika tidak ada data, maka akan mengembalikan widget kosong (SizedBox.shrink()).

<img src="https://github.com/AgungRizkiSaputra/StreamBuilderAgung/blob/main/image/GIFP5soal12.gif" width="150px">
