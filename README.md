@@ -4,27 +4,67 @@
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="https://avatars.githubusercontent.com/u/191036346?s=400&u=5e0cfd2c82d417eac15602e7ea528698d989beb1&v=4" type="image/png"> <!-- Favicon -->
    <title>Cats Coding Batch</title>
    <title>CCB.exe</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: url('https://via.placeholder.com/1920x1080/ffddb3/ffffff?text=выгувыгувыгу') no-repeat center center fixed; /* Фоновое изображение */
            background: linear-gradient(to bottom right, #ff7e5f, #feb47b);
            background-size: cover;
            margin: 0;
            padding: 20px;
        }
        header {
            background: #e3a250; /* Оранжевый цвет */
            color: #fff;
            text-align: center;
            margin: 20px 0;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
        background: linear-gradient(to right, #feb47b, #ff7e5f); /* Градиентный фон */
        color: white; /* Цвет текста */
        text-align: center; /* Центрируем текст */
        padding: 40px 20px; /* Отступы */
        border-radius: 10px; /* Скругление углов */
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2); /* Тень */
        margin-bottom: 20px; /* Отступ снизу */
        }
        h1 {
            margin: 0;
        font-size: 2.5em; /* Размер заголовка */
        margin: 0; /* Убираем отступы */
        font-family: 'Arial', sans-serif; /* Шрифт заголовка */
        }
        .tagline {
        font-size: 1.2em; /* Размер текста */
        margin-top: 10px; /* Отступ сверху */
        font-family: 'Arial', sans-serif; /* Шрифт описания */
        }
        .info-section {
        margin: 20px 0;
        padding: 20px;
        background: #f9f9f9; /* Светлый фон */
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .info-section h2 {
        text-align: center; /* Центрируем заголовок секции */
        color: #333; /* Цвет заголовка секции */
        }
        .info-text h3 {
        margin: 0; /* Убираем отступы */
        color: #ffbb00; /* Цвет заголовка */
        }
        .info-text p {
        margin: 5px 0; /* Отступы для описания */
        color: #666; /* Цвет описания */
        line-height: 1.5; /* Межстрочный интервал */
        }
        .info-member {
        display: flex; /* Используем flexbox для выравнивания */
        align-items: center; /* Центрируем по вертикали */
        margin: 15px 0;
        padding: 20px; /* Увеличенные отступы для объема */
        background: #fff; /* Белый фон для участников */
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        section {
            margin: 20px 0;
            padding: 20px;
@@ -39,13 +79,50 @@
            color: #777;
        }
        .team-member {
            margin: 10px 0;
        display: flex; /* Используем flexbox для выравнивания */
        align-items: center; /* Центрируем по вертикали */
        margin: 15px 0;
        padding: 10px;
        background: #fff; /* Белый фон для участников */
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s; /* Плавный переход при наведении */
        }
        .team-member:hover {
        transform: scale(1.02); /* Увеличение при наведении */
        }
        .member-icon {
        font-size: 40px; /* Размер иконки */
        margin-right: 15px; /* Отступ между иконкой и текстом */
        }
        .member-info h3 {
        margin: 0; /* Убираем отступы */
        color: #ffa600; /* Цвет имени участника */
        }
        .member-info p {
        margin: 5px 0 0; /* Отступы для описания */
        color: #666; /* Цвет описания */
        }
        h2 {
        text-align: center;
        color: #333; /* Цвет заголовка */
        }
        .project {
            position: relative;
            background: #f9f9f9; /* Светлый фон */
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            transition: transform 0.3s; /* Плавный переход при наведении */
            text-decoration: none
        }
        .project:hover {
        transform: scale(1.02); /* Увеличение при наведении */
        }
        .project h3 {
            margin: 0;
@@ -62,70 +139,167 @@
            text-decoration: none;
        }
        .project a:hover {
            text-decoration: underline;
            text-decoration: none;
        }
        .social-links {
        .button {
            display: inline-block;
            padding: 10px 20px;
            margin-top: 10px;
            background-color: #ffddb3; /* Цвет фона */
            color: white; /* Цвет текста */
            text-decoration: none; /* Убираем подчеркивание */
            border-radius: 5px; /* Скругление углов */
            transition: background-color 0.3s, transform 0.3s; /* Плавный переход */
        }
        .social-links a {
            margin: 0 10px;
            color: #ff9422; /* Оранжевый цвет */
            text-decoration: none;
        }
        .social-links a:hover {
            text-decoration: underline;
        .button:hover {
        background-color: #c38942; /* Цвет фона при наведении */
        transform: scale(1.05); /* Увеличение кнопки при наведении */
        }
        .project-member {
        margin: 15px 0;
        padding: 20px; /* Увеличенные отступы для объема */
        background: linear-gradient(to right, #feb47b, #ff7e5f); /* Градиентный фон */
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        } 
    </style>
</head>
<body>

<header>
    <h1>Cats Coding Batch</h1>
    <p>Команда программистов, создающих удивительные проекты!</p>
    <div class="info-member">
      <div class="info-text">
          <h3>О нас</h3>
          <p>Мы — команда увлеченных программистов, работающих над различными проектами в области разработки программного обеспечения. Наша цель — создавать инновационные решения, которые делают жизнь людей проще и интереснее.</p>
      </div>
</header>
<section>
    <h2>О нас</h2>
    <p>Мы - группа увлеченных программистов, которые любят кодить и делиться своими знаниями. Наша цель - создавать качественные и инновационные решения для различных задач.</p>
</section>
<section>
    <h2>Участники команды</h2>
    <div class="team-member">🐱 FoxInaBoX - Главный прогромист</div>
    <div class="team-member">🐱 Random7YT - Саппортер</div>
  <h2>Участники команды</h2>
  <div class="team-member">
      <div class="member-icon">🐱</div>
      <div class="member-info">
          <h3>FoxInaBoX</h3>
          <p>Главный программист</p>
      </div>
  </div>
  <div class="team-member">
      <div class="member-icon">🐱</div>
      <div class="member-info">
          <h3>Random7YT</h3>
          <p>Саппортер</p>
      </div>
  </div>
</section>

<section>
    <h2>Проекты</h2>
    <div class="project">
        <h3>🐾 Проект 1: Активатор Windows - K.E.Y.S</h3>
        <img src="https://raw.githubusercontent.com/Cats-coding-batch/keys/main/K.E.Y.S.png" alt="Чо инет грузит, а?">
        <p>Программа **KEYS** — это активатор для операционных систем Windows, который позволяет генерировать ключи активации. Она предназначена для упрощения процесса активации Windows, обеспечивая пользователей необходимыми ключами для различных версий ОС. Программа может использоваться как для личных нужд.</p>
        <a href="https://github.com/Cats-coding-batch/keys" target="_blank">Посмотреть проект</a>
        <a href="https://www.youtube.com/watch?v=jdXdT3TkYiA" class="status ready">✅ Готово</a>
        <img src="https://i.imgur.com/m2eWvSm.png" alt="Чо инет грузит, а?">
        <p>KEYS — это активатор для операционных систем Windows, который позволяет генерировать ключи активации. Она предназначена для упрощения процесса активации Windows, обеспечивая пользователей необходимыми ключами для различных версий ОС</p>
    </div>
    <div class="project">
        <h3>🐾 Проект 2: Портфолио для дизайнеров</h3>
        <img src="https://via.placeholder.com/400x200" alt="Портфолио для дизайнеров">
        <p>Интерактивное портфолио, позволяющее дизайнерам демонстрировать свои работы. Использует HTML, CSS и JavaScript.</p>
        <a href="https://example.com/project2" target="_blank">Посмотреть проект</a>
        <h3>🐾 Проект 2: Tweaker</h3>
        <a href="https://www.youtube.com/watch?v=jdXdT3TkYiA" class="status in-development">🔄 В разработке</a>
        <img src="https://via.placeholder.com/400x200" alt="ааа">
        <p>Проект в разработке, подробности позже</p>
        <a href="https://example.com/project3" target="_blank" class="button">Посмотреть проект</a>
    </div>
    <div class="project">
        <h3>🐾 Проект 3: Чат-бот для поддержки клиентов</h3>
          <a href="https://www.youtube.com/watch?v=jdXdT3TkYiA" class="status beta">🛠️ Бета</a>
        <img src="https://via.placeholder.com/400x200" alt="Чат-бот для поддержки клиентов">
        <p>Чат-бот, который отвечает на часто задаваемые вопросы и помогает пользователям находить нужную информацию. Разработан с использованием Python и Flask.</p>
        <a href="https://example.com/project3" target="_blank">Пос мотреть проект</a>
        <a href="https://example.com/project3" target="_blank" class="button">Посмотреть проект</a>
    </div>
</section>
<style>
  .status {
  position: absolute; /* Абсолютное позиционирование */
  bottom: 10px; /* Отступ от нижней границы */
  right: 10px; /* Отступ от правой границы */
  font-weight: bold;
  padding: 5px 10px;
  border-radius: 5px;
  display: inline-block;
  margin-top: 5px;
  color: white; /* Цвет текста статуса */
  text-decoration: none; /* Убираем подчеркивание */
  transition: background-color 0.3s; /* Плавный переход */
  }
  .status:hover {
  opacity: 0.8; /* Эффект при наведении */
  }
  .ready {
  background-color: #28a745; /* Зеленый для готового */
  }
  .in-development {
  background-color: #ffc107; /* Желтый для в разработке */
  }

<section>
    <h2>Контакты</h2>
    <p>Если у вас есть вопросы или предложения, свяжитесь с нами по электронной почте: <a href="mailto:info@catscodingbatch.com">TEST BOBRA</a></p>
    <div class="social-links">
        <a href="https://facebook.com/catscodingbatch" target="_blank">Telegram</a>
        <a href="https://twitter.com/catscodingbatch" target="_blank">GitHub</a>
  .beta {
  background-color: #17a2b8; /* Голубой для бета */
  }
</style>
<section class="contact-section">
  <h2>Контакты</h2>
  <div class="social-links">
    <div class="social-member">
      <a href="https://t.me/Cats_coding_batch" target="_blank" class="social-button">
          <img src="https://img.icons8.com/color/48/000000/telegram-app.png" alt="Telegram" class="social-icon"> Telegram
      </a>
      <a href="https://github.com/Cats-coding-batch/" target="_blank" class="social-button">
          <img src="https://img.icons8.com/color/48/000000/github.png" alt="GitHub" class="social-icon"> GitHub
      </a>
    </div>
  </div>
</section>

<style>
  .social-links {
      display: flex; /* Используем flexbox для выравнивания */
      justify-content: center; /* Центрируем кнопки */
      gap: 20px; /* Отступ между кнопками */
  }
  .social-button {
      display: flex; /* Используем flexbox для иконки и текста */
      align-items: center; /* Центрируем по вертикали */
      background: #ffddb3; /* Цвет фона кнопки */
      color: rgb(131, 55, 0); /* Цвет текста */
      padding: 10px 15px; /* Отступы */
      border-radius: 5px; /* Скругление углов */
      text-decoration: none; /* Убираем подчеркивание */
      transition: background-color 0.3s, transform 0.3s; /* Плавный переход */
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1); /* Тень */
      margin: 0 10px; /* Отступ между кнопками */
  }
  .social-button:hover {
      background: #c38942; /* Цвет фона при наведении */
      transform: scale(1.05); /* Увеличение при наведении */
  }
  .social-icon {
      margin-right: 8px; /* Отступ между иконкой и текстом */
      width: 24px; /* Ширина иконки */
      height: auto; /* Автоматическая высота */
  }
  .social-member {
      display: flex; /* Используем flexbox для выравнивания */
      align-items: center; /* Центрируем по вертикали */
      margin: 15px 0;
      padding: 20px; /* Увеличенные отступы для объема */
      background: linear-gradient(to right, #feb47b, #ff7e5f); /* Градиентный фон */
      border-radius: 5px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
</style>
<footer>
    <p>&copy; 2077 Cats Coding Batch. Все права не защищены. (Бета верисия оаоао)</p>
</footer>
