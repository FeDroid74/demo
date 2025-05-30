# Учебное пособие по веб-разработке

Данный документ представляет собой сборник исходных кодов для веб-приложения, разработанного в рамках учебного проекта. Код каждого файла представлен в неизменном виде и сопровождается только названием файла. Материалы структурированы для удобства изучения и повторения, предназначены для использования в образовательных целях.

---

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Грузовозофф</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
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
				<!-- <div class="adv-block">
                    <h3>Доступные цены</h3>
                    <p>Мы предлагаем конкурентоспособные цены на все наши услуги.</p>
                </div> -->
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
						<input type="tel" pattern="^\+7\(\d{3}\)-\d{3}-\d{2}-\d{2}$" placeholder="+7 (123) 456-78-90" required>
						<input type="text" placeholder="Ваш комментарий" required>
						<button id="feedback-btn" type="button">Отправить</button>
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
	// document.querySelector('.feedback-btn').addEventListener('click', function() {
    //     alert("Спасибо за ваш интерес! Мы свяжемся с вами в ближайшее время.");
    // });

    document.getElementById("feedback-btn").onclick = function() {
	  alert("Спасибо за ваш интерес! Мы свяжемся с вами в ближайшее время.");
	}
</script>

</html>
```

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
	max-width: 1200px;
	width: 100%;
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
	width: 100%;
	max-width: 600px;
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

@media (max-width: 390px) {
	.container {
        max-width: 100%;
        padding: 0 15px;
    }

    h1 {
        font-size: 36px;
        margin: 20px 0;
    }

    h2 {
        font-size: 28px;
        margin: 40px 0;
    }

    h3 {
        font-size: 20px;
        margin-bottom: 8px;
    }

    p {
        font-size: 16px;
    }

    section {
        padding: 50px 0;
    }

    .header-container {
        width: 100%;
        flex-direction: column;
        align-items: center;
    }

    .header-logo {
        font-size: 24px;
        margin-bottom: 10px;
    }

    header nav {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .header-link {
        margin: 5px 0 !important;
        font-size: 16px;
    }

    .header-link:last-child {
        margin-left: 0;
    }

    .section-intro {
        padding: 60px 0;
    }

    .intro p {
        width: 100%;
        font-size: 18px;
        margin-bottom: 30px;
    }

    .intro a {
        padding: 10px 30px;
        font-size: 18px;
    }

    .about {
        flex-direction: column;
    }

    .about-block {
        width: 100% !important;
        margin-bottom: 20px;
    }

	.about-block p {
		width: 90%;
		margin-bottom: 20px;
	}

    .about-block img {
        width: 100%;
        height: auto;
    }

    .adv {
        flex-direction: column;
        align-items: center;
    }

    .adv-block {
        width: 100%;
        margin-bottom: 20px;
    }

    .adv-block p {
        width: 100%;
    }

    .feedback-block input {
        width: 70%;
        height: 50px;
        font-size: 14px;
        margin: 10px 0;
    }

    .feedback-block button {
        font-size: 16px;
        padding: 8px 24px;
    }

    footer {
        margin-top: 40px;
        padding: 15px 0;
    }

    footer p {
        font-size: 14px;
    }
}
```

```php
<?php
$host = 'localhost';
$dbname = 'demo';
$username = 'root';
$password = '';

$pdo = new PDO("mysql:host=$host;dbname=$dbname", $username, $password);
?>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Регистрация</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="css/main.css">
</head>
<body>
	<a class="back" href="index.html">Назад</a>

	<form action="/server/registration.php" method="post">
		<input type="text" minlength="6" name="username" placeholder="Введите логин" required>
		<input type="password" minlength="6" name="password" placeholder="Введите пароль" required>
		<input type="text" name="fullname" placeholder="Введите ФИО" required>
		<input type="tel" name="telnum" pattern="^\+7\(\d{3}\)-\d{3}-\d{2}-\d{2}$" placeholder="Введите номер телефона" required>
		<input type="email" name="email" placeholder="Введите адрес электронной почты" required>
		<button type="submit">Зарегистрироваться</button><br><br>
		<a href="login.html">Уже зарегистрированы?</a>
	</form>
</body>
</html>
```

```php
<?php
require 'db.php';

$username = $_POST['username'];
$password = $_POST['password'];
$fullname = $_POST['fullname'];
$telnum = $_POST['telnum'];
$email = $_POST['email'];
$role = 0;

$sql = "INSERT INTO user (username, password, fullname, telnum, email, role)
        VALUES ('$username', '$password', '$fullname', '$telnum', '$email', $role)";

if ($pdo->exec($sql)) {
    header('Location: ../login.html');
} else {
    echo "Ошибка регистрации.";
}
?>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Вход</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="css/main.css">
</head>
<body>
	<a class="back" href="index.html">Назад</a>

	<form action="/server/login.php" method="post">
		<input type="text" name="username" placeholder="Введите логин" required>
		<input type="password" name="password" placeholder="Введите пароль" required>
		<button type="submit">Войти</button><br><br>
		<a href="registration.html">Нет аккаунта?</a>
	</form>
</body>
</html>
```

