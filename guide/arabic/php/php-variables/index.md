---
title: PHP Variables
localeTitle: متغيرات PHP
---
## المتغيرات

المتغيرات هي "حاويات" لتخزين المعلومات. يتم الإعلان عن المتغيرات باستخدام علامة الدولار ($) متبوعة مباشرة باسم المتغير. على سبيل المثال ، سيعمل قالب التعليمة البرمجية أدناه على إنشاء متغير يسمى `myVariable` وتعيين سلسلة `Hello World` إليه.

```php
<?php
$myVariable = "Hello World";
$x = 5;
$y = 10.5;
$z = '42';
?>
``` 

بعد تنفيذ البيانات أعلاه، المتغير `$myVariable` سيعقد سلسلة مع قيمة أهلا بالعالم! المتغير `$x` سيعقدون صحيح بقيمة 5 و المتغير `$y` سيعقد تعويم بقيمة من 10.5 ، وسيحتوي المتغير `$z` على سلسلة بقيمة 42.

# تسمية المتغيرات

كما هو الحال مع أي لغة برمجة ، فإن PHP لديها قواعد معينة تنطبق على متغيرات التسمية. ستتبع أسماء المتغيرات الصالحة القواعد التالية

*   يجب أن يبدأ المتغير بالعلامة $ ، متبوعًا باسم المتغير
*   يجب أن يبدأ اسم المتغير بحرف أو حرف الشرطة السفلية
*   لا يمكن أن يبدأ اسم المتغير برقم
*   لا يمكن أن يحتوي اسم المتغير على أحرف أبجدية رقمية والشرطات السفلية (Az و 0-9 و \_)
*   أسماء المتغيرات حساسة لحالة الأحرف (عمر $ و $ AGE متغيرين مختلفين)

# المتغيرات المحددة مسبقا

يحتوي PHP على عدة كلمات رئيسية خاصة بينما تكون أسماء المتغيرات "الصالحة" ، لا يمكن استخدامها للمتغيرات الخاصة بك. والسبب في ذلك هو أن اللغة نفسها قد حددت بالفعل هذه المتغيرات وقد تم استخدامها لأغراض خاصة. يتم سرد العديد من الأمثلة أدناه ، للحصول على قائمة كاملة ، راجع [موقع وثائق PHP](https://secure.php.net/manual/en/language.variables.predefined.php) .

*   `$this`
*   `$_GET`
*   `$_POST`
*   `$_SERVER`
*   `$_FILES`

# تعيين قيم للمتغيرات

لتعيين قيمة لمتغير ، يمكنك ببساطة كتابة المتغير متبوعًا بمعامِل equals (=) متبوعًا بالقيمة. فمثلا

`PHP $myVariable = "Hello World"; $number1 = 5; $number2 = 10; $total = $number1 + $number2;`

ربما لاحظت عدة أشياء مهمة حول المثال أعلاه. أول متغير أعلنته مساويا لـ **Hello World** ، محاط بعلامات اقتباس. هذا لأن **Hello World** عبارة عن سلسلة من النص ويجب أن تكون سلاسل الأحرف محاطة بعلامات اقتباس. السطر الثاني الذي أعلنت عنه `$number1` مساوٍ لقيمة 5. كان بإمكاني الإعلان عن `$number1` ليكون مساوياً لـ `"5"` ، الأمر الذي من شأنه أن يخبر PHP أنني أريد تخزين 5 كسلسلة ، وليس قيمة فعلية. الفرق هو أنه لا يمكنك إجراء الحساب (كما فعلت في السطر الرابع) على السلاسل. السطر الرابع أعلن `$total` مساوٍ لقيم `$number1` بالإضافة إلى `$number2` . وهذا ما يسمى التصريح بقيمة حسب المرجع.

# PHP هي لغة مكتوبة بشكل فضفاض

في المثال أعلاه ، لاحظ أنه لم يكن علينا إخبار PHP بنوع البيانات المتغير. تقوم لغة PHP تلقائيًا بتحويل المتغير إلى نوع البيانات الصحيح ، وفقًا لقيمته. بلغات أخرى مثل C و C ++ و Java ، يجب أن يعلن المبرمج عن اسم المتغير ونوعه قبل استخدامه.

# استنتاج

تجعل PHP من السهل العمل مع المتغيرات ، ويجب عليك التفكير في المتغيرات كحاويات لتخزين المعلومات. لمزيد من المعلومات راجع هذه الموارد:

*   [PHP المتغيرات الوثائق](http://php.net/manual/en/language.variables.php)
*   [W3Schools متغيرات PHP](https://www.w3schools.com/php/php_variables.asp)
*   [أنواع البيانات PHP](https://guide.freecodecamp.org/php/data-types)