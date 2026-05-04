<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stabilité & Systèmes | Miora</title>
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
            --transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
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

        /* Background dégradé fixe pour la profondeur */
        .bg-glow {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 80% 20%, #0a0a35 0%, transparent 40%),
                        radial-gradient(circle at 10% 80%, #080825 0%, transparent 40%);
            z-index: -1;
        }

        .container { max-width: 1200px; margin: 0 auto; padding: 0 40px; }
        section { padding: 120px 0; }

        h1, h2 { font-family: var(--font-title); letter-spacing: -0.04em; line-height: 1.1; }
        h2 { font-size: clamp(2rem, 4vw, 3rem); margin-bottom: 50px; }

        /* --- HERO --- */
        .hero { min-height: 100vh; display: flex; align-items: center; }
        .hero-layout { display: grid; grid-template-columns: 1.3fr 0.7fr; gap: 80px; align-items: center; }
        
        .hero h1 { font-size: clamp(2.8rem, 6vw, 4.5rem); margin-bottom: 30px; }
        .hero p { font-size: 1.2rem; color: var(--text-muted); max-width: 580px; margin-bottom: 30px; font-weight: 300; }

        .hero-list { list-style: none; margin-bottom: 45px; }
        .hero-list li { margin-bottom: 12px; display: flex; align-items: center; font-size: 1.1rem; }
        .hero-list li::before { content: ""; width: 6px; height: 6px; background: var(--accent); border-radius: 50%; margin-right: 15px; }

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
        .btn:hover { transform: scale(1.05); box-shadow: 0 20px 40px rgba(255,255,255,0.15); }
        .sub-btn { display: block; margin-top: 15px; font-size: 0.85rem; color: var(--text-muted); opacity: 0.7; }

        .carousel-img { width: 100%; height: auto; animation: float 10s ease-in-out infinite; }

        /* --- CARDS UX --- */
        .grid-ux { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .card-ux {
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 40px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }
        .card-ux:hover { border-color: var(--accent); background: rgba(255,255,255,0.06); transform: translateY(-5px); }
        .card-ux h3 { font-family: var(--font-title); font-size: 1.5rem; margin-bottom: 15px; }

        /* --- PRICE SECTION --- */
        .offer-container {
            margin-top: 60px;
            background: var(--accent);
            color: var(--bg-dark);
            padding: 80px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 40px;
        }
        .price-text h2 { color: var(--bg-dark); margin-bottom: 10px; font-size: 5rem; }
        .price-text p { color: rgba(5, 5, 26, 0.7); font-weight: 600; }

        /* --- FORMULAIRE --- */
        .form-box { max-width: 700px; margin: 0 auto; background: var(--bg-card); padding: 60px; border: 1px solid var(--border); }
        input, select, textarea { 
            width: 100%; padding: 20px; background: transparent; border: none; border-bottom: 1px solid var(--border);
            color: white; margin-bottom: 30px; font-family: var(--font-main); font-size: 1rem; transition: var(--transition);
        }
        input:focus { border-bottom-color: var(--accent); outline: none; }

        @keyframes float { 0%, 100% { transform: translateY(0) rotate(0); } 50% { transform: translateY(-25px) rotate(1deg); } }

        @media (max-width: 992px) {
            .hero-layout { grid-template-columns: 1fr; text-align: center; }
            .hero-list li { justify-content: center; }
            .offer-container { flex-direction: column; text-align: center; padding: 40px; }
            .price-text h2 { font-size: 3.5rem; }
        }
    </style>
</head>
<body>

    <div class="bg-glow"></div>

    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu.</h1>
                <p>Tu es coach, ton revenu fait le yo‑yo et tu es épuisée par la complexité. Ici, on démantèle le superflu pour bâtir un système qui dure.</p>
                <ul class="hero-list">
                    <li>Finit le bricolage au feeling</li>
                    <li>Un flux de demandes prévisible</li>
                    <li>Ton identité, sans les masques</li>
                </ul>
                <a href="#contact" class="btn">Je veux mon plan personnalisé</a>
                <span class="sub-btn">30 minutes en visio pour faire le point, sans bullshit.</span>
            </div>
            <div class="hero-visual">
                <img src="Cheval.png" alt="Architecture de vente" class="carousel-img">
            </div>
        </div>
    </section>

    <section>
        <div class="container">
            <h2>Est-ce que c'est toi ?</h2>
            <div class="grid-ux">
                <div class="card-ux">
                    <h3>Le Yo-Yo Permanent</h3>
                    <p>Tes mois se suivent mais ne se ressemblent jamais. L'insécurité est ton quotidien.</p>
                </div>
                <div class="card-ux">
                    <h3>L'Épuisement Digital</h3>
                    <p>Tu postes partout, tout le temps, sans savoir ce qui déclenche réellement une vente.</p>
                </div>
                <div class="card-ux">
                    <h3>Le Bruit Ambiant</h3>
                    <p>Scripts, challenges, hacks... Tu as tout testé et tu t'es perdue en chemin.</p>
                </div>
            </div>
        </div>
    </section>

    <section style="background: rgba(255,255,255,0.02);">
        <div class="container">
            <h2>L’Accélérateur Simple</h2>
            <div class="grid-ux">
                <div class="card-ux"><h3>01. Clarté</h3><p>On nettoie tes fondations pour ne garder que l'essentiel.</p></div>
                <div class="card-ux"><h3>02. Message</h3><p>On définit comment parler de ton offre avec impact et vérité.</p></div>
                <div class="card-ux"><h3>03. Système</h3><p>On déploie un canal unique et robuste. Zéro usine à gaz.</p></div>
                <div class="card-ux"><h3>04. Focus</h3><p>Ton plan d'action précis pour les 30 prochains jours.</p></div>
            </div>

            <div class="offer-container">
                <div class="price-text">
                    <p>INVESTISSEMENT</p>
                    <h2>800€</h2>
                    <p>Paiement en 1 ou 2 fois.</p>
                </div>
                <a href="#contact" class="btn" style="background: var(--bg-dark); color: white;">Réserver mon appel</a>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div style="text-align: center; margin-bottom: 60px;">
                <h2>Prête à devenir l'architecte<br>de ta réussite ?</h2>
                <p>Dis-moi où tu en es. Je te réponds sous 48h.</p>
            </div>
            <div class="form-box">
                <form>
                    <input type="text" placeholder="Ton prénom" required>
                    <input type="email" placeholder="Ton adresse email" required>
                    <select required>
                        <option value="" disabled selected>Type de coaching</option>
                        <option value="business">Business / Carrière</option>
                        <option value="vie">Vie / Mindset</option>
                        <option value="bienetre">Bien-être</option>
                    </select>
                    <textarea rows="4" placeholder="Ton défi majeur actuellement ?"></textarea>
                    <button type="submit" class="btn" style="width: 100%; border: none; cursor: pointer;">Envoyer la demande</button>
                </form>
            </div>
        </div>
    </section>

    <footer style="padding: 60px 0; text-align: center; border-top: 1px solid var(--border);">
        <p style="font-size: 0.9rem; letter-spacing: 2px; opacity: 0.5;">© MIORA — L'ARCHITECTE DE SYSTÈMES</p>
    </footer>

</body>
</html>
