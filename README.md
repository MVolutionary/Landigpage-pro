<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI-Landing Pro - Marcel Vogelsang | KI-Optimierte Enterprise Landingpages</title>
    <meta name="description" content="Steigern Sie Ihre Conversion-Rate um bis zu 400% mit KI-optimierten Landingpages. Premium-Services von Marcel Vogelsang mit garantierten Ergebnissen für Unternehmen.">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800;900&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Inter', sans-serif; }
        .gradient-bg { background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%); }
        .gold-gradient { background: linear-gradient(135deg, #ffd700 0%, #ffed4e 50%, #ffc107 100%); }
        .platinum-gradient { background: linear-gradient(135deg, #e6e6fa 0%, #d8bfd8 50%, #dda0dd 100%); }
        .text-shadow { text-shadow: 2px 2px 8px rgba(0,0,0,0.7); }
        .box-shadow-gold { box-shadow: 0 15px 35px rgba(255, 215, 0, 0.3); }
        .box-shadow-platinum { box-shadow: 0 20px 40px rgba(221, 160, 221, 0.4); }
        .hover-lift { transition: all 0.4s ease; }
        .hover-lift:hover { transform: translateY(-8px); box-shadow: 0 20px 40px rgba(255, 215, 0, 0.2); }
        .animate-pulse-slow { animation: pulse 3s infinite; }
        .animate-glow { animation: glow 2s ease-in-out infinite alternate; }
        @keyframes glow { from { box-shadow: 0 0 20px #dda0dd; } to { box-shadow: 0 0 40px #dda0dd, 0 0 60px #dda0dd; } }
        .bg-pattern { background-image: radial-gradient(circle at 2px 2px, rgba(255,215,0,0.1) 1px, transparent 0); background-size: 40px 40px; }
        .enterprise-badge { background: linear-gradient(45deg, #1e3a8a, #3b82f6); border: 2px solid #60a5fa; }
        .premium-card { background: linear-gradient(145deg, #1f2937 0%, #374151 100%); border: 1px solid #4b5563; }
        .platinum-card { background: linear-gradient(145deg, #2d1b69 0%, #3730a3 100%); border: 2px solid #dda0dd; }
        .pricing-card { transition: all 0.3s ease; }
        .pricing-card:hover { transform: scale(1.02); }
        .page-section { display: none; }
        .page-section.active { display: block; }
        .nav-item { cursor: pointer; transition: all 0.3s ease; }
        .nav-item:hover { color: #ffd700; }
        .nav-item.active { color: #ffd700; border-bottom: 2px solid #ffd700; }
        .floating-cta { position: fixed; bottom: 20px; right: 20px; z-index: 1000; }
        .bestseller-badge { position: absolute; top: -10px; right: -10px; background: #ff0000; color: white; padding: 5px 15px; border-radius: 20px; font-size: 12px; font-weight: bold; transform: rotate(10deg); }
        .platinum-special { border: 3px solid #dda0dd; position: relative; overflow: hidden; }
        .platinum-special::before { content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%; background: linear-gradient(45deg, transparent, rgba(221, 160, 221, 0.1), transparent); animation: shine 3s infinite; }
        @keyframes shine { 0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); } 100% { transform: translateX(100%) translateY(100%) rotate(45deg); } }
        
        /* Three Dots Menu Styles */
        .three-dots-menu { position: relative; display: inline-block; }
        .three-dots-trigger { 
            cursor: pointer; 
            padding: 8px; 
            border-radius: 50%; 
            transition: all 0.3s ease;
            background: rgba(255, 215, 0, 0.1);
            border: 1px solid #ffd700;
        }
        .three-dots-trigger:hover { 
            background: rgba(255, 215, 0, 0.2); 
            transform: scale(1.1);
        }
        .three-dots-content {
            position: absolute;
            top: 100%;
            left: 0;
            background: linear-gradient(145deg, #1f2937 0%, #374151 100%);
            border: 1px solid #ffd700;
            border-radius: 8px;
            padding: 16px;
            min-width: 200px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            opacity: 0;
            visibility: hidden;
            transform: translateY(-10px);
            transition: all 0.3s ease;
            z-index: 1000;
        }
        .three-dots-content.active {
            opacity: 1;
            visibility: visible;
            transform: translateY(0);
        }
        
        /* Pixel Animation */
        .pixel-grid {
            display: grid;
            grid-template-columns: repeat(8, 1fr);
            gap: 2px;
            margin-bottom: 12px;
        }
        .pixel {
            width: 12px;
            height: 12px;
            background: #374151;
            border-radius: 2px;
            transition: all 0.1s ease;
        }
        .pixel.active {
            background: #ffd700;
            box-shadow: 0 0 8px #ffd700;
        }
        
        /* Timeline Styles for About Section */
        .timeline { position: relative; padding-left: 30px; }
        .timeline::before {
            content: '';
            position: absolute;
            left: 15px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, #ffd700, #ff8c00);
        }
        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            padding-left: 30px;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -23px;
            top: 8px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #ffd700;
            border: 3px solid #1f2937;
        }
        .timeline-content {
            background: rgba(55, 65, 81, 0.5);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid #ffd700;
        }
        .journey-card {
            background: linear-gradient(145deg, #1f2937 0%, #374151 100%);
            border: 1px solid #4b5563;
            transition: all 0.3s ease;
        }
        .journey-card:hover {
            transform: translateY(-5px);
            border-color: #ffd700;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.2);
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header -->
    <header class="gradient-bg sticky top-0 z-50 shadow-2xl border-b border-yellow-400 border-opacity-30">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-3" onclick="showPage('home')">
                <i class="fas fa-rocket text-yellow-400 text-3xl"></i>
                <div class="cursor-pointer">
                    <span class="text-2xl font-black text-yellow-400">AI-Landing Pro</span>
                    <div class="text-xs text-gray-300">by Marcel Vogelsang</div>
                </div>
            </div>
            <nav class="hidden md:flex space-x-8">
                <span class="nav-item active" onclick="showPage('home')">Home</span>
                <span class="nav-item" onclick="showPage('services')">Services</span>
                <span class="nav-item" onclick="showPage('pricing')">Preise</span>
                <span class="nav-item" onclick="showPage('ebooks')">E-Books</span>
                <span class="nav-item" onclick="showPage('about')">Über mich</span>
                <span class="nav-item" onclick="showPage('contact')">Kontakt</span>
            </nav>
            <div class="enterprise-badge px-4 py-2 rounded-full text-sm font-bold">
                <i class="fas fa-building mr-2"></i>Enterprise Ready
            </div>
        </div>
    </header>

    <!-- Home Page -->
    <section id="home" class="page-section active">
        <!-- Hero Section -->
        <div class="gradient-bg bg-pattern min-h-screen flex items-center py-20">
            <div class="container mx-auto px-4 text-center">
                <div class="max-w-6xl mx-auto">
                    <div class="mb-6">
                        <span class="bg-yellow-400 text-black px-6 py-2 rounded-full text-sm font-bold">
                            <i class="fas fa-crown mr-2"></i>Über 1000+ erfolgreiche Projekte
                        </span>
                    </div>
                    <h1 class="text-5xl md:text-8xl font-black mb-8 text-shadow leading-tight">
                        Steigern Sie Ihre <span class="text-yellow-400">Conversion-Rate</span>
                        <br>um bis zu <span class="text-yellow-400 animate-pulse-slow">400%</span>
                    </h1>
                    <p class="text-xl md:text-3xl mb-12 text-gray-300 leading-relaxed max-w-4xl mx-auto">
                        Professionelle KI-optimierte Landingpages für Unternehmen. 
                        <strong>Wissenschaftlich fundiert, garantierte ROI-Steigerung</strong> in nur 14 Tagen.
                    </p>
                    <div class="flex flex-col lg:flex-row gap-6 justify-center items-center mb-16">
                        <button onclick="showPage('contact')" class="gold-gradient text-black px-10 py-5 rounded-lg font-black text-xl hover:scale-105 transition-transform box-shadow-gold">
                            <i class="fas fa-chart-line mr-3"></i>
                            Kostenlose Conversion-Analyse
                        </button>
                        <button onclick="showPage('pricing')" class="border-3 border-yellow-400 text-yellow-400 px-10 py-5 rounded-lg font-black text-xl hover:bg-yellow-400 hover:text-black transition-colors">
                            <i class="fas fa-rocket mr-3"></i>
                            Pakete ansehen
                        </button>
                    </div>
                    <div class="grid md:grid-cols-4 gap-6 text-center mb-12">
                        <div class="bg-black bg-opacity-40 p-6 rounded-xl">
                            <div class="text-3xl font-black text-yellow-400 mb-2">1000+</div>
                            <div class="text-gray-300 text-sm">Erfolgreiche Projekte</div>
                        </div>
                        <div class="bg-black bg-opacity-40 p-6 rounded-xl">
                            <div class="text-3xl font-black text-yellow-400 mb-2">€2.5M+</div>
                            <div class="text-gray-300 text-sm">Zusätzlicher Umsatz</div>
                        </div>
                        <div class="bg-black bg-opacity-40 p-6 rounded-xl">
                            <div class="text-3xl font-black text-yellow-400 mb-2">387%</div>
                            <div class="text-gray-300 text-sm">Ø ROI-Steigerung</div>
                        </div>
                        <div class="bg-black bg-opacity-40 p-6 rounded-xl">
                            <div class="text-3xl font-black text-yellow-400 mb-2">14 Tage</div>
                            <div class="text-gray-300 text-sm">ROI-Garantie</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Quick Features -->
        <div class="py-20 bg-gray-900">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl md:text-5xl font-black text-center mb-16">Warum AI-Landing Pro?</h2>
                <div class="grid md:grid-cols-3 gap-8">
                    <div class="premium-card p-8 rounded-xl hover-lift text-center">
                        <div class="text-yellow-400 text-4xl mb-4">
                            <i class="fas fa-brain"></i>
                        </div>
                        <h3 class="text-2xl font-bold mb-4">KI-Optimierung</h3>
                        <p class="text-gray-400">Wissenschaftlich fundierte Algorithmen analysieren und optimieren jedes Element Ihrer Landingpage.</p>
                        <div class="three-dots-menu mt-4">
                            <div class="three-dots-trigger" onclick="toggleThreeDotsMenu(this)">
                                <i class="fas fa-ellipsis-h text-yellow-400"></i>
                            </div>
                            <div class="three-dots-content">
                                <div class="pixel-grid" id="pixel-grid-1"></div>
                                <h4 class="font-bold text-yellow-400 mb-2">KI-Features im Detail:</h4>
                                <ul class="text-sm space-y-1">
                                    <li>• Predictive Analytics</li>
                                    <li>• User Behavior Tracking</li>
                                    <li>• Dynamic Content Optimization</li>
                                    <li>• Real-time A/B Testing</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="premium-card p-8 rounded-xl hover-lift text-center">
                        <div class="text-yellow-400 text-4xl mb-4">
                            <i class="fas fa-rocket"></i>
                        </div>
                        <h3 class="text-2xl font-bold mb-4">Schnelle Ergebnisse</h3>
                        <p class="text-gray-400">Messbare Conversion-Steigerungen bereits nach 14 Tagen mit unserer bewährten Methodik.</p>
                        <div class="three-dots-menu mt-4">
                            <div class="three-dots-trigger" onclick="toggleThreeDotsMenu(this)">
                                <i class="fas fa-ellipsis-h text-yellow-400"></i>
                            </div>
                            <div class="three-dots-content">
                                <div class="pixel-grid" id="pixel-grid-2"></div>
                                <h4 class="font-bold text-yellow-400 mb-2">Bewährte Methodik:</h4>
                                <ul class="text-sm space-y-1">
                                    <li>• Psychologie-basiertes Design</li>
                                    <li>• Micro-Conversions Tracking</li>
                                    <li>• Iterative Optimierung</li>
                                    <li>• Performance Monitoring</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="premium-card p-8 rounded-xl hover-lift text-center">
                        <div class="text-yellow-400 text-4xl mb-4">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <h3 class="text-2xl font-bold mb-4">ROI-Garantie</h3>
                        <p class="text-gray-400">100% Geld-zurück-Garantie, wenn Sie nicht innerhalb von 14 Tagen messbare Verbesserungen sehen.</p>
                        <div class="three-dots-menu mt-4">
                            <div class="three-dots-trigger" onclick="toggleThreeDotsMenu(this)">
                                <i class="fas fa-ellipsis-h text-yellow-400"></i>
                            </div>
                            <div class="three-dots-content">
                                <div class="pixel-grid" id="pixel-grid-3"></div>
                                <h4 class="font-bold text-yellow-400 mb-2">Garantie-Details:</h4>
                                <ul class="text-sm space-y-1">
                                    <li>• 14 Tage Geld-zurück</li>
                                    <li>• Messbare KPIs erforderlich</li>
                                    <li>• Vollständige Erstattung</li>
                                    <li>• Keine versteckten Bedingungen</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Page -->
    <section id="services" class="page-section py-20 bg-gray-900">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-6xl font-black mb-8">Premium Services</h2>
                <p class="text-xl text-gray-400 max-w-4xl mx-auto">
                    Vollumfängliche Digital-Marketing-Lösungen für Unternehmen jeder Größe
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-12 max-w-6xl mx-auto mb-16">
                <div class="bg-black bg-opacity-30 p-12 rounded-2xl">
                    <div class="text-yellow-400 text-5xl mb-6">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="text-3xl font-bold mb-6">KI-Optimierte Landingpages</h3>
                    <p class="text-gray-300 text-lg mb-8">
                        Wissenschaftlich fundierte Conversion-Optimierung mit garantierter ROI-Steigerung. 
                        Speziell entwickelt für maximale Performance und hohe Traffic-Volumina.
                    </p>
                    <div class="grid grid-cols-2 gap-4 text-sm mb-6">
                        <div class="bg-gray-800 p-4 rounded-lg">
                            <div class="font-bold text-yellow-400 mb-2">Performance</div>
                            <div class="text-gray-400">Bis zu 400% Conversion-Steigerung</div>
                        </div>
                        <div class="bg-gray-800 p-4 rounded-lg">
                            <div class="font-bold text-yellow-400 mb-2">Speed</div>
                            <div class="text-gray-400">< 1.5s Ladezeit garantiert</div>
                        </div>
                        <div class="bg-gray-800 p-4 rounded-lg">
                            <div class="font-bold text-yellow-400 mb-2">Mobile</div>
                            <div class="text-gray-400">100% responsive Design</div>
                        </div>
                        <div class="bg-gray-800 p-4 rounded-lg">
                            <div class="font-bold text-yellow-400 mb-2">Support</div>
                            <div class="text-gray-400">30 Tage Premium-Support</div>
                        </div>
                    </div>
                    <button onclick="showPage('pricing')" class="gold-gradient text-black px-6 py-3 rounded-lg font-bold">
                        Pakete ansehen
                    </button>
                </div>
                
                <div class="bg-black bg-opacity-30 p-12 rounded-2xl">
                    <div class="text-yellow-400 text-5xl mb-6">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3 class="text-3xl font-bold mb-6">Premium E-Book Creation</h3>
                    <p class="text-gray-300 text-lg mb-8">
                        Professionelle E-Books für Lead-Generierung und Content-Marketing. 
                        Von Experten geschrieben, KI-optimiert und branchenspezifisch angepasst.
                    </p>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-gray-800 p-3 rounded-lg">
                            <span class="font-semibold">Kurz-Guide (5-10 Seiten)</span>
                            <span class="text-yellow-400 font-bold">€897</span>
                        </div>
                        <div class="flex justify-between items-center bg-gray-800 p-3 rounded-lg">
                            <span class="font-semibold">Standard E-Book (15-25 Seiten)</span>
                            <span class="text-yellow-400 font-bold">€1.497</span>
                        </div>
                        <div class="flex justify-between items-center bg-gray-800 p-3 rounded-lg
