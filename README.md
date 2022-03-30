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
<br>

Ini adalah hasil dari sintaks diatas :
![Gambar 2](screenshot/ss2.PNG) <br>

## B. Membuat Layout Sederhana
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

Kemudian tambahkan sintaks html seperti dibawah ini : <br>
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
![Gambar 4](screenshot/ss4.PNG) <br>

### 4. Membuat Hero Panel
Buat hero panel dengan menambahkan sintaks HTML seperti dibawah ini : <br>
```
   <section id="hero">
        <h1>Hello Sunshine!</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
            elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
            vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
            pretium ac.</p>
        <a href="home.html" class="btn btn-large"> Learn more &raquo;</a>
    </section>
```
<br>

Kemudian tambahkan file CSS seperti dibawah ini : <br>
```
    /* HERO PANEL */
    #hero {
        background-color: #e4e4e5;
        padding: 50px 20px;
        margin-bottom: 20px;
    }

    #hero h1 {
        margin-bottom: 20px;
        font-size: 35px;
    }

    #hero p {
        margin-bottom: 20px;
        font-size: 18px;
        line-height: 25px;
    }
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 5](screenshot/ss5.PNG) <br>

### 5. Mengatur Layout dan Sidebar
Untuk mengatur main content dan sidebar, tambahkan sintaks css seperti dibawah ini : <br>
```
    /* MAIN CONTENT */
    #wrapper {
        margin: 0;
    }
    #main {
        float: left;
        width: 640px;
        padding: 20px;
    }

    /* SIDEBAR AREA */
    #sidebar {
        float: left;
        width: 260px;
        padding: 20px;
    }
```
<br>

### 6. Membuat Sidebar Widget
Tambahkan element lain pada sidebar dengan sintaks html seperti dibawah ini : <br>
```
    <aside id="sidebar">
        <div class="widget-box">
            <h3 class="title">Widget Header</h3>
            <ul>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
                <li><a href="#">Widget Link</a></li>
            </ul>
        </div>
        <div class="widget-box">
            <h3 class="title">Widget Text</h3>
            <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt 
            arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer 
            pharetra est nunc, nec pretium nunc pretium ac.</p>
        </div>
    </aside>
```
<br>

Kemudian tambahkan sintaks CSS seperti dibawah ini : <br>
```
    /* WIDGET */
    .widget-box {
        border: 1px solid #eee;
        margin-bottom: 20px;
    }

    .widget-box .title {
        padding: 10px 16px;
        background-color: #0ca878;
        color: #fff;
    }

    .widget-box ul {
        list-style-type: none;
    }

    .widget-box li {
        border-bottom: 1px solid #eee;
    }

    .widget-box li a {
        padding: 10px 16px;
        color: #333;
        display: block;
        text-decoration: none;
    }

    .widget-box list-style:hover a {
        background-color: #eee;
    }

    .widget-box p {
        padding: 15px;
        line-height: 25px;
    }
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 6](screenshot/ss6.PNG) <br>

### 7. Mengatur Footer
Mengatur footer dengan sintaks css seperti dibawah ini : <br>
```
    /* FOOTER */
    footer {
        clear: both;
        background-color: #1d1d1d;
        padding: 20px;
        color: #eee;
    }  
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 7](screenshot/ss7.PNG) <br>

### 8. Menambahkan Elemen Lainnya pada Main Content
Menambahkan elemen lain dengan sintaks html seperti dibawah ini : <br>
```
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/e9967a/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
                euismod.</p>
            <a href="#" class="btn btn-default">View Detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/98b3cd/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
                euismod.</p>
            <a href="#" class="btn btn-default">View Detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/dddd88/fff.png"  alt="" class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis 
                euismod.</p>
            <a href="#" class="btn btn-default">View Detail</a>
        </div> 
    </div>
