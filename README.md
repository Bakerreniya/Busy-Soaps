<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Busy Body Soaps - Handcrafted Soap Art</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            /* VIBRANT, ENERGETIC COLOR SCHEME */
            --primary: #FF2E63;       /* Energetic Pink/Red */
            --secondary: #08D9D6;     /* Electric Teal */
            --accent: #FFA500;        /* Vibrant Orange */
            --highlight: #AA00FF;     /* Electric Purple */
            --dark: #252A34;          /* Dark Blue/Black */
            --light: #F5F5F5;         /* Off-white */
            --background: #0A0E17;    /* Deep Dark Blue */
            --card-bg: #1A1F2C;       /* Dark Card Background */
            --transition: all 0.3s ease;
            --glow: 0 0 15px currentColor;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--background);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
            font-size: 16px;
        }
        
        h1, h2, h3, h4, .logo-text, .section-title {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            color: var(--secondary);
            text-shadow: 0 0 10px rgba(8, 217, 214, 0.3);
            letter-spacing: -0.5px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            width: 100%;
        }
        
        /* Header & Navigation */
        header {
            background-color: var(--dark);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 3px solid var(--primary);
            box-shadow: 0 5px 25px rgba(255, 46, 99, 0.3);
            backdrop-filter: blur(10px);
            background-color: rgba(37, 42, 52, 0.95);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .logo-text {
            font-size: 24px;
            font-weight: 800;
            background: linear-gradient(45deg, var(--primary), var(--accent), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: logoGlow 2s ease-in-out infinite alternate;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        @keyframes logoGlow {
            from { 
                text-shadow: 0 0 5px var(--primary), 0 0 10px rgba(255, 46, 99, 0.3); 
            }
            to { 
                text-shadow: 0 0 15px var(--primary), 0 0 25px rgba(255, 46, 99, 0.5), 0 0 35px rgba(255, 46, 99, 0.2); 
            }
        }
        
        .logo-subtitle {
            font-family: 'Poppins', sans-serif;
            font-size: 12px;
            color: var(--secondary);
            font-weight: 500;
            margin-top: -2px;
            letter-spacing: 1px;
            text-transform: uppercase;
            display: none; /* Hidden on mobile, will show on larger screens */
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }
        
        nav a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 14px;
            transition: var(--transition);
            padding: 5px 0;
            position: relative;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-family: 'Montserrat', sans-serif;
        }
        
        nav a:hover {
            color: var(--primary);
            transform: translateY(-2px);
        }
        
        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            bottom: 0;
            left: 0;
            transition: var(--transition);
            box-shadow: var(--glow);
        }
        
        nav a:hover::after {
            width: 100%;
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: 2px solid var(--primary);
            color: var(--primary);
            font-size: 20px;
            cursor: pointer;
            padding: 8px 12px;
            border-radius: 4px;
            transition: var(--transition);
            z-index: 1001;
        }
        
        .mobile-menu-btn:hover {
            background-color: var(--primary);
            color: var(--dark);
            box-shadow: var(--glow);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--dark) 0%, var(--background) 100%);
            color: var(--light);
            padding: 60px 0;
            text-align: center;
            border-bottom: 3px solid var(--primary);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 30% 50%, rgba(255, 46, 99, 0.15) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .hero h1 {
            font-size: 36px;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: titlePulse 3s ease-in-out infinite;
            font-weight: 800;
            line-height: 1.2;
            padding: 0 10px;
        }
        
        @keyframes titlePulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }
        
        .hero p {
            font-size: 16px;
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--light);
            text-shadow: 0 2px 10px rgba(0,0,0,0.5);
            font-weight: 300;
            line-height: 1.8;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: var(--light);
            padding: 14px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 15px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            position: relative;
            overflow: hidden;
            z-index: 1;
            box-shadow: 0 5px 20px rgba(255, 46, 99, 0.4);
            font-family: 'Montserrat', sans-serif;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--secondary), var(--highlight));
            transition: var(--transition);
            z-index: -1;
        }
        
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(255, 46, 99, 0.6);
            letter-spacing: 2px;
        }
        
        .btn:hover::before {
            left: 0;
        }
        
        .btn-outline {
            display: inline-block;
            background-color: transparent;
            color: var(--primary);
            padding: 12px 24px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 13px;
            transition: var(--transition);
            border: 2px solid var(--primary);
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            position: relative;
            overflow: hidden;
            font-family: 'Montserrat', sans-serif;
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: var(--dark);
            transform: translateY(-3px);
            box-shadow: var(--glow);
            letter-spacing: 2px;
        }
        
        /* Products Section */
        .section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 32px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            box-shadow: var(--glow);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 25px;
            margin-bottom: 60px;
        }
        
        .product-card {
            background-color: var(--card-bg);
            border-radius: 15px;
            overflow: hidden;
            border: 2px solid transparent;
            background-clip: padding-box;
            transition: var(--transition);
            position: relative;
            max-width: 400px;
            margin: 0 auto;
            width: 100%;
        }
        
        .product-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent), var(--highlight));
            z-index: -1;
            border-radius: 17px;
            opacity: 0;
            transition: var(--transition);
        }
        
        .product-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }
        
        .product-card:hover::before {
            opacity: 1;
            animation: borderRotate 3s linear infinite;
        }
        
        @keyframes borderRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .product-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-bottom: 2px solid var(--primary);
            transition: var(--transition);
        }
        
        .product-card:hover .product-img {
            transform: scale(1.05);
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-name {
            font-size: 20px;
            margin-bottom: 10px;
            color: var(--secondary);
            text-shadow: 0 0 10px rgba(8, 217, 214, 0.3);
            font-weight: 700;
        }
        
        .product-desc {
            color: var(--light);
            margin-bottom: 20px;
            opacity: 0.9;
            font-weight: 300;
            line-height: 1.7;
            font-size: 15px;
        }
        
        /* About Section */
        .about {
            background: linear-gradient(135deg, var(--card-bg) 0%, var(--background) 100%);
            padding: 60px 0;
            border-top: 3px solid var(--secondary);
            border-bottom: 3px solid var(--accent);
            position: relative;
            overflow: hidden;
        }
        
        .about::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(170, 0, 255, 0.1) 0%, transparent 70%);
            pointer-events: none;
        }
        
        .about-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 40px;
            position: relative;
            z-index: 1;
        }
        
        .about-img {
            width: 100%;
            height: 300px;
            background-image: url('https://i.postimg.cc/LX8dfbLS/IMG_7106.jpg');
            background-size: cover;
            background-position: center;
            border: 3px solid transparent;
            border-radius: 10px;
            background-clip: padding-box;
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
            max-width: 500px;
        }
        
        .about-img::before {
            content: '';
            position: absolute;
            top: -3px;
            left: -3px;
            right: -3px;
            bottom: -3px;
            background: linear-gradient(45deg, var(--primary), var(--accent), var(--highlight));
            z-index: -1;
            border-radius: 13px;
            animation: borderRotate 4s linear infinite;
        }
        
        .about-text {
            width: 100%;
            max-width: 600px;
        }
        
        .about-text h2 {
            margin-bottom: 20px;
            font-size: 28px;
            color: var(--primary);
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 800;
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: var(--light);
            font-weight: 300;
            line-height: 1.8;
            font-size: 15px;
        }
        
        /* Slide Gallery Section */
        .gallery-section {
            padding: 60px 0;
            background: linear-gradient(135deg, var(--dark) 0%, var(--background) 100%);
            position: relative;
            overflow: hidden;
        }
        
        .gallery-section::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 100px;
            background: linear-gradient(to top, var(--background), transparent);
            pointer-events: none;
        }
        
        .slide-gallery {
            position: relative;
            width: 100%;
            margin: 30px auto 0;
            overflow: hidden;
            border: 3px solid transparent;
            border-radius: 15px;
            background-clip: padding-box;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.6);
        }
        
        .slide-gallery::before {
            content: '';
            position: absolute;
            top: -3px;
            left: -3px;
            right: -3px;
            bottom: -3px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            z-index: -1;
            border-radius: 18px;
            opacity: 0.7;
        }
        
        .slides-container {
            display: flex;
            transition: transform 0.5s ease;
        }
        
        .slide {
            min-width: 100%;
            height: 300px;
            position: relative;
        }
        
        .slide-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .slide:hover .slide-img {
            transform: scale(1.05);
        }
        
        .slide-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(37, 42, 52, 0.95), rgba(255, 46, 99, 0.8));
            color: var(--light);
            padding: 12px;
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 16px;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-shadow: 0 2px 5px rgba(0,0,0,0.5);
            font-weight: 600;
        }
        
        .gallery-controls {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            gap: 15px;
        }
        
        .prev-btn, .next-btn {
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: var(--light);
            border: none;
            width: 45px;
            height: 45px;
            cursor: pointer;
            transition: var(--transition);
            font-size: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            box-shadow: 0 5px 15px rgba(255, 46, 99, 0.4);
        }
        
        .prev-btn:hover, .next-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 20px rgba(255, 46, 99, 0.6);
        }
        
        .gallery-dots {
            display: flex;
            gap: 10px;
        }
        
        .dot {
            width: 12px;
            height: 12px;
            background-color: var(--card-bg);
            border-radius: 50%;
            cursor: pointer;
            transition: var(--transition);
            border: 2px solid var(--secondary);
        }
        
        .dot.active {
            background-color: var(--primary);
            transform: scale(1.2);
            box-shadow: 0 0 10px var(--primary);
        }
        
        .dot:hover {
            background-color: var(--accent);
        }
        
        /* Values Section */
        .values {
            padding: 60px 0;
            background: var(--background);
            position: relative;
            overflow: hidden;
        }
        
        .values::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 100%;
            background: radial-gradient(circle at 70% 30%, rgba(8, 217, 214, 0.1) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .values-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 25px;
            margin-top: 30px;
            position: relative;
            z-index: 1;
        }
        
        .value-card {
            text-align: center;
            padding: 25px 20px;
            border: 2px solid transparent;
            background: linear-gradient(135deg, var(--card-bg) 0%, rgba(37, 42, 52, 0.8) 100%);
            border-radius: 15px;
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            max-width: 400px;
            margin: 0 auto;
            width: 100%;
        }
        
        .value-card::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            z-index: -1;
            border-radius: 17px;
            opacity: 0;
            transition: var(--transition);
        }
        
        .value-card:hover {
            transform: translateY(-8px) scale(1.03);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5);
        }
        
        .value-card:hover::before {
            opacity: 1;
        }
        
        .value-icon {
            font-size: 40px;
            margin-bottom: 15px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 5px 15px rgba(255, 46, 99, 0.4));
        }
        
        .value-card h3 {
            margin-bottom: 15px;
            font-size: 20px;
            color: var(--secondary);
            text-shadow: 0 0 10px rgba(8, 217, 214, 0.3);
            font-weight: 700;
        }
        
        .value-card p {
            color: var(--light);
            font-weight: 300;
            line-height: 1.7;
            font-size: 15px;
        }
        
        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--dark) 0%, var(--background) 100%);
            color: var(--light);
            padding: 50px 0 20px;
            border-top: 3px solid var(--primary);
            position: relative;
            overflow: hidden;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 100%;
            background: radial-gradient(circle at 20% 80%, rgba(255, 46, 99, 0.1) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }
        
        .footer-section {
            width: 100%;
            max-width: 400px;
            margin: 0 auto;
        }
        
        .footer-logo {
            font-size: 24px;
            font-weight: 800;
            margin-bottom: 15px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 15px rgba(255, 46, 99, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .footer-section h3 {
            font-size: 18px;
            margin-bottom: 20px;
            color: var(--secondary);
            position: relative;
            padding-bottom: 8px;
            font-weight: 700;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            bottom: 0;
            left: 0;
            box-shadow: 0 0 10px var(--primary);
        }
        
        .footer-section p {
            margin-bottom: 15px;
            opacity: 0.9;
            font-weight: 300;
            font-size: 15px;
        }
        
        .social-icons {
            display: flex;
            gap: 12px;
            margin-top: 15px;
        }
        
        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            border-radius: 50%;
            color: var(--dark);
            font-size: 18px;
            transition: var(--transition);
            border: 2px solid transparent;
        }
        
        .social-icons a:hover {
            transform: translateY(-5px) rotate(15deg);
            box-shadow: 0 10px 20px rgba(255, 46, 99, 0.5);
            border-color: var(--light);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: var(--light);
            text-decoration: none;
            transition: var(--transition);
            opacity: 0.9;
            display: inline-block;
            padding: 3px 0;
            font-weight: 300;
            font-size: 15px;
        }
        
        .footer-links a:hover {
            opacity: 1;
            padding-left: 8px;
            color: var(--primary);
            transform: translateX(5px);
            font-weight: 500;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .contact-info div {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            font-size: 15px;
        }
        
        .contact-info i {
            width: 20px;
            color: var(--primary);
            margin-top: 3px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 13px;
            opacity: 0.8;
            position: relative;
            z-index: 1;
            font-weight: 300;
        }
        
        .highlight {
            color: var(--primary);
            font-weight: 700;
            text-shadow: 0 0 10px rgba(255, 46, 99, 0.5);
        }
        
        /* Tablet Styles (768px and up) */
        @media (min-width: 768px) {
            .logo-text {
                font-size: 28px;
            }
            
            .logo-subtitle {
                display: block;
                font-size: 12px;
            }
            
            .hero {
                padding: 80px 0;
            }
            
            .hero h1 {
                font-size: 42px;
            }
            
            .hero p {
                font-size: 17px;
            }
            
            .section-title {
                font-size: 36px;
                margin: 70px 0 50px;
            }
            
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 30px;
                margin-bottom: 70px;
            }
            
            .about-content {
                flex-direction: row;
                gap: 40px;
            }
            
            .about-img {
                height: 350px;
            }
            
            .about-text h2 {
                font-size: 32px;
            }
            
            .slide {
                height: 400px;
            }
            
            .values-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 30px;
            }
            
            .footer-content {
                flex-direction: row;
                flex-wrap: wrap;
                justify-content: space-between;
                gap: 40px;
            }
            
            .footer-section {
                flex: 1;
                min-width: 250px;
                margin: 0;
            }
        }
        
        /* Desktop Styles (1024px and up) */
        @media (min-width: 1024px) {
            .logo-text {
                font-size: 32px;
            }
            
            .logo-subtitle {
                font-size: 14px;
            }
            
            nav a {
                font-size: 16px;
                gap: 25px;
            }
            
            .hero {
                padding: 100px 0;
            }
            
            .hero h1 {
                font-size: 52px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .btn {
                padding: 16px 36px;
                font-size: 16px;
            }
            
            .btn-outline {
                padding: 14px 32px;
                font-size: 14px;
            }
            
            .section-title {
                font-size: 42px;
                margin: 80px 0 50px;
            }
            
            .products-grid {
                grid-template-columns: repeat(3, 1fr);
                gap: 30px;
                margin-bottom: 80px;
            }
            
            .product-card {
                max-width: none;
            }
            
            .product-img {
                height: 280px;
            }
            
            .about {
                padding: 80px 0;
            }
            
            .about-content {
                gap: 50px;
            }
            
            .about-img {
                height: 400px;
            }
            
            .about-text h2 {
                font-size: 36px;
            }
            
            .gallery-section {
                padding: 80px 0;
            }
            
            .slide {
                height: 500px;
            }
            
            .slide-gallery {
                max-width: 900px;
            }
            
            .values {
                padding: 80px 0;
            }
            
            .values-grid {
                grid-template-columns: repeat(4, 1fr);
                gap: 30px;
                margin-top: 40px;
            }
            
            .value-card {
                padding: 30px;
            }
            
            footer {
                padding: 70px 0 25px;
            }
            
            .footer-logo {
                font-size: 28px;
            }
            
            .footer-section h3 {
                font-size: 20px;
            }
        }
        
        /* Mobile Navigation Styles */
        @media (max-width: 767px) {
            nav ul {
                display: none;
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100vh;
                background-color: rgba(37, 42, 52, 0.98);
                flex-direction: column;
                padding: 80px 20px 40px;
                text-align: center;
                z-index: 999;
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
                backdrop-filter: blur(15px);
                overflow-y: auto;
            }
            
            nav ul.active {
                display: flex;
            }
            
            nav ul li {
                margin-bottom: 20px;
            }
            
            nav a {
                font-size: 18px;
                padding: 10px 0;
            }
            
            .mobile-menu-btn {
                display: flex;
                align-items: center;
                justify-content: center;
            }
            
            .header-container {
                position: relative;
            }
            
            /* Close button styles for mobile menu */
            .nav-close-btn {
                position: absolute;
                top: 20px;
                right: 20px;
                background: none;
                border: 2px solid var(--primary);
                color: var(--primary);
                font-size: 24px;
                cursor: pointer;
                padding: 5px 10px;
                border-radius: 4px;
                transition: var(--transition);
                display: none;
            }
            
            .nav-close-btn:hover {
                background-color: var(--primary);
                color: var(--dark);
                box-shadow: var(--glow);
            }
            
            nav ul.active ~ .nav-close-btn {
                display: block;
            }
        }
        
        /* Small mobile devices (max-width: 480px) */
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 30px;
            }
            
            .hero p {
                font-size: 15px;
                padding: 0 10px;
            }
            
            .btn {
                padding: 12px 24px;
                font-size: 14px;
            }
            
            .btn-outline {
                padding: 10px 20px;
                font-size: 12px;
            }
            
            .section-title {
                font-size: 28px;
                margin: 50px 0 30px;
            }
            
            .product-img {
                height: 220px;
            }
            
            .product-name {
                font-size: 18px;
            }
            
            .product-desc {
                font-size: 14px;
            }
            
            .about-img {
                height: 250px;
            }
            
            .about-text h2 {
                font-size: 24px;
            }
            
            .about-text p {
                font-size: 14px;
            }
            
            .slide {
                height: 250px;
            }
            
            .slide-caption {
                font-size: 14px;
                padding: 10px;
            }
            
            .value-card h3 {
                font-size: 18px;
            }
            
            .value-card p {
                font-size: 14px;
            }
            
            .footer-logo {
                font-size: 22px;
            }
            
            .social-icons a {
                width: 38px;
                height: 38px;
                font-size: 16px;
            }
            
            .contact-info div {
                font-size: 14px;
            }
        }
        
        /* Prevent horizontal scrolling on mobile */
        html, body {
            max-width: 100%;
            overflow-x: hidden;
        }
        
        /* Improve touch targets for mobile */
        .btn, .btn-outline, .prev-btn, .next-btn, .mobile-menu-btn, .social-icons a {
            min-height: 44px;
            min-width: 44px;
        }
        
        /* Improve text readability on mobile */
        p, li, a, span {
            line-height: 1.6;
        }
        
        /* Better spacing for mobile */
        section {
            padding-left: 15px;
            padding-right: 15px;
        }
        
        .container {
            padding-left: 15px;
            padding-right: 15px;
        }
    </style>
