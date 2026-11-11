# منصة المشتريات – خطوات الإعداد (مرة واحدة)

## أولًا: Firebase
1. ادخلي console.firebase.google.com وأنشئي مشروعًا جديدًا (اسم مثل value-capital-procurement)، وعطّلي Google Analytics.
2. **Build > Firestore Database > Create database**: اختاري الوضع Production، والمنطقة الأقرب (مثل Dammam أو Frankfurt).
3. **Build > Authentication > Get started > Sign-in method**: فعّلي **Anonymous** و**Email/Password**.
4. **Authentication > Users > Add user**: أضيفي بريدك وكلمة مرور قوية. هذا حساب المسؤول، ولا تنشئي حسابًا لغيرك.
5. **Authentication > Settings > Authorized domains > Add domain**: أضيفي `fvalue2026.github.io`.
6. **Firestore > Rules**: الصقي محتوى `firestore.rules` بعد استبدال `ADMIN_EMAIL_HERE` ببريدك، ثم Publish.
7. **Project settings > Your apps > </> (Web)**: سجّلي تطبيقًا، وانسخي كائن الإعدادات إلى `firebase-config.js` (أربع قيم).

## ثانيًا: الرفع على GitHub
1. في مستودع `value-capital-purchase-form` احتفظي بنسخة من `index.html` القديم (تنزيله أو إعادة تسميته).
2. ارفعي `index.html` و`firebase-config.js` و`logo.png` و`logo-po.png` (Add file > Upload files) واستبدلي الموجود، ثم Commit.
3. بعد دقيقة افتحي `https://fvalue2026.github.io/value-capital-purchase-form/`.

## الاستخدام
- الموظفون يفتحون الرابط ويقدمون الطلب بدون أي حساب، ويرون طلباتهم على نفس الجهاز والمتصفح.
- أنتِ تضغطين «دخول المسؤول» أعلى الصفحة، فتظهر لوحة المتابعة والاعتماد وأوامر الشراء.
- الجهاز الجديد أو المتصفح الآخر لا يعرض طلبات الموظف السابقة له، لكنها تظل ظاهرة لكِ.
