# FrontAccounting_Vazirmatn_TCPDF
فونت Vazirmatn برای TCPDF / FrontAccounting
=============================================


محتویات پوشه اصلی بسته:
- vazirmatn.php
- vazirmatn.z
- vazirmatn.ctg.z
- vazirmatn.ttf

Persian in FrontAccounting

Install fa_IR Persian Language within FA

Edit the encoding in lang/installed_languages.inc to be 'utf-8' for fa_IR language

Upload the Persian fonts (vazirmatn) to the reporting/fonts folder

Edit lines 158 in reporting/includes/class.pdf.inc to be:

case "fa_IR" : 	$fontname = "vazirmatn"; 	break;

از قبل باید زبان فارسی را در نرم افزار نصب و فعال کرده باشید
نصب:
1) از پوشه fonts در نصب FrontAccounting یک نسخه پشتیبان بگیرید.
2) همه فایلهای بالا را در پوشه فونت کپی کنید
   reporting/fonts
   (مسیر دقیق ممکن است با نسخه FrontAccounting فرق کند.)
3) در خط 158 فایل زیر
    
reporting/includes/class.pdf.inc 

کد زیر را وارد و ذخیره کنید

case "fa_IR" : 	$fontname = "vazirmatn"; 	break;


5) تنظیمات راست‌به‌چپ و شکل‌دهی متن فارسی/عربی در کد PDF باید مانند قبل فعال بماند.
   این بسته فقط فونت و نگاشت نویسه‌ها را فراهم می‌کند و جایگزین تنظیم RTL در برنامه نیست.

پوشش نویسه:
فونت ارسالی در جدول Unicode خود دارای حروف فارسی ک، ی، پ، ژ، چ و نیز فرم‌های
نمایشی عربی/فارسی است. نگاشت TCPDF برای کدهای Unicode موجود در فونت ساخته شده است.

بررسی‌های انجام‌شده:
- فایل TTF معتبر و قابل‌خواندن بود.
- نگاشت Unicode شامل 811 نویسه در محدوده BMP است.
- نگاشت CTG با اندازه مورد انتظار 131072 بایت ساخته و پس از فشرده‌سازی بازخوانی شد.
- کدهای U+06A9 (ک)، U+06CC (ی)، U+067E (پ)، U+0698 (ژ)، U+0686 (چ)
  و فرم‌های نمایشی متناظر دارای Glyph ID معتبر هستند.
- فایل PHP با php -l بررسی شد و خطای نحوی ندارد.

توجه:
این بسته روی فایل‌های اصلی aealarabiya تغییری ایجاد نمی‌کند. برای بازگشت، نام فونت
قبلی را در کد PDF برگردانید یا فایل‌های پشتیبان را بازیابی کنید.
