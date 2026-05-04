<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamoutardenoire | Systèmes de Vente</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- RESET & BASES --- */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        :root {
            --bg-deep-dark: #05051a;   
            --text-main: #FFFFFF;      
            --text-muted: #a8a8c2;     
            --accent-glow: rgba(255, 255, 255, 0.05); 
            --font-main: 'Inter', sans-serif;
            --font-title: 'Space Grotesk', sans-serif;
        }

        body {
            background-color: var(--bg-deep-dark);
            color: var(--text-main);
            font-family: var(--font-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 50px;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
        }

        /* Halo blanc en fond */
        .hero::before {
            content: '';
            position: absolute;
            left: 50%; top: 50%;
            transform: translate(-50%, -50%);
            width: 800px; height: 800px;
            background: var(--accent-glow);
            filter: blur(150px);
            z-index: -1;
        }

        .hero-layout {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            gap: 80px;
        }

        .hero-text { flex: 1.2; }
        .hero-visual { flex: 0.8; display: flex; justify-content: center; align-items: center; }

        .hero-text h1 {
            font-family: var(--font-title);
            font-size: 3rem;
            line-height: 1.1;
            margin-bottom: 30px;
            letter-spacing: -2px;
        }

        .hero-text p {
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-bottom: 25px;
            max-width: 550px;
            font-weight: 300;
        }

        .hero-text p.cta-sub {
            font-weight: 400;
            color: white;
            margin-bottom: 45px;
        }

        .btn-premium {
            display: inline-block;
            padding: 20px 40px;
            border: 1px solid rgba(255,255,255,0.8);
            color: white;
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.75rem;
            transition: 0.4s;
        }

        .btn-premium:hover {
            background: white;
            color: #05051a;
        }

        /* --- IMAGE MANÈGE STATIQUE --- */
        .carousel-static {
            width: 380px;
            height: auto;
            fill: #ffffff; /* L'image sera en blanc sur ton fond bleu */
        }

        @media (max-width: 900px) {
            .hero-layout { flex-direction: column; text-align: center; padding-top: 50px; }
            .hero-text h1 { font-size: 2.2rem; }
            .carousel-static { width: 280px; }
        }
    </style>
</head>
<body>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu de coaching !</h1>
                <p>Tu es coach, tu as déjà des clientes, mais ton revenu fait le yo‑yo et tu es épuisée par les “stratégies miracles” et les to‑do listes infinies.</p>
                <p class="cta-sub">Ici, on enlève le superflu, on garde ce qui marche, et tu repars avec un plan simple que tu peux tenir.</p>
                <a href="#" class="btn-premium">Démarrer le démantèlement</a>
            </div>

            <div class="hero-visual">
                <!-- Reproduction fidèle de téléchargement_2.png en SVG blanc -->
                <svg class="carousel-static" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                    <!-- Toit -->
                    <path d="M10,40 L50,15 L90,40 Z" />
                    <path d="M10,40 Q50,30 90,40 L90,45 Q50,35 10,45 Z" />
                    <path d="M10,45 A5,5 0 0 0 20,45 A5,5 0 0 0 30,45 A5,5 0 0 0 40,45 A5,5 0 0 0 50,45 A5,5 0 0 0 60,45 A5,5 0 0 0 70,45 A5,5 0 0 0 80,45 A5,5 0 0 0 90,45" fill="none" stroke="white" stroke-width="1"/>
                    
                    <!-- Barre centrale -->
                    <rect x="49" y="15" width="2" height="75" />
                    
                    <!-- Chevaux (Silhouettes simplifiées de l'image) -->
                    <!-- Gauche -->
                    <rect x="24" y="45" width="1" height="35" />
                    <path d="M18,65 Q25,58 32,65 L32,72 Q25,78 18,72 Z" />
                    <!-- Centre -->
                    <path d="M43,68 Q50,61 57,68 L57,75 Q50,81 43,75 Z" />
                    <!-- Droite -->
                    <rect x="74" y="45" width="1" height="35" />
                    <path d="M68,65 Q75,58 82,65 L82,72 Q75,78 68,72 Z" />
                    
                    <!-- Socle -->
                    <path d="M15,90 L85,90 L90,95 L10,95 Z" />
                </svg>
            </div>
        </div>
    </section>

</body>
</html>
