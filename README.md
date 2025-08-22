<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Explore the diversity of India - culture, heritage, wildlife, beaches, and more. Discover Incredible India!">
    <link rel="icon" href="https://upload.wikimedia.org/wikipedia/commons/4/41/Flag_of_India.svg" type="image/svg+xml">
    <title>Incredible India | Explore the Diversity</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #030a11;
            color: #f5f5f5; /* changed from #333 for readability */
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, #ff9933 0%, #ffffff 50%, #138808 100%);
            color: #000;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            margin-right: 10px;
            color: #ff9933;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        nav {
            background-color: #120c0c;
            width: 100%;
            border-radius: 5px;
            margin-top: 10px;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: #ffffff; /* changed for contrast */
            font-weight: 600;
            padding: 10px 15px;
            display: block;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            background-color: #138808;
            color: #fff;
            border-radius: 5px;
        }
        
        .container {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1524492412937-b28074a5d7da?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            border-radius: 10px;
            margin-bottom: 40px;
            position: relative;
        }
        
        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            border-radius: 10px;
        }
        
        .hero-content {
            z-index: 1;
            max-width: 800px;
            padding: 20px;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.7);
        }
        
        .btn {
            display: inline-block;
            background: #ff9933;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #e5892b;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #138808;
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: #ff9933;
        }
        
        .regions {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }
        
        .region-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
            color: #333; /* content on white cards */
        }
        
        .region-card:hover {
            transform: translateY(-10px);
        }
        
        .region-img {
            height: 200px;
            overflow: hidden;
        }
        
        .region-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .region-card:hover .region-img img {
            transform: scale(1.1);
        }
        
        .region-content {
            padding: 20px;
        }
        
        .region-content h3 {
            color: #138808;
            margin-bottom: 15px;
        }
        
        .places {
            margin-bottom: 10px;
        }
        
        .places li {
            margin-bottom: 8px;
            list-style-type: none;
            position: relative;
            padding-left: 20px;
        }
        
        .places li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #ff9933;
        }
        
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 50px;
        }
        
        .category {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            color: #333;
        }
        
        .category h3 {
            color: #138808;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #ff9933;
        }
        
        footer {
            background: linear-gradient(135deg, #ff9933 0%, #ffffff 50%, #138808 100%);
            padding: 30px 0;
            text-align: center;
            margin-top: 50px;
            color: #000;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .developer {
            margin-top: 20px;
            font-weight: bold;
            color: #000;
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 5px 0;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero {
                height: 300px; /* smaller on mobile */
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="logo">
                <span class="logo-icon">✈️</span>
                <h1>Incredible India</h1>
            </div>
            <p>Explore the diversity and beauty of India</p>
            <nav>
                <ul>
                    <li><a href="#north">North India</a></li>
                    <li><a href="#south">South India</a></li>
                    <li><a href="#east">East India</a></li>
                    <li><a href="#west">West India</a></li>
                    <li><a href="#central">Central India</a></li>
                    <li><a href="#categories">Categories</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div class="container">
        <div class="hero">
            <div class="hero-content">
                <h2>Discover Incredible India</h2>
                <p>From the majestic Himalayas to the serene backwaters of Kerala, explore the diverse landscapes, cultures, and heritage of India.</p>
                <a href="#explore" class="btn">Explore Destinations</a>
            </div>
        </div>

        <!-- Regions Section -->
        <section id="explore">
            <h2 class="section-title">Explore India by Region</h2>
            <div class="regions">
                <!-- Example Card -->
                <div class="region-card" id="north">
                    <div class="region-img">
                        <img src="https://images.unsplash.com/photo-1524492412937-b28074a5d7da?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Snowy mountains and cultural sites of North India">
                    </div>
                    <div class="region-content">
                        <h3>North India</h3>
                        <ul class="places">
                            <li>Delhi (Red Fort, Qutub Minar)</li>
                            <li>Agra (Taj Mahal, Agra Fort)</li>
                            <li>Jaipur (Hawa Mahal, Amer Fort)</li>
                            <li>Varanasi (Ghats of Ganga, Kashi Vishwanath)</li>
                            <li>Amritsar (Golden Temple)</li>
                            <li>Shimla, Manali, Dharamshala</li>
                            <li>Rishikesh and Haridwar</li>
                            <li>Leh-Ladakh</li>
                        </ul>
                    </div>
                </div>
                <!-- Keep your other region cards unchanged, just update alt attributes similarly -->
            </div>
        </section>

        <!-- Categories Section -->
        <section id="categories">
            <h2 class="section-title">Explore by Category</h2>
            <div class="categories">
                <!-- Example Category -->
                <div class="category">
                    <h3>Historical Sites</h3>
                    <ul class="places">
                        <li>Taj Mahal, Agra</li>
                        <li>Red Fort, Delhi</li>
                        <li>Qutub Minar, Delhi</li>
                        <li>Fatehpur Sikri, UP</li>
                        <li>Hampi, Karnataka</li>
                        <li>Khajuraho, MP</li>
                        <li>Konark Sun Temple, Odisha</li>
                        <li>Amer Fort, Jaipur</li>
                    </ul>
                </div>
                <!-- Keep the rest same -->
            </div>
        </section>
    </div>

    <footer>
        <div class="footer-content">
            <p>&copy; 2023 Incredible India Tourism. All rights reserved.</p>
            <p class="developer">Developed by Navadeep</p>
        </div>
    </footer>
</body>
</html>
