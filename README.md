<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stabilité & Systèmes | Démanteler le cirque du coaching</title>
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
            transition: 0.4s;
        }

        .btn-premium:hover {
            background: white;
            color: #05051a;
        }

        /* --- L'IMAGE SANS CERCLE --- */
        .carousel-img {
            width: 450px; /* Légèrement agrandie car elle n'est plus contrainte par le cercle */
            height: auto;
            
        }

        @media (max-width: 900px) {
            .hero-layout { flex-direction: column; text-align: center; padding-top: 50px; }
            .hero-text h1 { font-size: 2.2rem; }
            .carousel-img { width: 300px; }
        }
    </style>
</head>
<body>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu !</h1>
                <p>Tu es coach, tu as déjà des clientes, mais ton revenu fait le yo‑yo et tu es épuisée par les “stratégies miracles” et les to‑do listes infinies.</p>
                <p class="cta-sub">Ici, on enlève le superflu, on garde ce qui marche, et tu repars avec un plan simple que tu peux tenir.</p>
                <a href="#" class="btn-premium">Démarrer le démantèlement</a>
            </div>

            <div class="hero-visual">
                <!-- Image brute sans conteneur circulaire -->
                <img src="Cheval.png" alt="Manège" class="carousel-img">
            </div>
        </div>
    </section>

</body>
</html>
