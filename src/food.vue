<script setup lang="ts">
import mbagasLogo from './assets/mbagas.svg'

defineProps<{
  onBack?: () => void
}>()
</script>

<template>
  <div class="min-h-screen bg-[#fdfbf7] text-[#222222] font-sans antialiased selection:bg-[#d9822b] selection:text-white">
    
    <!-- Header / Navbar -->
    <header class="max-w-6xl mx-auto px-6 py-6 flex items-center justify-between border-b border-[#eae6de]">
      <div class="flex items-center gap-2">
        <img :src="mbagasLogo" alt="M Bagas Logo" class="w-9 h-9" />
      </div>

      <nav class="hidden md:flex items-center gap-8 text-xs font-semibold tracking-wider text-[#555]">
        <button v-if="onBack" @click="onBack" class="hover:text-[#d9822b] transition-colors bg-transparent border-none cursor-pointer p-0 text-xs font-semibold tracking-wider text-[#555]">HOME</button>
        <a href="#overview" class="hover:text-[#d9822b] transition-colors">OVERVIEW</a>
        <a href="#pipeline" class="hover:text-[#d9822b] transition-colors">PIPELINE</a>
        <a href="#dashboard" class="hover:text-[#d9822b] transition-colors">DASHBOARD</a>
        <a href="#eda" class="hover:text-[#d9822b] transition-colors">EDA</a>
        <a href="#conclusion" class="hover:text-[#d9822b] transition-colors">CONCLUSION</a>
      </nav>
    </header>

    <!-- Hero Section -->
    <section id="overview" class="max-w-6xl mx-auto px-6 pt-16 pb-20 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
      <div class="lg:col-span-6 space-y-6">
        <div class="inline-block text-[11px] font-bold tracking-widest text-[#d9822b] uppercase bg-[#f5efe6] px-3 py-1 rounded">
          CASE STUDY · POWER BI & COMMERCE ANALYTICS
        </div>
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-normal leading-[1.1] tracking-tight text-[#111]">
          Food & Feed Sales <br />
          <span class="text-[#d9822b] font-medium">Performance Dashboard</span>
        </h1>
        <p class="text-base sm:text-lg text-[#666] max-w-xl leading-relaxed">
          An interactive, data-driven Power BI dashboard transforming complex agricultural commerce data into actionable business insights. This tool empowers regional leads to optimize supply chain efficiency and maximize revenue yield across top-tier SKUs.
        </p>
      </div>

      <!-- Right Side Isometric Graphic -->
      <div class="lg:col-span-6 flex justify-center">
        <div class="w-full max-w-lg bg-[#ebf2f5] border border-[#eae6de] rounded-[2.5rem] p-8 shadow-sm flex items-center justify-center overflow-hidden min-h-[300px]">
          <!-- Isometric SVG Illustration replicating "FOOD & FEED ANALYTICS" graphic -->
          <svg class="w-full h-auto max-w-[400px]" viewBox="0 0 400 280" fill="none" xmlns="http://www.w3.org/2000/svg">
            <!-- Isometric Grid Floor Grid -->
            <path d="M40 180 L200 100 L360 180 L200 260 Z" fill="#ffffff" opacity="0.8"/>
            <path d="M40 180 L200 100 L360 180 L200 260 Z" stroke="#e1e8ed" stroke-width="2"/>
            
            <!-- Grid Lines inside base -->
            <path d="M80 160 L200 220 M120 140 L240 200 M160 120 L280 180 M200 100 L320 160" stroke="#f0f4f8" stroke-width="1.5"/>
            <path d="M320 160 L200 220 M280 140 L160 200 M240 120 L120 180 M200 100 L80 160" stroke="#f0f4f8" stroke-width="1.5"/>

            <!-- Floating Label Card "FOOD & FEED ANALYTICS" -->
            <g transform="translate(250, 40)">
              <rect x="0" y="0" width="130" height="42" rx="6" fill="#1c3530" shadow="md"/>
              <text x="12" y="18" fill="#ffffff" font-family="sans-serif" font-size="9" font-weight="bold" letter-spacing="0.5">FOOD & FEED</text>
              <text x="12" y="30" fill="#d9822b" font-family="sans-serif" font-size="9" font-weight="bold" letter-spacing="0.5">ANALYTICS</text>
            </g>

            <!-- Floating Line Chart in 3D -->
            <path d="M80 170 L140 135 L200 155 L260 100 L320 115" stroke="#1c3530" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" opacity="0.8"/>
            <circle cx="80" cy="170" r="3.5" fill="#1c3530"/>
            <circle cx="140" cy="135" r="3.5" fill="#1c3530"/>
            <circle cx="200" cy="155" r="3.5" fill="#1c3530"/>
            <circle cx="260" cy="100" r="3.5" fill="#d9822b"/>
            <circle cx="320" cy="115" r="3.5" fill="#1c3530"/>

            <!-- 3D Bar 1: Blue Bar (Center-Left) -->
            <!-- Base at 130, 185 -->
            <g>
              <!-- Top Face -->
              <path d="M130 150 L155 137.5 L180 150 L155 162.5 Z" fill="#3b82f6"/>
              <!-- Left Face -->
              <path d="M130 150 L130 185 L155 197.5 L155 162.5 Z" fill="#2563eb"/>
              <!-- Right Face -->
              <path d="M155 162.5 L155 197.5 L180 185 L180 150 Z" fill="#1d4ed8"/>
            </g>

            <!-- 3D Bar 2: Orange Bar (Center-Right) -->
            <!-- Base at 180, 210, higher Z -->
            <g>
              <!-- Top Face -->
              <path d="M180 130 L205 117.5 L230 130 L205 142.5 Z" fill="#f97316"/>
              <!-- Left Face -->
              <path d="M180 130 L180 180 L205 192.5 L205 142.5 Z" fill="#ea580c"/>
              <!-- Right Face -->
              <path d="M205 142.5 L205 192.5 L230 180 L230 130 Z" fill="#c2410c"/>
            </g>

            <!-- 3D Bar 3: Light Grey/Yellow Bar (Front) -->
            <g>
              <!-- Top Face -->
              <path d="M230 180 L250 170 L270 180 L250 190 Z" fill="#fbbf24"/>
              <!-- Left Face -->
              <path d="M230 180 L230 210 L250 220 L250 190 Z" fill="#f59e0b"/>
              <!-- Right Face -->
              <path d="M250 190 L250 220 L270 210 L270 180 Z" fill="#d97706"/>
            </g>

            <!-- Donut Chart 3D Mockup (Right) -->
            <ellipse cx="290" cy="190" rx="30" ry="16" fill="none" stroke="#e2e8f0" stroke-width="8"/>
            <ellipse cx="290" cy="190" rx="30" ry="16" fill="none" stroke="#f97316" stroke-width="8" stroke-dasharray="100 80" stroke-dashoffset="30"/>
            <ellipse cx="290" cy="190" rx="30" ry="16" fill="none" stroke="#3b82f6" stroke-width="8" stroke-dasharray="50 130" stroke-dashoffset="-70"/>

            <!-- Floating Mini Card (Left side) -->
            <g transform="translate(70, 70)">
              <!-- Card Base -->
              <rect x="0" y="0" width="80" height="40" rx="6" fill="#ffffff" stroke="#e1e8ed" stroke-width="1"/>
              <!-- Sparkline -->
              <path d="M10 28 L25 18 L40 25 L55 12 L70 20" stroke="#f97316" stroke-width="2" stroke-linecap="round" fill="none"/>
              <text x="8" y="10" fill="#777777" font-family="sans-serif" font-size="6" font-weight="bold">WEEKLY TREND</text>
              <text x="45" y="35" fill="#111111" font-family="sans-serif" font-size="6" font-weight="bold">$257,914</text>
            </g>
          </svg>
        </div>
      </div>
    </section>

    <!-- The Problem & The Objective Section -->
    <section class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Problem Card -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-lg bg-[#fff9f0] border border-[#fde8c5] text-[#d9822b] flex items-center justify-center text-lg font-bold">
              ⚠️
            </div>
            <h3 class="text-xl font-medium text-[#111]">The Problem</h3>
          </div>
          <p class="text-sm sm:text-base text-[#555] leading-relaxed">
            A significant portion of the total revenue is concentrated in specific food categories and seasons. However, analyzing complex, multi-variable transaction data sets to pinpoint these revenue drivers accurately remains a significant challenge for regional leads, often leading to missed opportunities for supply chain optimization.
          </p>
        </div>

        <!-- Objective Card -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-lg bg-[#f0f7ff] border border-[#d6eaff] text-[#3b82f6] flex items-center justify-center text-lg font-bold">
              🌐
            </div>
            <h3 class="text-xl font-medium text-[#111]">The Objective</h3>
          </div>
          <p class="text-sm sm:text-base text-[#555] leading-relaxed">
            The primary goal is to develop a comprehensive, interactive dashboard that visualizes key sales metrics and logistics indicators. This tool will allow clinical staff and researchers to quickly identify patterns, demographic vulnerabilities, and comorbid conditions, facilitating data-driven decision-making.
          </p>
        </div>
      </div>
    </section>

    <!-- Data Processing Pipeline -->
    <section id="pipeline" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-2xl sm:text-3xl font-medium text-[#111] mb-3">Data Processing Pipeline</h2>
        <p class="text-sm sm:text-base text-[#666]">
          Standardized steps taken to ensure data integrity before visualization.
        </p>
      </div>

      <!-- Flowchart Layout -->
      <div class="relative max-w-3xl mx-auto">
        <!-- Vertical Connection Line -->
        <div class="absolute left-1/2 top-0 bottom-0 w-0.5 bg-[#eae6de] -translate-x-1/2 hidden md:block"></div>

        <div class="space-y-12 relative">
          <!-- Step 1 -->
          <div class="flex flex-col md:flex-row items-center md:justify-between">
            <div class="w-full md:w-[45%] bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm md:text-right relative">
              <h3 class="text-lg font-semibold text-[#111] mb-2">Null Value Imputation</h3>
              <p class="text-sm text-[#666] leading-relaxed">
                Resolved missing regional tags using KNN nearest neighbor algorithm to preserve dataset size without introducing significant bias, ensuring a complete dataset for accurate modeling.
              </p>
              <!-- Connector dot for desktop -->
              <div class="absolute top-1/2 -right-4 w-3.5 h-3.5 rounded-full bg-white border-2 border-[#d9822b] translate-y-[-50%] translate-x-[50%] hidden md:block"></div>
            </div>
            <div class="w-[10%] hidden md:block"></div>
            <div class="w-full md:w-[45%] hidden md:block"></div>
          </div>

          <!-- Step 2 -->
          <div class="flex flex-col md:flex-row items-center md:justify-between">
            <div class="w-full md:w-[45%] hidden md:block"></div>
            <div class="w-[10%] hidden md:block"></div>
            <div class="w-full md:w-[45%] bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm relative">
              <h3 class="text-lg font-semibold text-[#111] mb-2">Categorical Normalization</h3>
              <p class="text-sm text-[#666] leading-relaxed">
                Standardized categories for consistency. For instance, merged redundant product sub-categories (e.g., 'Organic' and 'Bio') to simplify subsequent analysis and visualization in Power BI.
              </p>
              <!-- Connector dot for desktop -->
              <div class="absolute top-1/2 -left-4 w-3.5 h-3.5 rounded-full bg-white border-2 border-[#d9822b] translate-y-[-50%] translate-x-[-50%] hidden md:block"></div>
            </div>
          </div>

          <!-- Step 3 -->
          <div class="flex flex-col md:flex-row items-center md:justify-between">
            <div class="w-full md:w-[45%] bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm md:text-right relative">
              <h3 class="text-lg font-semibold text-[#111] mb-2">Outlier Treatment</h3>
              <p class="text-sm text-[#666] leading-relaxed">
                Capped anomalous revenue spikes (&gt;3 IQR) in Q4 wholesale data to preserve the dataset size without introducing significant bias, ensuring a complete dataset for accurate modeling.
              </p>
              <!-- Connector dot for desktop -->
              <div class="absolute top-1/2 -right-4 w-3.5 h-3.5 rounded-full bg-white border-2 border-[#d9822b] translate-y-[-50%] translate-x-[50%] hidden md:block"></div>
            </div>
            <div class="w-[10%] hidden md:block"></div>
            <div class="w-full md:w-[45%] hidden md:block"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Analysis Toolchain Section -->
    <section class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
      <div class="text-center max-w-2xl mx-auto mb-10">
        <h2 class="text-2xl sm:text-3xl font-medium text-[#111]">Analysis Toolchain</h2>
      </div>

      <div class="bg-white border border-[#eae6de] rounded-3xl p-8 max-w-3xl mx-auto shadow-sm">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center divide-y md:divide-y-0 md:divide-x divide-[#eae6de]">
          <!-- SQL Server -->
          <div class="flex flex-col items-center p-4">
            <div class="w-12 h-12 rounded-xl bg-[#eff6ff] flex items-center justify-center mb-4 border border-[#dbeafe]">
              <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" />
              </svg>
            </div>
            <h4 class="font-semibold text-sm tracking-wider text-[#111]">SQL Server</h4>
            <p class="text-xs text-[#777] mt-1">Extraction & Cleaning</p>
          </div>

          <!-- Excel -->
          <div class="flex flex-col items-center p-4">
            <div class="w-12 h-12 rounded-xl bg-[#ecfdf5] flex items-center justify-center mb-4 border border-[#d1fae5]">
              <svg class="w-6 h-6 text-emerald-600" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 17v-2m3 2v-4m3 4v-6m2 10H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
              </svg>
            </div>
            <h4 class="font-semibold text-sm tracking-wider text-[#111]">Excel</h4>
            <p class="text-xs text-[#777] mt-1">Validation & Prototyping</p>
          </div>

          <!-- Power BI -->
          <div class="flex flex-col items-center p-4">
            <div class="w-12 h-12 rounded-xl bg-[#fffbeb] flex items-center justify-center mb-4 border border-[#fef3c7]">
              <svg class="w-6 h-6 text-amber-500" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" d="M16 8v8m-4-5v5m-4-2v2m-2 4h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
              </svg>
            </div>
            <h4 class="font-semibold text-sm tracking-wider text-[#111]">Power BI</h4>
            <p class="text-xs text-[#777] mt-1">Modeling & Dashboards</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Dashboard Implementation -->
    <section id="dashboard" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
      <div class="text-center max-w-2xl mx-auto mb-12">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-2">IMPLEMENTATION</div>
        <h2 class="text-2xl sm:text-3xl font-medium text-[#111] mb-2">Dashboard Implementation</h2>
        <p class="text-xs sm:text-sm text-[#666]">
          Interactive Power BI dashboard providing real-time visibility into revenue generation, volume drivers, and profit margins.
        </p>
      </div>

      <!-- KPI Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
        <!-- KPI 1 -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
          <div class="text-[11px] font-bold text-[#888] tracking-widest uppercase mb-1">TOTAL REVENUE</div>
          <div class="text-3xl font-bold text-[#d9822b]">309 <span class="text-xl font-normal text-[#222]">bn</span></div>
          <div class="text-xs text-emerald-600 font-medium mt-2 flex items-center gap-1">
            📈 +12.4% vs last year
          </div>
        </div>

        <!-- KPI 2 -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
          <div class="text-[11px] font-bold text-[#888] tracking-widest uppercase mb-1">TOTAL VOLUME SOLD</div>
          <div class="text-3xl font-bold text-blue-600">3 <span class="text-xl font-normal text-[#222]">M MT</span></div>
          <div class="text-xs text-emerald-600 font-medium mt-2 flex items-center gap-1">
            📈 +8.2% vs last year
          </div>
        </div>

        <!-- KPI 3 -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
          <div class="text-[11px] font-bold text-[#888] tracking-widest uppercase mb-1">TOTAL TRANSACTIONS</div>
          <div class="text-3xl font-bold text-[#222]">5,002</div>
          <div class="text-xs text-rose-600 font-medium mt-2 flex items-center gap-1">
            📉 -1.5% vs last year
          </div>
        </div>
      </div>

      <!-- Main Interactive Dashboard Grid -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        
        <!-- Chart 1: Top Volume Drivers -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-base font-semibold text-[#111] mb-6">Top Volume Drivers (Items Sold)</h3>
          <div class="space-y-5">
            <!-- Cleo Cat Food -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Cleo Cat Food</span>
                <span class="text-[#777]">0.65M</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-blue-600 h-full rounded-full" style="width: 100%"></div>
              </div>
            </div>

            <!-- Bolt Cat Food -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Bolt Cat Food</span>
                <span class="text-[#777]">0.62M</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-blue-600 h-full rounded-full" style="width: 95.3%"></div>
              </div>
            </div>

            <!-- Bolt Dog Food -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Bolt Dog Food</span>
                <span class="text-[#777]">0.61M</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-blue-600 h-full rounded-full" style="width: 93.8%"></div>
              </div>
            </div>

            <!-- Fiesta Seafood Shrimp Roll -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Fiesta Seafood Shrimp Roll</span>
                <span class="text-[#777]">0.33M</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-gray-400 h-full rounded-full" style="width: 50.7%"></div>
              </div>
            </div>

            <!-- Shifudo Fish Roll -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Shifudo Fish Roll</span>
                <span class="text-[#777]">0.32M</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-gray-400 h-full rounded-full" style="width: 49.2%"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Chart 2: Transaction Distribution -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm flex flex-col justify-between">
          <h3 class="text-base font-semibold text-[#111] mb-4">Transaction Distribution</h3>
          
          <div class="flex items-center justify-center py-6">
            <!-- Donut Mockup with text inside -->
            <div class="relative w-44 h-44 flex items-center justify-center">
              <svg class="w-full h-full transform -rotate-90" viewBox="0 0 100 100">
                <!-- Inner circle path background -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#f0ece1" stroke-width="12" />
                
                <!-- Pet Food Segment (34.47%) -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#d9822b" stroke-width="12"
                        stroke-dasharray="82.2 238.76" stroke-dashoffset="0" />
                
                <!-- Frozen Food Segment (19.29%) -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#fda4af" stroke-width="12"
                        stroke-dasharray="46.0 238.76" stroke-dashoffset="-82.2" />

                <!-- Pakan Udang Segment (19.27%) -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#ca8a04" stroke-width="12"
                        stroke-dasharray="46.0 238.76" stroke-dashoffset="-128.2" />

                <!-- Pakan Ikan Segment (14.53%) -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#facc15" stroke-width="12"
                        stroke-dasharray="34.6 238.76" stroke-dashoffset="-174.2" />

                <!-- Desinfektan Segment (12.44%) -->
                <circle cx="50" cy="50" r="38" fill="transparent" stroke="#fed7aa" stroke-width="12"
                        stroke-dasharray="29.7 238.76" stroke-dashoffset="-208.8" />
              </svg>
              <!-- Center Absolute Label -->
              <div class="absolute text-center">
                <div class="text-sm font-bold text-[#111]">34%</div>
                <div class="text-[9px] font-bold text-[#777] uppercase tracking-wider">PET FOOD</div>
              </div>
            </div>
          </div>

          <!-- Custom Grid Legend below -->
          <div class="grid grid-cols-2 gap-x-6 gap-y-2 text-xs text-[#555] pt-4 border-t border-[#eae6de]">
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full bg-[#d9822b] shrink-0"></span>
              <span class="font-medium">Pet Food: <strong class="text-[#222]">34.47%</strong></span>
            </div>
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full bg-[#fda4af] shrink-0"></span>
              <span class="font-medium">Frozen Food: <strong class="text-[#222]">19.29%</strong></span>
            </div>
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full bg-[#ca8a04] shrink-0"></span>
              <span class="font-medium">Pakan Udang: <strong class="text-[#222]">19.27%</strong></span>
            </div>
            <div class="flex items-center gap-2">
              <span class="w-3 h-3 rounded-full bg-[#facc15] shrink-0"></span>
              <span class="font-medium">Pakan Ikan: <strong class="text-[#222]">14.53%</strong></span>
            </div>
            <div class="flex items-center gap-2 col-span-2">
              <span class="w-3 h-3 rounded-full bg-[#fed7aa] shrink-0"></span>
              <span class="font-medium">Desinfektan: <strong class="text-[#222]">12.44%</strong></span>
            </div>
          </div>
        </div>

        <!-- Chart 3: Highest Profit Realization -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-base font-semibold text-[#111] mb-6">Highest Profit Realization</h3>
          <div class="space-y-5">
            <!-- Bolt Cat Food -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Bolt Cat Food</span>
                <span class="text-[#777]">93bn</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-[#854d0e] h-full rounded-full" style="width: 100%"></div>
              </div>
            </div>

            <!-- Super Carp S99 -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Super Carp S99</span>
                <span class="text-[#777]">45bn</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-[#854d0e] h-full rounded-full" style="width: 48.3%"></div>
              </div>
            </div>

            <!-- Novo 6003 -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Novo 6003</span>
                <span class="text-[#777]">41bn</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-[#854d0e] h-full rounded-full" style="width: 44.1%"></div>
              </div>
            </div>

            <!-- Bintang 581 -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Bintang 581</span>
                <span class="text-[#777]">27bn</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-gray-400 h-full rounded-full" style="width: 29%"></div>
              </div>
            </div>

            <!-- Cleo Cat Food -->
            <div>
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-[#222]">Cleo Cat Food</span>
                <span class="text-[#777]">26bn</span>
              </div>
              <div class="h-2 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                <div class="bg-gray-400 h-full rounded-full" style="width: 28%"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Chart 4: Lowest Total Revenue -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm flex flex-col justify-between">
          <h3 class="text-base font-semibold text-[#111] mb-4">Lowest Total Revenue</h3>
          
          <div class="overflow-x-auto w-full flex-grow">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="border-b border-[#eae6de] text-xs font-bold text-[#777] uppercase tracking-wider">
                  <th class="py-3 px-2">Rank</th>
                  <th class="py-3 px-2">Product Name</th>
                  <th class="py-3 px-2 text-right">Total Revenue</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs">
                <tr>
                  <td class="py-3 px-2 text-[#777]">1</td>
                  <td class="py-3 px-2 font-medium text-[#222]">Fiesta Sardine</td>
                  <td class="py-3 px-2 text-right font-bold text-rose-600">0.13bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-2 text-[#777]">2</td>
                  <td class="py-3 px-2 font-medium text-[#222]">Takari Fish Food</td>
                  <td class="py-3 px-2 text-right font-bold text-rose-600">0.22bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-2 text-[#777]">3</td>
                  <td class="py-3 px-2 font-medium text-[#222]">CP Classic Jan Fish</td>
                  <td class="py-3 px-2 text-right font-bold text-rose-600">0.23bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-2 text-[#777]">4</td>
                  <td class="py-3 px-2 font-medium text-[#222]">Fresh Frozen Pangasius</td>
                  <td class="py-3 px-2 text-right font-bold text-rose-600">0.36bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-2 text-[#777]">5</td>
                  <td class="py-3 px-2 font-medium text-[#222]">T78-2A</td>
                  <td class="py-3 px-2 text-right font-bold text-rose-600">0.60bn</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>

      </div>
    </section>

    <!-- Exploratory Data Analysis -->
    <section id="eda" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
      <div class="text-center max-w-2xl mx-auto mb-12">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-2">ANALYSIS</div>
        <h2 class="text-2xl sm:text-3xl font-medium text-[#111] mb-2">Exploratory Data Analysis</h2>
        <p class="text-xs sm:text-sm text-[#666]">
          Detailed breakdown of sales performance, product rankings, category contributions, and strategic business recommendations.
        </p>
      </div>

      <div class="space-y-12">

        <!-- 1. Overall Sales Performance -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-[#111] mb-2">1. Overall Sales Performance</h3>
          <p class="text-sm text-[#666] mb-6">The dashboard shows the following overall business performance:</p>

          <div class="overflow-x-auto mb-6">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="bg-[#f8f6f0] border-b border-[#eae6de] text-xs font-bold text-[#555] uppercase">
                  <th class="py-3 px-4">KPI</th>
                  <th class="py-3 px-4">Result</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs sm:text-sm">
                <tr>
                  <td class="py-3 px-4 font-medium text-[#222]">Total Revenue</td>
                  <td class="py-3 px-4 font-bold text-[#d9822b]">309bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 font-medium text-[#222]">Total Sold</td>
                  <td class="py-3 px-4 font-bold text-blue-600">3M</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 font-medium text-[#222]">Total Transaction</td>
                  <td class="py-3 px-4 font-bold text-[#222]">5.002K</td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Insight</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>The business generated approximately 309bn in total revenue.</li>
                <li>Total product sales reached approximately 3 million units.</li>
                <li>The dataset contains approximately 5,002 transactions.</li>
                <li>The high sales volume indicates strong overall product movement across the business.</li>
              </ul>
            </div>

            <div class="bg-[#f8f6f0] p-5 rounded-xl border-l-4 border-[#1c3530]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Recommendation</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Continue monitoring products that contribute significantly to total sales.</li>
                <li>Identify products with high sales but relatively low profit margins.</li>
                <li>Use sales trends to improve inventory planning.</li>
                <li>Prioritize products with consistent demand.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- 2. Best-Selling Products -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-[#111] mb-2">2. Best-Selling Products</h3>
          <p class="text-sm text-[#666] mb-6">The dashboard identifies the following products with the highest number of items sold:</p>

          <div class="overflow-x-auto mb-6">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="bg-[#f8f6f0] border-b border-[#eae6de] text-xs font-bold text-[#555] uppercase">
                  <th class="py-3 px-4">Rank</th>
                  <th class="py-3 px-4">Product</th>
                  <th class="py-3 px-4 text-right">Items Sold</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs sm:text-sm">
                <tr>
                  <td class="py-3 px-4 text-[#777]">1</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Cleo Cat Food</td>
                  <td class="py-3 px-4 text-right font-bold text-[#d9822b]">0.65M</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">2</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Bolt Cat Food</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">0.62M</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">3</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Bolt Dog Food</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">0.61M</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">4</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Fiesta Seafood Shrimp Roll</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">0.33M</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">5</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Shifudo Fish Roll</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">0.32M</td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Insight</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Cleo Cat Food has the highest sales volume at approximately 0.65M units.</li>
                <li>Bolt Cat Food follows with approximately 0.62M units.</li>
                <li>Bolt Dog Food also performs strongly with approximately 0.61M units.</li>
                <li>The top three products have significantly higher sales volumes than the other products shown.</li>
              </ul>
            </div>

            <div class="bg-[#f8f6f0] p-5 rounded-xl border-l-4 border-[#1c3530]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Recommendation</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Maintain sufficient inventory for high-demand products.</li>
                <li>Prioritize high-selling products in sales campaigns.</li>
                <li>Analyze customer demand for cat and dog food products.</li>
                <li>Consider bundling high-volume products with lower-performing products.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- 3. Transaction Distribution by Category -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-[#111] mb-2">3. Transaction Distribution by Category</h3>
          <p class="text-sm text-[#666] mb-6">The transaction distribution is:</p>

          <div class="overflow-x-auto mb-6">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="bg-[#f8f6f0] border-b border-[#eae6de] text-xs font-bold text-[#555] uppercase">
                  <th class="py-3 px-4">Rank</th>
                  <th class="py-3 px-4">Category</th>
                  <th class="py-3 px-4">Transactions</th>
                  <th class="py-3 px-4 text-right">Percentage</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs sm:text-sm">
                <tr>
                  <td class="py-3 px-4 text-[#777]">1</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Pet Food</td>
                  <td class="py-3 px-4 text-[#555]">1.72K</td>
                  <td class="py-3 px-4 text-right font-bold text-[#d9822b]">34.47%</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">2</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Frozen Food</td>
                  <td class="py-3 px-4 text-[#555]">0.97K</td>
                  <td class="py-3 px-4 text-right font-semibold text-[#222]">19.29%</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">3</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Pakan Udang</td>
                  <td class="py-3 px-4 text-[#555]">0.96K</td>
                  <td class="py-3 px-4 text-right font-semibold text-[#222]">19.27%</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">4</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Pakan Ikan</td>
                  <td class="py-3 px-4 text-[#555]">0.73K</td>
                  <td class="py-3 px-4 text-right font-semibold text-[#222]">14.53%</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">5</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Desinfektan</td>
                  <td class="py-3 px-4 text-[#555]">0.62K</td>
                  <td class="py-3 px-4 text-right font-semibold text-[#222]">12.44%</td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Insight</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Pet Food has the highest transaction volume with approximately 1.72K transactions.</li>
                <li>Pet Food contributes approximately 34.47% of total transactions.</li>
                <li>Frozen Food and Pakan Udang have similar transaction volumes.</li>
                <li>Desinfektan has the lowest transaction contribution among the categories displayed.</li>
              </ul>
            </div>

            <div class="bg-[#f8f6f0] p-5 rounded-xl border-l-4 border-[#1c3530]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Recommendation</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Maintain product availability within the Pet Food category.</li>
                <li>Analyze why Frozen Food and Pakan Udang have similar transaction levels.</li>
                <li>Develop promotional campaigns for lower-transaction categories.</li>
                <li>Evaluate whether Desinfektan requires additional marketing or product positioning.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- 4. Highest Total Profit -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-[#111] mb-2">4. Highest Total Profit</h3>
          <p class="text-sm text-[#666] mb-6">The products with the highest total profit are:</p>

          <div class="overflow-x-auto mb-6">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="bg-[#f8f6f0] border-b border-[#eae6de] text-xs font-bold text-[#555] uppercase">
                  <th class="py-3 px-4">Rank</th>
                  <th class="py-3 px-4">Product</th>
                  <th class="py-3 px-4 text-right">Total Profit</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs sm:text-sm">
                <tr>
                  <td class="py-3 px-4 text-[#777]">1</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Bolt Cat Food</td>
                  <td class="py-3 px-4 text-right font-bold text-emerald-600">93bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">2</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Super Carp S99</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">45bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">3</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Novo 6003</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">41bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">4</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Bintang 581</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">27bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">5</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Cleo Cat Food</td>
                  <td class="py-3 px-4 text-right font-bold text-[#222]">26bn</td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Insight</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Bolt Cat Food generates the highest total profit at approximately 93bn.</li>
                <li>Its profit is significantly higher than the second-ranked product, Super Carp S99 at approximately 45bn.</li>
                <li>Cleo Cat Food has the highest sales volume but ranks fifth among the products shown by total profit.</li>
                <li>This indicates that sales volume alone does not necessarily determine the highest profit contribution.</li>
              </ul>
            </div>

            <div class="bg-[#f8f6f0] p-5 rounded-xl border-l-4 border-[#1c3530]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Recommendation</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Prioritize Bolt Cat Food because of its strong profit contribution.</li>
                <li>Analyze the profit margin of high-volume products such as Cleo Cat Food.</li>
                <li>Identify pricing and cost structures behind high-profit products.</li>
                <li>Consider increasing promotional support for products with both high sales and high profit.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- 5. Lowest Total Revenue -->
        <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-[#111] mb-2">5. Lowest Total Revenue</h3>
          <p class="text-sm text-[#666] mb-6">The products with the lowest total revenue shown in the dashboard are:</p>

          <div class="overflow-x-auto mb-6">
            <table class="w-full text-left text-sm border-collapse">
              <thead>
                <tr class="bg-[#f8f6f0] border-b border-[#eae6de] text-xs font-bold text-[#555] uppercase">
                  <th class="py-3 px-4">Rank</th>
                  <th class="py-3 px-4">Product</th>
                  <th class="py-3 px-4 text-right">Total Revenue</th>
                </tr>
              </thead>
              <tbody class="divide-y divide-[#eae6de] text-xs sm:text-sm">
                <tr>
                  <td class="py-3 px-4 text-[#777]">1</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Fiesta Sardine</td>
                  <td class="py-3 px-4 text-right font-bold text-rose-600">0.13bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">2</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Takari Fish Food</td>
                  <td class="py-3 px-4 text-right font-bold text-rose-600">0.22bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">3</td>
                  <td class="py-3 px-4 font-medium text-[#222]">CP Classic Jan Fish</td>
                  <td class="py-3 px-4 text-right font-bold text-rose-600">0.23bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">4</td>
                  <td class="py-3 px-4 font-medium text-[#222]">Fresh Frozen Pangasius</td>
                  <td class="py-3 px-4 text-right font-bold text-rose-600">0.36bn</td>
                </tr>
                <tr>
                  <td class="py-3 px-4 text-[#777]">5</td>
                  <td class="py-3 px-4 font-medium text-[#222]">T78-2A</td>
                  <td class="py-3 px-4 text-right font-bold text-rose-600">0.60bn</td>
                </tr>
              </tbody>
            </table>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Insight</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Fiesta Sardine has the lowest total revenue at approximately 0.13bn.</li>
                <li>Takari Fish Food and CP Classic Jan Fish generate approximately 0.22bn and 0.23bn respectively.</li>
                <li>The products shown have considerably lower revenue compared with the strongest-performing products.</li>
                <li>These products may require further investigation to determine whether the issue comes from low sales volume, pricing, availability, or demand.</li>
              </ul>
            </div>

            <div class="bg-[#f8f6f0] p-5 rounded-xl border-l-4 border-[#1c3530]">
              <h4 class="text-sm font-bold text-[#111] mb-2">Recommendation</h4>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Analyze sales volume and transaction frequency for low-revenue products.</li>
                <li>Evaluate product pricing and profitability.</li>
                <li>Consider promotional campaigns for products with low demand.</li>
                <li>Review inventory levels to avoid excessive stock on slow-moving products.</li>
                <li>Consider discontinuing or replacing products with consistently poor performance.</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Key Business Insights -->
        <div class="bg-[#1c3530] text-white rounded-2xl p-6 sm:p-8 shadow-sm">
          <h3 class="text-xl font-semibold text-white mb-2">Key Business Insights</h3>
          <p class="text-xs sm:text-sm text-[#adb5bd] mb-6">Based on the dashboard analysis:</p>

          <ul class="grid grid-cols-1 md:grid-cols-2 gap-3 text-xs sm:text-sm text-gray-200">
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Total Revenue reached approximately 309bn.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Approximately 3M products were sold.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>The dataset contains approximately 5.002K transactions.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Cleo Cat Food is the highest-selling product by quantity at 0.65M units.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Bolt Cat Food generates the highest total profit at approximately 93bn.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Pet Food has the highest transaction contribution at 34.47%.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Fiesta Sardine has the lowest total revenue among the products displayed.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>High sales volume does not necessarily mean the highest profit.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Pet Food is an important category due to its dominant transaction contribution.</span>
            </li>
            <li class="flex items-start gap-2 bg-[#254640] p-3 rounded-lg border border-white/10">
              <span class="text-[#d9822b] font-bold">✓</span>
              <span>Low-performing products should be evaluated based on demand, price, margin, and inventory movement.</span>
            </li>
          </ul>
        </div>

        <!-- Business Recommendations -->
        <div class="bg-white border-2 border-[#d9822b] rounded-2xl p-6 sm:p-8 shadow-md">
          <h3 class="text-xl font-semibold text-[#111] mb-2">Business Recommendations</h3>
          <p class="text-xs sm:text-sm text-[#666] mb-6">Based on the analysis, several actions can be considered:</p>

          <div class="space-y-6">
            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-base font-bold text-[#111] mb-1">1. Focus on High-Profit Products</h4>
              <p class="text-xs sm:text-sm text-[#555] leading-relaxed">
                Products such as Bolt Cat Food, Super Carp S99, and Novo 6003 should receive greater attention because they generate significant profit.
              </p>
            </div>

            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-base font-bold text-[#111] mb-1">2. Maintain High-Demand Inventory</h4>
              <p class="text-xs sm:text-sm text-[#555] leading-relaxed">
                Products such as Cleo Cat Food, Bolt Cat Food, and Bolt Dog Food have high sales volumes and should have sufficient inventory availability.
              </p>
            </div>

            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-base font-bold text-[#111] mb-1">3. Improve Low-Performing Products</h4>
              <p class="text-xs sm:text-sm text-[#555] mb-2 leading-relaxed">
                Products with low revenue should be evaluated based on:
              </p>
              <ul class="list-disc pl-5 space-y-1 text-xs sm:text-sm text-[#555]">
                <li>Sales volume</li>
                <li>Customer demand</li>
                <li>Pricing</li>
                <li>Profit margin</li>
                <li>Inventory availability</li>
                <li>Promotional effectiveness</li>
              </ul>
            </div>

            <div class="bg-[#fdf9f3] p-5 rounded-xl border-l-4 border-[#d9822b]">
              <h4 class="text-base font-bold text-[#111] mb-1">4. Strengthen Pet Food Category</h4>
              <p class="text-xs sm:text-sm text-[#555] leading-relaxed">
                Pet Food contributes the largest share of transactions. The business can explore additional products, bundles, and promotions within this category.
              </p>
            </div>
          </div>
        </div>

      </div>
    </section>



    <!-- Conclusion & Footer Section -->
    <section id="conclusion" class="bg-[#1c3530] text-white py-24 mt-12 relative overflow-hidden">
      <div class="max-w-4xl mx-auto px-6 text-center space-y-8">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase">CONCLUSION</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-white">Supply Chain Optimization Summary</h2>
        <p class="text-sm sm:text-base text-[#adb5bd] max-w-3xl mx-auto leading-relaxed">
          The transaction data reveals a heavily concentrated portfolio, with Pet Food emerging as the undeniable market leader. However, the combined strength of aquaculture feeds and Frozen Food indicates a diversified secondary market. To sustain growth, the strategy must balance aggressive expansion and premiumization in the dominant Pet Food sector while optimizing inventory and margins across the remaining robust categories to ensure holistic business stability.
        </p>

        <!-- Get In Touch Floating Banner -->
        <div class="mt-16 bg-[#d9822b] rounded-3xl p-8 sm:p-12 max-w-xl mx-auto shadow-xl space-y-6 text-center relative z-10">
          <h3 class="text-xl sm:text-2xl font-bold text-white">Get in Touch <br><span class="text-sm font-normal text-white/90">Let's Connect</span></h3>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-4 pt-2">
            <!-- Email -->
            <a href="mailto:afrizalmbagas@gmail.com" class="w-full sm:w-auto bg-[#1a1a1a] hover:bg-black text-white px-6 py-3 rounded-xl text-sm font-semibold transition-colors flex items-center justify-center gap-2 shadow">
              <svg class="w-4 h-4 fill-none stroke-current" viewBox="0 0 24 24" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
              </svg>
              afrizalmbagas@gmail.com
            </a>

            <!-- LinkedIn -->
            <a href="https://www.linkedin.com/in/m-bagas-afrizal" target="_blank" class="w-full sm:w-auto bg-white hover:bg-gray-100 text-[#1a1a1a] px-6 py-3 rounded-xl text-sm font-semibold transition-colors flex items-center justify-center gap-2 shadow">
              LinkedIn
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer id="contact" class="bg-[#fdfbf7] text-[#222] py-12 border-t border-[#eae6de]">
      <div class="max-w-6xl mx-auto px-6 text-center text-xs text-[#777]">
        <div>© 2026 M. Bagas. All rights reserved.</div>
      </div>
    </footer>

  </div>
</template>

<style scoped>
/* Scoped custom styling if any is needed */
</style>
