<script setup lang="ts">
import { ref } from 'vue'
import Portofolio from './Portofolio.vue'
import mbagasLogo from './assets/mbagas.svg'

const currentView = ref<'home' | 'stroke'>('home')
const mobileMenuOpen = ref(false)

const projects = [
  {
    category: 'PYTHON · MACHINE LEARNING',
    title: 'Dataset of processed feed products and frozen food',
    description: 'Developed a predictive model identifying at-risk customers, reducing churn by 18% over two quarters.',
    chartType: 'line',
    action: 'home'
  },
  {
    category: 'SQL · OPERATIONS',
    title: 'Sneaker sales dataset & Logistics Analytics',
    description: 'Analyzed global logistics and retail sales data to optimize inventory routing, saving $1.2M in annual freight costs.',
    chartType: 'bars',
    action: 'home'
  },
  {
    category: 'SQL · POWER BI',
    title: 'Stroke Patient Dashboard & Healthcare Analytics',
    description: 'Built a unified executive dashboard connecting disparate clinical data sources for real-time stroke risk tracking.',
    chartType: 'donut',
    action: 'stroke'
  }
]

const capabilities = [
  {
    icon: '📊',
    title: 'Data Visualization',
    description: 'Transforming complex datasets into intuitive, interactive dashboards that empower non-technical stakeholders to explore data independently.'
  },
  {
    icon: '📈',
    title: 'Predictive Modeling',
    description: 'Building robust machine learning models to forecast trends, anticipate customer behavior, and optimize resource allocation.'
  },
  {
    icon: '🔀',
    title: 'Business Intelligence',
    description: 'Designing and implementing end-to-end BI pipelines, from data warehousing to automated reporting architectures.'
  },
  {
    icon: '💡',
    title: 'Data Strategy',
    description: 'Consulting on data governance, tech stack selection, and establishing a data-driven culture within organizations.'
  }
]

const toolkit = [
  { name: 'Python', type: 'LANG' },
  { name: 'SQL', type: 'LANG' },
  { name: 'GitHub', type: 'TOOL' },
  { name: 'TensorFlow', type: 'ML' },
  { name: 'Tableau', type: 'VIZ' },
  { name: 'Power BI', type: 'VIZ' },
  { name: 'Looker Studio', type: 'VIZ' },
  { name: 'Excel', type: 'TOOL' }
]

function openProject(action: string) {
  if (action === 'stroke') {
    currentView.value = 'stroke'
    window.scrollTo({ top: 0, behavior: 'smooth' })
  }
}

