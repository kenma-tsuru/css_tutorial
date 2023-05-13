# Exercise 2

## Coding

1. กำหนด `index1.html` และ `css1.css` จง apply css จากไฟล์ `css1.css` ให้กับไฟล์ `index1.html` โดยใช้วิธี external stylesheet
2. กำหนด `index2.html` และ `css2.css` จง**ใช้ข้อมูล**จากไฟล์ `css2.css` เพื่อกำหนด style ให้กับไฟล์ `index2.html` โดยใช้วิธี internal stylesheet


## Short Answer
1. กำหนด css และ html ดังต่อไปนี้ จงหาว่าข้อความภายใต้ h1 เป็นสีอะไร และเป็นไปตามกฎข้อใด (cascading/specificity) และเพราะเหตุใด

```html
<div class="box">
  <h1 class="text">Hello, world!</p>
</div>
```
```css
h1 {
  color: red;
}

div h1 {
  color: blue;
}
```
2. กำหนด css และ html ดังต่อไปนี้ จงหาว่าข้อความภายใต้ p เป็นสีอะไร และเป็นไปตามกฎข้อใด (cascading/specificity) และเพราะเหตุใด

```html
<div class="box">
  <p class="text">Hello, world!</p>
</div>

```
```css
.box p {
  color: red;
}

p.text {
  color: blue;
}

```
3. กำหนด css และ html ดังต่อไปนี้ จงหาว่าข้อความภายใต้ p เป็นสีอะไร และเป็นไปตามกฎข้อใด (cascading/specificity) และเพราะเหตุใด

```html
<div class="box">
  <p>Hello, world!</p>
</div>
```
```css
p {
  color: red;
}

.box p {
  color: blue;
}
```
4. กำหนด css และ html ดังต่อไปนี้ จงหาว่าข้อความภายใต้ p เป็นสีอะไร และเป็นไปตามกฎข้อใด (cascading/specificity) และเพราะเหตุใด

```html
<div class="box">
  <p>Hello, world!</p>
</div>


```
```css
p {
  color: red;
}

.box {
  color: blue;
}
```


```
5. (คะแนนพิเศษ) กำหนด css และ html ดังต่อไปนี้ จงหาว่าข้อความภายใต้ p เป็นสีอะไร และเป็นไปตามกฎข้อใด (cascading/specificity) และเพราะเหตุใด

```html
<div id="wrapper">
  <p class="text">Hello, world!</p>
</div>

```
```css
#wrapper .text {
  color: red;
}

div p {
  color: blue;
}

```
