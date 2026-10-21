<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<meta name="theme-color" content="#171513">
<meta name="description" content="Portfolio de Pierre YABRO, graphiste spécialisé en identité visuelle, logos, affiches événementielles et communication digitale à Abidjan.">

<title>Pierre YABRO — Portfolio Graphiste</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo:wght@300;400;500;600;700;800;900&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
:root {
    --paper: #f4f1ec;
    --paper-2: #e9e5de;
    --ink: #171513;
    --ink-2: #5f5a54;
    --rule: #cfc9c0;
    --accent: #d96a35;
    --night: #14120f;
    --white: #ffffff;
    --radius: 4px;
}

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-snap-type: y proximity;
}

body {
    margin: 0;
    background: var(--paper);
    color: var(--ink);
    font-family: 'Archivo', Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
}

img {
    display: block;
    max-width: 100%;
}

a {
    color: inherit;
}

.mono {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    letter-spacing: .04em;
}

section {
    position: relative;
    width: 100%;
    min-height: 100vh;
    min-height: 100svh;
    padding: 72px clamp(22px, 5vw, 80px) 95px;
    overflow: hidden;
    background: var(--paper);
    color: var(--ink);
    scroll-snap-align: start;
}

.dark {
    background: var(--night);
    color: var(--paper);
}

.section-label {
    margin-bottom: 36px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    letter-spacing: .08em;
    text-transform: uppercase;
}

.section-title {
    margin: 0 0 28px;
    font-size: clamp(38px, 6vw, 92px);
    line-height: .98;
    font-weight: 900;
    letter-spacing: -.055em;
    overflow-wrap: anywhere;
}

.accent {
    color: var(--accent);
}

.muted {
    color: var(--ink-2);
}

.dark .muted {
    color: #b5ada3;
}

.folio {
    position: absolute;
    right: clamp(22px, 5vw, 80px);
    bottom: 22px;
    left: clamp(22px, 5vw, 80px);
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 16px;
    color: var(--ink-2);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
}

.folio b {
    color: var(--ink);
}

.dark .folio {
    color: #a29a90;
}

.dark .folio b {
    color: var(--paper);
}

.image-frame {
    width: 100%;
    overflow: hidden;
    background: #e9e5de;
    border: 1px solid rgba(0,0,0,.08);
}

.image-frame img {
    width: 100%;
    height: auto;
    object-fit: contain;
}

.work-image {
    display: block;
    width: 100%;
    height: auto;
    object-fit: contain;
    box-shadow: 0 12px 35px rgba(0,0,0,.12);
}

.caption {
    display: grid;
    grid-template-columns: 35px minmax(0, 1fr);
    gap: 5px 12px;
    margin-top: 18px;
}

.caption-number {
    color: var(--accent);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
}

.caption-title {
    margin: 0;
    font-size: clamp(18px, 2.1vw, 29px);
    line-height: 1.15;
    font-weight: 800;
    letter-spacing: -.025em;
}

.caption-meta {
    grid-column: 2;
    color: var(--ink-2);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    line-height: 1.7;
}

.dark .caption-meta {
    color: #aaa196;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 44px;
    align-items: start;
}

.project {
    min-width: 0;
}

.project img {
    width: 100%;
    height: auto;
    object-fit: contain;
}

.project.single img {
    max-height: 75vh;
    width: auto;
    max-width: 100%;
    margin: auto;
}

.project.single .image-frame {
    padding: 15px;
}

.project.single .image-frame img {
    max-height: 65vh;
}

.hero-layout {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(300px, .9fr);
    gap: 50px;
    align-items: center;
    min-height: 65vh;
}

.hero-title {
    margin: 0;
    font-size: clamp(65px, 11vw, 155px);
    line-height: .82;
    font-weight: 900;
    letter-spacing: -.075em;
    text-transform: uppercase;
    overflow-wrap: anywhere;
}

.hero-title span {
    display: block;
}

.hero-description {
    max-width: 440px;
    margin: 30px 0 0;
    font-size: clamp(16px, 2vw, 23px);
    line-height: 1.55;
    color: #b5ada3;
}

