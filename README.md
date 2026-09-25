# Delete Account – Static Site (Render)

## الملفات
- `index.html` — نفس صفحة حذف الحساب، بس متسماة index.html عشان تفتح مباشرة من الدومين الرئيسي.
- `render.yaml` — إعدادات جاهزة لـ Render (اختياري، ممكن تعمل الإعداد يدوي من الداشبورد بدل ما تستخدمه).

## قبل الرفع
افتح `index.html` وعدّل:
1. `API_BASE_URL` في أول الـ `<script>` → حط رابط الـ backend بتاعك.
2. إيميل الدعم في الـ footer.

## طريقة النشر على Render (يدوي، من غير render.yaml)
1. حط الفولدر ده (أو الملف لوحده) في ريبو منفصل على GitHub/GitLab، أو فولدر مستقل جوه ريبو المشروع الحالي (مش لازم يكون داخل كود الـ backend).
2. على Render: **New → Static Site**.
3. اختار الريبو، وحدد:
   - **Root Directory**: مسار الفولدر ده لو هو جوه ريبو أكبر (مثلاً `delete-account-site`)، أو سيبه فاضي لو الريبو نفسه هو الفولدر ده.
   - **Build Command**: سيبه فاضي.
   - **Publish Directory**: `.`
4. اعمل Deploy. Render هيديك رابط زي:
   `https://delete-account-site.onrender.com`
5. لو عايز دومين مخصص (زي `delete.yourdomain.com`)، ضيفه من Settings → Custom Domain.

## طريقة النشر باستخدام render.yaml (Blueprint)
لو الريبو فيه `render.yaml` في الجذر، تقدر تستخدم **New → Blueprint** بدل الإعداد اليدوي، وهيقرأ الإعدادات من الملف مباشرة.

## بعد النشر
- خد اللينك النهائي (`https://.../` أو الدومين المخصص) وحطه في:
  **Play Console → App content → Data safety → Account deletion**
- تأكد إن الـ backend عندك مفعّل عليه CORS للدومين ده، وإلا طلب تسجيل الدخول والحذف هيتمنع من المتصفح.
# delete-account-site.
# delete-account-siteee
