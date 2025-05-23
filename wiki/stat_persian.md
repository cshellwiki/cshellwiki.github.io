# [سیستم‌عامل] C Shell (csh) stat معادل استفاده: نمایش اطلاعات فایل

## Overview
دستورات `stat` برای نمایش اطلاعات دقیق درباره فایل‌ها و دایرکتوری‌ها در سیستم‌عامل‌های یونیکس و لینوکس استفاده می‌شود. این اطلاعات شامل اندازه فایل، زمان آخرین دسترسی، زمان آخرین تغییر و مجوزهای دسترسی است.

## Usage
سینتکس پایه دستور `stat` به صورت زیر است:

```csh
stat [options] [arguments]
```

## Common Options
- `-c` : فرمت خروجی را مشخص می‌کند.
- `-f` : اطلاعات فایل را به صورت خلاصه نمایش می‌دهد.
- `--help` : راهنمای استفاده از دستور را نمایش می‌دهد.
- `--version` : نسخه دستور را نمایش می‌دهد.

## Common Examples
### نمایش اطلاعات یک فایل
برای نمایش اطلاعات یک فایل خاص، می‌توانید از دستور زیر استفاده کنید:

```csh
stat filename.txt
```

### نمایش اطلاعات چند فایل
برای نمایش اطلاعات چند فایل به صورت همزمان:

```csh
stat file1.txt file2.txt file3.txt
```

### استفاده از گزینه -c برای فرمت سفارشی
برای نمایش فقط اندازه فایل به صورت سفارشی:

```csh
stat -c %s filename.txt
```

### نمایش اطلاعات یک دایرکتوری
برای نمایش اطلاعات یک دایرکتوری:

```csh
stat /path/to/directory
```

## Tips
- از گزینه `-f` برای دریافت اطلاعات خلاصه و سریع استفاده کنید.
- فرمت‌های سفارشی با استفاده از گزینه `-c` می‌توانند به شما کمک کنند تا فقط اطلاعات مورد نیاز خود را دریافت کنید.
- برای بررسی مجوزهای دسترسی فایل، به اطلاعات نمایش داده شده در خروجی توجه کنید.