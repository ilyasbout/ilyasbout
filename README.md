body {
  font-family: Tahoma, sans-serif;
  background-color: #f4f4f4;
  padding: 20px;
  text-align: center;
  direction: rtl;
}
header {
  background-color: #2e7d32;
  color: white;
  padding: 10px;
}
button, input, textarea {
  padding: 10px;
  margin: 10px 0;
  border: none;
  width: 80%;
  max-width: 400px;
}
textarea {
  resize: vertical;
}
a {
  display: block;
  margin-top: 20px;
  color: #2e7d32;
  text-decoration: none;
}
ul {
  text-align: right;
  margin: 20px;
}
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>المحافِظ على الماء</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header><h1>مرحبا بك في Water Retainer</h1></header>
  <button onclick="location.href='dose.html'">احسب الجرعة</button>
  <button onclick="location.href='instructions.html'">طريقة الاستعمال</button>
  <button onclick="location.href='testimonials.html'">تجارب وشهادات</button>
  <button onclick="location.href='contact.html'">تواصل معنا</button>
  <button onclick="location.href='map.html'">خريطة الاستعمال</button>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>احسب الجرعة</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>حاسبة الجرعة</h1>
  <input type="number" id="length" placeholder="الطول (متر)">
  <input type="number" id="width" placeholder="العرض (متر)">
  <input type="number" id="lines" placeholder="عدد الصفوف">
  <input type="number" id="dose" placeholder="الجرعة (mL/m²)" value="2">
  <button onclick="calculate()">احسب</button>
  <p id="result"></p>

  <script>
    function calculate() {
      const l = parseFloat(document.getElementById('length').value) || 0;
      const w = parseFloat(document.getElementById('width').value) || 0;
      const n = parseFloat(document.getElementById('lines').value) || 0;
      const d = parseFloat(document.getElementById('dose').value) || 2;
      const area = l * w * n;
      const total = area * d;
      document.getElementById('result').innerHTML = 
        `المساحة = ${area.toFixed(2)} m²<br>الجرعة = ${total.toFixed(0)} mL ≈ ${(total/1000).toFixed(2)} L`;
    }
  </script>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>طريقة الاستعمال</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>طريقة الاستعمال</h1>
  <ul>
    <li>ذوب الجرعة فالماء: 2 أو 4 mL/m² حسب الحالة</li>
    <li>رش مباشرة على سطح التربة أو باستعمال قطرة قطرة</li>
    <li>كرر كل 45 يوم حسب نوع الزرع</li>
  </ul>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>تجارب وشهادات</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>شهادات فلاحين</h1>
  <p>✅ فلاح من الغرب: "نقصت عدد السقيات بـ 50%، وزاد الإنتاج!"</p>
  <p>✅ مهندس فلاح من مراكش: "ساعدني فالرطوبة خلال الجفاف."</p>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>تواصل معنا</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>تواصل معنا</h1>
  <form action="mailto:your@email.com" method="post" enctype="text/plain">
    <input type="text" name="name" placeholder="الاسم">
    <input type="email" name="email" placeholder="البريد الإلكتروني">
    <textarea name="message" placeholder="اكتب رسالتك هنا..."></textarea>
    <button type="submit">إرسال</button>
  </form>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>خريطة</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>خريطة مناطق التجربة</h1>
  <iframe src="https://www.google.com/maps/embed?pb=!1m18..." width="100%" height="300"></iframe>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>تحميل الكتيب</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>كتيب Water Retainer</h1>
  <p>يمكنك تحميل الكتيب العلمي فيه جميع التفاصيل التقنية والتجارب الميدانية.</p>
  <a href="white-paper.pdf" download style="font-weight: bold; font-size: 18px; color: #1565c0;">
    ⬇️ اضغط هنا لتحميل الكتيب (PDF)
  </a>
  <p style="margin-top:20px;">Format disponible aussi en français.</p>
  <a href="index.html">رجوع للرئيسية</a>
</body>
</html>
