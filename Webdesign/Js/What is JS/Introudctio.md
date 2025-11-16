<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>جزوه مبانی جاوااسکریپت</title>

  <style>
    body {
      font-family: "Vazirmatn", Tahoma, sans-serif;
      background: #f6f6f6;
      margin: 0;
      padding: 0;
      direction: rtl;
      line-height: 1.9;
    }

    .container {
      width: 85%;
      max-width: 900px;
      background: #fff;
      margin: 30px auto;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 0 12px rgba(0,0,0,0.1);
    }

    h1, h2, h3 {
      color: #333;
    }

    pre {
      background: #272822;
      color: #e6db74;
      padding: 12px;
      border-radius: 8px;
      overflow-x: auto;
    }

    code {
      color: #ffeb3b;
    }

    hr {
      margin: 35px 0;
    }

    .title {
      text-align: center;
      font-size: 28px;
      margin-bottom: 20px;
      color: #2c3e50;
    }
  </style>
</head>

<body>

<div class="container">

  <h1 class="title">جزوه آموزشی: مبانی پایه JavaScript</h1>

<h2>۱. جاوااسکریپت چیست؟</h2>
  <p>
    جاوااسکریپت زبان برنامه‌نویسی برای کنترل رفتار صفحات وب است.
    HTML اسکلت صفحه است، CSS ظاهر را می‌سازد و جاوااسکریپت هوش و تعامل را اضافه می‌کند.
  </p>

  <hr>

<h2>۲. نحوه نوشتن جاوااسکریپت</h2>

<h3>نوشتن داخل تگ <code>&lt;script&gt;</code></h3>
  <pre><code>&lt;script&gt;
  console.log("Hello JS!");
&lt;/script&gt;</code></pre>

<h3>فایل جدا (app.js)</h3>
  <pre><code>&lt;script src="app.js"&gt;&lt;/script&gt;</code></pre>

<h3>اجرا در Node.js</h3>
  <pre><code>node app.js</code></pre>

  <hr>

<h2>۳. متغیرها</h2>

<h3>let</h3>
  <pre><code>let score = 10;
score = 15;</code></pre>

<h3>const</h3>
  <pre><code>const pi = 3.14;</code></pre>

<h3>var</h3>
  <p>قدیمی و کمتر استفاده می‌شود.</p>

  <hr>

<h2>۴. انواع داده</h2>

<h3>Primitive</h3>
  <p>number – string – boolean – undefined – null – bigint – symbol</p>

<h3>Object</h3>
  <pre><code>let person = {
  name: "Ali",
  age: 17
};</code></pre>

  <hr>

<h2>۵. عملگرها</h2>

<h3>ریاضی</h3>
  <pre><code>+   -   *   /   %   **</code></pre>

<h3>مقایسه‌ای</h3>
  <pre><code>==   ===   >   &lt;   >=   <=</code></pre>

<h3>تفاوت == و ===</h3>
  <pre><code>"5" == 5   // true
"5" === 5  // false</code></pre>

  <hr>

<h2>۶. شرط‌ها</h2>

<h3>if / else</h3>
  <pre><code>let temp = 30;

if (temp &gt; 25) {
  console.log("گرمه!");
} else {
  console.log("خنکه!");
}</code></pre>

<h3>switch</h3>
  <pre><code>let grade = "A";

switch (grade) {
  case "A":
    console.log("عالی!");
    break;
  case "B":
    console.log("خوب!");
    break;
  default:
    console.log("نامشخص");
}</code></pre>

  <hr>

<h2>۷. حلقه‌ها</h2>

<h3>for</h3>
  <pre><code>for (let i = 0; i &lt; 5; i++) {
  console.log(i);
}</code></pre>

<h3>while</h3>
  <pre><code>let n = 0;
while (n &lt; 3) {
  console.log(n);
  n++;
}</code></pre>

<h3>for...of</h3>
  <pre><code>for (let x of [10, 20, 30]) {
  console.log(x);
}</code></pre>

<h3>for...in</h3>
  <pre><code>let person = {name: "Ali", age: 17};

for (let key in person) {
  console.log(key, person[key]);
}</code></pre>

  <hr>

<h2>۸. توابع</h2>

<h3>تابع معمولی</h3>
  <pre><code>function sum(a, b) {
  return a + b;
}</code></pre>

<h3>تابع فلشی (Arrow Function)</h3>
  <pre><code>const sum = (a, b) =&gt; a + b;</code></pre>

  <hr>

<h2>۹. آرایه‌ها</h2>

  <pre><code>let nums = [10, 20, 30];

nums.push(40);   // اضافه کردن
nums.pop();      // حذف آخرین مورد</code></pre>

  <hr>

<h2>۱۰. DOM چیست؟</h2>
  <p>
    DOM مدل درختی صفحه است. جاوااسکریپت می‌تواند عناصر را پیدا کند و تغییر دهد.
  </p>

  <pre><code>document.getElementById("title").innerText = "Hello!";</code></pre>

<h3>مثال رویداد</h3>
  <pre><code>document.querySelector("button").onclick = () =&gt; {
  alert("Clicked!");
};</code></pre>

  <hr>

<h2>۱۱. مثال ماشین حساب ساده</h2>

<h3>HTML</h3>
  <pre><code>&lt;input id="a" type="number" placeholder="عدد اول"&gt;
&lt;input id="b" type="number" placeholder="عدد دوم"&gt;
&lt;button onclick="calc()"&gt;جمع&lt;/button&gt;
&lt;p id="result"&gt;&lt;/p&gt;</code></pre>

<h3>JavaScript</h3>
  <pre><code>function calc() {
  const a = Number(document.getElementById("a").value);
  const b = Number(document.getElementById("b").value);
  document.getElementById("result").innerText = a + b;
}</code></pre>

</div>

</body>
</html>
