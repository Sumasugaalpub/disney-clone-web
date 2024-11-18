# نسخة محدثة من ديزني باستخدام React JS

![نسخة محدثة من ديزني باستخدام React JS](https://user-images.githubusercontent.com/71302066/201341087-e0d292e3-cc71-4691-b274-cb662b62da23.png "نسخة محدثة من ديزني باستخدام React JS")

## ⚠️ قبل أن تبدأ

1. تأكد من تثبيت **Git** و **NodeJS**.
2. قم بإنشاء ملف **firebase.js** داخل مجلد `src`.
3. محتويات **firebase.js**:

```js
import firebase from "firebase/compat/app";
import "firebase/compat/auth";
import "firebase/compat/firestore";
import "firebase/compat/storage";

// تكوين Firebase الخاص بك
const firebaseConfig = {
  apiKey: "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  authDomain: "testapp.firebaseapp.com",
  projectId: "testapp",
  storageBucket: "testapp.appspot.com",
  messagingSenderId: "0123456789",
  appId: "1:XXXXXXXXXXX:web:XXXXXXXXXXXXXXXXXXXX",
  measurementId: "G-XXXXXXXXXX",
};

// تهيئة تطبيق Firebase
const firebaseApp = firebase.initializeApp(firebaseConfig);
const db = firebaseApp.firestore(); // قاعدة بيانات Firebase
const auth = firebase.auth(); // مصادقة Firebase
const provider = new firebase.auth.GoogleAuthProvider(); // مزود Google للمصادقة
const storage = firebase.storage(); // تخزين Firebase

export { auth, provider, storage };
export default db;


الآن، للحصول على firebaseConfig الخاص بك، اذهب إلى Firebase وقم بإنشاء مشروع جديد.

اذهب إلى إعدادات المشروع واضغط على رمز الويب لإنشاء تطبيق ويب. اتبع التعليمات على الشاشة.



تأكد من إعداد استضافة Firebase أيضًا حتى تتمكن من استضافته لاحقًا عبر الإنترنت.


الآن، يمكنك نسخ تكوين Firebase الخاص بك بعد التوجيه.


ملاحظة: تأكد من عدم مشاركة تكوينك عبر الإنترنت.

لتمكين المصادقة عبر Google، اذهب إلى المصادقة/ابدأ الآن.

اضغط على Google وقم بتمكينه. ثم اضغط حفظ.



بمجرد تمكين مصادقة Google، قم بإنشاء قاعدة بيانات Firestore للحصول على تفاصيل الأفلام.

اذهب إلى قاعدة بيانات Firestore/إنشاء قاعدة بيانات. ابدأ في وضع الاختبار وحدد أفضل موقع لـ Firestore.

أنشئ مجموعة جديدة باسم المواضيع. ستجد جميع معلومات الأفلام في ملف disneyPlusMoviesData.json. يمكنك أيضًا إضافة أفلامك الخاصة.



:pushpin: كيفية استخدام هذا التطبيق؟
قم باستنساخ هذا المستودع إلى جهاز الكمبيوتر المحلي.
افتح الطرفية في الدليل الجذري.
اكتب وشغّل npm install أو yarn install.
بمجرد تثبيت الحزم، ابدأ التطبيق باستخدام npm start أو yarn start.
الآن تم تكوين التطبيق بالكامل ويمكنك البدء في استخدامه. :+1:
:camera: لقطات الشاشة:






:gear: تم البناء باستخدام
<img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" width="150" height="40" />

<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" width="150" />

<img src="https://img.shields.io/badge/firebase-ffca28?style=for-the-badge&logo=firebase&logoColor=black" width="150" />

:books: السكربتات المتاحة
في دليل المشروع، يمكنك تشغيل:

yarn start
يشغل التطبيق في وضع التطوير.
افتح http://localhost:3000 لعرضه في متصفحك.

ستتم إعادة تحميل الصفحة عندما تقوم بإجراء تغييرات.
قد ترى أيضًا أي أخطاء في وحدة التحكم.

yarn test
يشغل اختبار الوحدات في وضع المراقبة التفاعلية.
انظر القسم حول تشغيل الاختبارات لمزيد من المعلومات.

yarn build
يبني التطبيق للإنتاج في مجلد build.
يتم تجميع React بشكل صحيح في وضع الإنتاج وتحسين البناء للحصول على أفضل أداء.

يتم تصغير البناء وتضمين أسماء الملفات بها التجزئة.
تطبيقك جاهز للنشر!

انظر القسم حول النشر لمزيد من المعلومات.

yarn eject
ملاحظة: هذه عملية لا رجعة فيها. بمجرد أن تقوم بـ eject، لا يمكنك العودة!

إذا لم تكن راضيًا عن أداة البناء أو اختيارات التكوين، يمكنك إخراج عند أي وقت. ستقوم هذه العملية بنقل جميع ملفات التكوين والاعتماديات (webpack، Babel، ESLint، إلخ) إلى مشروعك حتى يكون لديك كامل التحكم فيهم.
