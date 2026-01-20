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
    <title>Fidalgo TV - Detalhes do Filme</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Fidalgo TV - Detalhes</h1>
        <a href="index.html">Voltar</a>
    </header>

    <section class="movie-player">
        <h2>Filme 1</h2>
        <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" width="100%" height="500" allowfullscreen></iframe>
    </section>

    <section class="movie-player">
        <h2>Filme 2</h2>
        <iframe src="https://www.youtube.com/embed/oHg5SJYRHA0" width="100%" height="500" allowfullscreen></iframe>
    </section>

    <section class="movie-player">
        <h2>Filme 3</h2>
        <iframe src="https://www.youtube.com/embed/6_b7RDuLwcI" width="100%" height="500" allowfullscreen></iframe>
    </section>

</body>
</html>
body { font-family: Arial, sans-serif; background:#111; color:#fff; margin:0; padding:0; }
header { background:#222; padding:20px; text-align:center; }
.movies { padding:20px; }
.movie-list { display:flex; gap:20px; justify-content:center; flex-wrap:wrap; }
.movie-item { width:200px; text-align:center; }
.movie-item img { width:100%; border-radius:10px; }
.movie-item h3 { margin-top:10px; }
a { text-decoration:none; color:white; }
// Por enquanto vazio, você pode adicionar carrossel ou animações depois
console.log("Fidalgo TV carregado!");
