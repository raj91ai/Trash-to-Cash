# Trash-to-Cash
Website 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TRASH TO CASH - Plastic Recycling Business</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            background-color: #ffffff;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            color: #2e7d32;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            color: #ff9800;
        }
        
        .logo span {
            color: #ff9800;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 25px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        .nav-links a:hover {
            color: #2e7d32;
            background-color: #f0f9f0;
        }
        
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #2e7d32;
        }
        
        /* Hero Section */
        .hero {
            padding: 160px 0 100px;
            background: linear-gradient(rgba(46, 125, 50, 0.9), rgba(76, 175, 80, 0.9));
            color: white;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 20px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
        }
        
        .hero-tagline {
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: #ffeb3b;
        }
        
        .hero p {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto 30px;
            opacity: 0.95;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff9800;
            color: white;
            padding: 14px 35px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            box-shadow: 0 4px 10px rgba(255, 152, 0, 0.3);
        }
        
        .btn:hover {
            background-color: #f57c00;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
        }
        
        .btn-secondary {
            background-color: transparent;
            border: 2px solid white;
            margin-left: 15px;
        }
        
        .btn-secondary:hover {
            background-color: rgba(255, 255, 255, 0.15);
        }
        
        /* Sections */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #2e7d32;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2:after {
            content: '';
            position: absolute;
            width: 70px;
            height: 4px;
            background-color: #ff9800;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }
        
        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 25px auto 0;
            font-size: 1.1rem;
        }
        
        /* Business Model Section */
        .business-model {
            background-color: #f0f9f0;
        }
        
        .model-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }
        
        .model-card {
            background-color: white;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            border-top: 5px solid #2e7d32;
            transition: transform 0.3s;
        }
        
        .model-card:hover {
            transform: translateY(-10px);
        }
        
        .model-card h3 {
            color: #2e7d32;
            margin-bottom: 20px;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .model-card h3 i {
            color: #ff9800;
        }
        
        /* Process Section */
        .process-steps {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 40px;
        }
        
        .process-step {
            flex: 1;
            min-width: 250px;
            text-align: center;
            padding: 30px 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }
        
        .step-number {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 45px;
            height: 45px;
            background-color: #2e7d32;
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.2rem;
            box-shadow: 0 3px 10px rgba(46, 125, 50, 0.3);
        }
        
        .step-icon {
            font-size: 2.5rem;
            color: #2e7d32;
            margin-bottom: 20px;
        }
        
        /* Financials Section */
        .financials {
            background-color: #f5f5f5;
        }
        
        .pricing-table {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .price-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .price-header {
            background-color: #2e7d32;
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        .price-header h4 {
            font-size: 1.3rem;
            margin-bottom: 5px;
        }
        
        .price-body {
            padding: 25px;
        }
        
        .price-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px dashed #eee;
        }
        
        .price-item:last-child {
            border-bottom: none;
        }
        
        /* Products Section */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-8px);
        }
        
        .product-img {
            height: 200px;
            background-color: #e8f5e9;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: #2e7d32;
        }
        
        .product-content {
            padding: 25px;
        }
        
        .product-content h4 {
            color: #2e7d32;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        /* Footer */
        footer {
            background-color: #1b5e20;
            color: white;
            padding: 70px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: #fff;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 40px;
            height: 3px;
            background-color: #ff9800;
            bottom: 0;
            left: 0;
        }
        
        .footer-column p, .footer-column a {
            color: #ddd;
            margin-bottom: 12px;
            display: block;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column a:hover {
            color: #ff9800;
            padding-left: 5px;
        }
        
        .contact-info i {
            width: 20px;
            margin-right: 10px;
            color: #ff9800;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #2e7d32;
            border-radius: 50%;
            color: white;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: #ff9800;
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #2e7d32;
            color: #ddd;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.6rem;
            }
            
            .process-steps {
                justify-content: center;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                padding-top: 50px;
                transition: left 0.3s;
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero-tagline {
                font-size: 1.2rem;
            }
            
            .btn-container {
                display: flex;
                flex-direction: column;
                gap: 15px;
                align-items: center;
            }
            
            .btn-secondary {
                margin-left: 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero {
                padding: 140px 0 80px;
            }
            
            .model-grid, .products-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">
                    <i class="fas fa-recycle"></i>
                    TRASH <span>TO CASH</span>
                </a>
                <div class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#business">Business Model</a></li>
                    <li><a href="#process">Process</a></li>
                    <li><a href="#financials">Financials</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#contact" class="btn">Partner With Us</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-tagline">From Trash to Cash: Building Startups with Waste</div>
            <h1>The Business of Waste: Turning Problems into Profits</h1>
            <p>We're transforming plastic waste into valuable resources, products, and sustainable profit. Waste management is not just about disposal – it's about creating economic value while saving our planet.</p>
            <div class="btn-container">
                <a href="#business" class="btn">Explore Our Business Model</a>
                <a href="#contact" class="btn btn-secondary">Join the Revolution</a>
            </div>
        </div>
    </section>

    <!-- Business Model Section -->
    <section class="section business-model" id="business">
        <div class="container">
            <div class="section-title">
                <h2>Our Business Model</h2>
                <p>Transforming waste management into a profitable, sustainable enterprise</p>
            </div>
            <div class="model-grid">
                <div class="model-card">
                    <h3><i class="fas fa-shopping-cart"></i> Initial Collection Plan</h3>
                    <p>We purchase plastic waste from existing waste collectors and businesses dealing in plastic waste materials. This creates an additional revenue stream for local waste collectors while ensuring a steady supply for our operations.</p>
                    <p><strong>Sources:</strong> Individual collectors, scrap dealers, community collection centers</p>
                </div>
                
                <div class="model-card">
                    <h3><i class="fas fa-trash-alt"></i> Types of Waste</h3>
                    <p><strong>Initial Focus (Phase 1):</strong></p>
                    <ul style="padding-left: 20px; margin-top: 10px;">
                        <li><strong>Non-biodegradable:</strong> Plastic, Metals, Glass</li>
                        <li><strong>Plastic Types:</strong> PET bottles, HDPE, LDPE, Single-use plastics</li>
                    </ul>
                    <p style="margin-top: 15px;"><strong>Future Expansion (Phase 2):</strong></p>
                    <ul style="padding-left: 20px;">
                        <li>Biodegradable waste (food, garden waste)</li>
                        <li>E-waste</li>
                        <li>Lithium batteries</li>
                        <li>Plastic to fuel conversion</li>
                    </ul>
                </div>
                
                <div class="model-card">
                    <h3><i class="fas fa-handshake"></i> Growth Strategy</h3>
                    <p>Starting with purchased sorted waste, then expanding to direct collection partnerships with municipal bodies (Nagar Panchayat and Nagar Nigam). As we grow, we'll implement more sophisticated sorting systems.</p>
                    <p><strong>Key Partnerships:</strong> Municipal corporations, Waste collector networks, Environmental agencies</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Process Section -->
    <section class="section" id="process">
        <div class="container">
            <div class="section-title">
                <h2>Our Recycling Process</h2>
                <p>From waste collection to finished products - a streamlined 4-step process</p>
            </div>
            
            <div class="process-steps">
                <div class="process-step">
                    <div class="step-number">1</div>
                    <div class="step-icon">
                        <i class="fas fa-sort"></i>
                    </div>
                    <h3>Sorting</h3>
                    <p>Initial purchase of pre-sorted plastic. As we grow, we'll implement our own sorting system starting with manual sorting (cost-effective) and eventually moving to AI-based sorting for efficiency.</p>
                    <p><strong>Method:</strong> Human sorting initially (cheap and effective)</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">2</div>
                    <div class="step-icon">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h3>Shredding</h3>
                    <p>Using industrial shredding machines to break down plastic into small pieces. Our machine processes 200kg/hour, is fully electric, and handles all types of plastic waste.</p>
                    <p><strong>Machine Cost:</strong> ₹50,000</p>
                    <p><strong>Capacity:</strong> 200kg/hour</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">3</div>
                    <div class="step-icon">
                        <i class="fas fa-shower"></i>
                    </div>
                    <h3>Washing</h3>
                    <p>Innovative washing system created with drums and motors to clean shredded plastic, removing contaminants and preparing material for melting.</p>
                    <p><strong>Setup Cost:</strong> ₹15,000 - ₹20,000</p>
                    <p><strong>Innovation:</strong> Custom-built system</p>
                </div>
                
                <div class="process-step">
                    <div class="step-number">4</div>
                    <div class="step-icon">
                        <i class="fas fa-fire"></i>
                    </div>
                    <h3>Melting & Molding</h3>
                    <p>Transforming cleaned plastic shreds into new products through melting and molding processes. Creating eco-bricks, crates, and various plastic products.</p>
                    <p><strong>Output:</strong> 2.4 - 3.5 tons per day</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Financials Section -->
    <section class="section financials" id="financials">
        <div class="container">
            <div class="section-title">
                <h2>Financial Breakdown</h2>
                <p>Transparent pricing and profitable production models</p>
            </div>
            
            <h3 style="text-align: center; margin-bottom: 30px; color: #2e7d32;">Purchase Rates (Per KG)</h3>
            <div class="pricing-table">
                <div class="price-card">
                    <div class="price-header">
                        <h4>Transparent Plastic Bottles</h4>
                    </div>
                    <div class="price-body">
                        <div class="price-item">
                            <span>Purchase Rate</span>
                            <span>₹20 - ₹25/kg</span>
                        </div>
                        <div class="price-item">
                            <span>Quality</span>
                            <span>High-grade PET</span>
                        </div>
                        <div class="price-item">
                            <span>Best For</span>
                            <span>Clear products</span>
                        </div>
                    </div>
                </div>
                
                <div class="price-card">
                    <div class="price-header">
                        <h4>Mixed Plastic Items</h4>
                    </div>
                    <div class="price-body">
                        <div class="price-item">
                            <span>Purchase Rate</span>
                            <span>₹10 - ₹15/kg</span>
                        </div>
                        <div class="price-item">
                            <span>Quality</span>
                            <span>Mixed plastics</span>
                        </div>
                        <div class="price-item">
                            <span>Best For</span>
                            <span>Colored products</span>
                        </div>
                    </div>
                </div>
                
                <div class="price-card">
                    <div class="price-header">
                        <h4>Single-Use Plastics</h4>
                    </div>
                    <div class="price-body">
                        <div class="price-item">
                            <span>Plastic Bags</span>
                            <span>₹2 - ₹5/kg</span>
                        </div>
                        <div class="price-item">
                            <span>Wafer Packets</span>
                            <span>₹8 - ₹10/kg</span>
                        </div>
                        <div class="price-item">
                            <span>Best For</span>
                            <span>Bricks & Crates</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <h3 style="text-align: center; margin: 50px 0 30px; color: #2e7d32;">Production & Profit Analysis</h3>
            
            <div class="model-grid">
                <div class="model-card">
                    <h3><i class="fas fa-cube"></i> Plastic Bricks</h3>
                    <div class="price-item">
                        <span>Raw Material (Single-use bags)</span>
                        <span>₹3/kg</span>
                    </div>
                    <div class="price-item">
                        <span>Daily Consumption</span>
                        <span>3000 kg</span>
                    </div>
                    <div class="price-item">
                        <span>Material Cost</span>
                        <span>₹9,000</span>
                    </div>
                    <div class="price-item">
                        <span>Labour Cost</span>
                        <span>₹2,500</span>
                    </div>
                    <div class="price-item">
                        <span>Electricity Cost</span>
                        <span>₹2,000</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; border-top: 2px solid #2e7d32;">
                        <span>Total Cost</span>
                        <span>₹13,500</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; color: #2e7d32;">
                        <span>Daily Production</span>
                        <span>10,000 bricks</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; color: #2e7d32;">
                        <span>Selling Price (₹5/brick)</span>
                        <span>₹50,000</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; background-color: #e8f5e9; padding: 15px; margin-top: 10px; border-radius: 5px;">
                        <span>DAILY PROFIT</span>
                        <span>₹36,500</span>
                    </div>
                </div>
                
                <div class="model-card">
                    <h3><i class="fas fa-pallet"></i> Plastic Crates</h3>
                    <div class="price-item">
                        <span>Raw Material (Single-use bags)</span>
                        <span>₹3/kg</span>
                    </div>
                    <div class="price-item">
                        <span>Daily Consumption</span>
                        <span>3000 kg</span>
                    </div>
                    <div class="price-item">
                        <span>Material Cost</span>
                        <span>₹9,000</span>
                    </div>
                    <div class="price-item">
                        <span>Labour Cost</span>
                        <span>₹2,500</span>
                    </div>
                    <div class="price-item">
                        <span>Electricity Cost</span>
                        <span>₹2,000</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; border-top: 2px solid #2e7d32;">
                        <span>Total Cost</span>
                        <span>₹13,500</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; color: #2e7d32;">
                        <span>Daily Production</span>
                        <span>5,000 crates</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; color: #2e7d32;">
                        <span>Selling Price (₹25/crate)</span>
                        <span>₹125,000</span>
                    </div>
                    <div class="price-item" style="font-weight: bold; background-color: #e8f5e9; padding: 15px; margin-top: 10px; border-radius: 5px;">
                        <span>DAILY PROFIT</span>
                        <span>₹111,500</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="section" id="products">
        <div class="container">
            <div class="section-title">
                <h2>Our Products</h2>
                <p>Transforming plastic waste into valuable, market-ready products</p>
            </div>
            
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-cube"></i>
                    </div>
                    <div class="product-content">
                        <h4>Plastic Eco-Bricks</h4>
                        <p>Strong, durable building bricks made from single-use plastic bags. Each brick weighs 300g and serves as an eco-friendly alternative to traditional bricks.</p>
                        <p><strong>Price:</strong> ₹5 per brick</p>
                        <p><strong>Daily Production:</strong> 10,000 units</p>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-pallet"></i>
                    </div>
                    <div class="product-content">
                        <h4>Plastic Crates</h4>
                        <p>Sturdy storage crates (400g each) perfect for agriculture, storage, and transportation. Made entirely from recycled plastic.</p>
                        <p><strong>Price:</strong> ₹25 per crate</p>
                        <p><strong>Daily Production:</strong> 5,000 units</p>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-chair"></i>
                    </div>
                    <div class="product-content">
                        <h4>Furniture Items</h4>
                        <p>Outdoor furniture, tables, chairs, and benches made from recycled plastic. Weather-resistant and durable for long-term use.</p>
                        <p><strong>Range:</strong> ₹500 - ₹5,000</p>
                        <p><strong>Market:</strong> Outdoor, institutional</p>
                    </div>
                </div>
                
                <div class="product-card">
                    <div class="product-img">
                        <i class="fas fa-trash-restore"></i>
                    </div>
                    <div class="product-content">
                        <h4>Dustbins & Utility Items</h4>
                        <p>Recycled plastic dustbins, toys, plastic rods, and thousands of other utility items for household and commercial use.</p>
                        <p><strong>Variety:</strong> 100+ products</p>
                        <p><strong>Applications:</strong> Home, office, public spaces</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>TRASH TO CASH</h3>
                    <p>Transforming plastic waste into profitable, sustainable products. Building a circular economy where waste becomes wealth and environmental responsibility creates economic opportunity.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <a href="#home">Home</a>
                    <a href="#business">Business Model</a>
                    <a href="#process">Recycling Process</a>
                    <a href="#financials">Financial Analysis</a>
                    <a href="#products">Our Products</a>
                </div>
                
                <div class="footer-column">
                    <h3>Accepted Materials</h3>
                    <a href="#">Transparent Plastic Bottles</a>
                    <a href="#">Mixed Plastic Items</a>
                    <a href="#">Single-Use Plastic Bags</a>
                    <a href="#">Wafer/Chip Packets</a>
                    <a href="#">Plastic Containers</a>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Information</h3>
                    <div class="contact-info">
                        <p><i class="fas fa-map-marker-alt"></i> Prince Recycling Project</p>
                        <p><i class="fas fa-phone"></i> +91 76318 34410</p>
                        <p><i class="fas fa-envelope"></i> trash2cash11@gmail.com</p>
                        <p><i class="fas fa-envelope"></i> prince86173@gmail.com</p>
                        <p><i class="fas fa-clock"></i> Mon-Sat: 8:00 AM - 8:00 PM</p>
                        <p><i class="fas fa-industry"></i> Capacity: 2.4-3.5 tons/day</p>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 TRASH TO CASH - Prince Recycling Project. All rights reserved. | "Waste management is not just about disposal – it's about creating value."</p>
                <p style="margin-top: 10px; font-size: 0.85rem;">Building startups with waste. Turning problems into profits.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            menuToggle.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                menuToggle.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    // Close mobile menu if open
                    navLinks.classList.remove('active');
                    menuToggle.innerHTML = '<i class="fas fa-bars"></i>';
                    
                    // Smooth scroll
                    window.scrollTo({
                        top: targetElement.offsetTop - 100,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Add shadow to header on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if(window.scrollY > 50) {
                header.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>