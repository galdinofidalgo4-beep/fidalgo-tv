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

    <!-- Filme 1 -->
    <section class="movie-player" id="filme1">
        <h2>Filme 1</h2>
        <video controls width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD10/tt21853596.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T213812Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=48aeb5620861bc3d3effcc1617c38465f5ac1f7ffb00c72bc3fc7e77effdcc40" type="video/mp4">
            Seu navegador não suporta o player de vídeo.
        </video>
    </section>

    <!-- Filme 2 -->
    <section class="movie-player" id="filme2">
        <h2>Filme 2</h2>
        <video controls width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt32304349.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=acbcf373741c7a4fe41703d7268b05a85f183e42e35bb51e4b3153844dbf51e5" type="video/mp4">
            Seu navegador não suporta o player de vídeo.
        </video>
    </section>

    <!-- Filme 3 -->
    <section class="movie-player" id="filme3">
        <h2>Filme 3</h2>
        <video controls width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt31186851.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214238Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=f8cb5508a01d0feac631f33dab9fce606674bd06f2b66b0db568159ba455675f" type="video/mp4">
            Seu navegador não suporta o player de vídeo.
        </video>
    </section>

</body>
</html>
