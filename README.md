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
![Gambar 2](screenshot/ss2.PNG) <br>

## A. Membuat Layout Sederhana
### 1. Membuat File HTML
Buatlah dokumen HTML seperti contoh dibawah ini : <br>
```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>LAYOUT SEDERHANA</title>
        <link rel="stylesheet" href="style_layout.css">
    </head>
    <body>
        <div id="container">
            <header>
                <h1>Layout Sederhana</h1>
            </header>
        </div>
    </body>
    </html>
```
<br>

Kemudian tambahkan sintaks kode seperti dibawah ini : <br>
```
    <nav>
        <a href="home.html" class="active">HOME</a>
        <a href="artikel.html">ARTIKEL</a>
        <a href="about.html">ABOUT</a>            
        <a href="kontak.html">KONTAK</a>
    </nav>
    <section id="hero"></section>
    <section id="wrapper">
        <section id="main"></section>
        <aside id="sidebar"></aside>
    </section>
    <footer>
        <p>&copy; 20212 - Universitas Pelita Bangsa</p>
    </footer>

```
<br>

Ini adalah hasil dari sintaks diatas :
![Gambar 3](screenshot/ss3.PNG) <br>

### 2. Menambahkan file CSS 
Buatlah dokumen file CSS dengan nama style_layout.css dengan sintaks seperti contoh dibawah ini : <br>
```
    /* RESET CSS*/
    * {
        margin: 0;
        padding: 0;
    }

    body {
        line-height: 1;
        font-size: 100%;
        font-family: 'Open Sans', sans-serif;
        color: #5a5a5a;
    }

    #container {
        width: 980px;
        margin: 0 auto;
        box-shadow: 0 0 1em #ccc;
    }

    /* HEADER*/
    header {
        padding: 20px;
    }

    header h1 {
        margin: 20px 10px;
        color: #a0a0a0;
    } 
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 4](screenshot/ss4.PNG) <br>

### 3. Membuat Navigasi
Mengatur navigasi pada file CSS dengan sintaks seperti contoh dibawah ini : <br>
```
    /* NAV */
    nav {
        display: block;
        background-color: #bebebe;
    }

    nav a {
        padding: 15px 30px;
        display: inline-block;
        color: #fff;
        font-size: 14px;
        text-decoration: none;
        font-weight: bold;
    }

    nav a.active,
    nav a:hover {
        background-color: #0ca878;
    }
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 5](screenshot/ss5.PNG) <br>

