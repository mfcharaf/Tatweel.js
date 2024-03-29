# مكتبة Tatweel.js
A Javascript library to stretch Arabic words in a proper way.

# لماذا يجب أن أستخدم tatweel.js ?
كما يعلم الحميع أنه في لغة 
CSS،
 تتحكم خاصية 
 `letter-spacing`
  في كمية المسافة بين كل حرف في أي نص داخل عنصر معين.
ولكن مع النصوص العربية، يمكن أن يسبب هذا مشكلة،
 لأن النص العربي يكون دائما مكتوبا بشكل حيث تكون الأحرف متصلة ببعضها البعض، مثل هذا النص:
 ```مرحبا بك``` 
هذه الخاصية في 
CSS
 تجعل النص يبدو أقل ملاءمة، وأحيانا صعب القراءة،
  ويصعب التمييز بين الكلمات. سيبدو شيئا مشابها لهذا:
   ```مـ ر حـ ب ا بـ ك```.

لهذا الغرض تم تطوير مكتبة  *TatweelJS* , فلقد تم انشاؤها لتحل محل `letter-spacing` في لغة الـ CSS , بحيث توفر تباعدًا مناسبًا بين الحروف لنصوص اللغة العربية.

النص العربي يتم تمدده فعليًا باستخدام الحرف 'ـ' وليس باستخدام مسافة فعلية، لذا نفضل أن نسميه *تطويلا* بدلاً من *تباعد - spacing*.
<img src="https://github.com/mfcharaf/Tatweel.js/blob/main/img/1.png" width="200" />


```
مرحبا بك
مــرحــبــا بــك 
مــرحـــبـــا بـــك
مـــرحــــبــــا بــــك
```


# كيفية استخدام tatweel.js ؟
## التثبيت
لاستخدام TatweelJS في مشروعك، ما عليك سوى استدعاء ملف tatweel.js في كود HTML الخاص بك.
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
For arabic documentations and more examples [click here](https://github.com/mfcharaf/Tatweel.js/blob/main/README-ar.md).
