
#  **Identitas**
* **Nama**        = Nazwa Aulia Dwi Purnomo <br>
* **NRP**         = 5027251018<br>
* **Kelas**       = B<br>
* **Mata Kuliah** = Struktur Data dan Pemograman Berorientasi Objek<br>
---

#  **Table of Contents**

* [Class](#1-class)
* [Object](#2-object)
* [Constructor](#3-constructor)
* [Destructor](#4-destructor)
* [Encapsulation](#1-encapsulation)
* [Inheritance](#2-inheritance)
* [Polymorphism](#3-polymorphism)
* [Abstraction](#4-abstraction)

---

# 1. Class

**Class** adalah blueprint atau rancangan yang digunakan untuk membuat object dalam pemrograman berorientasi objek. Di dalam class biasanya terdapat **atribut (variabel)** untuk menyimpan data dan **method (fungsi)** yang mendefinisikan perilaku dari object tersebut.

Class hanya berisi struktur atau konsep dasar suatu objek dan belum menjadi objek yang nyata sampai dibuat instance-nya. Dengan menggunakan class, programmer dapat mengorganisasi kode menjadi lebih terstruktur dan mudah digunakan kembali.


```java
class Car {
    String brand;
    String color;
    int speed;

    void drive() {
        System.out.println("Mobil sedang berjalan");
    }
}
```

---

# 2. Object

**Object** adalah hasil dari pembuatan sebuah class atau disebut juga **instance dari class**. Object memiliki atribut dan method yang sudah didefinisikan di dalam class, tetapi nilainya bisa berbeda untuk setiap object.

Dengan object, kita dapat menggunakan struktur yang sudah dibuat di class untuk merepresentasikan benda atau konsep nyata dalam program. Satu class dapat menghasilkan banyak object yang memiliki karakteristik berbeda.


```java
public class Main {
    public static void main(String[] args) {

        Car mobil1 = new Car();
        mobil1.brand = "Toyota";
        mobil1.color = "Merah";
        mobil1.speed = 120;

        System.out.println(mobil1.brand);
        mobil1.drive();
    }
}
```

---

# 3. Constructor

**Constructor** adalah method khusus yang otomatis dijalankan ketika sebuah object dibuat dari suatu class. Constructor biasanya digunakan untuk memberikan **nilai awal pada atribut** sehingga object langsung memiliki data saat pertama kali dibuat.

Dengan menggunakan constructor, proses inisialisasi object menjadi lebih praktis dan rapi karena data dapat langsung diisi ketika object dibuat. Constructor memiliki nama yang sama dengan nama class.


```java
class Car {

    String brand;
    String color;

    Car(String brand, String color) {
        this.brand = brand;
        this.color = color;
    }

    void showInfo() {
        System.out.println("Brand: " + brand);
        System.out.println("Color: " + color);
    }
}
```
---

# 4. Destructor

**Destructor** adalah method yang dijalankan ketika object sudah tidak digunakan lagi. Tujuannya adalah untuk membersihkan resource seperti memori atau koneksi yang sebelumnya digunakan oleh object tersebut.

Dalam bahasa Java sebenarnya tidak ada destructor seperti pada C++, karena Java menggunakan **Garbage Collector** yang secara otomatis menghapus object yang tidak lagi digunakan. Namun secara konsep, proses ini tetap berfungsi untuk mengelola memori program.


```java
class Car {

    protected void finalize() throws Throwable {
        System.out.println("Object mobil dihapus dari memori");
    }

}
```

---

# **4 Pillars of OOP**

## 1. Encapsulation

**Encapsulation** adalah konsep membungkus data dan method dalam satu class serta membatasi akses langsung ke data tersebut. Biasanya atribut dibuat **private**, kemudian diakses menggunakan method seperti **getter** dan **setter**.

Tujuan utama encapsulation adalah menjaga keamanan data dan mencegah perubahan yang tidak diinginkan dari luar class. Dengan cara ini, kontrol terhadap data menjadi lebih teratur.

```java
class Mahasiswa {

    private String nama;

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getNama() {
        return nama;
    }

}
```

---

## 2. Inheritance

**Inheritance** adalah konsep pewarisan dimana sebuah class dapat mewarisi atribut dan method dari class lain. Class yang diwarisi disebut **parent class**, sedangkan class yang mewarisi disebut **child class**.

Dengan inheritance, kode dapat digunakan kembali tanpa harus menulis ulang method yang sama. Hal ini membuat program lebih efisien dan lebih mudah dikembangkan.

```java
class Kendaraan {

    void jalan() {
        System.out.println("Kendaraan sedang berjalan");
    }

}

class Mobil extends Kendaraan {

    void klakson() {
        System.out.println("Tin tin!");
    }

}
```

---

## 3. Polymorphism

**Polymorphism** berarti satu method dapat memiliki banyak bentuk atau perilaku yang berbeda. Method yang sama dapat menghasilkan output yang berbeda tergantung object yang memanggilnya.

Polymorphism biasanya terjadi melalui **method overriding** atau **method overloading**, sehingga program menjadi lebih fleksibel dalam menangani berbagai jenis object.

```java
class Hewan {

    void suara() {
        System.out.println("Hewan bersuara");
    }

}

class Kucing extends Hewan {

    void suara() {
        System.out.println("Meong");
    }

}
```

---

## 4. Abstraction

**Abstraction** adalah konsep menyederhanakan sistem dengan hanya menampilkan bagian penting dan menyembunyikan detail implementasi yang tidak diperlukan oleh pengguna.

Dalam Java, abstraction biasanya diterapkan menggunakan **abstract class** atau **interface**. Dengan cara ini, programmer dapat fokus pada fungsi utama tanpa harus mengetahui detail internal dari sistem.

```java
abstract class Kendaraan {

    abstract void jalan();

}

class Motor extends Kendaraan {

    void jalan() {
        System.out.println("Motor sedang berjalan");
    }

}
```

