JEBHA STORE — نفس تصميم MENU PRO + لوحة تحكم حقيقية + نشر مجاني

1) صاوب حساب GitHub وحساب Supabase مجانيين.
2) فـSupabase دير New project. من SQL Editor لسق الكود الكامل ديال database.sql وشغلو.
3) فـSupabase > Authentication > Users زيد حساب مدير من "Add user" (ولا سجلو بطريقة آمنة). استعمل إيميلك الحقيقي وكلمة سر قوية.
4) رجع لـSQL Editor ونفّذ هاد التعليمة بوحدها بعد تبديل YOUR_EMAIL:
insert into public.admin_users(user_id)
select id from auth.users where lower(email)=lower('YOUR_EMAIL@example.com')
on conflict (user_id) do nothing;
5) فـSupabase > Project Settings > API خذ Project URL و publishable/anon KEY (المفتاح العام فقط).
6) حل config.js وبدل PASTE_YOUR_SUPABASE_URL و PASTE_YOUR_SUPABASE_PUBLISHABLE_KEY. لا تضع service_role أو secret key أبدا.
7) صاوب GitHub repository من نوع Public باسم jebha-store، ورفع الملفات كاملين: index.html وadmin.html وconfig.js وdatabase.sql وrobots.txt ... (الملف SQL ما خاصوش يكون منشور للضرورة، تقدر تحيدو من الرفع بعدما تنفذو).
8) GitHub > Settings > Pages > Deploy from branch > main / (root) > Save.
9) الموقع: https://USERNAME.github.io/jebha-store/
10) لوحة التحكم: https://USERNAME.github.io/jebha-store/admin.html
11) دخل بإيميل وكلمة سر المدير. زيد أول منتوج. المنتجات التجريبية ما غاديش تبقى فالموقع ملي قاعدة البيانات تتربط بنجاح؛ باش تعمرها دخل المنتجات من لوحة التحكم.
12) الظهور فـGoogle: دخل search.google.com/search-console، سجل رابط الموقع، تحقق من الملكية وطلب فهرسة الصفحة الرئيسية من URL Inspection. GitHub Pages كيعطي HTTPS ولكن ما كايضمنش الظهور الفوري ولا المرتبة. الكلمات الوصفية والمنتوجات اللي كتجي عبر Javascript ممكن Google يتأخر يفهرسها.

مهم: نسخة GitHub Pages ثابتة، لوحة التحكم والمنتجات محتاجين اتصال بالإنترنت وبـSupabase. تقدر تبقى بلا أداء بالبطاقة؛ الطلبات كتدوز عبر WhatsApp 212691747137. الاستضافة عندها خطة مجانية مع حدود. لا تشارك إيميل/كلمة سر/مفاتيح سرية ديالك. قبل البيع تأكد من السماح بإعادة بيع المنتجات.
