# Tatweel.js
A Javascript library to stretch Arabic words in a proper way.

## Why should I use tatweel.js ?
As you should know, in CSS the `letter-spacing` property controls the amount of space between each letter in a given element or block of text.
But with arabic texts this may cause an issue, because arabic text is always written where letters are attached to eachother, like this one ***مرحبا بك*** this CSS property makes the text look less conviniant, and some times hard to read, and distunguish between words. It will look like something like this ***مـ ر حـ ب ا بـ ك***.

This where our *Tatweel.JS* library becomes handy, It was created to replace the `letter-spacing` CSS property, it gives a proper spacing between letters for arabic text.
```
مرحبا بك
مــرحــبــا بــك 
مــرحـــبـــا بـــك
مـــرحــــبــــا بــــك
```