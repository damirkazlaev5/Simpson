
<html lang="ru" id="html-lang">
<head>
    <meta charset="UTF-8">
    <title>Симпсоны — фанатский сайт</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background: linear-gradient(135deg, #ffd700, #ff6b35);
            color: #222;
            line-height: 1.6;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        header {
            text-align: center;
            padding: 30px 0;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }
        h1 {
            color: #ffde00;
            text-shadow: 3px 3px 0 #fd0, -1px -1px 0 #fd0;
            font-size: 3.5rem;
            margin-bottom: 10px;
        }
        .lang-switch {
            position: absolute;
            top: 20px;
            right: 20px;
            background: #d40000;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 8px 15px;
            cursor: pointer;
            font-weight: bold;
        }
        .content {
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        .simpson-img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin: 20px auto;
            display: block;
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #2c3e50;
            color: white;
            margin-top: 30px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 id="title">🍩 Симпсоны</h1>
            <button class="lang-switch" onclick="switchLanguage()">English</button>
        </header>
        <div class="content">
            <h2 id="about-title">О сериале</h2>
            <p id="about-text">
                «Симпсоны» — американский анимационный ситком, созданный Мэттом Грейнингом для телеканала Fox.
                Сериал — сатирическое изображение американской жизни, воплощённое семьёй Симпсонов.
            </p>
           
            <p id="history-text">
                С момента премьеры 17 декабря 1989 года вышло более 750 эпизодов. Это самый длинный
                американский ситком, самый длинный американский анимационный проект и в 2023 году стал самым
                длинным сценарием прайм‑тайм сериала в истории США.
            </p>
        </div>
        <footer>
            &copy; <span id="year">2026</span> Фанатский сайт «Симпсонов». Все права защищены.
        </footer>
    </div>


    <script>
        const texts = {
            ru: {
                title: '🍩 Симпсоны',
                aboutTitle: 'О сериале',
                aboutText: '«Симпсоны» — американский анимационный ситком, созданный Мэттом Грейнингом для телеканала Fox. Сериал — сатирическое изображение американской жизни, воплощённое семьёй Симпсонов.',
                historyText: 'С момента премьеры 17 декабря 1989 года вышло более 750 эпизодов. Это самый длинный американский ситком, самый длинный американский анимационный проект и в 2023 году стал самым длинным сценарием прайм‑тайм сериала в истории США.',
                year: '2026'
            },
            en: {
                title: '🍩 The Simpsons',
                aboutTitle: 'About the Show',
                aboutText: '"The Simpsons" is an American animated sitcom created by Matt Groening for the Fox Broadcasting Company. The series is a satirical depiction of American life, epitomized by the Simpson family.',
                historyText: 'Since its debut on December 17, 1989, the show has broadcast over 750 episodes and is the longest-running American sitcom, the longest-running American animated program, and in 2023 became the longest-running scripted primetime television series in U.S. history.',
                year: '2026'
            }
        };

        function switchLanguage() {
            const lang = document.documentElement.lang === 'ru' ? 'en' : 'ru';
            document.documentElement.lang = lang;
            document.getElementById('title').textContent = texts[lang].title;
            document.getElementById('about-title').textContent = texts[lang].aboutTitle;
            document.getElementById('about-text').textContent = texts[lang].aboutText;
            document.getElementById('history-text').textContent = texts[lang].historyText;
            document.getElementById('year').textContent = texts[lang].year;
            document.querySelector('.lang-switch').textContent = lang === 'ru' ? 'English' : 'Русский';
        }
    </script>
</body>
</html>