```php
<?php
require 'db.php';

$username = $_POST['username'];
$password = $_POST['password'];

$sql = "SELECT * FROM user WHERE username = '$username' AND password = '$password'";
$result = $pdo->query($sql);
$user = $result->fetch();

if ($user) {
    if ($user['role'] == 1) {
        header('Location: ../admin.php');
    } else {
        header('Location: ../account.php');
    }
} else {
    echo "Неверный логин или пароль.";
}
?>
```

```php
<?php
require './server/db.php';

$user = $pdo->query("SELECT id, username, fullname, telnum, email FROM user");
$feedback = $pdo->query("SELECT name, telnum, date, time, weight, type, departure, delivery FROM feedback");
?>

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Админ-панель</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="css/main.css">
</head>
<body>
	<div>
		<a class="back" href="index.html">Выйти</a>

		<h1>Пользователи</h1>
		<table>
			<thead>
				<tr>
					<th>ID</th>
					<th>Логин</th>
					<th>ФИО</th>
					<th>Телефон</th>
					<th>Email</th>
				</tr>
			</thead>
			<tbody>
				<?php foreach ($user as $row): ?>
					<tr>
						<td><?= htmlspecialchars($row['id']) ?></td>
						<td><?= htmlspecialchars($row['username']) ?></td>
						<td><?= htmlspecialchars($row['fullname']) ?></td>
						<td><?= htmlspecialchars($row['telnum']) ?></td>
						<td><?= htmlspecialchars($row['email']) ?></td>
					</tr>
				<?php endforeach; ?>
			</tbody>
		</table>

		<br><br>
		
		<h1>Заявки</h1>
		<table>
			<thead>
				<tr>
					<th>Имя отправителя</th>
					<th>Номер телефона</th>
					<th>Дата</th>
					<th>Время</th>
					<th>Вес посылки</th>
					<th>Тип посылки</th>
					<th>Адрес отправления</th>
					<th>Адрес доставки</th>
					<th>Статус посылки</th>
				</tr>
			</thead>
			<tbody>
				<?php foreach ($feedback as $row): ?>
					<tr>
						<td><?= htmlspecialchars($row['name']) ?></td>
						<td><?= htmlspecialchars($row['telnum']) ?></td>
						<td><?= htmlspecialchars($row['date']) ?></td>
						<td><?= htmlspecialchars($row['time']) ?></td>
						<td><?= htmlspecialchars($row['weight']) ?></td>
						<td><?= htmlspecialchars($row['type']) ?></td>
						<td><?= htmlspecialchars($row['departure']) ?></td>
						<td><?= htmlspecialchars($row['delivery']) ?></td>
						<td>
							<select>
								<option value="pending">Новая</option>
								<option value="in_progress">В процессе</option>
								<option value="canceled">Отменено</option>
							</select>
						</td>
					</tr>
				<?php endforeach; ?>
			</tbody>
		</table>
	</div>
</body>
</html>
```

```php
<?php
require './server/db.php';

$feedback = $pdo->query("SELECT name, telnum, date, time, weight, type, departure, delivery FROM feedback");
?>

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Личный кабинет</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="css/main.css">
</head>
<body>
	<div>
		<a class="back" href="index.html">Выйти</a>

		<h1>Заявки</h1>
		<table>
			<thead>
				<tr>
					<th>Имя отправителя</th>
					<th>Номер телефона</th>
					<th>Дата</th>
					<th>Время</th>
					<th>Вес посылки</th>
					<th>Тип посылки</th>
					<th>Адрес отправления</th>
					<th>Адрес доставки</th>
				</tr>
			</thead>
			<tbody>
				<?php foreach ($feedback as $row): ?>
					<tr>
						<td><?= htmlspecialchars($row['name']) ?></td>
						<td><?= htmlspecialchars($row['telnum']) ?></td>
						<td><?= htmlspecialchars($row['date']) ?></td>
						<td><?= htmlspecialchars($row['time']) ?></td>
						<td><?= htmlspecialchars($row['weight']) ?></td>
						<td><?= htmlspecialchars($row['type']) ?></td>
						<td><?= htmlspecialchars($row['departure']) ?></td>
						<td><?= htmlspecialchars($row['delivery']) ?></td>
					</tr>
				<?php endforeach; ?>
			</tbody>
		</table>

		<br><br>

		<form action="/server/feedback.php" method="post">
			<input placeholder="Введите имя" name="name">
			<input type="tel" placeholder="Введите номер телефона" name="telnum">
			<input type="date" name="date">
			<input type="time" name="time">
			<input placeholder="Введите вес груза" name="weight">
			<input placeholder="Введите тип груза" name="type">
			<input placeholder="Введите адрес отправления" name="departure">
			<input placeholder="Введите адрес доставки" name="delivery">
			<button type="submit">Отправить</button>
		</form>
	</div>
</body>
</html>
```

