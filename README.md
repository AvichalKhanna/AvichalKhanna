
<div align="center">

<!-- QUANTUM HEADER SVG -->
<svg width="900" height="250" viewBox="0 0 900 250" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <radialGradient id="bgGrad" cx="50%" cy="50%" r="60%">
      <stop offset="0%" stop-color="#0a0a1a"/>
      <stop offset="60%" stop-color="#050510"/>
      <stop offset="100%" stop-color="#000008"/>
    </radialGradient>
    <radialGradient id="arcReactor" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00d4ff" stop-opacity="0.9"/>
      <stop offset="40%" stop-color="#0066cc" stop-opacity="0.4"/>
      <stop offset="100%" stop-color="#000033" stop-opacity="0"/>
    </radialGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="2.5" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="softglow">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <!-- Arc reactor pulse animation -->
    <style>
      .star { animation: twinkle var(--d,3s) ease-in-out infinite alternate; opacity: var(--o,0.6); }
      @keyframes twinkle { 0%{opacity:0.1} 100%{opacity:1} }
      .particle { animation: drift var(--pd,8s) linear infinite; }
      @keyframes drift {
        0%   { transform: translate(0,0) scale(1);   opacity:0; }
        10%  { opacity:1; }
        90%  { opacity:0.6; }
        100% { transform: translate(var(--tx,20px), var(--ty,-60px)) scale(0.3); opacity:0; }
      }
      .ring { animation: pulse var(--rd,3s) ease-in-out infinite; transform-origin: 450px 125px; }
      @keyframes pulse { 0%,100%{opacity:0.15;transform:scale(0.95)} 50%{opacity:0.5;transform:scale(1.05)} }
      .circuit { animation: trace var(--cd,4s) ease-in-out infinite alternate; }
      @keyframes trace { 0%{stroke-dashoffset:200} 100%{stroke-dashoffset:0} }
      .orbit { animation: revolve var(--od,12s) linear infinite; transform-origin: 450px 125px; }
      @keyframes revolve { from{transform:rotate(0deg)} to{transform:rotate(360deg)} }
    </style>
  </defs>

  <!-- Background -->
  <rect width="900" height="250" fill="url(#bgGrad)"/>

  <!-- Stars field -->
  <circle class="star" style="--d:2.1s;--o:0.8" cx="45" cy="18" r="1" fill="#ffffff"/>
  <circle class="star" style="--d:3.4s;--o:0.5" cx="120" cy="42" r="0.8" fill="#a0c4ff"/>
  <circle class="star" style="--d:1.8s;--o:0.9" cx="200" cy="12" r="1.2" fill="#ffffff"/>
  <circle class="star" style="--d:4.1s;--o:0.6" cx="310" cy="35" r="0.7" fill="#c0b4ff"/>
  <circle class="star" style="--d:2.7s;--o:0.7" cx="420" cy="8" r="1" fill="#ffffff"/>
  <circle class="star" style="--d:3.9s;--o:0.4" cx="530" cy="28" r="1.3" fill="#a0c4ff"/>
  <circle class="star" style="--d:2.3s;--o:0.8" cx="640" cy="15" r="0.9" fill="#ffffff"/>
  <circle class="star" style="--d:4.5s;--o:0.5" cx="750" cy="38" r="0.7" fill="#c0b4ff"/>
  <circle class="star" style="--d:1.9s;--o:0.9" cx="830" cy="10" r="1.1" fill="#ffffff"/>
  <circle class="star" style="--d:3.2s;--o:0.6" cx="880" cy="45" r="0.8" fill="#a0c4ff"/>
  <circle class="star" style="--d:2.6s;--o:0.7" cx="70" cy="80" r="0.6" fill="#ffffff"/>
  <circle class="star" style="--d:4.0s;--o:0.5" cx="160" cy="95" r="1" fill="#c0b4ff"/>
  <circle class="star" style="--d:2.2s;--o:0.8" cx="780" cy="70" r="0.8" fill="#ffffff"/>
  <circle class="star" style="--d:3.7s;--o:0.4" cx="860" cy="100" r="1.2" fill="#a0c4ff"/>
  <circle class="star" style="--d:1.7s;--o:0.9" cx="30" cy="145" r="0.7" fill="#ffffff"/>
  <circle class="star" style="--d:4.3s;--o:0.5" cx="100" cy="175" r="1" fill="#c0b4ff"/>
  <circle class="star" style="--d:2.8s;--o:0.7" cx="810" cy="155" r="0.9" fill="#ffffff"/>
  <circle class="star" style="--d:3.5s;--o:0.6" cx="875" cy="180" r="0.7" fill="#a0c4ff"/>
  <circle class="star" style="--d:2.0s;--o:0.8" cx="55" cy="220" r="1.1" fill="#ffffff"/>
  <circle class="star" style="--d:4.2s;--o:0.4" cx="140" cy="238" r="0.8" fill="#c0b4ff"/>
  <circle class="star" style="--d:2.5s;--o:0.7" cx="760" cy="215" r="1" fill="#ffffff"/>
  <circle class="star" style="--d:3.8s;--o:0.5" cx="855" cy="235" r="0.6" fill="#a0c4ff"/>

  <!-- Circuit traces left -->
  <g filter="url(#glow)" opacity="0.5">
    <polyline class="circuit" style="--cd:3s" points="0,60 80,60 80,90 160,90" stroke="#00d4ff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <polyline class="circuit" style="--cd:4.5s" points="0,110 60,110 60,140 130,140" stroke="#9d8fff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <polyline class="circuit" style="--cd:2.8s" points="0,170 90,170 90,200 150,200" stroke="#00d4ff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <circle cx="80" cy="60" r="2" fill="#00d4ff" opacity="0.8"/>
    <circle cx="80" cy="90" r="2" fill="#00d4ff" opacity="0.8"/>
    <circle cx="60" cy="110" r="2" fill="#9d8fff" opacity="0.8"/>
    <circle cx="90" cy="170" r="2" fill="#00d4ff" opacity="0.8"/>
  </g>

  <!-- Circuit traces right -->
  <g filter="url(#glow)" opacity="0.5">
    <polyline class="circuit" style="--cd:3.5s" points="900,60 820,60 820,90 740,90" stroke="#00d4ff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <polyline class="circuit" style="--cd:4s" points="900,110 840,110 840,140 770,140" stroke="#9d8fff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <polyline class="circuit" style="--cd:2.5s" points="900,170 810,170 810,200 750,200" stroke="#00d4ff" stroke-width="0.8" fill="none" stroke-dasharray="200" stroke-dashoffset="200"/>
    <circle cx="820" cy="60" r="2" fill="#00d4ff" opacity="0.8"/>
    <circle cx="820" cy="90" r="2" fill="#00d4ff" opacity="0.8"/>
    <circle cx="840" cy="110" r="2" fill="#9d8fff" opacity="0.8"/>
    <circle cx="810" cy="170" r="2" fill="#00d4ff" opacity="0.8"/>
  </g>

  <!-- Arc reactor center glow -->
  <circle cx="450" cy="125" r="80" fill="url(#arcReactor)" opacity="0.3"/>

  <!-- Orbital rings -->
  <ellipse class="ring" style="--rd:4s" cx="450" cy="125" rx="70" ry="25" stroke="#00d4ff" stroke-width="0.6" fill="none" opacity="0.2"/>
  <ellipse class="ring" style="--rd:2.8s" cx="450" cy="125" rx="95" ry="35" stroke="#9d8fff" stroke-width="0.5" fill="none" opacity="0.15"/>
  <ellipse class="ring" style="--rd:5s" cx="450" cy="125" rx="120" ry="18" stroke="#00aaff" stroke-width="0.5" fill="none" opacity="0.15" transform="rotate(30 450 125)"/>

  <!-- Orbiting dots -->
  <g class="orbit" style="--od:8s">
    <circle cx="520" cy="125" r="3" fill="#00d4ff" filter="url(#glow)" opacity="0.9"/>
  </g>
  <g class="orbit" style="--od:14s">
    <circle cx="380" cy="125" r="2" fill="#9d8fff" filter="url(#glow)" opacity="0.8"/>
  </g>
  <g class="orbit" style="--od:6s">
    <circle cx="450" cy="55" r="2.5" fill="#00aaff" filter="url(#glow)" opacity="0.8"/>
  </g>

  <!-- Floating particles -->
  <circle class="particle" style="--pd:7s;--tx:30px;--ty:-80px" cx="350" cy="180" r="1.5" fill="#00d4ff" opacity="0"/>
  <circle class="particle" style="--pd:9s;--tx:-20px;--ty:-70px" cx="420" cy="200" r="1" fill="#9d8fff" opacity="0" animation-delay="1s"/>
  <circle class="particle" style="--pd:6s;--tx:40px;--ty:-90px" cx="500" cy="190" r="2" fill="#00aaff" opacity="0"/>
  <circle class="particle" style="--pd:11s;--tx:-30px;--ty:-60px" cx="560" cy="170" r="1.2" fill="#c0b4ff" opacity="0"/>
  <circle class="particle" style="--pd:8s;--tx:15px;--ty:-75px" cx="300" cy="165" r="1.8" fill="#00d4ff" opacity="0"/>

  <!-- Main title -->
  <text x="450" y="108" text-anchor="middle" font-family="'Courier New', monospace" font-size="42" font-weight="700" fill="#e8e4ff" filter="url(#softglow)" letter-spacing="3">AVICHAL KHANNA</text>

  <!-- Subtitle -->
  <text x="450" y="138" text-anchor="middle" font-family="'Courier New', monospace" font-size="13" fill="#9d8fff" letter-spacing="2">AI / ML ENGINEER  •  BUILDER OF THINGS THAT SHOULD NOT EXIST YET</text>

  <!-- Bottom accent line -->
  <line x1="280" y1="158" x2="620" y2="158" stroke="#00d4ff" stroke-width="0.5" opacity="0.4"/>
  <circle cx="280" cy="158" r="2" fill="#00d4ff" opacity="0.6" filter="url(#glow)"/>
  <circle cx="620" cy="158" r="2" fill="#00d4ff" opacity="0.6" filter="url(#glow)"/>
  <circle cx="450" cy="158" r="3" fill="#9d8fff" opacity="0.8" filter="url(#glow)"/>
