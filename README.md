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

##### Binding Inline Css 🤡

Digunakan untuk memberi css langsung dari tag html nya

```sh
<h2 v-bind:style="{
    color : red,
    fontSize : 10px,
}"> Color Me </h2>
```

##### Shorthand Binding 🤗

Digunakan untuk menyingkat bind kita agar code menjadi sedikit dan rapih
Contoh :
| Dari | Menjadi |
| ---- | ------ |
| `<h1 v-bind:class="text-red"> Hay </h1>` | `<h1 :class="text-red"> Hay </h1>`
Kesimpulan : menghilangkan v-bind dengan langsung menulis attribute yang ingin kita gunakan :class, :id, :style, :disabled, dll..

##### Conditional Rendering 🤝

1. IF => hanya memiliki satu kondisi, dari contoh di bawah berarti div tersebut tidak tampil

```sh
const show = false;
<div v-if="show == true">this is show ?</div>
```

2. IF ELSE => memiliki 2 kondisi

```sh
const show = false;
<div v-if="show == true">this is show</div>
<div v-else> this is hidden </div>
```

3. IF ELSE IF => memiliki lebih dari 2 kondisi

```sh
const number = 10;
<div v-if="number / 2 == 5">kondition 1</div>
<div v-else-if="number / 2 == 1">kondition 2</div>
<div v-else>kondition 3</div>
```

4. V-SHOW => Digunakan untuk menyembunyikan sebuah div

Perbedaan ketika menggunakan v-show dan if di elemen html kita ?
| HTML Code | Browser Rendering |
| ---- | ---- |
| `<h1 v-show="false">Hai</h1>` | `<h1 style="display:none"></h1>`|
|`<h1 v-if="false"> Hai </h1>` | Browser tidak akan merender html kita jadi ini ketika di inspect element tidak akan ada |

##### List Rendering 👩‍🎤

Digunakan untuk melakukan sebuah looping data berbentuk array maupun object, disini akan ada beberapa cara looping di vue js dengan data yang berbeda

1. Looping Data Array

```sh
const names = ["Andi", "Andu","Pandu"]

<h3 v-for="(name, index) in names" :key="index">{{name}}</h3>
```

2. Looping Array Of Object

```sh
const dataStudents = [
{
id : 10002,
name : "Andi",
old : 19,
address : "Jakarta",
}

<!--untuk menampilkan data lebih dari satu dalam sebuah loop bisa membungkusnya menggunakan tag template atau tag div-->

<template v-for="student in dataStudents" :key="student.id">
    <h1>{{student.name}}</h1>
    <h2>{{student.old}}</h2>
    <p>{{student.address}}</p>
</template>
]
```

3. Looping Array In Object Of Array

```sh
const frameworks = [
{
    language : "JS",
    framework : ["React Js", "Svelt", "Vue Js", "Angular Js"]
}

<div v-for="(framework, index) in frameworks" :key="index">
<h1>{{framework.language}}</h1>
<p v-for="(data, index) in framework.framework" :key="index">
{{data}}</p>
</div>
]
```

4. Looping On Object Data

```sh
const names = {
    first : "Ananda",
    last : "Kuase"
}

<h1 v-for="(name, key, index) in names" :key="index">
{{name.first}} {{name.last}}
</h1>
```

# 🕵️ Terimakasih Tunggu Kelanjutannya 🕵️
