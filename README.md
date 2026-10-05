
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tajiri 3 Inc | Caribbean Bush Teas & Herbal Remedies</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Arial, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: #fcfbf7;
            color: #2d3748;
            line-height: 1.6;
        }

        .container {
            width: 85%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header Navigation */
        header {
            background-color: #1b4332;
            border-bottom: 3px solid #d4af37;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: #ffffff;
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .logo span {
            color: #d4af37;
        }

        nav ul {
            list-style: none;
            display: flex;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            color: #e2e8f0;
            text-decoration: none;
            font-size: 1rem;
            transition: 0.3s;
            font-weight: 500;
        }

        nav ul li a:hover {
            color: #d4af37;
        }

        /* Buttons & Utility */
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: #d4af37;
            color: #1b4332;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            transition: 0.3s ease;
            text-transform: uppercase;
            font-size: 0.9rem;
            border: none;
            cursor: pointer;
            text-align: center;
        }

        .btn:hover {
            background-color: #2d6a4f;
            color: #ffffff;
            transform: translateY(-2px);
        }

        .section-title {
            text-align: center;
            font-size: 2.3rem;
            color: #1b4332;
            margin-bottom: 40px;
            position: relative;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 3px;
            background-color: #d4af37;
            margin: 15px auto 0;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(27, 67, 50, 0.85), rgba(27, 67, 50, 0.85)), 
                        url('https://images.unsplash.com/photo-1576092768241-dec231879fc3?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
            padding: 130px 0;
            color: #ffffff;
            text-align: center;
        }

        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            letter-spacing: 1px;
        }

        .hero p {
            font-size: 1.25rem;
            max-width: 750px;
            margin: 0 auto 30px;
            color: #e2e8f0;
        }

        /* Products Section */
        .products-section {
            padding: 80px 0;
            background-color: #f4f1ea;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .product-card {
            background-color: #ffffff;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
            border-top: 4px solid #1b4332;
            transition: 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            border-top-color: #d4af37;
        }

        .product-card img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .product-card-body {
            padding: 25px;
            flex: 1;
        }

        .product-card h3 {
            font-size: 1.35rem;
            color: #1b4332;
            margin-bottom: 12px;
        }

        .product-card p {
            color: #4a5568;
            font-size: 0.95rem;
        }

        /* Locations Section */
        .locations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .location-card {
            background-color: #fcfbf7;
            border: 1px solid #e2e8f0;
            padding: 30px;
            border-radius: 8px;
            text-align: center;
        }

        .location-card h3 {
            color: #1b4332;
            font-size: 1.4rem;
            margin-bottom: 10px;
        }

        .location-card p a {
            color: #1b4332;
            font-weight: bold;
            text-decoration: none;
            font-size: 1.1rem;
        }

        .location-card p a:hover {
            color: #d4af37;
            text-decoration: underline;
        }

        /* Booking / Order Contact Form */
        .booking-section {
            padding: 80px 0;
            background-color: #ffffff;
        }

        .booking-form {
            max-width: 650px;
            margin: 0 auto;
            background-color: #fcfbf7;
            padding: 40px;
            border-radius: 10px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.02);
        }

        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }

        .form-group label {
            display: block;
            font-size: 0.95rem;
            color: #2d3748;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .form-group input, 
        .form-group select, 
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #cbd5e1;
            border-radius: 5px;
            font-size: 1rem;
            color: #1b4332;
            background-color: #ffffff;
            transition: 0.3s;
        }

        .form-group input:focus, 
        .form-group select:focus, 
        .form-group textarea:focus {
            border-color: #d4af37;
            outline: none;
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }

        /* Footer */
        footer {
            background-color: #1b4332;
            color: #e2e8f0;
            padding: 40px 0 20px;
            text-align: center;
            border-top: 5px solid #d4af37;
        }

        footer p {
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <!-- Header Navigation -->
    <header>
        <div class="container nav-container">
            <div class="logo">TAJIRI 3 <span>BUSH TEA</span></div>
            <nav>
                <ul>
                    <li><a href="#about">Our Teas</a></li>
                    <li><a href="#locations">Locations</a></li>
                    <li><a href="#contact">Order / Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Authentic Caribbean Bush Teas</h1>
            <p>Hand-harvested leaves, plants, and herbs straight from the Caribbean. Experience natural wellness through Soursop, Mango Leaf, Lemongrass, and traditional blends.</p>
            <a href="#contact" class="btn">Order Your Blend</a>
        </div>
    </section>

    <!-- Tea Collection / Products Section -->
    <section id="about" class="products-section">
        <div class="container">
            <h2 class="section-title">Herbal Tea Collection</h2>
            <div class="products-grid">
                
                <!-- Soursop Leaf Tea Card -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1615485290382-441e4d049cb5?auto=format&fit=crop&w=800&q=80" alt="Soursop Leaf Tea Leaves and Fruit">
                    <div class="product-card-body">
                        <h3>Soursop Leaf (Guanabana)</h3>
                        <p>Renowned across the islands for its calming properties and high antioxidant concentration. Brewed from pure, sun-dried wild Soursop leaves.</p>
                    </div>
                </div>

                <!-- Mango Leaf Tea Card -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1553279768-865429fa0078?auto=format&fit=crop&w=800&q=80" alt="Fresh Green Mango Leaves">
                    <div class="product-card-body">
                        <h3>Caribbean Mango Leaf</h3>
                        <p>Rich in vitamins, essential minerals, and polyphenols. Traditionally used in island remedies to balance natural energy and promote vitality.</p>
                    </div>
                </div>

                <!-- Lemongrass Tea Card -->
                <div class="product-card">
                    <img src="https://images.unsplash.com/photo-1597318181409-cf64d0b5d8a2?auto=format&fit=crop&w=800&q=80" alt="Fresh Lemongrass Plant and Herbal Tea">
                    <div class="product-card-body">
                        <h3>Lemongrass (Fever Grass)</h3>
                        <p>A staple in Caribbean households with a crisp citrus aroma. Known for digestive support, refreshing immune boosts, and overall relaxation.</p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Contact & Locations Section -->
    <section id="contact" class="booking-section">
        <div class="container">
            
            <!-- Locations Cards -->
            <div id="locations">
                <h2 class="section-title">Our Physical Locations</h2>
                <div class="locations-grid">
                    <div class="location-card">
                        <h3>New York City</h3>
                        <p>Phone: <a href="tel:3479569055">(347) 956-9055</a></p>
                    </div>
                    <div class="location-card">
                        <h3>Houston</h3>
                        <p>Phone: <a href="tel:8324215566">(832) 421-5566</a></p>
                    </div>
                </div>
            </div>

            <!-- Booking / Order Form -->
            <h2 class="section-title" style="margin-top: 40px;">Order & General Inquiries</h2>
            <form action="https://formspree.io/f/mjykjkqp" method="POST" class="booking-form">
                
                <div class="form-group">
                    <label for="full-name">Full Name</label>
                    <input type="text" id="full-name" name="name" placeholder="John Doe" required>
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" placeholder="john@example.com" required>
                </div>

                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" name="phone" placeholder="(555) 000-0000">
                </div>

                <div class="form-group">
                    <label for="tea-selection">Select Primary Herbal Tea</label>
                    <select id="tea-selection" name="tea_requested" required>
                        <option value="" disabled selected>Select a Bush Tea</option>
                        <option value="Soursop Leaf Tea">Soursop Leaf (Guanabana)</option>
                        <option value="Mango Leaf Tea">Caribbean Mango Leaf</option>
                        <option value="Lemongrass Tea">Lemongrass (Fever Grass)</option>
                        <option value="Variety Sampler Pack">Custom Island Variety Pack</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="message">Your Message or Order Details</label>
                    <textarea id="message" name="message" rows="5" placeholder="Specify quantity, delivery questions, or wholesale inquiries..." required></textarea>
                </div>

                <button type="submit" class="btn" style="width: 100%;">Submit Inquiry</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2026 Tajiri 3 Inc. All Rights Reserved.</p>
        </div>
    </footer>

    <!-- Botpress Webchat Integration & Active Triggers -->
    <script src="https://cdn.botpress.cloud/webchat/v5.0/inject.js"></script>
    <script src="https://files.bpcontent.cloud/2026/10/02/18/20261002184708-NHYAO47K.js"></script>
    <script>
        window.addEventListener('load', function() {
            if (window.botpress) {
                window.botpress.on('webchat:ready', () => {
                    window.botpress.open();
                });
            }
        });
    </script>

</body>
</html>
