# Day-10-of-Claude-AI-challenge-
Day 10/60 - Built a complete AI-powered  personal portfolio website using Claude AI.  No coding background. Just prompt engineering  + consistency. ABTalks 60-Day Claude Challenge  🚀 #ClaudeAI #ABTalks #BuildInPublic
# Day 10 - AI Portfolio Website 🌐

## What I Built
A complete personal portfolio website using 
Claude AI — no manual coding required.

## Features
- Hero section with typing animation
- Dark/Light mode toggle
- Animated skill bars
- Project showcase cards
- Achievements section
- Contact form
- Mobile responsive
- Smooth scroll animations

## Skills Used
- Prompt Engineering
- AI-Assisted Web Development
- HTML + Tailwind CSS
- Vanilla JavaScript

## Tools
- Claude AI (claude.ai)
- GitHub Pages

## Key Learning
Modern portfolios can be built by anyone 
using AI — no coding background needed.

## Part of
ABTalks 60-Day Claude AI Mastery Challenge
Day 10/60 ✅

## Live File
<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anamika Dixit | Performance Marketing Freelancer</title>
  <meta name="description" content="Anamika Dixit - Performance Marketing Freelancer specializing in Google Ads, Meta Ads, and GA4. Founder of NexaGrowth Digital." />
  <meta name="keywords" content="Performance Marketing, Google Ads, Meta Ads, GA4, Freelancer, NexaGrowth Digital, Kanpur" />
  <meta property="og:title" content="Anamika Dixit | Performance Marketing Freelancer" />
  <meta property="og:description" content="Helping brands grow with data-driven performance marketing." />
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            brand: {
              pink: '#F472B6',
              purple: '#A855F7',
              rose: '#FB7185',
              dark: '#0D0D14',
              card: '#13131F',
              border: '#1E1E2E',
            }
          },
          fontFamily: {
            display: ['Syne', 'sans-serif'],
            body: ['Inter', 'sans-serif'],
          }
        }
      }
    }
  </script>
  <style>
    * { scroll-behavior: smooth; }
    body { font-family: 'Inter', sans-serif; }
    h1, h2, h3, .font-display { font-family: 'Syne', sans-serif; }

    /* Gradient text */
    .grad-text {
      background: linear-gradient(135deg, #F472B6 0%, #A855F7 50%, #FB7185 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* Glow effect */
    .glow {
      box-shadow: 0 0 30px rgba(168, 85, 247, 0.15), 0 0 60px rgba(244, 114, 182, 0.08);
    }

    /* Nav active */
    .nav-active { color: #F472B6 !important; }

    /* Skill bar animation */
    .skill-bar { transition: width 1.5s cubic-bezier(0.4, 0, 0.2, 1); }

    /* Typing cursor */
    .cursor::after {
      content: '|';
      animation: blink 0.8s infinite;
      color: #F472B6;
    }
    @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }

    /* Fade in on scroll */
    .fade-in { opacity: 0; transform: translateY(30px); transition: all 0.7s ease; }
    .fade-in.visible { opacity: 1; transform: translateY(0); }

    /* Card hover */
    .project-card {
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border: 1px solid #1E1E2E;
    }
    .project-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 20px 40px rgba(168, 85, 247, 0.2);
      border-color: #A855F7;
    }

    /* Light mode overrides */
    html.light body { background: #F8F8FC; color: #1a1a2e; }
    html.light .bg-brand-dark { background: #F8F8FC; }
    html.light .bg-brand-card { background: #FFFFFF; }
    html.light .text-gray-300 { color: #4a4a6a; }
    html.light .text-gray-400 { color: #6a6a8a; }
    html.light .text-gray-500 { color: #8a8aaa; }
    html.light .border-brand-border { border-color: #E2E2F0; }
    html.light nav { background: rgba(248, 248, 252, 0.95) !important; border-color: #E2E2F0; }
    html.light .project-card { border-color: #E2E2F0; background: #FFFFFF; }
    html.light .project-card:hover { border-color: #A855F7; }

    /* Hero bg pattern */
    .hero-bg {
      background:
        radial-gradient(ellipse 80% 50% at 50% -10%, rgba(168,85,247,0.18) 0%, transparent 70%),
        radial-gradient(ellipse 40% 30% at 80% 60%, rgba(244,114,182,0.1) 0%, transparent 60%);
    }

    /* Scrollbar */
    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: #0D0D14; }
    ::-webkit-scrollbar-thumb { background: #A855F7; border-radius: 2px; }
  </style>
</head>
<body class="bg-brand-dark text-white min-h-screen">

  <!-- NAV -->
  <nav id="navbar" class="fixed top-0 left-0 right-0 z-50 bg-brand-dark/90 backdrop-blur-md border-b border-brand-border transition-all duration-300">
    <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
      <a href="#home" class="font-display font-800 text-xl grad-text">AD</a>
      <div class="hidden md:flex items-center gap-8">
        <a href="#about" class="nav-link text-gray-400 hover:text-white text-sm font-medium transition-colors">About</a>
        <a href="#skills" class="nav-link text-gray-400 hover:text-white text-sm font-medium transition-colors">Skills</a>
        <a href="#projects" class="nav-link text-gray-400 hover:text-white text-sm font-medium transition-colors">Projects</a>
        <a href="#achievements" class="nav-link text-gray-400 hover:text-white text-sm font-medium transition-colors">Achievements</a>
        <a href="#contact" class="nav-link text-gray-400 hover:text-white text-sm font-medium transition-colors">Contact</a>
      </div>
      <div class="flex items-center gap-3">
        <button onclick="toggleTheme()" class="w-9 h-9 rounded-full border border-brand-border flex items-center justify-center text-gray-400 hover:text-white hover:border-brand-purple transition-all" title="Toggle theme">
          <span id="theme-icon">☀️</span>
        </button>
        <!-- Mobile menu -->
        <button onclick="toggleMobileMenu()" class="md:hidden w-9 h-9 rounded-full border border-brand-border flex items-center justify-center text-gray-400">☰</button>
      </div>
    </div>
    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden md:hidden bg-brand-card border-t border-brand-border px-4 py-4">
      <div class="flex flex-col gap-4">
        <a href="#about" onclick="closeMobileMenu()" class="text-gray-300 hover:text-brand-pink font-medium">About</a>
        <a href="#skills" onclick="closeMobileMenu()" class="text-gray-300 hover:text-brand-pink font-medium">Skills</a>
        <a href="#projects" onclick="closeMobileMenu()" class="text-gray-300 hover:text-brand-pink font-medium">Projects</a>
        <a href="#achievements" onclick="closeMobileMenu()" class="text-gray-300 hover:text-brand-pink font-medium">Achievements</a>
        <a href="#contact" onclick="closeMobileMenu()" class="text-gray-300 hover:text-brand-pink font-medium">Contact</a>
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <section id="home" class="hero-bg min-h-screen flex items-center justify-center px-4 pt-20">
    <div class="max-w-4xl mx-auto text-center">
      <!-- Badge -->
      <div class="inline-flex items-center gap-2 bg-brand-card border border-brand-border rounded-full px-4 py-1.5 mb-8 text-sm text-gray-400">
        <span class="w-2 h-2 rounded-full bg-green-400 animate-pulse"></span>
        Available for freelance projects
      </div>

      <!-- Name -->
      <h1 class="font-display text-5xl md:text-7xl font-800 mb-4 leading-tight">
        Anamika<br/><span class="grad-text">Dixit</span>
      </h1>

      <!-- Typing title -->
      <p class="text-xl md:text-2xl text-gray-300 mb-6 font-medium">
        <span id="typed-text" class="cursor"></span>
      </p>

      <!-- Location -->
      <p class="text-gray-500 mb-8 flex items-center justify-center gap-2">
        <span>📍</span> Kanpur, Uttar Pradesh, India
      </p>

      <!-- CTA Buttons -->
      <div class="flex flex-wrap items-center justify-center gap-4 mb-12">
        <a href="#projects" class="px-6 py-3 rounded-full font-semibold text-sm" style="background: linear-gradient(135deg, #F472B6, #A855F7); color: white;">
          View My Work ✨
        </a>
        <a href="#contact" class="px-6 py-3 rounded-full font-semibold text-sm border border-brand-border text-gray-300 hover:border-brand-purple hover:text-white transition-all">
          Let's Connect →
        </a>
      </div>

      <!-- Social Links -->
      <div class="flex items-center justify-center gap-5">
        <a href="https://www.linkedin.com/in/anamika-dixit-198a293b9" target="_blank" class="flex items-center gap-2 text-gray-400 hover:text-brand-pink transition-colors text-sm font-medium">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
        <a href="https://github.com/Anamikalearns-ai" target="_blank" class="flex items-center gap-2 text-gray-400 hover:text-brand-purple transition-colors text-sm font-medium">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
          GitHub
        </a>
        <a href="https://instagram.com/anamika.learnsppc" target="_blank" class="flex items-center gap-2 text-gray-400 hover:text-brand-rose transition-colors text-sm font-medium">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" fill="none" stroke="currentColor" stroke-width="2"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5" stroke="currentColor" stroke-width="2"/></svg>
          Instagram
        </a>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" class="py-24 px-4">
    <div class="max-w-5xl mx-auto">
      <div class="fade-in grid md:grid-cols-2 gap-12 items-center">
        <div>
          <p class="text-brand-pink text-sm font-semibold tracking-widest uppercase mb-3">About Me</p>
          <h2 class="font-display text-4xl md:text-5xl font-bold mb-6">
            Turning Clicks into<br/><span class="grad-text">Conversions</span>
          </h2>
          <p class="text-gray-300 leading-relaxed mb-4">
            I'm a performance marketing freelancer from Kanpur, India, specializing in Google Ads, Meta Ads, and GA4 analytics. I founded <strong class="text-white">NexaGrowth Digital</strong> with one mission — helping businesses grow through data-driven ad strategies.
          </p>
          <p class="text-gray-400 leading-relaxed mb-6">
            Currently on a 60-Day AI Mastery journey, building AI-powered tools and documenting my learning publicly. I believe in learning out loud and growing together with the community.
          </p>
          <div class="flex flex-wrap gap-3">
            <span class="px-3 py-1.5 rounded-full text-xs font-medium bg-pink-500/10 text-pink-400 border border-pink-500/20">🎯 Performance Marketing</span>
            <span class="px-3 py-1.5 rounded-full text-xs font-medium bg-purple-500/10 text-purple-400 border border-purple-500/20">🤖 AI Enthusiast</span>
            <span class="px-3 py-1.5 rounded-full text-xs font-medium bg-rose-500/10 text-rose-400 border border-rose-500/20">📊 Data Analytics</span>
          </div>
        </div>
        <div class="grid grid-cols-2 gap-4">
          <div class="bg-brand-card border border-brand-border rounded-2xl p-6 glow">
            <p class="text-3xl font-display font-bold grad-text">1+</p>
            <p class="text-gray-400 text-sm mt-1">Year Learning Journey</p>
          </div>
          <div class="bg-brand-card border border-brand-border rounded-2xl p-6">
            <p class="text-3xl font-display font-bold grad-text">10+</p>
            <p class="text-gray-400 text-sm mt-1">AI Projects Built</p>
          </div>
          <div class="bg-brand-card border border-brand-border rounded-2xl p-6">
            <p class="text-3xl font-display font-bold grad-text">3</p>
            <p class="text-gray-400 text-sm mt-1">Core Specializations</p>
          </div>
          <div class="bg-brand-card border border-brand-border rounded-2xl p-6 glow">
            <p class="text-3xl font-display font-bold grad-text">60</p>
            <p class="text-gray-400 text-sm mt-1">Day AI Challenge</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills" class="py-24 px-4 bg-brand-card">
    <div class="max-w-5xl mx-auto">
      <div class="fade-in text-center mb-14">
        <p class="text-brand-pink text-sm font-semibold tracking-widest uppercase mb-3">What I Know</p>
        <h2 class="font-display text-4xl md:text-5xl font-bold">Skills & <span class="grad-text">Expertise</span></h2>
      </div>

      <div class="fade-in grid md:grid-cols-2 gap-12">
        <!-- Skill bars -->
        <div>
          <h3 class="font-display text-lg font-semibold mb-6 text-gray-200">Core Skills</h3>
          <div class="space-y-5" id="skill-bars">
            <div>
              <div class="flex justify-between text-sm mb-2"><span class="text-gray-300">Google Ads</span><span class="text-brand-pink">85%</span></div>
              <div class="h-2 bg-brand-border rounded-full overflow-hidden"><div class="skill-bar h-full rounded-full w-0" style="background: linear-gradient(90deg, #F472B6, #A855F7)" data-width="85%"></div></div>
            </div>
            <div>
              <div class="flex justify-between text-sm mb-2"><span class="text-gray-300">Meta Ads</span><span class="text-brand-pink">80%</span></div>
              <div class="h-2 bg-brand-border rounded-full overflow-hidden"><div class="skill-bar h-full rounded-full w-0" style="background: linear-gradient(90deg, #A855F7, #FB7185)" data-width="80%"></div></div>
            </div>
            <div>
              <div class="flex justify-between text-sm mb-2"><span class="text-gray-300">GA4 Analytics</span><span class="text-brand-pink">75%</span></div>
              <div class="h-2 bg-brand-border rounded-full overflow-hidden"><div class="skill-bar h-full rounded-full w-0" style="background: linear-gradient(90deg, #F472B6, #A855F7)" data-width="75%"></div></div>
            </div>
            <div>
              <div class="flex justify-between text-sm mb-2"><span class="text-gray-300">AI Prompt Engineering</span><span class="text-brand-pink">90%</span></div>
              <div class="h-2 bg-brand-border rounded-full overflow-hidden"><div class="skill-bar h-full rounded-full w-0" style="background: linear-gradient(90deg, #A855F7, #FB7185)" data-width="90%"></div></div>
            </div>
            <div>
              <div class="flex justify-between text-sm mb-2"><span class="text-gray-300">Content Marketing</span><span class="text-brand-pink">78%</span></div>
              <div class="h-2 bg-brand-border rounded-full overflow-hidden"><div class="skill-bar h-full rounded-full w-0" style="background: linear-gradient(90deg, #F472B6, #A855F7)" data-width="78%"></div></div>
            </div>
          </div>
        </div>

        <!-- Tech tags -->
        <div>
          <h3 class="font-display text-lg font-semibold mb-6 text-gray-200">Tools & Technologies</h3>
          <div class="flex flex-wrap gap-2 mb-8">
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">Google Ads Manager</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">Meta Business Suite</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">Google Analytics 4</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">Claude AI</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">Canva</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">CapCut</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">GitHub</span>
            <span class="px-3 py-1.5 bg-brand-dark border border-brand-border rounded-full text-xs text-gray-300 hover:border-brand-pink hover:text-brand-pink transition-all cursor-default">HTML/CSS</span>
          </div>

          <h3 class="font-display text-lg font-semibold mb-4 text-gray-200">Soft Skills</h3>
          <div class="flex flex-wrap gap-2">
            <span class="px-3 py-1.5 bg-purple-500/10 border border-purple-500/20 rounded-full text-xs text-purple-300">Strategic Thinking</span>
            <span class="px-3 py-1.5 bg-pink-500/10 border border-pink-500/20 rounded-full text-xs text-pink-300">Client Communication</span>
            <span class="px-3 py-1.5 bg-rose-500/10 border border-rose-500/20 rounded-full text-xs text-rose-300">Self Learning</span>
            <span class="px-3 py-1.5 bg-purple-500/10 border border-purple-500/20 rounded-full text-xs text-purple-300">Problem Solving</span>
            <span class="px-3 py-1.5 bg-pink-500/10 border border-pink-500/20 rounded-full text-xs text-pink-300">Content Creation</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects" class="py-24 px-4">
    <div class="max-w-5xl mx-auto">
      <div class="fade-in text-center mb-14">
        <p class="text-brand-pink text-sm font-semibold tracking-widest uppercase mb-3">What I've Built</p>
        <h2 class="font-display text-4xl md:text-5xl font-bold">Featured <span class="grad-text">Projects</span></h2>
      </div>

      <div class="fade-in grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Project 1 -->
        <div class="project-card bg-brand-card rounded-2xl p-6">
          <div class="w-10 h-10 rounded-xl flex items-center justify-center text-xl mb-4" style="background: linear-gradient(135deg, #F472B6, #A855F7)">🥗</div>
          <h3 class="font-display font-bold text-lg mb-2">NutriScope</h3>
          <p class="text-gray-400 text-sm leading-relaxed mb-4">AI-powered nutrition tracking app that analyzes meals and gives personalized health insights using Claude AI.</p>
          <div class="flex flex-wrap gap-1.5">
            <span class="px-2 py-0.5 bg-pink-500/10 text-pink-400 rounded text-xs">HTML</span>
            <span class="px-2 py-0.5 bg-purple-500/10 text-purple-400 rounded text-xs">Claude AI</span>
            <span class="px-2 py-0.5 bg-rose-500/10 text-rose-400 rounded text-xs">JavaScript</span>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card bg-brand-card rounded-2xl p-6">
          <div class="w-10 h-10 rounded-xl flex items-center justify-center text-xl mb-4" style="background: linear-gradient(135deg, #A855F7, #FB7185)">🌿</div>
          <h3 class="font-display font-bold text-lg mb-2">Environmental Health Analyzer</h3>
          <p class="text-gray-400 text-sm leading-relaxed mb-4">AI dashboard that analyzes environmental health data and visualizes pollution, air quality, and climate insights.</p>
          <div class="flex flex-wrap gap-1.5">
            <span class="px-2 py-0.5 bg-pink-500/10 text-pink-400 rounded text-xs">React</span>
            <span class="px-2 py-0.5 bg-purple-500/10 text-purple-400 rounded text-xs">Claude AI</span>
            <span class="px-2 py-0.5 bg-rose-500/10 text-rose-400 rounded text-xs">Data Viz</span>
          </div>
        </div>

        <!-- Project 3 -->
 
