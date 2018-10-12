---
title: Logistic Regression
localeTitle: الانحدار اللوجستي
---
## الانحدار اللوجستي

![وظيفة لوجيستية](https://qph.fs.quoracdn.net/main-qimg-7c9b7670c90b286160a88cb599d1b733) الانحدار اللوجستي يشبه إلى حد كبير الانحدار الخطي في أنه يحاول التنبؤ بمتغير الاستجابة Y مع مجموعة من متغيرات الإدخال X. إنه شكل من أشكال التعلم الخاضع للإشراف ، والذي يحاول التنبؤ باستجابات البيانات غير المعلنة وغير المرئية عن طريق التدريب الأول مع البيانات المسمى ، ومجموعة من الملاحظات لكل من المتغيرات المستقلة (X) والمتغيرات التابعة (Y). ولكن بينما يفترض [الانحدار الخطي](https://guide.freecodecamp.org/machine-learning/linear-regression) أن متغير الاستجابة (Y) يكون كمياً أو متواصلاً ، فإن الانحدار اللوجستي يستخدم على وجه التحديد عندما يكون متغير الاستجابة نوعياً أو منفصلاً. ![الخطية مقابل اللوجستي](http://www.saedsayad.com/images/LogReg_1.png)

#### كيف تعمل

نماذج الانحدار اللوجستي من المحتمل أن Y ، متغير الاستجابة ، ينتمي إلى فئة معينة. في كثير من الحالات ، يكون متغير الاستجابة عبارة عن متغير ثنائي ، لذا فإن الانحدار اللوجستي سيحتاج إلى نموذج دالة y = f (x) التي تخرج قيمة عادية تتراوح من 0 إلى 1 على سبيل المثال لجميع قيم X ، المقابلة القيمتين الممكنة لـ Y. وهي تقوم بذلك باستخدام الدالة اللوجيستية: الانحدار اللوجستي هو تحليل الانحدار المناسب لإجراء عندما يكون المتغير التابع ثنائي التفرع (ثنائي). مثل جميع التحليلات الانحدار ، الانحدار اللوجستي هو تحليل تنبؤي. يستخدم الانحدار اللوجستي لوصف البيانات ولشرح العلاقة بين متغير ثنائي تابع واحد ومتغير واحد أو أكثر من المتغيرات المستقلة الاسمية أو الترتيبية أو الفاصلة أو على مستوى النسبة.

![دالة التكلفه](https://cdn-images-1.medium.com/max/800/1*wHtYmENzug_W6fIE9xY8aw.jpeg) يستخدم الانحدار اللوجستي لحل مشاكل التصنيف ، حيث يكون الناتج من النموذج y∈ {0،1}. هنا ، 0 هو فئة سالبة و 1 فئة موجبة. لنفترض أن لدينا فرضية hθ (x) ، حيث x هي مجموعة البيانات لدينا (مصفوفة) للطول m. θ هي مصفوفة parameteric. لدينا: 0 <hθ (x) <1

في الانحدار اللوجستي ، hθ (x) هي دالة sigmoid ، وبالتالي hθ (x) = g (θ'x). g (θ'x) = 1/1 + e ^ (- θ'x)

ملحوظة: θ 'is θ transpose.

#### دالة التكلفه

دالة التكلفة المستخدمة للانحدار اللوجستي هي:

J (θ) = (1 / m) ∑Cost (hθ (x (i))، y (i)) ، حيث يكون التجميع من i = 1 إلى m.

التكلفة (hθ (x)، y) = - log (hθ (x)) إذا كان y = 1 التكلفة (hθ (x)، y) = - log (1 − hθ (x)) if y = 0

#### التنبؤات باستخدام الانحدار اللوجستي:

نماذج الانحدار اللوجستي احتمال الطبقة الافتراضية (أي الطبقة الأولى). يمكنك تصنيف النتائج المقدمة بواسطة:

y = e ^ (b0 + b1 _X) / (1 + e ^ (b0 + b1_ X))

يتم تعيين 0.5 كاختيار حد السدادة التي يتم تصنيف y≥0.5 لها كالفئة A والتي تم تصنيف y <0.5 لها كالفئة ب.

#### الانحدار اللوجستي متعدد الطبقات:

على الرغم من أنك سترى أن الانحدار اللوجستي يتم استخدامه عادة في حالة التصنيف الثنائي ولكن يمكنك استخدامه أيضًا في حالة التصنيف إلى فئات متعددة من خلال:

##### طريقة واحدة مقابل واحدة:

هنا يتم إنشاء مصنف لكل فصل على حدة ويعتبر المصنف الذي يحصل على أعلى درجة كمخرج.

##### واحد مقابل كل طريقة:

هنا متعددة (N \* N (N-1) / 2 حيث N = لا. من الطبقات) المصنوعات الثنائية تتم ثم من خلال مقارنة درجاتهم يتم الحصول على الإخراج.

#### تطبيقات الانحدار اللوجستي:

1) لتصنيف البريد كرسائل غير مرغوب فيها أو ليست رسائل غير مرغوب فيها. 2) لتحديد وجود أو عدم وجود مرض معين مثل السرطان على أساس الأعراض والبيانات الطبية الأخرى. 3) تصنيف الصور على أساس بيانات البكسل.

#### افتراضات الانحدار اللوجستي

يتطلب الانحدار اللوجستي الثنائي أن يكون المتغير التابع ثنائيًا. بالنسبة إلى الانحدار الثنائي ، ينبغي أن يمثل عامل المستوى 1 للمتغير التابع النتيجة المرجوة. يجب تضمين المتغيرات ذات المعنى فقط. يجب أن تكون المتغيرات المستقلة مستقلة عن بعضها البعض. بمعنى ، يجب أن يكون النموذج قليلة أو لا. ترتبط المتغيرات المستقلة خطيًا باحتمالات السجل. الانحدار اللوجستي يتطلب أحجام عينة كبيرة جدا.

#### معلومات اكثر:

لمزيد من القراءة لبناء خطوة الانحدار اللوجستي بخطوة:

*   انقر [هنا](https://medium.com/towards-data-science/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8) لمقال عن بناء الانحدار اللوجستي في بيثون.
*   انقر [هنا](http://nbviewer.jupyter.org/gist/justmarkham/6d5c061ca5aee67c4316471f8c2ae976) لمقال آخر حول بناء الانحدار المنطقي.
*   انقر [هنا](http://nbviewer.jupyter.org/gist/justmarkham/6d5c061ca5aee67c4316471f8c2ae976) لمقال آخر حول الرياضيات والحدس وراء الانحدار المنطقي.