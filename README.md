<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamoutardenoire | Architecte de Systèmes</title>
    <!-- Polices Premium -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- CONFIGURATION GLOBALE --- */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        :root {
            --bg-deep-dark: #05051a;   /* Ton Bleu Nuit précis */
            --text-main: #FFFFFF;      
            --text-muted: #8e8ea8;     
            --accent-glow: rgba(255, 255, 255, 0.08); /* Glow Blanc subtil */
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
            padding: 0 40px;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
        }

        /* Le Halo Blanc en fond */
        .hero::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 600px;
            height: 600px;
            background: var(--accent-glow);
            filter: blur(120px);
            border-radius: 50%;
            z-index: -1;
        }

        .hero-layout {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            gap: 60px;
        }

        .hero-text { flex: 1.2; }
        .hero-visual { flex: 0.8; display: flex; justify-content: center; }

        .hero-text h1 {
            font-family: var(--font-title);
            font-size: 3.5rem;
            line-height: 1.1;
            margin-bottom: 25px;
            letter-spacing: -2px;
        }

        .hero-text p {
            font-size: 1.25rem;
            color: var(--text-muted);
            margin-bottom: 45px;
            max-width: 500px;
        }

        .btn-premium {
            display: inline-block;
            padding: 20px 40px;
            background-color: #ffffff;
            color: #05051a;
            text-decoration: none;
            font-weight: 700;
            border-radius: 2px;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.8rem;
            transition: 0.3s cubic-bezier(0.19, 1, 0.22, 1);
        }

        .btn-premium:hover {
            background: transparent;
            color: white;
            box-shadow: inset 0 0 0 2px white;
            transform: translateY(-5px);
        }

        /* --- DESSIN CIRQUE MINIMALISTE --- */
        .circus-icon {
            position: relative;
            width: 240px;
            height: 200px;
            animation: float 4s ease-in-out infinite;
        }

        .tent-top {
            width: 0;
            height: 0;
            border-left: 120px solid transparent;
            border-right: 120px solid transparent;
            border-bottom: 80px solid #ffffff;
        }

        .tent-body {
            width: 240px;
            height: 100px;
            background: repeating-linear-gradient(
                90deg,
                #ffffff,
                #ffffff 20px,
                #05051a 20px,
                #05051a 40px
            );
            border: 1px solid #ffffff;
            position: relative;
        }

        .door {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 50px;
            background-color: #05051a;
            border-radius: 20px 20px 0 0;
            border: 1px solid #ffffff;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-25px); }
        }

        /* Responsive Mobile */
        @media (max-width: 768px) {
            .hero-layout { flex-direction: column; text-align: center; }
            .hero-text h1 { font-size: 2.5rem; }
            .hero-visual { margin-top: 40px; }
        }
    </style>
</head>
<body>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu de coaching !</h1>
                <p>Architecte de systèmes de vente. Je démantèle le chaos pour bâtir ta structure de conversion.</p>
                <a href="#" class="btn-premium">Démarrer le démantèlement</a>
            </div>

            <div class="hero-visual">
                <div class="circus-icon">
                    <div class="tent-top"></div>
                    <div class="tent-body">
                        <div class="door"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</body>
</html>
