<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Odacity - Fashion Landing Page</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            color: #333;
            line-height: 1.6;
        }

        /* Navbar */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 10%;
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
            color: #333;
        }

        .logo span {
            color: #ed6c30;
        }

        .nav-links {
            display: flex;
            gap: 60px;
        }

        .nav-links a {
            text-decoration: none;
            color: #666;
            font-size: 14px;
            text-transform: capitalize;
        }

        .login-btn {
            border: 1px solid #ed6c30;
            color: #ed6c30;
            padding: 8px 28px;
            border-radius: 6px;
            text-decoration: none;
            font-size: 14px;
        }

        /* Hero Section */
        .hero {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 10%;
            min-height: 80vh;
        }

        .hero-text {
            max-width: 500px;
        }

        .hero-text h1 {
            font-size: 36px;
            margin-bottom: 10px;
            line-height: 1.3;
        }

        .hero-text p {
            color: #777;
            font-size: 18px;
            margin-bottom: 30px;
        }

        .shop-btn {
            background-color: #ed6c30;
            color: white;
            padding: 12px 40px;
            border: none;
            border-radius: 2px;
            font-size: 16px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            box-shadow: 0 4px 12px rgba(237, 108, 48, 0.3);
        }

        .hero-image {
            position: relative;
        }

        .hero-image .circle {
            position: absolute;
            top: 20px;
            right: 0;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background-color: #ed6c30;
            z-index: -1;
        }

        .hero-image img {
            width: 400px;
            position: relative;
            z-index: 1;
        }

        /* Brands Section */
        .brands {
            display: flex;
            justify-content: flex-start;
            align-items: center;
            gap: 40px;
            padding: 20px 10%;
            opacity: 0.7;
        }

        .brands img {
            height: 30px;
        }

        .brands-text {
            font-size: 10px;
            color: #999;
            margin-left: 10%;
            margin-bottom: 40px;
        }

        /* Top Category */
        .top-category {
            padding: 40px 10%;
        }

        .top-category h2 {
            font-size: 18px;
            margin-bottom: 30px;
        }

        .category-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }

        .category-card {
            position: relative;
        }

        .category-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
        }

        .category-card .overlay-btn {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            background-color: #ed6c30;
            color: white;
            padding: 10px 20px;
            border: none;
            font-size: 14px;
        }

        .category-quote {
            max-width: 600px;
            margin-bottom: 40px;
        }

        .category-quote p {
            margin: 5px 0;
            color: #777;
        }

        .quote-text {
            text-align: center;
            max-width: 600px;
            margin: 0 auto 60px auto;
            color: #666;
        }

        /* Brighten Section */
        .brighten {
            padding: 0 10% 60px;
        }

        .brighten h2 {
            font-size: 18px;
            margin-bottom: 30px;
        }

        .brighten-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin-bottom: 40px;
        }

        .brighten-card {
            position: relative;
        }

        .brighten-card img {
            width: 100%;
            height: 280px;
            object-fit: cover;
        }

        .brighten-card .price-tag {
            position: absolute;
            bottom: 10px;
            left: 20%;
            background-color: white;
            padding: 5px 10px;
            border-radius: 4px;
            font-weight: bold;
        }

        .brighten-card .label {
            position: absolute;
            bottom: 10px;
            left: 0;
            background-color: #ed6c30;
            color: white;
            padding: 5px 10px;
            font-size: 12px;
        }

        .banner-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0;
        }

        .banner-section img {
            width: 100%;
            height: 400px;
            object-fit: cover;
        }

        .banner-text {
            background-color: #ffd4c4;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 40px;
        }

        .banner-text h3 {
            margin-bottom: 15px;
        }

        .banner-text p {
            color: #555;
            margin-bottom: 25px;
            font-size: 14px;
        }

        /* Explore Section */
        .explore {
            padding: 0 10% 60px;
        }

        .explore h2 {
            font-size: 18px;
            margin-bottom: 30px;
        }

        .explore-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
        }

        .explore-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            margin-bottom: 15px;
        }

        .explore-card p {
            color: #555;
        }

        /* Footer */
        footer {
            background-color: #fff;
            padding: 40px 10%;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 30px;
            border-top: 1px solid #eee;
        }

        .footer-logo {
            font-size: 22px;
            font-weight: bold;
            color: #333;
            margin-bottom: 15px;
        }

        .footer-logo span {
            color: #ed6c30;
        }

        .footer-desc {
            font-size: 12px;
            color: #777;
            margin-bottom: 20px;
        }

        .app-buttons img {
            height: 35px;
            margin-right: 10px;
        }

        .footer-column h4 {
            font-size: 14px;
            margin-bottom: 15px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 8px;
        }

        .footer-column ul li a {
            text-decoration: none;
            color: #777;
            font-size: 13px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            color: #333;
            font-size: 18px;
        }

        .copyright {
            text-align: center;
            padding: 20px 0;
            color: #999;
            font-size: 12px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero {
                flex-direction: column;
                text-align: center;
            }

            .hero-image img {
                width: 300px;
                margin-top: 30px;
            }

            .category-grid,
            .brighten-grid,
            .explore-grid,
            .banner-section,
            footer {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav>
        <div class="logo"><span>o</span>dacity</div>
        <div class="nav-links">
            <a href="#">About</a>
            <a href="#">Offer</a>
            <a href="#">Shop</a>
            <a href="#">Contact</a>
        </div>
        <a href="#" class="login-btn">Login</a>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-text">
            <h1>Clothes mean nothing until someone lives in them</h1>
            <p>Style is a way to say who you are without having to speak</p>
            <a href="#" class="shop-btn">Shop</a>
        </div>
        <div class="hero-image">
            <div class="circle"></div>
            <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80" alt="Fashion Model">
        </div>
    </section>

    <!-- Brands -->
    <div class="brands">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/Emporio_Armani_logo.svg/200px-Emporio_Armani_logo.svg.png" alt="Armani">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Burberry_logo.svg/200px-Burberry_logo.svg.png" alt="Burberry">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/00/Levi%27s-logo.svg/200px-Levi%27s-logo.svg.png" alt="Levi's">
        <span>❈CITY FASHION❈</span>
    </div>
    <div class="brands-text">
        What you wear is how you present yourself to the world, especially today, when human contacts are so quick. Fashion is instant language<br>
        I firmly believe that with the right footwear one can rule the world.
    </div>

    <!-- Top Category -->
    <section class="top-category">
        <h2>Top Category</h2>
        <div class="category-grid">
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
            </div>
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
                <button class="overlay-btn">Full Body Out Come</button>
            </div>
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
            </div>
        </div>
        <div class="category-quote">
            <p>You can have anything you want in life if you dress for it</p>
            <p>Clothes mean nothing until someone lives in them.</p>
            <p>Style is a way to say who you are without having to speak</p>
        </div>
        <div class="quote-text">
            Don't be into trends. Don't make fashion own you, but you decide what you are, what you want to express by the way you dress and the way to live
        </div>
    </section>

    <!-- Brighten Section -->
    <section class="brighten">
        <h2>Brighten Up your Daily Routine</h2>
        <div class="brighten-grid">
            <div class="brighten-card">
                <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
                <div class="label">Emotional brunette woman bluecoat</div>
                <div class="price-tag">$30</div>
            </div>
            <div class="brighten-card">
                <img src="https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
            </div>
            <div class="brighten-card">
                <img src="https://images.unsplash.com/photo-1502823403499-6ccfcf4fb453?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
            </div>
            <div class="brighten-card">
                <img src="https://images.unsplash.com/photo-1509631179647-0177331693ae?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Fashion">
            </div>
        </div>
        <div class="banner-section">
            <img src="https://images.unsplash.com/photo-1518611012118-696072aa579a?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Banner">
            <div class="banner-text">
                <h3>Teamwork begins by building trust</h3>
                <p>Don't be into trends. Don't make fashion own you, but you decide what you are, what you want to express by the way you dress and the way to live</p>
                <a href="#" class="shop-btn">Shop</a>
            </div>
        </div>
    </section>

    <!-- Explore Section -->
    <section class="explore">
        <h2>More to explore</h2>
        <div class="explore-grid">
            <div class="explore-card">
                <img src="https://images.unsplash.com/photo-1502823403499-6ccfcf4fb453?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Explore">
                <p>We are always interested in getting to our local Registered Massage Therapists!</p>
            </div>
            <div class="explore-card">
                <img src="https://images.unsplash.com/photo-1509631179647-0177331693ae?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Explore">
                <p>We hire those who have a passion for their industry, and a desire to help their community</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-column">
            <div class="footer-logo"><span>o</span>dacity</div>
            <p class="footer-desc">Is a practice committed to helping patients be pain-free, we are always accepting resumes from those clinicians and administrative staff who pride themselves on accepting new challenges</p>
            <div class="app-buttons">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/200px-Google_Play_Store_badge_EN.svg.png" alt="Google Play">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Download_on_the_App_Store_Badge.svg/200px-Download_on_the_App_Store_Badge.svg.png" alt="App Store">
            </div>
        </div>
        <div class="footer-column">
            <h4>Category</h4>
            <ul>
                <li><a href="#">Physiotherapist</a></li>
                <li><a href="#">Chiropractor</a></li>
                <li><a href="#">Registered Massage Therapist</a></li>
                <li><a href="#">Osteopathic Manual Practitioner</a></li>
            </ul>
        </div>
        <div class="footer-column">
            <h4>About</h4>
            <ul>
                <li><a href="#">Competitive Per</a></li>
                <li><a href="#">Treatment Compensation</a></li>
                <li><a href="#">Additional Income Through Enhanced Treatment Modalities</a></li>
            </ul>
        </div>
        <div class="footer-column">
            <h4>Support</h4>
            <ul>
                <li><a href="#">FAQ</a></li>
                <li><a href="#">Massage Expert</a></li>
                <li><a href="#">Provincial</a></li>
            </ul>
            <div class="social-links">
                <a href="#"><ion-icon name="logo-facebook"></ion-icon></a>
                <a href="#"><ion-icon name="logo-instagram"></ion-icon></a>
                <a href="#"><ion-icon name="logo-linkedin"></ion-icon></a>
                <a href="#"><ion-icon name="logo-twitter"></ion-icon></a>
            </div>
        </div>
    </footer>
    <div class="copyright">
        Design By Sourav Aich
    </div>

    <!-- Ionicons -->
    <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
</body>
</html>
