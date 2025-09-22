# REPORT.md
Tugas Asistensi Dasar Pemrograman 2 

## Identitas
- Nama : Wahyu Adithya Prasath 
- NRP  : 5022251166
- Modul: 2

---

## Log Commit
1. **Commit 1** - Clone repo template 
2. **Commit 2** - Perbaikan parameter fungsi `read_matrix` (menggunakan `int M[N][N]`).
3. **Commit 3** - Perbaikan loop `read_matrix` (mengganti `k < N` menjadi `j < N`).
4. **Commit 4** - Mengganti format input dari `%lf` ke `%d`.
5. **Commit 5** - Menambahkan deklarasi variabel `sum` di fungsi `multiply()`.
6. **Commit 6** - Mengganti `printf("%c")` menjadi `printf("%d")` pada fungsi `print_matrix()`.
7. **Commit 7** - Menambahkan titik koma hilang setelah `read_matrix(B);`.
8. **Commit 8** - Program berhasil dikompilasi dan dijalankan dengan output sesuai.

---

## Perbandingan Kode Asal dan Kode Perbaikan

### 1. Parameter fungsi `read_matrix`
- **Kode Asal:**
  ```c
  void read_matrix(int M[x][y])

  void read_matrix(int M[N][N]) //kode perbaikan (x dan y tidak pernah didefinisikan.)


### 2. Perbaikan Loop `read_matrix`
- **Kode Asal:**
  ```c
  for (int j = 0; k < N; j++)

  for (int j = 0; j < N; j++)//kode perbaikan (variabel k dipakai padahal loop pakai j.)

### 3.Mengganti format input
- **Kode Asal:**
  ```c
  scanf("%lf", &M[i][j]);

  scanf("%d", &M[i][j]);//kode perbaikan (%lf untuk double, padahal array bertipe int.)

### 4.Menambahkan deklarasi variabel `sum`
- **Kode Asal:**
  ```c
  sum = 0;
  sum += A[i][k] * B[k][j];

  int sum = 0;//kode perbaikan (ariabel sum belum pernah dideklarasikan.)

### 5.Mengganti `printf("%c")` menjadi `printf("%d")` pada fungsi `print_matrix()`.
- **Kode Asal:**
  ```c
  printf("%c ", M[i][j]);

  printf("%d ", M[i][j]);//kode perbaikan (%c hanya untuk karakter.)

### 6.Menambahkan titik koma hilang setelah `read_matrix(B);`.
- **Kode Asal:**
  ```c
  read_matrix(B)

  read_matrix(B);//kode perbaikan (kurang ; diakhir )


  Contoh input
  Masukkan elemen matriks A (3x3):
  1 2 3
  4 5 6
  7 8 9

  Masukkan elemen matriks B (3x3):
  9 8 7
  6 5 4
  3 2 1
  
  contoh output
  Hasil perkalian matriks:
  30 24 18
  84 69 54
  138 114 90

