
# Методичка по созданию сайта "Грузовозофф"

Эта методичка описывает процесс создания сайта для компании "Грузовозофф", предоставляющей услуги грузоперевозок. Сайт включает основные разделы: шапку, вступительный блок, информацию о компании, преимущества, форму обратной связи и подвал. В методичке рассматриваются структура HTML, стили CSS и базовая JavaScript-логика.

## 1. Общая структура проекта

Проект состоит из двух основных файлов:
- `index.html` — HTML-разметка страницы.
- `css/style.css` — файл стилей для оформления страницы.

Также используется шрифт Inter, подключенный через Google Fonts.

## 2. HTML-разметка (`index.html`)

HTML-структура включает следующие основные секции:
- **Шапка (`header`)**: Логотип и навигация с ссылками на регистрацию и авторизацию.
- **Вступительный блок (`section-intro`)**: Приветственный текст и кнопка "Узнать".
- **О нас**: Информация о компании и изображение.
- **Преимущества**: Три блока с описанием ключевых преимуществ компании.
- **Форма обратной связи**: Простая форма с полями для имени, телефона и комментария.
- **Подвал (`footer`)**: Копирайт с годом.

### Код HTML


<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>Сайт</title>
	<link rel="stylesheet" href="css/style.css">
</head>
<body>
	<header>
		<div class="header-container">
			<a class="header-logo" href="index.html">Грузовозофф</a>
			<nav>
				<a class="header-link" href="registration.html">Регистрация</a>
				<a class="header-link" href="login.html">Авторизация</a>
			</nav>
		</div>
	</header>

	<section class="section-intro">
		<div class="container">
			<div class="intro">
				<h1>Грузовозофф</h1>
				<p>Мы предоставляем услуги грузоперевозок по всей стране c широким спектром услуг, включая экспедирование и складские услуги. Быстро, надежно и безопасно.</p>
				<a href="#">Узнать</a>
			</div>
		</div>
	</section>

	<section>
		<div class="container">
			<h2>О нас</h2>
			<div class="about">
				<div class="about-block">
					<h3>О компании</h3>
					<p>Грузовозофф - это команда профессионалов, которая занимается грузоперевозками с 2005 года.</p>
				</div>
				<div class="about-block">
					<img src="./img/image.jpg">
				</div>
			</div>
		</div>
	</section>

	<section>
		<div class="container">
			<h2>Преимущества</h2>
			<div class="adv">
				<div class="adv-block">
					<h3>Надежность</h3>
					<p>Мы ценим ваше время и гарантируем быструю доставку грузов.</p>
				</div>
				<div class="adv-block">
					<h3>Безопасность</h3>
					<p>Все грузы застрахованы, что обеспечивает дополнительную защиту.</p>
				</div>
				<div class="adv-block">
					<h3>Профессионализм</h3>
					<p>Наша команда состоит из опытных специалистов в области логистики.</p>
				</div>
			</div>
		</div>
	</section>

	<section>
		<div class="container">
			<h2>Оставьте заявку</h2>
			<div class="feedback">
				<div class="feedback-block">
					<form class="feedback-form">
						<input type="text" placeholder="Федор" required>
						<input type="tel" placeholder="+7 (123) 456-78-90" required>
						<input type="text" placeholder="Ваш комментарий" required>
						<button id="feedback-btn" type="button">Оставить заявку</button>
					</form>
				</div>
			</div>
		</div>
	</section>

	<footer>
		<p>(С) 2025. Все права защищены</p>
	</footer>
</body>

<script>
    document.getElementById("feedback-btn").onclick = function() {
	  alert("Спасибо за ваш интерес! Мы свяжемся с вами в ближайшее время.");
	}
</script>
</html>


### Основные элементы HTML
- Используется семантическая разметка с тегами `<header>`, `<section>`, `<nav>`, `<footer>`.
- Контейнер `.container` ограничивает ширину контента до 1200px.
- Форма обратной связи содержит три поля ввода и кнопку с обработчиком события в JavaScript.

## 3. CSS-стили (`style.css`)

Стили определяют внешний вид сайта, включая шрифты, цвета, отступы и адаптивное отображение блоков. Используется шрифт Inter, подключенный через Google Fonts.

### Код CSS

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

* {
	margin: 0 auto;
	padding: 0;
	font-family: Inter, sans-serif;
	line-height: 1.6em;
}

