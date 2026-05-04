<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamoutardenoire | Systèmes de Vente</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
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
            overflow: hidden;
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

        /* Halo blanc diffus */
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

        .hero-text { flex: 1.3; }
        .hero-visual { flex: 0.7; display: flex; justify-content: center; align-items: center; }

        .hero-text h1 {
            font-family: var(--font-title);
            font-size: 3.2rem;
            line-height: 1.1;
            margin-bottom: 30px;
            letter-spacing: -2px;
        }

        .hero-text p {
            font-size: 1.15rem;
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
            transition: 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .btn-premium:hover {
            background: white;
            color: #05051a;
            transform: translateY(-5px);
        }

        /* --- LE CHEVAL EN LIGNE CONTINUE (SVG) --- */
        .horse-container {
            width: 350px;
            height: 350px;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: carouselMove 3s ease-in-out infinite; /* Le mouvement de haut en bas */
        }

        .horse-svg {
            width: 100%;
            height: auto;
            stroke: #ffffff;
            stroke-width: 1;
            fill: none;
            stroke-linecap: round;
            stroke-linejoin: round;
            opacity: 0.8;
        }

        /* Mouvement fluide de haut en bas */
        @keyframes carouselMove {
            0%, 100% { transform: translateY(-20px); }
            50% { transform: translateY(20px); }
        }

        @media (max-width: 900px) {
            .hero-layout { flex-direction: column; text-align: center; padding-top: 50px; }
            .hero-text h1 { font-size: 2.2rem; }
            .hero-text p { margin: 0 auto 20px auto; }
            .horse-container { width: 250px; height: 250px; }
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
                <div class="horse-container">
                    <!-- SVG One-Line Horse -->
                    <svg class="horse-svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                        <path d="M20,60 C20,60 25,40 40,35 C55,30 65,35 70,30 C75,25 75,15 75,15 M75,15 C75,15 80,25 70,40 C60,55 45,55 35,65 C25,75 25,85 25,85 M25,85 L45,85 M55,85 L75,85 M50,10 L50,90" />
                        <circle cx="50" cy="10" r="1" fill="white" />
                        <circle cx="50" cy="90" r="1" fill="white" />
                    </svg>
                </div>
            </div>
        </div>
    </section>

</body>
</html>
