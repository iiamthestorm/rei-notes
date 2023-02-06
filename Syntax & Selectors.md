#CSS
# Basic Syntax

At the most basic level, [[CSS]] is made up of various rules. These rules are made up of a selector (more on this in a bit) and a semi-colon separated list of declarations, with each of those declarations being made up of a property:value pair.

<img src="https://cdn.statically.io/gh/TheOdinProject/curriculum/05ce472eabf8e04eeb2cc9139e66db884074fd7d/foundations/html_css/css-foundations/imgs/00.jpg">

# Selectors

Selector biasanya merupakan elemen-elemen html yang akan digunakan untuk mengaplikasikan [[CSS]] untuk  rules2 tertentu. Disini akan dijelaskan beberapa selector yang paling sering digunakan.

## Universal Selector

Universal Selector adalah selector yang selectornya berupa element arterisk (\*). Bisa dilihat contoh sebagai berikut :
 
```css
* {
  color: purple;
}
```

## Type Selector

Type Selector adalah selector yang berupa element dari html itu sendiri seperti \<p>, \<div>, \<h1>. Bisa dilihat contoh sebagai berikut :

```
<!-- index.html -->

<div>Hello, World!</div>
<div>Hello again!</div>
<p>Hi...</p>
<div>Okay, bye.</div>
```

```
/* styles.css */

div {
  color: white;
}
```

Disini bisa dilihat bahwa element \<div> akan mendapatkan warna font white sedangkan element \<p> tidak.

## Class Selector

Class Selector adalah selector yang bisa kita gunakan untuk mengganti nama element. Biasanya case sensitive dan bisa digunakan untuk berbagai element. Bisa dilihat sebagai berikut:

```html
<body>
  <div class="container"> 
  ......
  </div>
  <p class="container">
  ......
  </p>
</body>
```

```CSS
.container {
  color: white;
  background-color: black;
}
```

Bisa dilihat dari gambar diatas bahwa class "container" dari tag \<div> bisa menjadi selector [[CSS]]. Class Selector juga bisa dipakai 2 kali dalam tag html. Multi Class Selector juga bisa dipakai didalam tag html. Contoh seperti berikut :

```html
<body>
  <div class="container"> 
  ......
  </div>
  <p class="container paragraph">
  ......
  </p>
</body>
```
```CSS
.container {
  color: white;
  background-color: black;
}

.paragraph {
  font-size: 12px;
}
```

dari gambar diatas, bisa dilihat 2 class diapply kan dalam 1 element html. Class seperti ```class="alert-text severe-alert"``` juga bisa diaplikasikan.

## ID Selector

ID Selector sebenarnya memiliki fungsi yang hampir sama dengan Class Selector, yaitu sama sama menggantikan atau mengaliaskan suatu element html. Tetapi ID Selector lebih strict dengan berbagai ketentuan sebagai berikut: 
- ID Selector tidak bisa diduplikasi untuk memberi 2 element html. Contohnya :
```html
<body>
  <p id="title">.....</p>
  <p id="title">.....</p>
</body>
```
- ID Selector tidak bisa memiliki whitespace.
```html
<body>
  <p id="title subtitle">.....</p>
</body>
```
- Daripada menggunakan \. (arterisk), ID Selector menggunakan \#.
```html
<body>
  <p id="title">.....</p>
</body>
```

```CSS
#title {
  color: white;
}
```

Sebenarnya Class Selector sudah cukup untuk membuat referensi, tidak perlu memakai ID Selector. ID Selector biasanya digunakan untuk situasi yang memang penting untuk memakainya seperti dalam hal "Specificity" (Hirarki Kepentingan Selector), Maka dalam hal ini ID Selector memang tinggi hirarkinya daripada Class Selector. 

## Grouping Selectors

Bagaimana cara mendeklarasikan apabila kita mempunyai 2 elements yang mempunyai "beberapa" style yang sama ? Biasanya kita menulis nya sebagai berikut:

```html
<body>
  <h1 class="h1-container">...</h1>
  <h2 class="h2-container">...</h2>
</body
```

```CSS
.h1-container {
  color: white;
  background-color: black;
  /* beberapa style lain yang unique*/
}

.h2-container {
  color: white;
  background-color: black;
  /* beberapa style lain yang unique*/
}
```

```.h1-container``` dan ```.h2-container``` sama sama memiliki beberapa style yang sama seperti ```color: white;``` dan ```background-color: black;``` tetapi hal ini hanya memperpanjang kodingan. Cara untuk mempersingkat dan membuatnya lebih rapi adalah dengan cara menggrupkan selector seperti berikut:

```css
.h1-container,
.h2-container {
  color: white;
  background-color: black;
  /* beberapa style lain yang unique*/
}

.h1-container {
  /* beberapa style lain yang unique*/
}

.h2-container {
  /* beberapa style lain yang unique*/
}
```

Cara diatas sangat efisien dan berguna dan sering di aplikasi kan dalam membuat [[CSS]].

## Chaining Selectors

Another way to use selectors is to chain them as a list without any separation. Let’s say we had the following HTML:

```html
<div>
  <div class="subsection header">Latest Posts</div>
  <p class="subsection preview">This is where a preview for a post might go.</p>
</div>
```

We have two elements with the `subsection` class that have some sort of unique styles, but what if we only want to apply a separate rule to the element that also has `header` as a second class? Well, we could chain both the class selectors together in our [[CSS]] like so:

```css
.subsection.header {
  color: red;
}
```

What `.subsection.header` does is it selects any element that has both the `subsection` _and_ `header` classes. Notice how there isn’t any space between the `.subsection` and `.header` class selectors. This syntax basically works for chaining any combination of selectors, except for chaining more than one [type selector](https://www.theodinproject.com/lessons/foundations-css-foundations#type-selectors).

This can also be used to chain a class and an ID, as shown below:

```html
<div>
  <div class="subsection header">Latest Posts</div>
  <p class="subsection" id="preview">This is where a preview for a post might go.</p>
</div>
```

You can take the two elements above and combine them with the following:

```css
.subsection.header {
  color: red;
}

.subsection#preview {
  color: blue;
}
```

In general, you can’t chain more than one type selector since an element can’t be two different types at once. For example, chaining two type selectors like `div` and `p` would give us the selector `divp`, which wouldn’t work since the selector would try to find a literal `<divp>` element, which doesn’t exist.


























