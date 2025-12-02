
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BusySoaps - Handcrafted Soap Art</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lora:wght@400;500;600;700&family=Open+Sans:wght@300;400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            /* Lighter, greener colors */
            --logo-tan: #f9f4e8;
            --logo-green: #7a9a6f;
            --logo-green-light: #8aaa7f;
            --logo-green-dark: #6a8a5f;
            --tan-light: #fefaf0;
            --tan-medium: #f0e8d8;
            --tan-dark: #e2dac8;
            --cream: #fffef9;
            --transition: all 0.3s ease;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            background-color: var(--cream);
            color: var(--logo-green);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, .logo-text, .section-title {
            font-family: 'Lora', serif;
            font-weight: 600;
            color: var(--logo-green);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            background-color: var(--logo-tan);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid var(--logo-green);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo {
            height: 65px;
            filter: drop-shadow(0 2px 4px rgba(122, 154, 111, 0.2));
        }
        
        .logo-text {
            font-size: 32px;
            font-weight: 700;
            color: var(--logo-green);
        }
        
        .logo-text span {
            color: var(--logo-green);
            font-weight: 400;
            font-style: italic;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }
        
        nav a {
            color: var(--logo-green);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: var(--transition);
            padding: 5px 0;
            position: relative;
        }
        
        nav a:hover {
            color: var(--logo-green-dark);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--logo-green);
            bottom: 0;
            left: 0;
            transition: var(--transition);
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--logo-green);
            font-size: 24px;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background-color: var(--logo-tan);
            color: var(--logo-green);
            padding: 100px 0;
            text-align: center;
            border-bottom: 3px solid var(--logo-green);
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--logo-green);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--logo-green);
            color: var(--logo-tan);
            padding: 14px 32px;
            border-radius: 0;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: var(--transition);
            border: 2px solid var(--logo-green);
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--logo-green-dark);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(122, 154, 111, 0.2);
        }
        
        .btn-outline {
            display: inline-block;
            background-color: transparent;
            color: var(--logo-green);
            padding: 12px 30px;
            border-radius: 0;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: var(--transition);
            border: 2px solid var(--logo-green);
            cursor: pointer;
        }
        
        .btn-outline:hover {
            background-color: var(--logo-green);
            color: var(--logo-tan);
        }
        
        /* Products Section */
        .section-title {
            text-align: center;
            margin: 80px 0 50px;
            font-size: 40px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 3px;
            background-color: var(--logo-green);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 30px;
            margin-bottom: 80px;
        }
        
        .product-card {
            background-color: var(--logo-tan);
            border-radius: 0;
            overflow: hidden;
            border: 2px solid var(--logo-green);
            transition: var(--transition);
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(122, 154, 111, 0.15);
        }
        
        .product-img {
            width: 100%;
            height: 280px;
            object-fit: cover;
            border-bottom: 2px solid var(--logo-green);
        }
        
        .product-info {
            padding: 25px;
        }
        
        .product-name {
            font-size: 24px;
            margin-bottom: 10px;
            color: var(--logo-green);
        }
        
        .product-desc {
            color: var(--logo-green);
            margin-bottom: 20px;
            opacity: 0.9;
        }
        
        /* About Section */
        .about {
            background-color: var(--cream);
            padding: 80px 0;
            border-top: 3px solid var(--logo-green);
            border-bottom: 3px solid var(--logo-green);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-img {
            flex: 1;
            height: 400px;
            background-image: url('https://i.postimg.cc/LX8dfbLS/IMG_7106.jpg');
            background-size: cover;
            background-position: center;
            border: 3px solid var(--logo-green);
            background-color: var(--logo-tan);
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h2 {
            margin-bottom: 25px;
            font-size: 32px;
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: var(--logo-green);
        }
        
        /* Slide Gallery Section */
        .gallery-section {
            padding: 80px 0;
            background-color: var(--logo-tan);
        }
        
        .slide-gallery {
            position: relative;
            max-width: 900px;
            margin: 40px auto 0;
            overflow: hidden;
            border: 3px solid var(--logo-green);
        }
        
        .slides-container {
            display: flex;
            transition: transform 0.5s ease;
        }
        
        .slide {
            min-width: 100%;
            height: 500px;
            position: relative;
        }
        
        .slide-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .slide-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(122, 154, 111, 0.85);
            color: var(--logo-tan);
            padding: 15px;
            text-align: center;
            font-family: 'Lora', serif;
            font-size: 18px;
        }
        
        .gallery-controls {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            gap: 20px;
        }
        
        .prev-btn, .next-btn {
            background-color: var(--logo-green);
            color: var(--logo-tan);
            border: none;
            width: 50px;
            height: 50px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .prev-btn:hover, .next-btn:hover {
            background-color: var(--logo-green-dark);
        }
        
        .gallery-dots {
            display: flex;
            gap: 10px;
        }
        
        .dot {
            width: 12px;
            height: 12px;
            background-color: var(--tan-medium);
            border-radius: 50%;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .dot.active {
            background-color: var(--logo-green);
        }
        
        /* Values Section */
        .values {
            padding: 80px 0;
            background-color: var(--cream);
        }
        
        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .value-card {
            text-align: center;
            padding: 30px;
            border: 2px solid var(--logo-green);
            background-color: var(--logo-tan);
            transition: var(--transition);
        }
        
        .value-card:hover {
            transform: translateY(-5px);
            background-color: var(--tan-light);
        }
        
        .value-icon {
            font-size: 40px;
            color: var(--logo-green);
            margin-bottom: 20px;
        }
        
        .value-card h3 {
            margin-bottom: 15px;
            font-size: 22px;
        }
        
        /* Footer */
        footer {
            background-color: var(--logo-green);
            color: var(--logo-tan);
            padding: 70px 0 25px;
            border-top: 3px solid var(--logo-tan);
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-logo {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--logo-tan);
        }
        
        .footer-section h3 {
            font-size: 20px;
            margin-bottom: 25px;
            color: var(--logo-tan);
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 2px;
            background-color: var(--logo-tan);
            bottom: 0;
            left: 0;
        }
        
        .footer-section p {
            margin-bottom: 15px;
            opacity: 0.9;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(249, 244, 232, 0.2);
            border-radius: 0;
            color: var(--logo-tan);
            font-size: 18px;
            transition: var(--transition);
            border: 1px solid var(--logo-tan);
        }
        
        .social-icons a:hover {
            background-color: var(--logo-tan);
            color: var(--logo-green);
            transform: translateY(-3px);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: var(--logo-tan);
            text-decoration: none;
            transition: var(--transition);
            opacity: 0.9;
        }
        
        .footer-links a:hover {
            opacity: 1;
            padding-left: 5px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .contact-info div {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-info i {
            width: 20px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 25px;
            border-top: 1px solid rgba(249, 244, 232, 0.3);
            font-size: 14px;
            opacity: 0.8;
        }
        
        .highlight {
            color: var(--logo-tan);
            font-weight: 700;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 40px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .slide {
                height: 400px;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--logo-tan);
                flex-direction: column;
                padding: 20px;
                text-align: center;
                border-top: 3px solid var(--logo-green);
                z-index: 999;
            }
            
            nav ul.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            .section-title {
                font-size: 32px;
            }
            
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .slide {
                height: 350px;
            }
        }
        
        @media (max-width: 576px) {
            .logo-text {
                font-size: 28px;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .section-title {
                font-size: 28px;
            }
            
            .footer-content {
                flex-direction: column;
            }
            
            .slide {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <!-- Header with Logo -->
    <header>
        <div class="container header-container">
            <div class="logo-container">
                <img src="https://i.postimg.cc/Kz8XLHLH/IMG_7117.jpg" alt="BusySoaps Logo" class="logo">
                <div class="logo-text">Busy<span>Soaps</span></div>
            </div>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#values">Values</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Handcrafted Soap Art</h1>
            <p>Natural, clean, and thoughtfully crafted soaps made with only the finest ingredients. Each bar is a unique creation designed to elevate your daily routine.</p>
            <a href="#products" class="btn">Shop Collection</a>
        </div>
    </section>
    
    <!-- Products Section -->
    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title">Our Collection</h2>
            <div class="products-grid">
                <div class="product-card">
                    <img src="https://i.postimg.cc/mDgxM5Cs/IMG_7110.jpg" alt="Aloe Vera and Turmeric Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Aloe Vera & Turmeric</h3>
                        <p class="product-desc">Soothing aloe vera combined with anti-inflammatory turmeric for calm, radiant skin. Perfect for sensitive or irritated skin types.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <img src="https://i.postimg.cc/B6nWDVDm/IMG_7116.jpg" alt="Lavender and Honey Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Lavender & Honey</h3>
                        <p class="product-desc">Calming lavender essential oil paired with moisturizing raw honey. A relaxing blend perfect for evening baths and dry skin.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
                
                <div class="product-card">
                    <img src="https://i.postimg.cc/pTLN868S/IMG_7108.jpg" alt="Bamboo Charcoal and Turmeric Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Bamboo Charcoal & Turmeric</h3>
                        <p class="product-desc">Detoxifying bamboo charcoal combined with brightening turmeric. Deep cleans pores while reducing inflammation and blemishes.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About BusySoaps</h2>
            <div class="about-content">
                <div class="about-img"></div>
                <div class="about-text">
                    <h2>Crafting with Purpose</h2>
                    <p>BusySoaps was born from a passion for creating beautiful, functional products that honor both artistry and simplicity. Each soap is handcrafted with intention, using only natural ingredients that nourish the skin.</p>
                    <p>Our process combines traditional soapmaking techniques with modern design sensibilities. We believe that the products we use daily should be both effective and beautiful, creating moments of mindfulness in everyday routines.</p>
                    <p>From selecting sustainable ingredients to designing each bar's aesthetic, every step is done with care and attention to detail.</p>
                    <a href="#gallery" class="btn">View Our Gallery</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Values Section -->
    <section class="values" id="values">
        <div class="container">
            <h2 class="section-title">Our Values</h2>
            <div class="values-grid">
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3>Natural Ingredients</h3>
                    <p>We use only plant-based oils, butters, and botanicals in our formulations.</p>
                </div>
                
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-hand-rock"></i>
                    </div>
                    <h3>Handcrafted</h3>
                    <p>Every bar is made by hand in small batches for quality and attention to detail.</p>
                </div>
                
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3>Artistic Design</h3>
                    <p>We believe everyday products should be beautiful as well as functional.</p>
                </div>
                
                <div class="value-card">
                    <div class="value-icon">
                        <i class="fas fa-recycle"></i>
                    </div>
                    <h3>Sustainable</h3>
                    <p>Eco-friendly packaging and responsible sourcing are central to our practice.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Slide Gallery Section -->
    <section class="gallery-section" id="gallery">
        <div class="container">
            <h2 class="section-title" style="color: var(--logo-green);">Our Gallery</h2>
            
            <div class="slide-gallery">
                <div class="slides-container" id="slidesContainer">
                    <div class="slide">
                        <img src="https://i.postimg.cc/mDgxM5Cs/IMG_7110.jpg" alt="Aloe Vera and Turmeric Soap Detail" class="slide-img">
                        <div class="slide-caption">Aloe Vera & Turmeric Soap</div>
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/B6nWDVDm/IMG_7116.jpg" alt="Lavender and Honey Soap Detail" class="slide-img">
                        <div class="slide-caption">Lavender & Honey Soap</div>
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/pTLN868S/IMG_7108.jpg" alt="Bamboo Charcoal and Turmeric Soap Detail" class="slide-img">
                        <div class="slide-caption">Bamboo Charcoal & Turmeric Soap</div>
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/DZwVsMsY/IMG_7109.jpg" alt="Soap Making Process" class="slide-img">
                        <div class="slide-caption">The Soap Making Process</div>
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/zDLVLPGC/IMG_7130.jpg" alt="Soap Collection Display" class="slide-img">
                        <div class="slide-caption">Our Soap Collection</div>
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/667y71pV/IMG_7128.jpg" alt="Natural Ingredients" class="slide-img">
                        <div class="slide-caption">Natural Ingredients We Use</div>
                    </div>
                </div>
                
                <div class="gallery-controls">
                    <button class="prev-btn" id="prevBtn">
                        <i class="fas fa-chevron-left"></i>
                    </button>
                    
                    <div class="gallery-dots" id="galleryDots">
                        <!-- Dots will be generated by JavaScript -->
                    </div>
                    
                    <button class="next-btn" id="nextBtn">
                        <i class="fas fa-chevron-right"></i>
                    </button>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <div class="footer-logo">BusySoaps</div>
                    <p>Handcrafted soap creations where natural ingredients meet artistic design.</p>
                    <div class="social-icons">
                        <a href="https://instagram.com/busysoap" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="#" target="_blank"><i class="fab fa-etsy"></i></a>
                        <a href="#" target="_blank"><i class="far fa-envelope"></i></a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#products">Products</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#values">Our Values</a></li>
                        <li><a href="#gallery">Gallery</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Contact</h3>
                    <div class="contact-info">
                        <div><i class="fas fa-map-marker-alt"></i> <span>Mebi Kli Lopera Rd</span></div>
                        <div><i class="far fa-envelope"></i> <span>info@busysoaps.com</span></div>
                        <div><i class="fas fa-phone"></i> <span>(215) 651-3763</span></div>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 BusySoaps. All rights reserved. <span class="highlight">CLEAN</span></p>
            </div>
        </div>
    </footer>
    
    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navMenu = document.getElementById('navMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            navMenu.classList.toggle('active');
            const icon = mobileMenuBtn.querySelector('i');
            if (navMenu.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-times');
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            }
        });
        
        // Close menu when clicking a link
        const navLinks = document.querySelectorAll('nav a');
        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
                const icon = mobileMenuBtn.querySelector('i');
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Slide Gallery Functionality
        const slidesContainer = document.getElementById('slidesContainer');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const galleryDots = document.getElementById('galleryDots');
        
        let currentSlide = 0;
        const totalSlides = document.querySelectorAll('.slide').length;
        
        // Create dots for each slide
        for (let i = 0; i < totalSlides; i++) {
            const dot = document.createElement('div');
            dot.classList.add('dot');
            if (i === 0) dot.classList.add('active');
            dot.addEventListener('click', () => {
                goToSlide(i);
            });
            galleryDots.appendChild(dot);
        }
        
        // Function to go to specific slide
        function goToSlide(slideIndex) {
            if (slideIndex < 0) slideIndex = totalSlides - 1;
            if (slideIndex >= totalSlides) slideIndex = 0;
            
            currentSlide = slideIndex;
            slidesContainer.style.transform = `translateX(-${currentSlide * 100}%)`;
            
            // Update active dot
            document.querySelectorAll('.dot').forEach((dot, index) => {
                if (index === currentSlide) {
                    dot.classList.add('active');
                } else {
                    dot.classList.remove('active');
                }
            });
        }
        
        // Next slide
        nextBtn.addEventListener('click', () => {
            goToSlide(currentSlide + 1);
        });
        
        // Previous slide
        prevBtn.addEventListener('click', () => {
            goToSlide(currentSlide - 1);
        });
        
        // Auto slide every 5 seconds
        let slideInterval = setInterval(() => {
            goToSlide(currentSlide + 1);
        }, 5000);
        
        // Pause auto slide on hover
        const slideGallery = document.querySelector('.slide-gallery');
        slideGallery.addEventListener('mouseenter', () => {
            clearInterval(slideInterval);
        });
        
        slideGallery.addEventListener('mouseleave', () => {
            slideInterval = setInterval(() => {
                goToSlide(currentSlide + 1);
            }, 5000);
        });
        
        // Touch/swipe support for mobile
        let startX = 0;
        let endX = 0;
        
        slideGallery.addEventListener('touchstart', (e) => {
            startX = e.touches[0].clientX;
        });
        
        slideGallery.addEventListener('touchend', (e) => {
            endX = e.changedTouches[0].clientX;
            handleSwipe();
        });
        
        function handleSwipe() {
            const threshold = 50;
            const diff = startX - endX;
            
            if (Math.abs(diff) > threshold) {
                if (diff > 0) {
                    // Swipe left - next slide
                    goToSlide(currentSlide + 1);
                } else {
                    // Swipe right - previous slide
                    goToSlide(currentSlide - 1);
                }
            }
        }
    </script>
</body>
</html>
