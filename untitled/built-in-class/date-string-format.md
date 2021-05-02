# Date String Format

ketika kita menggunakan tanggal dan waktu, kita perlu memahami format yang dipakai oleh standar dunia. Ini berguna dan memudahkan kita untuk melakukan konversi dan manipulasi sebuah tanggal. Format date string sendiri, secara umum terdiri dari:

| Format | Penjelasan |
| :--- | :--- |
| YYYY | 4 digit tahun, misalkan : 2021 |
| MM | 2 digit bulan, misalkan : 01 berarti Januari |
| DD | 2 digit tanggal 0 sampai 31 |
| HH | 2 digit jam 0 sampai 23 |
| mm | 2 digit menit 0 sampai 59 |
| ss | 2 detik detik 0 sampai 49 |
| sss | 3 digit milidetik 0 sampai 999 |
| - | Pemisah untuk tanggal |
| : | Pemisah untuk waktu |
| Z | Berarti tanggal akan diatur sebagai UTC |

Dari tabel format di atas, ketika misalnya kita akan melakukan parsing baik dari string ke milliseconds ataupun sebaliknya, kita dapat memanfaat format di atas.

Untuk Date Object javascript sendiri, nilai epoch dimulai dari 0 untuk tanggal 1 January, 1970, 00:00:00 UTC

