<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sheffield Luxury Rentals | Premium Apartments in Sheffield</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1580587771525-78b9dba3b914?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            padding: 2rem 0;
            text-align: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        nav {
            background-color: var(--primary);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
        }
        
        nav ul li {
            margin: 0 1rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        .search-bar {
            background-color: white;
            padding: 1.5rem;
            border-radius: 5px;
            max-width: 800px;
            margin: -3rem auto 2rem auto;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 10;
        }
        
        .search-bar form {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: space-between;
        }
        
        .search-bar select, .search-bar input {
            padding: 0.5rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            flex: 1;
            min-width: 150px;
        }
        
        .search-bar button {
            background-color: var(--secondary);
            color: white;
            border: none;
            padding: 0.5rem 1.5rem;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .search-bar button:hover {
            background-color: #2980b9;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary);
        }
        
        .properties {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        
        .property-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .property-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        .property-image {
            height: 250px;
            overflow: hidden;
            position: relative;
        }
        
        .property-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .property-card:hover .property-image img {
            transform: scale(1.05);
        }
        
        .status {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background-color: var(--success);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .status.rented {
            background-color: var(--accent);
        }
        
        .property-details {
            padding: 1.5rem;
        }
        
        .price {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .price span {
            font-size: 1rem;
            font-weight: normal;
            color: #777;
        }
        
        .address {
            color: #777;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }
        
        .address i {
            margin-right: 0.5rem;
            color: var(--secondary);
        }
        
        .features {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        .feature {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
        }
        
        .feature i {
            margin-right: 0.3rem;
            color: var(--secondary);
        }
        
        .actions {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
        }
        
        .btn {
            padding: 0.6rem 1.2rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .btn-primary {
            background-color: var(--secondary);
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
        }
        
        .btn-secondary {
            background-color: var(--light);
            color: var(--dark);
        }
        
        .btn-secondary:hover {
            background-color: #ddd;
        }
        
        .btn-danger {
            background-color: var(--accent);
            color: white;
        }
        
        .btn-danger:hover {
            background-color: #c0392b;
        }
        
        .payment-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .payment-content {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            max-width: 500px;
            width: 90%;
            position: relative;
        }
        
        .close-modal {
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 1.5rem;
            cursor: pointer;
            color: #777;
        }
        
        .payment-title {
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .payment-instructions {
            background-color: var(--light);
            padding: 1rem;
            border-radius: 5px;
            margin-bottom: 1.5rem;
        }
        
        .wallet-address {
            background-color: #f0f0f0;
            padding: 1rem;
            border-radius: 5px;
            font-family: monospace;
            word-break: break-all;
            margin: 1rem 0;
            font-size: 0.9rem;
        }
        
        .qr-code {
            text-align: center;
            margin: 1rem 0;
        }
        
        .qr-code img {
            max-width: 200px;
            height: auto;
        }
        
        .disclaimer {
            font-size: 0.8rem;
            color: #777;
            margin-top: 1rem;
        }
        
        footer {
            background-color: var(--primary);
            color: white;
            padding: 3rem 1rem;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            text-align: left;
        }
        
        .footer-section h3 {
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .footer-section p, .footer-section a {
            color: #ddd;
            margin-bottom: 0.5rem;
            display: block;
            text-decoration: none;
        }
        
        .footer-section a:hover {
            color: var(--secondary);
        }
        
        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-icons a {
            color: white;
            font-size: 1.2rem;
        }
        
        .copyright {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
            
            .search-bar form {
                flex-direction: column;
            }
            
            .properties {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">Sheffield <span>Luxury Rentals</span></div>
        <div class="tagline">Premium apartments in the heart of Sheffield</div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#properties">Properties</a></li>
            <li><a href="#about">About Us</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <div class="search-bar">
        <form>
            <select name="location">
                <option value="">All Locations</option>
                <option value="city-centre">City Centre</option>
                <option value="kelham-island">Kelham Island</option>
                <option value="ecclesall">Ecclesall</option>
                <option value="crookes">Crookes</option>
            </select>
            <select name="bedrooms">
                <option value="">Bedrooms</option>
                <option value="1">1 Bedroom</option>
                <option value="2">2 Bedrooms</option>
                <option value="3">3+ Bedrooms</option>
            </select>
            <select name="price">
                <option value="">Price Range</option>
                <option value="0-800">£0 - £800</option>
                <option value="800-1200">£800 - £1200</option>
                <option value="1200-2000">£1200+</option>
            </select>
            <button type="submit">Search</button>
        </form>
    </div>
    
    <div class="container" id="properties">
        <h2 class="section-title">Available Properties in Sheffield</h2>
        <div class="properties">
            <!-- Property 1 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Modern Apartment in Kelham Island">
                    <div class="status">Available</div>
                </div>
                <div class="property-details">
                    <div class="price">£1,150 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> Kelham Island, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 2 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 1 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 850 sqft</div>
                        <div class="feature"><i class="fas fa-wifi"></i> WiFi</div>
                    </div>
                    <p>Stunning modern apartment in the vibrant Kelham Island area. Open plan living with high-end finishes and balcony overlooking the river.</p>
                    <div class="actions">
                        <button class="btn btn-primary rent-btn" data-property="Kelham Island Apartment">Rent Now</button>
                    </div>
                </div>
            </div>
            
            <!-- Property 2 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1522708323590-d24dbb6b0267?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Luxury City Centre Apartment">
                    <div class="status rented">Rented</div>
                </div>
                <div class="property-details">
                    <div class="price">£1,450 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> City Centre, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 2 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 2 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 1100 sqft</div>
                        <div class="feature"><i class="fas fa-swimming-pool"></i> Gym</div>
                    </div>
                    <p>Luxury penthouse in the heart of Sheffield with panoramic city views. Includes access to building amenities including gym and concierge.</p>
                    <div class="actions">
                        <button class="btn btn-secondary" disabled>Rented</button>
                    </div>
                </div>
            </div>
            
            <!-- Property 3 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1493809842364-78817add7ffb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Ecclesall Road Apartment">
                    <div class="status">Available</div>
                </div>
                <div class="property-details">
                    <div class="price">£950 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> Ecclesall, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 1 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 1 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 650 sqft</div>
                        <div class="feature"><i class="fas fa-parking"></i> Parking</div>
                    </div>
                    <p>Charming one-bedroom apartment on popular Ecclesall Road. Recently refurbished with modern kitchen and bathroom.</p>
                    <div class="actions">
                        <button class="btn btn-primary rent-btn" data-property="Ecclesall Road Apartment">Rent Now</button>
                    </div>
                </div>
            </div>
            
            <!-- Property 4 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1582268611958-ebfd161ef9cf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Crookes Victorian House">
                    <div class="status">Available</div>
                </div>
                <div class="property-details">
                    <div class="price">£1,800 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> Crookes, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 3 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 2 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 1800 sqft</div>
                        <div class="feature"><i class="fas fa-home"></i> Garden</div>
                    </div>
                    <p>Beautiful Victorian house in the popular Crookes area. Period features combined with modern comforts and private garden.</p>
                    <div class="actions">
                        <button class="btn btn-primary rent-btn" data-property="Crookes Victorian House">Rent Now</button>
                    </div>
                </div>
            </div>
            
            <!-- Property 5 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1502672260266-1c1ef2d93688?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Neepsend Luxury Loft">
                    <div class="status rented">Rented</div>
                </div>
                <div class="property-details">
                    <div class="price">£1,300 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> Neepsend, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 2 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 1 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 1200 sqft</div>
                        <div class="feature"><i class="fas fa-warehouse"></i> Loft</div>
                    </div>
                    <p>Industrial-chic loft conversion in the up-and-coming Neepsend area. Exposed brick, high ceilings and large windows.</p>
                    <div class="actions">
                        <button class="btn btn-secondary" disabled>Rented</button>
                    </div>
                </div>
            </div>
            
            <!-- Property 6 -->
            <div class="property-card">
                <div class="property-image">
                    <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Endcliffe New Build">
                    <div class="status">Available</div>
                </div>
                <div class="property-details">
                    <div class="price">£1,650 <span>/month</span></div>
                    <div class="address"><i class="fas fa-map-marker-alt"></i> Endcliffe, Sheffield</div>
                    <div class="features">
                        <div class="feature"><i class="fas fa-bed"></i> 2 Bed</div>
                        <div class="feature"><i class="fas fa-bath"></i> 2 Bath</div>
                        <div class="feature"><i class="fas fa-vector-square"></i> 950 sqft</div>
                        <div class="feature"><i class="fas fa-car"></i> Parking</div>
                    </div>
                    <p>Brand new luxury apartment in the desirable Endcliffe area. High-spec finishes and private balcony with green views.</p>
                    <div class="actions">
                        <button class="btn btn-primary rent-btn" data-property="Endcliffe New Build">Rent Now</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="container" id="about">
        <h2 class="section-title">About Sheffield Luxury Rentals</h2>
        <p style="text-align: center; max-width: 800px; margin: 0 auto 2rem auto;">
            Sheffield Luxury Rentals specializes in premium rental properties in Sheffield's most sought-after neighborhoods. 
            We offer a curated selection of high-end apartments and houses, all carefully vetted for quality and comfort. 
            Our streamlined booking process makes securing your dream home effortless.
        </p>
        
        <div style="display: flex; justify-content: center; gap: 2rem; flex-wrap: wrap; margin-top: 2rem;">
            <div style="background-color: white; padding: 1.5rem; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); text-align: center; max-width: 250px;">
                <i class="fas fa-home" style="font-size: 2rem; color: var(--secondary); margin-bottom: 1rem;"></i>
                <h3 style="margin-bottom: 0.5rem;">Premium Properties</h3>
                <p style="font-size: 0.9rem;">Only the highest quality homes in Sheffield's best locations</p>
            </div>
            <div style="background-color: white; padding: 1.5rem; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); text-align: center; max-width: 250px;">
                <i class="fas fa-lock" style="font-size: 2rem; color: var(--secondary); margin-bottom: 1rem;"></i>
                <h3 style="margin-bottom: 0.5rem;">Secure Payments</h3>
                <p style="font-size: 0.9rem;">Blockchain technology ensures your deposit is safe</p>
            </div>
            <div style="background-color: white; padding: 1.5rem; border-radius: 8px; box-shadow: 0 5px 15px rgba(0,0,0,0.1); text-align: center; max-width: 250px;">
                <i class="fas fa-headset" style="font-size: 2rem; color: var(--secondary); margin-bottom: 1rem;"></i>
                <h3 style="margin-bottom: 0.5rem;">24/7 Support</h3>
                <p style="font-size: 0.9rem;">Our team is always available to assist you</p>
            </div>
        </div>
    </div>
    
    <div class="payment-modal" id="paymentModal">
        <div class="payment-content">
            <span class="close-modal">&times;</span>
            <h2 class="payment-title">Secure Your Rental</h2>
            <div class="payment-instructions">
                <p>To secure this property, please send the deposit amount of <strong>£1,000</strong> to our Taproot Bitcoin wallet address below. Once payment is confirmed, we will contact you to complete the rental agreement.</p>
            </div>
            
            <h3>Property: <span id="propertyName"></span></h3>
            
            <div class="qr-code">
                <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=bitcoin:bc1p2mlnlmluamk80a3xlw9d3luucr0crtcne8xyepl88n5k4vfznf7skd4t4r" alt="Bitcoin QR Code">
            </div>
            
            <p>Send payment to this Taproot Bitcoin wallet address:</p>
            <div class="wallet-address">bc1p2mlnlmluamk80a3xlw9d3luucr0crtcne8xyepl88n5k4vfznf7skd4t4r</div>
            
            <p style="margin-top: 1rem;"><strong>Important:</strong> After making payment, please email your transaction ID and contact details to <a href="mailto:Shefielduni@proton.me">Shefielduni@proton.me</a> or WhatsApp us at +44 7832 714017.</p>
            
            <div class="disclaimer">
                <p><strong>Disclaimer:</strong> Deposits are fully refundable if the property becomes unavailable. Sheffield Luxury Rentals is not responsible for incorrect payments sent to the wrong address. Please double-check the wallet address before sending.</p>
            </div>
            
            <div style="display: flex; justify-content: space-between; margin-top: 2rem;">
                <button class="btn btn-danger" id="refundBtn">Refund My Deposit</button>
                <button class="btn btn-secondary" id="complaintBtn">File a Complaint</button>
            </div>
        </div>
    </div>
    
    <footer id="contact">
        <div class="footer-content">
            <div class="footer-section">
                <h3>Contact Us</h3>
                <p><i class="fas fa-envelope"></i> Shefielduni@proton.me</p>
                <p><i class="fas fa-phone"></i> +44 7832 714017</p>
                <p><i class="fas fa-map-marker-alt"></i> Sheffield, UK</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Quick Links</h3>
                <a href="#">Home</a>
                <a href="#properties">Properties</a>
                <a href="#about">About Us</a>
                <a href="#contact">Contact</a>
                <a href="#" id="footerRefundBtn">Refund Deposit</a>
                <a href="#" id="footerComplaintBtn">File a Complaint</a>
            </div>
            
            <div class="footer-section">
                <h3>Legal</h3>
                <a href="#">Terms & Conditions</a>
                <a href="#">Privacy Policy</a>
                <a href="#">Cookie Policy</a>
                <a href="#">Rental Agreement</a>
            </div>
        </div>
        
        <div class="copyright">
            &copy; 2023 Sheffield Luxury Rentals. All rights reserved.
        </div>
    </footer>
    
    <script>
        // Payment Modal Functionality
        const rentButtons = document.querySelectorAll('.rent-btn');
        const paymentModal = document.getElementById('paymentModal');
        const closeModal = document.querySelector('.close-modal');
        const propertyName = document.getElementById('propertyName');
        const refundBtn = document.getElementById('refundBtn');
        const complaintBtn = document.getElementById('complaintBtn');
        const footerRefundBtn = document.getElementById('footerRefundBtn');
        const footerComplaintBtn = document.getElementById('footerComplaintBtn');
        
        rentButtons.forEach(button => {
            button.addEventListener('click', function() {
                propertyName.textContent = this.getAttribute('data-property');
                paymentModal.style.display = 'flex';
                document.body.style.overflow = 'hidden';
            });
        });
        
        closeModal.addEventListener('click', function() {
            paymentModal.style.display = 'none';
            document.body.style.overflow = 'auto';
        });
        
        window.addEventListener('click', function(e) {
            if (e.target === paymentModal) {
                paymentModal.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });
        
        refundBtn.addEventListener('click', function() {
            alert('For deposit refunds, please contact us at Shefielduni@proton.me with your payment details and reason for refund.');
        });
        
        complaintBtn.addEventListener('click', function() {
            alert('To file a complaint regarding your deposit, please email us at Shefielduni@proton.me with details of your issue.');
        });
        
        footerRefundBtn.addEventListener('click', function(e) {
            e.preventDefault();
            alert('For deposit refunds, please contact us at Shefielduni@proton.me with your payment details and reason for refund.');
        });
        
        footerComplaintBtn.addEventListener('click', function(e) {
            e.preventDefault();
            alert('To file a complaint regarding your deposit, please email us at Shefielduni@proton.me with details of your issue.');
        });
    </script>
</body>
</html>
