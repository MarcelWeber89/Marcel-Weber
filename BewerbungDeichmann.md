<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interaktives Bewerbungs-Microlearning</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body { font-family: 'Inter', sans-serif; }
        
        .fade-in {
            animation: fadeIn 0.6s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .progress-bar {
            transition: width 0.5s ease-in-out;
        }
        
        .module-card {
            transition: all 0.3s ease;
        }
        
        .module-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .completed {
            background: linear-gradient(135deg, #16a34a, #15803d);
        }
        
        .current {
            background: linear-gradient(135deg, #10b981, #059669);
        }
        
        .locked {
            background: linear-gradient(135deg, #6b7280, #4b5563);
        }
    </style>
</head>
<body class="bg-gradient-to-br from-green-50 to-emerald-100 min-h-screen">
    <div class="container mx-auto px-4 py-8 max-w-4xl">
        <!-- Header -->
        <div class="text-center mb-8 fade-in">
            <h1 class="text-4xl font-bold text-gray-800 mb-2">🎓 Interaktives Bewerbungs-Microlearning</h1>
            <p class="text-lg text-gray-600">Coordinator Learning & Development (m/w/d) - Deichmann</p>
            <div class="mt-4 bg-white rounded-full px-6 py-2 inline-block shadow-sm">
                <span class="text-sm font-medium text-gray-700">Fortschritt: </span>
                <span id="progress-text" class="font-bold text-green-600">0%</span>
            </div>
        </div>

        <!-- Progress Bar -->
        <div class="bg-white rounded-full h-3 mb-8 shadow-inner">
            <div id="progress-bar" class="progress-bar bg-gradient-to-r from-green-500 to-green-600 h-3 rounded-full" style="width: 0%"></div>
        </div>

        <!-- Learning Modules -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
            <!-- Modul 1: Über mich -->
            <div class="module-card current rounded-xl p-6 text-white cursor-pointer" onclick="openModule(1)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 1</h3>
                    <span class="text-2xl">👋</span>
                </div>
                <h4 class="font-medium mb-2">Über mich</h4>
                <p class="text-sm opacity-90">Lernen Sie mich kennen</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>

            <!-- Modul 2: Meine Erfahrung -->
            <div class="module-card locked rounded-xl p-6 text-white cursor-pointer" onclick="openModule(2)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 2</h3>
                    <span class="text-2xl">🔒</span>
                </div>
                <h4 class="font-medium mb-2">Meine Erfahrung</h4>
                <p class="text-sm opacity-90">L&D Expertise & Projekte</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>

            <!-- Modul 3: Warum ich? -->
            <div class="module-card locked rounded-xl p-6 text-white cursor-pointer" onclick="openModule(3)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 3</h3>
                    <span class="text-2xl">🔒</span>
                </div>
                <h4 class="font-medium mb-2">Warum ich?</h4>
                <p class="text-sm opacity-90">Mein Mehrwert für Sie</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>

            <!-- Modul 4: Meine Vision -->
            <div class="module-card locked rounded-xl p-6 text-white cursor-pointer" onclick="openModule(4)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 4</h3>
                    <span class="text-2xl">🔒</span>
                </div>
                <h4 class="font-medium mb-2">Meine Vision</h4>
                <p class="text-sm opacity-90">Zukunft des Lernens</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>

            <!-- Modul 5: Interaktive Demo -->
            <div class="module-card locked rounded-xl p-6 text-white cursor-pointer" onclick="openModule(5)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 5</h3>
                    <span class="text-2xl">🔒</span>
                </div>
                <h4 class="font-medium mb-2">Interaktive Demo</h4>
                <p class="text-sm opacity-90">Meine Arbeitsweise</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>

            <!-- Modul 6: Kontakt -->
            <div class="module-card locked rounded-xl p-6 text-white cursor-pointer" onclick="openModule(6)">
                <div class="flex items-center justify-between mb-4">
                    <h3 class="text-lg font-semibold">Modul 6</h3>
                    <span class="text-2xl">🔒</span>
                </div>
                <h4 class="font-medium mb-2">Nächste Schritte</h4>
                <p class="text-sm opacity-90">Lassen Sie uns sprechen</p>
                <div class="mt-4 flex items-center">
                    <div class="w-2 h-2 bg-white rounded-full mr-2"></div>
                    <span class="text-xs">2 Min</span>
                </div>
            </div>
        </div>

        <!-- Learning Content Modal -->
        <div id="modal" class="fixed inset-0 bg-black bg-opacity-50 hidden items-center justify-center z-50 p-4">
            <div class="bg-white rounded-2xl max-w-2xl w-full max-h-[90vh] overflow-y-auto">
                <div class="p-6">
                    <div class="flex justify-between items-center mb-6">
                        <h2 id="modal-title" class="text-2xl font-bold text-gray-800"></h2>
                        <button onclick="closeModal()" class="text-gray-500 hover:text-gray-700 text-2xl">&times;</button>
                    </div>
                    
                    <div id="modal-content" class="space-y-6">
                        <!-- Content wird dynamisch geladen -->
                    </div>
                    
                    <div class="flex justify-between items-center mt-8 pt-6 border-t">
                        <button id="prev-btn" onclick="previousModule()" class="px-6 py-2 bg-gray-200 text-gray-700 rounded-lg hover:bg-gray-300 transition-colors hidden">
                            ← Zurück
                        </button>
                        <div class="flex-1"></div>
                        <button id="next-btn" onclick="nextModule()" class="px-6 py-3 bg-gradient-to-r from-green-500 to-emerald-600 text-white rounded-lg hover:from-green-600 hover:to-emerald-700 transition-all font-medium">
                            Weiter →
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        let currentModule = 0;
        let completedModules = [];
        
        const moduleContent = {
            1: {
                title: "👋 Über mich",
                content: `
                    <div class="space-y-6">
                        <div class="bg-green-50 rounded-xl p-6">
                            <h3 class="text-xl font-semibold text-green-800 mb-4">Hallo! Ich bin Marcel Weber</h3>
                            <p class="text-gray-700 leading-relaxed">
                                Mit über 10 Jahren Erfahrung im Einzelhandel und internationalen Trainingsfunktionen 
                                entwickle ich Lern- und Entwicklungsprogramme, die Mitarbeitende gezielt befähigen und 
                                messbare Geschäftserfolge erzielen. Als Coordinator Learning & Development möchte ich 
                                bei Deichmann eine zukunftsfähige Lernkultur mitgestalten.
                            </p>
                        </div>
                        
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="bg-green-50 rounded-lg p-4">
                                <h4 class="font-semibold text-green-800 mb-2">🎯 Meine Stärken</h4>
                                <ul class="text-sm text-gray-700 space-y-1">
                                    <li>• Strategische Lernziele mit Praxis verbinden</li>
                                    <li>• Globale Blended-Learning-Konzepte</li>
                                    <li>• Skalierbare & effiziente Prozesse</li>
                                    <li>• Verhaltensänderung & KPI-Verbesserung</li>
                                </ul>
                            </div>
                            
                            <div class="bg-purple-50 rounded-lg p-4">
                                <h4 class="font-semibold text-purple-800 mb-2">🚀 Meine Tools</h4>
                                <ul class="text-sm text-gray-700 space-y-1">
                                    <li>• Power BI, Power Automate, Power Apps</li>
                                    <li>• Avendoo, Axonify</li>
                                    <li>• Canva, SAP, Jira, Confluence</li>
                                    <li>• KI-Anwendungen & Prozessautomatisierung</li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="bg-green-100 rounded-xl p-6">
                            <h4 class="font-semibold text-green-800 mb-3">🎯 Warum Deichmann?</h4>
                            <p class="text-gray-700">
                                Gespräche mit aktuellen und ehemaligen Deichmann-Mitarbeitenden haben mir gezeigt, dass hier ein internationales Umfeld auf gelebte Entwicklungschancen trifft. Diese Kombination aus globaler Perspektive und praxisnaher Gestaltungskraft motiviert mich besonders. Ich möchte meine Erfahrung in Learning & Development einbringen, um diese Kultur aktiv mitzugestalten.
                            </p>
                        </div>
                    </div>
                `
            },
            2: {
                title: "🎓 Meine Erfahrung",
                content: `
                    <div class="space-y-6">
                        <div class="bg-green-50 rounded-xl p-6">
                            <h3 class="text-xl font-semibold text-green-800 mb-4">Meine L&D Journey</h3>
                            <div class="space-y-4">
                                <div class="border-l-4 border-green-500 pl-4">
                                    <h4 class="font-semibold text-gray-800">Global Training & Development Manager - Emma – The Sleep Company</h4>
                                    <p class="text-sm text-gray-600 mb-2">01/2019 - 09/2024</p>
                                    <p class="text-gray-700">Entwicklung globaler Verkaufsprozesse, Quality Management und digitaler Trainingsplattformen für alle Emma Stores weltweit - perfekte Vorbereitung für Deichmanns 4.700 Standorte in 34 Ländern</p>
                                </div>
                                
                                <div class="border-l-4 border-green-500 pl-4">
                                    <h4 class="font-semibold text-gray-800">Training & Development Manager Offline Global</h4>
                                    <p class="text-sm text-gray-600 mb-2">05/2023 - 09/2024</p>
                                    <p class="text-gray-700">Entwicklung digitaler Trainingsplattformen, Ausbildung von Store Managern und C-Level Onboarding</p>
                                </div>
                                
                                <div class="border-l-4 border-purple-500 pl-4">
                                    <h4 class="font-semibold text-gray-800">Training & Development Manager Online Global</h4>
                                    <p class="text-sm text-gray-600 mb-2">08/2021 - 04/2023</p>
                                    <p class="text-gray-700">E-Learning-Entwicklung für LMS-Plattform (Avendoo), Quality Management für Call Center Global</p>
                                </div>
                                
                                <div class="border-l-4 border-orange-500 pl-4">
                                    <h4 class="font-semibold text-gray-800">Sales Trainer - Swiss Sense</h4>
                                    <p class="text-sm text-gray-600 mb-2">10/2024 - 12/2024</p>
                                    <p class="text-gray-700">Training on-the-Job für Verkaufstechnik, Verkauf von Boxspringbetten</p>
                                </div>
                                
                                <div class="border-l-4 border-gray-500 pl-4">
                                    <h4 class="font-semibold text-gray-800">Aktuelle Projekte - IMR GmbH</h4>
                                    <p class="text-sm text-gray-600 mb-2">05/2025 - Heute</p>
                                    <p class="text-gray-700">Prozessoptimierung, Digitalisierung und Automatisierung im KMU-Kontext</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="grid md:grid-cols-3 gap-4">
                            <div class="bg-white rounded-lg p-4 shadow-sm border">
                                <div class="text-2xl font-bold text-blue-600">↗️</div>
                                <div class="text-sm text-gray-600">Signifikante Steigerung der Verkaufsperformance</div>
                            </div>
                            <div class="bg-white rounded-lg p-4 shadow-sm border">
                                <div class="text-2xl font-bold text-green-600">↘️</div>
                                <div class="text-sm text-gray-600">Sinkende Retourenquoten durch bessere Schulungen</div>
                            </div>
                            <div class="bg-white rounded-lg p-4 shadow-sm border">
                                <div class="text-2xl font-bold text-purple-600">📈</div>
                                <div class="text-sm text-gray-600">Gestärkte Mitarbeiterzufriedenheit</div>
                            </div>
                        </div>
                        
                        <div class="bg-gray-50 rounded-xl p-6">
                            <h4 class="font-semibold text-gray-800 mb-3">🏆 Highlight-Projekte</h4>
                            <div class="space-y-4">
                                <div>
                                    <p class="text-gray-700 mb-2">
                                        <strong>"Globale Trainingsplattform Emma Stores"</strong> - Entwicklung des gesamten Verkaufsprozesses 
                                        für alle globalen Emma Stores (Eigen- und Franchise-Filialen) mit digitalem Quality Management.
                                    </p>
                                    <div class="text-sm text-gray-600">
                                        <strong>Ergebnis:</strong> Stores starteten direkt mit hohen Verkaufszahlen beim Launch, erfolgreiche Vermeidung von Downselling und gestärktes Cross-Selling
                                    </div>
                                </div>
                                
                                <div>
                                    <p class="text-gray-700 mb-2">
                                        <strong>"18-Monats E-Learning-Programm"</strong> - Konzeption und Entwicklung umfassender 
                                        E-Learnings für LMS-Plattform (Avendoo) mit integriertem Quality Management.
                                    </p>
                                    <div class="text-sm text-gray-600">
                                        <strong>Ergebnis:</strong> Skalierbare Trainingsstruktur für globale Call Center Operations
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                `
            },
            3: {
                title: "🌟 Warum ich?",
                content: `
                    <div class="space-y-6">
                        <div class="bg-gradient-to-r from-green-50 to-emerald-50 rounded-xl p-6">
                            <h3 class="text-xl font-semibold text-green-800 mb-4">Mein Mehrwert für Deichmann</h3>
                            <p class="text-gray-700 leading-relaxed">
                                Als Coordinator Learning & Development bringe ich genau die Expertise mit, die in Ihrer 
                                Stellenausschreibung gesucht wird: eTrainings, Blended Learning und digitale Lernmedien 
                                für ein globales Familienunternehmen mit über 49.000 Mitarbeitern.
                            </p>
                        </div>
                        
                        <div class="space-y-4">
                            <div class="bg-white rounded-lg p-5 shadow-sm border-l-4 border-green-500">
                                <h4 class="font-semibold text-gray-800 mb-2">🎯 eTrainings & Blended Learning</h4>
                                <p class="text-gray-700 text-sm">
                                    Ich entwickle eTrainings, Präsenztrainings und Blended Learning Konzepte - 
                                    genau wie in Ihrer Stellenausschreibung gefordert.
                                </p>
                            </div>
                            
                            <div class="bg-white rounded-lg p-5 shadow-sm border-l-4 border-emerald-500">
                                <h4 class="font-semibold text-gray-800 mb-2">🎬 Digitale Lernmedien</h4>
                                <p class="text-gray-700 text-sm">
                                    Erklärvideos, Grafiken und Teilnehmerunterlagen - ich erstelle alle 
                                    Lernmedien eigenständig über verschiedene Kanäle.
                                </p>
                            </div>
                            
                            <div class="bg-white rounded-lg p-5 shadow-sm border-l-4 border-green-600">
                                <h4 class="font-semibold text-gray-800 mb-2">🏪 Einzelhandelserfahrung</h4>
                                <p class="text-gray-700 text-sm">
                                    10+ Jahre im Einzelhandel - von der Ausbildung bis zum Global Manager. 
                                    Ich verstehe die Herausforderungen Ihrer Branche.
                                </p>
                            </div>
                            
                            <div class="bg-white rounded-lg p-5 shadow-sm border-l-4 border-teal-500">
                                <h4 class="font-semibold text-gray-800 mb-2">🤝 Stakeholder-Management</h4>
                                <p class="text-gray-700 text-sm">
                                    Kritisch konstruktiv & lösungsorientiert arbeite ich mit internen und 
                                    externen Stakeholdern zusammen.
                                </p>
                            </div>
                            
                            <div class="bg-white rounded-lg p-5 shadow-sm border-l-4 border-lime-500">
                                <h4 class="font-semibold text-gray-800 mb-2">📚 Organisationstalent</h4>
                                <p class="text-gray-700 text-sm">
                                    Von Teamworkshops über Quality Analysen bis hin zu Personalentwicklungsmaßnahmen - 
                                    ich organisiere komplexe L&D-Projekte mit großem Verständnis für Unternehmensbedürfnisse.
                                </p>
                            </div>
                        </div>
                        
                        <div class="bg-green-100 rounded-xl p-6">
                            <h4 class="font-semibold text-green-800 mb-3">💡 Meine Philosophie für Deichmann</h4>
                            <p class="text-gray-700 italic">
                                "Verkaufen ist kein Zufall. Kenne ich Mensch, Material und stelle vor allem die richtigen Fragen, 
                                ist Verkauf planbar. Diese Philosophie übertrage ich auf L&D: Kenne ich die Lernenden, die Inhalte 
                                und stelle die richtigen Fragen zur Bedarfsanalyse, wird Lernerfolg messbar und planbar."
                            </p>
                        </div>
                    </div>
                `
            },
            4: {
                title: "🔮 Meine Vision",
                content: `
                    <div class="space-y-6">
                        <div class="bg-gradient-to-r from-purple-50 to-pink-50 rounded-xl p-6">
                            <h3 class="text-xl font-semibold text-purple-800 mb-4">Die Zukunft des Lernens gestalten</h3>
                            <p class="text-gray-700 leading-relaxed">
                                Ich sehe L&D nicht als Kostenstelle, sondern als strategischen Wachstumstreiber. 
                                Meine Vision: Eine Lernkultur, die Mitarbeiter zu Höchstleistungen inspiriert.
                            </p>
                        </div>
                        
                        <div class="grid md:grid-cols-2 gap-6">
                            <div class="space-y-4">
                                <h4 class="font-semibold text-gray-800">🎯 Meine Ziele für Ihr Unternehmen:</h4>
                                
                                <div class="bg-blue-50 rounded-lg p-4">
                                    <h5 class="font-medium text-blue-800 mb-2">Erste 90 Tage</h5>
                                    <ul class="text-sm text-gray-700 space-y-1">
                                        <li>• Bedarfsanalyse & Stakeholder-Interviews</li>
                                        <li>• Quick Wins identifizieren</li>
                                        <li>• L&D-Strategie entwickeln</li>
                                    </ul>
                                </div>
                                
                                <div class="bg-green-50 rounded-lg p-4">
                                    <h5 class="font-medium text-green-800 mb-2">Erstes Jahr</h5>
                                    <ul class="text-sm text-gray-700 space-y-1">
                                        <li>• Digitale Lernplattform optimieren</li>
                                        <li>• Microlearning-Bibliothek aufbauen</li>
                                        <li>• Messbare Erfolge demonstrieren</li>
                                    </ul>
                                </div>
                            </div>
                            
                            <div class="space-y-4">
                                <h4 class="font-semibold text-gray-800">🚀 Innovative Ansätze:</h4>
                                
                                <div class="bg-white rounded-lg p-4 shadow-sm">
                                    <h5 class="font-medium text-gray-800 mb-2">🎮 Gamification</h5>
                                    <p class="text-sm text-gray-600">Spielerische Elemente für höhere Engagement-Raten</p>
                                </div>
                                
                                <div class="bg-white rounded-lg p-4 shadow-sm">
                                    <h5 class="font-medium text-gray-800 mb-2">🤖 AI-Personalisierung</h5>
                                    <p class="text-sm text-gray-600">Adaptive Lernpfade basierend auf individuellen Bedürfnissen</p>
                                </div>
                                
                                <div class="bg-white rounded-lg p-4 shadow-sm">
                                    <h5 class="font-medium text-gray-800 mb-2">📱 Mobile-First</h5>
                                    <p class="text-sm text-gray-600">Lernen jederzeit und überall ermöglichen</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="bg-green-50 rounded-xl p-6">
                            <h4 class="font-semibold text-green-800 mb-3">🎯 Mein Versprechen für Deichmann</h4>
                            <p class="text-gray-700 mb-4">
                                Als Coordinator Learning & Development bringe ich genau die Expertise mit, die Deichmann braucht: 
                                eTrainings, Präsenztrainings und Blended Learning Konzepte für über 49.000 Mitarbeiter. 
                                Meine Einzelhandelserfahrung und globale L&D-Kompetenz passen perfekt zu Ihren Anforderungen.
                            </p>
                            
                            <div class="bg-white rounded-lg p-4 mt-4">
                                <h5 class="font-medium text-green-800 mb-2">📈 Perfekte Passung zur Stellenausschreibung</h5>
                                <ul class="text-sm text-gray-700 space-y-1">
                                    <li>• ✅ Erste Erfahrungen im Einzelhandel (10+ Jahre)</li>
                                    <li>• ✅ Affinität zu digitalen Lernmedien (Avendoo, E-Learning)</li>
                                    <li>• ✅ Blended Learning Konzepte (Emma Global)</li>
                                    <li>• ✅ Hands-On-Mentalität & strukturiertes Arbeiten</li>
                                    <li>• ✅ Sehr gute Deutsch- und Englischkenntnisse</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                `
            },
            5: {
                title: "🎮 Interaktive Demo",
                content: `
                    <div class="space-y-6">
                        <div class="bg-gradient-to-r from-green-50 to-blue-50 rounded-xl p-6">
                            <h3 class="text-xl font-semibold text-green-800 mb-4">Erleben Sie meine Arbeitsweise</h3>
                            <p class="text-gray-700">
                                Diese Mini-Demo zeigt, wie ich komplexe Themen in interaktive, 
                                engagierende Lernerfahrungen verwandle.
                            </p>
                        </div>
                        
                        <div class="bg-white rounded-xl p-6 shadow-sm">
                            <h4 class="font-semibold text-gray-800 mb-4">🧠 Quick Learning Challenge</h4>
                            <p class="text-gray-700 mb-4">Welcher Lerntyp sind Sie? Klicken Sie auf Ihre bevorzugte Lernmethode:</p>
                            
                            <div class="grid md:grid-cols-2 gap-4 mb-6">
                                <button onclick="selectLearningType('visual')" class="learning-type-btn bg-blue-100 hover:bg-blue-200 p-4 rounded-lg text-left transition-colors">
                                    <div class="text-2xl mb-2">👁️</div>
                                    <div class="font-medium text-blue-800">Visuell</div>
                                    <div class="text-sm text-gray-600">Diagramme, Infografiken, Videos</div>
                                </button>
                                
                                <button onclick="selectLearningType('auditory')" class="learning-type-btn bg-green-100 hover:bg-green-200 p-4 rounded-lg text-left transition-colors">
                                    <div class="text-2xl mb-2">🎧</div>
                                    <div class="font-medium text-green-800">Auditiv</div>
                                    <div class="text-sm text-gray-600">Podcasts, Diskussionen, Musik</div>
                                </button>
                                
                                <button onclick="selectLearningType('kinesthetic')" class="learning-type-btn bg-purple-100 hover:bg-purple-200 p-4 rounded-lg text-left transition-colors">
                                    <div class="text-2xl mb-2">✋</div>
                                    <div class="font-medium text-purple-800">Kinästhetisch</div>
                                    <div class="text-sm text-gray-600">Hands-on, Experimente, Bewegung</div>
                                </button>
                                
                                <button onclick="selectLearningType('reading')" class="learning-type-btn bg-orange-100 hover:bg-orange-200 p-4 rounded-lg text-left transition-colors">
                                    <div class="text-2xl mb-2">📚</div>
                                    <div class="font-medium text-orange-800">Lesen/Schreiben</div>
                                    <div class="text-sm text-gray-600">Texte, Listen, Notizen</div>
                                </button>
                            </div>
                            
                            <div id="learning-result" class="hidden bg-gray-50 rounded-lg p-4">
                                <h5 class="font-medium text-gray-800 mb-2">🎯 Ihr personalisierter Lernansatz:</h5>
                                <p id="learning-recommendation" class="text-gray-700"></p>
                            </div>
                        </div>
                        
                        <div class="bg-yellow-50 rounded-xl p-6">
                            <h4 class="font-semibold text-yellow-800 mb-3">💡 Das zeigt meine Arbeitsweise</h4>
                            <ul class="text-gray-700 space-y-2 text-sm">
                                <li>• <strong>Personalisierung:</strong> Jeder Lerner bekommt maßgeschneiderte Inhalte</li>
                                <li>• <strong>Interaktivität:</strong> Aktive Teilnahme statt passiver Konsumption</li>
                                <li>• <strong>Sofortiges Feedback:</strong> Lerner erhalten direkte Rückmeldung</li>
                                <li>• <strong>Engagement:</strong> Spielerische Elemente erhöhen die Motivation</li>
                            </ul>
                        </div>
                    </div>
                `
            },
            6: {
                title: "🤝 Nächste Schritte",
                content: `
                    <div class="space-y-6">
                        <div class="bg-gradient-to-r from-green-50 to-emerald-50 rounded-xl p-6 text-center">
                            <h3 class="text-2xl font-semibold text-green-800 mb-4">Lassen Sie uns sprechen!</h3>
                            <p class="text-gray-700 leading-relaxed">
                                Sie haben gesehen, wie ich eTrainings und Blended Learning Konzepte umsetze. 
                                Als Coordinator Learning & Development möchte ich diese Expertise in die 
                                zukunftsfähige Lernkultur bei Deichmann einbringen.
                            </p>
                        </div>
                        
                        <div class="grid md:grid-cols-2 gap-6">
                            <div class="bg-white rounded-xl p-6 shadow-sm">
                                <h4 class="font-semibold text-gray-800 mb-4">📞 Kontakt</h4>
                                <div class="space-y-3">
                                    <div class="flex items-center">
                                        <span class="text-blue-600 mr-3">📧</span>
                                        <span class="text-gray-700">Marcel.1989.Weber@gmail.com</span>
                                    </div>
                                    <div class="flex items-center">
                                        <span class="text-green-600 mr-3">📱</span>
                                        <span class="text-gray-700">0176 46538643</span>
                                    </div>
                                    <div class="flex items-center">
                                        <span class="text-blue-600 mr-3">💼</span>
                                        <span class="text-gray-700">linkedin.com/in/marcel-weber-031917179</span>
                                    </div>
                                    <div class="flex items-center">
                                        <span class="text-purple-600 mr-3">📍</span>
                                        <span class="text-gray-700">Nockwinkel 44, 45277 Essen</span>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="bg-white rounded-xl p-6 shadow-sm">
                                <h4 class="font-semibold text-gray-800 mb-4">🎯 Was Sie erwarten können</h4>
                                <ul class="text-gray-700 space-y-2 text-sm">
                                    <li>• Detaillierte Bedarfsanalyse</li>
                                    <li>• Konkrete Lösungsvorschläge</li>
                                    <li>• ROI-Prognosen für L&D-Investitionen</li>
                                    <li>• Portfolio meiner besten Projekte</li>
                                </ul>
                            </div>
                        </div>
                        
                        <div class="bg-green-50 rounded-xl p-6">
                            <h4 class="font-semibold text-green-800 mb-3">🚀 Bereit für den nächsten Schritt?</h4>
                            <p class="text-gray-700 mb-4">
                                Ich freue mich darauf, mit Ihnen zu besprechen, wie wir gemeinsam eine 
                                Lernkultur schaffen können, die Deichmann voranbringt.
                            </p>
                        </div>
                        
                        <div class="bg-gradient-to-r from-blue-50 to-purple-50 rounded-xl p-6">
                            <h4 class="font-semibold text-blue-800 mb-4 text-center">🎮 Bonus: Memory Challenge</h4>
                            <p class="text-gray-700 text-center mb-4">
                                Wie gut haben Sie aufgepasst? Finden Sie die passenden Paare zu meinen Stärken!
                            </p>
                            
                            <div id="memory-game" class="grid grid-cols-4 gap-3 max-w-md mx-auto mb-4">
                                <!-- Memory cards will be generated by JavaScript -->
                            </div>
                            
                            <div class="text-center">
                                <div id="game-status" class="text-sm text-gray-600 mb-3">Klicken Sie auf zwei Karten, um sie umzudrehen</div>
                                <div id="game-score" class="font-medium text-blue-800">Versuche: 0</div>
                                <button onclick="resetGame()" class="mt-3 px-4 py-2 bg-blue-600 hover:bg-blue-700 text-white rounded-lg transition-colors text-sm">
                                    🔄 Neues Spiel
                                </button>
                            </div>
                            
                            <div id="game-complete" class="hidden mt-4 p-4 bg-green-100 rounded-lg text-center">
                                <h5 class="font-semibold text-green-800 mb-2">🎉 Perfekt!</h5>
                                <p class="text-green-700 text-sm">
                                    Genau so funktioniert effektives Lernen: Durch Interaktion und spielerische Elemente 
                                    bleiben Inhalte besser im Gedächtnis. Das ist mein Ansatz für Deichmann!
                                </p>
                            </div>
                        </div>
                        
                        <div class="text-center bg-gray-50 rounded-xl p-6">
                            <p class="text-gray-600 text-sm mb-2">
                                Vielen Dank, dass Sie sich die Zeit genommen haben, mein interaktives Anschreiben zu durchlaufen!
                            </p>
                            <p class="text-gray-800 font-medium">
                                Diese Erfahrung ist nur ein kleiner Vorgeschmack auf das, was möglich ist. 🚀
                            </p>
                        </div>
                    </div>
                `
            }
        };
        
        function openModule(moduleNumber) {
            if (moduleNumber > completedModules.length + 1) {
                alert('Bitte absolvieren Sie die vorherigen Module zuerst!');
                return;
            }
            
            currentModule = moduleNumber;
            const modal = document.getElementById('modal');
            const title = document.getElementById('modal-title');
            const content = document.getElementById('modal-content');
            const prevBtn = document.getElementById('prev-btn');
            const nextBtn = document.getElementById('next-btn');
            
            title.textContent = moduleContent[moduleNumber].title;
            content.innerHTML = moduleContent[moduleNumber].content;
            
            // Button visibility
            prevBtn.style.display = moduleNumber > 1 ? 'block' : 'none';
            nextBtn.textContent = moduleNumber === 6 ? 'Abschließen' : 'Weiter →';
            
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }
        
        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
            document.getElementById('modal').classList.remove('flex');
        }
        
        function nextModule() {
            if (!completedModules.includes(currentModule)) {
                completedModules.push(currentModule);
                updateProgress();
                updateModuleStatus(currentModule);
            }
            
            if (currentModule < 6) {
                openModule(currentModule + 1);
            } else {
                closeModal();
                showCompletionMessage();
            }
        }
        
        function previousModule() {
            if (currentModule > 1) {
                openModule(currentModule - 1);
            }
        }
        
        function updateProgress() {
            const progress = (completedModules.length / 6) * 100;
            document.getElementById('progress-bar').style.width = progress + '%';
            document.getElementById('progress-text').textContent = Math.round(progress) + '%';
        }
        
        function updateModuleStatus(moduleNumber) {
            const modules = document.querySelectorAll('.module-card');
            const currentModuleCard = modules[moduleNumber - 1];
            
            // Mark as completed
            currentModuleCard.classList.remove('current', 'locked');
            currentModuleCard.classList.add('completed');
            currentModuleCard.querySelector('span').textContent = '✅';
            
            // Unlock next module
            if (moduleNumber < 6) {
                const nextModuleCard = modules[moduleNumber];
                nextModuleCard.classList.remove('locked');
                nextModuleCard.classList.add('current');
                nextModuleCard.querySelector('span').textContent = '🔓';
            }
        }
        
        function showCompletionMessage() {
            alert('🎉 Herzlichen Glückwunsch! Sie haben das interaktive Microlearning abgeschlossen. Ich freue mich auf unser Gespräch!');
        }
        
        function selectLearningType(type) {
            const recommendations = {
                visual: 'Für Sie würde ich visuelle Lernpfade mit Infografiken, interaktiven Diagrammen und Video-Tutorials entwickeln.',
                auditory: 'Ihr Lernprogramm würde Podcasts, Diskussionsrunden und Audio-basierte Microlearning-Module enthalten.',
                kinesthetic: 'Sie profitieren von Simulationen, praktischen Übungen und interaktiven Workshops.',
                reading: 'Ihr Programm würde strukturierte Texte, Checklisten und schriftliche Reflexionsaufgaben beinhalten.'
            };
            
            document.getElementById('learning-result').classList.remove('hidden');
            document.getElementById('learning-recommendation').textContent = recommendations[type];
            
            // Visual feedback
            document.querySelectorAll('.learning-type-btn').forEach(btn => {
                btn.classList.remove('ring-2', 'ring-blue-500');
            });
            event.target.closest('.learning-type-btn').classList.add('ring-2', 'ring-blue-500');
        }
        
        function scheduleCall() {
            alert('📅 Vielen Dank für Ihr Interesse! In einer echten Anwendung würde hier ein Kalendertool geöffnet werden.');
        }
        
        function downloadPortfolio() {
            alert('📁 Portfolio-Download würde hier starten. In der echten Version erhalten Sie meine vollständigen Projektbeispiele.');
        }
        
        // Close modal when clicking outside
        document.getElementById('modal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });
        
        // Memory Game Logic
        let memoryCards = [
            { id: 1, content: '🎯', match: 'Strategisch' },
            { id: 2, content: 'Strategisch', match: '🎯' },
            { id: 3, content: '🌍', match: 'Out of the box' },
            { id: 4, content: 'Out of the box', match: '🌍' },
            { id: 5, content: '📊', match: 'Messbar' },
            { id: 6, content: 'Messbar', match: '📊' },
            { id: 7, content: '🚀', match: 'Innovativ' },
            { id: 8, content: 'Innovativ', match: '🚀' }
        ];
        
        let flippedCards = [];
        let matchedPairs = 0;
        let attempts = 0;
        let gameInitialized = false;
        
        function initMemoryGame() {
            if (gameInitialized) return;
            
            const gameContainer = document.getElementById('memory-game');
            if (!gameContainer) return;
            
            // Shuffle cards
            const shuffledCards = [...memoryCards].sort(() => Math.random() - 0.5);
            
            gameContainer.innerHTML = '';
            shuffledCards.forEach((card, index) => {
                const cardElement = document.createElement('div');
                cardElement.className = 'memory-card bg-blue-600 hover:bg-blue-700 text-white rounded-lg p-3 cursor-pointer transition-all duration-300 text-center text-sm font-medium min-h-[60px] flex items-center justify-center';
                cardElement.dataset.cardId = card.id;
                cardElement.dataset.content = card.content;
                cardElement.dataset.match = card.match;
                cardElement.textContent = '?';
                cardElement.onclick = () => flipCard(cardElement);
                gameContainer.appendChild(cardElement);
            });
            
            gameInitialized = true;
        }
        
        function flipCard(cardElement) {
            if (flippedCards.length >= 2 || cardElement.classList.contains('flipped') || cardElement.classList.contains('matched')) {
                return;
            }
            
            cardElement.classList.add('flipped');
            cardElement.textContent = cardElement.dataset.content;
            cardElement.classList.remove('bg-blue-600', 'hover:bg-blue-700');
            cardElement.classList.add('bg-green-500');
            
            flippedCards.push(cardElement);
            
            if (flippedCards.length === 2) {
                attempts++;
                document.getElementById('game-score').textContent = `Versuche: ${attempts}`;
                
                setTimeout(() => {
                    checkMatch();
                }, 1000);
            }
        }
        
        function checkMatch() {
            const [card1, card2] = flippedCards;
            
            if (card1.dataset.content === card2.dataset.match || card1.dataset.match === card2.dataset.content) {
                // Match found
                card1.classList.add('matched');
                card2.classList.add('matched');
                card1.classList.remove('bg-green-500');
                card2.classList.remove('bg-green-500');
                card1.classList.add('bg-green-600');
                card2.classList.add('bg-green-600');
                
                matchedPairs++;
                
                if (matchedPairs === 4) {
                    document.getElementById('game-status').textContent = '🎉 Alle Paare gefunden!';
                    document.getElementById('game-complete').classList.remove('hidden');
                }
            } else {
                // No match
                card1.classList.remove('flipped', 'bg-green-500');
                card2.classList.remove('flipped', 'bg-green-500');
                card1.classList.add('bg-blue-600', 'hover:bg-blue-700');
                card2.classList.add('bg-blue-600', 'hover:bg-blue-700');
                card1.textContent = '?';
                card2.textContent = '?';
            }
            
            flippedCards = [];
        }
        
        function resetGame() {
            flippedCards = [];
            matchedPairs = 0;
            attempts = 0;
            gameInitialized = false;
            
            document.getElementById('game-score').textContent = 'Versuche: 0';
            document.getElementById('game-status').textContent = 'Klicken Sie auf zwei Karten, um sie umzudrehen';
            document.getElementById('game-complete').classList.add('hidden');
            
            initMemoryGame();
        }
        
        // Initialize memory game when module 6 is opened
        const originalOpenModule = openModule;
        openModule = function(moduleNumber) {
            originalOpenModule(moduleNumber);
            if (moduleNumber === 6) {
                setTimeout(() => {
                    initMemoryGame();
                }, 100);
            }
        };
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'96e19bb3727a1dd2',t:'MTc1NTAxODg1Ny4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
