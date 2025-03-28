# [نظام التشغيل] C Shell (csh) grep الاستخدام: البحث عن النصوص في الملفات

## Overview
أداة `grep` هي أداة قوية تُستخدم للبحث عن نصوص معينة داخل الملفات. تُعتبر `grep` اختصارًا لـ "Global Regular Expression Print"، وتساعد المستخدمين في تحديد مواقع النصوص أو الأنماط داخل الملفات النصية.

## Usage
تستخدم `grep` بشكل أساسي للبحث عن نصوص أو أنماط محددة. الصيغة الأساسية للأمر هي:

```
grep [options] [arguments]
```

## Common Options
- `-i`: تجاهل حالة الأحرف أثناء البحث.
- `-v`: عكس النتائج، أي عرض الأسطر التي لا تحتوي على النص المحدد.
- `-r`: البحث بشكل متكرر في جميع الملفات داخل الدليل والمجلدات الفرعية.
- `-n`: عرض رقم السطر مع كل نتيجة.
- `-c`: عرض عدد الأسطر التي تحتوي على النص المحدد بدلاً من عرض الأسطر نفسها.

## Common Examples
- **البحث عن نص معين في ملف:**
  ```csh
  grep "نص" filename.txt
  ```

- **البحث عن نص مع تجاهل حالة الأحرف:**
  ```csh
  grep -i "نص" filename.txt
  ```

- **البحث في جميع الملفات داخل مجلد:**
  ```csh
  grep -r "نص" /path/to/directory
  ```

- **عرض رقم السطر مع النتائج:**
  ```csh
  grep -n "نص" filename.txt
  ```

- **عد الأسطر التي تحتوي على نص معين:**
  ```csh
  grep -c "نص" filename.txt
  ```

## Tips
- استخدم الخيار `-i` للبحث عن نصوص دون القلق بشأن حالة الأحرف.
- عند البحث في مجلدات كبيرة، استخدم الخيار `-r` لتسهيل عملية البحث.
- تأكد من استخدام علامات اقتباس حول النصوص التي تحتوي على مسافات.
- يمكنك دمج `grep` مع أوامر أخرى باستخدام الأنابيب (`|`) لزيادة فعالية البحث.