</head>
<body>
    <!-- Header with Logo -->
    <header>
        <div class="container header-container">
            <div class="logo-container">
                <div>
                    <div class="logo-text">BUSY BODY SOAPS</div>
                    <div class="logo-subtitle">HANDCRAFTED WITH CARE</div>
                </div>
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
            <h2 class="section-title">About Busy Body Soaps</h2>
            <div class="about-content">
                <div class="about-img"></div>
                <div class="about-text">
                    <h2>Crafting with Purpose</h2>
                    <p>Busy Body Soaps was born from a passion for creating beautiful, functional products that honor both artistry and simplicity. Each soap is handcrafted with intention, using only natural ingredients that nourish the skin.</p>
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
            <h2 class="section-title" style="color: var(--secondary);">Our Gallery</h2>
            
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
                    <div class="footer-logo">BUSY BODY SOAPS</div>
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
                        <div><i class="fas fa-phone"></i> <span>(215) 651-3763</span></div>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Busy Body Soaps. All rights reserved. <span class="highlight">CLEAN</span></p>
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
                document.body.style.overflow = 'hidden'; // Prevent scrolling when menu is open
            } else {
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
                document.body.style.overflow = 'auto'; // Restore scrolling
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
                document.body.style.overflow = 'auto'; // Restore scrolling
            });
        });
        
        // Close menu when clicking outside
        document.addEventListener('click', (e) => {
            if (navMenu.classList.contains('active') && 
                !navMenu.contains(e.target) && 
                !mobileMenuBtn.contains(e.target)) {
                navMenu.classList.remove('active');
                const icon = mobileMenuBtn.querySelector('i');
                icon.classList.remove('fa-times');
                icon.classList.add('fa-bars');
                document.body.style.overflow = 'auto'; // Restore scrolling
            }
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
        let isSwiping = false;
        
        slideGallery.addEventListener('touchstart', (e) => {
            startX = e.touches[0].clientX;
            isSwiping = true;
        });
        
        slideGallery.addEventListener('touchmove', (e) => {
            if (isSwiping) {
                endX = e.touches[0].clientX;
            }
        });
        
        slideGallery.addEventListener('touchend', () => {
            if (isSwiping) {
                handleSwipe();
                isSwiping = false;
            }
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
        
        // Adjust slide height on window resize
        function adjustSlideHeight() {
            const slides = document.querySelectorAll('.slide');
            const windowWidth = window.innerWidth;
            
            if (windowWidth < 768) {
                slides.forEach(slide => {
                    slide.style.height = '250px';
                });
            } else if (windowWidth < 1024) {
                slides.forEach(slide => {
                    slide.style.height = '400px';
                });
            } else {
                slides.forEach(slide => {
                    slide.style.height = '500px';
                });
            }
        }
        
        // Initial adjustment
        adjustSlideHeight();
        
        // Adjust on window resize
        window.addEventListener('resize', adjustSlideHeight);
        
        // Prevent zoom on double-tap on mobile
        let lastTouchEnd = 0;
        document.addEventListener('touchend', function(event) {
            const now = (new Date()).getTime();
            if (now - lastTouchEnd <= 300) {
                event.preventDefault();
            }
            lastTouchEnd = now;
        }, false);
    </script>
</body>
</html>
