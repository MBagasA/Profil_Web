<script setup lang="ts">
import mbagasLogo from './assets/mbagas.svg'

defineProps<{
  projectType?: string
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

    <!-- ========================================== -->
    <!-- CASE STUDY 1: SNEAKER SALES & LOGISTICS    -->
    <!-- ========================================== -->
    <template v-if="projectType === 'sneaker'">
      <!-- Case Study Hero Section -->
      <section id="overview" class="max-w-6xl mx-auto px-6 pt-16 pb-20 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        <div class="lg:col-span-7 space-y-6">
          <div class="inline-block text-[11px] font-bold tracking-widest text-[#d9822b] uppercase bg-[#f5efe6] px-3 py-1 rounded">
            CASE STUDY · SQL & OPERATIONS ANALYTICS
          </div>
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-normal leading-[1.1] tracking-tight text-[#111]">
            Sneaker Sales & <span class="text-[#d9822b] font-medium">Logistics Analytics</span>
          </h1>
          <p class="text-base sm:text-lg text-[#666] max-w-xl leading-relaxed">
            Analyzed global retail transactions and multi-tier freight routing data to optimize inventory distribution, reduce transit times, and eliminate $1.2M in annual shipping inefficiencies.
          </p>
        </div>

        <div class="lg:col-span-5 relative flex justify-center">
          <div class="w-full max-w-md bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm relative">
            <div class="bg-[#f8f6f0] rounded-xl p-6 h-64 flex flex-col items-center justify-center relative overflow-hidden text-center border border-[#eae6de]">
              <div class="text-[10px] font-bold tracking-widest text-[#d9822b] mb-2">SUPPLY CHAIN & LOGISTICS</div>
              <div class="text-xl font-medium text-[#111] mb-4">$1.2M FREIGHT SAVINGS</div>
              <svg class="w-24 h-24 text-[#d9822b]" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
              </svg>
            </div>
            <div class="absolute -bottom-4 left-6 bg-white border border-[#eae6de] rounded-xl px-5 py-3 shadow-md flex items-center gap-3">
              <div>
                <div class="text-xl font-bold text-[#111]">$1.2M Saved</div>
                <div class="text-[11px] text-[#777] font-medium tracking-wide">Optimized global inventory routing</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- The Problem & The Objective -->
      <section class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm">
            <div class="flex items-center gap-3 mb-4">
              <span class="w-8 h-8 rounded-lg bg-[#fdf5eb] text-[#d9822b] flex items-center justify-center text-sm font-bold">⚠️</span>
              <h3 class="text-xl font-medium text-[#111]">The Problem</h3>
            </div>
            <p class="text-sm sm:text-base text-[#555] leading-relaxed">
              Rapid global expansion led to fragmented warehousing and inefficient freight routing. High shipping overheads, delayed last-mile deliveries, and suboptimal inventory stock levels across regional hubs caused a significant drain on quarterly operating margins.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm">
            <div class="flex items-center gap-3 mb-4">
              <span class="w-8 h-8 rounded-lg bg-[#fdf5eb] text-[#d9822b] flex items-center justify-center text-sm font-bold">🎯</span>
              <h3 class="text-xl font-medium text-[#111]">The Objective</h3>
            </div>
            <p class="text-sm sm:text-base text-[#555] leading-relaxed">
              Develop a robust SQL-driven logistics analytics model to evaluate global shipping lanes, consolidate freight carriers, reposition high-demand sneaker inventory closer to key consumer hubs, and drive measurable freight cost reductions.
            </p>
          </div>
        </div>
      </section>

      <!-- Data Processing Pipeline -->
      <section id="pipeline" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">DATA PIPELINE</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-10">Logistics Data Architecture</h2>
        
        <div class="space-y-6 max-w-4xl mx-auto">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">1</span>
              Cleaning Transactional & Freight Logs
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Aggregated 1.5M+ retail transactions and carrier dispatch logs across 4 continents. Resolved timestamp discrepancies, normalized SKU nomenclature, and removed anomalous duplicate shipment entries using advanced SQL window functions.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">2</span>
              Route Optimization & Cost-per-Mile Modeling
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Calculated freight cost-per-mile across primary shipping lanes. Segmented carriers by transit reliability and fuel surcharge fluctuations to identify underperforming logistics partners.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">3</span>
              Warehouse Demand Density Mapping
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Implemented geographic clustering queries in SQL to pinpoint regional surges in sneaker demand, guiding inventory redistribution to secondary fulfillment centers.
            </p>
          </div>
        </div>
      </section>

      <!-- Dashboard Implementation -->
      <section id="dashboard" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">IMPLEMENTATION</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-4">Logistics & Sales Dashboard</h2>
        <p class="text-base text-[#666] mb-8">
          Interactive executive dashboard providing real-time visibility into freight expenditure, shipping times, and retail SKU performance.
        </p>

        <div class="bg-[#fdf9f3] border-2 border-[#d9822b] rounded-3xl overflow-hidden shadow-lg">
          <div class="bg-[#d9822b] text-white px-8 py-4 flex items-center justify-between">
            <div class="font-bold text-lg tracking-wider">Global Logistics & Sales Analytics</div>
            <div class="text-xs bg-white/20 px-3 py-1 rounded">SQL & TABLEAU · LIVE</div>
          </div>

          <div class="p-6 sm:p-10 space-y-8">
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Annual Freight Saved</div>
                <div class="text-3xl font-bold text-[#111]">$1.2M</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[90%]"></div>
                </div>
              </div>
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Total Shipments Tracked</div>
                <div class="text-3xl font-bold text-[#111]">1.48M</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[75%]"></div>
                </div>
              </div>
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Avg Transit Time</div>
                <div class="text-3xl font-bold text-[#111]">3.2 Days</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[65%]"></div>
                </div>
              </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <h4 class="text-sm font-semibold text-[#111] mb-4">Freight Cost by Region ($K)</h4>
                <div class="h-48 flex items-end justify-between gap-4 pt-6 px-4 border-b border-[#eae6de]">
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">$420K</span>
                    <div class="w-full bg-[#d9822b] opacity-50 h-24 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">North America</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">$310K</span>
                    <div class="w-full bg-[#d9822b] opacity-70 h-18 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Europe</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#111]">$580K</span>
                    <div class="w-full bg-[#d9822b] h-full rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Asia-Pacific</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">$190K</span>
                    <div class="w-full bg-[#d9822b] opacity-30 h-12 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">LatAm</span>
                  </div>
                </div>
              </div>

              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm flex flex-col justify-between">
                <h4 class="text-sm font-semibold text-[#111] mb-2">Top Selling Sneaker Categories</h4>
                <div class="space-y-3 pt-2">
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Limited Edition Retro Runners</span><span>42%</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] h-full w-[42%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Performance Basketball</span><span>28%</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-75 h-full w-[28%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Everyday Lifestyle Cw</span><span>22%</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-50 h-full w-[22%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Skateboarding Series</span><span>8%</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-30 h-full w-[8%]"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Exploratory Data Analysis -->
      <section id="eda" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">ANALYSIS</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-10">Logistics Exploratory Data Analysis</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">01</span>
                <span class="text-xs font-semibold text-[#888]">SHIPPING LANES</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">Carrier Surcharge Bottlenecks</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  Cross-Pacific shipping routes incurred 35% higher fuel surcharges during peak Q4 shipping windows due to carrier consolidation.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Diversify carrier contracts and pre-book container slot allocations 60 days in advance to lock in predictable freight rates.
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">02</span>
                <span class="text-xs font-semibold text-[#888]">INVENTORY PLACEMENT</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">Warehouse Stock Distribution</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  Centralizing top 20 sneaker SKUs in regional hubs reduced last-mile transit times by 48 hours.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Automate inventory redistribution rules based on real-time point-of-sale velocity triggers.
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Conclusion Section -->
      <section id="conclusion" class="bg-[#1c3530] text-white py-20 my-12">
        <div class="max-w-4xl mx-auto px-6 text-center space-y-6">
          <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase">CONCLUSION</div>
          <h2 class="text-3xl sm:text-4xl font-normal text-white">Supply Chain Optimization Summary</h2>
          <p class="text-base sm:text-lg text-[#adb5bd] leading-relaxed">
            By combining rigorous SQL log analysis with geographic inventory routing, the Sneaker Sales & Logistics Analytics initiative successfully slashed annual freight overhead by $1.2M while accelerating delivery times across major global markets.
          </p>
        </div>
      </section>
    </template>

    <!-- ========================================== -->
    <!-- CASE STUDY 2: STROKE PATIENT DASHBOARD     -->
    <!-- ========================================== -->
    <template v-else>
      <!-- Case Study Hero Section -->
      <section id="overview" class="max-w-6xl mx-auto px-6 pt-16 pb-20 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        <div class="lg:col-span-7 space-y-6">
          <div class="inline-block text-[11px] font-bold tracking-widest text-[#d9822b] uppercase bg-[#f5efe6] px-3 py-1 rounded">
            CASE STUDY · HEALTHCARE ANALYTICS
          </div>
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-normal leading-[1.1] tracking-tight text-[#111]">
            Stroke Patient <span class="text-[#d9822b] font-medium">Dashboard</span>
          </h1>
          <p class="text-base sm:text-lg text-[#666] max-w-xl leading-relaxed">
            An interactive, data-driven Power BI dashboard transforming complex stroke patient data into actionable clinical insights. This tool empowers healthcare providers to proactively monitor high-risk patients and optimize preventative care strategies.
          </p>
        </div>

        <div class="lg:col-span-5 relative flex justify-center">
          <div class="w-full max-w-md bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm relative">
            <div class="bg-[#f8f6f0] rounded-xl p-6 h-64 flex flex-col items-center justify-center relative overflow-hidden text-center border border-[#eae6de]">
              <div class="text-[10px] font-bold tracking-widest text-[#d9822b] mb-2">HEALTHCARE ANALYTICS</div>
              <div class="text-xl font-medium text-[#111] mb-4">DATA INSIGHTS</div>
              <svg class="w-24 h-24 text-[#d9822b]" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path stroke-linecap="round" stroke-linejoin="round" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z" />
              </svg>
            </div>
            <div class="absolute -bottom-4 left-6 bg-white border border-[#eae6de] rounded-xl px-5 py-3 shadow-md flex items-center gap-3">
              <div>
                <div class="text-xl font-bold text-[#111]">249 Patients</div>
                <div class="text-[11px] text-[#777] font-medium tracking-wide">High-risk Stroke cohort analyzed</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- The Problem & The Objective -->
      <section class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm">
            <div class="flex items-center gap-3 mb-4">
              <span class="w-8 h-8 rounded-lg bg-[#fdf5eb] text-[#d9822b] flex items-center justify-center text-sm font-bold">⚠️</span>
              <h3 class="text-xl font-medium text-[#111]">The Problem</h3>
            </div>
            <p class="text-sm sm:text-base text-[#555] leading-relaxed">
              Strokes are a leading cause of mortality and long-term disability globally. Early identification of high-risk individuals is crucial for effective intervention. However, analyzing complex, multi-variable patient data sets to pinpoint these risk factors accurately remains a significant challenge for healthcare providers, often leading to missed opportunities for preventative care.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm">
            <div class="flex items-center gap-3 mb-4">
              <span class="w-8 h-8 rounded-lg bg-[#fdf5eb] text-[#d9822b] flex items-center justify-center text-sm font-bold">🎯</span>
              <h3 class="text-xl font-medium text-[#111]">The Objective</h3>
            </div>
            <p class="text-sm sm:text-base text-[#555] leading-relaxed">
              The primary goal is to develop a comprehensive, interactive dashboard that visualizes key stroke risk indicators. This tool will allow clinical staff and researchers to quickly identify patterns, demographic vulnerabilities, and comorbid conditions, facilitating data-driven decision-making and targeted preventative interventions.
            </p>
          </div>
        </div>
      </section>

      <!-- Data Processing Pipeline -->
      <section id="pipeline" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">DATA PIPELINE</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-10">Data Processing Pipeline</h2>
        
        <div class="space-y-6 max-w-4xl mx-auto">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">1</span>
              Handling Missing Value
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Identified 201 missing values in the <code class="bg-[#f8f6f0] px-1.5 py-0.5 rounded text-[#d9822b] text-xs font-mono">bmi</code> column. Imputed these values using the median BMI to preserve the dataset size without introducing significant bias, ensuring a complete dataset for accurate modeling.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">2</span>
              Categorical Variable Encoding
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Standardized categories for consistency. For instance, unified variations in <code class="bg-[#f8f6f0] px-1.5 py-0.5 rounded text-[#d9822b] text-xs font-mono">smoking_status</code> (e.g., merging "formerly smoked" into a consistent format) and <code class="bg-[#f8f6f0] px-1.5 py-0.5 rounded text-[#d9822b] text-xs font-mono">work_type</code> to simplify subsequent analysis and visualization in Power BI.
            </p>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-6 sm:p-8 shadow-sm">
            <h3 class="text-lg font-medium text-[#111] mb-2 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-[#f5efe6] text-[#d9822b] text-xs flex items-center justify-center font-bold">3</span>
              Outlier Detection (Optional but considered)
            </h3>
            <p class="text-sm text-[#666] leading-relaxed pl-8">
              Identified potential outliers in glucose and BMI distributions using IQR methods. Evaluated impact on predictive skewness and retained verified clinical extremes to maintain realistic risk representation.
            </p>
          </div>
        </div>
      </section>

      <!-- Dashboard Implementation -->
      <section id="dashboard" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">IMPLEMENTATION</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-4">Dashboard Implementation</h2>
        <p class="text-base text-[#666] mb-8">
          Interactive Power BI dashboard providing immediate visual insights into stroke risk demographics and clinical indicators.
        </p>

        <div class="bg-[#fdf9f3] border-2 border-[#d9822b] rounded-3xl overflow-hidden shadow-lg">
          <div class="bg-[#d9822b] text-white px-8 py-4 flex items-center justify-between">
            <div class="font-bold text-lg tracking-wider">Stroke Health Dashboard</div>
            <div class="text-xs bg-white/20 px-3 py-1 rounded">POWER BI · INTERACTIVE</div>
          </div>

          <div class="p-6 sm:p-10 space-y-8">
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Total Patients by stroke</div>
                <div class="text-3xl font-bold text-[#111]">249</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[85%]"></div>
                </div>
              </div>
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Avg Glucose by stroke</div>
                <div class="text-3xl font-bold text-[#111]">132.54</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[70%]"></div>
                </div>
              </div>
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <div class="text-xs font-semibold text-[#888] mb-1">Avg BMI by stroke</div>
                <div class="text-3xl font-bold text-[#111]">30.09</div>
                <div class="mt-4 h-1.5 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                  <div class="bg-[#d9822b] h-full w-[60%]"></div>
                </div>
              </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <h4 class="text-sm font-semibold text-[#111] mb-4">Total Stroke Case By Age segment</h4>
                <div class="h-48 flex items-end justify-between gap-2 pt-6 px-4 border-b border-[#eae6de]">
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">1</span>
                    <div class="w-full bg-[#d9822b] opacity-30 h-4 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Children</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">1</span>
                    <div class="w-full bg-[#d9822b] opacity-40 h-4 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Teenager</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">33</span>
                    <div class="w-full bg-[#d9822b] opacity-60 h-16 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Senior</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#666]">58</span>
                    <div class="w-full bg-[#d9822b] opacity-80 h-28 rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Mature</span>
                  </div>
                  <div class="flex flex-col items-center gap-2 flex-1">
                    <span class="text-xs font-bold text-[#111]">156</span>
                    <div class="w-full bg-[#d9822b] h-full rounded-t"></div>
                    <span class="text-[10px] text-[#777]">Elderly</span>
                  </div>
                </div>
              </div>

              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm flex flex-col justify-between">
                <h4 class="text-sm font-semibold text-[#111] mb-2">Smoking Lifestyle and Stroke Risk</h4>
                <div class="flex items-center justify-center py-4">
                  <div class="w-36 h-36 rounded-full border-8 border-[#d9822b] border-t-[#1c3530] border-r-[#e5c5a3] flex items-center justify-center shadow-inner">
                    <div class="text-center">
                      <div class="text-xs font-bold text-[#111]">Lifestyle</div>
                      <div class="text-[10px] text-[#777]">Risk Factor</div>
                    </div>
                  </div>
                </div>
                <div class="grid grid-cols-2 gap-2 text-xs text-[#555] pt-2 border-t border-[#eae6de]">
                  <div>• Never Smoked: <strong>0.79K (15.4%)</strong></div>
                  <div>• Unknown: <strong>1.89K (37.0%)</strong></div>
                  <div>• Formerly Smoked: <strong>0.88K (17.3%)</strong></div>
                  <div>• Smokes: <strong>1.54K (30.2%)</strong></div>
                </div>
              </div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <h4 class="text-sm font-semibold text-[#111] mb-4">Total Stroke Cases By Work Type</h4>
                <div class="space-y-3">
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Private</span><span>149</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] h-full w-[90%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Self-Employed</span><span>65</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-75 h-full w-[45%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Govt_Job</span><span>33</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-50 h-full w-[25%]"></div>
                    </div>
                  </div>
                  <div>
                    <div class="flex justify-between text-xs text-[#666] mb-1"><span>Children</span><span>2</span></div>
                    <div class="h-3 w-full bg-[#f0ece1] rounded-full overflow-hidden">
                      <div class="bg-[#d9822b] opacity-30 h-full w-[5%]"></div>
                    </div>
                  </div>
                </div>
              </div>

              <div class="bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm">
                <h4 class="text-sm font-semibold text-[#111] mb-4">Demographics (Gender & Marital Status)</h4>
                <div class="grid grid-cols-2 gap-6 pt-4">
                  <div class="bg-[#f8f6f0] p-4 rounded-xl text-center">
                    <div class="text-xs text-[#777] font-medium mb-1">Female / Male</div>
                    <div class="text-lg font-bold text-[#111]">141 / 108</div>
                    <div class="text-[10px] text-[#d9822b] mt-1 font-semibold">Total Cases: 249</div>
                  </div>
                  <div class="bg-[#f8f6f0] p-4 rounded-xl text-center">
                    <div class="text-xs text-[#777] font-medium mb-1">Ever Married (Yes / No)</div>
                    <div class="text-lg font-bold text-[#111]">120 / 21</div>
                    <div class="text-[10px] text-[#d9822b] mt-1 font-semibold">High correlation</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Exploratory Data Analysis -->
      <section id="eda" class="max-w-6xl mx-auto px-6 py-16 border-t border-[#eae6de]">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">ANALYSIS</div>
        <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-10">Exploratory Data Analysis</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">01</span>
                <span class="text-xs font-semibold text-[#888]">DEMOGRAPHIC RISK</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">Age and Stroke Risk</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  A significant correlation exists between increasing age and the likelihood of suffering a stroke. The incidence rate rises sharply in patients over the age of 55.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Implement targeted screening and preventative care programs specifically for the demographic aged 55 and older.
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">02</span>
                <span class="text-xs font-semibold text-[#888]">CLINICAL COMORBIDITIES</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">Comorbidities (Hypertension & Heart Disease)</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  Patients presenting with hypertension or underlying heart disease exhibit a substantially higher risk profile for stroke compared to those without these conditions.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Prioritize rigorous monitoring and aggressive management of blood pressure and cardiovascular health to mitigate stroke risk in these patient groups.
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">03</span>
                <span class="text-xs font-semibold text-[#888]">METABOLIC HEALTH</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">Average Glucose Levels</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  Elevated average glucose levels are positively associated with an increased incidence of stroke events, highlighting the role of metabolic health.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Promote lifestyle interventions focusing on diet and exercise to regulate blood sugar levels, particularly in pre-diabetic or diabetic patients.
                </div>
              </div>
            </div>
          </div>

          <div class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between mb-4">
                <span class="text-xs font-bold tracking-widest text-[#d9822b]">04</span>
                <span class="text-xs font-semibold text-[#888]">BODY MASS INDEX</span>
              </div>
              <h3 class="text-xl font-medium text-[#111] mb-4">BMI and Stroke Risk</h3>
              <div class="space-y-4 text-sm text-[#555]">
                <div class="bg-[#fdf9f3] p-4 rounded-xl border-l-4 border-[#d9822b]">
                  <strong class="text-[#111] block mb-1">INSIGHT</strong>
                  While a correlation exists, Body Mass Index (BMI) alone appears to be a less dominant independent predictor of stroke compared to age or specific cardiovascular comorbidities within this dataset.
                </div>
                <div class="bg-[#f8f6f0] p-4 rounded-xl">
                  <strong class="text-[#111] block mb-1">RECOMMENDATION</strong>
                  Maintain BMI monitoring as part of comprehensive health assessments, but weight management programs should be integrated with strategies addressing primary risk factors like hypertension.
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="mt-8 bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm">
          <div class="flex items-center justify-between mb-4">
            <span class="text-xs font-bold tracking-widest text-[#d9822b]">05</span>
            <span class="text-xs font-semibold text-[#888]">LIFESTYLE HABITS</span>
          </div>
          <h3 class="text-xl font-medium text-[#111] mb-4">Smoking Status</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-sm text-[#555]">
            <div class="bg-[#fdf9f3] p-6 rounded-xl border-l-4 border-[#d9822b]">
              <strong class="text-[#111] block mb-2">INSIGHT</strong>
              The data suggests a nuanced relationship where former smokers present a higher incidence of stroke compared to never-smokers. This likely reflects cumulative long-term vascular damage that persists even after cessation.
            </div>
            <div class="bg-[#f8f6f0] p-6 rounded-xl">
              <strong class="text-[#111] block mb-2">RECOMMENDATION</strong>
              Intensify public health campaigns and clinical support for smoking cessation. Crucially, clinicians must recognize former smokers as a higher-category risk requiring vigilant, ongoing cardiovascular monitoring despite having quit.
            </div>
          </div>
        </div>
      </section>

      <!-- Conclusion Section -->
      <section id="conclusion" class="bg-[#1c3530] text-white py-20 my-12">
        <div class="max-w-4xl mx-auto px-6 text-center space-y-6">
          <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase">CONCLUSION</div>
          <h2 class="text-3xl sm:text-4xl font-normal text-white">Summary of Findings</h2>
          <p class="text-base sm:text-lg text-[#adb5bd] leading-relaxed">
            The Stroke Patient Dashboard successfully translates complex demographic and clinical data into a clear, actionable format. The EDA confirms that advancing age, hypertension, and heart disease are paramount risk factors. By deploying this dashboard, healthcare facilities can shift towards proactive patient management, utilizing data to prioritize high-risk individuals for targeted interventions, ultimately improving patient outcomes and resource allocation.
          </p>
        </div>
      </section>
    </template>

    <!-- Footer / Get In Touch -->
    <footer id="contact" class="bg-[#fdfbf7] text-[#222] py-20 border-t border-[#eae6de]">
      <div class="max-w-4xl mx-auto px-6 text-center space-y-8">
        <p class="text-base sm:text-lg text-[#555] max-w-2xl mx-auto leading-relaxed">
          Interested in collaborating on data projects, analytics, or research? I'd love to hear from you.
        </p>
        
        <div class="flex flex-wrap items-center justify-center gap-4">
          <!-- Email Button -->
          <a href="mailto:afrizalmbagas@gmail.com" class="bg-[#b85624] hover:bg-[#a04920] text-white px-6 py-3.5 rounded-xl font-medium text-sm transition-colors flex items-center gap-2 shadow-sm">
            <svg class="w-5 h-5 fill-none stroke-current" viewBox="0 0 24 24" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
            afrizalmbagas@gmail.com
          </a>

          <!-- LinkedIn Button -->
          <a href="https://linkedin.com" target="_blank" class="bg-white hover:bg-[#f5efe6] text-[#111] px-6 py-3.5 rounded-xl font-medium text-sm border border-[#eae6de] transition-colors flex items-center gap-2 shadow-sm">
            <svg class="w-4 h-4 fill-current text-[#111]" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
            LinkedIn
            <svg class="w-3.5 h-3.5 fill-none stroke-current text-[#555]" viewBox="0 0 24 24" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
          </a>
        </div>
      </div>
      <div class="max-w-6xl mx-auto px-6 pt-16 mt-16 border-t border-[#eae6de] text-xs text-[#777] flex justify-center">
        <div>© 2026 M. Bagas. All rights reserved.</div>
      </div>
    </footer>

  </div>
</template>
