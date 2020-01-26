<div dir="rtl">

# دليل المبتدئين لإستعمال الشبكة البرقية لديكريد (DCR)

![](https://miro.medium.com/max/1280/1*wQWOA9X22Hv6qXZpO0aKlA.png)

_دليل اختبار الشبكة البرقية لديكريد ([dcrlnd](https://github.com/decred/dcrlnd)) للمبتدئين._

تم تصميم الشبكة البرقية (LN) في الأصل لجعل المعاملات الدقيقة سريعة ورخيصة على البتكوين ممكنة. وتقوم هذه التقنية بتغيير سعة معالجة المعاملات من BTC إلى معاملات لا نهائية تقريبًا في الثانية نظرًا لأنها تمثل حل طبقة ثانية. ولحسن الحظ، يمكن تنفيذ الشبكة البرقية على قمة سلاسل الكتل أيضًا. و ديكريد أول من تقوم بذلك.

سيوضح لك هذا الدليل كيفية استخدام الشبكة البرقية على شبكة إختبار ديكريد. إن الاختبار مهم لتصفية الأخطاء الأخيرة ومن المفيد لأي شخص يريد تجربة هذه التقنية الجديدة من دون المخاطرة بأموال حقيقية.

إذا كان لديك أي أسئلة، انضم إلى [غرف دردشة](https://www.decred.org/community/) ديكريد!

الخطوات الواجب اتخاذها:

**1. يجب تثبيت ديكريديتون**

* [decred.org/wallets](https://decred.org/wallets/)
* إذا كنت قد قمت بتثبيت ديكريديتون، فتحقق مما إذا كان لديك أحدث إصدار (وهو 1.5 في وقت الكتابة)

**2. تعديل ملف الإعدادات لتعيين "ln\_enabled" على "true"**

* تأكد من إغلاق محفظة ديكريديتون
* ابحث عن ملف الإعدادات في مجلد ديكريديتون. يعتمد موقع ملف الإعدادات على نظام التشغيل: [docs.decred.org/wallets/decrediton/decrediton-troubleshooting/#location-of-data-and-log-files](https://docs.decred.org/wallets/decrediton/decrediton-troubleshooting/#location-of-data-and-log-files)
* افتح ملف الإعدادات باستخدام محرر نصوص
* قم بتغيير إعداد `ln\_enabled` إلى `true`

**3. تعديل ملف الإعدادات للإنتقال إلى شبكة الإختبار**

* في نفس ملف الإعدادات، بدّل `network` إلى `testnet`

**4. قم بإنشاء محفظة testnet واتركها متزامنة (لا يوجد تحقق بسيط للدفع)**

* إفتح ديكريديتون وقم بإنشاء (أو استعادة) محفظة اختبار كاملة
* أثناء انتظار المزامنة، انتقل إلى قراءة بعض [القصص المصورة](https://dcrcomic.org/)

**5. افتح محفظتك واحصل على عملات إختبار DCR مجانية**

* سيعطيك موقع [faucet.decred.org ](https://faucet.decred.org/) عملات إختبار DCR مجانية

**6. إنشاء محفظة DCRLND جديدة**

* إذا قمت بالخطوة 2 بشكل صحيح، يمكنك الوصول إلى قائمة "الشبكة البرقية" من محفظتك لإنشاء محفظة جديدة للشبكة البرقية

![](https://miro.medium.com/max/1475/1*kEfWAZHbLlTJD6W4hOqFzg.png)

* حدد ما إذا كنت تريد القيادة الآلية (غير ضرورية لهذا الدليل)
* انقر فوق “Start And Unlock LN Wallet”

![](https://miro.medium.com/max/1026/1*wvCzO_lgWpIxUPlXkE1eAQ.png)

* إنتقل إلى قائمة “Accounts”

![](https://miro.medium.com/max/1685/1*0AYZL3WvHiPNckfBvtPsDQ.png)

* يجب أن يظهر حساب الشبكة البرقية الجديد الخاص بك

**7. إرسال عملات DCR الإختبارية من الحساب الافتراضي إلى حساب الشبكة البرقية**

لاستخدام محفظة الشبكة البرقية، يجب أن يكون لديك أموال فيها.

* انتقل إلى قائمة "Transactions"
* في علامة التبويب "Send"، انقر فوق الرمز المجاور لحقل "From"

![](https://miro.medium.com/max/1144/0*rOuDJuka8X52YhBo)

* حدد حساب الشبكة البرقية الجديد في الحقل إلى "To"

![](https://miro.medium.com/max/1173/1*X1OnibaXbIQK2w5-nDF25A.png)

* انقل مبلغًا صغيرًا لفتح بعض القنوات
* ارجع إلى قائمة "Lightning Network"
* انتظر التأكيد

![](https://miro.medium.com/max/1494/1*FbIyChOXwVBDyeIMMWm8cg.png)

* تهانينا، أنت الآن جاهز لفتح القنوات ✅

**8أ. فتح القنوات بصنبور الشبكة البرقية على شبكة الاختبار**

* انتقل إلى علامة التبويب "Channels" في قائمة "Lightning Network"

![](https://miro.medium.com/max/1714/1*SXqfLXBUmWJk0LRIRWa2UA.png)

* إنتقل إلى أحد صنابير الشبكة البرقية على شبكة الاختبار:
  * مثال: [testnet-dcrln-01.matheusd.com](https://testnet-dcrln-01.matheusd.com/)
  * البديل: [testnet-dcrln-01.davec.name](https://testnet-dcrln-01.davec.name/)
* قم بالنزول إلى الأسفل

![](https://miro.medium.com/max/1498/1*rFKyt-4AFu9JK-ZFlQxQUg.png)

* انسخ بيانات (node@ip:port) الموضحة أعلاه
* ارجع إلى محفظة ديكريديتون الخاصة بك
* الصق البيانات في حقل "Counterparty"

![](https://miro.medium.com/max/1733/1*0A5Gv7A941P8ERoAfuS-Hw.png)

* حدد مقدار الحجم الذي يجب أن تكون عليه القناة
* يتيح لك خيار "Push Amount" إرسال بعض DCR إلى الطرف الآخر حتى تتمكن من استلامها مرة أخرى كمدفوعات لاختبار القناة. وهو في الأساس **هدية** إلى الطرف البعيد لاختبار كل الوظائف
* انقر فوق "Open" وانتظر التأكيد
* بعد التأكيد، ستظهر القناة المعلّقة على أنها مفتوحة
* يمكنك أيضًا عرض حالة القناة على صفحة صنبور الشبكة البرقية

**8ب. فتح قنوات مع عقد الشبكة البرقية الأخرى**

* انتقل إلى علامة التبويب "Channels" في قائمة "Lightning Network"
* انتقل إلى خريطة شبكة الإختبار للشبكة البرقية: [ln-map-testnet.jamieholdstock.com](https://ln-map-testnet.jamieholdstock.com/)
* اختر عقدة يمكن الوصول إليها تريد الاتصال بها
* (قد تظهر العقدة أحيانًا كقابلة للوصول، بينما لا تستجيب عقدة dcrlnd الأساسية بسبب مشكلة ما)

![](https://miro.medium.com/max/1200/1*GcqTVz_81lz_gGq4mXDJRw.png)

* ابحث عن "Pubkey" و "Addresses" العقدة
* عد إلى محفظة ديكريديتون الخاصة بك
* أدخل `Pubkey@Addresses` في حقل "Counterparty"

![](https://miro.medium.com/max/1746/1*zkX0n_68LnJJjJ933pO5TA.png)

* حدد مقدار الحجم الذي يجب أن تكون عليه القناة
* يتيح لك خيار "Push Amount" إرسال بعض DCR إلى الطرف الآخر حتى تتمكن من استلامها مرة أخرى كمدفوعات لاختبار القناة. وهو في الأساس **هدية** إلى الطرف البعيد لاختبار كل الوظائف
* انقر فوق "Open" وانتظر التأكيد
* بعد التأكيد، ستظهر القناة المعلّقة على أنها مفتوحة
* يمكنك أيضًا عرض حالة القناة على [خريطة شبكة الإختبار للشبكة البرقية](https://ln-map-testnet.jamieholdstock.com/)

**9. أغلق القنوات من محفظتك**

* انتقل إلى علامة التبويب "Channels" في قائمة "Lightning Network"
* انقر فوق علامة التقاطع في الزاوية العلوية اليمنى للقناة المفتوحة
* انقر على "Confirm" وانتظر التأكيد

![](https://miro.medium.com/max/1273/1*4vHZtYH64f66Z3kCTX7xkQ.png)

**10أ. كيفية إنشاء فواتير الشبكة البرقية**

لاستلام القيمة على الشبكة البرقية (داخل قناة أو عبر خطوات)، يجب إنشاء فاتورة. يمكن دفع كل فاتورة مرة واحدة فقط.

* انتقل إلى علامة التبويب "Invoices" في قائمة "Lightning Network"

![](https://miro.medium.com/max/1284/1*nrFwG7heQMHeiUHEXxbsxA.png)

* أضف الوصف المناسب
* اطلب قيمة بحد أقصى 0.00001 DCR
(ينطبق الحد الأقصى على فواتير الصنابير فقط)
* انقر فوق علامة الجمع الزرقاء
* انسخ كود الفاتورة

**اختياري: اسمح لصنبور الشبكة البرقية بدفع فاتورتك**

عند تبادل القيمة مع عقد الشبكة البرقية أخرى (الخطوة 8ب)، يمكنك ببساطة إرسال كود الفاتورة عبر الدردشة. ويمكن للطرف الآخر بعد ذلك دفع الفاتورة (الخطوة 10ب). إذا كنت تختبر الأشياء بمفردك، فاستخدم الشبكة البرقية لدفع الفواتير.

* انتقل إلى أحد صنابير الشبكة البرقية على شبكة الاختبار:
  مثال: [testnet-dcrln-01.matheusd.com](https://testnet-dcrln-01.matheusd.com/)
  البديل: [testnet-dcrln-01.davec.name](https://testnet-dcrln-01.davec.name/)
* أنزل للأسفل إلى قسم "Pay Invoice"
* الصق كود الفاتورة في حقل "Invoice code"

![](https://miro.medium.com/max/1705/1*GIWAlLKhV5MGEnpvFjdlww.png)

* انقر فوق "Pay Invoice" ✅
* يجب أن تظهر الفاتورة المدفوعة في قسم "Latest Invoices"

**اختياري: إنشاء فواتير باستخدام صنبور الشبكة البرقية**

عند تبادل القيمة مع عقد أخرى بواسطة الشبكة البرقية (الخطوة 8ب)، ستتلقى كود الفواتير الخاصة بها. يمكنك بعد ذلك اتباع الخطوات أدناه في 10ب. إذا كنت تختبر الأشياء بمفردك، فاستخدم الصنبور الخاص بالشبكة البرقية لإنشاء فواتير صالحة.

* انتقل إلى أحد صنابير الشبكة البرقية على شبكة الاختبار:
  * مثال: [testnet-dcrln-01.matheusd.com](https://testnet-dcrln-01.matheusd.com/)
  * البديل: [testnet-dcrln-01.davec.name](https://testnet-dcrln-01.davec.name/)
* أنزل للأسفل إلى قسم "Generate Invoice"
* أضف وصفا مناسبا
* اختر مبلغ الفاتورة

![](https://miro.medium.com/max/1709/1*h62IZ61-XWOsFxeLJ1At8g.png)

* أنقر على "Generate Invoice"
* انسخ كود الفاتورة

**10ب. كيفية إرسال مدفوعات بواسطة الشبكة البرقية**

لإرسال الدفعات عبر الشبكة البرقية (ضمن قناة أو عبر خطوات)، يجب أن تطلب من الطرف الآخر فاتورة صالحة. يمكن دفع كل فاتورة مرة واحدة فقط.

* انتقل إلى علامة التبويب "Payments" في قائمة "Lightning Network"
* الصق كود الفاتورة في حقل "Payment Request"
* ستظهر تفاصيل الفاتورة تلقائيًا

![](https://miro.medium.com/max/1276/1*9jDgiDjZX-uE45RfZYrckQ.png)

* انقر فوق "Send" ✅
* يجب أن تظهر الدفعة في قسم "Latest Payments"

## الملاحظات النهائية

يجب أن تكون لديك الآن فكرة عن أساسيات الشبكة البرقية. من المحتمل أن تتغير واجهة المستخدم الخاصة بضيچريديتون في المستقبل، ولكن المفاهيم الأساسية ستبقى كما هي.

شكرًا لمساعدتنا في اختبار الشبكة البرقية لديكريد وتذكّر إرسال عملات DCR الإختبارية مرة أخرى [إلى الصنبور](https://faucet.decred.org/) بعد الانتهاء!

إذا كنت ترغب في إنشاء دليل تعليمي لسطر الأوامر، [فاقرأ هذا المنشور](https://github.com/fguisso/dcrlnd/blob/78a411ceb27f423166f419d930c9eb370b629745/docker/README.md) بواسطة مطور ديكريد fguisso وراجع [وثائق dcrlnd](https://github.com/decred/dcrlnd/blob/master/docs/QUICKSTART.md).

إذا أردت معرفة المزيد حول الشبكة البرقية، شاهد مقاطع الفيديو التالية:

[![LN - How does it work?](https://res.cloudinary.com/marcomontalbano/image/upload/v1579814820/video_to_markdown/images/youtube--QzY27b2REwg-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/QzY27b2REwg "LN - How does it work?")

_تستكشف هذه الحلقة الأعمال الداخلية للشبكة البرقية_

[![Deep Dive - LN](https://res.cloudinary.com/marcomontalbano/image/upload/v1579814988/video_to_markdown/images/youtube--N3WO5YXpD7M-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/N3WO5YXpD7M "Deep Dive - LN")

_يتحدث مطور ديكريد عن الحالة الحالية للشبكة البرقية_

رابط النص الأصلي: [Beginner guide to the Decred (DCR) Lightning Network](https://medium.com/decred/beginner-guide-to-the-decred-dcr-lightning-network-917f8ad304aa) بقلم Noah Piereau

تمت الترجمة إلى اللغة العربية بواسطة: arij@، قام بالمراجعة abdulrahman4@.

</div>
