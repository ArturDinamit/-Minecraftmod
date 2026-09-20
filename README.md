```html
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Моды Minecraft</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #111;
    color: white;
}

.header {
    padding: 20px;
    text-align: center;
    background: #191919;
}

.header h1 {
    margin: 0;
}

.container {
    padding: 20px;
    max-width: 600px;
    margin: auto;
}

.mod-card {
    background: #202020;
    border-radius: 18px;
    overflow: hidden;
    cursor: pointer;
    box-shadow: 0 5px 20px rgba(0,0,0,0.4);
}

.mod-card img {
    width: 100%;
    display: block;
}

.mod-info {
    padding: 15px;
}

.mod-info h2 {
    margin: 0 0 7px;
}

.mod-info p {
    margin: 0;
    color: #bbb;
}

/* Полноэкранное меню */

.modal {
    position: fixed;
    inset: 0;
    background: #111;
    display: none;
    z-index: 1000;
    overflow-y: auto;
}

.modal.active {
    display: block;
}

.modal-content {
    min-height: 100vh;
    padding: 25px;
    display: flex;
    flex-direction: column;
}

.close {
    align-self: flex-end;
    width: 45px;
    height: 45px;
    border: 0;
    border-radius: 50%;
    background: #292929;
    color: white;
    font-size: 25px;
    cursor: pointer;
}

.modal-image {
    width: 100%;
    max-width: 600px;
    margin: 20px auto;
    border-radius: 18px;
}

.description {
    max-width: 600px;
    margin: auto;
    width: 100%;
}

.description h2 {
    font-size: 28px;
}

.description p {
    color: #ccc;
    line-height: 1.5;
}

.download {
    display: block;
    max-width: 600px;
    width: 100%;
    margin: 30px auto 10px;
    padding: 17px;
    background: #35a853;
    color: white;
    text-align: center;
    text-decoration: none;
    border-radius: 12px;
    font-size: 18px;
    font-weight: bold;
}

.download:hover {
    background: #2d9148;
}

.note {
    max-width: 600px;
    margin: 10px auto;
    color: #888;
    text-align: center;
    font-size: 13px;
}
</style>
</head>

<body>

<header class="header">
    <h1>Моды Minecraft</h1>
</header>

<main class="container">

    <div class="mod-card" onclick="openMod()">

        <!-- Фото мода -->
        <img
            src="https://media.forgecdn.net/attachments/1396/956/mss-cover.png"
            alt="More Simple Structures">

        <div class="mod-info">
            <h2>More Simple Structures</h2>
            <p>Нажми чтобы посмотреть мод</p>
        </div>

    </div>

</main>


<!-- Полноэкранное окно -->

<div class="modal" id="modModal">

    <div class="modal-content">

        <button class="close" onclick="closeMod()">×</button>

        <img
            class="modal-image"
            src="https://media.forgecdn.net/attachments/1396/956/mss-cover.png"
            alt="More Simple Structures">

        <div class="description">

            <h2>More Simple Structures</h2>

            <p>
                Тут пока ничего нет
            </p>

            <p>
                Добавляет новые структуры в Minecraft Bedrock.
            </p>

        </div>

        <!-- КНОПКА СКАЧИВАНИЯ -->
        <a
            class="download"
            href="https://www.curseforge.com/minecraft-bedrock/addons/more-simple-structures-addon/files/8796286"
            target="_blank">
            Скачать мод
        </a>

        <div class="note">
            Откроется страница настоящего файла .mcaddon
        </div>

    </div>

</div>


<script>

function openMod() {
    document.getElementById("modModal").classList.add("active");
}

function closeMod() {
    document.getElementById("modModal").classList.remove("active");
}

</script>

</body>
</html>
```
