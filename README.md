fidalgo-tv-premium/
│
├─ index.html           ← Página inicial com carrossel e filmes
├─ movie-detail.html    ← Player premium para cada filme
├─ css/
│   └─ style.css        ← Estilo moderno e responsivo
├─ js/
│   ├─ script.js        ← Carrossel e geração de filmes
│   └─ movies.js        ← Lista de filmes em JSON
└─ images/
    ├─ filme1.jpg
    ├─ filme2.jpg
    └─ filme3.jpg
    const filmes = [
  {
    titulo: "Filme 1",
    capa: "images/filme1.jpg",
    src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD10/tt21853596.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T213812Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=48aeb5620861bc3d3effcc1617c38465f5ac1f7ffb00c72bc3fc7e77effdcc40",
    descricao: "Ação intensa e aventura emocionante."
  },
  {
    titulo: "Filme 2",
    capa: "images/filme2.jpg",
    src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt32304349.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=acbcf373741c7a4fe41703d7268b05a85f183e42e35bb51e4b3153844dbf51e5",
    descricao: "Comédia divertida para toda família."
  },
  {
    titulo: "Filme 3",
    capa: "images/filme3.jpg",
    src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt31186851.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214238Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=f8cb5508a01d0feac631f33dab9fce606674bd06f2b66b0db568159ba455675f",
    descricao: "Drama emocionante com finais surpreendentes."
  }
];
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Fidalgo TV Premium</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Fidalgo TV Premium</h1>
    </header>

    <section class="movies" id="movie-section">
        <h2>Filmes em Destaque</h2>
        <div class="movie-list">
            <!-- Filmes serão carregados pelo JS -->
        </div>
    </section>

    <script src="js/movies.js"></script>
    <script src="js/script.js"></script>
</body>
</html>
const container = document.querySelector(".movie-list");

filmes.forEach(filme => {
    const card = document.createElement("div");
    card.classList.add("movie-item");

    card.innerHTML = `
        <a href="movie-detail.html#${filme.titulo.replace(/\s+/g, '')}">
            <img src="${filme.capa}" alt="${filme.titulo}">
            <h3>${filme.titulo}</h3>
            <p>${filme.descricao}</p>
        </a>
    `;

    container.appendChild(card);
});
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Fidalgo TV - Player</title>
    <link href="https://vjs.zencdn.net/8.22.0/video-js.css" rel="stylesheet" />
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>Fidalgo TV - Player</h1>
        <a href="index.html">Voltar</a>
    </header>

    <section class="movie-player">
        <h2>Filme 1</h2>
        <video id="filme1" class="video-js vjs-big-play-centered" controls preload="auto" width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD10/tt21853596.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T213812Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=48aeb5620861bc3d3effcc1617c38465f5ac1f7ffb00c72bc3fc7e77effdcc40" type="video/mp4">
        </video>

        <h2>Filme 2</h2>
        <video id="filme2" class="video-js vjs-big-play-centered" controls preload="auto" width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt32304349.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=acbcf373741c7a4fe41703d7268b05a85f183e42e35bb51e4b3153844dbf51e5" type="video/mp4">
        </video>

        <h2>Filme 3</h2>
        <video id="filme3" class="video-js vjs-big-play-centered" controls preload="auto" width="100%" height="500">
            <source src="http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt31186851.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214238Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=f8cb5508a01d0feac631f33dab9fce606674bd06f2b66b0db568159ba455675f" type="video/mp4">
        </video>
    </section>

    <script src="https://vjs.zencdn.net/8.22.0/video.min.js"></script>
</body>
</html>
body { font-family: 'Arial', sans-serif; background:#111; color:#fff; margin:0; padding:0; }
header { background:#222; padding:20px; text-align:center; }
h1 { margin:0; font-size:2rem; }
.movies { padding:20px; }
.movie-list { display:flex; gap:20px; justify-content:center; flex-wrap:wrap; }
.movie-item { width:220px; text-align:center; border-radius:10px; overflow:hidden; transition: transform 0.3s; cursor:pointer; }
.movie-item:hover { transform: scale(1.05); }
.movie-item img { width:100%; border-radius:10px; }
.movie-item h3 { margin-top:10px; font-size:1.1rem; }
.movie-item p { font-size:0.9rem; margin-top:5px; color:#ccc; }
a { text-decoration:none; color:white; }
.movie-player { padding:20px; text-align:center; }