.cover {
    min-height: 100vh;
    min-height: 100svh;
    padding-top: 35px;
    background: var(--paper);
}

.cover-tag {
    display: flex;
    flex-wrap: wrap;
    gap: 12px 25px;
    align-items: center;
    text-transform: uppercase;
}

.cover-tag span:last-child {
    color: var(--accent);
}

.cover-layout {
    display: grid;
    grid-template-columns: 1.05fr .95fr;
    gap: 30px;
    align-items: center;
    min-height: 75vh;
    padding: 45px 0;
}

.cover-name {
    position: relative;
    z-index: 2;
    margin: 0;
    font-size: clamp(65px, 11vw, 160px);
    line-height: .82;
    letter-spacing: -.075em;
    font-weight: 900;
    text-transform: uppercase;
    overflow-wrap: anywhere;
}

.cover-name span {
    display: block;
}

.cover-art {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 15px;
    align-items: center;
}

.cover-art img {
    width: 100%;
    height: auto;
    object-fit: contain;
    box-shadow: 0 15px 40px rgba(0,0,0,.16);
}

.cover-art img:nth-child(2) {
    margin-top: 35px;
}

.cover-art img:nth-child(3) {
    grid-column: 1 / -1;
    width: 82%;
    margin: -10px auto 0;
}

.about-layout {
    display: grid;
    grid-template-columns: minmax(0, 1.4fr) minmax(260px, .8fr);
    gap: 65px;
}

.about-statement {
    margin: 0 0 32px;
    font-size: clamp(30px, 5vw, 66px);
    line-height: 1.1;
    font-weight: 700;
    letter-spacing: -.04em;
}

.about-description {
    max-width: 720px;
    color: var(--ink-2);
    font-size: clamp(16px, 1.8vw, 22px);
    line-height: 1.75;
}

.expertise-title {
    margin: 0 0 20px;
    color: var(--ink-2);
}

.expertise-item {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    align-items: baseline;
    padding: 20px 0;
    border-top: 1px solid var(--rule);
    font-size: clamp(17px, 2vw, 26px);
    font-weight: 700;
}

.expertise-item span:last-child {
    color: var(--accent);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
}

.chapter-number {
    margin-bottom: 35px;
}

.contact-section {
    background: var(--accent);
    color: #fff8f2;
}

.contact-title {
    margin: 50px 0;
    font-size: clamp(52px, 10vw, 145px);
    line-height: .9;
    font-weight: 900;
    letter-spacing: -.065em;
    overflow-wrap: anywhere;
}

.contact-layout {
    display: flex;
    justify-content: space-between;
    align-items: end;
    gap: 30px;
    margin-top: 80px;
}

.contact-email {
    display: inline-block;
    margin-top: 12px;
    font-size: clamp(18px, 3.5vw, 43px);
    font-weight: 700;
    text-decoration: none;
    overflow-wrap: anywhere;
}

.contact-services {
    font-size: 15px;
    line-height: 1.8;
    text-align: right;
}

.navigation {
    position: fixed;
    z-index: 100;
    top: 50%;
    right: 12px;
    display: flex;
    flex-direction: column;
    gap: 9px;
    transform: translateY(-50%);
}

.navigation a {
    display: block;
    width: 9px;
    height: 9px;
    border: 1px solid #8e8275;
    border-radius: 50%;
    background: rgba(244,241,236,.7);
}

.navigation a:hover,
.navigation a:focus {
    background: var(--accent);
    border-color: var(--accent);
}

.back-top {
    position: fixed;
    z-index: 100;
    right: 18px;
    bottom: 18px;
    padding: 10px 14px;
    border: 0;
    border-radius: 3px;
    background: var(--ink);
    color: white;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    text-decoration: none;
}

img {
    background-color: transparent;
}

@media (min-width: 1500px) {
    section {
        padding-right: max(80px, calc((100vw - 1600px)/2));
        padding-left: max(80px, calc((100vw - 1600px)/2));
    }
}

