# مكتبة Tatweel.js
مكتبة جافاسكريبت لتمديد الكلمات العربية بشكل لائق.

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
## طريقة الإستخدام
لتطبيق التمديد على نصك، ما عليك سوى إضافة اسم الفئة (كلاس) `tatweel` إلى عنصر HTML الخاص بك.
```html
<span class="tatweel">مرحبا بك</span>
```
النتيجة:
```
مـــرحـــبـــا بـــك
```
## إضافة المزيد من التمديد  
كما تلاحظ، فإن قيمة التمديد الافتراضية هي 3 (ـــ).  
لتغيير ذلك، يمكنك أيضًا إضافة اسم الفئة `tw-*` (على سبيل المثال، <code>.tw-1</code> <code>.tw-2</code> <code>.tw-3</code>).
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
## تطبيق التمديد على العناصر الفرعية  
بشكل افتراضي، يعمل **tatweel.js** فقط مع النص داخل العنصر نفسه، وأي نص داخل عناصره الفرعية لن يتأثر.<br>  
لتطبيق التمديد على العناصر الفرعية، ما عليك سوى إضافة اسم الفئة `tw-childs`، وسيؤثر ذلك على أي نص داخل العنصر وعناصره الفرعية.  

**مثال 01: بدون تضمين العناصر الفرعية**
```html
<div class="tatweel tw-5">
     مرحبا بك
     <br>
     <span>أهلا وسهلا</span>
</div>
```
النتيجة:
```
مـــــرحـــــبـــــا بـــــك
أهلا وسهلا
```

**مثال 02: تضمين العناصر الفرعية**
```html
<div class="tatweel tw-childs tw-5">
     مرحبا بك
     <br>
     <span>أهلا وسهلا</span>
</div>
```
النتيجة:
```
مـــــرحـــــبـــــا بـــــك 
أهـــــلا وســـــهـــــلا
```

# المزيد من الأمثلة  
للاطلاع على التوثيق باللغة الإنجليزية ومزيد من الأمثلة [إضغط هنا](https://github.com/mfcharaf/Tatweel.js/).
