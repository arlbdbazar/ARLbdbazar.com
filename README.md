# ARLbdbazar.com
Online business
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARL BD BAZAR - অনলাইন শপিং মল</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background: #f5f5f5;
            color: #333;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* হেডার */
        header {
            background: linear-gradient(135deg, #FF6B6B, #FF8E72);
            color: white;
            padding: 20px 0;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .logo {
            font-size: 1.8em;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .header-right {
            display: flex;
            gap: 20px;
            align-items: center;
        }
        
        .search-bar {
            display: flex;
            gap: 10px;
        }
        
        .search-bar input {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            width: 250px;
        }
        
        .search-bar button {
            background: white;
            color: #FF6B6B;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }
        
        .header-icons {
            display: flex;
            gap: 15px;
            font-size: 1.3em;
            cursor: pointer;
        }
        
        .cart-badge {
            background: white;
            color: #FF6B6B;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8em;
            font-weight: bold;
            position: absolute;
            top: -8px;
            right: -8px;
        }
        
        .cart-icon {
            position: relative;
        }
        
        /* নেভিগেশন */
        nav {
            background: rgba(0,0,0,0.1);
            padding: 10px 0;
        }
        
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 5px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 5px;
            transition: all 0.3s;
            cursor: pointer;
            display: inline-block;
        }
        
        nav a:hover {
            background: rgba(0,0,0,0.2);
        }
        
        /* ব্যানার */
        .banner {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 50px 20px;
            text-align: center;
            border-radius: 10px;
            margin: 30px 0;
        }
        
        .banner h2 {
            font-size: 2.5em;
            margin-bottom: 15px;
        }
        
        .banner p {
            font-size: 1.2em;
            margin-bottom: 20px;
        }
        
        /* ক্যাটাগরি */
        .categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin: 30px 0;
        }
        
        .category-box {
            background: white;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        .category-box:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            background: #FF6B6B;
            color: white;
        }
        
        .category-box .icon {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        .category-box h3 {
            font-size: 1em;
        }
        
        /* পণ্য সেকশন */
        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 40px 0 20px 0;
        }
        
        .section-header h2 {
            font-size: 2em;
        }
        
        .view-all {
            color: #FF6B6B;
            text-decoration: none;
            font-weight: bold;
            cursor: pointer;
        }
        
        /* পণ্য গ্রিড */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }
        
        .product-image {
            width: 100%;
            height: 180px;
            background: linear-gradient(135deg, #FF6B6B, #FF8E72);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4em;
            color: white;
        }
        
        .product-info {
            padding: 15px;
        }
        
        .product-info h3 {
            font-size: 1em;
            margin-bottom: 8px;
            color: #333;
        }
        
        .product-rating {
            color: #FFC107;
            font-size: 0.9em;
            margin-bottom: 8px;
        }
        
        .product-price {
            display: flex;
            gap: 10px;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .new-price {
            font-size: 1.3em;
            color: #FF6B6B;
            font-weight: bold;
        }
        
        .old-price {
            text-decoration: line-through;
            color: #999;
        }
        
        .discount-badge {
            background: #FF6B6B;
            color: white;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8em;
            font-weight: bold;
        }
        
        .product-actions {
            display: flex;
            gap: 10px;
        }
        
        .btn {
            flex: 1;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
            font-size: 0.9em;
        }
        
        .btn-primary {
            background: #FF6B6B;
            color: white;
        }
        
        .btn-primary:hover {
            background: #E55039;
        }
        
        .btn-secondary {
            background: #f0f0f0;
            color: #333;
        }
        
        .btn-secondary:hover {
            background: #e0e0e0;
        }
        
        /* শপিং কার্ট */
        .cart-sidebar {
            position: fixed;
            right: -400px;
            top: 0;
            width: 400px;
            height: 100vh;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.2);
            overflow-y: auto;
            z-index: 1000;
            transition: right 0.3s;
            padding: 20px;
        }
        
        .cart-sidebar.open {
            right: 0;
        }
        
        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .close-cart {
            background: none;
            border: none;
            font-size: 1.5em;
            cursor: pointer;
        }
        
        .cart-items {
            margin-bottom: 20px;
            max-height: 400px;
            overflow-y: auto;
        }
        
        .cart-item {
            display: flex;
            gap: 10px;
            padding: 10px;
            border-bottom: 1px solid #eee;
            margin-bottom: 10px;
        }
        
        .cart-item-image {
            width: 60px;
            height: 60px;
            background: #f0f0f0;
            border-radius: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
        }
        
        .cart-item-details {
            flex: 1;
        }
        
        .cart-item-details h4 {
            font-size: 0.9em;
            margin-bottom: 5px;
        }
        
        .cart-item-price {
            color: #FF6B6B;
            font-weight: bold;
            font-size: 0.95em;
        }
        
        .cart-summary {
            border-top: 2px solid #eee;
            padding-top: 15px;
            margin-bottom: 15px;
        }
        
        .summary-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .total-amount {
            font-size: 1.2em;
            color: #FF6B6B;
            font-weight: bold;
        }
        
        .checkout-btn {
            width: 100%;
            padding: 15px;
            background: #FF6B6B;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .checkout-btn:hover {
            background: #E55039;
        }
        
        /* ফুটার */
        footer {
            background: #333;
            color: white;
            padding: 40px 20px;
            margin-top: 50px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            margin-bottom: 15px;
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 8px;
        }
        
        .footer-section a {
            color: #ccc;
            text-decoration: none;
            cursor: pointer;
        }
        
        .footer-section a:hover {
            color: #FF6B6B;
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #555;
        }
        
        /* মোবাইল */
        @media (max-width: 768px) {
            .search-bar input {
                width: 100%;
            }
            
            .products-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .cart-sidebar {
                width: 100%;
                right: -100%;
            }
            
            .banner h2 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <!-- হেডার -->
    <header>
        <div class="container">
            <div class="header-top">
                <div class="logo">
                    🛍️ ARL BD BAZAR
                </div>
                
                <div class="header-right">
                    <div class="search-bar">
                        <input type="text" id="searchInput" placeholder="পণ্য খুঁজুন...">
                        <button onclick="search()">🔍</button>
                    </div>
                    
                    <div class="header-icons">
                        <span title="প্রিয় তালিকা">❤️</span>
                        <div class="cart-icon" onclick="toggleCart()">
                            🛒
                            <span class="cart-badge" id="cartCount">0</span>
                        </div>
                        <span title="অ্যাকাউন্ট">👤</span>
                    </div>
                </div>
            </div>
            
            <!-- নেভিগেশন -->
            <nav>
                <ul>
                    <li><a onclick="scrollToSection('home')">🏠 হোম</a></li>
                    <li><a onclick="scrollToSection('deals')">🔥 ডিল</a></li>
                    <li><a onclick="scrollToSection('featured')">⭐ ফিচার্ড</a></li>
                    <li><a onclick="scrollToSection('contact')">📞 যোগাযোগ</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- মেইন কন্টেন্ট -->
    <div class="container">
        <!-- ব্যানার -->
        <div class="banner" id="home">
            <h2>🎉 স্বাগতম ARL BD BAZAR এ</h2>
            <p>সেরা দামে সেরা পণ্য</p>
            <button class="btn btn-primary" style="padding: 12px 30px;">এখনই কেনাকাটা করুন</button>
        </div>
        
        <!-- ক্যাটাগরি -->
        <div class="section-header">
            <h2>📂 ক্যাটাগরি</h2>
        </div>
        <div class="categories">
            <div class="category-box" onclick="filterProducts('toys')">
                <div class="icon">🚗</div>
                <h3>খেলনা</h3>
            </div>
            <div class="category-box" onclick="filterProducts('electronics')">
                <div class="icon">📱</div>
                <h3>ইলেকট্রনিক্স</h3>
            </div>
            <div class="category-box" onclick="filterProducts('clothing')">
                <div class="icon">👕</div>
                <h3>কাপড়</h3>
            </div>
            <div class="category-box" onclick="filterProducts('home')">
                <div class="icon">🏠</div>
                <h3>গৃহস্থালী</h3>
            </div>
            <div class="category-box" onclick="filterProducts('books')">
                <div class="icon">📚</div>
                <h3>বই</h3>
            </div>
            <div class="category-box" onclick="filterProducts('all')">
                <div class="icon">🌟</div>
                <h3>সব দেখুন</h3>
            </div>
        </div>
        
        <!-- বিশেষ অফার -->
        <div class="section-header" id="deals">
            <h2>🔥 বিশেষ অফার</h2>
            <a class="view-all" onclick="alert('আরও অফার দেখুন')">সব দেখুন →</a>
        </div>
        <div class="products-grid" id="dealsGrid">
            <!-- ডিল পণ্য এখানে যাবে -->
        </div>
        
        <!-- ফিচার্ড পণ্য -->
        <div class="section-header" id="featured">
            <h2>⭐ ফিচার্ড পণ্য</h2>
            <a class="view-all" onclick="alert('আরও পণ্য দেখুন')">সব দেখুন →</a>
        </div>
        <div class="products-grid" id="featuredGrid">
            <!-- ফিচার্ড পণ্য এখানে যাবে -->
        </div>
    </div>
    
    <!-- ফুটার -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>🛍️ ARL BD BAZAR</h3>
                    <p>আমরা আপনার বিশ্বস্ত অনলাইন শপিং পার্টনার</p>
                </div>
                
                <div class="footer-section">
                    <h3>কুইক লিংক</h3>
                    <ul>
                        <li><a onclick="alert('পৃষ্ঠা চলছে')">আমাদের সম্পর্কে</a></li>
                        <li><a onclick="alert('পৃষ্ঠা চলছে')">সহায়তা</a></li>
                        <li><a onclick="alert('পৃষ্ঠা চলছে')">শর্তাবলী</a></li>
                        <li><a onclick="alert('পৃষ্ঠা চলছে')">গোপনীয়তা নীতি</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>যোগাযোগ করুন</h3>
                    <ul>
                        <li>📞 +8801734347211</li>
                        <li>📧 info@arlbdbazar.com</li>
                        <li>📍 ঢাকা, বাংলাদেশ</li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>অনুসরণ করুন</h3>
                    <ul>
                        <li><a onclick="alert('Facebook এ যাচ্ছেন')">📘 Facebook</a></li>
                        <li><a onclick="alert('Instagram এ যাচ্ছেন')">📷 Instagram</a></li>
                        <li><a onclick="alert('WhatsApp এ যাচ্ছেন')">💬 WhatsApp</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2025 ARL BD BAZAR। সর্বাধিকার সংরক্ষিত।</p>
            </div>
        </div>
    </footer>
    
    <!-- শপিং কার্ট সাইডবার -->
    <div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h3>🛒 আমার কার্ট</h3>
            <button class="close-cart" onclick="toggleCart()">✕</button>
        </div>
        
        <div class="cart-items" id="cartItems">
            <p style="text-align: center; color: #999;">কার্ট খালি</p>
        </div>
        
        <div class="cart-summary">
            <div class="summary-row">
                <span>সাবটোটাল:</span>
                <span id="subtotal">৳0</span>
            </div>
            <div class="summary-row">
                <span>ডেলিভারি:</span>
                <span>৳100</span>
            </div>
            <div class="summary-row">
                <span class="total-amount">মোট:</span>
                <span class="total-amount" id="total">৳100</span>
            </div>
        </div>
        
        <button class="checkout-btn" onclick="checkout()">🛒 চেকআউট করুন</button>
    </div>
    
    <script>
        // সাম্পল পণ্য ডেটা
        const products = [
            { id: 1, name: 'লাল খেলনা গাড়ি', price: 3500, oldPrice: 4500, category: 'toys', emoji: '🚗', rating: 4.5 },
            { id: 2, name: 'পিংক খেলনা গাড়ি', price: 4000, oldPrice: 5000, category: 'toys', emoji: '💗', rating: 4.8 },
            { id: 3, name: 'নীল খেলনা গাড়ি', price: 3800, oldPrice: 4800, category: 'toys', emoji: '🔵', rating: 4.3 },
            { id: 4, name: 'হলুদ খেলনা গাড়ি', price: 3200, oldPrice: 4200, category: 'toys', emoji: '🟡', rating: 4.2 },
            { id: 5, name: 'স্মার্টফোন', price: 15000, oldPrice: 18000, category: 'electronics', emoji: '📱', rating: 4.6 },
            { id: 6, name: 'ওয়্যারলেস হেডফোন', price: 2500, oldPrice: 3500, category: 'electronics', emoji: '🎧', rating: 4.4 },
            { id: 7, name: 'শার্ট', price: 800, oldPrice: 1200, category: 'clothing', emoji: '👕', rating: 4.1 },
            { id: 8, name: 'প্যান্ট', price: 1200, oldPrice: 1800, category: 'clothing', emoji: '👖', rating: 4.0 },
        ];
        
        let cart = [];
        
        // পণ্য রেন্ডার করুন
        function renderProducts(category = 'toys') {
            const filtered = category === 'all' ? products : products.filter(p => p.category === category);
            
            const html = filtered.map(product => {
                const discount = Math.round(((product.oldPrice - product.price) / product.oldPrice) * 100);
                return `
                    <div class="product-card">
                        <div class="product-image">${product.emoji}</div>
                        <div class="product-info">
                            <h3>${product.name}</h3>
                            <div class="product-rating">⭐ ${product.rating}</div>
                            <div class="product-price">
                                <span class="new-price">৳${product.price}</span>
                                <span class="old-price">৳${product.oldPrice}</span>
                                <span class="discount-badge">${discount}% ছাড়</span>
                            </div>
                            <div class="product-actions">
                                <button class="btn btn-primary" onclick="addToCart(${product.id})">🛒 কার্টে যোগ করুন</button>
                                <button class="btn btn-secondary" onclick="addToWishlist(${product.id})">❤️</button>
                            </div>
                        </div>
                    </div>
                `;
            }).join('');
            
            document.getElementById('dealsGrid').innerHTML = html;
            document.getElementById('featuredGrid').innerHTML = html;
        }
        
        // কার্টে যোগ করুন
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(p => p.id === productId);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({ ...product, quantity: 1 });
            }
            
            updateCart();
            alert(`✅ ${product.name} কার্টে যোগ হয়েছে!`);
        }
        
        // কার্ট আপডেট করুন
        function updateCart() {
            document.getElementById('cartCount').textContent = cart.reduce((sum, item) => sum + item.quantity, 0);
            
            const cartItemsHTML = cart.map(item => `
                <div class="cart-item">
                    <div class="cart-item-image">${item.emoji}</div>
                    <div class="cart-item-details">
                        <h4>${item.name}</h4>
                        <div class="cart-item-price">৳${item.price} × ${item.quantity}</div>
                    </div>
                </div>
            `).join('');
            
            document.getElementById('cartItems').innerHTML = cartItemsHTML || '<p style="text-align: center; color: #999;">কার্ট খালি</p>';
            
            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const total = subtotal + 100;
            
            document.getElementById('subtotal').textContent = `৳${subtotal}`;
            document.getElementById('total').textContent = `৳${total}`;
        }
        
        // কার্ট টগল করুন
        function toggleCart() {
            document.getElementById('cartSidebar').classList.toggle('open');
        }
        
        // ক্যাটাগরি ফিল্টার করুন
        function filterProducts(category) {
            renderProducts(category);
        }
        
        // চেকআউট করুন
        function checkout() {
            if (cart.length === 0) {
                alert('❌ কার্ট খালি! কিছু পণ্য যোগ করুন।');
                return;
            }
            const total = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0) + 100;
            alert(`✅ আপনার অর্ডার নিশ্চিত করা হয়েছে!\n\nমোট টাকা: ৳${total}\n\n📞 আমরা শীঘ্রই যোগাযোগ করব।`);
            cart = [];
            updateCart();
            toggleCart();
        }
        
        // প্রিয় তালিকায় যোগ করুন
        function addToWishlist(productId) {
            const product = products.find(p => p.id === productId);
            alert(`❤️ ${product.name} প্রিয় তালিকায় যোগ হয়েছে!`);
        }
        
        // সার্চ করুন
        function search() {
            const query = document.getElementById('searchInput').value;
            alert(`🔍 "${query}" খুঁজছি...`);
        }
        
        // সেকশনে স্ক্রল করুন
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({ behavior: 'smooth' });
        }
        
        // পেজ লোড হলে পণ্য রেন্ডার করুন
        window.addEventListener('load', () => {
            renderProducts('toys');
        });
    </script>
</body>
</html>