</section>
```
<br>

Kemudian tambahkan sintaks pada CSS seperti dibawah ini : <br>
```
    /* BOX */
    .box {
        display: block;
        float: left;
        width: 33.333333%;
        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
        padding: 0px 10px;
        text-align: center;
    }

    .box h3 {
        margin: 15px 0px;
    }

    .box p {
        line-height: 20px;
        font-size: 14px;
        margin-bottom: 15px;
    }

    .box img {
        border: 0;
        vertical-align: middle;
    }

    .image-circle {
        border-radius: 50%;
    }

    .row {
        margin: 0 -10px;
        box-sizing: border-box;
        -moz-box-sizing: border-box;
        -webkit-box-sizing: border-box;
    }

    .row:after, .row:before,
    .entry:after, .entry:before {
    content:'';
    display:table;
    }
    .row:after,
    .entry:after {
    clear:both;
    }
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 8](screenshot/ss8.PNG) <br>

### 9. Menambahkan Content Artikel
Menambahkan content artikel sebelum `</section>` dengan sintaks html seperti dibawah ini : <br>
```
    <hr class="divider">
        <article class="entry">
            <h2>First Featurette Heading</h2>
            <img src="https://dummyimage.com/150/94d194/fff.png" alt="">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
                elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
              pretium ac.</p>
        </article>
    <hr class="divider">
        <article class="entry">
            <h2>First Featurette Heading</h2>
            <img src="https://dummyimage.com/150/94d194/fff.png" alt="" class="right-img">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
                elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, 
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
                pretium ac.</p>
        </article>
```
<br>

Kemudian tambahkan sintaks pada CSS seperti dibawah ini : <br>
```
    .divider {
        border: 0;
        border-top: 1px solid #eee;
        margin: 40px 0;
    }

    /* ENTRY */
    .entry {
        margin: 15px 0px;
    }

    .entry h2 {
        margin-bottom: 20px;
    }

    .entry p {
        line-height: 25px;
    }

    .entry img {
        float: left;
        border-radius: 5px;
        margin-right: 15px;
    }

    .entry .right-img {
        float: right;
        margin-left: 15px;
    }
```
<br>

Ini adalah hasil refresh dari sintaks diatas :
![Gambar 9](screenshot/ss9.PNG) <br>


## SOAL

### Pertanyaan dan Tugas


### 1. Tambahkan Layout untuk menu About, buat single layout yang berisi deskripsi, portfolio, dll ! <br>
Jawab : <br>

Berikut adalah sintaks html nya : <br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABOUT</title>
    <link rel="stylesheet" href="style_about.css">
</head>
<body>
    <div id="container">
        <header>
             <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="lab4_layout.html" >HOME</a>
            <a href="artikel.html">ARTIKEL</a>
            <a href="lab4_about.html" class="active">ABOUT</a>
            <a href="lab4_contact.html">KONTAK</a>
        </nav>
        <section id="hero">
            <img src="https://dummyimage.com/120/0ca878/fff.png" alt="" class="image-circle">
            <h3>TITLE</h3>
            <p>Donec sed odio dui.</p>
        </section>
        <section id="main">
            <div class="about">
                <h1>ABOUT US</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem 
                    elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,                         vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc 
                    pretium ac.</p>
            </div>
        </section>
        <section id="portopolio">
            <div class="row">
                <h3>PORTOFOLIO</h3>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/e9967a/fff.png" alt="">
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/94d194/fff.png" alt="" >
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/dddd88/fff.png"  alt="" >
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/94d194/fff.png" alt="" >
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/dddd88/fff.png"  alt="" >
                </div>
                <div class="box">
                    <img src="https://dummyimage.com/250x150/e9967a/fff.png" alt="">
                </div>  
            </div>
        <footer>
            <p>&copy; 2022 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
<br>

Berikut adalah sintaks css nya : <br>
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


/* HERO PANEL */
#hero {
    padding: 50px 15px;
    margin-bottom: 10px;
    font-family: 'Open Sans', sans-serif;
}

#hero h3 {
    font-size: 35px;
    font-family: 'Open Sans', sans-serif;
    margin-bottom: 15px;
    margin-top: 15px;
    text-align: center;
}

#hero p {
    font-size: 18px;
    font-family: 'Open Sans', sans-serif;
    line-height: 25px;
    text-align: center;
}
#hero img {
    border: 0;
    vertical-align: middle;
    margin-left: 44%;
}

