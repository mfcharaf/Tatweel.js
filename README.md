<p align="left"> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="20" height="20"/> </a> </p>

# Tatweel.js
A Javascript library to stretch Arabic words in a proper way.

# Why should I use tatweel.js ?
As you should know, in CSS the `letter-spacing` property controls the amount of space between each letter in a given element or block of text.
But with arabic texts this may cause an issue, because arabic text is always written where letters are attached to eachother, like this one ```مرحبا بك``` This CSS property makes the text look less conviniant, and some times hard to read, and distunguish between words. It will look like something like this ```مـ ر حـ ب ا بـ ك```.

This where our *TatweelJS* library becomes handy, It was created to replace the `letter-spacing` CSS property, it gives a proper spacing between letters for arabic text.

The arabic text is actually stretched by using the 'ـ' character and not an actual space, so we prefer to call it *stretching* and not *spacing*.

<img src="https://github.com/mfcharaf/Tatweel.js/blob/main/img/1.png" width="200" />


```
مرحبا بك
مــرحــبــا بــك 
مــرحـــبـــا بـــك
مـــرحــــبــــا بــــك
```

# How to use tatweel.js ?
## Installation
To use TatweelJS in your project, simply just call the `tatweel.js` file in your HTML code 
```js
<script type="text/javascript" src="../js/tatweel.js"></script>
```
## Simple usage
To apply the stretching to your text, just add the `tatweel` class name to your html element.
```html
<span class="tatweel">مرحبا بك</span>
```
Output:
```
مـــرحـــبـــا بـــك
```
## Add more stretching
As you notice the default stretching value is 3 (ـــ).
To change that you can also add the `tw-*` class name (eg., <code>.tw-1</code> <code>.tw-2</code> <code>.tw-3</code> )
```html
<span class="tatweel tw-1">مرحبا بك</span>
<span class="tatweel tw-2">مرحبا بك</span>
<span class="tatweel tw-3">مرحبا بك</span>
<span class="tatweel tw-5">مرحبا بك</span>
```
Output:
```
مـرحـبـا بـك 
مــرحــبــا بــك 
مـــرحـــبـــا بـــك 
مـــــرحـــــبـــــا بـــــك 
```
## Apply stretching to child elements
By default, tatweel.js only works with the text inside the element, any text inside its child elements will not be affected.<br>
To apply stretching on child elements just add the `tw-childs` class name, this will affect any text inside the elements and its child elements.

**Example 01 : Not including child elements**
```html
<div class="tatweel tw-5">
     مرحبا بك
     <br>
     <span>أهلا وسهلا</span>
</div>
```
Output:
```
مـــــرحـــــبـــــا بـــــك
أهلا وسهلا
```

**Example 02 : Including child elements**
```html
<div class="tatweel tw-childs tw-5">
     مرحبا بك
     <br>
     <span>أهلا وسهلا</span>
</div>
```
Output:
```
مـــــرحـــــبـــــا بـــــك 
أهـــــلا وســـــهـــــلا
```