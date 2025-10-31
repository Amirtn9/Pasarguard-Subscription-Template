<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<title>راهنمای نصب تمپلیت‌های Pasarguard</title>
</head>
<body dir="rtl">

<h1>🚀 راهنمای نصب تمپلیت‌های Pasarguard</h1>

<p>در این صفحه، تمام تمپلیت‌های موجود برای Pasarguard قرار دارند و می‌توانید با دنبال کردن مراحل زیر، آنها را نصب و فعال کنید.</p>

<hr>

<h2>۱. تمپلیت اصلی Pasarguard</h2>

<h3>مرحله ۱: دانلود قالب</h3>
<pre><code>sudo wget -N -P /var/lib/pasarguard/templates/subscription/ https://github.com/PasarGuard/subscription-template/releases/latest/download/index.html</code></pre>

<h3>مرحله ۲: پیکربندی Pasarguard</h3>
<pre><code>echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"' | sudo tee -a /opt/pasarguard/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/pasarguard/.env</code></pre>
<p>یا به صورت دستی فایل <code>/opt/pasarguard/.env</code> را باز کرده و خطوط زیر را از حالت کامنت خارج کنید:</p>
<pre><code>CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"</code></pre>

<h3>مرحله ۳: ریستارت Pasarguard</h3>
<pre><code>pasarguard restart</code></pre>

<hr>

<h2>۲. قالب LightWaySub - روشن</h2>

<h3>مرحله ۱: دانلود قالب روشن</h3>
<pre><code>sudo wget -N -P /var/lib/pasarguard/templates/subscription/ https://github.com/MatinDehghanian/LightWaySub/releases/latest/download/index.html</code></pre>

<h3>مرحله ۲: پیکربندی فایل .env</h3>
<pre><code>echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"' | sudo tee -a /opt/pasarguard/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/pasarguard/.env</code></pre>
<p>یا به صورت دستی فایل <code>/opt/pasarguard/.env</code> را باز کرده و خطوط زیر را از حالت کامنت خارج کنید:</p>
<pre><code>CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"</code></pre>

<h3>مرحله ۳: ریستارت Pasarguard</h3>
<pre><code>pasarguard restart</code></pre>

<hr>

<h2>۳. قالب LightWaySub - تیره</h2>

<h3>مرحله ۱: دانلود قالب تیره</h3>
<pre><code># دریافت خودکار آخرین لینک قالب تیره
DARK_URL=$(curl -s https://api.github.com/repos/MatinDehghanian/LightWaySub/releases | grep -E '"browser_download_url".*-dark.*index\.html"' | head -1 | cut -d '"' -f 4)
sudo wget -N -P /var/lib/pasarguard/templates/subscription/ "$DARK_URL"</code></pre>

<h3>مرحله ۲: پیکربندی فایل .env</h3>
<pre><code>echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"' | sudo tee -a /opt/pasarguard/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/pasarguard/.env</code></pre>
<p>یا به صورت دستی فایل <code>/opt/pasarguard/.env</code> را باز کرده و خطوط زیر را از حالت کامنت خارج کنید:</p>
<pre><code>CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"</code></pre>

<h3>مرحله ۳: ریستارت Pasarguard</h3>
<pre><code>pasarguard restart</code></pre>

</body>
</html>
