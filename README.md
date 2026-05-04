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

        /* --- MANÈGE FILAIRE ANIMÉ --- */
        .carousel-container {
            width: 400px;
            height: 400px;
            position: relative;
        }

        .carousel-svg {
            width: 100%;
            height: auto;
            stroke: #ffffff;
            stroke-width: 0.8;
            fill: none;
        }

        /* Animation Rotation simulée */
        .horse-group {
            animation: carouselRotate 8s linear infinite;
        }

        /* Animation Haut/Bas décalée pour chaque cheval */
        .horse { animation: gallop 3s ease-in-out infinite; }
        .h2 { animation-delay: -1s; }
        .h3 { animation-delay: -2s; }

        @keyframes gallop {
            0%, 100% { transform: translateY(-8px); }
            50% { transform: translateY(8px); }
        }

        @keyframes carouselRotate {
            0% { transform: translateX(10px); opacity: 0.8; }
            50% { transform: translateX(-10px); opacity: 1; }
            100% { transform: translateX(10px); opacity: 0.8; }
        }

        @media (max-width: 900px) {
            .hero-layout { flex-direction: column; text-align: center; padding-top: 50px; }
            .hero-text h1 { font-size: 2.2rem; }
            .carousel-container { width: 280px; height: 280px; }
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
                <div class="carousel-container">
                    <svg class="carousel-svg" viewBox="0 0 120 120" xmlns="http://www.w3.org/2000/svg">
                        <!-- Toit (Inspiré de téléchargement.png) -->
                        <path d="M10,40 L60,10 L110,40 Z" />
                        <path d="M10,40 Q60,30 110,40" />
                        <path d="M10,40 C10,45 20,50 30,45 C40,40 50,50 60,45 C70,40 80,50 90,45 C100,40 110,45 110,40" />

                        <!-- Barre Centrale et Plateau -->
                        <line x1="60" y1="10" x2="60" y2="105" stroke-dasharray="2,2" />
                        
                        <g class="horse-group">
                            <!-- Cheval 1 -->
                            <g class="horse h1">
                                <line x1="30" y1="45" x2="30" y2="95" opacity="0.3" />
                                <path d="M25,75 Q30,65 35,70 Q40,75 38,85 Q35,90 28,88 Z" stroke-width="0.6"/>
                            </g>
                            <!-- Cheval 2 (Centre) -->
                            <g class="horse h2">
                                <line x1="60" y1="48" x2="60" y2="98" opacity="0.3" />
                                <path d="M55,78 Q60,68 65,73 Q70,78 68,88 Q65,93 58,91 Z" stroke-width="0.6"/>
                            </g>
                            <!-- Cheval 3 -->
                            <g class="horse h3">
                                <line x1="90" y1="45" x2="90" y2="95" opacity="0.3" />
                                <path d="M85,75 Q90,65 95,70 Q100,75 98,85 Q95,90 88,88 Z" stroke-width="0.6"/>
                            </g>
                        </g>

                        <!-- Socle -->
                        <ellipse cx="60" cy="105" rx="50" ry="8" />
                        <path d="M15,108 L105,108 L110,115 L10,115 Z" />
                    </svg>
                </div>
            </div>
        </div>
    </section>

</body>
</html>
