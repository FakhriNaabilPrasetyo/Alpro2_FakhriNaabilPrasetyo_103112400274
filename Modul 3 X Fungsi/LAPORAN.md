<h1 align="center">Laporan Praktikum Modul 3<br>Fungsi</h1>

<p align="center">FAKHRI NAABIL PRASETYO - 103112400274</p> 

### Soal 1
```go
package main

import "fmt"

// Digunakan untuk menghitung nilai faktorial dari n
func Faktorial(n int) int {
	var hasil int

	if n == 0 {
		return 1
	}

	hasil = 1
	for i := 1; i <= n; i++ {
		hasil *= i
	}

	return hasil
}

// Digunakan untuk permutasi
func Permutasi(n, r int) int {
	var hasil int
	hasil = Faktorial(n) / Faktorial(n-r)

	return hasil
}

// Fungsi yang digunakan untuk mengombinasikan 
func Kombinasi(n, r int) int {
	var hasil int
	hasil = Faktorial(n) / (Faktorial(r) * Faktorial(n-r))
	return hasil
}

func main() {
	var a, b, c, d int
	fmt.Scan(&a, &b, &c, &d)

	if a >= c && b >= d {
		fmt.Println(Permutasi(a, c), Kombinasi(a, c))
		fmt.Println(Permutasi(b, d), Kombinasi(b, d))
	}
}
```
![](Soal1.png)

Penjelasan  :
Program ini menghitung faktorial, permutasi, dan kombinasi berdasarkan input pengguna. Faktorial digunakan sebagai dasar perhitungan, di mana permutasi menghitung jumlah cara menyusun elemen dengan memperhatikan urutan, sedangkan kombinasi menghitung jumlah cara memilih elemen tanpa memperhatikan urutan. Program menerima empat angka sebagai input, lalu memproses apakah nilai yang dimasukkan memenuhi syarat sebelum melakukan perhitungan.


### Soal 2
```go
package main

  

import "fmt"

  

// Fungsi untuk menyimpan rumus f

func f(x int) int {

    var rumus int

    rumus = x * x

    return rumus

}

  

// Fungsi untuk menyimpan rumus g

func g(x int) int {

    var rumus int

    rumus = x - 2

    return rumus

}

  

// Fungsi untuk menyimpan rumus h

func h(x int) int {

    var rumus int

    rumus = x + 1

    return rumus

}

  

func main() {

  

    var x1, x2, x3, fogoh, gohof, hofog int

    fmt.Scan(&x1, &x2, &x3)

  

    fogoh = f(g(h(x1)))

    gohof = g(h(f(x2)))

    hofog = h(f(g(x3)))

  

    fmt.Println(fogoh, gohof, hofog)

  

}
```
![](Soal2.png)

Penjelasan  :
Ketika program diatas dijalankan, maka program akan meminta pengguna untuk memasukan 3 buah inputan. 3 buah inputan ini kemudian akan diolah dan menghasilkan 3 output, yaitu:
1. Menggunakan rumus f(g(h(x1)))
2. Menggunakan rumus g(h(f(x1)))
3. Menggunakan rumus h(f(g(x1)))


### Soal 3
```go
package main

  

import (

    "fmt"

    "math"

)

  

// Fungsi jarak menghitung jarak antara dua titik (a,b) dan (c,d)

func jarak(a, b, c, d float64) float64 {

    return math.Sqrt(math.Pow(a-c, 2) + math.Pow(b-d, 2))

}

  

// Fungsi didalam mengecek apakah titik (x,y) berada dalam lingkaran

func didalam(cx, cy, r, x, y float64) bool {

    return jarak(cx, cy, x, y) <= r

}

  

func main() {

    var cx1, cy1, r1, cx2, cy2, r2, x, y float64

    var didalam1, didalam2 bool

  

    fmt.Scan(&cx1, &cy1, &r1)

    fmt.Scan(&cx2, &cy2, &r2)

    fmt.Scan(&x, &y)

  

    didalam1 = didalam(cx1, cy1, r1, x, y)

    didalam2 = didalam(cx2, cy2, r2, x, y)

  

    if didalam1 && didalam2 {

        fmt.Println("Titik di dalam lingkaran 1 dan 2")

    } else if didalam1 {

        fmt.Println("Titik di dalam lingkaran 1")

    } else if didalam2 {

        fmt.Println("Titik di dalam lingkaran 2")

    } else {

        fmt.Println("Titik di luar lingkaran 1 dan 2")

    }

}
```
![](Soal3.png)

Penjelasan  :
Program ini menentukan apakah suatu titik berada di dalam satu atau dua lingkaran berdasarkan input pengguna. Jarak antara titik dan pusat lingkaran dihitung menggunakan rumus Euclidean, dan hasilnya dibandingkan dengan jari-jari lingkaran untuk menentukan posisi titik. Program menerima koordinat pusat dan jari-jari dua lingkaran, serta koordinat titik yang diuji, kemudian mengevaluasi apakah titik tersebut berada dalam satu, kedua, atau di luar lingkaran. Hasil akhirnya ditampilkan dalam bentuk teks sesuai dengan kondisi yang terjadi.

