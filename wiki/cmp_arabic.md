# [نظام التشغيل] C Shell (csh) cmp الاستخدام: مقارنة الملفات

## Overview
يستخدم الأمر `cmp` لمقارنة ملفين ثنائيين أو نصيين، ويظهر الفرق بينهما. إذا كانت الملفات متطابقة، فلن يتم عرض أي شيء، وإذا كان هناك اختلاف، سيظهر موقع الاختلافات.

## Usage
يمكن استخدام الأمر `cmp` بالشكل التالي:

```
cmp [options] [arguments]
```

## Common Options
- `-l`: يعرض مواقع الاختلافات في شكل أرقام بايت.
- `-s`: لا يعرض أي مخرجات، فقط يعيد حالة الخروج.
- `-i <n>`: يتجاهل أول `n` بايت من كل ملف.
- `-b`: يعرض الاختلافات في شكل بايتات.

## Common Examples
- لمقارنة ملفين وعرض الاختلافات:
    ```csh
    cmp file1.txt file2.txt
    ```

- لمقارنة ملفين مع عرض مواقع الاختلافات:
    ```csh
    cmp -l file1.bin file2.bin
    ```

- لاستخدام الأمر بدون أي مخرجات، فقط للتحقق من التطابق:
    ```csh
    cmp -s file1.txt file2.txt
    ```

- لتجاهل أول 10 بايت من كل ملف أثناء المقارنة:
    ```csh
    cmp -i 10 file1.txt file2.txt
    ```

## Tips
- تأكد من استخدام الخيار `-s` إذا كنت تريد فقط معرفة ما إذا كانت الملفات متطابقة دون الحاجة إلى تفاصيل.
- استخدم الخيار `-l` للحصول على معلومات دقيقة حول مواقع الاختلافات، خاصة عند التعامل مع الملفات الثنائية.
- من المفيد دائمًا إجراء نسخ احتياطية من الملفات قبل إجراء المقارنات، خاصة إذا كنت تعمل على ملفات مهمة.