```php
<?php
require 'db.php';

$name = $_POST['name'];
$telnum = $_POST['telnum'];
$date = $_POST['date'];
$time = $_POST['time'];
$weight = $_POST['weight'];
$type = $_POST['type'];
$departure = $_POST['departure'];
$delivery  = $_POST['delivery'];

$sql = "INSERT INTO feedback (name, telnum, date, time, weight, type, departure, delivery)
		VALUES ('$username', '$telnum', '$date', '$time', '$weight', '$type', '$departure', '$delivery')";

if ($pdo->exec($sql)) {
	echo 'Заявка успешно отправлена';
} else {
	echo 'Ошибка оформления заявки';
}
?>
```

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

* {
	margin: 0 auto;
	padding: 0;
	font-family: Inter, sans-serif;
}

body {
	width: 1200px;
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
	min-height: 100vh;
}

input {
	padding: 0 20px;
	margin-bottom: 30px;
	font-size: 16px;
	height: 60px;
	width: 92%;
}

button {
	background-color: dodgerblue;
	color: #fff;
	padding: 10px 24px;
	font-size: 20px;
	padding: 12px 36px;
	cursor: pointer;
	border: none;
	border-radius: 30px;
	transition: background-color 0.3s;
}

button:hover {
	background-color: blue;
}

div {
	width: 100%;
	padding: 40px;
	text-align: center;
}

h1 {
	margin-bottom: 30px;
}

a {
    color: dodgerblue;
	text-decoration: none;
    transition: color 0.3s ease;
}

a:hover {
    text-decoration: underline;
}

.back {
	position: absolute;
	top: 30px;
    left: 40px;
}

table {
	width: 96%;
	border-collapse: collapse;
	margin-top: 20px;
}

th, td {
	padding: 15px;
	border: 1px solid gray;
	text-align: center;
}

th {
	background-color: dodgerblue;
	color: white;
}

select {
    background-color: white;
    padding: 10px;
    border: gray 1px solid;
}

@media screen and (max-width: 390px) {
    body {
        width: 100%;
        padding: 0 10px;
    }

	form {
		margin-left: -20px;
	}

    input {
        width: 80%;
        height: 50px;
        font-size: 14px;
        margin-bottom: 20px;
        padding: 0 10px;
    }

    button {
        font-size: 16px;
        padding: 10px 24px;
    }

    div {
        padding: 20px;
    }

    h1 {
        font-size: 24px;
        margin-bottom: 20px;
    }

    a {
        font-size: 14px;
    }

	.back {
        top: 15px;
        left: 15px;
    }

	table {
        width: 100%;
        margin-top: 10px;
    }

    th, td {
        padding: 8px;
        font-size: 12px;
    }

    select {
        width: 100%;
        padding: 8px;
        font-size: 14px;
	}
}
```

```sql
CREATE TABLE `feedback` (
  `id` int(11) NOT NULL,
  `name` varchar(150) COLLATE utf8mb4_unicode_ci NOT NULL,
  `telnum` varchar(18) COLLATE utf8mb4_unicode_ci NOT NULL,
  `date` varchar(10) COLLATE utf8mb4_unicode_ci NOT NULL,
  `time` varchar(10) COLLATE utf8mb4_unicode_ci NOT NULL,
  `weight` varchar(10) COLLATE utf8mb4_unicode_ci NOT NULL,
  `type` varchar(50) COLLATE utf8mb4_unicode_ci NOT NULL,
  `departure` varchar(150) COLLATE utf8mb4_unicode_ci NOT NULL,
  `delivery` varchar(150) COLLATE utf8mb4_unicode_ci NOT NULL
)

CREATE TABLE `user` (
  `id` int(11) NOT NULL,
  `username` varchar(50) COLLATE utf8mb4_unicode_ci NOT NULL,
  `password` varchar(250) COLLATE utf8mb4_unicode_ci NOT NULL,
  `fullname` varchar(150) COLLATE utf8mb4_unicode_ci NOT NULL,
  `telnum` varchar(18) COLLATE utf8mb4_unicode_ci NOT NULL,
  `email` varchar(50) COLLATE utf8mb4_unicode_ci NOT NULL,
  `role` int(1) NOT NULL
)
```
