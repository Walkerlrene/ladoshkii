<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Студия творчества «Ладошки»</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Roboto, system-ui, -apple-system, sans-serif;
      background-color: #fdf8f7;  /* нежный тёплый фон */
      color: #4e4e4e;
      line-height: 1.6;
    }

    /* мягкие, пастельные тона + акцент (коралловый) */
    h1, h2, h3 {
      font-weight: 400;
      letter-spacing: 0.02em;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 3rem 5%;
    }

    /* ===== ХЕДЕР ===== */
    header {
      background: #ffffff;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.02);
      padding: 0.8rem 5%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo-block {
      display: flex;
      align-items: center;
      gap: 1rem;
    }

    .logo-block img {
      height: 70px;
      width: auto;
      transition: transform 0.3s;
    }

    .logo-block img:hover {
      transform: scale(1.02);
    }

    .studio-name {
      font-size: 2rem;
      font-weight: 300;
      color: #b2a38b;  /* приглушённый песочный */
      letter-spacing: 2px;
      border-left: 2px solid #f5c4b4;
      padding-left: 1rem;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 2.2rem;
    }

    nav a {
      text-decoration: none;
      color: #6d6d6d;
      font-weight: 500;
      font-size: 1.1rem;
      transition: color 0.2s ease;
      padding-bottom: 4px;
      border-bottom: 2px solid transparent;
    }

    nav a:hover {
      color: #f08a7a;  /* акцент — нежный коралл */
      border-bottom-color: #f5c4b4;
    }

    /* ===== ЗАГОЛОВКИ СЕКЦИЙ ===== */
    .section-title {
      text-align: center;
      font-size: 2.5rem;
      margin-bottom: 2rem;
      color: #6b5e4f;
      position: relative;
      padding-bottom: 0.8rem;
    }

    .section-title::after {
      content: '';
      display: block;
      width: 100px;
      height: 3px;
      background: #f5c4b4;  /* пастельно-персиковый */
      margin: 0.5rem auto 0;
      border-radius: 4px;
    }

    /* ===== БЛОК О НАС ===== */
    .about {
      background: #ffffffd9;
      backdrop-filter: blur(2px);
      border-radius: 40px 40px 20px 20px;
      padding: 2.5rem 2rem;
      box-shadow: 0 10px 25px rgba(175, 140, 120, 0.08);
      margin-bottom: 1rem;
    }

    .about p {
      font-size: 1.3rem;
      text-align: center;
      max-width: 850px;
      margin: 1rem auto 0;
      color: #5f5b57;
      line-height: 1.7;
    }

    /* ===== КАРТОЧКИ НАПРАВЛЕНИЙ ===== */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 2.5rem;
      margin: 2.5rem 0 1rem;
    }

    .card {
      background: #ffffff;
      border-radius: 30px;
      padding: 2rem 1.5rem;
      box-shadow: 0 15px 30px rgba(190, 150, 130, 0.05);
      transition: 0.3s;
      text-align: center;
      border: 1px solid #f8e3db;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 35px rgba(200, 150, 130, 0.15);
      border-color: #f5c4b4;
    }

    .card h3 {
      font-size: 2rem;
      font-weight: 350;
      color: #c28e7a;  /* приглушённый терракот */
      margin-bottom: 0.8rem;
    }

    .card p {
      color: #7b756f;
      font-size: 1.1rem;
    }

    /* ===== ПРЕПОДАВАТЕЛИ (КРУГЛЫЕ АВАТАРКИ-ЗАГЛУШКИ) ===== */
    .teachers-wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 3rem 4rem;
      margin: 3rem 0;
    }

    .teacher-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 160px;
    }

    .teacher-photo {
      width: 140px;
      height: 140px;
      border-radius: 50%;
      background: #e4d5cd;  /* нейтральный фон-заглушка */
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3.5rem;
      color: #a78e81;
      box-shadow: 0 8px 18px #e7cfc0;
      margin-bottom: 1rem;
      transition: 0.3s;
      border: 3px solid #f5ded5;
    }

    .teacher-item:hover .teacher-photo {
      border-color: #f5b4a0;
      transform: scale(1.02);
    }

    .teacher-item h4 {
      font-size: 1.5rem;
      font-weight: 400;
      color: #7c6b60;
    }

    .teacher-item p {
      color: #af988b;
      font-size: 1rem;
    }

    /* ===== КОНТАКТЫ И КАРТА ===== */
    .contact-section {
      background: #fef6f2;  /* очень светлый персик */
      border-radius: 50px 50px 20px 20px;
      padding: 2.5rem 2rem;
    }

    .contact-flex {
      display: flex;
      flex-wrap: wrap;
      gap: 2.5rem;
      align-items: flex-start;
    }

    .contact-details {
      flex: 1 1 280px;
    }

    .contact-details p {
      margin: 1.3rem 0;
      display: flex;
      align-items: center;
      gap: 1.2rem;
      font-size: 1.2rem;
      background: #fffcf9;
      padding: 0.6rem 1.2rem;
      border-radius: 60px;
      box-shadow: 0 2px 8px #f2ded5;
    }

    .contact-details i {
      font-style: normal;
      font-size: 1.8rem;
      width: 2rem;
      color: #e6a692;
    }

    .map-container {
      flex: 2 1 500px;
      height: 350px;
      border-radius: 30px;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(190, 140, 120, 0.15);
      border: 2px solid #fff2ea;
    }

    .map-container iframe {
      width: 100%;
      height: 100%;
      border: 0;
      display: block;
    }

    /* ===== ФУТЕР ===== */
    footer {
      background: #e9dad2;  /* нежная светлая охра */
      color: #5d534b;
      text-align: center;
      padding: 2.2rem 1rem;
      margin-top: 3rem;
      font-size: 1.1rem;
    }

    .social-links {
      margin: 1rem 0 0.3rem;
    }

    .social-links a {
      color: #a48070;
      text-decoration: none;
      margin: 0 1rem;
      font-size: 1.7rem;
      transition: 0.2s;
      display: inline-block;
    }

    .social-links a:hover {
      color: #f08a7a;  /* акцент */
      transform: translateY(-3px);
    }

    /* мелочи */
    .highlight {
      color: #e6a692;
      font-weight: 400;
    }

    hr {
      border: none;
      height: 1px;
      background: linear-gradient(90deg, transparent, #f5c4b4, transparent);
      margin: 2rem 0;
    }

    @media (max-width: 800px) {
      header {
        flex-direction: column;
        text-align: center;
        gap: 0.5rem;
      }
      .logo-block {
        flex-direction: column;
        border-bottom: 1px dashed #f5c4b4;
        padding-bottom: 0.8rem;
      }
      .studio-name {
        border-left: none;
        padding-left: 0;
      }
      nav ul {
        justify-content: center;
        gap: 1.2rem;
        flex-wrap: wrap;
      }
      .contact-flex {
        flex-direction: column;
      }
      .section-title {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>

<!-- ХЕДЕР с логотипом -->
<header>
  <div class="logo-block">
    <!-- приложенное изображение Logo21.png -->
    <img src="Logo21.png" alt="Логотип студии творчества и каллиграфии">
    <span class="studio-name">Ладошки</span>
  </div>
  <nav>
    <ul>
      <li><a href="#">Главная</a></li>
      <li><a href="#">О нас</a></li>
      <li><a href="#">Занятия</a></li>
      <li><a href="#">Педагоги</a></li>
      <li><a href="#">Контакты</a></li>
    </ul>
  </nav>
</header>

<main>
  <!-- БЛОК 1: О студии (болванка под лого уже использована, здесь текст) -->
  <section class="container">
    <div class="about">
      <h2 class="section-title">Добро пожаловать в «Ладошки»</h2>
      <p>Мы — уютная студия, где дети знакомятся с миром творчества, каллиграфии и искусства.  Мягкая атмосфера, опытные педагоги и авторские программы помогают раскрыть таланты каждого ребёнка.</p>
    </div>
  </section>

  <!-- БЛОК 2: Направления (карточки) -->
  <section class="container">
    <h2 class="section-title">Чем мы занимаемся</h2>
    <div class="cards-grid">
      <div class="card">
        <h3>🖌️ Рисование</h3>
        <p>Акварель, гуашь, пастель — развиваем фантазию и чувство цвета.</p>
      </div>
      <div class="card">
        <h3>✍️ Каллиграфия</h3>
        <p>Красивый почерк, острые перья и буквы с душой. Для детей от 7 лет.</p>
      </div>
      <div class="card">
        <h3>🧶 Лепка</h3>
        <p>Глина, пластилин, масса для лепки — создаём объёмные истории.</p>
      </div>
      <div class="card">
        <h3>📖 Арт-терапия</h3>
        <p>Мягкие занятия для гармоничного развития и снятия напряжения.</p>
      </div>
    </div>
  </section>

  <!-- БЛОК 3: Преподаватели (кружки-заглушки) -->
  <section class="container">
    <h2 class="section-title">Наши педагоги</h2>
    <div class="teachers-wrapper">
      <div class="teacher-item">
        <div class="teacher-photo">👩‍🎨</div>
        <h4>Анна</h4>
        <p>художник, каллиграф</p>
      </div>
      <div class="teacher-item">
        <div class="teacher-photo">🧑‍🏫</div>
        <h4>Елена</h4>
        <p>керамист, скульптор</p>
      </div>
      <div class="teacher-item">
        <div class="teacher-photo">👩‍🦰</div>
        <h4>Мария</h4>
        <p>арт-терапевт</p>
      </div>
      <div class="teacher-item">
        <div class="teacher-photo">👨‍🎨</div>
        <h4>Дмитрий</h4>
        <p>график, иллюстратор</p>
      </div>
    </div>
  </section>

  <!-- БЛОК КОНТАКТЫ + КАРТА -->
  <section class="container contact-section">
    <h2 class="section-title">Контакты</h2>
    <div class="contact-flex">
      <!-- левая часть: контактные данные -->
      <div class="contact-details">
        <p><i>📍</i> ул. Творческая, д. 15, Москва</p>
        <p><i>📞</i> +7 (495) 123-45-67</p>
        <p><i>✉️</i> hello@ladoshki.art</p>
        <p><i>🕒</i> пн–пт: 10:00 – 19:00, сб: 11:00 – 17:00</p>
        <p><i>📷</i> @ladoshki_studio</p>
      </div>

      <!-- правая часть: интерактивная карта (OpenStreetMap) -->
      <div class="map-container">
        <!-- Вставка карты с меткой в центре Москвы (пример) -->
        <iframe src="https://www.openstreetmap.org/export/embed.html?bbox=37.6184%2C55.7512%2C37.6284%2C55.7612&amp;layer=mapnik&amp;marker=55.7562%2C37.6234" loading="lazy" referrerpolicy="no-referrer-when-downgrade" title="карта с меткой студии Ладошки"></iframe>
      </div>
    </div>
  </section>
</main>

<!-- ФУТЕР -->
<footer>
  <p>© 2026 Студия творчества «Ладошки»</p>
  <p>развитие через искусство и каллиграфию</p>
  <div class="social-links">
    <a href="#" title="Telegram">📱</a>
    <a href="#" title="VK">📘</a>
    <a href="#" title="WhatsApp">📞</a>
  </div>
  <p style="font-size: 0.9rem; margin-top: 1.5rem; opacity: 0.7;">сделано с любовью к детям</p>
</footer>

</body>
</html>
