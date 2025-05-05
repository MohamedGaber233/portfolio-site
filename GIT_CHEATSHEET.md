# Git Cheatsheet & Guide

هذا الدليل يجمع جميع أوامر Git التي استخدمناها في مشروع الـ Portfolio مع شرح لكل أمر وكومنت يساعدك تفهمه.

---

## 1. تهيئة المستودع (Initialize Repository)

```bash
git init
# ← ينشئ مجلد .git/ في المشروع ويبدأ تتبّع التغييرات

git config --global user.name "Your Name"
# ← يضبط اسمك الذي سيظهر في جميع الكوميتات

git config --global user.email "you@example.com"
# ← يضبط بريدك الإلكتروني للكوميتات

git add .
# ← يضيف كل الملفات الجديدة والمعدّلة إلى منطقة الـ staging
git commit -m "رسالة توضيحية"
# ← يُنشئ commit جديد يحوي التغييرات في الـ staging area

git checkout -b feature/contact-form
# ← ينشئ فرعاً جديداً اسمه feature/contact-form وينتقل إليه

git checkout main
# ← العودة إلى الفرع الرئيسي (main أو master حسب إعدادك)

git merge feature/contact-form
# ← يدمج تغييرات feature/contact-form في الفرع الحالي
git remote add origin https://github.com/YourUsername/portfolio-site.git
# ← يربط المستودع المحلي بمستودع GitHub البعيد

git branch -M main
# ← (اختياري) يعيد تسمية الفرع الرئيسي إلى main

git push -u origin main
# ← يدفع الفرع main إلى الريموت origin ويضبط التتبع التلقائي

git stash
# ← يخزن التعديلات غير الملتزم بها مؤقتاً ويعيد Working Directory نظيفاً

git stash pop
# ← يستعيد آخر stash ويطبّقه على الشجرة الحالية ثم يزيله من القائمة

git reset --soft HEAD~1
# ← يُرجع HEAD إلى الـ commit السابق دون مسح التعديلات من Working Directory

git reset --hard HEAD~1
# ← يعيد HEAD والـ Working Directory إلى الحالة قبل الـ commit تماماً

git revert HEAD
# ← ينشئ commit جديد يعكس تغييرات آخر commit دون حذف التاريخ