@media (max-width: 850px) {
    html {
        scroll-snap-type: none;
    }

    section {
        min-height: auto;
        padding: 45px 22px 75px;
    }

    .cover {
        min-height: 100svh;
    }

    .cover-layout {
        grid-template-columns: 1fr;
        gap: 40px;
        padding: 65px 0 35px;
    }

    .cover-name {
        font-size: clamp(58px, 15vw, 115px);
    }

    .cover-art {
        max-width: 560px;
    }

    .about-layout {
        grid-template-columns: 1fr;
        gap: 35px;
    }

    .projects-grid {
        grid-template-columns: 1fr;
        gap: 42px;
    }

    .hero-layout {
        grid-template-columns: 1fr;
        gap: 35px;
        min-height: auto;
        padding: 35px 0;
    }

    .hero-title {
        font-size: clamp(54px, 12vw, 105px);
    }

    .hero-description {
        margin-top: 0;
    }

    .contact-layout {
        flex-direction: column;
        align-items: flex-start;
        margin-top: 50px;
    }

    .contact-services {
        text-align: left;
    }

    .navigation {
        right: 5px;
        gap: 7px;
    }

    .navigation a {
        width: 7px;
        height: 7px;
    }

    .folio {
        position: relative;
        right: auto;
        bottom: auto;
        left: auto;
        margin-top: 45px;
    }
}

@media (max-width: 480px) {
    section {
        padding: 32px 17px 55px;
    }

    .cover-tag {
        gap: 8px 14px;
        font-size: 10px;
    }

    .cover-name {
        font-size: clamp(50px, 15vw, 75px);
    }

    .cover-art {
        gap: 9px;
    }

    .section-title {
        font-size: 39px;
    }

    .caption {
        grid-template-columns: 26px minmax(0, 1fr);
        gap: 6px 8px;
    }

    .caption-title {
        font-size: 20px;
    }

    .folio {
        font-size: 9px;
    }

    .contact-title {
        font-size: 52px;
    }

    .contact-email {
        font-size: 18px;
    }

    .navigation {
        display: none;
    }
}

@media print {
    .navigation,
    .back-top {
        display: none;
    }

    section {
        min-height: auto;
        break-after: page;
        overflow: visible;
    }

    .folio {
        position: static;
        margin-top: 30px;
    }
}
</style>
</head>

<body>

<nav class="navigation" aria-label="Navigation entre les sections">
    <a href="#accueil" aria-label="Accueil"></a>
    <a href="#apropos" aria-label="À propos"></a>
    <a href="#affiches" aria-label="Affiches"></a>
    <a href="#gloire" aria-label="Grande soirée de gloire"></a>
    <a href="#priere" aria-label="Jeûne et prière"></a>
    <a href="#saintecene" aria-label="Sainte-Cène"></a>
    <a href="#pentecote" aria-label="Pentecôte"></a>
    <a href="#festival" aria-label="Festival"></a>
    <a href="#concerts" aria-label="Concerts"></a>
    <a href="#logos" aria-label="Logos"></a>
    <a href="#identites" aria-label="Identités visuelles"></a>
    <a href="#contact" aria-label="Contact"></a>
</nav>

<!-- 01 : COUVERTURE -->
<section class="cover" id="accueil">
    <div class="cover-tag mono">
        <span>Portfolio</span>
        <span>Design graphique</span>
        <span>2019 — 2026</span>
    </div>

    <div class="cover-layout">
        <div>
            <h1 class="cover-name">
                <span>Pierre</span>
                <span class="accent">YABRO</span>
            </h1>
            <p class="mono muted" style="margin-top:25px">
                GRAPHISTE · ABIDJAN, CÔTE D'IVOIRE
            </p>
        </div>

        <div class="cover-art">
            <img src="img/06-republic-festival.jpg"
                 alt="Affiche Republic Festival"
                 loading="eager">

            <img src="img/04-sainte-cene.jpg"
                 alt="Affiche de la Sainte-Cène"
                 loading="eager">

            <img src="img/01-soiree-gloire.jpg"
                 alt="Affiche Grande soirée de gloire"
                 loading="eager">
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Graphiste</span>
        <span>01 / 12</span>
    </div>
