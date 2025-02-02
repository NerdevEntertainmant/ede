<!DOCTYPE html>
<html lang="NerdevEntertainment.hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Nerdev Entertainment</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #000000;
            color: #ff0000;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #1a1a1a;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 3em;
            text-transform: uppercase;
            color: #ff0000;
        }

        nav {
            background-color: #333333;
            padding: 10px 0;
            text-align: center;
        }

        nav a {
            color: #ff0000;
            padding: 10px 20px;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.2em;
            background-color: #444444;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.3s;
        }

        nav a:hover {
            background-color: #ff0000;
            color: #000000;
            transform: scale(1.1);
        }

        .container {
            padding: 30px;
            text-align: center;
            margin: 30px auto;
            max-width: 1200px;
        }

        .section-title {
            font-size: 2em;
            margin-bottom: 15px;
            text-transform: uppercase;
            color: #ff5500;
        }

        .forum {
            background-color: #1a1a1a;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }

        .forum input, .forum textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #555;
            border-radius: 5px;
            background-color: #222222;
            color: #ff0000;
        }

        .forum button {
            padding: 10px 20px;
            background-color: #ff0000;
            color: #000000;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.3s;
        }

        .forum button:hover {
            background-color: #ff5500;
            transform: scale(1.1);
        }

        .post {
            background-color: #222222;
            padding: 15px;
            border-radius: 5px;
            margin: 10px 0;
            text-align: left;
        }

        .post h3 {
            color: #ff5500;
            margin: 0;
        }

        footer {
            background-color: #1a1a1a;
            color: #ff0000;
            text-align: center;
            padding: 10px;
            font-size: 1.2em;
        }
    </style>
</head>
<body>

<header>
    <h1>Nerdev Entertainment</h1>
    <p>Játékfejlesztés és Horror Élmények</p>
</header>

<nav>
    <a href="#about">Rólunk</a>
    <a href="#games">Játékaink</a>
    <a href="#news">Hírek</a>
    <a href="#forum">Fórum</a>
    <a href="#contact">Kapcsolat</a>
</nav>

<div class="container" id="about">
    <h2 class="section-title">Rólunk</h2>
    <p>Üdvözlünk a Nerdev Entertainment hivatalos weboldalán! Mi egy magyar játékfejlesztő csapat vagyunk, akik izgalmas és egyedi játékokat készítenek.</p>
</div>

<div class="container" id="games">
    <h2 class="section-title">Játékaink</h2>

    <div class="game">
        <h3>The Secrets Items</h3>
        <p>Első játékunk, a *The Secrets Items*, egy horror játék, amely borzalmas titkokat rejt. Fedezd fel és próbálj túlélni!</p>
        <h4>Aktuális verzió: 0.5</h4>
        <p><strong>Letöltés:</strong> <a href="https://nerdev1.itch.io/the-secrets-items-fullgameanddlc" target="_blank">Itch.io (Nerdev1)</a></p>
    </div>

    <div class="game">
        <h3>The Shadow Writing</h3>
        <p>A *The Shadow Writing* egy új horror élmény, amelyben a rejtélyek és a sötétség dominálnak.</p>
        <h4>Aktuális verzió: Fejlesztés alatt</h4>
        <p><strong>Letöltés:</strong> <a href="https://nerdev1.itch.io/the-shadow-whritning" target="_blank">Itch.io</a></p>
    </div>
</div>

<div class="container" id="forum">
    <h2 class="section-title">Fórum</h2>
    <div class="forum">
        <h3>Tegyen fel egy kérdést vagy írjon hozzászólást!</h3>
        <input type="text" id="username" placeholder="Név">
        <textarea id="question" rows="4" placeholder="Írja be a kérdését vagy hozzászólását..."></textarea>
        <button onclick="addPost()">Küldés</button>
        <div id="forum-posts"></div>
    </div>
</div>

<div class="container" id="contact">
    <h2 class="section-title">Kapcsolat</h2>
    <p>E-mail: <a href="mailto:nerdev7@gmail.com">nerdev7@gmail.com</a></p>
</div>

<footer>
    <p>&copy; 2025 Nerdev Entertainment. Minden jog fenntartva.</p>
</footer>

<script>
    function addPost() {
        var username = document.getElementById("username").value;
        var question = document.getElementById("question").value;

        if (username === "" || question === "") {
            alert("Kérlek, tölts ki minden mezőt!");
            return;
        }

        var postContainer = document.getElementById("forum-posts");
        var newPost = document.createElement("div");
        newPost.classList.add("post");
        newPost.innerHTML = "<h3>" + username + ":</h3><p>" + question + "</p>";

        postContainer.prepend(newPost);

        document.getElementById("username").value = "";
        document.getElementById("question").value = "";
    }
</script>

</body>
</html>
