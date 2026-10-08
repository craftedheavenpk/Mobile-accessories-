<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hypermart Mobiles & Accessories | Lahore</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brandPrimary: '#2563eb', // Modern Tech Blue
                        brandDark: '#1e293b',
                        brandAccent: '#f59e0b',
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col">

    <!-- Top Announcement Bar -->
    <div class="bg-blue-600 text-white text-xs py-2 px-4 text-center font-medium">
        <i class="fa-solid fa-truck-fast mr-2"></i> 100% Original Mobile Accessories & PTA Approved Phones | WhatsApp: 03034812714
    </div>

    <!-- Header / Navbar -->
    <header class="sticky top-0 z-40 bg-slate-900/95 backdrop-blur-md border-b border-slate-800 shadow-lg">
        <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between">
            
            <!-- Mobile Menu & Logo -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleSideMenu()" class="text-blue-400 text-xl p-1 focus:outline-none md:hidden">
                    <i class="fa-solid fa-bars"></i>
                </button>
                <a href="#" class="flex items-center space-x-2">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-blue-600 to-indigo-500 flex items-center justify-center shadow-md">
                        <i class="fa-solid fa-mobile-screen-button text-white text-lg"></i>
                    </div>
                    <div>
                        <span class="text-xl font-bold tracking-tight text-white block leading-none">Hypermart Mobiles</span>
                        <span class="text-[10px] text-blue-400 tracking-wider uppercase font-semibold">Gulberg III, Lahore</span>
                    </div>
                </a>
            </div>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-6 font-medium text-sm">
                <a href="#home" class="hover:text-blue-400 transition">Home</a>
                <a href="#phones" class="hover:text-blue-400 transition">New & Used Phones</a>
                <a href="#accessories" class="hover:text-blue-400 transition">Accessories</a>
                <a href="#repair" class="hover:text-blue-400 transition">Repairing Services</a>
                <a href="#contact" class="hover:text-blue-400 transition">Contact</a>
            </nav>

            <!-- Cart / Bucket Button -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleCart()" class="relative bg-blue-600 hover:bg-blue-500 text-white px-4 py-2 rounded-xl font-medium text-sm flex items-center shadow transition">
                    <i class="fa-solid fa-bag-shopping mr-2"></i>
                    <span class="hidden sm:inline">Cart</span>
                    <span id="cart-count" class="absolute -top-1.5 -right-1.5 bg-red-500 text-white text-xs w-5 h-5 rounded-full flex items-center justify-center font-bold shadow">0</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Side Menu Drawer for Mobile -->
    <div id="sideMenu" class="fixed inset-0 z-50 bg-black/70 backdrop-blur-sm hidden transition-opacity">
        <div class="bg-slate-900 w-72 h-full p-6 flex flex-col justify-between shadow-2xl border-r border-slate-800 transform -translate-x-full transition-transform duration-300" id="sideMenuPanel">
            <div>
                <div class="flex items-center justify-between mb-8">
                    <div class="flex items-center space-x-2">
                        <div class="w-8 h-8 rounded-lg bg-blue-600 flex items-center justify-center">
                            <i class="fa-solid fa-mobile-screen-button text-white text-sm"></i>
                        </div>
                        <span class="font-bold text-lg text-white">Hypermart Mobiles</span>
                    </div>
                    <button onclick="toggleSideMenu()" class="text-slate-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>
                <nav class="flex flex-col space-y-4 font-medium text-sm">
                    <a href="#home" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-blue-400 py-2 border-b border-slate-800"><i class="fa-solid fa-house w-6 text-blue-500"></i> <span>Home</span></a>
                    <a href="#phones" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-blue-400 py-2 border-b border-slate-800"><i class="fa-solid fa-mobile w-6 text-blue-500"></i> <span>New & Used Phones</span></a>
                    <a href="#accessories" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-blue-400 py-2 border-b border-slate-800"><i class="fa-solid fa-headphones w-6 text-blue-500"></i> <span>Mobile Accessories</span></a>
                    <a href="#repair" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-blue-400 py-2 border-b border-slate-800"><i class="fa-solid fa-screwdriver-wrench w-6 text-blue-500"></i> <span>Repairing Services</span></a>
                    <a href="#contact" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-slate-300 hover:text-blue-400 py-2 border-b border-slate-800"><i class="fa-solid fa-phone w-6 text-blue-500"></i> <span>Contact & WhatsApp</span></a>
                </nav>
            </div>
            <div class="text-xs text-slate-500 text-center py-4 border-t border-slate-800">
                <p>© 2026 Hypermart Mobiles Lahore</p>
                <p class="mt-1">WhatsApp: 03034812714</p>
            </div>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-r from-slate-950 via-blue-950 to-slate-900 py-12 px-4 text-center border-b border-slate-800">
        <div class="max-w-4xl mx-auto">
            <span class="inline-block bg-blue-900/50 text-blue-300 text-xs font-semibold px-4 py-1.5 rounded-full mb-4 border border-blue-700/40">
                <i class="fa-solid fa-shield-halved text-amber-400 mr-1.5"></i> Lahore's Most Trusted Mobile & Tech Store
            </span>
            <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight text-white mb-4">
                Latest Smartphones & Premium <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-indigo-300">Tech Accessories</span>
            </h1>
            <p class="text-slate-300 text-sm sm:text-base max-w-2xl mx-auto mb-8 leading-relaxed">
                Explore brand new PTA approved smartphones, verified used phones in pristine condition, original fast chargers, holders, cables, pouches, touch smartwatches, and expert mobile repair services.
            </p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#phones" class="bg-blue-600 hover:bg-blue-500 text-white font-medium px-6 py-3 rounded-xl shadow-lg transition flex items-center text-sm">
                    <i class="fa-solid fa-mobile mr-2"></i> Browse Phones
                </a>
                <a href="#accessories" class="bg-slate-800 hover:bg-slate-700 text-blue-200 border border-slate-700 font-medium px-6 py-3 rounded-xl transition flex items-center text-sm">
                    <i class="fa-solid fa-headphones mr-2 text-blue-400"></i> View Accessories
                </a>
            </div>
        </div>
    </section>

    <!-- Brand Logos Section -->
    <section class="bg-slate-900/60 py-6 border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-xs uppercase tracking-widest text-slate-400 mb-4 font-semibold">Authorized Dealership & Dealing Brands</p>
            <div class="flex flex-wrap justify-center items-center gap-6 sm:gap-10 text-slate-400 font-bold text-base sm:text-lg">
                <span class="hover:text-blue-400 transition flex items-center"><i class="fa-brands fa-apple text-xl mr-2"></i> Apple</span>
                <span class="hover:text-blue-400 transition flex items-center"><i class="fa-solid fa-mobile-button text-xl mr-2"></i> Samsung</span>
                <span class="hover:text-blue-400 transition">Xiaomi</span>
                <span class="hover:text-blue-400 transition">OnePlus</span>
                <span class="hover:text-blue-400 transition">Vivo</span>
                <span class="hover:text-blue-400 transition">Oppo</span>
                <span class="hover:text-blue-400 transition">Realme</span>
                <span class="hover:text-blue-400 transition">Infinix</span>
            </div>
        </div>
    </section>

    <!-- Main Content Container -->
    <div class="max-w-7xl mx-auto px-4 py-10 flex-grow w-full space-y-16">

        <!-- Section 1: New & Used Mobile Phones -->
        <section id="phones">
            <div class="flex items-center justify-between mb-6 bg-slate-900/80 p-4 rounded-2xl border border-slate-800">
                <div>
                    <h2 class="text-xl sm:text-2xl font-bold text-white flex items-center">
                        <i class="fa-solid fa-mobile-screen text-blue-500 mr-2"></i> New & Used Mobile Phones
                    </h2>
                    <p class="text-xs text-slate-400 mt-0.5">PriceOye inspired best market rates with warranty and checking guarantee.</p>
                </div>
            </div>

            <!-- Phones Grid: 2 per row on mobile, up to 4 on desktop -->
            <div id="phones-grid" class="grid grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6">
                <!-- Populated via JS -->
            </div>
        </section>

        <!-- Section 2: Mobile Accessories -->
        <section id="accessories">
            <div class="flex items-center justify-between mb-6 bg-slate-900/80 p-4 rounded-2xl border border-slate-800">
                <div>
                    <h2 class="text-xl sm:text-2xl font-bold text-white flex items-center">
                        <i class="fa-solid fa-headphones text-blue-500 mr-2"></i> Mobile Accessories & Gadgets
                    </h2>
                    <p class="text-xs text-slate-400 mt-0.5">Chargers, holders, cables, pouches, smartwatches, speakers & more.</p>
                </div>
            </div>

            <!-- Accessories Grid: 2 per row on mobile, up to 4 on desktop -->
            <div id="accessories-grid" class="grid grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6">
                <!-- Populated via JS -->
            </div>
        </section>

        <!-- Section 3: Repairing Services Booking -->
        <section id="repair" class="bg-gradient-to-br from-slate-900 to-blue-950/40 border border-slate-800 rounded-3xl p-6 sm:p-8">
            <div class="max-w-3xl mx-auto text-center">
                <div class="w-12 h-12 rounded-2xl bg-blue-600/20 text-blue-400 flex items-center justify-center mx-auto mb-4 text-xl">
                    <i class="fa-solid fa-screwdriver-wrench"></i>
                </div>
                <h2 class="text-2xl font-bold text-white mb-2">Expert Mobile Repairing Services</h2>
                <p class="text-slate-300 text-xs sm:text-sm mb-6 leading-relaxed">
                    Broken screen? Battery draining fast? Charging port issue or software glitch? Get your smartphone repaired by certified technicians in Gulberg III, Lahore with genuine parts and quick turnaround.
                </p>
                <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 text-left mb-6">
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                        <h4 class="font-bold text-white text-sm mb-1"><i class="fa-solid fa-display text-blue-400 mr-1.5"></i> Screen Replacement</h4>
                        <p class="text-xs text-slate-400">Original display installation with touch guarantee.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                        <h4 class="font-bold text-white text-sm mb-1"><i class="fa-solid fa-battery-full text-blue-400 mr-1.5"></i> Battery Health</h4>
                        <p class="text-xs text-slate-400">High capacity battery replacement with warranty.</p>
                    </div>
                    <div class="bg-slate-900 p-4 rounded-xl border border-slate-800">
                        <h4 class="font-bold text-white text-sm mb-1"><i class="fa-solid fa-microchip text-blue-400 mr-1.5"></i> General Repair</h4>
                        <p class="text-xs text-slate-400">Camera, speaker, charging jack & software fixing.</p>
                    </div>
                </div>
                <a href="https://wa.me/923034812714?text=Hello%20Hypermart%20Mobiles,%20I%20want%20to%20inquire%20about%20mobile%20repair%20services." target="_blank" class="inline-flex items-center bg-blue-600 hover:bg-blue-500 text-white font-semibold px-6 py-3 rounded-xl shadow-lg transition text-sm">
                    <i class="fa-brands fa-whatsapp text-lg mr-2"></i> Book Repair via WhatsApp
                </a>
            </div>
        </section>

    </div>

    <!-- Contact & Store Information Section -->
    <section id="contact" class="max-w-4xl mx-auto px-4 py-8 mb-12 w-full text-center">
        <h2 class="text-2xl font-bold text-white mb-4">Contact & Store Location</h2>
        <div class="bg-slate-900 p-6 rounded-2xl border border-slate-800 inline-block w-full max-w-xl text-left shadow-lg">
            <div class="space-y-3 text-sm text-slate-300">
                <p><i class="fa-solid fa-location-dot text-blue-400 w-6"></i> <strong>Location:</strong> Main Plaza, Gulberg III, Lahore</p>
                <p><i class="fa-solid fa-phone text-blue-400 w-6"></i> <strong>WhatsApp Helpline:</strong> 03034812714</p>
                <p><i class="fa-solid fa-credit-card text-blue-400 w-6"></i> <strong>JazzCash / EasyPaisa:</strong> 03034812714</p>
                <p><i class="fa-solid fa-clock text-blue-400 w-6"></i> <strong>Timings:</strong> 10:00 AM – 9:00 PM (Monday to Saturday)</p>
            </div>
        </div>
    </section>

    <!-- Cart / Bucket Drawer Overlay -->
    <div id="cartDrawer" class="fixed inset-0 z-50 bg-black/70 backdrop-blur-sm hidden flex justify-end transition-opacity">
        <div class="bg-slate-900 w-full max-w-md h-full p-5 flex flex-col justify-between shadow-2xl border-l border-slate-800 transform translate-x-full transition-transform duration-300" id="cartPanel">
            <div>
                <div class="flex items-center justify-between pb-4 border-b border-slate-800">
                    <div class="flex items-center space-x-2">
                        <i class="fa-solid fa-bag-shopping text-blue-400 text-lg"></i>
                        <h3 class="font-bold text-lg text-white">Your Shopping Cart</h3>
                    </div>
                    <button onclick="toggleCart()" class="text-slate-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>

                <!-- Cart Items List -->
                <div id="cart-items" class="py-4 space-y-3 overflow-y-auto max-h-[calc(100vh-280px)]">
                    <p class="text-slate-500 text-center py-8 text-sm">Your cart is currently empty.</p>
                </div>
            </div>

            <!-- Cart Footer & WhatsApp Checkout -->
            <div class="pt-4 border-t border-slate-800">
                <div class="flex justify-between items-center mb-4 text-base font-bold text-white">
                    <span>Total Amount:</span>
                    <span id="cart-total" class="text-blue-400">Rs. 0</span>
                </div>
                <button onclick="checkoutWhatsApp()" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-semibold py-3 rounded-xl shadow-lg transition flex items-center justify-center space-x-2 text-sm">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>Checkout via WhatsApp</span>
                </button>
                <p class="text-[11px] text-slate-500 text-center mt-2">Payments accepted via Cash on Delivery, JazzCash & EasyPaisa (03034812714).</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-800 py-8 px-4 text-center text-xs text-slate-500">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4">
            <div class="flex items-center space-x-2">
                <div class="w-7 h-7 rounded-lg bg-blue-600 flex items-center justify-center">
                    <i class="fa-solid fa-mobile-screen-button text-white text-xs"></i>
                </div>
                <span class="font-bold text-white text-sm">Hypermart Mobiles & Accessories</span>
            </div>
            <p>© 2026 Hypermart Mobiles Lahore. All rights reserved.</p>
            <div class="flex space-x-4 text-slate-400 text-base">
                <a href="https://wa.me/923034812714" target="_blank" class="hover:text-blue-400"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="#home" class="hover:text-blue-400"><i class="fa-solid fa-arrow-up"></i></a>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        const phones = [
            {
                id: 1,
                name: "iPhone 13 Pro (Used - 90% Battery)",
                category: "Used Phone",
                price: 215000,
                image: "https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?auto=format&fit=crop&w=500&q=80",
                desc: "Pristine condition JV/Factory Unlocked iPhone 13 Pro. Clean body, Face ID working, PTA approved."
            },
            {
                id: 2,
                name: "Samsung Galaxy S22 Ultra (Used)",
                category: "Used Phone",
                price: 185000,
                image: "https://images.unsplash.com/photo-1610945265064-0e34e5519bbf?auto=format&fit=crop&w=500&q=80",
                desc: "Flagship performance with S-Pen included. Scratchless screen and excellent battery backup."
            },
            {
                id: 3,
                name: "Infinix Hot 40 Pro (Brand New)",
                category: "New Phone",
                price: 45999,
                image: "https://images.unsplash.com/photo-1598327105666-5b89351aff97?auto=format&fit=crop&w=500&q=80",
                desc: "Official PTA approved brand new smartphone with 8GB RAM, 256GB storage, and 120Hz display."
            },
            {
                id: 4,
                name: "Tecno Spark 20 Pro (Brand New)",
                category: "New Phone",
                price: 41999,
                image: "https://images.unsplash.com/photo-1565849904461-04a58ad377e0?auto=format&fit=crop&w=500&q=80",
                desc: "Stylish design with massive storage, smooth gaming processor, and 108MP ultra-clear camera."
            }
        ];

        const accessories = [
            {
                id: 5,
                name: "65W Fast PD Charger Adapter",
                category: "Charger & Adapter",
                price: 2499,
                image: "https://images.unsplash.com/photo-1583863788434-e58a36330cf0?auto=format&fit=crop&w=500&q=80",
                desc: "Ultra-fast Type-C wall charger with multiple safety protections. Charges phones and laptops rapidly."
            },
            {
                id: 6,
                name: "Magnetic Car Phone Holder",
                category: "Holder",
                price: 899,
                image: "https://images.unsplash.com/photo-1584438784894-089d6a62b8fa?auto=format&fit=crop&w=500&q=80",
                desc: "Sturdy dashboard mount with strong magnetic grip. 360-degree rotation for easy navigation while driving."
            },
            {
                id: 7,
                name: "Heavy Duty Braided Type-C Cable",
                category: "Cable",
                price: 499,
                image: "https://images.unsplash.com/photo-1544652478-6553e5828a23?auto=format&fit=crop&w=500&q=80",
                desc: "Tangle-free nylon braided fast charging and data transfer cable. Durable connectors built to last."
            },
            {
                id: 8,
                name: "Stainless Steel SIM Ejector Pin Set",
                category: "Pins",
                price: 150,
                image: "https://images.unsplash.com/photo-1526738549149-8e07eca6c147?auto=format&fit=crop&w=500&q=80",
                desc: "Pack of 3 premium stainless steel SIM tray removal pins. Compact and reliable pocket tool."
            },
            {
                id: 9,
                name: "Transparent Shockproof Silicon Pouch",
                category: "Pouch",
                price: 399,
                image: "https://images.unsplash.com/photo-1601784551446-20c9e07cdbdb?auto=format&fit=crop&w=500&q=80",
                desc: "Crystal clear anti-yellowing silicon back cover with reinforced air-cushion corners for drop protection."
            },
            {
                id: 10,
                name: "Bluetooth Wireless Soundbar Speaker",
                category: "Speaker",
                price: 2999,
                image: "https://images.unsplash.com/photo-1545454675-3531b543be5d?auto=format&fit=crop&w=500&q=80",
                desc: "Powerful stereo bass wireless speaker with Bluetooth 5.0, FM radio, AUX, and TF card support."
            },
            {
                id: 11,
                name: "Smart Touch AMOLED Smartwatch",
                category: "Touch Watch",
                price: 3499,
                image: "https://images.unsplash.com/photo-1508685096489-7aacd43bd3b1?auto=format&fit=crop&w=500&q=80",
                desc: "Fitness tracking, heart rate monitor, Bluetooth calling, and vibrant touch screen display with extra strap."
            }
        ];

        let cart = [];

        function renderStore() {
            const phonesGrid = document.getElementById('phones-grid');
            const accessoriesGrid = document.getElementById('accessories-grid');

            phonesGrid.innerHTML = phones.map(p => productCardHTML(p)).join('');
            accessoriesGrid.innerHTML = accessories.map(a => productCardHTML(a)).join('');
        }

        function productCardHTML(p) {
            return `
                <div class="bg-slate-900 rounded-2xl border border-slate-800 overflow-hidden flex flex-col justify-between shadow-md hover:border-blue-500/50 transition">
                    <div>
                        <div class="relative h-44 sm:h-52 overflow-hidden bg-slate-950">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover hover:scale-105 transition duration-300">
                            <span class="absolute top-2 left-2 bg-blue-950/90 text-blue-300 text-[10px] font-semibold px-2.5 py-1 rounded-full border border-blue-800">${p.category}</span>
                        </div>
                        <div class="p-3 sm:p-4">
                            <h3 class="font-bold text-sm sm:text-base text-white mb-1 line-clamp-1">${p.name}</h3>
                            <p class="text-xs text-slate-300 line-clamp-3 mb-3 leading-relaxed">${p.desc}</p>
                        </div>
                    </div>
                    <div class="p-3 sm:p-4 pt-0 flex items-center justify-between border-t border-slate-800/80 mt-auto">
                        <span class="font-bold text-blue-400 text-sm sm:text-base">Rs. ${p.price.toLocaleString()}</span>
                        <button onclick="addToCart(${p.id})" class="bg-blue-600 hover:bg-blue-500 text-white text-xs font-semibold px-3 py-2 rounded-xl transition flex items-center shadow">
                            <i class="fa-solid fa-plus mr-1"></i> Add
                        </button>
                    </div>
                </div>
            `;
        }

        function toggleSideMenu() {
            const menu = document.getElementById('sideMenu');
            const panel = document.getElementById('sideMenuPanel');
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('-translate-x-full'), 10);
            } else {
                panel.classList.add('-translate-x-full');
                setTimeout(() => menu.classList.add('hidden'), 300);
            }
        }

        function toggleCart() {
            const drawer = document.getElementById('cartDrawer');
            const panel = document.getElementById('cartPanel');
            if (drawer.classList.contains('hidden')) {
                drawer.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('translate-x-full'), 10);
            } else {
                panel.classList.add('translate-x-full');
                setTimeout(() => drawer.classList.add('hidden'), 300);
            }
        }

        function addToCart(id) {
            const allItems = [...phones, ...accessories];
            const product = allItems.find(p => p.id === id);
            const existing = cart.find(item => item.id === id);
            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...product, qty: 1 });
            }
            updateCartUI();
            toggleCart();
        }

        function changeQty(id, delta) {
            const item = cart.find(i => i.id === id);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    cart = cart.filter(i => i.id !== id);
                }
            }
            updateCartUI();
        }

        function updateCartUI() {
            const countEl = document.getElementById('cart-count');
            const itemsEl = document.getElementById('cart-items');
            const totalEl = document.getElementById('cart-total');

            const totalCount = cart.reduce((sum, item) => sum + item.qty, 0);
            countEl.innerText = totalCount;

            if (cart.length === 0) {
                itemsEl.innerHTML = `<p class="text-slate-500 text-center py-8 text-sm">Your cart is currently empty.</p>`;
                totalEl.innerText = "Rs. 0";
                return;
            }

            let totalPrice = 0;
            itemsEl.innerHTML = cart.map(item => {
                totalPrice += item.price * item.qty;
                return `
                    <div class="flex items-center justify-between bg-slate-800 p-3 rounded-xl border border-slate-700 text-sm">
                        <div class="flex-grow pr-2">
                            <h4 class="font-semibold text-white text-xs line-clamp-1">${item.name}</h4>
                            <p class="text-blue-400 text-xs">Rs. ${item.price.toLocaleString()} x ${item.qty}</p>
                        </div>
                        <div class="flex items-center space-x-2">
                            <button onclick="changeQty(${item.id}, -1)" class="bg-slate-700 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-slate-600">-</button>
                            <span class="text-xs font-bold text-white">${item.qty}</span>
                            <button onclick="changeQty(${item.id}, 1)" class="bg-slate-700 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-slate-600">+</button>
                        </div>
                    </div>
                `;
            }).join('');

            totalEl.innerText = `Rs. ${totalPrice.toLocaleString()}`;
        }

        function checkoutWhatsApp() {
            if (cart.length === 0) {
                alert("Your cart is empty! Please add items before checking out.");
                return;
            }

            let message = "Hello Hypermart Mobiles, I want to place an order:%0A%0A";
            let total = 0;

            cart.forEach((item, index) => {
                let sub = item.price * item.qty;
                total += sub;
                message += `${index + 1}. ${item.name} (Qty: ${item.qty}) - Rs. ${sub.toLocaleString()}%0A`;
            });

            message += `%0A*Total Bill: Rs. ${total.toLocaleString()}*%0A%0APayment Method: JazzCash / EasyPaisa / Cash on Delivery%0ADelivery Address: [Please provide your Lahore address here]`;

            const whatsappUrl = `https://wa.me/923034812714?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }

        window.onload = renderStore;
    </script>
</body>
</html>