</section>

<!-- 02 : À PROPOS -->
<section id="apropos">
    <div class="section-label">À propos de moi</div>

    <div class="about-layout">
        <div>
            <p class="about-statement">
                Graphiste créatif, je transforme les idées en créations visuelles
                <span class="accent">modernes, percutantes et professionnelles.</span>
            </p>

            <p class="about-description">
                Spécialisé dans la conception d'identités visuelles, de logos,
                d'affiches publicitaires et de visuels pour les réseaux sociaux.
                Mes créations accompagnent principalement des églises,
                des structures événementielles et des festivals à Abidjan.
            </p>
        </div>

        <div>
            <p class="expertise-title mono">MES EXPERTISES</p>

            <div class="expertise-item">
                <span>Identité visuelle</span>
                <span>01</span>
            </div>

            <div class="expertise-item">
                <span>Logos</span>
                <span>02</span>
            </div>

            <div class="expertise-item">
                <span>Affiches publicitaires</span>
                <span>03</span>
            </div>

            <div class="expertise-item">
                <span>Réseaux sociaux</span>
                <span>04</span>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Portfolio</span>
        <span>02 / 12</span>
    </div>
</section>

<!-- 03 : OUVERTURE AFFICHES -->
<section class="dark" id="affiches">
    <div class="section-label chapter-number">CHAPITRE 01 — COMMUNICATION ÉVÉNEMENTIELLE</div>

    <div class="hero-layout">
        <h2 class="hero-title">
            Affiches
            <span class="accent">événementielles</span>
        </h2>

        <p class="hero-description">
            Cultes, soirées, festivals et concerts : des affiches pensées
            pour attirer l'attention, communiquer un message et valoriser
            chaque événement, sur papier comme sur les réseaux sociaux.
        </p>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Portfolio</span>
        <span>03 / 12</span>
    </div>
</section>

<!-- 04 : GRANDE SOIRÉE DE GLOIRE -->
<section id="gloire">
    <div class="section-label">01 — GRANDE SOIRÉE DE GLOIRE</div>

    <div class="projects-grid">
        <div class="project single">
            <img class="work-image"
                 src="img/01-soiree-gloire.jpg"
                 alt="Affiche Tu verras la gloire de Dieu"
                 loading="lazy">
        </div>

        <div class="project">
            <div class="mono accent">PROJET 01</div>

            <h2 class="section-title" style="margin-top:20px">
                Tu verras la gloire de Dieu
            </h2>

            <p class="muted" style="line-height:1.8">
                Grande soirée de gloire<br>
                Génération Chrétienne d'Impact<br>
                2026
            </p>

            <p style="line-height:1.8">
                Conception d'une affiche événementielle destinée à annoncer
                une rencontre chrétienne et à mettre en valeur son thème.
            </p>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>04 / 12</span>
    </div>
</section>

<!-- 05 : JEÛNE ET ANNÉE DE GLOIRE -->
<section id="priere">
    <div class="section-label">02 — CAMPAGNES ET COMMUNICATION RELIGIEUSE</div>

    <div class="projects-grid">
        <div class="project">
            <img class="work-image"
                 src="img/02-10-jours.jpg"
                 alt="Affiche 10 jours de jeûne et prière"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">02</span>
                <h3 class="caption-title">10 jours de jeûne et prière</h3>
                <div class="caption-meta">GCI — Janvier 2024</div>
            </div>
        </div>

        <div class="project">
            <img class="work-image"
                 src="img/03-2025-gloire.jpg"
                 alt="Affiche 2025 année de gloire et de règne"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">03</span>
                <h3 class="caption-title">2025, année de gloire et de règne</h3>
                <div class="caption-meta">GCI — Affiche annuelle 2025</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>05 / 12</span>
    </div>
</section>

