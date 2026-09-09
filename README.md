<h1 align="center" id="title">WUI (WordPress + XUI Panel)</h1>

<p align="center"><img src="/logo.png" alt="project-image"></p>

<p align="center" id="description">Hide the X-UI Panel (Alireza - MHSanaei) behind WordPress! Everything on a single port!</p>

<p align="center"><img src="https://img.shields.io/badge/MHSanaei%203X--UI%20v3.7.0-34d399" alt="shields"> <img src="https://img.shields.io/badge/Alireza0%20XUI%20v1.12.0-8A2BE2" alt="shields"> <img src="https://img.shields.io/badge/HAProxy-SNI_Routing-orange" alt="shields"></p>

<h2>🧐 Features</h2>
<br>
<p align="center"><img src="/sc.JPG" alt="project-image"></p>
<br>
<p style="direction:rtl ; text-align:right">
✅مخفی سازی پنل xui به کمک مسیر خاص در پشت سایت وردپرسی
<p style="direction:rtl ; text-align:right">
✅پشتیبانی از پنل های سنایی (3X-UI تا v3.7.0) و علیرضا (تا v1.12.0)
<p style="direction:rtl ; text-align:right">
✅ایجاد اتوماتیک اینباند ها و مسیر ها در HAProxy
<p style="direction:rtl ; text-align:right">
✅نصب وب سرور آپاچی، PHP ،Mysql و HAProxy و تنظیم خودکار آنها
<p style="direction:rtl ; text-align:right">
✅نصب وردپرس در کنار پنل X-UI (نصب خودکار از صفر / نصب در کنار پنل قبلی)
<p style="direction:rtl ; text-align:right">
✅پشتیبانی از تمامی قابلیت های وردپرس (در دو حالت http و https)
<p style="direction:rtl ; text-align:right">
✅تک پورت شدن پنل و کانفیگ ها (پورت های 443 و 80) با SNI Routing هوشمند
<p style="direction:rtl ; text-align:right">
✅پشتیبانی از کانفیگ های خفن و به‌روز:

VMESS TCP http (header)

VLESS / Trojan / VMess XHTTP TLS (جدید ✨)

VLESS TCP/GRPC REALITY (passthrough واقعی، بدون تداخل)
<p style="direction:rtl ; text-align:right">
✅هاردنینگ مخفی‌سازی: هدرهای امنیتی، مخفی کردن ورژن آپاچی/PHP، غیرفعال کردن Trace
<p style="direction:rtl ; text-align:right">
✅دریافت خودکار سرتیفیکیت برای وردپرس و پنل (acme.sh)
<p style="direction:rtl ; text-align:right">
✅پین نسخه پنل (نصب نسخه دلخواه به‌جای latest)
<p style="direction:rtl ; text-align:right">

<h2>🆕 What's new in this fork</h2>
<p style="direction:rtl ; text-align:right">
🔧 بازنویسی مسیریابی 443: یک فرانت‌اند TCP با SNI-routing (قبلاً دو فرانت‌اند روی یک پورت رقابت می‌کردند)
<p style="direction:rtl ; text-align:right">
🔧 فیکس زنجیره sed تمیزکاری cert، فیکس ری‌استارت سرویس‌ها بعد از Get SSL، فیکس ریستور بکاپ، ولیدیشن پورت‌ها
<p style="direction:rtl ; text-align:right">
✨ پشتیبانی از XHTTP، جدیدترین ترنسپورت Xray
<p style="direction:rtl ; text-align:right">

<h2>🛠 Installation Steps:</h2>

<br>
<br>
<p>1. نصب اسکریپت</p>

```bash
git clone https://github.com/KanekiDevPro/WUI.git /root/wui-dds && chmod +x /root/wui-dds/install.sh && /root/wui-dds/install.sh
```
<br>
<p>2. اجرای اسکریپت</p>

```bash
wui-dds
```
<br>
<h2>⚙️ Optional: pin panel version</h2>

<p>بالای اسکریپت (قبل از اجرا) نسخه دلخواه را ست کنید، خالی یعنی latest:</p>

```bash
XUI_VERSION_MH="v3.7.0"
XUI_VERSION_ALI="v1.12.0"
```

<h2>🍰 Guidelines:</h2>
<p style="direction:rtl ; text-align:right">
❔ این اسکریپت در دو حالت نصب میشه :
<p style="direction:rtl ; text-align:right">
 1. در کنار پنل xui (بتا) در این حالت شما از قبل پنل xui سنایی یا علیرضا رو از قبل نصب کردین و حالا میخواید در کنارشون وردپرس رو نصب کنین. این ویژگی در حالت بتا قرار داره
<p style="direction:rtl ; text-align:right">
 2. نصب خودکار در این حالت شما یک سرور خام دارین و فقط نیاز به یک دامنه دارین! اسکریپت همه ی کارهارو برای شما انجام میده. نسخه ی مورد نظر شما (سنایی/علیرضا) نصب میشه، سرتیفیکیت ها گرفته میشه و یک سایت وردپرسی به همراه یک پنل xui مخفی به شما تحویل میشه!
<p style="direction:rtl ; text-align:right">
⚠️ پیش‌نیاز: سرور خام (ترجیحاً Ubuntu 22.04/24.04)، رکورد DNS دامنه به IP سرور، پورت‌های 80 و 443 آزاد
