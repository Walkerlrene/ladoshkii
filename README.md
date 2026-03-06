<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Студия творчества Ладошки</title>
    <style>
        /* Общие сбросы и мягкая цветовая палитра */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #fefaf5; /* очень теплый, нежный фон */
            color: #4a4a4a; /* мягкий серый для текста */
            line-height: 1.6;
        }

        /* Акцентный цвет (персиковый/коралловый) */
        .accent {
            color: #ff9f8c; /* акцент для текста */
        }
        .accent-bg {
            background-color: #ffb6a3; /* более нежный акцент для фона кнопок */
            color: white;
        }
        .accent-border {
            border-color: #ff9f8c;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Хэдер */
        header {
            background-color: #ffffffd9; /* полупрозрачный белый для легкости */
            backdrop-filter: blur(5px);
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.03);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 10;
            border-bottom: 1px solid #ffe3d8;
        }

        .header-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        /* Болванка под лого */
        .logo-placeholder {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .logo-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #ffd5c2, #ffe8df);
            border-radius: 50%; /* круг, как отпечаток ладошки */
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ff9f8c;
            font-size: 24px;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(255, 159, 140, 0.2);
            border: 2px solid #ffd5c2;
        }
        .logo-text {
            font-size: 24px;
            font-weight: 300;
            letter-spacing: 2px;
            color: #6b5a54;
        }
        .logo-text span {
            font-weight: 600;
            color: #ff8a73;
        }

        /* Навигация */
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        nav a {
            text-decoration: none;
            color: #5f5f5f;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 16px;
        }
        nav a:hover {
            color: #ff8a73;
        }

        /* Блоки */
        .section {
            padding: 70px 0;
            border-bottom: 1px solid #ffe9e0;
        }
        .section:last-of-type {
            border-bottom: none;
        }

        .section-title {
            font-size: 36px;
            font-weight: 300;
            margin-bottom: 40px;
            text-align: center;
            color: #6b5a54;
        }
        .section-title span {
            font-weight: 500;
            color: #ff9f8c;
        }

        /* Герой (приветственный блок) */
        .hero {
            background: linear-gradient(135deg, #fff2ea, #fffaf5);
            border-radius: 30px;
            padding: 50px 40px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 20px;
            box-shadow: 0 10px 25px rgba(255, 159, 140, 0.1);
        }
        .hero-content {
            flex: 1 1 300px;
        }
        .hero-content h1 {
            font-size: 48px;
            font-weight: 300;
            margin-bottom: 20px;
            color: #4e3e38;
        }
        .hero-content h1 strong {
            font-weight: 600;
            color: #ff8a73;
        }
        .hero-content p {
            font-size: 18px;
            margin-bottom: 30px;
            color: #7a6a64;
        }
        .btn {
            display: inline-block;
            padding: 12px 35px;
            background-color: #ffb6a3;
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(255, 159, 140, 0.3);
            transition: background 0.3s, transform 0.2s;
            border: none;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #ff9f8c;
            transform: scale(1.02);
        }
        .hero-image {
            flex: 0 0 200px;
            height: 200px;
            background: #ffd5c2;
            border-radius: 50% 50% 50% 20%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            color: #ffb6a3;
            box-shadow: 0 15px 20px rgba(0,0,0,0.05);
        }

        /* Сетка для блоков с занятиями и преимуществами */
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }
        .card {
            background: white;
            padding: 30px 20px;
            border-radius: 30px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.02);
            text-align: center;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid #ffede6;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(255, 159, 140, 0.15);
            border-color: #ffd5c2;
        }
        .card-icon {
            font-size: 48px;
            margin-bottom: 15px;
            color: #ffb6a3;
        }
        .card h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: #6b5a54;
        }
        .card p {
            color: #8f7e78;
            font-size: 15px;
        }

        /* Контакты + карта */
        .contacts-map-wrapper {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            background: white;
            border-radius: 40px;
            padding: 40px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.02);
            border: 1px solid #ffede6;
        }
        .contacts-info {
            flex: 1 1 250px;
        }
        .contacts-info h3 {
            font-size: 28px;
            font-weight: 400;
            margin-bottom: 25px;
            color: #6b5a54;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
            font-size: 18px;
        }
        .contact-item .emoji {
            font-size: 24px;
            background: #ffede6;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }
        .map-placeholder {
            flex: 2 1 400px;
            background: #f0eae7;
            border-radius: 30px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 250px;
            border: 2px dashed #ffd5c2;
            color: #9e8d86;
        }
        .map-placeholder .map-text {
            font-size: 16px;
            margin-bottom: 10px;
            background: white;
            padding: 5px 15px;
            border-radius: 40px;
        }
        .fake-map-grid {
            display: grid;
            grid-template-columns: repeat(10, 1fr);
            gap: 3px;
            width: 100%;
            max-width: 400px;
        }
        .fake-map-cell {
            aspect-ratio: 1/1;
            background: #ffd5c2;
            border-radius: 4px;
            opacity: 0.5;
        }
        .fake-map-cell.accent {
            background: #ff9f8c;
            opacity: 1;
        }

        /* Футер */
        footer {
            background: #fff2ea;
            padding: 30px 0;
            margin-top: 30px;
            border-top: 1px solid #ffe3d8;
            color: #7a6a64;
        }
        .footer-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px;
        }
        .footer-logo-small {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .footer-logo-small .logo-icon {
            width: 35px;
            height: 35px;
            font-size: 18px;
        }
        .copyright {
            font-size: 14px;
        }
        .social-icons {
            display: flex;
            gap: 20px;
        }
        .social-icons span {
            background: white;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.02);
            color: #ff9f8c;
            font-weight: 600;
            border: 1px solid #ffd5c2;
        }

        /* адаптив */
        @media (max-width: 700px) {
            .header-inner {
                flex-direction: column;
                gap: 15px;
            }
            nav ul {
                gap: 15px;
                flex-wrap: wrap;
                justify-content: center;
            }
            .hero-content h1 {
                font-size: 36px;
            }
            .section-title {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>

    <!-- Хэдер -->
    <header>
        <div class="container header-inner">
            <!-- болванка под лого -->
            <div class="logo-placeholder">
                <div class="logo-icon">🖐️</div>
                <div class="logo-text">студия <span>Ладошки</span></div>
            </div>
            <nav>
                <ul>
                    <li><a href="#about">О нас</a></li>
                    <li><a href="#classes">Занятия</a></li>
                    <li><a href="#contacts">Контакты</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <!-- Герой-блок (приветствие) -->
        <section class="hero">
            <div class="hero-content">
                <h1>Творим с <strong>радостью</strong></h1>
                <p>Студия творчества «Ладошки» — мягкое развитие и яркие открытия для ваших детей от 2 до 10 лет.</p>
                <a href="#contacts" class="btn">Записаться</a>
            </div>
            <div class="hero-image">
                🎨✨
            </div>
        </section>

        <!-- Блок "О нас" -->
        <section id="about" class="section">
            <h2 class="section-title"><span>Немного</span> о нас</h2>
            <div class="cards-grid">
                <div class="card">
                    <div class="card-icon">🖌️</div>
                    <h3>Авторский подход</h3>
                    <p>Занятия, которые развивают воображение и мелкую моторику через игру и творчество.</p>
                </div>
                <div class="card">
                    <div class="card-icon">👩‍🎨</div>
                    <h3>Опытные педагоги</h3>
                    <p>Наши преподаватели — молодые художники и педагоги с большим сердцем.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🏡</div>
                    <h3>Уютная студия</h3>
                    <p>Светлое пространство, где каждый ребенок чувствует себя как дома.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🌟</div>
                    <h3>Маленькие группы</h3>
                    <p>До 6 человек, чтобы уделить внимание каждому юному творцу.</p>
                </div>
            </div>
        </section>

        <!-- Блок "Занятия" -->
        <section id="classes" class="section">
            <h2 class="section-title">Наши <span>занятия</span></h2>
            <div class="cards-grid">
                <div class="card">
                    <div class="card-icon">🎨</div>
                    <h3>Рисование</h3>
                    <p>Акварель, гуашь, пальчиковые краски — от 3 лет.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🤲</div>
                    <h3>Лепка</h3>
                    <p>Пластилин, тесто, глина — развиваем тактильные ощущения.</p>
                </div>
                <div class="card">
                    <div class="card-icon">✂️</div>
                    <h3>Аппликация</h3>
                    <p>Создаем коллажи из бумаги, ткани и природных материалов.</p>
                </div>
                <div class="card">
                    <div class="card-icon">🎭</div>
                    <h3>Мастер-классы</h3>
                    <p>Тематические праздники и творческие проекты для всей семьи.</p>
                </div>
            </div>
        </section>

        <!-- Блок Контакты + Карта (визуальная болванка) -->
        <section id="contacts" class="section">
            <h2 class="section-title"><span>Как</span> нас найти</h2>
            <div class="contacts-map-wrapper">
                <div class="contacts-info">
                    <h3>Контакты</h3>
                    <div class="contact-item">
                        <span class="emoji">📍</span> ул. Малышей, д. 15
                    </div>
                    <div class="contact-item">
                        <span class="emoji">📞</span> +7 (999) 123-45-67
                    </div>
                    <div class="contact-item">
                        <span class="emoji">✉️</span> hello@ladoshki.studio
                    </div>
                    <div class="contact-item">
                        <span class="emoji">🕒</span> Пн-Пт: 9:00–19:00, Сб: 10:00–16:00
                    </div>
                    <div style="margin-top: 30px;">
                        <a href="#" class="btn" style="padding: 10px 25px; font-size: 16px;">Позвонить</a>
                    </div>
                </div>
                <!-- Болванка под карту (декоративная) -->
                <div class="map-placeholder">
                    <div class="map-text">🗺️ Здесь будет карта (Яндекс/Google Maps)</div>
                    <div class="fake-map-grid">
                        <!-- просто декоративная сетка как намёк на карту -->
                        <div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div>
                        <div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div>
                        <div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div>
                        <div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div>
                        <div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell accent"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div><div class="fake-map-cell"></div>
                    </div>
                    <p style="margin-top: 15px; font-size: 14px;">м. Творческая, 5 минут пешком</p>
                </div>
            </div>
        </section>
    </main>

    <!-- Футер -->
    <footer>
        <div class="container footer-inner">
            <div class="footer-logo-small">
                <div class="logo-icon">🖐️</div>
                <span>студия Ладошки</span>
            </div>
            <div class="copyright">
                © 2025 Ладошки. С любовью к детям.
            </div>
            <div class="social-icons">
                <span>📷</span>
                <span>📘</span>
                <span>🎵</span>
            </div>
        </div>
    </footer>

    <!-- Небольшой скрипт для плавного скролла по якорям (необязательно) -->
    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });
    </script>
</body>
</html>
