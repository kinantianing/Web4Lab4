# Web4Lab4

**Nama    : Aning Kinanti** <br>
**NIM     : 312010364** <br>
**Kelas   : TI.20.A2** <br>
**Matkul  : Pemrograman Web** <br>

# Membuat Box Element dan Layout Sederhana

## A. Membuat Box Element
### 1. Membuat File HTML
Buatlah dokumen HTML seperti contoh dibawah ini : <br>
```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>BOX ELEMENT</title>
    </head>
    <body>
        <header>
            <h1>Box Element</h1>
        </header>
    </body>
    </html>
```
<br>

### 2. Membuat Box Element
Lalu tambahkan sintaks dibawah ini pada tag <body> untuk membuat box element dengan tag `<div>` : <br>
```
    <section>
        <div class="div1">DIV 1</div>
        <div class="div2">DIV 2</div>
        <div class="div3">DIV 3</div>
    </section>
```
<br>

### 3. Menambahkan CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut : <br>
```
    <style>
        div {
            float: left;
            padding: 10px;
        }
        .div1 {
            background: lightcoral;
        }
        .div2 {
            background: burlywood;
        }
        .div3 {
            background: lightgreen;
        }
    </style>
```
<br>

Ini adalah hasil dari sintaks diatas :
![Gambar 1](screenshot/ss1.PNG) <br>

### 4. Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk 
mengaturnya. <br>
Tambahkan element div lainnya seteleah div3 seperti berikut : <br>
```
    <section>
        <div class="div1">DIV 1</div>
        <div class="div2">DIV 2</div>
        <div class="div3">DIV 3</div>
        <div class="div4">DIV 4</div>
    </section>
```
<br>

Kemudian atur property clear pada CSS seperti berikut : <br>
```
    .div4 {
        background-color: lightblue;
        clear: left;
        float: none;        
    }
```

Ini adalah hasil dari sintaks diatas :
![Gambar 1](screenshot/ss1.PNG) <br>