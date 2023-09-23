<p align="left"> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="20" height="20"/> </a> </p>

# Tatweel.js
A Javascript library to stretch Arabic words in a proper way.

## Why should I use tatweel.js ?
As you should know, in CSS the `letter-spacing` property controls the amount of space between each letter in a given element or block of text.
But with arabic texts this may cause an issue, because arabic text is always written where letters are attached to eachother, like this one ```مرحبا بك``` This CSS property makes the text look less conviniant, and some times hard to read, and distunguish between words. It will look like something like this ```مـ ر حـ ب ا بـ ك```.

This where our *TatweelJS* library becomes handy, It was created to replace the `letter-spacing` CSS property, it gives a proper spacing between letters for arabic text.

The arabic text is actually stretched by using the 'ـ' character and not an actual space, so we prefer to call it *stretching* and not *spacing*.
```
مرحبا بك
مــرحــبــا بــك 
مــرحـــبـــا بـــك
مـــرحــــبــــا بــــك
```

## How to use tatweel.js ?
To use TatweelJS in your project, simply just call the `tatweel.js` file in your HTML code 
```js
<script type="text/javascript" src="../js/tatweel.js"></script>
```
To apply the stretching to your text, just add the `tatweel` class name to your html element.
```html
<span class="tatweel">مرحبا بك</span>
```
Output:<br>مـــرحـــبـــا بـــك

As you notice the default stretching value is 3 (ـــ).
To change that you can also add the `tw-*` class name (eg., <code>.tw-1</code> <code>.tw-2</code> <code>.tw-3</code> )
```html
<span class="tatweel tw-1">مرحبا بك</span>
<span class="tatweel tw-2">مرحبا بك</span>
<span class="tatweel tw-3">مرحبا بك</span>
<span class="tatweel tw-5">مرحبا بك</span>
```
Output:<br>
مـرحـبـا بـك <br>
مــرحــبــا بــك <br>
مـــرحـــبـــا بـــك <br>
مـــــرحـــــبـــــا بـــــك <br>