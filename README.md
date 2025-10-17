<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khmer Music Collective - Media Center</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Configure Tailwind for custom colors and Inter font -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'primary-dark': '#111827', // Deep Dark Blue/Gray
                        'card-dark': '#1F2937',    // Slightly Lighter Card Background
                        'accent': '#6366F1',       // Indigo Accent
                        'accent-light': '#818CF8', // Lighter Indigo
                    }
                }
            }
        }
    </script>
    <style>
        /* Set default font and background */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* primary-dark */
            color: white;
            scroll-behavior: smooth;
        }
        /* Custom scrollbar styling (optional but nice touch for dark sites) */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-thumb {
            background: #4B5563;
            border-radius: 10px;
        }
        /* Aspect ratio container for the video player */
        .video-container {
            position: relative;
            width: 100%;
            padding-top: 56.25%; /* 16:9 Aspect Ratio */
            background-color: #000;
        }
        .video-container img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .video-play-button {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(255, 255, 255, 0.2);
            padding: 1rem;
            border-radius: 50%;
            transition: all 0.3s;
        }
        .video-container:hover .video-play-button {
            background-color: rgba(255, 255, 255, 0.4);
            transform: translate(-50%, -50%) scale(1.1);
        }
    </style>
</head>
<body class="antialiased">

    <!-- Navbar (Fixed Top) -->
    <header class="sticky top-0 z-50 bg-primary-dark/95 backdrop-blur-sm shadow-xl">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo/Brand -->
                <a href="#" class="flex-shrink-0 text-2xl font-bold text-accent hover:text-accent-light transition duration-300">
                    KMC <span class="text-white text-sm font-normal block -mt-1">Collective</span>
                </a>

                <!-- Desktop Navigation Links -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#artists" class="text-white hover:text-accent transition duration-150 py-2">Artists</a>
                    <a href="#music" class="text-white hover:text-accent transition duration-150 py-2">Music</a>
                    <a href="#videos" class="text-white hover:text-accent transition duration-150 py-2">Media Center</a>
                    <a href="#news" class="text-white hover:text-accent transition duration-150 py-2">News & Events</a>
                </nav>

                <!-- Mobile Menu Button (Hamburger) -->
                <button id="mobile-menu-button" class="md:hidden text-white p-2 rounded-md hover:bg-gray-800 transition duration-150">
                    <i data-lucide="menu" class="w-6 h-6"></i>
                </button>
            </div>
        </div>
        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-primary-dark/95 border-t border-gray-700">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#artists" class="block px-3 py-2 rounded-md text-base font-medium text-white hover:bg-gray-700 hover:text-accent">Artists</a>
                <a href="#music" class="block px-3 py-2 rounded-md text-base font-medium text-white hover:bg-gray-700 hover:text-accent">Music</a>
                <a href="#videos" class="block px-3 py-2 rounded-md text-base font-medium text-white hover:bg-gray-700 hover:text-accent">Media Center</a>
                <a href="#news" class="block px-3 py-2 rounded-md text-base font-medium text-white hover:bg-gray-700 hover:text-accent">News & Events</a>
            </div>
        </div>
    </header>

    <main>
        <!-- 1. Hero Section -->
        <section class="relative h-[60vh] md:h-[80vh] flex items-center justify-center overflow-hidden bg-cover bg-center" 
                 style="background-image: url('https://placehold.co/1200x800/2A3749/EFEFEF?text=Sound+of+New+Cambodia');">
            
            <!-- Dark Overlay for Readability -->
            <div class="absolute inset-0 bg-primary-dark opacity-60"></div>

            <!-- Content -->
            <div class="relative z-10 text-center px-4 max-w-4xl">
                <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight mb-4 leading-tight">
                    The Pulse of <span class="text-accent-light">New Khmer Music</span>
                </h1>
                <p class="text-lg sm:text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
                    Breaking boundaries and blending tradition with modern, globally-inspired sounds from Phnom Penh.
                </p>
                <a href="#videos" class="inline-flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-full text-white bg-accent hover:bg-indigo-700 shadow-lg shadow-indigo-500/50 transition duration-300 transform hover:scale-[1.02]">
                    <i data-lucide="monitor-play" class="w-5 h-5 mr-2"></i>
                    Watch Videos
                </a>
            </div>
        </section>

        <!-- 2. Featured Artists -->
        <section id="artists" class="py-16 md:py-24 bg-primary-dark">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 border-b-2 border-accent inline-block pb-2">Featured Artists</h2>
                
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6 lg:gap-8">
                    
                    <!-- Artist Card 1 -->
                    <div class="group rounded-xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:-translate-y-1 bg-card-dark">
                        <img src="https://placehold.co/600x600/374151/FFFFFF?text=Artist+A" onerror="this.onerror=null;this.src='https://placehold.co/600x600/374151/FFFFFF?text=Artist+A';" alt="Sovannary" class="w-full h-48 object-cover group-hover:opacity-80 transition duration-300">
                        <div class="p-4 text-center">
                            <h3 class="text-lg font-semibold text-white group-hover:text-accent transition duration-150">Sovannary</h3>
                            <p class="text-sm text-gray-400">Hip Hop / Pop</p>
                        </div>
                    </div>

                    <!-- Artist Card 2 -->
                    <div class="group rounded-xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:-translate-y-1 bg-card-dark">
                        <img src="https://placehold.co/600x600/374151/FFFFFF?text=Artist+B" onerror="this.onerror=null;this.src='https://placehold.co/600x600/374151/FFFFFF?text=Artist+B';" alt="Sokha" class="w-full h-48 object-cover group-hover:opacity-80 transition duration-300">
                        <div class="p-4 text-center">
                            <h3 class="text-lg font-semibold text-white group-hover:text-accent transition duration-150">Sokha</h3>
                            <p class="text-sm text-gray-400">Indie Rock</p>
                        </div>
                    </div>

                    <!-- Artist Card 3 -->
                    <div class="group rounded-xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:-translate-y-1 bg-card-dark">
                        <img src="https://placehold.co/600x600/374151/FFFFFF?text=Artist+C" onerror="this.onerror=null;this.src='https://placehold.co/600x600/374151/FFFFFF?text=Artist+C';" alt="DJ Vibe" class="w-full h-48 object-cover group-hover:opacity-80 transition duration-300">
                        <div class="p-4 text-center">
                            <h3 class="text-lg font-semibold text-white group-hover:text-accent transition duration-150">DJ Vibe</h3>
                            <p class="text-sm text-gray-400">Electronic / EDM</p>
                        </div>
                    </div>

                    <!-- Artist Card 4 -->
                    <div class="group rounded-xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:-translate-y-1 bg-card-dark">
                        <img src="https://placehold.co/600x600/374151/FFFFFF?text=Artist+D" onerror="this.onerror=null;this.src='https://placehold.co/600x600/374151/FFFFFF?text=Artist+D';" alt="Khmer Soul" class="w-full h-48 object-cover group-hover:opacity-80 transition duration-300">
                        <div class="p-4 text-center">
                            <h3 class="text-lg font-semibold text-white group-hover:text-accent transition duration-150">Khmer Soul</h3>
                            <p class="text-sm text-gray-400">Traditional Fusion</p>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-12">
                    <a href="#" class="inline-flex items-center text-accent-light hover:text-white font-medium transition duration-300">
                        View All Roster 
                        <i data-lucide="arrow-right" class="w-4 h-4 ml-1"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- 3. Latest Releases (Music) -->
        <section id="music" class="py-16 md:py-24 bg-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 border-b-2 border-accent inline-block pb-2">Latest Releases</h2>
                
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                    
                    <!-- Release Card 1 -->
                    <div class="bg-card-dark p-6 rounded-xl shadow-xl hover:bg-gray-700 transition duration-300">
                        <div class="flex items-start space-x-4">
                            <img src="https://placehold.co/150x150/4B5563/FFFFFF?text=Album+1" onerror="this.onerror=null;this.src='https://placehold.co/150x150/4B5563/FFFFFF?text=Album+1';" alt="Album Art" class="w-24 h-24 rounded-lg flex-shrink-0 shadow-lg">
                            <div class="flex-grow">
                                <p class="text-sm text-accent-light mb-1">Single | OCT 2025</p>
                                <h3 class="text-xl font-bold text-white mb-1 truncate">City Lights</h3>
                                <p class="text-gray-400 mb-3 truncate">By Sovannary</p>
                                <a href="#" class="text-sm font-medium text-white bg-accent px-3 py-1 rounded-full hover:bg-indigo-700 transition duration-150 flex items-center w-fit">
                                    <i data-lucide="play" class="w-3 h-3 mr-1"></i> Play
                                </a>
                            </div>
                        </div>
                    </div>
                    <!-- Release Card 2 -->
                    <div class="bg-card-dark p-6 rounded-xl shadow-xl hover:bg-gray-700 transition duration-300">
                        <div class="flex items-start space-x-4">
                            <img src="https://placehold.co/150x150/4B5563/FFFFFF?text=Album+2" onerror="this.onerror=null;this.src='https://placehold.co/150x150/4B5563/FFFFFF?text=Album+2';" alt="Album Art" class="w-24 h-24 rounded-lg flex-shrink-0 shadow-lg">
                            <div class="flex-grow">
                                <p class="text-sm text-accent-light mb-1">EP | SEP 2025</p>
                                <h3 class="text-xl font-bold text-white mb-1 truncate">Apsara's Dance</h3>
                                <p class="text-gray-400 mb-3 truncate">By Khmer Soul</p>
                                <a href="#" class="text-sm font-medium text-white bg-accent px-3 py-1 rounded-full hover:bg-indigo-700 transition duration-150 flex items-center w-fit">
                                    <i data-lucide="play" class="w-3 h-3 mr-1"></i> Play
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Release Card 3 -->
                    <div class="bg-card-dark p-6 rounded-xl shadow-xl hover:bg-gray-700 transition duration-300">
                        <div class="flex items-start space-x-4">
                            <img src="https://placehold.co/150x150/4B5563/FFFFFF?text=Album+3" onerror="this.onerror=null;this.src='https://placehold.co/150x150/4B5563/FFFFFF?text=Album+3';" alt="Album Art" class="w-24 h-24 rounded-lg flex-shrink-0 shadow-lg">
                            <div class="flex-grow">
                                <p class="text-sm text-accent-light mb-1">Album | AUG 2025</p>
                                <h3 class="text-xl font-bold text-white mb-1 truncate">Electric Dreams</h3>
                                <p class="text-gray-400 mb-3 truncate">By DJ Vibe</p>
                                <a href="#" class="text-sm font-medium text-white bg-accent px-3 py-1 rounded-full hover:bg-indigo-700 transition duration-150 flex items-center w-fit">
                                    <i data-lucide="play" class="w-3 h-3 mr-1"></i> Play
                                </a>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- 4. Media Center (Videos) -->
        <section id="videos" class="py-16 md:py-24 bg-primary-dark">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 border-b-2 border-accent inline-block pb-2">KMC Media Center</h2>

                <div class="flex flex-col lg:flex-row gap-8">
                    
                    <!-- Main Video Player and Info (2/3rds width on desktop) -->
                    <div class="lg:w-2/3">
                        <div class="bg-card-dark rounded-xl overflow-hidden shadow-2xl mb-6">
                            <!-- Video Placeholder -->
                            <div id="main-video-player" class="video-container">
                                <img id="video-thumbnail" src="https://placehold.co/1280x720/6366F1/FFFFFF?text=FEATURED+VIDEO+NOW" alt="Featured Video Thumbnail">
                                <div class="video-play-button cursor-pointer">
                                    <i data-lucide="play" class="w-12 h-12 text-white fill-current"></i>
                                </div>
                            </div>
                            <!-- Video Details -->
                            <div class="p-6">
                            <h3 id="video-title" class="text-2xl font-bold mb-2">City Lights (Official Music Video)</h3>
                                <p id="video-artist" class="text-accent-light text-lg mb-4">By Sovannary</p>
                                <p id="video-description" class="text-gray-400 text-sm">A mesmerizing visual journey through the streets of Phnom Penh at night, blending urban grit with traditional Khmer artistry. Directed by KMC Studio.</p>
                                <div class="flex items-center space-x-4 mt-4 text-sm text-gray-400">
                                    <span class="flex items-center"><i data-lucide="clock" class="w-4 h-4 mr-1"></i> 3:45</span>
                                    <span class="flex items-center"><i data-lucide="eye" class="w-4 h-4 mr-1"></i> 1.2M Views</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Video Playlist Sidebar (1/3rd width on desktop) -->
                    <div class="lg:w-1/3">
                        <h4 class="text-xl font-bold mb-4">More Videos</h4>
                        <div id="playlist-container" class="space-y-4 max-h-[80vh] overflow-y-auto pr-2">
                            <!-- Playlist Items are generated here -->
                        </div>
                    </div>
                </div>
            </div>
        </section>


        <!-- 5. Latest News & Events -->
        <section id="news" class="py-16 md:py-24 bg-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 border-b-2 border-accent inline-block pb-2">Latest News & Events</h2>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    
                    <!-- News Card 1 -->
                    <div class="bg-card-dark rounded-xl overflow-hidden shadow-xl">
                        <img src="https://placehold.co/800x450/253347/FFFFFF?text=Festival+Announcement" onerror="this.onerror=null;this.src='https://placehold.co/800x450/253347/FFFFFF?text=Festival+Announcement';" alt="News Image" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <p class="text-xs text-accent mb-2 uppercase tracking-wider">Event News</p>
                            <h3 class="text-xl font-semibold mb-3 hover:text-accent transition duration-150"><a href="#">KMC Artists Dominate Angkor Festival Lineup</a></h3>
                            <p class="text-gray-400 text-sm">Four of our top acts are confirmed to headline the main stage in Siem Reap next month...</p>
                        </div>
                    </div>

                    <!-- News Card 2 -->
                    <div class="bg-card-dark rounded-xl overflow-hidden shadow-xl">
                        <img src="https://placehold.co/800x450/253347/FFFFFF?text=New+Studio" onerror="this.onerror=null;this.src='https://placehold.co/800x450/253347/FFFFFF?text=New+Studio';" alt="News Image" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <p class="text-xs text-accent mb-2 uppercase tracking-wider">Industry Update</p>
                            <h3 class="text-xl font-semibold mb-3 hover:text-accent transition duration-150"><a href="#">New State-of-the-Art Recording Studio Opens</a></h3>
                            <p class="text-gray-400 text-sm">We've expanded our capabilities with a cutting-edge facility designed for modern production...</p>
                        </div>
                    </div>

                    <!-- News Card 3 -->
                    <div class="bg-card-dark rounded-xl overflow-hidden shadow-xl">
                    <img src="https://placehold.co/800x450/253347/FFFFFF?text=Interview" onerror="this.onerror=null;this.src='https://placehold.co/800x450/253347/FFFFFF?text=Interview';" alt="News Image" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <
