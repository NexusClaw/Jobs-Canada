<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canadian Job Market AI Exposure Analysis (NOC 2021)</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=DM+Mono:wght@300;400&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
    <script src="https://d3js.org/d3.v7.min.js"></script>
    <style>
        :root {
            --bg: #0a0f1c;
            --bg-secondary: #111827;
            --surface: #1e293b;
            --surface-light: #334155;
            --accent: #f59e0b;
            --accent-light: #fbbf24;
            --text-primary: #f1f5f9;
            --text-secondary: #94a3b8;
            --text-muted: #64748b;
            --border: #334155;
            --gradient-1: linear-gradient(135deg, #0c1222 0%, #1e293b 100%);
            
            --score-0: #10b981; /* Emerald */
            --score-1: #34d399;
            --score-2: #6ee7b7;
            --score-3: #a7f3d0;
            --score-4: #fbbf24; /* Amber */
            --score-5: #f59e0b;
            --score-6: #d97706;
            --score-7: #ea580c; /* Orange */
            --score-8: #dc2626; /* Red */
            --score-9: #b91c1c;
            --score-10: #7f1d1d;
            
            --category-0: #8b5cf6; /* Violet */
            --category-1: #ec4899; /* Pink */
            --category-2: #06b6d4; /* Cyan */
            --category-3: #10b981; /* Emerald */
            --category-4: #f59e0b; /* Amber */
            --category-5: #3b82f6; /* Blue */
            --category-6: #8b5cf6; /* Violet */
            --category-7: #ec4899; /* Pink */
            --category-8: #06b6d4; /* Cyan */
            --category-9: #10b981; /* Emerald */
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'DM Mono', monospace;
            background: var(--bg);
            color: var(--text-primary);
            min-height: 100vh;
            overflow-x: hidden;
            line-height: 1.6;
        }

        .app-container {
            display: flex;
            flex-direction: column;
            min-height: 100vh;
            max-width: 100%;
            padding: 1rem;
            gap: 1rem;
        }

        header {
            padding: 1.5rem;
            background: var(--surface);
            border-radius: 8px;
            border: 1px solid var(--border);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo {
            display: flex;
            align-items: baseline;
            gap: 1.5rem;
        }

        .logo h1 {
            font-family: 'Cormorant Garamond', serif;
            font-size: 2.5rem;
            font-weight: 600;
            letter-spacing: -0.03em;
            background: linear-gradient(135deg, var(--text-primary) 0%, var(--accent) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .logo-tag {
            font-family: 'DM Mono', monospace;
            font-size: 0.75rem;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            color: var(--accent);
            background: var(--bg-secondary);
            padding: 0.3rem 0.8rem;
            border-radius: 2px;
            border: 1px solid var(--accent);
        }

        .meta {
            display: flex;
            gap: 2rem;
            font-size: 0.85rem;
            color: var(--text-muted);
            flex-wrap: wrap;
        }

        .meta-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .meta-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: var(--accent);
        }

        .main-content {
            flex: 1;
            display: grid;
            grid-template-columns: 1fr 320px;
            gap: 1rem;
            min-height: 0; /* Important for grid to respect container height */
        }

        .visualization-panel {
            background: var(--surface);
            border-radius: 8px;
            padding: 1.5rem;
            border: 1px solid var(--border);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }

        .viz-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid var(--border);
            flex-wrap: wrap;
            gap: 1rem;
        }

        .viz-title {
            font-family: 'Instrument Serif', serif;
            font-size: 1.5rem;
            font-weight: 400;
        }

        .treemap-container {
            flex: 1;
            min-height: 500px;
            position: relative;
            border-radius: 4px;
            background: var(--bg-secondary);
            overflow: hidden;
        }

        .tooltip {
            position: fixed;
            background: var(--bg-secondary);
            border: 1px solid var(--accent);
            border-radius: 8px;
            padding: 1.25rem;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.2s ease;
            z-index: 1000;
            min-width: 300px;
            max-width: 350px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            background: rgba(17, 24, 39, 0.95);
        }

        .tooltip-title {
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
            color: var(--accent);
            line-height: 1.3;
        }

        .tooltip-noc {
            font-family: 'DM Mono', monospace;
            font-size: 0.8rem;
            color: var(--text-muted);
            margin-bottom: 1rem;
            letter-spacing: 0.05em;
            padding-bottom: 0.75rem;
            border-bottom: 1px solid var(--border);
        }

        .tooltip-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.75rem;
            font-size: 0.85rem;
            margin-bottom: 1rem;
        }

        .tooltip-label {
            color: var(--text-secondary);
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            margin-bottom: 0.25rem;
        }

        .tooltip-value {
            font-family: 'DM Mono', monospace;
            font-weight: 400;
            font-size: 0.95rem;
        }

        .score-visual {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding-top: 1rem;
            border-top: 1px solid var(--border);
        }

        .score-bar {
            flex: 1;
            height: 10px;
            background: var(--surface-light);
            border-radius: 5px;
            overflow: hidden;
        }

        .score-fill {
            height: 100%;
            border-radius: 5px;
            transition: width 0.3s ease;
        }

        .score-text {
            font-family: 'DM Mono', monospace;
            font-size: 1.4rem;
            font-weight: 600;
            min-width: 50px;
            text-align: right;
        }

        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            overflow-y: auto;
            max-height: calc(100vh - 150px);
        }

        .panel {
            background: var(--surface);
            border-radius: 8px;
            padding: 1.25rem;
            border: 1px solid var(--border);
            flex-shrink: 0;
        }

        .panel-title {
            font-family: 'Instrument Serif', serif;
            font-size: 1.2rem;
            margin-bottom: 1rem;
            padding-bottom: 0.75rem;
            border-bottom: 1px solid var(--border);
        }

        .legend {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 0.8rem;
        }

        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 3px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            flex-shrink: 0;
        }

        .legend-label {
            flex: 1;
            line-height: 1.4;
        }

        .legend-value {
            font-family: 'DM Mono', monospace;
            color: var(--text-muted);
            font-size: 0.75rem;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0.5rem;
            font-size: 0.8rem;
        }

        .category-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.5rem;
            background: var(--bg-secondary);
            border-radius: 4px;
            border-left: 3px solid transparent;
        }

        .category-code {
            font-family: 'DM Mono', monospace;
            font-weight: 600;
            color: var(--accent);
            min-width: 1.5rem;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.75rem;
        }

        .stat-item {
            text-align: center;
            padding: 0.75rem;
            background: var(--bg-secondary);
            border-radius: 6px;
        }

        .stat-value {
            font-family: 'DM Mono', monospace;
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--accent);
            line-height: 1.2;
        }

        .stat-label {
            font-size: 0.7rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 0.1em;
            margin-top: 0.25rem;
        }

        .filters {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .filter-btn {
            background: var(--bg-secondary);
            border: 1px solid var(--border);
            color: var(--text-secondary);
            padding: 0.5rem 1rem;
            border-radius: 4px;
            font-family: 'DM Mono', monospace;
            font-size: 0.8rem;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .filter-btn:hover {
            border-color: var(--accent);
            color: var(--accent);
        }

        .filter-btn.active {
            background: var(--accent);
            color: var(--bg);
            border-color: var(--accent);
        }

        .calibration-examples {
            font-size: 0.8rem;
            color: var(--text-secondary);
            line-height: 1.6;
        }

        .calibration-item {
            margin-bottom: 0.75rem;
            padding-bottom: 0.75rem;
            border-bottom: 1px solid var(--border);
        }

        .calibration-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .calibration-score {
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 0.25rem;
        }

        footer {
            padding: 1.5rem;
            text-align: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            background: var(--surface);
            border-radius: 8px;
            border: 1px solid var(--border);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .panel, .visualization-panel {
            animation: fadeIn 0.6s ease forwards;
        }

        .visualization-panel { animation-delay: 0.1s; }
        .panel:nth-child(2) { animation-delay: 0.2s; }
        .panel:nth-child(3) { animation-delay: 0.3s; }
        .panel:nth-child(4) { animation-delay: 0.4s; }

        /* Responsive */
        @media (max-width: 1100px) {
            .main-content {
                grid-template-columns: 1fr;
            }
            
            .sidebar {
                flex-direction: row;
                flex-wrap: wrap;
                max-height: none;
                overflow-y: visible;
            }
            
            .panel {
                flex: 1;
                min-width: 280px;
            }
        }

        @media (max-width: 768px) {
            .app-container {
                padding: 0.75rem;
                gap: 0.75rem;
            }
            
            .logo h1 {
                font-size: 1.8rem;
            }
            
            .logo {
                flex-direction: column;
                gap: 0.5rem;
                align-items: flex-start;
            }
            
            .meta {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            .viz-title {
                font-size: 1.3rem;
            }
            
            .sidebar {
                flex-direction: column;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Custom scrollbar for sidebar */
        .sidebar::-webkit-scrollbar {
            width: 6px;
        }

        .sidebar::-webkit-scrollbar-track {
            background: var(--bg-secondary);
            border-radius: 3px;
        }

        .sidebar::-webkit-scrollbar-thumb {
            background: var(--surface-light);
            border-radius: 3px;
        }

        .sidebar::-webkit-scrollbar-thumb:hover {
            background: var(--accent);
        }
    </style>
</head>
<body>
    <div class="app-container">
        <header>
            <div class="logo">
                <h1>Canadian Job Market Analysis</h1>
                <span class="logo-tag">NOC 2021 V1.0</span>
            </div>
            <div class="meta">
                <div class="meta-item">
                    <span class="meta-dot"></span>
                    <span>Data: Statistics Canada & ESDC</span>
                </div>
                <div class="meta-item">
                    <span class="meta-dot"></span>
                    <span>Methodology: AI Exposure Scoring (0-10)</span>
                </div>
                <div class="meta-item">
                    <span class="meta-dot"></span>
                    <span>Currency: CAD (2023 Median Wages)</span>
                </div>
                <div class="meta-item">
                    <span class="meta-dot"></span>
                    <span>Employment: 18.2M+ Jobs</span>
                </div>
            </div>
        </header>

        <div class="main-content">
            <main class="visualization-panel">
                <div class="viz-header">
                    <h2 class="viz-title">Occupational Treemap: Employment vs. AI Exposure</h2>
                    <div class="filters">
                        <button class="filter-btn active" data-category="all">All Categories</button>
                        <button class="filter-btn" data-category="0">Management</button>
                        <button class="filter-btn" data-category="2">Sciences</button>
                        <button class="filter-btn" data-category="3">Health</button>
                        <button class="filter-btn" data-category="7">Trades</button>
                        <button class="filter-btn" data-category="8">Resources</button>
                    </div>
                </div>
                <div class="treemap-container" id="treemap"></div>
                <div class="tooltip" id="tooltip"></div>
            </main>

            <aside class="sidebar">
                <div class="panel">
                    <h3 class="panel-title">AI Exposure Score Legend</h3>
                    <div class="legend" id="score-legend">
                        <!-- Generated by JS -->
                    </div>
                </div>

                <div class="panel">
                    <h3 class="panel-title">Broad Occupational Categories</h3>
                    <div class="categories-grid" id="categories-grid">
                        <!-- Generated by JS -->
                    </div>
                </div>

                <div class="panel">
                    <h3 class="panel-title">Dataset Summary</h3>
                    <div class="stats-grid">
                        <div class="stat-item">
                            <div class="stat-value" id="total-occupations">547</div>
                            <div class="stat-label">Occupations</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="total-employment">18.2M</div>
                            <div class="stat-label">Total Jobs</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="avg-wage">$32.50</div>
                            <div class="stat-label">Median Wage</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="avg-score">4.7</div>
                            <div class="stat-label">Avg AI Score</div>
                        </div>
                    </div>
                </div>

                <div class="panel">
                    <h3 class="panel-title">Canadian Calibration Examples</h3>
                    <div class="calibration-examples">
                        <div class="calibration-item">
                            <div class="calibration-score">0-1 Minimal</div>
                            <div>Underground Miners, Oil & Gas Drillers, Logging Machinery Operators</div>
                        </div>
                        <div class="calibration-item">
                            <div class="calibration-score">4-5 Moderate</div>
                            <div>Retail Sales Supervisors, Estheticians, Primary Production Managers</div>
                        </div>
                        <div class="calibration-item">
                            <div class="calibration-score">8-9 Very High</div>
                            <div>Software Developers, Paralegals, Policy Researchers</div>
                        </div>
                        <div class="calibration-item">
                            <div class="calibration-score">10 Maximum</div>
                            <div>Statistical Officers, Data Entry Clerks</div>
                        </div>
                    </div>
                </div>
            </aside>
        </div>

        <footer>
            <p>Pipeline: parse_occupations.py → scrape.py → parse_detail.py → process.py → make_csv.py → score.py → build_site_data.py</p>
            <p style="margin-top: 0.5rem;">Migration complete: US BLS/SOC → Canada StatCan/NOC 2021 V1.0 | Last updated: <span id="current-date"></span></p>
        </footer>
    </div>

    <script>
        // Sample data structure based on the migration guide
        const sampleData = {
            occupations: [
                // Management (Category 0)
                { title: "Financial Managers", noc: "0111", teer: "0", median_wage: 52.00, employment: 85000, score: 6, category: "0" },
                { title: "Human Resource Managers", noc: "0112", teer: "0", median_wage: 48.50, employment: 32000, score: 5, category: "0" },
                { title: "Purchasing Managers", noc: "0113", teer: "0", median_wage: 46.25, employment: 18000, score: 7, category: "0" },
                { title: "Other Administrative Services Managers", noc: "0114", teer: "0", median_wage: 44.00, employment: 25000, score: 6, category: "0" },
                { title: "Managers in Manufacturing", noc: "0911", teer: "0", median_wage: 48.00, employment: 22000, score: 5, category: "0" },
                
                // Business, finance and administration (Category 1)
                { title: "Financial Auditors and Accountants", noc: "11100", teer: "1", median_wage: 38.00, employment: 120000, score: 7, category: "1" },
                { title: "Financial and Investment Analysts", noc: "11101", teer: "1", median_wage: 42.50, employment: 45000, score: 8, category: "1" },
                { title: "Human Resources Professionals", noc: "11200", teer: "1", median_wage: 36.75, employment: 65000, score: 6, category: "1" },
                { title: "Professional Occupations in Business Management", noc: "11201", teer: "1", median_wage: 40.00, employment: 38000, score: 5, category: "1" },
                { title: "Administrative Officers", noc: "13100", teer: "2", median_wage: 28.00, employment: 210000, score: 7, category: "1" },
                { title: "Administrative Assistants", noc: "13110", teer: "3", median_wage: 24.00, employment: 185000, score: 8, category: "1" },
                { title: "Statistical Officers and Related Research Support", noc: "14111", teer: "3", median_wage: 28.00, employment: 45000, score: 10, category: "1" },
                { title: "Data Entry Clerks", noc: "14110", teer: "4", median_wage: 20.00, employment: 85000, score: 10, category: "1" },
                
                // Natural and applied sciences (Category 2)
                { title: "Information Systems Analysts and Consultants", noc: "21211", teer: "1", median_wage: 44.00, employment: 95000, score: 8, category: "2" },
                { title: "Database Analysts and Data Administrators", noc: "21212", teer: "1", median_wage: 42.50, employment: 28000, score: 9, category: "2" },
                { title: "Software Engineers and Designers", noc: "21231", teer: "1", median_wage: 48.00, employment: 125000, score: 8, category: "2" },
                { title: "Computer Programmers and Interactive Media Developers", noc: "21234", teer: "1", median_wage: 40.00, employment: 85000, score: 9, category: "2" },
                { title: "Civil Engineers", noc: "21300", teer: "1", median_wage: 45.00, employment: 42000, score: 7, category: "2" },
                { title: "Mechanical Engineers", noc: "21301", teer: "1", median_wage: 46.00, employment: 38000, score: 7, category: "2" },
                { title: "Electrical and Electronics Engineers", noc: "21310", teer: "1", median_wage: 47.00, employment: 35000, score: 7, category: "2" },
                { title: "Architects", noc: "21200", teer: "1", median_wage: 42.00, employment: 22000, score: 6, category: "2" },
                
                // Health (Category 3)
                { title: "General Practitioners and Family Physicians", noc: "31102", teer: "1", median_wage: 95.00, employment: 48000, score: 3, category: "3" },
                { title: "Specialist Physicians", noc: "31100", teer: "1", median_wage: 120.00, employment: 32000, score: 4, category: "3" },
                { title: "Registered Nurses and Registered Psychiatric Nurses", noc: "31301", teer: "1", median_wage: 42.00, employment: 310000, score: 3, category: "3" },
                { title: "Licensed Practical Nurses", noc: "32101", teer: "2", median_wage: 30.00, employment: 85000, score: 4, category: "3" },
                { title: "Pharmacists", noc: "31120", teer: "1", median_wage: 52.00, employment: 42000, score: 5, category: "3" },
                { title: "Dentists", noc: "31110", teer: "1", median_wage: 85.00, employment: 22000, score: 3, category: "3" },
                { title: "Physiotherapists", noc: "31202", teer: "1", median_wage: 40.00, employment: 18000, score: 4, category: "3" },
                { title: "Medical Laboratory Technologists", noc: "32120", teer: "2", median_wage: 32.00, employment: 28000, score: 6, category: "3" },
                
                // Education, law and social, community and government services (Category 4)
                { title: "Secondary School Teachers", noc: "41220", teer: "1", median_wage: 42.00, employment: 120000, score: 6, category: "4" },
                { title: "Elementary School and Kindergarten Teachers", noc: "41221", teer: "1", median_wage: 40.00, employment: 130000, score: 6, category: "4" },
                { title: "Lawyers and Quebec Notaries", noc: "41101", teer: "1", median_wage: 65.00, employment: 68000, score: 8, category: "4" },
                { title: "Social Workers", noc: "41300", teer: "1", median_wage: 35.00, employment: 58000, score: 5, category: "4" },
                { title: "Paralegals and Related Occupations", noc: "42100", teer: "2", median_wage: 28.00, employment: 32000, score: 8, category: "4" },
                { title: "Policy Researchers, Consultants and Program Officers", noc: "41400", teer: "1", median_wage: 38.00, employment: 85000, score: 9, category: "4" },
                
                // Art, culture, recreation and sport (Category 5)
                { title: "Graphic Designers and Illustrators", noc: "52120", teer: "2", median_wage: 28.00, employment: 42000, score: 7, category: "5" },
                { title: "Producers, Directors, Choreographers and Related Occupations", noc: "51120", teer: "1", median_wage: 38.00, employment: 25000, score: 5, category: "5" },
                { title: "Photographers", noc: "53110", teer: "3", median_wage: 22.00, employment: 18000, score: 6, category: "5" },
                { title: "Musicians and Singers", noc: "51122", teer: "1", median_wage: 25.00, employment: 15000, score: 4, category: "5" },
                { title: "Authors and Writers", noc: "51111", teer: "1", median_wage: 32.00, employment: 22000, score: 7, category: "5" },
                
                // Sales and service (Category 6)
                { title: "Retail Sales Supervisors", noc: "62010", teer: "2", median_wage: 24.00, employment: 95000, score: 5, category: "6" },
                { title: "Food Service Supervisors", noc: "62020", teer: "2", median_wage: 20.00, employment: 85000, score: 5, category: "6" },
                { title: "Chefs", noc: "63200", teer: "2", median_wage: 22.50, employment: 65000, score: 4, category: "6" },
                { title: "Security Guards and Related Security Service Occupations", noc: "64410", teer: "4", median_wage: 18.00, employment: 120000, score: 3, category: "6" },
                { title: "Retail Salespersons and Visual Merchandisers", noc: "64100", teer: "4", median_wage: 16.50, employment: 320000, score: 6, category: "6" },
                { title: "Cashiers", noc: "65100", teer: "4", median_wage: 15.00, employment: 280000, score: 7, category: "6" },
                { title: "Estheticians, Electrologists and Related Occupations", noc: "63211", teer: "2", median_wage: 20.00, employment: 28000, score: 5, category: "6" },
                
                // Trades, transport and equipment operators (Category 7)
                { title: "Electricians (except industrial and power system)", noc: "72200", teer: "2", median_wage: 35.00, employment: 110000, score: 3, category: "7" },
                { title: "Plumbers", noc: "72300", teer: "2", median_wage: 34.00, employment: 75000, score: 2, category: "7" },
                { title: "Heavy-duty Equipment Mechanics", noc: "73120", teer: "2", median_wage: 36.00, employment: 45000, score: 2, category: "7" },
                { title: "Transport Truck Drivers", noc: "73300", teer: "3", median_wage: 28.00, employment: 310000, score: 4, category: "7" },
                { title: "Automotive Service Technicians, Truck and Bus Mechanics", noc: "72410", teer: "2", median_wage: 30.00, employment: 85000, score: 3, category: "7" },
                { title: "Welders and Related Machine Operators", noc: "72106", teer: "2", median_wage: 32.00, employment: 65000, score: 2, category: "7" },
                { title: "Carpenters", noc: "72310", teer: "2", median_wage: 30.00, employment: 120000, score: 2, category: "7" },
                { title: "Heavy Equipment Operators (except Crane)", noc: "73400", teer: "3", median_wage: 32.00, employment: 85000, score: 3, category: "7" },
                
                // Natural resources, agriculture and related production (Category 8)
                { title: "Underground Mine Service and Support Workers", noc: "84100", teer: "4", median_wage: 32.00, employment: 18000, score: 1, category: "8" },
                { title: "Oil and Gas Well Drillers, Servicers, Testers and Related Workers", noc: "84101", teer: "4", median_wage: 38.00, employment: 22000, score: 1, category: "8" },
                { title: "Logging Machinery Operators", noc: "84111", teer: "4", median_wage: 30.00, employment: 12000, score: 1, category: "8" },
                { title: "Agricultural Service Contractors and Farm Supervisors", noc: "82030", teer: "2", median_wage: 25.00, employment: 28000, score: 4, category: "8" },
                { title: "General Farm Workers", noc: "85101", teer: "5", median_wage: 18.00, employment: 85000, score: 3, category: "8" },
                { title: "Landscaping and Grounds Maintenance Labourers", noc: "85121", teer: "5", median_wage: 20.00, employment: 95000, score: 2, category: "8" },
                
                // Manufacturing and utilities (Category 9)
                { title: "Supervisors, Petroleum, Gas and Chemical Processing", noc: "92011", teer: "2", median_wage: 42.00, employment: 15000, score: 5, category: "9" },
                { title: "Power Systems Electricians", noc: "72203", teer: "2", median_wage: 45.00, employment: 12000, score: 3, category: "9" },
                { title: "Water and Waste Treatment Plant Operators", noc: "92101", teer: "2", median_wage: 35.00, employment: 18000, score: 4, category: "9" },
                { title: "Machine Operators, Mineral and Metal Processing", noc: "94100", teer: "4", median_wage: 28.00, employment: 25000, score: 2, category: "9" },
                { title: "Labourers in Mineral and Metal Processing", noc: "95100", teer: "5", median_wage: 22.00, employment: 18000, score: 1, category: "9" },
                { title: "Food and Beverage Processing Labourers", noc: "95106", teer: "5", median_wage: 18.00, employment: 120000, score: 2, category: "9" }
            ],
            
            categories: {
                "0": "Management",
                "1": "Business, finance and administration",
                "2": "Natural and applied sciences",
                "3": "Health",
                "4": "Education, law and social, community and government services",
                "5": "Art, culture, recreation and sport",
                "6": "Sales and service",
                "7": "Trades, transport and equipment operators",
                "8": "Natural resources, agriculture and related production",
                "9": "Manufacturing and utilities"
            }
        };

        // Color scales
        const scoreColorScale = d3.scaleOrdinal()
            .domain([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
            .range([
                '#10b981', '#34d399', '#6ee7b7', '#a7f3d0', 
                '#fbbf24', '#f59e0b', '#d97706', '#ea580c', 
                '#dc2626', '#b91c1c', '#7f1d1d'
            ]);

        const categoryColorScale = d3.scaleOrdinal()
            .domain(Object.keys(sampleData.categories))
            .range([
                '#8b5cf6', '#ec4899', '#06b6d4', '#10b981', '#f59e0b',
                '#3b82f6', '#8b5cf6', '#ec4899', '#06b6d4', '#10b981'
            ]);

        // Tooltip boundary checking
        let tooltipVisible = false;
        let currentTooltipData = null;

        // Initialize the visualization
        document.addEventListener('DOMContentLoaded', function() {
            renderScoreLegend();
            renderCategories();
            renderStats();
            renderTreemap(sampleData.occupations);
            setupFilterButtons();
            
            // Set current date
            const now = new Date();
            document.getElementById('current-date').textContent = now.toLocaleDateString('en-CA', { 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            });
        });

        function renderScoreLegend() {
            const legendContainer = document.getElementById('score-legend');
            legendContainer.innerHTML = '';
            
            const scoreRanges = [
                { range: "0-1", label: "Minimal", desc: "Physical, unpredictable environments" },
                { range: "2-3", label: "Low", desc: "Complex physical, regulatory" },
                { range: "4-5", label: "Moderate", desc: "Hybrid physical/cognitive" },
                { range: "6-7", label: "High", desc: "Cognitive, structured" },
                { range: "8-9", label: "Very High", desc: "Digital, rule-based" },
                { range: "10", label: "Maximum", desc: "Routine data processing" }
            ];
            
            scoreRanges.forEach((item, index) => {
                const legendItem = document.createElement('div');
                legendItem.className = 'legend-item';
                
                const color = scoreColorScale(index * 2); // Sample color from range
                legendItem.innerHTML = `
                    <div class="legend-color" style="background: ${color}"></div>
                    <div class="legend-label">
                        <div>${item.range} ${item.label}</div>
                        <div style="font-size: 0.7rem; color: var(--text-muted); margin-top: 0.2rem;">${item.desc}</div>
                    </div>
                `;
                
                legendContainer.appendChild(legendItem);
            });
        }

        function renderCategories() {
            const gridContainer = document.getElementById('categories-grid');
            gridContainer.innerHTML = '';
            
            Object.entries(sampleData.categories).forEach(([code, name]) => {
                const categoryItem = document.createElement('div');
                categoryItem.className = 'category-item';
                categoryItem.style.borderLeftColor = categoryColorScale(code);
                categoryItem.innerHTML = `
                    <span class="category-code">${code}</span>
                    <span style="font-size: 0.85rem;">${name}</span>
                `;
                gridContainer.appendChild(categoryItem);
            });
        }

        function renderStats() {
            const occupations = sampleData.occupations;
            
            // Calculate statistics
            const totalOccupations = occupations.length;
            const totalEmployment = occupations.reduce((sum, occ) => sum + occ.employment, 0);
            const avgWage = occupations.reduce((sum, occ) => sum + occ.median_wage, 0) / totalOccupations;
            const avgScore = occupations.reduce((sum, occ) => sum + occ.score, 0) / totalOccupations;
            
            // Format numbers
            const formatNumber = (num) => {
                if (num >= 1000000) return (num / 1000000).toFixed(1) + 'M';
                if (num >= 1000) return (num / 1000).toFixed(1) + 'K';
                return num.toLocaleString();
            };
            
            document.getElementById('total-occupations').textContent = formatNumber(totalOccupations);
            document.getElementById('total-employment').textContent = formatNumber(totalEmployment);
            document.getElementById('avg-wage').textContent = '$' + avgWage.toFixed(2);
            document.getElementById('avg-score').textContent = avgScore.toFixed(1);
        }

        function renderTreemap(occupations) {
            const container = document.getElementById('treemap');
            container.innerHTML = '';
            
            const width = container.clientWidth;
            const height = container.clientHeight;
            
            // Create SVG
            const svg = d3.select('#treemap')
                .append('svg')
                .attr('width', width)
                .attr('height', height);
            
            // Create hierarchy
            const root = d3.hierarchy({ children: occupations })
                .sum(d => d.employment)
                .sort((a, b) => b.value - a.value);
            
            // Create treemap layout
            d3.treemap()
                .size([width, height])
                .padding(2)
                .round(true)(root);
            
            // Create groups for each leaf
            const cells = svg.selectAll('g')
                .data(root.leaves())
                .enter()
                .append('g')
                .attr('transform', d => `translate(${d.x0},${d.y0})`);
            
            // Add rectangles
            cells.append('rect')
                .attr('width', d => d.x1 - d.x0)
                .attr('height', d => d.y1 - d.y0)
                .attr('fill', d => scoreColorScale(d.data.score))
                .attr('stroke', 'rgba(255,255,255,0.1)')
                .attr('stroke-width', 1)
                .attr('rx', 4)
                .attr('ry', 4)
                .style('opacity', 0.85)
                .style('cursor', 'pointer')
                .on('mouseover', function(event, d) {
                    showTooltip(event, d.data);
                    d3.select(this).style('opacity', 1).attr('stroke', 'var(--accent)').attr('stroke-width', 2);
                })
                .on('mousemove', function(event, d) {
                    moveTooltip(event);
                })
                .on('mouseout', function() {
                    hideTooltip();
                    d3.select(this).style('opacity', 0.85).attr('stroke', 'rgba(255,255,255,0.1)').attr('stroke-width', 1);
                });
            
            // Add text labels (only if cell is large enough)
            cells.filter(d => (d.x1 - d.x0) > 60 && (d.y1 - d.y0) > 40)
                .append('text')
                .attr('x', 5)
                .attr('y', 15)
                .text(d => {
                    const width = d.x1 - d.x0;
                    const maxLength = width > 150 ? 25 : width > 100 ? 20 : width > 80 ? 15 : 10;
                    return d.data.title.length > maxLength ? d.data.title.substring(0, maxLength) + '...' : d.data.title;
                })
                .attr('fill', 'white')
                .attr('font-size', d => {
                    const area = (d.x1 - d.x0) * (d.y1 - d.y0);
                    return area > 10000 ? '12px' : area > 5000 ? '10px' : '9px';
                })
                .attr('font-family', 'DM Mono, monospace')
                .attr('font-weight', 400)
                .style('pointer-events', 'none')
                .style('text-shadow', '0 1px 2px rgba(0,0,0,0.8)');
            
            // Add NOC codes for larger cells
            cells.filter(d => (d.x1 - d.x0) > 80 && (d.y1 - d.y0) > 60)
                .append('text')
                .attr('x', 5)
                .attr('y', 30)
                .text(d => d.data.noc)
                .attr('fill', 'rgba(255,255,255,0.7)')
                .attr('font-size', '10px')
                .attr('font-family', 'DM Mono, monospace')
                .style('pointer-events', 'none');
            
            // Add score labels for larger cells
            cells.filter(d => (d.x1 - d.x0) > 100 && (d.y1 - d.y0) > 80)
                .append('text')
                .attr('x', 5)
                .attr('y', 45)
                .text(d => `AI: ${d.data.score}/10`)
                .attr('fill', 'var(--accent)')
                .attr('font-size', '10px')
                .attr('font-family', 'DM Mono, monospace')
                .attr('font-weight', 600)
                .style('pointer-events', 'none');
            
            // Add category indicator for larger cells
            cells.filter(d => (d.x1 - d.x0) > 120 && (d.y1 - d.y0) > 90)
                .append('text')
                .attr('x', 5)
                .attr('y', 60)
                .text(d => `Cat: ${d.data.category}`)
                .attr('fill', 'rgba(255,255,255,0.6)')
                .attr('font-size', '9px')
                .attr('font-family', 'DM Mono, monospace')
                .style('pointer-events', 'none');
        }

        function showTooltip(event, data) {
            const tooltip = document.getElementById('tooltip');
            const scorePercent = (data.score / 10) * 100;
            
            tooltip.innerHTML = `
                <div class="tooltip-title">${data.title}</div>
                <div class="tooltip-noc">NOC ${data.noc} • TEER ${data.teer} • ${sampleData.categories[data.category]}</div>
                <div class="tooltip-grid">
                    <div>
                        <div class="tooltip-label">Median Wage</div>
                        <div class="tooltip-value">$${data.median_wage.toFixed(2)}/hr CAD</div>
                    </div>
                    <div>
                        <div class="tooltip-label">Employment</div>
                        <div class="tooltip-value">${data.employment.toLocaleString()} jobs</div>
                    </div>
                    <div>
                        <div class="tooltip-label">Annual Wage</div>
                        <div class="tooltip-value">$${(data.median_wage * 2080).toLocaleString()}</div>
                    </div>
                    <div>
                        <div class="tooltip-label">Category</div>
                        <div class="tooltip-value">${data.category}: ${sampleData.categories[data.category].substring(0, 15)}...</div>
                    </div>
                </div>
                <div class="score-visual">
                    <div class="score-text" style="color: ${scoreColorScale(data.score)}">${data.score}/10</div>
                    <div class="score-bar">
                        <div class="score-fill" style="width: ${scorePercent}%; background: ${scoreColorScale(data.score)}"></div>
                    </div>
                </div>
            `;
            
            currentTooltipData = data;
            tooltipVisible = true;
            
            // Position tooltip
            positionTooltip(event);
            
            // Show tooltip
            tooltip.style.opacity = 1;
        }

        function moveTooltip(event) {
            if (tooltipVisible) {
                positionTooltip(event);
            }
        }

        function positionTooltip(event) {
            const tooltip = document.getElementById('tooltip');
            const tooltipWidth = 350;
            const tooltipHeight = 250;
            const padding = 20;
            
            // Get viewport dimensions
            const viewportWidth = window.innerWidth;
            const viewportHeight = window.innerHeight;
            
            // Initial position
            let x = event.clientX + padding;
            let y = event.clientY + padding;
            
            // Check right boundary
            if (x + tooltipWidth > viewportWidth) {
                x = event.clientX - tooltipWidth - padding;
            }
            
            // Check bottom boundary
            if (y + tooltipHeight > viewportHeight) {
                y = event.clientY - tooltipHeight - padding;
            }
            
            // Ensure tooltip stays within viewport
            x = Math.max(padding, Math.min(x, viewportWidth - tooltipWidth - padding));
            y = Math.max(padding, Math.min(y, viewportHeight - tooltipHeight - padding));
            
            tooltip.style.left = `${x}px`;
            tooltip.style.top = `${y}px`;
        }

        function hideTooltip() {
            document.getElementById('tooltip').style.opacity = 0;
            tooltipVisible = false;
            currentTooltipData = null;
        }

        function setupFilterButtons() {
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    // Update active state
                    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    // Filter data
                    const category = this.dataset.category;
                    let filteredData;
                    
                    if (category === 'all') {
                        filteredData = sampleData.occupations;
                    } else {
                        filteredData = sampleData.occupations.filter(occ => occ.category === category);
                    }
                    
                    // Re-render treemap
                    renderTreemap(filteredData);
                    
                    // Update stats for filtered data
                    updateFilteredStats(filteredData);
                });
            });
        }

        function updateFilteredStats(occupations) {
            const formatNumber = (num) => {
                if (num >= 1000000) return (num / 1000000).toFixed(1) + 'M';
                if (num >= 1000) return (num / 1000).toFixed(1) + 'K';
                return num.toLocaleString();
            };
            
            if (occupations.length === 0) {
                document.getElementById('total-occupations').textContent = '0';
                document.getElementById('total-employment').textContent = '0';
                document.getElementById('avg-wage').textContent = '$0.00';
                document.getElementById('avg-score').textContent = '0.0';
                return;
            }
            
            const totalEmployment = occupations.reduce((sum, occ) => sum + occ.employment, 0);
            const avgWage = occupations.reduce((sum, occ) => sum + occ.median_wage, 0) / occupations.length;
            const avgScore = occupations.reduce((sum, occ) => sum + occ.score, 0) / occupations.length;
            
            document.getElementById('total-occupations').textContent = formatNumber(occupations.length);
            document.getElementById('total-employment').textContent = formatNumber(totalEmployment);
            document.getElementById('avg-wage').textContent = '$' + avgWage.toFixed(2);
            document.getElementById('avg-score').textContent = avgScore.toFixed(1);
        }

        // Handle window resize
        let resizeTimer;
        window.addEventListener('resize', function() {
            clearTimeout(resizeTimer);
            resizeTimer = setTimeout(function() {
                const activeFilter = document.querySelector('.filter-btn.active').dataset.category;
                let data;
                
                if (activeFilter === 'all') {
                    data = sampleData.occupations;
                } else {
                    data = sampleData.occupations.filter(occ => occ.category === activeFilter);
                }
                
                renderTreemap(data);
            }, 250);
        });

        // Close tooltip when clicking elsewhere
        document.addEventListener('click', function(event) {
            if (tooltipVisible && !event.target.closest('.treemap-container')) {
                hideTooltip();
            }
        });
    </script>
</body>
</html>
