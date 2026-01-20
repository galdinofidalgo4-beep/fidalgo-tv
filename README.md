<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Fidalgo TV</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Fidalgo TV</h1>
    </header>

    <section class="movies">
        <h2>Filmes em Destaque</h2>
        <div class="movie-list">

            <div class="movie-item">
                <a href="movie-detail.html#filme1">
                    <img src="images/filme1.jpg" alt="Filme 1">
                    <h3>Filme 1</h3>
                </a>
            </div>

            <div class="movie-item">
                <a href="movie-detail.html#filme2">
                    <img src="images/filme2.jpg" alt="Filme 2">
                    <h3>Filme 2</h3>
                </a>
            </div>

            <div class="movie-item">
                <a href="movie-detail.html#filme3">
                    <img src="images/filme3.jpg" alt="Filme 3">
                    <h3>Filme 3</h3>
                </a>
            </div>

        </div>
    </section>

    <script src="js/script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Fidalgo TV - Detalhes</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Fidalgo TV - Detalhes</h1>
        <a href="index.html">Voltar</a>
    </header>

    <section class="movie-player" id="filme1">
        <h2>Filme 1</h2>
        <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY" width="100%" height="500" allowfullscreen></iframe>
    </section>

    <section class="movie-player" id="filme2">
        <h2>Filme 2</h2>
        <iframe src="https://www.youtube.com/embed/5qap5aO4i9A" width="100%" height="500" allowfullscreen></iframe>
    </section>

    <section class="movie-player" id="filme3">
        <h2>Filme 3</h2>
        <iframe src="https://www.youtube.com/embed/6_b7RDuLwcI" width="100%" height="500" allowfullscreen></iframe>
    </section>

</body>
</html>
