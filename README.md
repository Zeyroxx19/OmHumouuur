<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Musée des Espoirs Perdus</title>

<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        background: #0b4ea2;
        color: white;
        margin: 0;
    }

    header {
        padding: 60px 20px;
        background: #06367a;
    }

    h1 {
        font-size: 40px;
        margin-bottom: 10px;
    }

    .section {
        padding: 40px 20px;
    }

    .card {
        background: white;
        color: black;
        padding: 20px;
        margin: 15px auto;
        width: 250px;
        border-radius: 10px;
    }

    button {
        padding: 12px 20px;
        border: none;
        background: red;
        color: white;
        font-size: 18px;
        border-radius: 6px;
        cursor: pointer;
    }

    footer {
        background: #04224f;
        padding: 20px;
        margin-top: 40px;
    }
</style>
</head>

<body>

<header>
    <h1>Musée des Espoirs Perdus</h1>
    <p>Bienvenue sur le site officiel des prochains trophées</p>
    <button onclick="scrollToTrophees()">Voir la salle des trophées</button>
</header>

<div class="section" id="trophees">
    <h2>🏆 Salle des trophées</h2>

    <div class="card">Chargement... 12%</div>
    <div class="card">Projet en cours depuis 2010</div>
    <div class="card">Erreur 404 : trophée introuvable</div>
</div>

<div class="section">
    <h2>📢 Excuses officielles</h2>
    <p id="excuse">Clique pour générer une excuse</p>
    <button onclick="newExcuse()">Nouvelle excuse</button>
</div>

<div class="section">
    <h2>⏱️ Compteur officiel</h2>
    <p>Jours depuis la dernière désillusion :</p>
    <h1 id="counter">0</h1>
</div>

<footer>
    Site non sponsorisé par la réalité.
</footer>

<script>
function scrollToTrophees() {
    document.getElementById("trophees").scrollIntoView({behavior:"smooth"});
}

const excuses = [
    "La pelouse",
    "L'arbitre",
    "La météo",
    "Mercure rétrograde",
    "Encore Paris",
    "Trop de pression",
    "Pas assez de chance"
];

function newExcuse() {
    const random = Math.floor(Math.random() * excuses.length);
    document.getElementById("excuse").innerText = excuses[random];
}

// faux compteur qui reste à 0 😈
setInterval(() => {
    document.getElementById("counter").innerText = 0;
}, 1000);
</script>

</body>
</html>
