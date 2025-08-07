<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Dom Veka — Современные дома в ЛО и СПб</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap" rel="stylesheet">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
  <meta name="description" content="Dom Veka — строительство современных домов в Ленинградской области и Санкт-Петербурге. Индивидуальные проекты, высокое качество, разумные цены.">
  <meta name="keywords" content="строительство домов, Ленинградская область, СПб, современные дома, Dom Veka">
  <meta name="author" content="Dom Veka">
  <meta property="og:title" content="Dom Veka — Современные дома в ЛО и СПб">
  <meta property="og:description" content="Индивидуальные проекты домов от 15 до 50 млн ₽. Качество, стиль, комфорт.">
  <meta property="og:type" content="website">
  <meta property="og:image" content="https://ваш-сайт.github.io/house1.jpg">
  <style>
    body {
      margin: 0;
      font-family: 'Montserrat', sans-serif;
      background: #fff;
      color: #000;
      line-height: 1.6;
    }
    header {
      background: #000;
      color: #fff;
      text-align: center;
      padding: 40px 20px;
    }
    header img {
      height: 60px;
      margin-bottom: 10px;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    h2 {
      font-size: 1.8em;
      margin-bottom: 20px;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }
    .gallery img {
      width: 100%;
      border-radius: 8px;
      object-fit: cover;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      transition: transform 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.02);
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-family: inherit;
      font-size: 1em;
    }
    input[type="submit"] {
      background: #000;
      color: #fff;
      border: none;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    input[type="submit"]:hover {
      background: #333;
    }
    #price {
      font-weight: bold;
    }
    iframe {
      border: none;
      border-radius: 8px;
      width: 100%;
      height: 300px;
    }
    footer {
      background: #000;
      color: #fff;
      text-align: center;
      padding: 30px 20px;
      margin-top: 40px;
    }
    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      animation: fadeIn 1s ease-out forwards;
    }
    @keyframes fadeIn {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <header>
    <img src="logo.png" alt="Dom Veka">
    <h1>Dom Veka</h1>
    <p>Современные дома в Ленинградской области и Санкт-Петербурге</p>
  </header>

  <section class="fade-in">
    <h2>О компании</h2>
    <p>Dom Veka — команда профессионалов, специализирующихся на строительстве домов стоимостью от 15 до 50 миллионов рублей. Мы создаем комфортные, энергоэффективные и стильные дома, учитывая индивидуальные пожелания каждого клиента. Работаем в ЛО и СПб, соблюдаем сроки и гарантируем качество.</p>
  </section>

  <section class="fade-in">
    <h2>Галерея проектов</h2>
    <div class="gallery">
      <img src="house1.jpg" alt="Дом 1">
      <img src="house2.jpg" alt="Дом 2">
    </div>
  </section>

  <section class="fade-in">
    <h2>Калькулятор стоимости</h2>
    <label for="area">Введите площадь дома (м²):</label>
    <input type="number" id="area" placeholder="Например, 250" oninput="calculatePrice()">
    <p id="price">Стоимость: —</p>
  </section>

  <section class="fade-in">
    <h2>Отзывы клиентов</h2>
    <div style="display: grid; gap: 20px;">
      <div style="background:#f0f0f0; padding:20px; border-radius:8px;">
        <p>🏡 “Дом получился именно таким, как мы мечтали. Команда Dom Veka — настоящие профессионалы!”</p>
        <p><strong>— Анна, Гатчина</strong></p>
      </div>
      <div style="background:#f0f0f0; padding:20px; border-radius:8px;">
        <p>🔨 “Строительство прошло быстро, качественно и без сюрпризов. Спасибо!”</p>
        <p><strong>— Дмитрий, Всеволожск</strong></p>
      </div>
    </div>
  </section>

  <section class="fade-in">
    <h2>Связаться через Telegram</h2>
    <form id="tgForm">
      <input type="text" id="tgName" placeholder="Ваше имя" required>
      <input type="email" id="tgEmail" placeholder="Email" required>
      <textarea id="tgMessage" placeholder="Сообщение" required></textarea>
      <input type="submit" value="Отправить в Telegram">
    </form>
    <p id="tgStatus"></p>
  </section>

  <section class="fade-in">
    <h2>Мы на карте</h2>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!..." loading="lazy"></iframe>
  </section>

  <footer>
    &copy; 2025 Dom Veka. Все права защищены. | info@domveka.ru | +7 (812) 123-45-67
  </footer>

  <script>
    function calculatePrice() {
      const area = document.getElementById("area").value;
      const price = area * 15000;
      document.getElementById("price").innerText = area ? `Стоимость: ${price.toLocaleString()} ₽` : 'Стоимость: —';
    }

    const faders = document.querySelectorAll('.fade-in');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.animationPlayState = 'running';
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.3 });

    faders.forEach(el => {
      el.style.animationPlayState = 'paused';
      observer.observe(el);
    });

    // Telegram форма
    const token = 'ВАШ_ТОКЕН';
    const chatId = 'ВАШ_CHAT_ID';

    document.getElementById('tgForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('tgName').value;
      const email = document.getElementById('tgEmail').value;
      const message = document.getElementById('tgMessage').value;

      const text = `📩 Новое сообщение с сайта Dom Veka:\n👤 Имя: ${name}\n📧 Email: ${email}\n📝 Сообщение: ${message}`;

      fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ chat_id: chatId, text })
      })
      .then(res => res.ok ? tgStatus.innerText = 'Сообщение отправлено!' : tgStatus.innerText = 'Ошибка отправки.')
      .catch(() => tgStatus.innerText = 'Ошибка соединения.');
    });
  </script>

</body>
</html>
