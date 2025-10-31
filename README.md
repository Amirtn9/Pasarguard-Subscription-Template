<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<title>راهنمای نصب قالب اشتراک Pasarguard</title>
</head>
<body dir="rtl">

<h1>🚀 نصب قالب اشتراک Pasarguard</h1>

<p>این قالب، تمپلیت اصلی Pasarguard است و مخصوص سرویس Pasarguard طراحی شده است.</p>

<h2>۱. دانلود قالب</h2>
<pre><code>sudo wget -N -P /var/lib/pasarguard/templates/subscription/ https://github.com/PasarGuard/subscription-template/releases/latest/download/index.html</code></pre>

<h2>۲. پیکربندی Pasarguard</h2>
<p>دستورات زیر را در ترمینال سرور اجرا کنید:</p>
<pre><code>echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"' | sudo tee -a /opt/pasarguard/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/pasarguard/.env</code></pre>

<p>یا به صورت دستی فایل <code>.env</code> در پوشه <code>/opt/pasarguard</code> را باز کرده و خطوط زیر را از حالت کامنت خارج کنید:</p>
<pre><code>CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"</code></pre>

<h2>۳. راه‌اندازی مجدد Pasarguard</h2>
<pre><code>pasarguard restart</code></pre>

<p>✅ تمپلیت اصلی Pasarguard با موفقیت نصب و فعال شد.</p>

</body>
</html>