.image-circle {
    border-radius: 50%;
}

/** about **/

.about {
    padding: 80px 80px;
    margin-left: 15px;
    margin-right: 15px;
    margin-bottom: 15px;
    text-align: center;
    background-color: #e4e4e5;
    font-family: 'Open Sans', sans-serif;
}

.about h1 {
    margin: 15px 0px;
    font-size: 25px;
}

.about p {
    line-height: 20px;
    margin-top: 50px;
    font-size: 18px;
    margin-bottom: 15px;
}

/* FOOTER */
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
}

/* BOX */
.box {
    display: block;
    float: left;
    width: 33.333333%;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    padding: 0px 10px;
    text-align: center;
    margin-bottom: 30px;
}

.row h3 {
    margin-bottom: 40px;
    font-size: 25px;
}

.box img {
    border: 0;
    vertical-align: middle;
}

.row {
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    padding: 50px 50px;
    text-align: center;
    background-color: #fff;
}

.row:after, .row:before,
.entry:after, .entry:before {
 content:'';
 display:table;
}
.row:after,
.entry:after {
 clear:both;
}

```
<br>

![Gambar 10](screenshot/ss10.PNG) <br>
![Gambar 11](screenshot/ss11.PNG) <br>
![Gambar 12](screenshot/ss12.PNG) <br>
<br>


### 2. Tambahkan layout untuk menu Contact, yang berisi form isian: nama, email, message, dll ! <br>
Jawab : <br>
    
Berikut adalah sintaks html nya : <br>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CONTACT</title>
    <link rel="stylesheet" href="style_contact.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="lab4_layout.html">HOME</a>
            <a href="artikel.html">ARTIKEL</a>
            <a href="lab4_about.html">ABOUT</a>
            <a href="lab4_contact.html" class="active">KONTAK</a>
        </nav>
        <section id="hero">
            <h1>Contact</h1>
                <form action="proses.php" method="post">
                    <fieldset>
                        <legend>Contact Us</legend>
                        <div class="form-group">
                            <label for="nama">Nama</label>
                            <input type="text" id="nama"  placeholder="Masukan Nama">
                        </div>
                        <div class="form-group">
                            <label for="email">E-mail</label>
                            <input type="email" id="email"  placeholder="Masukan E-mail">
                        </div>
                        <div class="form-group">
                            <label for="Web">Website URL</label>
                            <input type="web" id="web"  placeholder="Masukan Website URL">
                        </div>
                        <div class="form-group">
                            <label for="pesan">Pesan</label>
                            <textarea  rows="10" placeholder="Masukan Pesan"></textarea>
                        </div>
                            <button type="submit" class="btn btn-danger">Kirim Pesan</button>
                    </fieldset>
                </form>
        </section>
        <footer>
            <p>&copy; 2022 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
<br>

Berikut adalah sintaks css nya : <br>
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

/* HERO PANEL */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}

legend {
    text-align: center;
    font-family: sans-serif;
}

/* INPUT */
input {
    width: 99%;
    font-family: 'Open Sans', sans-serif;
}

.form-group {
    margin-top: 25px;
    margin-left: 15px;
    font-family: 'Open Sans', sans-serif;
}

label {
    margin-left: 12px;
    font-family: 'Open Sans', sans-serif;
}

input {
    width: 97%;
    padding: 10px 15px;
    margin: 10px 10px;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
}

textarea {
    width: 97%;
    padding: 10px 15px;
    margin: 10px 10px;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
}

button[type=submit] {
    margin-left: 25px;
    padding: 10px 10px;
    margin-bottom: 25px;
    margin-top: 15px;
    background-color: #0ca878;
    border: 1px solid #197a43;
    color: #fff;  
    font-weight: bold;
    font-family: 'Open Sans', sans-serif;
}


/* FOOTER */
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
}

```
<br>

![Gambar 13](screenshot/ss13.PNG) <br>
![Gambar 14](screenshot/ss14.PNG) <br>