</svg>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=17&pause=1000&color=9D8FFF&center=true&vCenter=true&width=620&lines=LLM+Inference+%7C+RLHF+%7C+MoE+Transformers;4.2x+throughput+%7C+73%25+harmful+output+reduction;Building+JARVIS+from+scratch;B.Tech+Data+Science+%40+MUJ+%E2%80%A2+CGPA+9.89;Open+to+ML%2FAI+Internships)](https://github.com/AvichalKhanna)

<br/>

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/avichalkhanna)&nbsp;
[![Gmail](https://img.shields.io/badge/-Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:avichalkhanna111@gmail.com)&nbsp;
[![GitHub](https://img.shields.io/badge/-GitHub-161b22?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;
![Visitors](https://komarev.com/ghpvc/?username=AvichalKhanna&color=9d8fff&style=for-the-badge&label=PROFILE+VIEWS)

</div>

---

## ⚡ About Me

- 🎓 B.Tech Data Science · Manipal University Jaipur · **CGPA 9.89** · Graduating 2028
- 🧠 Building production-grade ML systems — LLM inference, RLHF pipelines, MoE architectures
- 🤖 Currently building **CANDIS** — a fully local, always-on personal AI OS (JARVIS-style)
- 🏛️ Joint Secretary · Cyber Space Club · 150+ members · 15,000+ students impacted
- ⚙️ Hardware: GTX 1650 · Oracle VPS · Android via Termux
- 🚀 Seeking **ML / AI Internship**

---

## 🏅 Highlights

| Award | Details |
|---|---|
| 🏆 **Inspire Award Manak** | Rs. 10,000 grant · Dept. of Science & Technology, Govt. of India · Top district-level nominee nationwide |
| 🥇 **Cosmos Hackathon — 1st Place** | Audience Favourite among 400+ participants · shipped working ML solution in 24 hours |
| 📋 **Dean's List — 3 Consecutive Semesters** | Top 1% of Data Science cohort · CGPA 9.89/10 across all semesters |

---

## 🚀 Featured Projects

### ⚡ LLM Inference Optimization Engine
> `Python` `PyTorch` `CUDA` `Triton` `Docker` `Kubernetes`

Serving system for LLaMA-2-7B with continuous batching, KV-cache management, and INT8 quantization.
- **4.2x throughput improvement** vs naive serving
- **60% memory reduction** · Benchmarked against vLLM baseline

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Benchmark](https://img.shields.io/badge/-View%20Benchmark-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

### 🧠 Sparse MoE Transformer — Switch Transformer Replication
> `PyTorch` `CUDA` `Weights & Biases` `HuggingFace`

Implemented Sparse Mixture-of-Experts from scratch on WikiText-103 with 8-expert routing.
- **2.4x throughput** over dense baseline at equivalent perplexity
- Optimized load balancing loss to prevent expert collapse

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

### 🎯 RLHF Fine-tuning Pipeline
> `PyTorch` `TRL` `HuggingFace` `Weights & Biases`

End-to-end RLHF on GPT-2: SFT → reward model training → PPO-based policy optimization.
- **73% reduction in harmful outputs** on custom safety benchmark vs base model

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-View%20Results-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

### 🤖 PRism — AI GitHub PR Review Agent
> `FastAPI` `Groq llama-3.3-70b` `Supabase` `React/Vite` `Render`

Automated pull request reviewer that hooks into GitHub events, runs LLM analysis via Groq, tracks history in Supabase, and surfaces results on a live React dashboard.

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna/PRism)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna/PRism)

---

### 🔍 Neural Information Retrieval Engine
> `PyTorch` `FAISS` `Elasticsearch` `FastAPI` `Docker` `AWS`

Hybrid dense-sparse retrieval: BM25 + fine-tuned bi-encoder (BERT) + FAISS over 1M+ document corpus.
- **MRR@10 of 0.38** — 31% over BM25 baseline
- **sub-50ms p99 latency** via FastAPI

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

### 🎬 YouTube Shorts Automation Pipeline
> `FFmpeg` `Groq TTS` `Gemini` `FastAPI` `React/Vite`

Records developer portfolio sites → AI script via Gemini → voiceover via Groq TTS → word-by-word subtitle burn via FFmpeg → auto-upload to YouTube. Fully autonomous, zero human touch.

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![YouTube](https://img.shields.io/badge/-YouTube%20Channel-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://youtube.com/@DesignWithKaran)

---

### 🌾 Krishi Mitra AI — AI for Indian Farmers
> `Computer Vision` `NLP` `PyTorch` `Python`

Crop disease detection + E-Tehsil services + 30-day weather, yield, and navigation forecasting for India's agricultural sector.

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

### 🧘 Saarthi — AI Therapy Assistant
> `PyTorch` `Opacus` `gRPC` `Docker` `Python`

Privacy-first AI therapy assistant with voice I/O, empathetic conversation, and appointment booking with human therapists via function calling.

[![GitHub](https://img.shields.io/badge/-View%20Code-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/AvichalKhanna)&nbsp;[![Live Demo](https://img.shields.io/badge/-Live%20Demo-9d8fff?style=flat-square&logo=vercel&logoColor=white)](https://github.com/AvichalKhanna)

---

## 🛠 Tech Stack

<div align="center">

![skills](https://skillicons.dev/icons?i=python,pytorch,tensorflow,fastapi,react,docker,kubernetes,aws,linux,git,postgres,redis&perline=12)

</div>

| Domain | Stack |
|---|---|
| **ML / AI** | PyTorch · TensorFlow · HuggingFace · Scikit-Learn · OpenCV · SpaCy · NLTK |
| **LLM Systems** | llama.cpp · TRL · GGUF · bitsandbytes · FAISS · Triton · vLLM |
| **APIs / Backend** | FastAPI · Flask · Django · Node.js · Express · GraphQL · gRPC |
| **Cloud / DevOps** | AWS (EC2, S3, Lambda) · GCP (BigQuery, Vertex AI) · Docker · Kubernetes · CI/CD |
| **Databases** | PostgreSQL · MySQL · SQLite · Redis · Elasticsearch · Supabase |
| **Languages** | Python · C++ · Java · JavaScript · TypeScript · SQL · Bash |

---

## 📊 GitHub Stats

<div align="center">

<table border="0" cellpadding="6">
  <tr>
    <td>
      <img src="https://github-readme-stats.vercel.app/api?username=AvichalKhanna&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=9d8fff&icon_color=9d8fff&text_color=c9d1d9&rank_icon=github" />
    </td>
    <td>
      <img src="https://streak-stats.demolab.com?user=AvichalKhanna&theme=tokyonight&hide_border=true&background=0d1117&ring=9d8fff&fire=9d8fff&currStreakLabel=9d8fff" />
    </td>
  </tr>
</table>

</div>

---

## 🕸 Contribution Map

<div align="center">

![activity](https://github-readme-activity-graph.vercel.app/graph?username=AvichalKhanna&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=9d8fff&line=9d8fff&point=e0d7ff&area=true&area_color=9d8fff&height=220)

</div>

---

<!-- QUANTUM FOOTER SVG -->
<div align="center">
<svg width="900" height="140" viewBox="0 0 900 140" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <radialGradient id="fBg" cx="50%" cy="0%" r="80%">
      <stop offset="0%" stop-color="#0a0a2a"/>
      <stop offset="100%" stop-color="#000008"/>
    </radialGradient>
    <filter id="fGlow">
      <feGaussianBlur stdDeviation="2" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <style>
      .fstar { animation: ftwinkle var(--d,3s) ease-in-out infinite alternate; }
      @keyframes ftwinkle { 0%{opacity:0.1} 100%{opacity:0.9} }
      .fcirc { animation: fpulse var(--d,4s) ease-in-out infinite; }
      @keyframes fpulse { 0%,100%{r:var(--r1,3);opacity:0.2} 50%{r:var(--r2,6);opacity:0.6} }
      .fline { animation: ftrace var(--d,5s) ease-in-out infinite alternate; }
      @keyframes ftrace { 0%{opacity:0.05} 100%{opacity:0.45} }
    </style>
  </defs>

  <rect width="900" height="140" fill="url(#fBg)"/>

  <!-- Top border glow -->
  <line x1="0" y1="1" x2="900" y2="1" stroke="#9d8fff" stroke-width="0.5" opacity="0.3"/>
  <line x1="0" y1="1" x2="900" y2="1" stroke="#00d4ff" stroke-width="0.3" opacity="0.2"/>

  <!-- Stars -->
  <circle class="fstar" style="--d:2.1s" cx="50" cy="30" r="1" fill="#fff" opacity="0.6"/>
  <circle class="fstar" style="--d:3.4s" cx="130" cy="15" r="0.8" fill="#a0c4ff" opacity="0.5"/>
  <circle class="fstar" style="--d:1.8s" cx="230" cy="45" r="1.1" fill="#fff" opacity="0.7"/>
  <circle class="fstar" style="--d:4.0s" cx="370" cy="20" r="0.7" fill="#c0b4ff" opacity="0.5"/>
  <circle class="fstar" style="--d:2.6s" cx="500" cy="38" r="1" fill="#fff" opacity="0.6"/>
  <circle class="fstar" style="--d:3.8s" cx="620" cy="12" r="0.9" fill="#a0c4ff" opacity="0.5"/>
  <circle class="fstar" style="--d:2.3s" cx="740" cy="40" r="1.2" fill="#fff" opacity="0.7"/>
  <circle class="fstar" style="--d:4.5s" cx="840" cy="22" r="0.7" fill="#c0b4ff" opacity="0.4"/>
  <circle class="fstar" style="--d:1.9s" cx="880" cy="55" r="1" fill="#fff" opacity="0.6"/>
  <circle class="fstar" style="--d:3.1s" cx="20" cy="80" r="0.8" fill="#a0c4ff" opacity="0.4"/>
  <circle class="fstar" style="--d:2.7s" cx="160" cy="95" r="1" fill="#fff" opacity="0.5"/>
  <circle class="fstar" style="--d:4.2s" cx="700" cy="90" r="0.9" fill="#c0b4ff" opacity="0.4"/>
  <circle class="fstar" style="--d:2.0s" cx="860" cy="100" r="1.1" fill="#fff" opacity="0.6"/>

  <!-- Horizontal quantum lines -->
  <line class="fline" style="--d:3s" x1="0" y1="65" x2="340" y2="65" stroke="#00d4ff" stroke-width="0.5"/>
  <line class="fline" style="--d:4s" x1="560" y1="65" x2="900" y2="65" stroke="#00d4ff" stroke-width="0.5"/>

  <!-- Center node -->
  <circle class="fcirc" style="--d:3s;--r1:4;--r2:8" cx="450" cy="65" r="4" fill="none" stroke="#9d8fff" stroke-width="1" filter="url(#fGlow)"/>
  <circle cx="450" cy="65" r="2.5" fill="#9d8fff" opacity="0.9" filter="url(#fGlow)"/>

  <!-- Side nodes -->
  <circle cx="340" cy="65" r="2" fill="#00d4ff" opacity="0.7" filter="url(#fGlow)"/>
  <circle cx="560" cy="65" r="2" fill="#00d4ff" opacity="0.7" filter="url(#fGlow)"/>

  <!-- Footer text -->
  <text x="450" y="110" text-anchor="middle" font-family="'Courier New', monospace" font-size="11" fill="#9d8fff" opacity="0.7" letter-spacing="2">⚡ BUILDING THE FUTURE, ONE MODEL AT A TIME ⚡</text>
  <text x="450" y="128" text-anchor="middle" font-family="'Courier New', monospace" font-size="9" fill="#5a5a8a" letter-spacing="1">avichalkhanna111@gmail.com  •  github.com/AvichalKhanna</text>
</svg>
</div>
