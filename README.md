<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Miora | Architecte de Systèmes</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-dark: #05051a; 
            --bg-card: rgba(255, 255, 255, 0.03);
            --text-main: #FFFFFF;
            --text-muted: #a8a8c2;
            --accent: #ffffff;
            --border: rgba(255, 255, 255, 0.1);
            --font-main: 'Inter', sans-serif;
            --font-title: 'Space Grotesk', sans-serif;
            --transition: all 0.6s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            font-family: var(--font-main);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        /* Effet de profondeur architecturale */
        .bg-glow {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 80% 20%, #0a0a35 0%, transparent 40%),
                        radial-gradient(circle at 10% 80%, #080825 0%, transparent 40%);
            z-index: -1;
        }

        .container { max-width: 1200px; margin: 0 auto; padding: 0 40px; }
        section { padding: 100px 0; }

        h1, h2 { font-family: var(--font-title); letter-spacing: -0.04em; line-height: 1.1; }

        /* --- HERO SECTION --- */
        .hero { min-height: 100vh; display: flex; align-items: center; }
        .hero-layout { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 80px; align-items: center; }
        
        .hero h1 { font-size: clamp(2.5rem, 6vw, 4.2rem); margin-bottom: 30px; }
        .hero p { font-size: 1.2rem; color: var(--text-muted); max-width: 580px; margin-bottom: 35px; font-weight: 300; }

        .btn {
            display: inline-block;
            padding: 22px 45px;
            background: var(--accent);
            color: var(--bg-dark);
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.15em;
            font-size: 0.8rem;
            transition: var(--transition);
        }
        .btn:hover { transform: translateY(-5px); box-shadow: 0 20px 40px rgba(255,255,255,0.15); }
        
        .sub-btn { display: block; margin-top: 15px; font-size: 0.85rem; color: var(--text-muted); opacity: 0.7; }

        .carousel-img { 
            width: 100%; 
            max-width: 500px;
            height: auto; 
            animation: float 10s ease-in-out infinite; 
        }

        /* --- GRID & CARDS --- */
        .grid-ux { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; margin-top: 50px; }
        .card-ux {
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 40px;
            transition: var(--transition);
        }
        .card-ux:hover { border-color: var(--accent); background: rgba(255,255,255,0.06); }
        .card-ux h3 { font-family: var(--font-title); margin-bottom: 15px; font-size: 1.4rem; }

        /* --- OFFRE IMPACT --- */
        .offer-highlight {
            background: var(--accent);
            color: var(--bg-dark);
            padding: 80px 40px;
            text-align: center;
            margin-top: 60px;
        }
        .offer-highlight h2 { color: var(--bg-dark); font-size: clamp(3rem, 8vw, 5rem); margin-bottom: 10px; }
        .offer-highlight p { font-weight: 600; text-transform: uppercase; letter-spacing: 2px; }

        /* --- FORMULAIRE --- */
        .form-box { max-width: 600px; margin: 60px auto 0; }
        input, select, textarea { 
            width: 100%; padding: 15px; background: transparent; border: none; 
            border-bottom: 1px solid var(--border); color: white; margin-bottom: 30px;
            font-family: var(--font-main); transition: var(--transition);
        }
        input:focus { border-bottom-color: var(--accent); outline: none; }

        @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }

        @media (max-width: 992px) {
            .hero-layout { grid-template-columns: 1fr; text-align: center; }
            .hero-visual { order: -1; margin-bottom: 40px; }
            .hero p { margin-left: auto; margin-right: auto; }
        }
    </style>
</head>
<body>

    <div class="bg-glow"></div>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu.</h1>
                <p>Tu es coach, ton revenu fait le yo‑yo et tu es épuisée par la complexité. On démantèle le superflu pour bâtir un système robuste.</p>
                <a href="#contact" class="btn">Je veux mon plan personnalisé</a>
                <span class="sub-btn">30 min en visio pour faire le point, sans bullshit.</span>
            </div>
            <div class="hero-visual">
                <img src="Cheval.png" alt="Système de vente stable" class="carousel-img">
            </div>
        </div>
    </section>

    <section id="offre">
        <div class="container">
            <h2>L’Accélérateur Simple</h2>
            <div class="grid-ux">
                <div class="card-ux"><h3>01. Clarté</h3><p>On nettoie tes fondations pour ne garder que l'essentiel qui vend.</p></div>
                <div class="card-ux"><h3>02. Message</h3><p>On définit comment parler de ton offre avec impact et vérité.</p></div>
                <div class="card-ux"><h3>03. Système</h3><p>Un canal unique, une méthode simple. Zéro usine à gaz.</p></div>
                <div class="card-ux"><h3>04. Focus</h3><p>Ton plan d'action précis pour les 30 prochains jours.</p></div>
            </div>
            
            <div class="offer-highlight">
                <p>Investissement</p>
                <h2>800€</h2>
                <a href="#contact" class="btn" style="background: var(--bg-dark); color: white; margin-top: 30px;">Démarrer le démantèlement</a>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div style="text-align: center;">
                <h2>Prête à arrêter de bricoler ?</h2>
                <div class="form-box">
                    <form>
                        <input type="text" placeholder="Prénom" required>
                        <input type="email" placeholder="Email" required>
                        <textarea rows="4" placeholder="Qu'est-ce que tu veux améliorer en priorité ?"></textarea>
                        <button type="submit" class="btn" style="width: 100%; border: none; cursor: pointer;">Envoyer ma demande</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer style="padding: 60px 0; text-align: center; border-top: 1px solid var(--border);">
        <p style="font-size: 0.8rem; letter-spacing: 2px; opacity: 0.4;">© MIORA — ARCHITECTE DE SYSTÈMES</p>
    </footer>

</body>
</html>
