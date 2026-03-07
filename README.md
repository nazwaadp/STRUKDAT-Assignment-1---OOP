
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
* [Encapsulation](#1-encapsulation)
* [Inheritance](#2-inheritance)
* [Polymorphism](#3-polymorphism)
* [Abstraction](#4-abstraction)


# 1. Class

**Class** adalah blueprint atau rancangan yang digunakan untuk membuat object dalam pemrograman berorientasi objek. Di dalam class biasanya terdapat **atribut (variabel)** untuk menyimpan data dan **method (fungsi)** yang mendefinisikan perilaku dari object tersebut.

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

**Object** adalah hasil dari pembuatan sebuah class atau disebut juga **instance dari class**. Object memiliki atribut dan method yang sudah didefinisikan di dalam class, tetapi nilainya bisa berbeda untuk setiap object.

Dengan object, kita dapat menggunakan struktur yang sudah dibuat di class untuk merepresentasikan benda atau konsep nyata dalam program. Satu class dapat menghasilkan banyak object yang memiliki karakteristik berbeda.


```java
public class Campur {
    public static void main(String[] args) throws Exception {

      Car myCar = new Car();
      Car myHonda = new Car("Honda", "yellow", "Brio", 150);

      System.out.println("My mobil: " + myHonda.getBrand());
    }
}
```

# 3. Constructor

**Constructor** adalah method khusus yang otomatis dijalankan ketika sebuah object dibuat dari suatu class. Constructor biasanya digunakan untuk memberikan **nilai awal pada atribut** sehingga object langsung memiliki data saat pertama kali dibuat.

Dengan menggunakan constructor, proses inisialisasi object menjadi lebih praktis dan rapi karena data dapat langsung diisi ketika object dibuat. Constructor memiliki nama yang sama dengan nama class.

```java
public Car() {
}

public Car (String brand, String color, String type, int speed) {
    this.brand = brand;
    this.color = color;
    this.type = type;
    this.speed = speed;
}
```

# **4 Pillars of OOP**

## 1. Encapsulation

**Encapsulation** adalah konsep membungkus data dan method dalam satu class serta membatasi akses langsung ke data tersebut. Biasanya atribut dibuat **private**, kemudian diakses menggunakan method seperti **getter** dan **setter**.

Tujuan utama encapsulation adalah menjaga keamanan data dan mencegah perubahan yang tidak diinginkan dari luar class. Dengan cara ini, kontrol terhadap data menjadi lebih teratur.

```java
private String brand;
private String color;
private String type;
private int speed;

public String getBrand() {
    return brand;
}
```

---

## 2. Inheritance

**Inheritance** adalah konsep pewarisan dimana sebuah class dapat mewarisi atribut dan method dari class lain. Class yang diwarisi disebut **parent class**, sedangkan class yang mewarisi disebut **child class**.

Dengan inheritance, kode dapat digunakan kembali tanpa harus menulis ulang method yang sama. Hal ini membuat program lebih efisien dan lebih mudah dikembangkan.

---

## 3. Polymorphism

**Polymorphism** berarti satu method dapat memiliki banyak bentuk atau perilaku yang berbeda. Method yang sama dapat menghasilkan output yang berbeda tergantung object yang memanggilnya.

Polymorphism biasanya terjadi melalui **method overriding** atau **method overloading**, sehingga program menjadi lebih fleksibel dalam menangani berbagai jenis object.

---

## 4. Abstraction

**Abstraction** adalah konsep menyederhanakan sistem dengan hanya menampilkan bagian penting dan menyembunyikan detail implementasi yang tidak diperlukan oleh pengguna.

Dalam Java, abstraction biasanya diterapkan menggunakan **abstract class** atau **interface**. Dengan cara ini, programmer dapat fokus pada fungsi utama tanpa harus mengetahui detail internal dari sistem.

