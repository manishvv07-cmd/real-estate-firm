<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shree Niwas Realty - Uma Gangeshwer Skyrise</title>
    
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    // Corporate colors directly from the logo (Deep Blue/Grey and Muted Gold)
                    colors: {
                        'primary': '#2C3540',    // Deep Blue/Grey from logo background
                        'secondary': '#AA8453',  // Muted Gold from logo graphic
                        'neutral-bg': '#F8F8F8', // Very light grey for contrast sections
                        'gold-dark': '#8A6B3F',  // Slightly darker gold for hover states
                        'text-light': '#D4D4D4', // Light text for dark backgrounds
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        /* Custom styles for professional look and mobile performance */
        .project-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(44, 53, 64, 0.2); /* Use primary for shadow */
        }
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: #AA8453; /* Muted Gold underline */
            margin: 10px auto 0;
            border-radius: 9999px;
        }
        .btn-primary {
            transition: background-color 0.3s, transform 0.1s;
        }
        .btn-primary:active {
            transform: scale(0.98);
        }
        /* Style for displaying images cleanly in a grid on large screens, stacked on mobile */
        .image-grid-item {
            display: block;
            width: 100%;
            height: auto;
            border-radius: 0.75rem; /* rounded-xl */
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
        }
        /* Loading spinner animation */
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .spinner {
            border: 4px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: #AA8453;
            width: 20px;
            height: 20px;
            animation: spin 1s ease-in-out infinite;
            display: inline-block;
            margin-right: 8px;
        }
    </style>