<!-- 06 : SAINTE-CÈNE ET PROGRAMME -->
<section class="dark" id="saintecene">
    <div class="section-label">03 — COMMUNICATION D'ÉGLISE</div>

    <div class="projects-grid">
        <div class="project">
            <img class="work-image"
                 src="img/04-sainte-cene.jpg"
                 alt="Affiche Le mystère de la Sainte-Cène"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">04</span>
                <h3 class="caption-title">Le mystère de la Sainte-Cène</h3>
                <div class="caption-meta">GCI — Mars 2025</div>
            </div>
        </div>

        <div class="project">
            <img class="work-image"
                 src="img/11-programme-eglise.jpg"
                 alt="Programme de l'église"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">05</span>
                <h3 class="caption-title">Programme de l'église</h3>
                <div class="caption-meta">GCI — Visuel pour réseaux sociaux</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>06 / 12</span>
    </div>
</section>

<!-- 07 : CÔTE D'IVOIRE ET PENTECÔTE -->
<section id="pentecote">
    <div class="section-label">04 — CÉLÉBRATIONS ET CULTES SPÉCIAUX</div>

    <div class="projects-grid">
        <div class="project">
            <img class="work-image"
                 src="img/05-cote-ivoire.jpg"
                 alt="Affiche La Côte d'Ivoire appartient à l'Éternel"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">06</span>
                <h3 class="caption-title">La Côte d'Ivoire appartient à l'Éternel</h3>
                <div class="caption-meta">Culte spécial — Mai 2024</div>
            </div>
        </div>

        <div class="project">
            <img class="work-image"
                 src="img/07-pentecote.jpg"
                 alt="Affiche Pentecôte 2024"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">07</span>
                <h3 class="caption-title">Pentecôte 2024</h3>
                <div class="caption-meta">Une génération nouvelle — GCI</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>07 / 12</span>
    </div>
</section>

<!-- 08 : FESTIVAL ET CULTE PROPHÉTIQUE -->
<section style="background:var(--paper-2)" id="festival">
    <div class="section-label">05 — FESTIVALS ET RENCONTRES</div>

    <div class="projects-grid">
        <div class="project">
            <img class="work-image"
                 src="img/06-republic-festival.jpg"
                 alt="Affiche Republic Festival, Festival de Gospel Urbain d'Abidjan"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">08</span>
                <h3 class="caption-title">Festival de Gospel Urbain d'Abidjan</h3>
                <div class="caption-meta">Republic Festival — 4ᵉ édition</div>
            </div>
        </div>

        <div class="project">
            <img class="work-image"
                 src="img/08-culte-prophetique.jpg"
                 alt="Affiche Culte prophétique"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">09</span>
                <h3 class="caption-title">Culte prophétique</h3>
                <div class="caption-meta">Tu es le choix de Dieu — Novembre 2023</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>08 / 12</span>
    </div>
</section>

<!-- 09 : CONCERTS DE CHARITÉ -->
<section id="concerts">
    <div class="section-label">06 — STRUCTURE ÉVÉNEMENTIELLE GENYA</div>

    <h2 class="section-title">Concerts de charité</h2>

    <p class="muted" style="max-width:650px;line-height:1.8;margin-bottom:40px">
        Une série d'affiches conçues pour promouvoir des événements
        de solidarité et de musique.
    </p>

    <div class="projects-grid">
        <div class="project">
            <img class="work-image"
                 src="img/09-concert-charite-2019.jpg"
                 alt="Affiche Concert de charité 2019"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">10</span>
                <h3 class="caption-title">Concert de charité</h3>
                <div class="caption-meta">Édition 2019</div>
            </div>
        </div>

        <div class="project">
            <img class="work-image"
                 src="img/10-concert-charite-2020.jpg"
                 alt="Affiche Concert de charité 2020"
                 loading="lazy">

            <div class="caption">
                <span class="caption-number">11</span>
                <h3 class="caption-title">Concert de charité</h3>
                <div class="caption-meta">Édition 2020</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Affiches</span>
        <span>09 / 12</span>
    </div>
</section>

