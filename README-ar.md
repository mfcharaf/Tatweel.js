# مكتبة Tatweel.js
A Javascript library to stretch Arabic words in a proper way.

# لماذا يجب أن أستخدم tatweel.js ?
كما تعلم جيدا، في CSS، تتحكم خاصية `letter-spacing` في كمية المسافة بين كل حرف في عنصر معين أو كتلة نص.
ولكن مع النصوص العربية، يمكن أن يسبب هذا مشكلة، لأن النص العربي دائمًا مكتوبًا بحيث تكون الأحرف متصلة ببعضها البعض، مثل هذا النص: ```مرحبا بك``` هذه الخاصية في CSS تجعل النص يبدو أقل ملاءمة، وأحيانا صعب القراءة، وصعب التمييز بين الكلمات. سيبدو شيئا مشابها لهذا: ```مـ ر حـ ب ا بـ ك```.

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

# More examples
For arabic documentations and more examples [click here](#).