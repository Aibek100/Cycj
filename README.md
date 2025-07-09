<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DevMaster – Learn Programming</title>
  <style>
    body { font-family: sans-serif; margin:0; padding:0; color:#333; }
    .container { max-width:1000px; margin:0 auto; padding:20px; }
    header { background:#007acc; color:#fff; padding:15px; display:flex; justify-content:space-between; align-items:center; }
    select { padding:5px; }
    nav { margin:20px 0; }
    .cards { display:grid; grid-template-columns:repeat(auto-fill,minmax(280px,1fr)); gap:20px; }
    .card { background:#f0f0f0; padding:20px; border-radius:8px; text-align:center; }
    button { background:#007acc; color:#fff; border:none; padding:10px 15px; border-radius:4px; cursor:pointer; }
    button:hover { background:#005fa3; }
    footer { text-align:center; padding:15px; margin-top:30px; background:#eee; }
  </style>
</head>
<body>
  <header class="container">
    <h1 id="title">DevMaster – Learn Programming</h1>
    <select id="lang-switch">
      <option value="en">English</option>
      <option value="ru">Русский</option>
      <option value="kz">Қазақша</option>
      <option value="kg">Кыргызча</option>
      <option value="uz">O‘zbekcha</option>
    </select>
  </header>

  <main class="container">
    <p id="subtitle">Choose a programming language to start learning:</p>
    <nav class="cards">
      <div class="card">
        <h3 id="lang-python">Python</h3>
        <button id="btn-python">Start Learning</button>
      </div>
      <div class="card">
        <h3 id="lang-html">HTML & CSS</h3>
        <button id="btn-html">Start Learning</button>
      </div>
      <div class="card">
        <h3 id="lang-js">JavaScript</h3>
        <button id="btn-js">Start Learning</button>
      </div>
      <div class="card">
        <h3 id="lang-cpp">C++</h3>
        <button id="btn-cpp">Start Learning</button>
      </div>
      <div class="card">
        <h3 id="lang-java">Java</h3>
        <button id="btn-java">Start Learning</button>
      </div>
      <div class="card">
        <h3 id="lang-sql">SQL</h3>
        <button id="btn-sql">Start Learning</button>
      </div>
    </nav>
  </main>

  <footer class="container">
    <p id="footer">© DevMaster 2025. All rights reserved.</p>
  </footer>

  <script>
    const texts = {
      en: {
        title: "DevMaster – Learn Programming",
        subtitle: "Choose a programming language to start learning:",
        "btn-python": "Start Learning",
        "btn-html": "Start Learning",
        "btn-js": "Start Learning",
        "btn-cpp": "Start Learning",
        "btn-java": "Start Learning",
        "btn-sql": "Start Learning",
      },
      ru: {
        title: "DevMaster – Изучай программирование",
        subtitle: "Выбери язык программирования:",
        "btn-python": "Начать",
        "btn-html": "Начать",
        "btn-js": "Начать",
        "btn-cpp": "Начать",
        "btn-java": "Начать",
        "btn-sql": "Начать",
      },
      kz: { title: "DevMaster – Бағдарламалауды үйрен", subtitle: "Бағдарламалау тілін таңда:", "btn-python":"Бастау","btn-html":"Бастау","btn-js":"Бастау","btn-cpp":"Бастау","btn-java":"Бастау","btn-sql":"Бастау" },
      kg: { title: "DevMaster – Программалоону үйрөн", subtitle: "Программалоо тилин тандоо:", "btn-python":"Баштоо","btn-html":"Баштоо","btn-js":"Баштоо","btn-cpp":"Баштоо","btn-java":"Баштоо","btn-sql":"Баштоо" },
      uz: { title: "DevMaster – Dasturlashni o‘rgan", subtitle: "Dasturlash tilini tanlang:", "btn-python":"Boshlash","btn-html":"Boshlash","btn-js":"Boshlash","btn-cpp":"Boshlash","btn-java":"Boshlash","btn-sql":"Boshlash" },
    };

    const switcher = document.getElementById("lang-switch");
    function applyLang(lang) {
      const t = texts[lang] || texts.en;
      document.getElementById("title").textContent = t.title;
      document.getElementById("subtitle").textContent = t.subtitle;
      ["python","html","js","cpp","java","sql"].forEach(code => {
        document.getElementById(`btn-${code}`).textContent = t[`btn-${code}`];
      });
    }
    switcher.addEventListener("change", e => {
      applyLang(e.target.value);
    });
    // init
    applyLang("en");
  </script>
</body>
</html>