function goHome() {
  currentView.value = 'home'
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <Portofolio v-if="currentView === 'stroke'" projectType="stroke" :onBack="goHome" />

  <div v-else class="min-h-screen bg-[#fdfbf7] text-[#222222] font-sans antialiased selection:bg-[#d9822b] selection:text-white">
    
    <!-- Header / Navbar -->
    <header class="max-w-6xl mx-auto px-6 py-6 flex items-center justify-between border-b border-[#eae6de]">
      <div class="flex items-center gap-2">
        <img :src="mbagasLogo" alt="M Bagas Logo" class="w-9 h-9" />
      </div>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8 text-xs font-semibold tracking-wider text-[#555]">
        <a href="#home" class="hover:text-[#d9822b] transition-colors">HOME</a>
        <a href="#about" class="hover:text-[#d9822b] transition-colors">ABOUT</a>
        <a href="#services" class="hover:text-[#d9822b] transition-colors">SERVICES</a>
        <a href="#portfolio" class="hover:text-[#d9822b] transition-colors">PORTFOLIO</a>
        <a href="#contact" class="hover:text-[#d9822b] transition-colors">CONTACT</a>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="mobileMenuOpen = !mobileMenuOpen" class="md:hidden text-2xl focus:outline-none">
        ☰
      </button>
    </header>

    <!-- Mobile Nav Modal -->
    <div v-if="mobileMenuOpen" class="md:hidden bg-[#fdfbf7] border-b border-[#eae6de] px-6 py-4 flex flex-col gap-4 text-sm font-semibold text-[#555]">
      <a href="#home" @click="mobileMenuOpen = false" class="hover:text-[#d9822b]">HOME</a>
      <a href="#about" @click="mobileMenuOpen = false" class="hover:text-[#d9822b]">ABOUT</a>
      <a href="#services" @click="mobileMenuOpen = false" class="hover:text-[#d9822b]">SERVICES</a>
      <a href="#portfolio" @click="mobileMenuOpen = false" class="hover:text-[#d9822b]">PORTFOLIO</a>
      <a href="#contact" @click="mobileMenuOpen = false" class="hover:text-[#d9822b]">CONTACT</a>
    </div>

    <!-- Hero Section -->
    <section id="home" class="max-w-6xl mx-auto px-6 pt-16 pb-24 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
      <div class="lg:col-span-7 space-y-6">
        <div class="inline-block text-[11px] font-bold tracking-widest text-[#d9822b] uppercase bg-[#f5efe6] px-3 py-1 rounded">
          DATA ANALYTICS & PORTFOLIO
        </div>
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-normal leading-[1.1] tracking-tight text-[#111]">
          Transforming Complex Data Into <span class="text-[#d9822b] font-medium">Valuable Insights</span>
        </h1>
        <p class="text-base sm:text-lg text-[#666] max-w-xl leading-relaxed">
          I help businesses make smarter decisions through data storytelling and advanced analytics. Explore interactive case studies and dashboard designs.
        </p>
        <div class="flex flex-wrap items-center gap-4 pt-2">
          <a href="#portfolio" class="bg-[#222] hover:bg-[#d9822b] text-white text-xs font-semibold tracking-wider px-6 py-3.5 rounded transition-colors shadow-sm">
            EXPLORE PORTFOLIO
          </a>
          <a href="#contact" class="text-xs font-semibold tracking-wider text-[#222] hover:text-[#d9822b] flex items-center gap-2 py-3.5 transition-colors">
            GET IN TOUCH <span class="text-sm">→</span>
          </a>
        </div>
      </div>

      <!-- Hero Graphic Card -->
      <div class="lg:col-span-5 relative flex justify-center">
        <div class="w-full max-w-md bg-white border border-[#eae6de] rounded-2xl p-6 shadow-sm relative">
          <div class="bg-[#f8f6f0] rounded-xl p-6 h-64 flex items-center justify-center relative overflow-hidden">
            <svg class="w-full h-full text-[#d9822b]" viewBox="0 0 200 160" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M20 130L60 90L90 110L140 50L180 30" stroke="#d9822b" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
              <circle cx="180" cy="30" r="5" fill="#d9822b"/>
              <circle cx="140" cy="50" r="4" fill="#111"/>
              <circle cx="90" cy="110" r="4" fill="#111"/>
              <circle cx="60" cy="90" r="4" fill="#111"/>
              <circle cx="20" cy="130" r="4" fill="#111"/>
              <rect x="130" y="80" width="12" height="50" rx="2" fill="#e5ded0"/>
              <rect x="150" y="65" width="12" height="65" rx="2" fill="#d9822b" fill-opacity="0.3"/>
              <rect x="110" y="95" width="12" height="35" rx="2" fill="#111" fill-opacity="0.1"/>
            </svg>
          </div>
          <div class="absolute -bottom-4 left-6 bg-white border border-[#eae6de] rounded-xl px-5 py-3 shadow-md flex items-center gap-3">
            <div>
              <div class="text-2xl font-bold text-[#111]">$1.2M</div>
              <div class="text-[11px] text-[#777] font-medium tracking-wide">Freight Cost Saved via SQL</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Section 01 / Profile -->
    <section id="about" class="max-w-6xl mx-auto px-6 py-20 border-t border-[#eae6de]">
      <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">01 / PROFILE</div>
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
        <div class="lg:col-span-5 space-y-4">
          <h2 class="text-3xl sm:text-4xl font-normal text-[#111] leading-tight">
            The Person Behind the Data
          </h2>
          <div class="pt-6">
            <svg class="w-full h-24 text-[#d9822b]" viewBox="0 0 300 80" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M10 70C50 50 80 60 120 40C160 20 200 45 250 15L290 10" stroke="#d9822b" stroke-width="2" stroke-dasharray="4 4" opacity="0.6"/>
              <path d="M10 65C50 45 80 55 120 35C160 15 200 40 250 10L290 5" stroke="#d9822b" stroke-width="2.5"/>
            </svg>
          </div>
        </div>
        <div class="lg:col-span-7 space-y-4 text-[#555] text-base leading-relaxed">
          <p>
            I don't just see rows and columns; I see human behavior, market trends, and hidden opportunities. My passion lies in extracting narratives from data noise.
          </p>
          <p>
            With a background in statistics and operations research, my approach is analytical yet highly creative. I have a deep passion for data storytelling, where I bridge technical complexity with tangible business strategies. I am committed to driving data-driven growth by ensuring every finding can be effectively communicated to stakeholders. Over the past decade, I have worked across various sectors to build robust data pipelines, design intuitive dashboards, and present insights that directly influence C-suite level strategies.
          </p>
        </div>
      </div>
    </section>

    <!-- Section 02 / Capabilities -->
    <section id="services" class="max-w-6xl mx-auto px-6 py-20 border-t border-[#eae6de]">
      <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">02 / CAPABILITIES</div>
      <h2 class="text-3xl sm:text-4xl font-normal text-[#111] mb-12">
        Data Solutions Built for Impact
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div v-for="(cap, i) in capabilities" :key="i" class="bg-white border border-[#eae6de] rounded-2xl p-8 shadow-sm hover:shadow-md transition-shadow flex flex-col justify-between">
          <div>
            <div class="w-12 h-12 bg-[#f8f6f0] rounded-xl flex items-center justify-center text-xl mb-6 border border-[#eae6de]">
              {{ cap.icon }}
            </div>
            <h3 class="text-xl font-medium text-[#111] mb-3">{{ cap.title }}</h3>
            <p class="text-sm text-[#666] leading-relaxed">{{ cap.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Section 03 / Selected Works -->
    <section id="portfolio" class="max-w-6xl mx-auto px-6 py-20 border-t border-[#eae6de]">
      <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-12 gap-4">
        <div>
          <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">03 / SELECTED WORKS</div>
          <h2 class="text-3xl sm:text-4xl font-normal text-[#111]">Impact Through Analysis</h2>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div v-for="(project, i) in projects" :key="i" class="group flex flex-col" :class="{ 'cursor-pointer': project.action === 'stroke' }" @click="openProject(project.action)">
          <div class="bg-[#f4efe6] border border-[#eae6de] rounded-2xl h-56 mb-5 flex items-center justify-center relative overflow-hidden group-hover:border-[#d9822b] transition-colors">
            <div v-if="project.chartType === 'line'" class="w-3/4 h-2/3 flex items-end">
              <svg class="w-full h-full text-[#d9822b]" viewBox="0 0 200 120" fill="none">
                <path d="M10 100 Q 60 40, 110 70 T 190 20" stroke="#d9822b" stroke-width="3" stroke-linecap="round"/>
              </svg>
            </div>
            <div v-else-if="project.chartType === 'bars'" class="w-3/4 h-2/3 flex items-end justify-around gap-2 px-4">
              <div class="w-6 bg-[#d9822b] opacity-30 h-1/2 rounded-t"></div>
              <div class="w-6 bg-[#d9822b] opacity-60 h-3/4 rounded-t"></div>
              <div class="w-6 bg-[#d9822b] h-full rounded-t"></div>
            </div>
            <div v-else class="w-full h-full flex flex-col items-center justify-center p-4 text-center">
              <div class="w-16 h-16 rounded-full border-4 border-[#d9822b] border-t-transparent mb-2"></div>
              <span class="text-[10px] font-bold text-[#d9822b] bg-white px-2 py-0.5 rounded shadow-sm">CLICK TO VIEW CASE STUDY</span>
            </div>
          </div>
          <div class="text-[11px] font-bold tracking-wider text-[#888] mb-2">{{ project.category }}</div>
          <h3 class="text-lg font-medium text-[#111] mb-2 leading-snug group-hover:text-[#d9822b] transition-colors">{{ project.title }}</h3>
          <p class="text-sm text-[#666] mb-4 leading-relaxed flex-grow">{{ project.description }}</p>
          <button v-if="project.action === 'stroke'" @click.stop="openProject(project.action)" class="text-xs font-semibold tracking-wider text-[#111] hover:text-[#d9822b] flex items-center gap-1 transition-colors text-left">
            VIEW CASE STUDY →
          </button>
        </div>
      </div>
    </section>

    <!-- Section 04 / Toolkit -->
    <section class="bg-[#1c3530] text-white py-24 mt-12">
      <div class="max-w-6xl mx-auto px-6">
        <div class="text-xs font-semibold tracking-widest text-[#d9822b] uppercase mb-3">04 / TOOLKIT</div>
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center mb-16">
          <div class="lg:col-span-6">
            <h2 class="text-3xl sm:text-4xl font-normal text-white mb-4">The Analytical Stack</h2>
            <p class="text-[#adb5bd] text-base leading-relaxed">
              Proficient across the modern data stack, from scripting and statistical modeling to visualization and deployment.
            </p>
          </div>
        </div>

        <div class="grid grid-cols-2 sm:grid-cols-4 gap-4">
          <div v-for="(tool, i) in toolkit" :key="i" class="bg-[#24433d] border border-[#2f554e] rounded-xl p-5 flex flex-col justify-between hover:border-[#d9822b] transition-colors">
            <span class="text-[10px] font-bold tracking-widest text-[#d9822b]">{{ tool.type }}</span>
            <span class="text-lg font-medium text-white mt-6">{{ tool.name }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
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