</head>
<body class="bg-neutral-bg font-sans text-gray-800">

    <!-- Sticky Header/Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo & Company Name (Image) -->
            <a href="#" class="flex items-center">
                <img src="uploaded:1000698215.jpg-bffe198a-624e-43f3-a675-cc3b3e5155bf"
                     onerror="this.onerror=null; this.src='https://placehold.co/150x50/2C3540/AA8453?text=Shree+Niwas+Realty';"
                     alt="Shree Niwas Realty Logo" 
                     class="h-10 w-auto object-contain rounded-lg border border-secondary">
            </a>

            <!-- Desktop Menu -->
            <nav class="hidden md:flex space-x-8 font-medium text-primary">
                <a href="#projects" class="hover:text-secondary transition duration-150">Our Project</a>
                <a href="#amenities" class="hover:text-secondary transition duration-150">Amenities</a>
                <a href="#details" class="hover:text-secondary transition duration-150">Floor Plans</a>
                <a href="#why-us" class="hover:text-secondary transition duration-150">Why Us</a>
                <a href="#contact" class="px-5 py-2 bg-secondary text-white rounded-lg shadow-lg hover:bg-gold-dark transition duration-150 font-semibold">
                    Inquire Now
                </a>
            </nav>

            <!-- Mobile Menu Button (Hamburger) -->
            <button id="mobile-menu-button" class="md:hidden text-primary hover:text-secondary p-2 rounded-lg transition duration-150">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
            </button>
        </div>

        <!-- Mobile Dropdown Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-xl py-2 px-4 border-t border-gray-100">
            <a href="#projects" class="block py-2 text-primary hover:bg-gray-50 rounded-md transition duration-150">Our Project</a>
            <a href="#amenities" class="block py-2 text-primary hover:bg-gray-50 rounded-md transition duration-150">Amenities</a>
            <a href="#details" class="block py-2 text-primary hover:bg-gray-50 rounded-md transition duration-150">Floor Plans</a>
            <a href="#why-us" class="block py-2 text-primary hover:bg-gray-50 rounded-md transition duration-150">Why Us</a>
            <a href="#contact" class="block py-2 mt-1 text-white bg-secondary hover:bg-gold-dark rounded-md transition duration-150 font-semibold text-center">Inquire Now</a>
        </div>
    </header>

    <!-- Hero Section / Project Highlight -->
    <section id="projects" class="relative bg-primary text-text-light py-16 sm:py-24 lg:py-32 overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center relative z-10">
            <!-- Tagline -->
            <p class="text-secondary text-lg sm:text-xl font-semibold mb-3 uppercase tracking-wider">
                Creating dreams into reality.
            </p>
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold mb-4 leading-tight">
                Uma Gangeshwer Skyrise
            </h1>
            <p class="text-lg sm:text-xl mb-8 opacity-90 max-w-2xl mx-auto">
                Discover modern living at Patherdi Phata, Nashik. Luxury apartments built with precision and care.
            </p>
            <div class="flex flex-col sm:flex-row justify-center items-center space-y-4 sm:space-y-0 sm:space-x-4">
                <a href="#contact" class="btn-primary bg-secondary text-white font-bold py-3 px-8 rounded-xl shadow-lg hover:shadow-xl hover:bg-gold-dark transition duration-300 text-lg w-full sm:w-auto">
                    Book Site Visit
                </a>
                <a href="#details" class="py-3 px-8 text-white border-2 border-white rounded-xl hover:bg-white hover:text-primary transition duration-300 font-medium text-lg w-full sm:w-auto">
                    View Floor Plans
                </a>
            </div>
        </div>
        <!-- Background wave (optional visual effect) -->
        <svg class="absolute bottom-0 w-full h-auto opacity-10" viewBox="0 0 1440 320" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
            <path fill="#2C3540" fill-opacity="1" d="M0,160L48,170.7C96,181,192,203,288,197.3C384,192,480,160,576,144C672,128,768,128,864,154.7C960,181,1056,235,1152,240C1248,245,1344,203,1392,181.3L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path>
        </svg>
    </section>

    <!-- Project Details & Image Showcase Section -->
    <section class="py-16 sm:py-20 lg:py-28 bg-neutral-bg">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <h2 class="section-title text-3xl sm:text-4xl font-extrabold text-center text-primary mb-16">
                Project Overview
            </h2>

            <!-- Grid for Project Image and Key Info -->
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-12">
                
                <!-- 1. Building Image -->
                <div class="lg:col-span-2">
                    <img src="uploaded:1000709402.png-f8d60eea-df16-4d38-8a93-0732bd901876" 
                         onerror="this.onerror=null; this.src='https://placehold.co/800x600/2C3540/AA8453?text=Building+Rendering+Image';"
                         alt="Uma Gangeshwer Skyrise Building Rendering" 
                         class="image-grid-item w-full h-full object-cover shadow-2xl">
                </div>

                <!-- 2. Key Details Box -->
                <div class="bg-white p-8 rounded-xl shadow-xl border-t-4 border-secondary flex flex-col justify-center">
                    <h3 class="text-2xl font-bold text-primary mb-6">Pricing & Availability</h3>
                    
                    <div class="space-y-4">
                        <div class="border-b pb-3 border-gray-200">
                            <p class="text-sm text-gray-500">Location</p>
                            <p class="font-semibold text-lg text-primary">Patherdi Phata, Nashik</p>
                        </div>
                        <div class="border-b pb-3 border-gray-200">
                            <p class="text-sm text-gray-500">Unit Type</p>
                            <p class="font-semibold text-lg text-primary">3 BHK Apartments</p>
                        </div>
                        <div class="border-b pb-3 border-gray-200">
                            <p class="text-sm text-gray-500">Carpet Area (Approx.)</p>
                            <p class="font-semibold text-lg text-primary">1625 sq.ft</p>
                        </div>
                        <div>
                            <p class="text-sm text-gray-500">Starting Price</p>
                            <p class="font-extrabold text-3xl text-secondary">₹ 75,00,000</p>
                            <p class="text-sm text-gray-600">+ Taxes Applicable</p>
                        </div>
                    </div>
                    
                    <a href="#contact" class="btn-primary w-full mt-8 py-3 bg-secondary text-white font-bold rounded-lg hover:bg-gold-dark transition duration-300 text-lg text-center">
                        Check Availability
                    </a>
                </div>
            </div>
            
            <!-- --- EXCLUSIVE AMENITIES SECTION --- -->
            <section id="amenities" class="pt-16">
                <h3 class="text-2xl sm:text-3xl font-extrabold text-center text-primary mb-12">Exclusive Amenities</h3>
                
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                    
                    <!-- Amenity 1: Power Backup -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2v10m0 10v-3m0-13h6a2 2 0 0 1 2 2v6a2 2 0 0 1-2 2h-6m0-10H6a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h6"/><path d="M10 10a2 2 0 1 1 4 0 2 2 0 0 1-4 0z"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">100% Power Backup</p>
                    </div>

                    <!-- Amenity 2: CCTV Surveillance -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 6L20 6A2 2 0 0 1 22 8L22 18A2 2 0 0 1 20 20L5 20A2 2 0 0 1 3 18L3 8A2 2 0 0 1 5 6z"/><circle cx="12" cy="13" r="3"/><line x1="17" x2="17.01" y1="10" y2="10"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">CCTV Security</p>
                    </div>
                    
                    <!-- Amenity 3: Modern Elevators -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2v20m-3-3l3 3 3-3m-3-14l3-3 3 3"/><rect width="18" height="18" x="3" y="3" rx="2"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">High-Speed Elevators</p>
                    </div>

                    <!-- Amenity 4: Dedicated Parking -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="18" height="12" x="3" y="10" rx="2"/><path d="M7 10v-4a2 2 0 0 1 2-2h6a2 2 0 0 1 2 2v4"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">Covered Parking</p>
                    </div>

                    <!-- Amenity 5: Fire Safety Systems -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2h-4a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2z"/><path d="M12 20v2m-3-2a3 3 0 0 0 6 0m-9-6h18m-9-8V2"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">Fire Safety Systems</p>
                    </div>
                    
                    <!-- Amenity 6: Intercom Facility -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 19c-2.3 0-5.7.5-8.5 2.5l-.2-.2C5 17.5 4 15 4 12V5a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v7c0 3-1 5.5-4.3 8.3z"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">Intercom Facility</p>
                    </div>

                    <!-- Amenity 7: Rainwater Harvesting -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 20V5m-4 4L12 5l4 4"/><path d="M2 14c0 3.73 3.32 6.8 7.55 7.93a1 1 0 0 0 .9 0C18.68 20.8 22 17.73 22 14c0-3.37-2.73-6-6-6-1.57 0-3.04.57-4 1.5-1.01-.93-2.43-1.5-4-1.5-3.27 0-6 2.63-6 6z"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">Rainwater Harvesting</p>
                    </div>
                    
                    <!-- Amenity 8: Grand Entrance -->
                    <div class="p-4 bg-white rounded-xl shadow-md border-b-4 border-secondary hover:shadow-lg transition duration-300">
                        <svg class="w-10 h-10 text-secondary mx-auto mb-3" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M10 12v.01m4-.01v.01m-4 4v.01m4-.01v.01m-2-18c-3.3 0-6 2.7-6 6v14h12V6c0-3.3-2.7-6-6-6z"/></svg>
                        <p class="font-semibold text-primary text-sm sm:text-base">Grand Entrance Lobby</p>
                    </div>
                </div>
            </section>
            <!-- END AMENITIES SECTION -->


            <!-- --- Floor Plans and Parking Section --- -->
            <div id="details" class="pt-24">
                <h3 class="text-2xl sm:text-3xl font-extrabold text-center text-primary mb-10">Detailed Floor Plans</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    
                    <!-- Floor Plan Image -->
                    <div class="bg-white p-4 rounded-xl shadow-lg">
                        <h4 class="text-xl font-bold text-primary mb-3 text-center">Typical Floor Layout (1625 sq.ft)</h4>
                        <img src="uploaded:1000710693.png-3ae4f7f4-6989-428c-915d-947fa5c30180" 
                             onerror="this.onerror=null; this.src='https://placehold.co/600x600/AA8453/2C3540?text=Floor+Plan+Image';"
                             alt="Floor Plan" 
                             class="image-grid-item">
                    </div>

                    <!-- Parking Plan Image -->
                    <div class="bg-white p-4 rounded-xl shadow-lg">
                        <h4 class="text-xl font-bold text-primary mb-3 text-center">Parking Level Layout</h4>
                        <img src="uploaded:1000710697.png-6f8d6bb0-ef6d-48cf-b34c-5accd2a42ed5" 
                             onerror="this.onerror=null; this.src='https://placehold.co/600x600/AA8453/2C3540?text=Parking+Plan+Image';"
                             alt="Parking Plan" 
                             class="image-grid-item">
                    </div>
                </div>
            </div>
            
        </div>
    </section>

    <!-- Why Choose Us Section (Builder Strengths) -->
    <section id="why-us" class="py-16 sm:py-20 lg:py-28 bg-white border-t border-b border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="section-title text-3xl sm:text-4xl font-extrabold text-center text-primary mb-16">The Shree Niwas Advantage</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Advantage Card 1: Quality & Materials -->
                <div class="p-6 bg-neutral-bg rounded-xl shadow-lg text-center hover:shadow-2xl transition duration-300 border-t-4 border-secondary">
                    <svg class="w-12 h-12 text-secondary mx-auto mb-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-2.5-2.5a6 6 0 0 0-7.94-7.94l3.77-3.77a1 1 0 0 0 0-1.4l1.6-1.6a1 1 0 0 0 1.4 0z"/><path d="m5.5 8.5 2 2"/></svg>
                    <h3 class="text-xl font-bold mb-3 text-primary">Superior Build Quality</h3>
                    <p class="text-gray-600">Committed to using high-grade, certified construction materials for lasting durability and safety.</p>
                </div>

                <!-- Advantage Card 2: Transparency & Delivery -->
                <div class="p-6 bg-neutral-bg rounded-xl shadow-lg text-center hover:shadow-2xl transition duration-300 border-t-4 border-primary">
                    <svg class="w-12 h-12 text-primary mx-auto mb-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="rou
