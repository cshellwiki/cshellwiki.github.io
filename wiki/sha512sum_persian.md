# [سیستم‌عامل‌های یونیکس] C Shell (csh) sha512sum استفاده: محاسبه و تأیید هش SHA-512

## Overview
دستور `sha512sum` برای محاسبه و تأیید هش SHA-512 از فایل‌ها استفاده می‌شود. این دستور به شما کمک می‌کند تا یک مقدار هش منحصر به فرد برای داده‌های خود تولید کنید که می‌تواند برای بررسی صحت و یکپارچگی فایل‌ها مورد استفاده قرار گیرد.

## Usage
سینتکس پایه دستور به صورت زیر است:

```csh
sha512sum [options] [arguments]
```

## Common Options
- `-b`: محاسبه هش برای فایل‌های باینری.
- `-c`: تأیید هش‌های موجود در یک فایل.
- `--quiet`: خاموش کردن خروجی غیرضروری.
- `--help`: نمایش راهنمای استفاده از دستور.

## Common Examples
### محاسبه هش یک فایل
برای محاسبه هش SHA-512 یک فایل، از دستور زیر استفاده کنید:

```csh
sha512sum filename.txt
```

### تأیید هش از یک فایل
برای تأیید هش‌های ذخیره شده در یک فایل، می‌توانید از گزینه `-c` استفاده کنید:

```csh
sha512sum -c checksums.txt
```

### محاسبه هش برای چندین فایل
برای محاسبه هش چندین فایل به صورت همزمان، می‌توانید نام فایل‌ها را به دستور اضافه کنید:

```csh
sha512sum file1.txt file2.txt file3.txt
```

## Tips
- همیشه هش فایل‌های مهم خود را ذخیره کنید تا در آینده بتوانید صحت آن‌ها را بررسی کنید.
- از گزینه `-b` برای فایل‌های باینری استفاده کنید تا از محاسبات نادرست جلوگیری شود.
- برای تأیید صحت فایل‌ها، از یک فایل چک‌سوم معتبر استفاده کنید.