a {
	text-decoration: none;
}

h1 {
	text-align: center;
	margin: 30px 0;
	font-size: 64px;
}

h2 {
	font-size: 48px;
	margin: 60px 0;
	text-align: center;
}

h3 {
	margin-bottom: 10px;
	font-size: 30px;
}

p {
	font-size: 18px;
}

button {
	background-color: dodgerblue;
	padding: 8px 36px;
	border: none;
	border-radius: 30px;
	cursor: pointer;
	color: white;
	font-size: 20px;
	transition: background-color 0.3s;
}

button:hover {
	background-color: blue;
}

.container {
	max-width: 1200px;
	margin: 0 auto;
}

section {
	padding: 100px 0;
}

header {
	background-color: dodgerblue;
	padding: 20px 0;
}

.header-container {
	width: 1200px;
	display: flex;
	justify-content: space-between;
}

header a {
	color: white;
	margin: 0;
}

header a:hover {
	text-decoration: underline;
}

header nav {
	margin: 0;
}

.header-link:last-child {
	margin-left: 15px;
}

.section-intro {
	padding: 180px 0;
}

.intro {
	text-align: center;
}

.intro p {
	width: 840px;
	font-size: 24px;
	margin-bottom: 60px;
}

.intro a {
    background-color: dodgerblue;
    color: white;
    padding: 12px 48px;
    font-size: 24px;
    border-radius: 30px;
    transition: background-color 0.3s ease;
}

.intro a:hover {
    background-color: blue;
}

.about {
	display: flex;
	justify-content: space-around;
	align-items: center;
}

.about-block {
	width: 600px;
	text-align: center;
}

.about-block:first-child {
	width: 400px;
}

.about img {
	width: 600px;
	height: 400px;
}

.adv {
	display: flex;
	justify-content: space-between;
	text-align: center;
}

.adv-block p {
	width: 360px;
}

.feedback {
	display: flex;
	justify-content: space-around;
	align-items: center;
	text-align: center;
}

.feedback-block input {
	padding: 0 20px;
	height: 60px;
	width: 90%;
	font-size: 16px;
	margin: 20px 0;
}

.feedback-block button {
	margin-top: 20px;
}

footer {
	background-color: dodgerblue;
	padding: 20px 0;
	text-align: center;
	margin-top: 80px;
}

footer p {
	font-size: 16px;
	color: white;
}
```

### Основные особенности стилей
- **Шрифты**: Используется шрифт Inter с различными весами (300–800).
- **Цвета**: Основной цвет — `dodgerblue`, при наведении используется более темный `blue`.
- **Контейнеры**: Класс `.container` ограничивает ширину контента до 1200px.
- **Flexbox**: Используется для выравнивания блоков в секциях "О нас", "Преимущества" и "Обратная связь".
- **Анимации**: Плавные переходы для кнопок и ссылок при наведении (`transition: background-color 0.3s`).

## 4. JavaScript-логика

JavaScript используется для обработки клика по кнопке формы обратной связи, выводящей уведомление.

### Код JavaScript
JavaScript-код встроен в HTML-файл в теге `<script>`:

```javascript
document.getElementById("feedback-btn").onclick = function() {
    alert("Спасибо за ваш интерес! Мы свяжемся с вами в ближайшее время.");
}
```

### Описание
- Обработчик события `onclick` привязан к кнопке с `id="feedback-btn"`.
- При клике выводится всплывающее сообщение с помощью `alert`.

## 5. Рекомендации по улучшению

1. **Адаптивность**: Добавить медиа-запросы в CSS для поддержки мобильных устройств.
2. **Валидация формы**: Реализовать проверку введенных данных (например, формат телефона).
3. **Доступность**: Добавить атрибуты ARIA для улучшения доступности.
4. **Изображения**: Убедиться, что путь к изображению (`./img/image.jpg`) корректен, или заменить на реальное изображение.
5. **SEO**: Добавить мета-теги (description, keywords) для улучшения поисковой оптимизации.

## 6. Инструкции по запуску

1. Создайте папку проекта.
2. Поместите `index.html` и папку `css` с файлом `style.css` в эту папку.
3. Убедитесь, что папка `img` содержит изображение `image.jpg` (или обновите путь в HTML).
4. Откройте `index.html` в браузере для просмотра сайта.

</xaiArtifact>
