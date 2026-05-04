<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stabilité & Systèmes | Démanteler le cirque du coaching</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-dark: #05051a; 
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
            color: var(--text-main);
            font-family: var(--font-main);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        .container { max-width: 1100px; margin: 0 auto; padding: 0 30px; }
        
        section { padding: 100px 0; border-bottom: 1px solid rgba(255,255,255,0.05); }

        h1, h2, h3 { font-family: var(--font-title); line-height: 1.1; margin-bottom: 30px; }
        p { color: var(--text-muted); margin-bottom: 20px; font-weight: 300; }

        /* --- HERO --- */
        .hero { min-height: 100vh; display: flex; align-items: center; background: radial-gradient(circle at 80% 20%, var(--bg-accent) 0%, var(--bg-dark) 70%); }
        .hero-layout { display: grid; grid-template-columns: 1.2fr 0.8fr; gap: 60px; align-items: center; }
        .hero h1 { font-size: clamp(2.5rem, 5vw, 3.8rem); letter-spacing: -0.03em; }
        
        .hero-list { list-style: none; margin: 30px 0; }
        .hero-list li { margin-bottom: 15px; display: flex; align-items: center; color: white; font-weight: 400; }
        .hero-list li::before { content: "→"; margin-right: 15px; color: var(--text-muted); }

        .btn-premium {
            display: inline-block;
            padding: 20px 40px;
            background: white;
            color: var(--bg-dark);
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            font-size: 0.85rem;
            transition: var(--transition);
        }
        .btn-premium:hover { transform: translateY(-3px); box-shadow: 0 10px 30px rgba(255,255,255,0.2); }
        .sub-btn { display: block; margin-top: 15px; font-size: 0.8rem; color: var(--text-muted); }

        .carousel-img { width: 100%; height: auto; animation: float 8s ease-in-out infinite; }

        /* --- SECTION 2: EST-CE TOI --- */
        .pain-points { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-top: 50px; }
        .card { padding: 30px; border: 1px solid rgba(255,255,255,0.1); transition: var(--transition); }
        .card:hover { background: rgba(255,255,255,0.03); border-color: white; }

        /* --- SECTION 3: ACCELERATEUR --- */
        .offer-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; margin: 50px 0; }
        .step { background: rgba(255,255,255,0.03); padding: 25px; border-top: 2px solid white; }
        .step h3 { font-size: 1.2rem; margin-bottom: 15px; }
        .price-box { text-align: center; padding: 60px; background: white; color: var(--bg-dark); margin-top: 40px; }
        .price-box h2 { font-size: 4rem; margin-bottom: 10px; }

        /* --- FORMULAIRE --- */
        .form-container { max-width: 600px; margin: 50px auto; }
        input, select, textarea { 
            width: 100%; padding: 15px; background: transparent; border: 1px solid rgba(255,255,255,0.2); 
            color: white; margin-bottom: 20px; font-family: var(--font-main);
        }
        input:focus, textarea:focus { border-color: white; outline: none; }

        @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }

        @media (max-width: 900px) { .hero-layout { grid-template-columns: 1fr; text-align: center; } .hero-list li { justify-content: center; } }
    </style>
