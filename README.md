# planetdestock
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Maquette - Planet Street Destock</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            color: #333;
            line-height: 1.6;
        }

        /* ===== HEADER ===== */
        .top-bar {
            background-color: #000;
            color: #FDB913;
            text-align: center;
            padding: 10px;
            font-size: 14px;
            font-weight: 500;
        }

        header {
            background-color: #fff;
            padding: 15px 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
        }

        .logo-circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .logo-text {
            font-size: 22px;
            font-weight: 700;
            color: #000;
        }

        .logo-text span {
            color: #FDB913;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            text-decoration: none;
            color: #000;
            font-weight: 500;
            font-size: 15px;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #FDB913;
        }

        /* ===== HERO ===== */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('../photo/WhatsApp Image 2026-01-15 at 13.26.00.jpeg');
            background-size: cover;
            background-position: center;
            height: 600px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
        }

        .hero-content h1 {
            font-size: 60px;
            font-weight: 700;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        .hero-content h1 span {
            color: #FDB913;
        }

        .hero-content .slogan {
            font-size: 28px;
            margin-bottom: 20px;
            color: #FDB913;
            font-weight: 500;
        }

        .hero-content p {
            font-size: 18px;
            max-width: 600px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            padding: 15px 40px;
            background-color: #FDB913;
            color: #000;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            border-radius: 4px;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn:hover {
            background-color: #e5a610;
            transform: translateY(-2px);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid #fff;
            color: #fff;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background-color: #fff;
            color: #000;
        }

        /* ===== CHIFFRES ===== */
        .stats {
            background-color: #000;
            padding: 60px 50px;
            display: flex;
            justify-content: center;
            gap: 100px;
        }

        .stat-item {
            text-align: center;
            color: #fff;
        }

        .stat-number {
            font-size: 48px;
            font-weight: 700;
            color: #FDB913;
        }

        .stat-label {
            font-size: 16px;
            opacity: 0.8;
        }

        /* ===== SECTIONS ===== */
        section {
            padding: 80px 50px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .section-title p {
            font-size: 18px;
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }

        /* ===== RÉASSURANCE ===== */
        .reassurance {
            background-color: #f5f5f5;
        }

        .reassurance-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .reassurance-item {
            background-color: #fff;
            padding: 40px 30px;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s;
        }

        .reassurance-item:hover {
            transform: translateY(-5px);
        }

        .reassurance-icon {
            width: 80px;
            height: 80px;
            background-color: #FDB913;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 36px;
        }

        .reassurance-item h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .reassurance-item p {
            color: #666;
        }

        /* ===== COMMENT CA MARCHE ===== */
        .how-it-works {
            background-color: #fff;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .step {
            text-align: center;
            position: relative;
        }

        .step-number {
            width: 60px;
            height: 60px;
            background-color: #FDB913;
            color: #000;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: 700;
            margin: 0 auto 20px;
        }

        .step h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }

        .step p {
            color: #666;
            font-size: 14px;
        }

        /* ===== MARQUES ===== */
        .brands {
            background-color: #f5f5f5;
        }

        .brands-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .brand-item {
            background-color: #fff;
            padding: 25px;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: all 0.3s;
            cursor: pointer;
        }

        .brand-item:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        .brand-logo {
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 14px;
            color: #333;
        }

        .see-all {
            text-align: center;
            margin-top: 40px;
        }

        /* ===== BONS PLANS ===== */
        .deals {
            background-color: #fff;
        }

        .deals-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .deal-card {
            background-color: #fff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .deal-card:hover {
            transform: translateY(-5px);
        }

        .deal-image {
            height: 200px;
            background-color: #eee;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #999;
            position: relative;
        }

        .deal-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: #FDB913;
            color: #000;
            padding: 8px 15px;
            font-weight: 700;
            font-size: 18px;
            border-radius: 4px;
        }

        .deal-content {
            padding: 20px;
        }

        .deal-content h3 {
            font-size: 18px;
            margin-bottom: 5px;
        }

        .deal-content p {
            color: #666;
            font-size: 14px;
        }

        /* ===== TÉMOIGNAGES ===== */
        .testimonials {
            background-color: #000;
            color: #fff;
        }

        .testimonials .section-title h2 {
            color: #fff;
        }

        .testimonials .section-title p {
            color: rgba(255,255,255,0.7);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .testimonial-card {
            background-color: #1a1a1a;
            padding: 30px;
            border-radius: 8px;
            text-align: center;
        }

        .stars {
            color: #FDB913;
            font-size: 20px;
            margin-bottom: 15px;
        }

        .testimonial-text {
            font-style: italic;
            margin-bottom: 20px;
            opacity: 0.9;
            line-height: 1.8;
        }

        .testimonial-author {
            color: #FDB913;
            font-weight: 500;
        }

        /* ===== GALERIE ===== */
        .gallery {
            background-color: #f5f5f5;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .gallery-item {
            height: 250px;
            background-color: #ddd;
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 14px;
            cursor: pointer;
            transition: opacity 0.3s;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }

        .gallery-item:hover {
            opacity: 0.8;
        }

        /* ===== INSTAGRAM ===== */
        .instagram {
            background-color: #fff;
        }

        .instagram-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 15px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .instagram-item {
            height: 200px;
            background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 14px;
        }

        .instagram-handle {
            text-align: center;
            margin-top: 30px;
        }

        .instagram-handle a {
            font-size: 24px;
            color: #000;
            text-decoration: none;
            font-weight: 600;
        }

        /* ===== NEWSLETTER ===== */
        .newsletter {
            background-color: #FDB913;
            text-align: center;
        }

        .newsletter h2 {
            font-size: 32px;
            margin-bottom: 10px;
        }

        .newsletter p {
            margin-bottom: 30px;
            font-size: 18px;
        }

        .newsletter-form {
            display: flex;
            justify-content: center;
            gap: 15px;
            max-width: 500px;
            margin: 0 auto;
        }

        .newsletter-form input {
            flex: 1;
            padding: 15px 20px;
            border: none;
            border-radius: 4px;
            font-size: 16px;
        }

        .newsletter-form button {
            padding: 15px 30px;
            background-color: #000;
            color: #fff;
            border: none;
            border-radius: 4px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .newsletter-form button:hover {
            background-color: #333;
        }

        /* ===== FOOTER ===== */
        footer {
            background-color: #000;
            color: #fff;
            padding: 60px 50px 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 50px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-brand .logo-text {
            color: #fff;
            font-size: 24px;
            margin-bottom: 15px;
        }

        .footer-brand p {
            opacity: 0.7;
            font-size: 14px;
            line-height: 1.8;
        }

        .footer-section h4 {
            color: #FDB913;
            margin-bottom: 20px;
            font-size: 16px;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section li {
            margin-bottom: 10px;
        }

        .footer-section a {
            color: #fff;
            text-decoration: none;
            opacity: 0.7;
            font-size: 14px;
            transition: opacity 0.3s;
        }

        .footer-section a:hover {
            opacity: 1;
            color: #FDB913;
        }

        .footer-bottom {
            border-top: 1px solid #333;
            margin-top: 40px;
            padding-top: 20px;
            text-align: center;
            opacity: 0.5;
            font-size: 14px;
        }

        /* ===== PAGE INDICATOR ===== */
        .page-indicator {
            position: fixed;
            top: 50%;
            right: 20px;
            transform: translateY(-50%);
            background-color: rgba(0,0,0,0.8);
            color: #fff;
            padding: 15px 20px;
            border-radius: 8px;
            font-size: 12px;
            z-index: 9999;
        }

        .page-indicator h3 {
            color: #FDB913;
            margin-bottom: 10px;
            font-size: 14px;
        }

        .page-indicator ul {
            list-style: none;
        }

        .page-indicator li {
            margin-bottom: 5px;
            padding-left: 15px;
            position: relative;
        }

        .page-indicator li::before {
            content: "→";
            position: absolute;
            left: 0;
            color: #FDB913;
        }

        /* ===== MAQUETTE LABEL ===== */
        .maquette-label {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background-color: #e74c3c;
            color: #fff;
            text-align: center;
            padding: 10px;
            font-weight: 600;
            z-index: 10000;
            font-size: 14px;
        }

        body {
            padding-top: 40px;
        }
    </style>
</head>
<body>

<!-- Label Maquette -->
<div class="maquette-label">
    MAQUETTE VISUELLE - Aperçu du futur site Planet Street Destock
</div>

<!-- Indicateur de page -->
<div class="page-indicator">
    <h3>PAGE D'ACCUEIL</h3>
    <ul>
        <li>En-tête</li>
        <li>Hero</li>
        <li>Chiffres</li>
        <li>Réassurance</li>
        <li>Comment ça marche</li>
        <li>Marques</li>
        <li>Bons Plans</li>
        <li>Témoignages</li>
        <li>Galerie</li>
        <li>Instagram</li>
        <li>Newsletter</li>
        <li>Pied de page</li>
    </ul>
</div>

<!-- Bandeau promo -->
<div class="top-bar">
    Arrivage permanent - Jusqu'à -50% sur les grandes marques
</div>

<!-- Header -->
<header>
    <div class="logo">
        <div class="logo-circle"><img src="../photo/WhatsApp Image 2026-01-14 at 14.40.22.jpeg" alt="Logo Planet Street Destock"></div>
        <div class="logo-text">PLANET STREET <span>DESTOCK</span></div>
    </div>
    <nav>
        <ul>
            <li><a href="MAQUETTE-VISUELLE.html" class="active">Accueil</a></li>
            <li><a href="MAQUETTE-MARQUES.html">Nos Marques</a></li>
            <li><a href="MAQUETTE-BONS-PLANS.html">Bons Plans</a></li>
            <li><a href="MAQUETTE-VIP.html">Programme VIP</a></li>
            <li><a href="MAQUETTE-FAQ.html">FAQ</a></li>
            <li><a href="MAQUETTE-CONTACT.html">Contact</a></li>
        </ul>
    </nav>
</header>

<!-- Hero -->
<section class="hero">
    <div class="hero-content">
        <h1>PLANET STREET <span>DESTOCK</span></h1>
        <p class="slogan">Des Marques, Des Prix</p>
        <p>Votre magasin spécialisé dans le destockage de grandes marques de jeans, prêt-à-porter et streetwear.</p>
        <a href="MAQUETTE-MARQUES.html" class="btn">Découvrir nos marques</a>
        <a href="MAQUETTE-CONTACT.html" class="btn btn-outline">Nous trouver</a>
    </div>
</section>

<!-- Stats -->
<section class="stats">
    <div class="stat-item">
        <div class="stat-number">+20</div>
        <div class="stat-label">ans d'expérience</div>
    </div>
    <div class="stat-item">
        <div class="stat-number">+500m²</div>
        <div class="stat-label">d'espace</div>
    </div>
    <div class="stat-item">
        <div class="stat-number">14+</div>
        <div class="stat-label">marques</div>
    </div>
    <div class="stat-item">
        <div class="stat-number">-50%</div>
        <div class="stat-label">de réduction</div>
    </div>
</section>

<!-- Réassurance -->
<section class="reassurance">
    <div class="section-title">
        <h2>Pourquoi nous choisir ?</h2>
        <p>Des avantages exclusifs pour nos clients</p>
    </div>
    <div class="reassurance-grid">
        <div class="reassurance-item">
            <div class="reassurance-icon">⭐</div>
            <h3>Programme Fidélité</h3>
            <p>Votre fidélité récompensée : recevez 10% de vos achats en bon d'achat</p>
        </div>
        <div class="reassurance-item">
            <div class="reassurance-icon">👕</div>
            <h3>Marques Iconiques</h3>
            <p>Les plus grandes marques de streetwear et workwear à prix déstockés</p>
        </div>
        <div class="reassurance-item">
            <div class="reassurance-icon">📍</div>
            <h3>Magasin Bordeaux</h3>
            <p>+500m² d'espace à Villenave-d'Ornon, parking gratuit</p>
        </div>
    </div>
</section>

<!-- Comment ça marche -->
<section class="how-it-works">
    <div class="section-title">
        <h2>Comment ça marche ?</h2>
        <p>Le destockage de qualité, simplement</p>
    </div>
    <div class="steps">
        <div class="step">
            <div class="step-number">1</div>
            <h3>Fins de collections</h3>
            <p>Nous achetons les fins de collections des grandes marques</p>
        </div>
        <div class="step">
            <div class="step-number">2</div>
            <h3>Prix réduits</h3>
            <p>Nous vous les proposons avec des réductions de -20% à -50%</p>
        </div>
        <div class="step">
            <div class="step-number">3</div>
            <h3>Vous économisez</h3>
            <p>Vous achetez des produits neufs et authentiques à prix réduits</p>
        </div>
    </div>
</section>

<!-- Marques -->
<section class="brands">
    <div class="section-title">
        <h2>Nos Marques Partenaires</h2>
        <p>Chaque jour, des articles de qualité issus des collections des Grandes Marques</p>
    </div>
    <div class="brands-grid">
        <div class="brand-item"><div class="brand-logo">CARHARTT</div></div>
        <div class="brand-item"><div class="brand-logo">LEVI'S</div></div>
        <div class="brand-item"><div class="brand-logo">VOLCOM</div></div>
        <div class="brand-item"><div class="brand-logo">G-STAR</div></div>
        <div class="brand-item"><div class="brand-logo">SUPERDRY</div></div>
        <div class="brand-item"><div class="brand-logo">ELEMENT</div></div>
        <div class="brand-item"><div class="brand-logo">DICKIES</div></div>
        <div class="brand-item"><div class="brand-logo">QUIKSILVER</div></div>
        <div class="brand-item"><div class="brand-logo">BILLABONG</div></div>
        <div class="brand-item"><div class="brand-logo">LEE</div></div>
        <div class="brand-item"><div class="brand-logo">ONLY</div></div>
        <div class="brand-item"><div class="brand-logo">LE TEMPS DES CERISES</div></div>
        <div class="brand-item"><div class="brand-logo">ROXY</div></div>
        <div class="brand-item"><div class="brand-logo">REPLAY</div></div>
    </div>
    <div class="see-all">
        <a href="MAQUETTE-MARQUES.html" class="btn">Voir toutes nos marques</a>
    </div>
</section>

<!-- Bons Plans -->
<section class="deals">
    <div class="section-title">
        <h2>Bons Plans de la Semaine</h2>
        <p>Des réductions exceptionnelles - Quantités limitées</p>
    </div>
    <div class="deals-grid">
        <div class="deal-card">
            <div class="deal-image" style="background-image: url('../photo/levis.jpeg');">
                <div class="deal-badge">-30%</div>
            </div>
            <div class="deal-content">
                <h3>Jean Levi's 501</h3>
                <p>Le classique intemporel</p>
            </div>
        </div>
        <div class="deal-card">
            <div class="deal-image" style="background-image: url('../photo/carrhart.jpeg');">
                <div class="deal-badge">-50%</div>
            </div>
            <div class="deal-content">
                <h3>Veste Carhartt</h3>
                <p>Workwear authentique</p>
            </div>
        </div>
        <div class="deal-card">
            <div class="deal-image" style="background-image: url('../photo/element .jpeg');">
                <div class="deal-badge">-40%</div>
            </div>
            <div class="deal-content">
                <h3>T-shirt Element</h3>
                <p>Style skateboard</p>
            </div>
        </div>
    </div>
    <div class="see-all">
        <a href="MAQUETTE-BONS-PLANS.html" class="btn">Voir tous les bons plans</a>
    </div>
</section>

<!-- Témoignages -->
<section class="testimonials">
    <div class="section-title">
        <h2>Ce que disent nos clients</h2>
        <p>Plus de 20 ans de confiance</p>
    </div>
    <div class="testimonials-grid">
        <div class="testimonial-card">
            <div class="stars">★★★★★</div>
            <p class="testimonial-text">"Super magasin, j'y trouve toujours de bonnes affaires sur mes marques préférées ! Le personnel est accueillant et de bon conseil."</p>
            <div class="testimonial-author">— Marc D.</div>
        </div>
        <div class="testimonial-card">
            <div class="stars">★★★★★</div>
            <p class="testimonial-text">"Des prix imbattables sur des marques de qualité. Je recommande vivement ! J'ai équipé toute ma famille."</p>
            <div class="testimonial-author">— Sophie L.</div>
        </div>
        <div class="testimonial-card">
            <div class="stars">★★★★★</div>
            <p class="testimonial-text">"Plus de 20 ans que je suis client. Le service est toujours au top et les arrivages réguliers !"</p>
            <div class="testimonial-author">— Thomas R.</div>
        </div>
    </div>
</section>

<!-- Galerie -->
<section class="gallery">
    <div class="section-title">
        <h2>Notre Magasin</h2>
        <p>Découvrez notre espace de +500m² dédié aux grandes marques</p>
    </div>
    <div class="gallery-grid">
        <div class="gallery-item" style="background-image: url('../photo/WhatsApp Image 2026-01-15 at 13.26.00.jpeg');"></div>
        <div class="gallery-item" style="background-image: url('../photo/WhatsApp Image 2026-01-15 at 13.26.02.jpeg');"></div>
        <div class="gallery-item" style="background-image: url('../photo/portant .jpeg');"></div>
        <div class="gallery-item" style="background-image: url('../photo/mannequin 1.jpeg');"></div>
    </div>
</section>

<!-- Instagram -->
<section class="instagram">
    <div class="section-title">
        <h2>Suivez-nous sur Instagram</h2>
        <p>Nouveautés, arrivages, bons plans... Restez connectés !</p>
    </div>
    <div class="instagram-grid">
        <div class="instagram-item">Post Instagram</div>
        <div class="instagram-item">Post Instagram</div>
        <div class="instagram-item">Post Instagram</div>
        <div class="instagram-item">Post Instagram</div>
    </div>
    <div class="instagram-handle">
        <a href="https://www.instagram.com/planetstreetdestock_/" target="_blank">@planetstreetdestock_</a>
    </div>
</section>

<!-- Newsletter -->
<section class="newsletter">
    <h2>Restez Informé</h2>
    <p>Nouveaux arrivages, bons plans, promotions exclusives...</p>
    <div class="newsletter-form">
        <input type="email" placeholder="Votre adresse email">
        <button type="submit">S'inscrire</button>
    </div>
</section>

<!-- Footer -->
<footer>
    <div class="footer-content">
        <div class="footer-brand">
            <div class="logo-text">PLANET STREET <span style="color: #FDB913;">DESTOCK</span></div>
            <p>Des Marques, Des Prix</p>
            <br>
            <p>
                2 Rue Louis de Funès<br>
                33140 Villenave-d'Ornon<br>
                Lun-Sam : 10h-19h
            </p>
        </div>
        <div class="footer-section">
            <h4>Navigation</h4>
            <ul>
                <li><a href="MAQUETTE-VISUELLE.html">Accueil</a></li>
                <li><a href="MAQUETTE-MARQUES.html">Nos Marques</a></li>
                <li><a href="MAQUETTE-BONS-PLANS.html">Bons Plans</a></li>
                <li><a href="MAQUETTE-VIP.html">Programme VIP</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Informations</h4>
            <ul>
                <li><a href="MAQUETTE-FAQ.html">FAQ</a></li>
                <li><a href="MAQUETTE-CONTACT.html">Contact</a></li>
                <li><a href="#">Mentions légales</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Suivez-nous</h4>
            <ul>
                <li><a href="https://www.instagram.com/planetstreetdestock_/" target="_blank">Instagram</a></li>
                <li><a href="https://www.instagram.com/planetstreetdestock_/" target="_blank">@planetstreetdestock_</a></li>
            </ul>
        </div>
    </div>
    <div class="footer-bottom">
        © 2026 Planet Street Destock - Tous droits réservés
    </div>
</footer>

</body>
</html>
