<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gold Reserve Token | Affordable Gold-Backed Cryptocurrency</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: {
                            50: '#fef9e7',
                            100: '#fdf2d0',
                            200: '#fbe5a1',
                            300: '#f9d872',
                            400: '#f7cb43',
                            500: '#f5be14',
                            600: '#c49810',
                            700: '#93720c',
                            800: '#624c08',
                            900: '#312604',
                        },
                        secondary: {
                            50: '#f3f4f6',
                            100: '#e5e7eb',
                            200: '#d1d5db',
                            300: '#9ca3af',
                            400: '#6b7280',
                            500: '#4b5563',
                            600: '#374151',
                            700: '#1f2937',
                            800: '#111827',
                            900: '#0a0e17',
                        }
                    },
                    fontFamily: {
                        'display': ['Playfair Display', 'serif'],
                        'body': ['Montserrat', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        .animate-fade-in {
            animation: fadeIn 0.8s ease-out forwards;
        }
        .animate-delay-1 { animation-delay: 0.2s; }
        .animate-delay-2 { animation-delay: 0.4s; }
        .animate-delay-3 { animation-delay: 0.6s; }
        .animate-float {
            animation: float 4s ease-in-out infinite;
        }
        
        .smooth-scroll {
            scroll-behavior: smooth;
        }
        .card-hover {
            transition: all 0.3s ease;
            transform: translateY(0);
        }
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px -12px rgba(245, 190, 20, 0.25);
        }
        .gradient-bg {
            background: linear-gradient(135deg, #0a0e17 0%, #1f2937 100%);
        }
        .gold-gradient {
            background: linear-gradient(135deg, #f5be14 0%, #c49810 100%);
        }
        .gold-text {
            background: linear-gradient(135deg, #f5be14 0%, #c49810 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            color: transparent;
        }
        .progress-bar {
            height: 10px;
            border-radius: 5px;
            background: #374151;
            overflow: hidden;
        }
        .progress-fill {
            height: 100%;
            background: linear-gradient(to right, #f5be14, #c49810);
            transition: width 1s ease-in-out;
        }
        .faq-item {
            border-bottom: 1px solid #374151;
        }
        .faq-question {
            cursor: pointer;
            transition: all 0.3s ease;
        }
        .faq-question:hover {
            color: #f5be14;
        }
        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease;
        }
        .faq-item.active .faq-answer {
            max-height: 500px;
        }
        .affordable-badge {
            position: absolute;
            top: -10px;
            right: -10px;
            background: linear-gradient(135deg, #4ade80, #22c55e);
            color: #0a0e17;
            font-weight: 700;
            padding: 5px 15px;
            border-radius: 20px;
            transform: rotate(5deg);
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            z-index: 10;
        }
        .value-box {
            background: rgba(245, 190, 20, 0.1);
            border: 1px solid rgba(245, 190, 20, 0.3);
            border-radius: 10px;
            padding: 15px;
            margin: 15px 0;
        }
        .security-badge {
            display: inline-block;
            padding: 8px 15px;
            background: rgba(22, 163, 74, 0.2);
            border: 1px solid rgba(22, 163, 74, 0.5);
            border-radius: 20px;
            margin: 5px;
        }
        .token-countdown {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
        }
        .countdown-box {
            background: rgba(245, 190, 20, 0.1);
            border: 1px solid rgba(245, 190, 20, 0.3);
            border-radius: 8px;
            padding: 10px;
            min-width: 70px;
            text-align: center;
        }
        .countdown-value {
            font-size: 1.8rem;
            font-weight: bold;
            color: #f5be14;
        }
        .countdown-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            opacity: 0.8;
        }
        .team-member {
            transition: all 0.3s ease;
        }
        .team-member:hover {
            transform: translateY(-5px);
        }
        .vault-location {
            position: relative;
            overflow: hidden;
            border-radius: 12px;
        }
        .vault-location::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(10, 14, 23, 0.7), rgba(10, 14, 23, 0.9));
            z-index: 1;
        }
        .vault-content {
            position: relative;
            z-index: 2;
        }
        .presale-timer {
            background: rgba(31, 41, 55, 0.7);
            border: 2px solid rgba(245, 190, 20, 0.3);
            border-radius: 16px;
            padding: 20px;
            text-align: center;
            margin-bottom: 30px;
        }
        .wallet-connected {
            background: linear-gradient(135deg, #22c55e, #16a34a) !important;
        }
        .affordable-highlight {
            position: relative;
            display: inline-block;
        }
        .affordable-highlight::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 30%;
            background: rgba(34, 197, 94, 0.3);
            z-index: -1;
            border-radius: 4px;
        }
        .affordable-banner {
            background: linear-gradient(90deg, #22c55e, #16a34a);
            color: #111827;
            padding: 10px 0;
            text-align: center;
            font-weight: 600;
            position: relative;
            overflow: hidden;
        }
        .affordable-banner::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                rgba(255,255,255,0.1) 10px,
                rgba(255,255,255,0.1) 20px
            );
        }
        .affordable-card {
            border: 2px solid #22c55e;
            position: relative;
            overflow: hidden;
        }
        .affordable-card::after {
            content: 'AFFORDABLE';
            position: absolute;
            top: 15px;
            right: -35px;
            background: #22c55e;
            color: #111827;
            font-size: 0.75rem;
            font-weight: bold;
            padding: 3px 40px;
            transform: rotate(45deg);
        }
        .value-badge {
            background: linear-gradient(135deg, #22c55e, #16a34a);
            color: #111827;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: 600;
            display: inline-block;
            margin: 5px 0;
        }
        .token-balance {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background: rgba(31, 41, 55, 0.9);
            border: 2px solid #f5be14;
            border-radius: 12px;
            padding: 15px;
            z-index: 100;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
            backdrop-filter: blur(10px);
            display: none;
        }
        .token-balance-header {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 10px;
        }
        .token-balance-icon {
            background: #f5be14;
            color: #111827;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
        }
        .token-balance-value {
            font-size: 1.5rem;
            font-weight: bold;
            color: #f5be14;
            text-align: center;
            margin-bottom: 5px;
        }
        .token-balance-label {
            text-align: center;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        .close-balance {
            position: absolute;
            top: 5px;
            right: 10px;
            cursor: pointer;
            opacity: 0.7;
        }
        .close-balance:hover {
            opacity: 1;
        }
        .purchase-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(10, 14, 23, 0.9);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 200;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
            backdrop-filter: blur(5px);
        }
        .purchase-modal.active {
            opacity: 1;
            pointer-events: all;
        }
        .modal-content {
            background: linear-gradient(135deg, #1f2937, #111827);
            border-radius: 16px;
            width: 90%;
            max-width: 500px;
            padding: 30px;
            position: relative;
            border: 1px solid #374151;
            box-shadow: 0 25px 50px -12px rgba(245, 190, 20, 0.25);
        }
        .modal-header {
            text-align: center;
            margin-bottom: 20px;
        }
        .modal-icon {
            background: #f5be14;
            color: #111827;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
            font-size: 24px;
        }
        .modal-close {
            position: absolute;
            top: 15px;
            right: 15px;
            cursor: pointer;
            opacity: 0.7;
            font-size: 20px;
        }
        .modal-close:hover {
            opacity: 1;
        }
        .modal-details {
            background: rgba(245, 190, 20, 0.1);
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
        }
        .modal-detail {
            display: flex;
            justify-content: space-between;
            padding: 8px 0;
            border-bottom: 1px solid rgba(245, 190, 20, 0.2);
        }
        .modal-detail:last-child {
            border-bottom: none;
        }
        .modal-button {
            width: 100%;
            padding: 15px;
            border-radius: 12px;
            background: #f5be14;
            color: #111827;
            font-weight: bold;
            font-size: 1.1rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 15px;
        }
        .modal-button:hover {
            background: #c49810;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(196, 152, 16, 0.4);
        }
        .modal-button:disabled {
            background: #374151;
            color: #9ca3af;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            padding: 15px 25px;
            border-radius: 12px;
            color: white;
            font-weight: 600;
            z-index: 300;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            display: flex;
            align-items: center;
            gap: 10px;
            transform: translateX(120%);
            transition: transform 0.3s ease;
        }
        .notification.show {
            transform: translateX(0);
        }
        .notification.success {
            background: linear-gradient(135deg, #22c55e, #16a34a);
        }
        .notification.error {
            background: linear-gradient(135deg, #ef4444, #dc2626);
        }
        .notification.info {
            background: linear-gradient(135deg, #3b82f6, #2563eb);
        }
        .gold-coin {
            position: absolute;
            top: 20%;
            right: 10%;
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: radial-gradient(circle at 30% 30%, #f5be14, #c49810);
            box-shadow: 0 0 30px rgba(245, 190, 20, 0.5);
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }
        .gold-coin.small {
            width: 50px;
            height: 50px;
            top: 60%;
            left: 15%;
            animation: float 5s ease-in-out infinite;
            animation-delay: 0.5s;
        }
        .gold-coin.medium {
            width: 65px;
            height: 65px;
            top: 15%;
            left: 20%;
            animation: float 7s ease-in-out infinite;
            animation-delay: 1s;
        }
        .gold-bar {
            position: absolute;
            bottom: 10%;
            right: 20%;
            width: 120px;
            height: 30px;
            background: linear-gradient(135deg, #f5be14, #c49810);
            box-shadow: 0 0 30px rgba(245, 190, 20, 0.5);
            z-index: 1;
            border-radius: 5px;
            animation: float 8s ease-in-out infinite;
            animation-delay: 1.5s;
        }
    </style>
</head>
<body class="gradient-bg text-gray-100 font-body smooth-scroll">
    <!-- Decorative floating gold elements -->
    <div class="gold-coin animate-float"></div>
    <div class="gold-coin small animate-float"></div>
    <div class="gold-coin medium animate-float"></div>
    <div class="gold-bar animate-float"></div>

    <!-- Affordable Banner -->
    <div class="affordable-banner animate-pulse">
        <div class="container mx-auto px-4 relative z-10">
            <i class="fas fa-badge-percent mr-2"></i> 
            NEW LOWER FEES & MINIMUM INVESTMENT! 
            <span class="font-bold ml-2">Start with just $10</span>
        </div>
    </div>

    <!-- Header -->
    <header class="bg-secondary-800 bg-opacity-90 backdrop-blur-sm shadow-lg sticky top-0 z-50">
        <nav class="container mx-auto px-4 py-3 flex flex-col md:flex-row justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="bg-primary-500 p-2 rounded-full">
                    <i class="fas fa-coins text-secondary-900 text-xl"></i>
                </div>
                <div>
                    <h1 class="text-xl font-bold font-display">GOLD RESERVE TOKEN</h1>
                    <p class="text-xs text-primary-400">Affordable Gold-Backed Cryptocurrency</p>
                </div>
            </div>
            <div class="mt-3 md:mt-0 flex flex-wrap justify-center gap-3 md:gap-5">
                <a href="#presale" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">Presale</a>
                <a href="#investment" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">Investment</a>
                <a href="#benefits" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">Benefits</a>
                <a href="#security" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">Security</a>
                <a href="#team" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">Team</a>
                <a href="#faq" class="hover:text-primary-500 transition-colors px-3 py-1 rounded hover:bg-secondary-700">FAQ</a>
            </div>
            <div class="mt-3 md:mt-0 flex items-center gap-3">
                <button id="connectWallet" class="gold-gradient text-secondary-900 px-5 py-2 rounded-full font-semibold hover:opacity-90 transition-opacity flex items-center gap-2">
                    <i class="fas fa-wallet"></i> <span id="walletText">Connect Wallet</span>
                </button>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="relative py-20 md:py-32 overflow-hidden">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-b from-secondary-900 via-secondary-900/90 to-secondary-900"></div>
            <div class="absolute inset-0 opacity-10" style="background-image: url('https://www.transparenttextures.com/patterns/diagmonds.png');"></div>
            <div class="absolute top-10 right-10 w-40 h-40 bg-primary-500 rounded-full filter blur-3xl opacity-20"></div>
            <div class="absolute bottom-20 left-10 w-60 h-60 bg-primary-500 rounded-full filter blur-3xl opacity-20"></div>
        </div>
        <div class="container mx-auto px-4 relative z-10 text-center">
            <div class="max-w-4xl mx-auto animate-fade-in">
                <div class="inline-block mb-6 px-4 py-2 bg-secondary-700 rounded-full text-primary-500 animate-pulse">
                    <i class="fas fa-bolt mr-2"></i><span>Presale Live - Limited Time Offer!</span>
                </div>
                <h1 class="text-4xl md:text-6xl font-display font-bold mb-6 leading-tight">
                    <span class="affordable-highlight">Affordable</span> <span class="gold-text">Gold-Backed</span> Crypto
                </h1>
                <p class="text-xl mb-8 opacity-90 max-w-2xl mx-auto">
                    Now more accessible than ever! Invest in physical gold with cryptocurrency convenience. 
                    <span class="font-bold text-primary-400">Start with just $10.</span>
                </p>
                <div class="flex flex-col sm:flex-row justify-center gap-4 animate-delay-1">
                    <a href="#presale" class="gold-gradient text-secondary-900 px-8 py-4 rounded-full font-semibold text-lg hover:opacity-90 transition-opacity flex items-center justify-center gap-2">
                        <i class="fas fa-gem"></i> Join Presale - From $10
                    </a>
                    <a href="#investment" class="border-2 border-primary-500 text-primary-500 px-8 py-4 rounded-full font-semibold text-lg hover:bg-primary-500 hover:text-secondary-900 transition-colors flex items-center justify-center gap-2">
                        <i class="fas fa-chart-line"></i> View Investment Plans
                    </a>
                </div>
                
                <div class="mt-12 grid grid-cols-2 md:grid-cols-4 gap-4 max-w-3xl mx-auto">
                    <div class="bg-secondary-800 p-4 rounded-lg border border-secondary-700">
                        <div class="text-2xl font-bold text-primary-500">$10</div>
                        <div class="text-sm opacity-80">Minimum Investment</div>
                    </div>
                    <div class="bg-secondary-800 p-4 rounded-lg border border-secondary-700">
                        <div class="text-2xl font-bold text-primary-500">75%↓</div>
                        <div class="text-sm opacity-80">Lower Fees</div>
                    </div>
                    <div class="bg-secondary-800 p-4 rounded-lg border border-secondary-700">
                        <div class="text-2xl font-bold text-primary-500">$5-10</div>
                        <div class="text-sm opacity-80">Gas Fees</div>
                    </div>
                    <div class="bg-secondary-800 p-4 rounded-lg border border-secondary-700">
                        <div class="text-2xl font-bold text-primary-500">24K</div>
                        <div class="text-sm opacity-80">Pure Gold</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Value Proposition -->
    <section class="py-16 bg-secondary-800">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Unbeatable Value</h2>
                <p class="max-w-2xl mx-auto opacity-80">We've made gold investment more accessible than ever</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-secondary-700 p-6 rounded-xl text-center card-hover animate-fade-in animate-delay-1">
                    <div class="inline-block bg-green-500 p-4 rounded-full mb-4">
                        <i class="fas fa-wallet text-2xl text-secondary-900"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Lower Minimum Investment</h3>
                    <p class="opacity-80 mb-4">Start your gold portfolio with just $10 instead of $50</p>
                    <div class="value-badge">SAVINGS: $40</div>
                </div>
                
                <div class="bg-secondary-700 p-6 rounded-xl text-center card-hover animate-fade-in animate-delay-2">
                    <div class="inline-block bg-green-500 p-4 rounded-full mb-4">
                        <i class="fas fa-gas-pump text-2xl text-secondary-900"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Reduced Gas Fees</h3>
                    <p class="opacity-80 mb-4">Transaction costs slashed from $15-30 to just $5-10</p>
                    <div class="value-badge">SAVINGS: 65-75%</div>
                </div>
                
                <div class="bg-secondary-700 p-6 rounded-xl text-center card-hover animate-fade-in animate-delay-3">
                    <div class="inline-block bg-green-500 p-4 rounded-full mb-4">
                        <i class="fas fa-percentage text-2xl text-secondary-900"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Lower Fees Overall</h3>
                    <p class="opacity-80 mb-4">Management fees reduced by 75% across all tiers</p>
                    <div class="value-badge">SAVINGS: 75%</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Investment Options -->
    <section id="investment" class="py-16">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Affordable Investment Options</h2>
                <p class="max-w-2xl mx-auto opacity-80">Start with just $10 and grow your gold portfolio</p>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Starter Tier -->
                <div class="bg-secondary-800 p-8 rounded-xl shadow-xl card-hover affordable-card relative animate-fade-in animate-delay-1">
                    <div class="affordable-badge">Best Value</div>
                    <div class="text-center mb-6">
                        <div class="inline-block bg-secondary-700 p-3 rounded-full mb-4">
                            <i class="fas fa-gem text-primary-500 text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Starter</h3>
                        <div class="text-2xl font-bold text-primary-500 mb-2">$10-49</div>
                        <p class="text-sm opacity-80">Perfect for first-time investors</p>
                    </div>
                    <ul class="space-y-3 mb-8">
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>5-24 GRT Tokens</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Basic Investor Status</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Email Updates</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Community Access</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>+5% Bonus Tokens</span>
                        </li>
                    </ul>
                    <button class="w-full bg-secondary-700 text-white py-3 rounded-lg hover:bg-primary-500 hover:text-secondary-900 transition-colors investment-btn" data-tier="starter">
                        Start Investing
                    </button>
                </div>
                
                <!-- Silver Tier -->
                <div class="bg-secondary-800 p-8 rounded-xl shadow-xl card-hover border-2 border-primary-500 relative animate-fade-in">
                    <div class="affordable-badge">Most Popular</div>
                    <div class="text-center mb-6">
                        <div class="inline-block bg-secondary-700 p-3 rounded-full mb-4">
                            <i class="fas fa-crown text-primary-500 text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Silver Tier</h3>
                        <div class="text-2xl font-bold text-primary-500 mb-2">$50-199</div>
                        <p class="text-sm opacity-80">Great for building your gold portfolio</p>
                    </div>
                    <ul class="space-y-3 mb-8">
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>25-99 GRT Tokens</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Priority Support</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Early Access to Features</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Silver NFT Badge</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>+15% Bonus Tokens</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Quarterly Reports</span>
                        </li>
                    </ul>
                    <button class="w-full gold-gradient text-secondary-900 py-3 rounded-lg font-semibold hover:opacity-90 transition-opacity investment-btn" data-tier="silver">
                        Select Plan
                    </button>
                </div>
                
                <!-- Gold Tier -->
                <div class="bg-secondary-800 p-8 rounded-xl shadow-xl card-hover relative animate-fade-in animate-delay-1">
                    <div class="affordable-badge">VIP Benefits</div>
                    <div class="text-center mb-6">
                        <div class="inline-block bg-secondary-700 p-3 rounded-full mb-4">
                            <i class="fas fa-medal text-primary-500 text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Gold Tier</h3>
                        <div class="text-2xl font-bold text-primary-500 mb-2">$200+</div>
                        <p class="text-sm opacity-80">For serious gold investors</p>
                    </div>
                    <ul class="space-y-3 mb-8">
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>100+ GRT Tokens</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>VIP Support</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Gold NFT Certificate</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Governance Voting Rights</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>+30% Bonus Tokens</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Exclusive Events</span>
                        </li>
                        <li class="flex items-center gap-2">
                            <i class="fas fa-check-circle text-primary-500"></i>
                            <span>Physical Gold Redemption</span>
                        </li>
                    </ul>
                    <button class="w-full bg-secondary-700 text-white py-3 rounded-lg hover:bg-primary-500 hover:text-secondary-900 transition-colors investment-btn" data-tier="gold">
                        Go Premium
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Presale Section -->
    <section id="presale" class="py-16 bg-secondary-800">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Token Presale</h2>
                <p class="max-w-2xl mx-auto opacity-80">Join our presale with exclusive pricing and bonuses</p>
            </div>
            
            <div class="max-w-4xl mx-auto bg-secondary-700 rounded-2xl p-8 animate-fade-in animate-delay-1">
                <div class="presale-timer">
                    <h3 class="text-xl font-semibold mb-2">Presale Ends In:</h3>
                    <div class="token-countdown">
                        <div class="countdown-box">
                            <div class="countdown-value" id="days">07</div>
                            <div class="countdown-label">Days</div>
                        </div>
                        <div class="countdown-box">
                            <div class="countdown-value" id="hours">16</div>
                            <div class="countdown-label">Hours</div>
                        </div>
                        <div class="countdown-box">
                            <div class="countdown-value" id="minutes">45</div>
                            <div class="countdown-label">Minutes</div>
                        </div>
                        <div class="countdown-box">
                            <div class="countdown-value" id="seconds">30</div>
                            <div class="countdown-label">Seconds</div>
                        </div>
                    </div>
                </div>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                    <div>
                        <div class="bg-secondary-800 p-6 rounded-xl mb-6">
                            <h3 class="text-xl font-semibold mb-4">Presale Information</h3>
                            <div class="space-y-4">
                                <div class="flex justify-between items-center">
                                    <span>Token Price:</span>
                                    <span class="font-semibold text-primary-500">$1.20 per GRT</span>
                                </div>
                                <div class="flex justify-between items-center">
                                    <span>Presale Progress:</span>
                                    <span class="font-semibold">72%</span>
                                </div>
                                <div class="flex justify-between items-center">
                                    <span>Tokens Sold:</span>
                                    <span class="font-semibold">3,600,000 GRT</span>
                                </div>
                                <div class="flex justify-between items-center">
                                    <span>Hard Cap:</span>
                                    <span class="font-semibold">5,000,000 GRT</span>
                                </div>
                                <div>
                                    <div class="progress-bar">
                                        <div class="progress-fill" id="presaleProgress" style="width: 72%;"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="bg-secondary-800 p-6 rounded-xl">
                            <h3 class="text-xl font-semibold mb-4">Presale Bonuses</h3>
                            <div class="space-y-4">
                                <div class="flex items-center justify-between p-3 bg-secondary-700 rounded-lg">
                                    <div>
                                        <span>First 24 hours:</span>
                                        <div class="text-xs opacity-70">Limited time only</div>
                                    </div>
                                    <span class="font-bold text-primary-500">+30% Bonus</span>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-secondary-700 rounded-lg">
                                    <div>
                                        <span>Week 1:</span>
                                        <div class="text-xs opacity-70">Ends in 3 days</div>
                                    </div>
                                    <span class="font-bold text-primary-500">+20% Bonus</span>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-secondary-700 rounded-lg">
                                    <span>Week 2:</span>
                                    <span class="font-bold text-primary-500">+15% Bonus</span>
                                </div>
                                <div class="flex items-center justify-between p-3 bg-secondary-700 rounded-lg">
                                    <span>Final week:</span>
                                    <span class="font-bold text-primary-500">+10% Bonus</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="bg-secondary-800 p-8 rounded-xl">
                        <div class="text-center mb-6">
                            <div class="inline-block bg-primary-500 px-4 py-1 rounded-full mb-2">
                                <span>Special Presale Pricing</span>
                            </div>
                            <h3 class="text-xl font-semibold">Buy Tokens</h3>
                        </div>
                        <div class="space-y-6">
                            <div>
                                <label class="block mb-2">Investment Amount (USD)</label>
                                <div class="relative">
                                    <input type="number" min="10" value="100" class="w-full p-4 bg-secondary-700 border border-secondary-600 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary-500" placeholder="$10 minimum" id="investmentAmount">
                                    <div class="absolute inset-y-0 right-0 flex items-center pr-4">
                                        <i class="fas fa-dollar-sign text-primary-500"></i>
                                    </div>
                                </div>
                                <div class="flex justify-between mt-2 text-sm opacity-80">
                                    <span>Min: $10</span>
                                    <span>Max: $5,000</span>
                                </div>
                            </div>
                            <div>
                                <label class="block mb-2">You Receive (GRT)</label>
                                <div class="relative">
                                    <input type="text" class="w-full p-4 bg-secondary-700 border border-secondary-600 rounded-lg focus:outline-none focus:ring-2 focus:ring-primary-500" readonly id="tokensReceived" value="108.33 GRT">
                                    <div class="absolute inset-y-0 right-0 flex items-center pr-4">
                                        <i class="fas fa-coins text-primary-500"></i>
                                    </div>
                                </div>
                            </div>
                            <div class="bg-secondary-700 p-4 rounded-lg">
                                <div class="flex justify-between mb-1">
                                    <span>Token Price:</span>
                                    <span>$1.20</span>
                                </div>
                                <div class="flex justify-between mb-1">
                                    <span>Estimated Gas Fee:</span>
                                    <span class="text-primary-500">$5-10</span>
                                </div>
                                <div class="flex justify-between">
                                    <span>Bonus Tokens:</span>
                                    <span class="text-primary-500">+30% (Limited Time)</span>
                                </div>
                            </div>
                            <button id="buyTokensBtn" class="w-full gold-gradient text-secondary-900 py-4 rounded-lg font-semibold text-lg hover:opacity-90 transition-opacity flex items-center justify-center gap-2">
                                <i class="fas fa-lock"></i> Buy Tokens Securely
                            </button>
                            <div class="text-center text-sm opacity-80 mt-4">
                                By purchasing, you agree to our <a href="#" class="text-primary-500 hover:underline">Terms of Service</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ -->
    <section id="faq" class="py-16">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Frequently Asked Questions</h2>
                <p class="max-w-2xl mx-auto opacity-80">Find answers to common questions about GRT</p>
            </div>
            <div class="max-w-3xl mx-auto space-y-4">
                <div class="faq-item bg-secondary-800 rounded-xl overflow-hidden animate-fade-in animate-delay-1">
                    <div class="faq-question p-6 flex justify-between items-center">
                        <h3 class="text-lg font-semibold">Why have you lowered prices and fees?</h3>
                        <i class="fas fa-chevron-down text-primary-500"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="p-6 pt-0">
                            <p>We want to make gold investment accessible to everyone. By optimizing our contracts and securing better vaulting agreements, we've reduced costs significantly. These savings are passed directly to our investors through lower token prices and reduced transaction fees.</p>
                            <div class="bg-green-900/20 p-4 rounded-lg mt-3 border border-green-700">
                                <i class="fas fa-badge-percent text-green-500 mr-2"></i>
                                <span class="font-semibold">Result:</span> 75% lower fees and $10 minimum investment
                            </div>
                        </div>
                    </div>
                </div>
                <div class="faq-item bg-secondary-800 rounded-xl overflow-hidden animate-fade-in animate-delay-2">
                    <div class="faq-question p-6 flex justify-between items-center">
                        <h3 class="text-lg font-semibold">What's the minimum investment?</h3>
                        <i class="fas fa-chevron-down text-primary-500"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="p-6 pt-0">
                            <p>You can now start investing with as little as $10. This gets you approximately 8 GRT tokens after bonuses (at current pricing). We've eliminated the previous $50 minimum to make gold investment truly accessible.</p>
                            <div class="value-badge mt-3">$10 minimum investment</div>
                        </div>
                    </div>
                </div>
                <div class="faq-item bg-secondary-800 rounded-xl overflow-hidden animate-fade-in animate-delay-3">
                    <div class="faq-question p-6 flex justify-between items-center">
                        <h3 class="text-lg font-semibold">How much are gas fees now?</h3>
                        <i class="fas fa-chevron-down text-primary-500"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="p-6 pt-0">
                            <p>Through contract optimizations, we've reduced gas fees by approximately 65%. Current fees range between $5-10 depending on network conditions, down from $15-30 for similar transactions.</p>
                            <div class="flex mt-3 gap-2">
                                <div class="bg-red-900/30 p-2 rounded flex-1 text-center">
                                    <div class="text-sm opacity-80">Old Fees</div>
                                    <div class="font-bold text-red-400">$15-30</div>
                                </div>
                                <div class="bg-green-900/30 p-2 rounded flex-1 text-center">
                                    <div class="text-sm opacity-80">New Fees</div>
                                    <div class="font-bold text-green-400">$5-10</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="faq-item bg-secondary-800 rounded-xl overflow-hidden animate-fade-in">
                    <div class="faq-question p-6 flex justify-between items-center">
                        <h3 class="text-lg font-semibold">Will token prices increase after presale?</h3>
                        <i class="fas fa-chevron-down text-primary-500"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="p-6 pt-0">
                            <p>Yes. The presale price is 40% below our planned public launch price of $2.00 per token. Additionally, the bonus tokens are only available during presale, making this the most cost-effective time to invest.</p>
                        </div>
                    </div>
                </div>
                <div class="faq-item bg-secondary-800 rounded-xl overflow-hidden animate-fade-in animate-delay-1">
                    <div class="faq-question p-6 flex justify-between items-center">
                        <h3 class="text-lg font-semibold">How is my gold secured?</h3>
                        <i class="fas fa-chevron-down text-primary-500"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="p-6 pt-0">
                            <p>Physical gold backing your tokens is stored in Class III vaults operated by Brink's, Loomis, and Malca-Amit. These facilities feature 24/7 monitoring, biometric access controls, and are fully insured against theft and damage.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="py-16">
        <div class="container mx-auto px-4">
            <div class="bg-gradient-to-r from-primary-600 to-primary-800 rounded-2xl p-12 text-center relative overflow-hidden">
                <div class="absolute inset-0 opacity-10" style="background-image: url('https://www.transparenttextures.com/patterns/diagmonds.png');"></div>
                <div class="relative z-10">
                    <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Start Your Gold Investment Journey Today</h2>
                    <p class="text-xl mb-8 max-w-2xl mx-auto">Join thousands of investors securing their wealth with gold-backed crypto at our most affordable prices ever.</p>
                    <div class="flex flex-col sm:flex-row justify-center gap-4">
                        <a href="#presale" class="inline-block bg-white text-secondary-900 px-8 py-4 rounded-full font-semibold text-lg hover:bg-gray-100 transition-colors">
                            <i class="fas fa-gem mr-2"></i> Join Presale - From $10
                        </a>
                        <a href="#investment" class="inline-block border-2 border-white text-white px-8 py-4 rounded-full font-semibold text-lg hover:bg-white hover:text-secondary-900 transition-colors">
                            <i class="fas fa-chart-line mr-2"></i> View Investment Plans
                        </a>
                    </div>
                    <div class="mt-8 flex flex-wrap justify-center gap-6">
                        <div class="flex items-center gap-2">
                            <div class="w-3 h-3 rounded-full bg-green-500"></div>
                            <span>Minimum investment: $10</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <div class="w-3 h-3 rounded-full bg-green-500"></div>
                            <span>Gas fees: $5-10</span>
                        </div>
                        <div class="flex items-center gap-2">
                            <div class="w-3 h-3 rounded-full bg-green-500"></div>
                            <span>75% lower fees</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-secondary-900 py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center gap-3 mb-4">
                        <div class="bg-primary-500 p-2 rounded-full">
                            <i class="fas fa-coins text-secondary-900"></i>
                        </div>
                        <h3 class="text-xl font-bold font-display">GOLD RESERVE TOKEN</h3>
                    </div>
                    <p class="opacity-80 mb-4">Making gold investment accessible and affordable through blockchain technology.</p>
                    <div class="flex gap-4">
                        <a href="#" class="bg-secondary-800 p-2 rounded-full hover:bg-primary-500 transition-colors">
                            <i class="fab fa-telegram"></i>
                        </a>
                        <a href="#" class="bg-secondary-800 p-2 rounded-full hover:bg-primary-500 transition-colors">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="bg-secondary-800 p-2 rounded-full hover:bg-primary-500 transition-colors">
                            <i class="fab fa-discord"></i>
                        </a>
                        <a href="#" class="bg-secondary-800 p-2 rounded-full hover:bg-primary-500 transition-colors">
                            <i class="fab fa-medium"></i>
                        </a>
                    </div>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Resources</h3>
                    <ul class="space-y-2">
                        <li><a href="#presale" class="opacity-80 hover:text-primary-500 transition-colors">Presale</a></li>
                        <li><a href="#investment" class="opacity-80 hover:text-primary-500 transition-colors">Investment Plans</a></li>
                        <li><a href="#benefits" class="opacity-80 hover:text-primary-500 transition-colors">Benefits</a></li>
                        <li><a href="#security" class="opacity-80 hover:text-primary-500 transition-colors">Security</a></li>
                        <li><a href="#faq" class="opacity-80 hover:text-primary-500 transition-colors">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Legal</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="opacity-80 hover:text-primary-500 transition-colors">Terms of Service</a></li>
                        <li><a href="#" class="opacity-80 hover:text-primary-500 transition-colors">Privacy Policy</a></li>
                        <li><a href="#" class="opacity-80 hover:text-primary-500 transition-colors">Disclaimer</a></li>
                        <li><a href="#" class="opacity-80 hover:text-primary-500 transition-colors">Audit Reports</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Contact</h3>
                    <ul class="space-y-3">
                        <li class="flex items-start gap-2">
                            <i class="fas fa-envelope text-primary-500 mt-1"></i>
                            <a href="mailto:contact@goldreservetoken.io" class="opacity-80 hover:text-primary-500 transition-colors">contact@goldreservetoken.io</a>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fab fa-telegram text-primary-500 mt-1"></i>
                            <a href="https://t.me/GoldReserveToken" class="opacity-80 hover:text-primary-500 transition-colors">t.me/GoldReserveToken</a>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fab fa-twitter text-primary-500 mt-1"></i>
                            <a href="https://x.com/GoldReserveToken" class="opacity-80 hover:text-primary-500 transition-colors">@GoldReserveToken</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="mt-12 pt-8 border-t border-secondary-700 text-center">
                <p class="opacity-70">© 2024 Gold Reserve Token. All rights reserved.</p>
                <p class="text-sm opacity-60 mt-2">This website is for demonstration purposes only. Cryptocurrency investments are volatile and high risk. Always do your own research.</p>
            </div>
        </div>
    </footer>

    <!-- Token balance display -->
    <div class="token-balance" id="tokenBalance">
        <span class="close-balance" id="closeBalance"><i class="fas fa-times"></i></span>
        <div class="token-balance-header">
            <div class="token-balance-icon">
                <i class="fas fa-coins"></i>
            </div>
            <h4>Your GRT Balance</h4>
        </div>
        <div class="token-balance-value" id="balanceValue">0.00</div>
        <div class="token-balance-label">GRT Tokens</div>
    </div>

    <!-- Purchase Modal -->
    <div class="purchase-modal" id="purchaseModal">
        <div class="modal-content">
            <span class="modal-close" id="closeModal"><i class="fas fa-times"></i></span>
            <div class="modal-header">
                <div class="modal-icon">
                    <i class="fas fa-coins"></i>
                </div>
                <h3 class="text-xl font-semibold">Confirm Token Purchase</h3>
            </div>
            
            <div class="modal-details">
                <div class="modal-detail">
                    <span>Amount:</span>
                    <span id="modalAmount">$0.00</span>
                </div>
                <div class="modal-detail">
                    <span>Tokens:</span>
                    <span id="modalTokens">0.00 GRT</span>
                </div>
                <div class="modal-detail">
                    <span>Gas Fee:</span>
                    <span id="modalGasFee">$0.00</span>
                </div>
                <div class="modal-detail">
                    <span>Bonus:</span>
                    <span id="modalBonus">0.00 GRT</span>
                </div>
                <div class="modal-detail font-bold">
                    <span>Total Tokens:</span>
                    <span id="modalTotalTokens">0.00 GRT</span>
                </div>
            </div>
            
            <button class="modal-button" id="confirmPurchase">Confirm Purchase</button>
            <button class="modal-button bg-secondary-700 text-white hover:bg-secondary-600" id="cancelPurchase">Cancel</button>
        </div>
    </div>

    <!-- Notification Container -->
    <div id="notificationContainer"></div>

    <script>
        // User wallet and token state
        let userWalletConnected = false;
        let userTokenBalance = 0;
        let currentPurchase = {
            amount: 0,
            tokens: 0,
            bonus: 0,
            gasFee: 0
        };

        // DOM Elements
        const connectWalletBtn = document.getElementById('connectWallet');
        const walletText = document.getElementById('walletText');
        const tokenBalance = document.getElementById('tokenBalance');
        const balanceValue = document.getElementById('balanceValue');
        const closeBalance = document.getElementById('closeBalance');
        const buyTokensBtn = document.getElementById('buyTokensBtn');
        const investmentAmount = document.getElementById('investmentAmount');
        const tokensReceived = document.getElementById('tokensReceived');
        const purchaseModal = document.getElementById('purchaseModal');
        const closeModal = document.getElementById('closeModal');
        const cancelPurchase = document.getElementById('cancelPurchase');
        const confirmPurchase = document.getElementById('confirmPurchase');
        const modalAmount = document.getElementById('modalAmount');
        const modalTokens = document.getElementById('modalTokens');
        const modalGasFee = document.getElementById('modalGasFee');
        const modalBonus = document.getElementById('modalBonus');
        const modalTotalTokens = document.getElementById('modalTotalTokens');
        const investmentButtons = document.querySelectorAll('.investment-btn');
        const notificationContainer = document.getElementById('notificationContainer');
        
        // Show notification function
        function showNotification(message, type) {
            const notification = document.createElement('div');
            notification.className = `notification ${type}`;
            notification.innerHTML = `<i class="fas fa-${type === 'success' ? 'check-circle' : type === 'error' ? 'exclamation-circle' : 'info-circle'}"></i> ${message}`;
            notificationContainer.appendChild(notification);
            
            // Show notification
            setTimeout(() => {
                notification.classList.add('show');
            }, 10);
            
            // Hide after delay
            setTimeout(() => {
                notification.classList.remove('show');
                setTimeout(() => {
                    notification.remove();
                }, 300);
            }, 5000);
        }
        
        // Wallet connection functionality
        connectWalletBtn.addEventListener('click', function() {
            if (!userWalletConnected) {
                // Simulate wallet connection
                walletText.textContent = "0x742d...f44e";
                connectWalletBtn.classList.add('wallet-connected');
                userWalletConnected = true;
                
                // Show notification
                showNotification('Wallet connected successfully!', 'success');
                
                // Show token balance
                tokenBalance.style.display = 'block';
            } else {
                // Simulate disconnecting wallet
                walletText.textContent = "Connect Wallet";
                connectWalletBtn.classList.remove('wallet-connected');
                userWalletConnected = false;
                
                // Hide token balance
                tokenBalance.style.display = 'none';
                
                // Show notification
                showNotification('Wallet disconnected', 'info');
            }
        });
        
        // Close token balance
        closeBalance.addEventListener('click', function() {
            tokenBalance.style.display = 'none';
        });
        
        // Token calculator
        function calculateTokens(amount) {
            const tokenPrice = 1.20; // $1.20 per token
            const bonusRate = 0.30; // 30% bonus
            const baseTokens = amount / tokenPrice;
            const bonusTokens = baseTokens * bonusRate;
            const totalTokens = baseTokens + bonusTokens;
            
            // Calculate random gas fee between $5-10
            const gasFee = (5 + Math.random() * 5).toFixed(2);
            
            return {
                baseTokens: baseTokens,
                bonusTokens: bonusTokens,
                totalTokens: totalTokens,
                gasFee: gasFee
            };
        }
        
        // Update token display when investment amount changes
        investmentAmount.addEventListener('input', function() {
            const amount = parseFloat(this.value) || 0;
            
            if (amount >= 10 && amount <= 5000) {
                const result = calculateTokens(amount);
                tokensReceived.value = result.totalTokens.toFixed(2) + ' GRT';
            } else if (amount < 10) {
                tokensReceived.value = 'Minimum $10 investment';
            } else {
                tokensReceived.value = 'Maximum $5,000 investment';
            }
        });
        
        // Buy tokens button handler
        buyTokensBtn.addEventListener('click', function() {
            if (!userWalletConnected) {
                showNotification('Please connect your wallet first!', 'error');
                return;
            }
            
            const amount = parseFloat(investmentAmount.value) || 0;
            
            if (amount < 10) {
                showNotification('Minimum investment is $10', 'error');
                return;
            }
            
            if (amount > 5000) {
                showNotification('Maximum investment is $5000', 'error');
                return;
            }
            
            // Calculate tokens
            const result = calculateTokens(amount);
            
            // Set current purchase
            currentPurchase = {
                amount: amount,
                tokens: result.baseTokens,
                bonus: result.bonusTokens,
                gasFee: result.gasFee,
                totalTokens: result.totalTokens
            };
            
            // Update modal
            modalAmount.textContent = `$${amount.toFixed(2)}`;
            modalTokens.textContent = `${result.baseTokens.toFixed(2)} GRT`;
            modalGasFee.textContent = `$${result.gasFee}`;
            modalBonus.textContent = `${result.bonusTokens.toFixed(2)} GRT (+30%)`;
            modalTotalTokens.textContent = `${result.totalTokens.toFixed(2)} GRT`;
            
            // Show modal
            purchaseModal.classList.add('active');
        });
        
        // Investment plan buttons
        investmentButtons.forEach(button => {
            button.addEventListener('click', function() {
                if (!userWalletConnected) {
                    showNotification('Please connect your wallet first!', 'error');
                    return;
                }
                
                const tier = this.dataset.tier;
                let amount = 0;
                
                // Set investment amount based on tier
                if (tier === 'starter') amount = 25;
                else if (tier === 'silver') amount = 100;
                else if (tier === 'gold') amount = 250;
                
                // Calculate tokens
                const result = calculateTokens(amount);
                
                // Set current purchase
                currentPurchase = {
                    amount: amount,
                    tokens: result.baseTokens,
                    bonus: result.bonusTokens,
                    gasFee: result.gasFee,
                    totalTokens: result.totalTokens
                };
                
                // Update modal
                modalAmount.textContent = `$${amount.toFixed(2)}`;
                modalTokens.textContent = `${result.baseTokens.toFixed(2)} GRT`;
                modalGasFee.textContent = `$${result.gasFee}`;
                modalBonus.textContent = `${result.bonusTokens.toFixed(2)} GRT (+30%)`;
                modalTotalTokens.textContent = `${result.totalTokens.toFixed(2)} GRT`;
                
                // Show modal
                purchaseModal.classList.add('active');
            });
        });
        
        // Modal close handlers
        closeModal.addEventListener('click', function() {
            purchaseModal.classList.remove('active');
        });
        
        cancelPurchase.addEventListener('click', function() {
            purchaseModal.classList.remove('active');
        });
        
        // Confirm purchase handler
        confirmPurchase.addEventListener('click', function() {
            // Add tokens to user balance
            userTokenBalance += currentPurchase.totalTokens;
            balanceValue.textContent = userTokenBalance.toFixed(2);
            
            // Hide modal
            purchaseModal.classList.remove('active');
            
            // Show success notification
            showNotification(`Success! ${currentPurchase.totalTokens.toFixed(2)} GRT added to your wallet`, 'success');
            
            // Show token balance if hidden
            tokenBalance.style.display = 'block';
        });
        
        // FAQ accordion functionality
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const faqItem = question.closest('.faq-item');
                faqItem.classList.toggle('active');
                
                // Rotate icon
                const icon = question.querySelector('i');
                icon.classList.toggle('fa-chevron-down');
                icon.classList.toggle('fa-chevron-up');
            });
        });
        
        // Update presale progress
        function updateProgressBar() {
            const progressBar = document.getElementById('presaleProgress');
            let progress = 72;
            
            // Simulate progress increase
            setInterval(() => {
                if (progress < 100) {
                    progress += 0.1;
                    progressBar.style.width = progress + '%';
                }
            }, 5000);
        }
        
        // Countdown timer
        function updateCountdown() {
            const daysEl = document.getElementById('days');
            const hoursEl = document.getElementById('hours');
            const minutesEl = document.getElementById('minutes');
            const secondsEl = document.getElementById('seconds');
            
            // Set target date (7 days from now)
            const targetDate = new Date();
            targetDate.setDate(targetDate.getDate() + 7);
            
            function update() {
                const now = new Date();
                const diff = targetDate - now;
                
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((diff % (1000 * 60)) / 1000);
                
                daysEl.textContent = days.toString().padStart(2, '0');
                hoursEl.textContent = hours.toString().padStart(2, '0');
                minutesEl.textContent = minutes.toString().padStart(2, '0');
                secondsEl.textContent = seconds.toString().padStart(2, '0');
            }
            
            update();
            setInterval(update, 1000);
        }
        
        // Initialize functions
        document.addEventListener('DOMContentLoaded', function() {
            updateProgressBar();
            updateCountdown();
        });
    </script>
</body>
</html>
