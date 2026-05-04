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

        /* --- CARROUSEL FILAIRE --- */
        .carousel-svg {
            width: 320px;
            height: auto;
            stroke: #ffffff;
            stroke-width: 0.8;
            fill: none;
            stroke-linecap: round;
            stroke-linejoin: round;
        }

        /* Animation du mouvement vertical */
        .animated-horse {
            animation: gallop 3s ease-in-out infinite;
        }

        @keyframes gallop {
            0%, 100% { transform: translateY(-15px); }
            50% { transform: translateY(15px); }
        }

        @media (max-width: 900px) {
            .hero-layout { flex-direction: column; text-align: center; padding-top: 50px; }
            .hero-text h1 { font-size: 2.2rem; }
            .carousel-svg { width: 220px; }
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
                <!-- SVG MANÈGE FILAIRE -->
                <svg class="carousel-svg" viewBox="0 0 100 120" xmlns="http://www.w3.org/2000/svg">
                    <!-- Toit du manège -->
                    <path d="M10,40 L50,10 L90,40 Z" />
                    <path d="M10,40 Q50,30 90,40" />
                    <path d="M10,40 L10,45 Q50,35 90,45 L90,40" />
                    
                    <!-- Barre centrale -->
                    <line x1="50" y1="45" x2="50" y2="110" />
                    
                    <!-- Cheval animé (Tracé simplifié) -->
                    <g class="animated-horse">
                        <!-- Barre du cheval -->
                        <line x1="50" y1="50" x2="50" y2="100" stroke-dasharray="2,2" opacity="0.5" />
                        <!-- Corps du cheval -->
                        <path d="M35,75 Q35,60 50,60 Q65,60 70,50 Q75,45 75,55 Q70,75 55,75 Q45,75 40,85 Q35,90 30,80 Z" />
                        <!-- Jambes -->
                        <path d="M40,85 L35,95 M45,85 L42,95 M55,75 L58,85 M65,75 L68,85" />
                        <!-- Queue -->
                        <path d="M30,80 Q20,75 25,65" />
                    </g>

                    <!-- Socle -->
                    <path d="M20,110 L80,110 L85,115 L15,115 Z" />
                </svg>
            </div>
        </div>
    </section>

</body>
</html>
