# Video-cash-farm
Make money watching videos 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Make Money by Watching YouTube Video Fans'</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #1e3a8a 0%, #581c87 100%);
            min-height: 100vh;
            color: white;
        }

        .glass-panel {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .card-hover {
            transition: all 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .money-glow {
            text-shadow: 0 0 10px rgba(52, 211, 153, 0.8);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: rgba(0,0,0,0.1); 
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(255,255,255,0.3); 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(255,255,255,0.5); 
        }

        .gradient-text {
            background: linear-gradient(to right, #34d399, #60a5fa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .animate-pulse-slow {
            animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        .floating-icon {
            animation: float 4s ease-in-out infinite;
        }
    </style>
</head>
<body class="antialiased overflow-x-hidden">

    <!-- Navigation Bar -->
    <nav class="glass-panel sticky top-0 z-50 px-6 py-4 shadow-lg">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-yellow-400 rounded-full flex items-center justify-center text-blue-900 font-bold text-xl shadow-lg floating-icon">
                    <i class="fas fa-play"></i>
                </div>
                <div>
                    <h1 class="text-xl font-bold tracking-wide">VideoFans<span class="text-green-400">Cash</span></h1>
                    <p class="text-xs text-gray-300">By Ugo-Best💲</p>
                </div>
            </div>
            
            <!-- Search Box -->
            <div class="relative w-full md:w-1/3">
                <input type="text" id="searchInput" placeholder="Search platforms..." 
                    class="w-full px-5 py-2 rounded-full bg-white/10 border border-white/20 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-green-400 transition-all">
                <i class="fas fa-search absolute right-4 top-3 text-gray-400"></i>
            </div>

            <div class="flex items-center gap-4">
                <div class="hidden md:flex flex-col items-end">
                    <span class="text-xs text-gray-300">Current Balance</span>
                    <span class="font-bold text-green-400 text-lg">₦<span id="navBalance">0.00</span></span>
                </div>
                <button onclick="toggleWallet()" class="bg-green-500 hover:bg-green-600 text-white px-6 py-2 rounded-full font-bold shadow-lg transition-transform transform hover:scale-105 flex items-center gap-2">
                    <i class="fas fa-wallet"></i> Withdraw
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 py-8 space-y-12">

        <!-- Hero / Stats Section -->
        <section class="text-center py-10 relative">
            <div class="absolute top-0 left-1/2 transform -translate-x-1/2 w-full h-full bg-blue-500/20 blur-3xl -z-10 rounded-full"></div>
            <h2 class="text-4xl md:text-6xl font-extrabold mb-4">Make Money Watching <span class="gradient-text">YouTube Videos</span></h2>
            <p class="text-xl text-gray-200 mb-8">The #1 Platform for Video Fans in Nigeria & Worldwide</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto">
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-yellow-400 mb-1">₦2,000</div>
                    <div class="text-sm text-gray-300">Per 30s Video</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-blue-400 mb-1">Instant</div>
                    <div class="text-sm text-gray-300">Opay Withdrawal</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-green-400 mb-1">100%</div>
                    <div class="text-sm text-gray-300">Free Registration</div>
                </div>
            </div>
        </section>

        <!-- Main Platforms Section -->
        <section id="main-platforms">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Main Platforms</h3>
                    <p class="text-sm text-gray-400">Top earning opportunities</p>
                </div>
                <i class="fas fa-crown text-yellow-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="mainPlatformsGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- Essential for Video Fans Section -->
        <section id="essential-fans">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Essential for Video Fans</h3>
                    <p class="text-sm text-gray-400">Tools to boost your earnings</p>
                </div>
                <i class="fas fa-star text-purple-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="essentialGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- Comics and Light Novels Section -->
        <section id="comics-novels">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Comics & Light Novels</h3>
                    <p class="text-sm text-gray-400">Read & Watch to earn</p>
                </div>
                <i class="fas fa-book-open text-pink-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="comicsGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- International Resources Section -->
        <section id="international-resources">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">International Resources</h3>
                    <p class="text-sm text-gray-400">Global earning streams</p>
                </div>
                <i class="fas fa-globe text-blue-300 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="internationalGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

    </main>

    <!-- Wallet Modal -->
    <div id="walletModal" class="fixed inset-0 z-[100] hidden">
        <div class="absolute inset-0 bg-black/80 backdrop-blur-sm" onclick="toggleWallet()"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-full max-w-md p-4">
            <div class="glass-panel bg-gray-900 rounded-2xl p-6 shadow-2xl border border-green-500/30">
                <div class="flex justify-between items-center mb-6">
                    <h3 class="text-2xl font-bold text-white">My Wallet</h3>
                    <button onclick="toggleWallet()" class="text-gray-400 hover:text-white"><i class="fas fa-times text-xl"></i></button>
                </div>
                
                <div class="bg-gradient-to-r from-green-600 to-green-800 rounded-xl p-6 mb-6 text-center relative overflow-hidden">
                    <div class="absolute top-0 right-0 -mt-4 -mr-4 w-24 h-24 bg-white/10 rounded-full blur-xl"></div>
                    <p class="text-green-100 text-sm mb-1">Available Balance</p>
                    <h2 class="text-4xl font-bold text-white mb-2">₦<span id="walletBalance">0.00</span></h2>
                    <span class="inline-block px-3 py-1 bg-black/20 rounded-full text-xs text-green-100">Instant Withdrawal Active</span>
                </div>

                <div class="space-y-4">
                    <div>
                        <label class="block text-sm text-gray-400 mb-1">Opay Account Number</label>
                        <input type="number" placeholder="Enter 11 digit number" class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:border-green-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-sm text-gray-400 mb-1">Amount to Withdraw</label>
                        <input type="number" id="withdrawAmount" placeholder="Min ₦1000" class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:border-green-500 focus:outline-none">
                    </div>
                    <button onclick="processWithdrawal()" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-3 rounded-lg transition-colors shadow-lg shadow-green-500/20">
                        Withdraw to Opay
                    </button>
                </div>
                <p class="text-xs text-center text-gray-500 mt-4"><i class="fas fa-lock"></i> Secured by Ugo-Best💲 Financial Services</p>
            </div>
        </div>
    </div>

    <!-- Video Player Modal -->
    <div id="videoModal" class="fixed inset-0 z-[100] hidden flex items-center justify-center">
        <div class="absolute inset-0 bg-black/90 backdrop-blur-md" onclick="closeVideo()"></div>
        <div class="relative w-full max-w-4xl bg-black rounded-xl overflow-hidden shadow-2xl border border-gray-800 m-4">
            <div class="aspect-video bg-gray-900 flex items-center justify-center relative group">
                <!-- Simulated Video Content -->
                <div id="videoLoader" class="text-center">
                    <i class="fas fa-circle-notch fa-spin text-4xl text-red-600 mb-4"></i>
                    <p class="text-gray-400">Loading Advertisement...</p>
                </div>
                
                <div id="videoContent" class="hidden w-full h-full relative">
                    <img src="https://images.unsplash.com/photo-1611162617474-5b21e879e113?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover opacity-60" alt="Video Content">
                    <div class="absolute inset-0 flex items-center justify-center">
                        <div class="text-center">
                            <i class="fab fa-youtube text-6xl text-red-600 mb-2"></i>
                            <p class="text-white font-bold text-xl">Sponsored Content</p>
                        </div>
                    </div>
                    <!-- Progress Bar -->
                    <div class="absolute bottom-0 left-0 w-full h-2 bg-gray-700">
                        <div id="videoProgress" class="h-full bg-red-600 w-0 transition-all duration-[30000ms] ease-linear"></div>
                    </div>
                    <div class="absolute top-4 right-4 bg-black/70 px-3 py-1 rounded text-white text-sm">
                        <i class="fas fa-clock mr-1"></i> <span id="timer">30</span>s
                    </div>
                </div>
            </div>
            <div class="p-6 bg-gray-900 flex justify-between items-center">
                <div>
                    <h3 class="text-white font-bold text-lg" id="videoTitle">Watching Video...</h3>
                    <p class="text-gray-400 text-sm">Reward: ₦2,000.00</p>
                </div>
                <button id="claimBtn" disabled onclick="claimReward()" class="bg-gray-700 text-gray-400 font-bold py-2 px-6 rounded-lg cursor-not-allowed transition-all">
                    Claim Reward
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-white/10 bg-black/20 mt-12">
        <div class="max-w-7xl mx-auto px-4 py-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                <div class="text-center md:text-left">
                    <p class="text-sm text-gray-400">&copy; 2026 Ugo-Best💲 Entertainment. All rights reserved.</p>
                    <p class="text-xs text-gray-500 mt-1">Available in Nigeria and 150+ countries.</p>
                </div>
                <div class="flex gap-6 text-sm">
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">How to Earn</a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-5 right-5 transform translate-y-20 opacity-0 transition-all duration-300 z-[110] bg-white text-gray-900 px-6 py-4 rounded-lg shadow-2xl border-l-4 border-green-500 flex items-center gap-3">
        <i class="fas fa-check-circle text-green-500 text-xl"></i>
        <div>
            <h4 class="font-bold text-sm">Success</h4>
            <p class="text-xs text-gray-600" id="toastMsg">Operation completed.</p>
        </div>
    </div>

    <script>
        // --- Data Configuration ---
        const platformsData = {
            main: [
                { name: "YouTube Premium", icon: "fab fa-youtube", desc: "Watch high-value ads and trailers.", color: "text-red-500" },
                { name: "TikTok Rewards", icon: "fab fa-tiktok", desc: "Short videos, instant cash.", color: "text-white" },
                { name: "Netflix Previews", icon: "fas fa-film", desc: "Watch upcoming series trailers.", color: "text-red-600" },
                { name: "Vimeo Pro", icon: "fab fa-vimeo-v", desc: "Curated artistic content.", color: "text-blue-400" }
            ],
            essential: [
                { name: "Opay Wallet", icon: "fas fa-wallet", desc: "Secure your earnings instantly.", color: "text-green-500" },
                { name: "Data Saver", icon: "fas fa-wifi", desc: "Optimize streaming for less data.", color: "text-blue-300" },
                { name: "Time Tracker", icon: "fas fa-clock", desc: "Track your daily watch time.", color: "text-yellow-400" },
                { name: "Referral Hub", icon: "fas fa-users", desc: "Invite friends for ₦500 bonus.", color: "text-purple-400" }
            ],
            comics: [
                { name: "WebToon Cash", icon: "fas fa-book", desc: "Read comics, watch ads in-between.", color: "text-green-400" },
                { name: "Manga Plus", icon: "fas fa-dragon", desc: "Japanese content monetization.", color: "text-red-400" },
                { name: "Light Novel TV", icon: "fas fa-tv", desc: "Visual novel adaptations.", color: "text-pink-400" },
                { name: "Anime Clips", icon: "fas fa-ghost", desc: "Short anime episode reviews.", color: "text-indigo-400" }
            ],
            international: [
                { name: "USA Surveys", icon: "fas fa-flag-usa", desc: "High paying US market research.", color: "text-blue-500" },
                { name: "UK AdStream", icon: "fas fa-crown", desc: "British television trailers.", color: "text-yellow-600" },
                { name: "Global Crypto", icon: "fab fa-bitcoin", desc: "Earn crypto watching DeFi videos.", color: "text-orange-500" },
                { name: "Euro Vision", icon: "fas fa-euro-sign", desc: "European product launches.", color: "text-blue-600" }
            ]
        };

        // --- State Management ---
        let balance = 0.00;
        let isWatching = false;

        // --- Initialization ---
        document.addEventListener('DOMContentLoaded', () => {
            renderCards(platformsData.main, 'mainPlatformsGrid');
            renderCards(platformsData.essential, 'essentialGrid');
            renderCards(platformsData.comics, 'comicsGrid');
            renderCards(platformsData.international, 'internationalGrid');
            
            // Search Functionality
            document.getElementById('searchInput').addEventListener('input', (e) => {
                const term = e.target.value.toLowerCase();
                filterCards(term);
            });
        });

        // --- Rendering Logic ---
        function renderCards(data, containerId) {
            const container = document.getElementById(containerId);
            container.innerHTML = data.map(item => `
                <div class="glass-panel p-6 rounded-xl card-hover cursor-pointer group relative overflow-hidden" onclick="openVideo('${item.name}')">
                    <div class="absolute top-0 right-0 p-4 opacity-10 group-hover:opacity-20 transition-opacity">
                        <i class="${item.icon} text-6xl ${item.color}"></i>
                    </div>
                    <div class="relative z-10">
                        <div class="w-12 h-12 rounded-lg bg-white/10 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
                            <i class="${item.icon} text-2xl ${item.color}"></i>
                        </div>
                        <h4 class="font-bold text-lg mb-2 text-white group-hover:text-green-300 transition-colors">${item.name}</h4>
                        <p class="text-sm text-gray-400 mb-4">${item.desc}</p>
                        <div class="flex items-center justify-between mt-4 pt-4 border-t border-white/10">
                            <span class="text-xs font-mono text-green-400">+₦2,000</span>
                            <span class="text-xs text-gray-500"><i class="fas fa-play-circle mr-1"></i> Watch</span>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        function filterCards(term) {
            const allSections = ['mainPlatformsGrid', 'essentialGrid', 'comicsGrid', 'internationalGrid'];
            const allData = [...platformsData.main, ...platformsData.essential, ...platformsData.comics, ...platformsData.international];
            
            // Simple global filter for demo purposes
            allSections.forEach((sectionId, index) => {
                const sectionData = Object.values(platformsData)[index];
                const filtered = sectionData.filter(item => 
                    item.name.toLowerCase().includes(term) || 
                    item.desc.toLowerCase().includes(term)
                );
                renderCards(filtered, sectionId);
                
                // Hide section if empty
                const sectionEl = document.getElementById(sectionId).parentElement;
                if(filtered.length === 0 && term !== '') {
                    sectionEl.style.display = 'none';
                } else {
                    sectionEl.style.display = 'block';
                }
            });
        }

        // --- Video Simulation Logic ---
        function openVideo(title) {
            if(isWatching) return;
            
            const modal = document.getElementById('videoModal');
            const loader = document.getElementById('videoLoader');
            const content = document.getElementById('videoContent');
            const claimBtn = document.getElementById('claimBtn');
            const progress = document.getElementById('videoProgress');
            const timer = document.getElementById('timer');
            
            document.getElementById('videoTitle').innerText = title;
            modal.classList.remove('hidden');
            
            // Reset State
            loader.classList.remove('hidden');
            content.classList.add('hidden');
            claimBtn.disabled = true;
            claimBtn.classList.add('bg-gray-700', 'text-gray-400', 'cursor-not-allowed');
            claimBtn.classList.remove('bg-green-500', 'text-white', 'hover:bg-green-600');
            claimBtn.innerText = "Watching...";
            progress.style.width = '0%';
            
            // Simulate Loading
            setTimeout(() => {
                loader.classList.add('hidden');
                content.classList.remove('hidden');
                isWatching = true;
                
                // Start Timer
                let timeLeft = 30;
                timer.innerText = timeLeft;
                
                // Animate Progress
                // Force reflow
                void progress.offsetWidth; 
                progress.style.width = '100%';

                const interval = setInterval(() => {
                    timeLeft--;
                    timer.innerText = timeLeft;
                    
                    if(timeLeft <= 0) {
                        clearInterval(interval);
                        enableClaim();
                    }
                }, 1000);
                
                // Store interval ID on the button to clear it if closed early (optional cleanup)
                claimBtn.dataset.intervalId = interval;
            }, 1500);
        }

        function enableClaim() {
            const claimBtn = document.getElementById('claimBtn');
            claimBtn.disabled = false;
            claimBtn.classList.remove('bg-gray-700', 'text-gray-400', 'cursor-not-allowed');
            claimBtn.classList.add('bg-green-500', 'text-white', 'hover:bg-green-600', 'cursor-pointer');
            claimBtn.innerText = "Claim ₦2,000";
            isWatching = false;
        }

        function closeVideo() {
            document.getElementById('videoModal').classList.add('hidden');
            isWatching = false;
        }

        function claimReward() {
            balance += 2000;
            updateBalanceUI();
            closeVideo();
            showToast(`₦2,000 added to your wallet!`);
        }

        // --- Wallet Logic ---
        function toggleWallet() {
            const modal = document.getElementById('walletModal');
            modal.classList.toggle('hidden');
            updateBalanceUI();
        }

        function updateBalanceUI() {
            document.getElementById('walletBalance').innerText = balance.toLocaleString('en-US', {minimumFractionDigits: 2});
            document.getElementById('navBalance').innerText = balance.toLocaleString('en-US', {minimumFractionDigits: 2});
        }

        function processWithdrawal() {
            const amountInput = document.getElementById('withdrawAmount');
            const amount = parseFloat(amountInput.value);
            
            if (!amount || amount <= 0) {
                showToast("Please enter a valid amount.");
                return;
            }
            
            if (amount < 1000) {
                showToast("Minimum withdrawal is ₦1,000.");
                return;
            }
            
            if (amount > balance) {
                showToast("Insufficient balance.");
                return;
            }
            
            // Simulate Processing
            const btn = event.target;
            const originalText = btn.innerText;
            btn.innerText = "Processing...";
            btn.disabled = true;
            
            setTimeout(() => {
                balance -= amount;
                updateBalanceUI();
                amountInput.value = '';
                btn.innerText = originalText;
                btn.disabled = false;
                toggleWallet(); // Close modal
                showToast(`₦${amount.toLocaleString()} withdrawn to Opay successfully!`);
            }, 2000);
        }

        // --- Utilities ---
        function showToast(message) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMsg').innerText = message;
            toast.classList.remove('translate-y-20', 'opacity-0');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Make Money by Watching YouTube Video Fans'</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #1e3a8a 0%, #581c87 100%);
            min-height: 100vh;
            color: white;
        }

        .glass-panel {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .card-hover {
            transition: all 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .money-glow {
            text-shadow: 0 0 10px rgba(52, 211, 153, 0.8);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: rgba(0,0,0,0.1); 
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(255,255,255,0.3); 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: rgba(255,255,255,0.5); 
        }

        .gradient-text {
            background: linear-gradient(to right, #34d399, #60a5fa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .animate-pulse-slow {
            animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        .floating-icon {
            animation: float 4s ease-in-out infinite;
        }
    </style>
</head>
<body class="antialiased overflow-x-hidden">

    <!-- Navigation Bar -->
    <nav class="glass-panel sticky top-0 z-50 px-6 py-4 shadow-lg">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-yellow-400 rounded-full flex items-center justify-center text-blue-900 font-bold text-xl shadow-lg floating-icon">
                    <i class="fas fa-play"></i>
                </div>
                <div>
                    <h1 class="text-xl font-bold tracking-wide">VideoFans<span class="text-green-400">Cash</span></h1>
                    <p class="text-xs text-gray-300">By Ugo-Best💲</p>
                </div>
            </div>
            
            <!-- Search Box -->
            <div class="relative w-full md:w-1/3">
                <input type="text" id="searchInput" placeholder="Search platforms..." 
                    class="w-full px-5 py-2 rounded-full bg-white/10 border border-white/20 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-green-400 transition-all">
                <i class="fas fa-search absolute right-4 top-3 text-gray-400"></i>
            </div>

            <div class="flex items-center gap-4">
                <div class="hidden md:flex flex-col items-end">
                    <span class="text-xs text-gray-300">Current Balance</span>
                    <span class="font-bold text-green-400 text-lg">₦<span id="navBalance">0.00</span></span>
                </div>
                <button onclick="toggleWallet()" class="bg-green-500 hover:bg-green-600 text-white px-6 py-2 rounded-full font-bold shadow-lg transition-transform transform hover:scale-105 flex items-center gap-2">
                    <i class="fas fa-wallet"></i> Withdraw
                </button>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 py-8 space-y-12">

        <!-- Hero / Stats Section -->
        <section class="text-center py-10 relative">
            <div class="absolute top-0 left-1/2 transform -translate-x-1/2 w-full h-full bg-blue-500/20 blur-3xl -z-10 rounded-full"></div>
            <h2 class="text-4xl md:text-6xl font-extrabold mb-4">Make Money Watching <span class="gradient-text">YouTube Videos</span></h2>
            <p class="text-xl text-gray-200 mb-8">The #1 Platform for Video Fans in Nigeria & Worldwide</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto">
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-yellow-400 mb-1">₦2,000</div>
                    <div class="text-sm text-gray-300">Per 30s Video</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-blue-400 mb-1">Instant</div>
                    <div class="text-sm text-gray-300">Opay Withdrawal</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl">
                    <div class="text-3xl font-bold text-green-400 mb-1">100%</div>
                    <div class="text-sm text-gray-300">Free Registration</div>
                </div>
            </div>
        </section>

        <!-- Main Platforms Section -->
        <section id="main-platforms">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Main Platforms</h3>
                    <p class="text-sm text-gray-400">Top earning opportunities</p>
                </div>
                <i class="fas fa-crown text-yellow-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="mainPlatformsGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- Essential for Video Fans Section -->
        <section id="essential-fans">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Essential for Video Fans</h3>
                    <p class="text-sm text-gray-400">Tools to boost your earnings</p>
                </div>
                <i class="fas fa-star text-purple-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="essentialGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- Comics and Light Novels Section -->
        <section id="comics-novels">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">Comics & Light Novels</h3>
                    <p class="text-sm text-gray-400">Read & Watch to earn</p>
                </div>
                <i class="fas fa-book-open text-pink-400 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="comicsGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

        <!-- International Resources Section -->
        <section id="international-resources">
            <div class="flex justify-between items-end mb-6 border-b border-white/10 pb-2">
                <div>
                    <h3 class="text-2xl font-bold text-white">International Resources</h3>
                    <p class="text-sm text-gray-400">Global earning streams</p>
                </div>
                <i class="fas fa-globe text-blue-300 text-2xl"></i>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="internationalGrid">
                <!-- Content injected by JS -->
            </div>
        </section>

    </main>

    <!-- Wallet Modal -->
    <div id="walletModal" class="fixed inset-0 z-[100] hidden">
        <div class="absolute inset-0 bg-black/80 backdrop-blur-sm" onclick="toggleWallet()"></div>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-full max-w-md p-4">
            <div class="glass-panel bg-gray-900 rounded-2xl p-6 shadow-2xl border border-green-500/30">
                <div class="flex justify-between items-center mb-6">
                    <h3 class="text-2xl font-bold text-white">My Wallet</h3>
                    <button onclick="toggleWallet()" class="text-gray-400 hover:text-white"><i class="fas fa-times text-xl"></i></button>
                </div>
                
                <div class="bg-gradient-to-r from-green-600 to-green-800 rounded-xl p-6 mb-6 text-center relative overflow-hidden">
                    <div class="absolute top-0 right-0 -mt-4 -mr-4 w-24 h-24 bg-white/10 rounded-full blur-xl"></div>
                    <p class="text-green-100 text-sm mb-1">Available Balance</p>
                    <h2 class="text-4xl font-bold text-white mb-2">₦<span id="walletBalance">0.00</span></h2>
                    <span class="inline-block px-3 py-1 bg-black/20 rounded-full text-xs text-green-100">Instant Withdrawal Active</span>
                </div>

                <div class="space-y-4">
                    <div>
                        <label class="block text-sm text-gray-400 mb-1">Opay Account Number</label>
                        <input type="number" placeholder="Enter 11 digit number" class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:border-green-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-sm text-gray-400 mb-1">Amount to Withdraw</label>
                        <input type="number" id="withdrawAmount" placeholder="Min ₦1000" class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:border-green-500 focus:outline-none">
                    </div>
                    <button onclick="processWithdrawal()" class="w-full bg-green-500 hover:bg-green-600 text-white font-bold py-3 rounded-lg transition-colors shadow-lg shadow-green-500/20">
                        Withdraw to Opay
                    </button>
                </div>
                <p class="text-xs text-center text-gray-500 mt-4"><i class="fas fa-lock"></i> Secured by Ugo-Best💲 Financial Services</p>
            </div>
        </div>
    </div>

    <!-- Video Player Modal -->
    <div id="videoModal" class="fixed inset-0 z-[100] hidden flex items-center justify-center">
        <div class="absolute inset-0 bg-black/90 backdrop-blur-md" onclick="closeVideo()"></div>
        <div class="relative w-full max-w-4xl bg-black rounded-xl overflow-hidden shadow-2xl border border-gray-800 m-4">
            <div class="aspect-video bg-gray-900 flex items-center justify-center relative group">
                <!-- Simulated Video Content -->
                <div id="videoLoader" class="text-center">
                    <i class="fas fa-circle-notch fa-spin text-4xl text-red-600 mb-4"></i>
                    <p class="text-gray-400">Loading Advertisement...</p>
                </div>
                
                <div id="videoContent" class="hidden w-full h-full relative">
                    <img src="https://images.unsplash.com/photo-1611162617474-5b21e879e113?q=80&w=1000&auto=format&fit=crop" class="w-full h-full object-cover opacity-60" alt="Video Content">
                    <div class="absolute inset-0 flex items-center justify-center">
                        <div class="text-center">
                            <i class="fab fa-youtube text-6xl text-red-600 mb-2"></i>
                            <p class="text-white font-bold text-xl">Sponsored Content</p>
                        </div>
                    </div>
                    <!-- Progress Bar -->
                    <div class="absolute bottom-0 left-0 w-full h-2 bg-gray-700">
                        <div id="videoProgress" class="h-full bg-red-600 w-0 transition-all duration-[30000ms] ease-linear"></div>
                    </div>
                    <div class="absolute top-4 right-4 bg-black/70 px-3 py-1 rounded text-white text-sm">
                        <i class="fas fa-clock mr-1"></i> <span id="timer">30</span>s
                    </div>
                </div>
            </div>
            <div class="p-6 bg-gray-900 flex justify-between items-center">
                <div>
                    <h3 class="text-white font-bold text-lg" id="videoTitle">Watching Video...</h3>
                    <p class="text-gray-400 text-sm">Reward: ₦2,000.00</p>
                </div>
                <button id="claimBtn" disabled onclick="claimReward()" class="bg-gray-700 text-gray-400 font-bold py-2 px-6 rounded-lg cursor-not-allowed transition-all">
                    Claim Reward
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-white/10 bg-black/20 mt-12">
        <div class="max-w-7xl mx-auto px-4 py-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                <div class="text-center md:text-left">
                    <p class="text-sm text-gray-400">&copy; 2026 Ugo-Best💲 Entertainment. All rights reserved.</p>
                    <p class="text-xs text-gray-500 mt-1">Available in Nigeria and 150+ countries.</p>
                </div>
                <div class="flex gap-6 text-sm">
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">How to Earn</a>
                    <a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-5 right-5 transform translate-y-20 opacity-0 transition-all duration-300 z-[110] bg-white text-gray-900 px-6 py-4 rounded-lg shadow-2xl border-l-4 border-green-500 flex items-center gap-3">
        <i class="fas fa-check-circle text-green-500 text-xl"></i>
        <div>
            <h4 class="font-bold text-sm">Success</h4>
            <p class="text-xs text-gray-600" id="toastMsg">Operation completed.</p>
        </div>
    </div>

    <script>
        // --- Data Configuration ---
        const platformsData = {
            main: [
                { name: "YouTube Premium", icon: "fab fa-youtube", desc: "Watch high-value ads and trailers.", color: "text-red-500" },
                { name: "TikTok Rewards", icon: "fab fa-tiktok", desc: "Short videos, instant cash.", color: "text-white" },
                { name: "Netflix Previews", icon: "fas fa-film", desc: "Watch upcoming series trailers.", color: "text-red-600" },
                { name: "Vimeo Pro", icon: "fab fa-vimeo-v", desc: "Curated artistic content.", color: "text-blue-400" }
            ],
            essential: [
                { name: "Opay Wallet", icon: "fas fa-wallet", desc: "Secure your earnings instantly.", color: "text-green-500" },
                { name: "Data Saver", icon: "fas fa-wifi", desc: "Optimize streaming for less data.", color: "text-blue-300" },
                { name: "Time Tracker", icon: "fas fa-clock", desc: "Track your daily watch time.", color: "text-yellow-400" },
                { name: "Referral Hub", icon: "fas fa-users", desc: "Invite friends for ₦500 bonus.", color: "text-purple-400" }
            ],
            comics: [
                { name: "WebToon Cash", icon: "fas fa-book", desc: "Read comics, watch ads in-between.", color: "text-green-400" },
                { name: "Manga Plus", icon: "fas fa-dragon", desc: "Japanese content monetization.", color: "text-red-400" },
                { name: "Light Novel TV", icon: "fas fa-tv", desc: "Visual novel adaptations.", color: "text-pink-400" },
                { name: "Anime Clips", icon: "fas fa-ghost", desc: "Short anime episode reviews.", color: "text-indigo-400" }
            ],
            international: [
                { name: "USA Surveys", icon: "fas fa-flag-usa", desc: "High paying US market research.", color: "text-blue-500" },
                { name: "UK AdStream", icon: "fas fa-crown", desc: "British television trailers.", color: "text-yellow-600" },
                { name: "Global Crypto", icon: "fab fa-bitcoin", desc: "Earn crypto watching DeFi videos.", color: "text-orange-500" },
                { name: "Euro Vision", icon: "fas fa-euro-sign", desc: "European product launches.", color: "text-blue-600" }
            ]
        };

        // --- State Management ---
        let balance = 0.00;
        let isWatching = false;

        // --- Initialization ---
        document.addEventListener('DOMContentLoaded', () => {
            renderCards(platformsData.main, 'mainPlatformsGrid');
            renderCards(platformsData.essential, 'essentialGrid');
            renderCards(platformsData.comics, 'comicsGrid');
            renderCards(platformsData.international, 'internationalGrid');
            
            // Search Functionality
            document.getElementById('searchInput').addEventListener('input', (e) => {
                const term = e.target.value.toLowerCase();
                filterCards(term);
            });
        });

        // --- Rendering Logic ---
        function renderCards(data, containerId) {
            const container = document.getElementById(containerId);
            container.innerHTML = data.map(item => `
                <div class="glass-panel p-6 rounded-xl card-hover cursor-pointer group relative overflow-hidden" onclick="openVideo('${item.name}')">
                    <div class="absolute top-0 right-0 p-4 opacity-10 group-hover:opacity-20 transition-opacity">
                        <i class="${item.icon} text-6xl ${item.color}"></i>
                    </div>
                    <div class="relative z-10">
                        <div class="w-12 h-12 rounded-lg bg-white/10 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
                            <i class="${item.icon} text-2xl ${item.color}"></i>
                        </div>
                        <h4 class="font-bold text-lg mb-2 text-white group-hover:text-green-300 transition-colors">${item.name}</h4>
                        <p class="text-sm text-gray-400 mb-4">${item.desc}</p>
                        <div class="flex items-center justify-between mt-4 pt-4 border-t border-white/10">
                            <span class="text-xs font-mono text-green-400">+₦2,000</span>
                            <span class="text-xs text-gray-500"><i class="fas fa-play-circle mr-1"></i> Watch</span>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        function filterCards(term) {
            const allSections = ['mainPlatformsGrid', 'essentialGrid', 'comicsGrid', 'internationalGrid'];
            const allData = [...platformsData.main, ...platformsData.essential, ...platformsData.comics, ...platformsData.international];
            
            // Simple global filter for demo purposes
            allSections.forEach((sectionId, index) => {
                const sectionData = Object.values(platformsData)[index];
                const filtered = sectionData.filter(item => 
                    item.name.toLowerCase().includes(term) || 
                    item.desc.toLowerCase().includes(term)
                );
                renderCards(filtered, sectionId);
                
                // Hide section if empty
                const sectionEl = document.getElementById(sectionId).parentElement;
                if(filtered.length === 0 && term !== '') {
                    sectionEl.style.display = 'none';
                } else {
                    sectionEl.style.display = 'block';
                }
            });
        }

        // --- Video Simulation Logic ---
        function openVideo(title) {
            if(isWatching) return;
            
            const modal = document.getElementById('videoModal');
            const loader = document.getElementById('videoLoader');
            const content = document.getElementById('videoContent');
            const claimBtn = document.getElementById('claimBtn');
            const progress = document.getElementById('videoProgress');
            const timer = document.getElementById('timer');
            
            document.getElementById('videoTitle').innerText = title;
            modal.classList.remove('hidden');
            
            // Reset State
            loader.classList.remove('hidden');
            content.classList.add('hidden');
            claimBtn.disabled = true;
            claimBtn.classList.add('bg-gray-700', 'text-gray-400', 'cursor-not-allowed');
            claimBtn.classList.remove('bg-green-500', 'text-white', 'hover:bg-green-600');
            claimBtn.innerText = "Watching...";
            progress.style.width = '0%';
            
            // Simulate Loading
            setTimeout(() => {
                loader.classList.add('hidden');
                content.classList.remove('hidden');
                isWatching = true;
                
                // Start Timer
                let timeLeft = 30;
                timer.innerText = timeLeft;
                
                // Animate Progress
                // Force reflow
                void progress.offsetWidth; 
                progress.style.width = '100%';

                const interval = setInterval(() => {
                    timeLeft--;
                    timer.innerText = timeLeft;
                    
                    if(timeLeft <= 0) {
                        clearInterval(interval);
                        enableClaim();
                    }
                }, 1000);
                
                // Store interval ID on the button to clear it if closed early (optional cleanup)
                claimBtn.dataset.intervalId = interval;
            }, 1500);
        }

        function enableClaim() {
            const claimBtn = document.getElementById('claimBtn');
            claimBtn.disabled = false;
            claimBtn.classList.remove('bg-gray-700', 'text-gray-400', 'cursor-not-allowed');
            claimBtn.classList.add('bg-green-500', 'text-white', 'hover:bg-green-600', 'cursor-pointer');
            claimBtn.innerText = "Claim ₦2,000";
            isWatching = false;
        }

        function closeVideo() {
            document.getElementById('videoModal').classList.add('hidden');
            isWatching = false;
        }

        function claimReward() {
            balance += 2000;
            updateBalanceUI();
            closeVideo();
            showToast(`₦2,000 added to your wallet!`);
        }

        // --- Wallet Logic ---
        function toggleWallet() {
            const modal = document.getElementById('walletModal');
            modal.classList.toggle('hidden');
            updateBalanceUI();
        }

        function updateBalanceUI() {
            document.getElementById('walletBalance').innerText = balance.toLocaleString('en-US', {minimumFractionDigits: 2});
            document.getElementById('navBalance').innerText = balance.toLocaleString('en-US', {minimumFractionDigits: 2});
        }

        function processWithdrawal() {
            const amountInput = document.getElementById('withdrawAmount');
            const amount = parseFloat(amountInput.value);
            
            if (!amount || amount <= 0) {
                showToast("Please enter a valid amount.");
                return;
            }
            
            if (amount < 1000) {
                showToast("Minimum withdrawal is ₦1,000.");
                return;
            }
            
            if (amount > balance) {
                showToast("Insufficient balance.");
                return;
            }
            
            // Simulate Processing
            const btn = event.target;
            const originalText = btn.innerText;
            btn.innerText = "Processing...";
            btn.disabled = true;
            
            setTimeout(() => {
                balance -= amount;
                updateBalanceUI();
                amountInput.value = '';
                btn.innerText = originalText;
                btn.disabled = false;
                toggleWallet(); // Close modal
                showToast(`₦${amount.toLocaleString()} withdrawn to Opay successfully!`);
            }, 2000);
        }

        // --- Utilities ---
        function showToast(message) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMsg').innerText = message;
            toast.classList.remove('translate-y-20', 'opacity-0');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }
    </script>
</body>
</html>