</head>
<body>

    <!-- SECTION 1: HERO -->
    <section class="hero">
        <div class="container hero-layout">
            <div class="hero-text">
                <h1>On arrête le cirque,<br>on stabilise ton revenu.</h1>
                <p>Tu es coach, tu as déjà des clientes, mais ton revenu fait le yo‑yo et tu es épuisée par les stratégies compliquées.</p>
                <ul class="hero-list">
                    <li>Arrêter de bricoler ta com’ au feeling</li>
                    <li>Un système clair pour des appels chaque mois</li>
                    <li>Rester toi-même sans jouer un personnage</li>
                </ul>
                <a href="#contact" class="btn-premium">Je veux mon plan personnalisé</a>
                <span class="sub-btn">30 minutes en visio pour faire le point, sans pression.</span>
            </div>
            <div class="hero-visual">
                <img src="Cheval.png" alt="Système de vente stable" class="carousel-img">
            </div>
        </div>
    </section>

    <!-- SECTION 2: EST-CE TOI -->
    <section>
        <div class="container">
            <h2>Est‑ce que c’est toi ?</h2>
            <p>Si tu lis ça, il y a de grandes chances que tu te reconnaisses ici :</p>
            <div class="pain-points">
                <div class="card">Tes mois ne se ressemblent pas et ça t'épuise.</div>
                <div class="card">Tu es présente partout, mais tu ne sais pas ce qui vend.</div>
                <div class="card">Tu as testé trop de scripts et tu as perdu ton identité.</div>
                <div class="card">Tu veux un système que tu peux tenir même débordée.</div>
            </div>
        </div>
    </section>

    <!-- SECTION 3: L'ACCELERATEUR -->
    <section style="background: rgba(255,255,255,0.02);">
        <div class="container">
            <h2>L’Accélérateur Simple</h2>
            <p>4 sessions de 30 minutes pour remettre ton activité sur des rails.</p>
            
            <div class="offer-grid">
                <div class="step"><h3>1. Clarté</h3><p>Qui, quoi, pourquoi. On simplifie tes fondations.</p></div>
                <div class="step"><h3>2. Message</h3><p>Comment parler de ton offre sans forcer.</p></div>
                <div class="step"><h3>3. Système</h3><p>Un canal unique. Zéro usine à gaz.</p></div>
                <div class="step"><h3>4. Action</h3><p>Ton plan sur 30 jours. Ce qu'on garde, ce qu'on jette.</p></div>
            </div>

            <div class="price-box">
                <p style="color: #05051a; font-weight: 700; text-transform: uppercase;">Investissement</p>
                <h2>800 €</h2>
                <p style="color: #05051a;">Paiement en 1 ou 2 fois. Premier call décisif.</p>
                <a href="#contact" class="btn-premium" style="background: #05051a; color: white;">Réserver mon appel</a>
            </div>
        </div>
    </section>

    <!-- SECTION 5: MIORA -->
    <section>
        <div class="container">
            <div style="max-width: 800px;">
                <h2>Qui je suis (et ce que je refuse)</h2>
                <p>Je m’appelle <strong>Miora</strong>. J’accompagne des coachs à mettre en place des systèmes simples, sans tunnels compliqués ni manipulation.</p>
                <p>J'ai géré des systèmes pour des business à gros chiffres. J'en ai vu la complexité... et c'est précisément ce que je refuse de te vendre. Mon approche est basée sur la sincérité et le respect de tes limites.</p>
            </div>
        </div>
    </section>

    <!-- SECTION 6: FORMULAIRE -->
    <section id="contact">
        <div class="container">
            <div style="text-align: center;">
                <h2>Prête à arrêter de bricoler ?</h2>
                <p>Dis-moi où tu en es, je te réponds sous 48h.</p>
            </div>
            <div class="form-container">
                <form>
                    <input type="text" placeholder="Prénom" required>
                    <input type="email" placeholder="Email" required>
                    <select>
                        <option value="">Type de coaching</option>
                        <option value="vie">Vie / Mindset</option>
                        <option value="business">Business / Carrière</option>
                        <option value="bienetre">Bien-être</option>
                    </select>
                    <textarea rows="5" placeholder="Qu'est-ce que tu veux améliorer en priorité ?"></textarea>
                    <button type="submit" class="btn-premium" style="width: 100%; cursor: pointer; border: none;">Envoyer ma demande</button>
                </form>
            </div>
        </div>
    </section>

    <footer style="padding: 50px 0; text-align: center; border-top: 1px solid rgba(255,255,255,0.05);">
        <p style="font-size: 0.8rem;">© Miora – L’Accélérateur Simple</p>
    </footer>

</body>
</html>
