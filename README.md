# 🤖 Belajar Vue Js 3 🤖

##### Binding Text ✍️

Digunakan untuk menampilkan teks di elemen html kita, dengan cara ini akan meningkatkan performa aplikasi kita

```sh
<div v-text="your-text" />
```

##### Binding Html 🧶

Digunakan untuk merubah sebuah teks atau data dari html code menjadi text normal. Tetapi ini tidak begitu disarankan karena bisa menyebabkan serangan csr

```sh
<div v-html="<b>Hai</b>"/>
```

##### Binding Attributes 🧣

Digunakan untuk membuat attribute pada tag html

```sh
<h1 v-bind:html-attribute="your-data">Hay</h1>

contoh :
<h1 v-bind:id="your-style">Hai</h1>
```

##### Binding Class 👀

Digunakan untuk membuat class pada tag html kita
| Penjelasan | Penggunaan |
| ---------- | ---------- |
| Ketika menggunakan static class | <div class="your-css"></div> |
| Dinamis Class : Ketika ingin menerapkan satu style saja | <div  v-bind:class="isOpen && 'open'"></div> |
| Dinamis Class : Ketika ingin ada dua kondisi | <div v-bind:class="isOpen ? 'open' : 'close'"></div> |
| Dinamis Class : Ketika ingin menerapkan banyak kondisi dengan satu style bisa gunakan | <div v-bind:class="{'open' : isOpen,'finish' : isFinish,}"></div> |
| Dinamis Class : Ketika ingin menerapkan banyak kondisi dengan dua style | <div v-bind:class="[isOpen && 'open', isPromo ? 'promo' : 'no-promo']"></div> |

# 🕵️ Terimakasih Tunggu Kelanjutannya 🕵️
