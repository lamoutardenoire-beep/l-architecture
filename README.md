<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stabilité & Systèmes | Démanteler le cirque du coaching</title>
    
    <!-- Polices Premium -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-dark: #05051a; /* Ton bleu nuit profond */
            --bg-accent: #0a0a2e;
            --text-main: #FFFFFF;
            --text-muted: #a8a8c2;
            --accent-white: #ffffff;
            --font-main: 'Inter', sans-serif;
            --font-title: 'Space Grotesk', sans-serif;
            --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--bg-dark);
            /* Gradient radial pour la profondeur architecturale */
            background: radial-gradient(circle at 75% 30%, var(--bg-accent) 0%, var(--bg-dark) 80%);
            color: var(--text-main);
            font-family: var(--font-main);
            line-height: 1.5;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 40px;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
        }

        .hero-layout {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            align-items: center;
            gap: 80px;
            width: 100%;
        }

        /* --- SECTION TEXTE --- */
        .hero-text {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 0.8s forwards 0.2s;
        }

        .hero-text h1 {
            font-family: var(--font-title);
            font-size: clamp(2.5rem, 5vw, 3.8rem);
            line-height: 1.05;
            margin-bottom: 24px;
            letter-spacing: -0.03em;
        }

        .hero-text p {
            font-size: clamp(1rem, 2vw, 1.2rem);
            color: var(--text-muted);
            margin-bottom: 25px;
            max-width: 600px;
            font-weight: 300;
        }

        /* Accentuation du plan simple */
        .cta-sub {
            font-weight: 500 !important;
            color: var(--text-main) !important;
            margin-bottom: 45px !important;
            border-left: 3px solid var(--accent-white);
            padding-left: 20px;
        }

        /* --- BOUTON INTERACTIF --- */
        .btn-premium {
            display: inline-block;
            padding: 20px 40px;
            background: transparent;
            border: 1px solid rgba(255,255,255,0.4);
            color: white;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            font-size: 0.8rem;
            transition: var(--transition);
        }

        .btn-premium:hover {
            background: var(--accent-white);
            color: var(--bg-dark);
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(255,255,255,0.1);
        }

        /* --- VISUEL --- */
        .hero-visual {
            display: flex;
            justify-content: center;
            opacity: 0;
            animation: fadeIn 1s forwards 0.6s;
        }

        .carousel-img {
            max-width: 100%;
            width: 500px;
            height: auto;
            filter: brightness(0) invert(1); /* Image en blanc pur */
            animation: float 8s ease-in-out infinite;
        }

        /* Animations */
        @keyframes fadeIn {
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 992px) {
            .hero-layout {
                grid-template-columns: 1fr;
                text-align: center;
                padding: 80px 0;
            }
            .hero-text { order: 2; }
            .hero-visual { order: 1; margin-bottom: 40px; }
            .hero-text p { margin-left: auto; margin-right: auto; }
            .cta-sub { border-left: none; border-bottom: 2px solid white; padding: 0 0 20px 0; }
            .carousel-img { width: 320px; }
        }
    </style>
</head>
<body>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu.</h1>
                
                <p>Tu es coach, tu as déjà des clientes, mais ton revenu fait le yo‑yo et tu es épuisée par les stratégies miracles.</p>
                
                <p class="cta-sub">On enlève le superflu, on garde ce qui marche : repars avec un plan simple que tu peux tenir.</p>
                
                <a href="#" class="btn-premium">Démarrer le démantèlement</a>
            </div>

            <div class="hero-visual">
                <!-- L'image de ton manège/cheval, épurée -->
                <img src="Cheval.png" alt="Stabilité systémique" class="carousel-img">
            </div>
        </div>
    </section>

</body>
</html>
