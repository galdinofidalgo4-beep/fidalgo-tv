<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Fidalgo TV Premium</title>
<style>
/* ===== Estilo Geral ===== */
body {
    font-family: 'Arial', sans-serif;
    background:#111;
    color:#fff;
    margin:0;
    padding:0;
}
header {
    background:#222;
    padding:20px;
    text-align:center;
}
header h1 {
    margin:0;
    font-size:2rem;
}

/* ===== Carrossel ===== */
section h2 {
    text-align:center;
    margin-top:20px;
}
.movie-list {
    display:flex;
    overflow-x:auto;
    gap:20px;
    padding:20px;
    scroll-behavior:smooth;
}
.movie-item {
    min-width:200px;
    text-align:center;
    border-radius:10px;
    overflow:hidden;
    position:relative;
    cursor:pointer;
    transition: transform 0.3s, box-shadow 0.3s;
}
.movie-item:hover {
    transform: scale(1.08);
    box-shadow: 0 0 15px 3px #00ff99;
}
.movie-item img {
    width:100%;
    display:block;
    border-radius:10px;
}
.movie-item h3 {
    margin:10px 0 5px;
}
.movie-item p {
    font-size:0.9rem;
    color:#ccc;
    margin:0 10px 10px;
}

/* ===== Botão de Play ===== */
.play-btn {
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%, -50%);
    background: rgba(255,0,0,0.8);
    border-radius:50%;
    width:50px;
    height:50px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:24px;
    color:#fff;
    opacity:0.9;
    transition: transform 0.3s, background 0.3s;
}
.movie-item:hover .play-btn {
    transform:translate(-50%, -50%) scale(1.3);
    background:#ff3333;
}

/* ===== Player ===== */
.movie-player {
    text-align:center;
    padding:20px;
}
.movie-player video {
    width:90%;
    max-width:700px;
    border-radius:10px;
}

/* ===== Scrollbar bonita ===== */
.movie-list::-webkit-scrollbar {
    height:10px;
}
.movie-list::-webkit-scrollbar-thumb {
    background:#00ff99;
    border-radius:10px;
}
.movie-list::-webkit-scrollbar-track {
    background:#222;
}
</style>
</head>
<body>

<header>
    <h1>Fidalgo TV Premium</h1>
</header>

<section class="movies">
    <h2>Filmes em Destaque</h2>
    <div class="movie-list"></div>
</section>

<section class="movie-player">
    <h2>Player</h2>
    <video id="player" controls></video>
</section>

<script>
// Lista de filmes
const filmes = [
    {
        titulo: "Filme 1",
        capa: "https://via.placeholder.com/220x330?text=Filme+1",
        src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD10/tt21853596.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T213812Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=48aeb5620861bc3d3effcc1617c38465f5ac1f7ffb00c72bc3fc7e77effdcc40",
        descricao: "Ação intensa e aventura emocionante."
    },
    {
        titulo: "Filme 2",
        capa: "https://via.placeholder.com/220x330?text=Filme+2",
        src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt32304349.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214104Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=acbcf373741c7a4fe41703d7268b05a85f183e42e35bb51e4b3153844dbf51e5",
        descricao: "Comédia divertida para toda família."
    },
    {
        titulo: "Filme 3",
        capa: "https://via.placeholder.com/220x330?text=Filme+3",
        src: "http://b-howard.s3.us-central-1.wasabisys.com/4b5d/FHD4/tt31186851.mp4?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=XZN74AJF347JEO9YU5IC%2F20260120%2Fus-central-1%2Fs3%2Faws4_request&X-Amz-Date=20260120T214238Z&X-Amz-SignedHeaders=host&X-Amz-Expires=18000&X-Amz-Signature=f8cb5508a01d0feac631f33dab9fce606674bd06f2b66b0db568159ba455675f",
        descricao: "Drama emocionante com finais surpreendentes."
    }
];

// Montar carrossel
const container = document.querySelector(".movie-list");

filmes.forEach(filme => {
    const card = document.createElement("div");
    card.classList.add("movie-item");
    card.innerHTML = `
        <img src="${filme.capa}" alt="${filme.titulo}">
        <div class="play-btn">&#9658;</div>
        <h3>${filme.titulo}</h3>
        <p>${filme.descricao}</p>
    `;
    card.addEventListener("click", () => {
        const player = document.getElementById("player");
        player.src = filme.src;
        player.play();
        window.scrollTo({ top: player.offsetTop - 20, behavior: 'smooth' });
    });
    container.appendChild(card);
});
</script>

</body>
</html>
