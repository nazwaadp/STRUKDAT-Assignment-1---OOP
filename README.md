
#  **Identitas**
* **Nama**        = Nazwa Aulia Dwi Purnomo <br>
* **NRP**         = 5027251018<br>
* **Kelas**       = B<br>
* **Mata Kuliah** = Struktur Data dan Pemograman Berorientasi Objek<br>
---

#  **Table of Contents**

* [1. Class](#1-class)
* [2. Object](#2-object)
* [3. Constructor](#3-constructor)
* [4 Pillars of OOP - Encapsulation](#1-encapsulation) <br>
[4 Pillars of OOP - Inheritance](#2-inheritance) <br>
[4 Pillars of OOP - Polymorphism](#3-polymorphism) <br>
[4 Pillars of OOP - Abstraction](#4-abstraction)


# 1. Class
**Class** adalah blueprint atau rancangan yang digunakan untuk membuat object dalam pemrograman berorientasi objek. Di dalam class biasanya ada **atribut (variabel)** untuk menyimpan data dan **method (fungsi)** yang mendefinisikan sifat dari object tersebut. <br>
Class hanya berisi struktur atau konsep dasar suatu objek dan belum menjadi objek yang nyata sampai dibuat instance-nya. Dengan menggunakan class, kita dapat mengorganisasi kode menjadi lebih terstruktur dan mudah digunakan kembali.

```java
class Car {

    // atribut
    private String brand;
    private String color;
    private String type;
    private int speed;
}
```

# 2. Object

**Object** adalah hasil dari pembuatan sebuah class atau disebut juga **instance dari class**. Object memiliki atribut dan method yang sudah didefinisikan di dalam class, tetapi nilainya bisa berbeda untuk setiap object. <br>
Dengan menggunakan object, kita bisa membuat banyak objek dari satu class yang sama. Hal ini membuat program lebih fleksibel karena kita bisa merepresentasikan banyak benda atau data yang berbeda dengan struktur yang sama.

```java
Car myCar = new Car();
Car myHonda = new Car("Honda", "yellow", "Brio", 150);
```
Pada contoh tersebut dibuat dua object dari class Car, yaitu:
myCar, myHonda <br>
Object myHonda langsung memiliki data seperti brand Honda, warna kuning, tipe Brio, dan kecepatan 150.

# 3. Constructor

**Constructor** adalah **method khusus** yang otomatis dijalankan ketika sebuah object dibuat. Constructor biasanya digunakan untuk memberikan nilai awal pada atribut object sehingga object langsung siap digunakan. <br>
Constructor memiliki nama yang sama dengan nama class dan tidak memiliki tipe data return. Dalam satu class bisa terdapat lebih dari satu constructor dengan parameter yang berbeda.
```java
public Car() {
}
```

Constructor di atas adalah constructor kosong yang digunakan ketika object dibuat tanpa memberikan data.

```java
public Car (String brand, String color, String type, int speed) {
    this.brand = brand;
    this.color = color;
    this.type = type;
    this.speed = speed;
}
```
Constructor diatas sudah ada parameter yang sudah bisa digunakan untuk mengisi atribut mobil saat object dibuat.

# **4 Pillars of OOP**

## 1. Encapsulation

**Encapsulation** adalah konsep membungkus data dan method dalam satu class serta membatasi akses langsung ke data tersebut. Biasanya atribut dibuat **private**, kemudian diakses menggunakan method seperti **getter** dan **setter**. <br>
Tujuan utama encapsulation adalah menjaga keamanan data dan mencegah perubahan yang tidak diinginkan dari luar class. Dengan cara ini, kontrol terhadap data menjadi lebih teratur.

```java
private String brand;
private String color;
private String type;
private int speed;
```

Karena atribut dibuat private, data tersebut tidak bisa diakses langsung dari luar class. Untuk mengambil datanya digunakan method getter:

```java
public String getColor() {
    return color;
}
```

Contoh penggunaannya: <br>
``` java
System.out.println(myHonda.getColor());
```
Method ini akan mengambil nilai color dari object myHonda.

## 2. Inheritance

**Inheritance** adalah konsep pewarisan dimana sebuah class dapat mewarisi atribut dan method dari class lain. Class yang diwarisi disebut **parent class**, sedangkan class yang mewarisi disebut **child class**. <br>
Dengan inheritance, kode dapat digunakan kembali tanpa harus menulis ulang method yang sama. Hal ini membuat program lebih efisien dan lebih mudah dikembangkan.

## 3. Polymorphism

**Polymorphism** berarti satu method dapat memiliki banyak bentuk atau perilaku yang berbeda. Method yang sama dapat menghasilkan output yang berbeda tergantung object yang memanggilnya. <br>
Polymorphism biasanya terjadi melalui **method overriding** atau **method overloading**, sehingga program menjadi lebih fleksibel dalam menangani berbagai jenis object.

## 4. Abstraction

**Abstraction** adalah konsep menyederhanakan sistem dengan hanya menampilkan bagian penting dan menyembunyikan detail implementasi yang tidak diperlukan oleh pengguna. <br>
Dalam Java, abstraction biasanya diterapkan menggunakan **abstract class** atau **interface**. Dengan cara ini, kita dapat fokus pada fungsi utama tanpa harus mengetahui detail internal dari sistem.

# **Contoh latihan**
```java
public class WarnaMobil {
    public static void main(String[] args) throws Exception {

      Car myCar = new Car();
      Car myHonda = new Car("Honda", "kuning", "Brio", 150);

      System.out.println("Mobil saya berwarna: " + myHonda.getColor());
    }
}

class Car {
    // atribut 
    private String brand;
    private String color;
    private String type;
    private int speed;

    // constructor (harus sama dengan nama class nya)
    public Car() {
    }
    public Car (String brand, String color, String type, int speed) {
        this.brand = brand;
        this.color = color;
        this.type = type;
        this.speed = speed;
    }

    // method
    public void accelerate(int speedincrease) {
    }
    public String getColor() {
        return color;
    }

}
```
## Output
```
Mobil saya berwarna: kuning