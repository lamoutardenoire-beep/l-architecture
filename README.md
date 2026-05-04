<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamoutardenoire | Architecte de Systèmes</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        :root {
            --bg-deep-dark: #05051a;   
            --text-main: #FFFFFF;      
            --text-muted: #8e8ea8;     
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
            padding: 0 40px;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
        }

        /* Halo central très diffus */
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
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-bottom: 45px;
            max-width: 480px;
            font-weight: 300;
        }

        .btn-premium {
            display: inline-block;
            padding: 18px 35px;
            border: 1px solid rgba(255,255,255,0.3);
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

        /* --- LE SYSTÈME TOURNANT (Cheval de bois mécanique) --- */
        .system-loader {
            position: relative;
            width: 300px;
            height: 300px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* L'anneau principal */
        .orbit {
            position: absolute;
            width: 100%;
            height: 100%;
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: rotateSystem 20s linear infinite;
        }

        /* Les "chevaux" (points mécaniques fins) */
        .orbit::before, .orbit::after {
            content: '';
            position: absolute;
            width: 6px;
            height: 6px;
            background: white;
            border-radius: 50%;
            box-shadow: 0 0 15px white;
        }

        .orbit::before { top: -3px; left: 50%; }
        .orbit::after { bottom: -3px; left: 50%; }

        /* Deuxième anneau intérieur tournant en sens inverse */
        .inner-orbit {
            position: absolute;
            width: 60%;
            height: 60%;
            border: 1px dashed rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            animation: rotateSystem 10s linear infinite reverse;
        }

        /* Axe central fixe */
        .center-pivot {
            width: 2px;
            height: 40px;
            background: white;
            position: relative;
        }
        .center-pivot::before {
            content: '';
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            width: 10px; height: 10px;
            border: 1px solid white;
            background: var(--bg-deep-dark);
        }

        @keyframes rotateSystem {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @media (max-width: 768px) {
            .hero-layout { flex-direction: column; text-align: center; }
            .hero-text h1 { font-size: 2.2rem; }
            .system-loader { width: 200px; height: 200px; margin-top: 40px; }
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
                <div class="system-loader">
                    <div class="orbit"></div>
                    <div class="inner-orbit"></div>
                    <div class="center-pivot"></div>
                </div>
            </div>
        </div>
    </section>

</body>
</html>