<!-- 10 : OUVERTURE LOGOS -->
<section class="dark" id="logos">
    <div class="section-label">CHAPITRE 02 — IDENTITÉ VISUELLE</div>

    <div class="hero-layout">
        <h2 class="hero-title">
            Logos
            <span class="accent">&amp; identités</span>
        </h2>

        <p class="hero-description">
            Des emblèmes conçus pour représenter une communauté,
            transmettre ses valeurs et renforcer son identité visuelle.
        </p>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Portfolio</span>
        <span>10 / 12</span>
    </div>
</section>

<!-- 11 : LOGOS -->
<section id="identites">
    <div class="section-label">07 — CRÉATION DE LOGOS</div>

    <div class="projects-grid">
        <div class="project">
            <div class="image-frame" style="background:#fff;padding:15px">
                <img src="img/12-logo-jeunesse.jpg"
                     alt="Logo Jeunesse rassemblée pour le Christ"
                     loading="lazy">
            </div>

            <div class="caption">
                <span class="caption-number">12</span>
                <h3 class="caption-title">Jeunesse rassemblée pour le Christ</h3>
                <div class="caption-meta">Logo — 2026</div>
            </div>
        </div>

        <div class="project">
            <div class="image-frame" style="background:#f7f2e8;padding:15px">
                <img src="img/13-logo-congregation.jpg"
                     alt="Logo Congrégation internationale des jeunes serviteurs"
                     loading="lazy">
            </div>

            <div class="caption">
                <span class="caption-number">13</span>
                <h3 class="caption-title">Congrégation internationale des jeunes serviteurs</h3>
                <div class="caption-meta">Logo — 2026</div>
            </div>
        </div>
    </div>

    <div class="folio">
        <span><b>Pierre YABRO</b> — Identité visuelle</span>
        <span>11 / 12</span>
    </div>
</section>

<!-- 12 : CONTACT -->
<section class="contact-section" id="contact">
    <div class="section-label">CONTACT — COLLABORATIONS</div>

    <h2 class="contact-title">
        Travaillons<br>ensemble.
    </h2>

    <div class="contact-layout">
        <div>
            <div class="mono">ÉCRIVEZ-MOI</div>

            <a class="contact-email"
               href="mailto:pierreyabro93@gmail.com">
                pierreyabro93@gmail.com
            </a>
        </div>

        <div class="contact-services">
            Identités visuelles<br>
            Logos<br>
            Affiches événementielles<br>
            Réseaux sociaux
        </div>
    </div>

    <div class="folio" style="color:#ffe3d6">
        <span><b style="color:#fff">Pierre YABRO</b> — Graphiste</span>
        <span>12 / 12</span>
    </div>
</section>

<a href="#accueil" class="back-top">↑ HAUT</a>

<script>
(function () {
    "use strict";

    // Vérification des images du portfolio.
    document.querySelectorAll("img").forEach(function (img) {
        img.addEventListener("error", function () {
            console.error("Image introuvable :", img.getAttribute("src"));

            img.style.minHeight = "50px";
            img.style.border = "1px dashed #d96a35";
            img.style.backgroundColor = "#e9e5de";
            img.alt = "Image introuvable : " + img.getAttribute("src");
        });
    });

    // Navigation : affichage du lien de section actif.
    if ("IntersectionObserver" in window) {
        const sections = document.querySelectorAll("body > section");
        const links = document.querySelectorAll(".navigation a");

        const observer = new IntersectionObserver(function (entries) {
            entries.forEach(function (entry) {
                if (!entry.isIntersecting) return;

                const activeId = entry.target.id;

                links.forEach(function (link) {
                    if (link.getAttribute("href") === "#" + activeId) {
                        link.style.backgroundColor = "#d96a35";
                        link.style.borderColor = "#d96a35";
                    } else {
                        link.style.backgroundColor = "";
                        link.style.borderColor = "";
                    }
                });
            });
        }, {
            threshold: 0.35
        });

        sections.forEach(function (section) {
            observer.observe(section);
        });
    }
})();
</script>

</body>
</html>
