<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body, .readme-root {
    background: transparent;
    font-family: 'Inter', sans-serif;
    color: var(--text-primary);
  }

  .readme-root {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 0 2rem;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    overflow: hidden;
    border-radius: 16px;
    padding: 3rem 2.5rem 2.5rem;
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    margin-bottom: 1.5rem;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 50% at 80% 20%, rgba(168,85,247,0.18) 0%, transparent 70%),
      radial-gradient(ellipse 40% 60% at 10% 80%, rgba(34,211,238,0.12) 0%, transparent 60%);
    pointer-events: none;
  }

  .hero-grid {
    position: absolute;
    inset: 0;
    background-image: linear-gradient(rgba(168,85,247,0.06) 1px, transparent 1px),
                      linear-gradient(90deg, rgba(168,85,247,0.06) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
  }

  .hero-content { position: relative; z-index: 1; }

  .hero-top {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  .hero-avatar {
    width: 72px; height: 72px;
    border-radius: 50%;
    background: linear-gradient(135deg, #A855F7 0%, #22D3EE 100%);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Fira Code', monospace;
    font-size: 22px; font-weight: 700;
    color: #fff;
    flex-shrink: 0;
    box-shadow: 0 0 0 3px rgba(168,85,247,0.25);
  }

  .hero-name {
    font-size: 2.4rem;
    font-weight: 700;
    letter-spacing: -0.03em;
    line-height: 1.1;
    background: linear-gradient(135deg, #A855F7 0%, #22D3EE 60%, #A855F7 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 0.4rem;
  }

  .hero-role {
    font-size: 0.85rem;
    font-weight: 500;
    color: var(--text-muted);
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  .status-dot {
    display: inline-block;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: #22D3EE;
    margin-right: 6px;
    box-shadow: 0 0 0 3px rgba(34,211,238,0.2);
    animation: pulse-dot 2s ease-in-out infinite;
  }

  @keyframes pulse-dot {
    0%, 100% { box-shadow: 0 0 0 3px rgba(34,211,238,0.2); }
    50% { box-shadow: 0 0 0 6px rgba(34,211,238,0.08); }
  }

  .hero-links {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
    margin-top: 1.5rem;
  }

  .hero-link {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 999px;
    font-size: 0.78rem;
    font-weight: 500;
    text-decoration: none;
    border: 0.5px solid var(--border-strong);
    color: var(--text-secondary);
    background: var(--surface-2);
    transition: all 0.2s;
    cursor: pointer;
  }

  .hero-link:hover {
    border-color: rgba(168,85,247,0.5);
    color: #A855F7;
    background: rgba(168,85,247,0.06);
  }

  .hero-link.accent {
    background: linear-gradient(135deg, rgba(168,85,247,0.15), rgba(34,211,238,0.08));
    border-color: rgba(168,85,247,0.4);
    color: #A855F7;
  }

  /* ── DIVIDER ── */
  .section-divider {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin: 1.5rem 0 1rem;
  }

  .section-divider-line {
    flex: 1;
    height: 0.5px;
    background: linear-gradient(90deg, transparent, rgba(168,85,247,0.3), transparent);
  }

  .section-label {
    font-family: 'Fira Code', monospace;
    font-size: 0.72rem;
    font-weight: 600;
    color: #A855F7;
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }

  /* ── CODE BLOCK ── */
  .code-block {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    margin-bottom: 1.5rem;
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 10px 16px;
    border-bottom: 0.5px solid var(--border);
    background: var(--surface-0);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-r { background: #FF5F57; }
  .dot-y { background: #FFBD2E; }
  .dot-g { background: #28CA41; }

  .code-filename {
    font-family: 'Fira Code', monospace;
    font-size: 0.72rem;
    color: var(--text-muted);
    margin-left: 8px;
  }

  .code-body {
    padding: 1.2rem 1.5rem;
    font-family: 'Fira Code', monospace;
    font-size: 0.8rem;
    line-height: 1.8;
    color: var(--text-secondary);
    overflow-x: auto;
  }

  .t-purple { color: #A855F7; }
  .t-cyan   { color: #22D3EE; }
  .t-green  { color: #4ADE80; }
  .t-orange { color: #FB923C; }
  .t-muted  { color: var(--text-muted); }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
    gap: 10px;
    margin-bottom: 1.5rem;
  }

  .skill-card {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 12px;
    padding: 14px 12px;
    text-align: center;
    transition: all 0.2s;
    cursor: default;
  }

  .skill-card:hover {
    border-color: rgba(168,85,247,0.4);
    background: rgba(168,85,247,0.04);
    transform: translateY(-1px);
  }

  .skill-icon {
    font-size: 1.5rem;
    margin-bottom: 6px;
    display: block;
  }

  .skill-name {
    font-size: 0.72rem;
    font-weight: 600;
    color: var(--text-secondary);
    letter-spacing: 0.05em;
  }

  /* ── PROJECTS GRID ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 12px;
    margin-bottom: 1.5rem;
  }

  .project-card {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 12px;
    padding: 1.2rem;
    position: relative;
    overflow: hidden;
    transition: all 0.2s;
    cursor: pointer;
    text-decoration: none;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }

  .project-card.v1::before { background: linear-gradient(90deg, #A855F7, #22D3EE); }
  .project-card.v2::before { background: linear-gradient(90deg, #22D3EE, #4ADE80); }
  .project-card.v3::before { background: linear-gradient(90deg, #FB923C, #A855F7); }
  .project-card.v4::before { background: linear-gradient(90deg, #4ADE80, #22D3EE); }
  .project-card.v5::before { background: linear-gradient(90deg, #F472B6, #A855F7); }

  .project-card:hover {
    border-color: rgba(168,85,247,0.35);
    transform: translateY(-2px);
  }

  .project-emoji {
    font-size: 1.6rem;
    margin-bottom: 10px;
    display: block;
  }

  .project-name {
    font-size: 0.9rem;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 4px;
  }

  .project-desc {
    font-size: 0.76rem;
    color: var(--text-muted);
    line-height: 1.5;
    margin-bottom: 10px;
  }

  .project-tags {
    display: flex;
    gap: 4px;
    flex-wrap: wrap;
  }

  .tag {
    font-family: 'Fira Code', monospace;
    font-size: 0.65rem;
    padding: 2px 7px;
    border-radius: 999px;
    background: rgba(168,85,247,0.1);
    color: #A855F7;
    border: 0.5px solid rgba(168,85,247,0.25);
  }

  .tag.cyan {
    background: rgba(34,211,238,0.08);
    color: #22D3EE;
    border-color: rgba(34,211,238,0.2);
  }

  /* ── STATS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 10px;
    margin-bottom: 1.5rem;
  }

  .stat-card {
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 12px;
    padding: 1rem;
    text-align: center;
  }

  .stat-num {
    font-size: 1.6rem;
    font-weight: 700;
    background: linear-gradient(135deg, #A855F7, #22D3EE);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    display: block;
    line-height: 1.2;
  }

  .stat-label {
    font-size: 0.72rem;
    color: var(--text-muted);
    margin-top: 4px;
    letter-spacing: 0.06em;
  }

  /* ── FOOTER ── */
  .readme-footer {
    text-align: center;
    padding: 1.5rem;
    background: var(--surface-1);
    border: 0.5px solid var(--border);
    border-radius: 12px;
    margin-top: 0.5rem;
  }

  .footer-quote {
    font-family: 'Fira Code', monospace;
    font-size: 0.8rem;
    color: var(--text-muted);
    margin-bottom: 1rem;
  }

  .footer-quote span { color: #A855F7; }

  .copy-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 8px 18px;
    border-radius: 999px;
    font-size: 0.8rem;
    font-weight: 500;
    background: linear-gradient(135deg, rgba(168,85,247,0.15), rgba(34,211,238,0.1));
    border: 0.5px solid rgba(168,85,247,0.35);
    color: #A855F7;
    cursor: pointer;
    transition: all 0.2s;
  }

  .copy-btn:hover { opacity: 0.8; }

  .btn-row { display: flex; gap: 8px; justify-content: center; flex-wrap: wrap; }
</style>

<div class="readme-root">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-bg"></div>
    <div class="hero-grid"></div>
    <div class="hero-content">
      <div class="hero-top">
        <div>
          <div class="hero-name">Menna Aliwa</div>
          <div class="hero-role">
            <span class="status-dot"></span>
            Frontend Developer · IT Student @ Delta University
          </div>
        </div>
        <div class="hero-avatar">MA</div>
      </div>

      <div class="hero-links">
        <a class="hero-link accent" href="https://menna-portfolio-ruddy.vercel.app/" target="_blank">
          <i class="ti ti-world" aria-hidden="true"></i> Portfolio
        </a>
        <a class="hero-link" href="https://www.linkedin.com/in/menna-aliwa-a6943625a" target="_blank">
          <i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn
        </a>
        <a class="hero-link" href="https://github.com/mna80455-debug" target="_blank">
          <i class="ti ti-brand-github" aria-hidden="true"></i> GitHub
        </a>
        <a class="hero-link" href="mailto:mna80455@gmail.com">
          <i class="ti ti-mail" aria-hidden="true"></i> mna80455@gmail.com
        </a>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section-divider">
    <div class="section-divider-line"></div>
    <span class="section-label">// about.js</span>
    <div class="section-divider-line"></div>
  </div>

  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-r"></div>
      <div class="dot dot-y"></div>
      <div class="dot dot-g"></div>
      <span class="code-filename">about.js</span>
    </div>
    <div class="code-body">
      <span class="t-purple">const</span> <span class="t-cyan">menna</span> = {<br>
      &nbsp;&nbsp;<span class="t-green">name</span>:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class="t-orange">"Menna Aliwa"</span>,<br>
      &nbsp;&nbsp;<span class="t-green">location</span>:&nbsp;&nbsp; <span class="t-orange">"Egypt 🇪🇬"</span>,<br>
      &nbsp;&nbsp;<span class="t-green">university</span>: <span class="t-orange">"Delta University for Science & Technology"</span>,<br>
      &nbsp;&nbsp;<span class="t-green">faculty</span>:&nbsp;&nbsp; <span class="t-orange">"Industrial Technology & Energy — IT"</span>,<br><br>
      &nbsp;&nbsp;<span class="t-green">stack</span>: [<span class="t-orange">"React"</span>, <span class="t-orange">"TypeScript"</span>, <span class="t-orange">"Vite"</span>, <span class="t-orange">"Firebase"</span>, <span class="t-orange">"Tailwind"</span>],<br>
      &nbsp;&nbsp;<span class="t-green">passions</span>: [<span class="t-orange">"UI/UX"</span>, <span class="t-orange">"System Analysis"</span>, <span class="t-orange">"Design Systems"</span>],<br><br>
      &nbsp;&nbsp;<span class="t-green">building</span>:&nbsp; <span class="t-orange">"Smart QR SaaS · Web Platforms · AI-powered tools"</span>,<br>
      &nbsp;&nbsp;<span class="t-green">contact</span>:&nbsp; <span class="t-orange">"mna80455@gmail.com"</span>,<br><br>
      &nbsp;&nbsp;<span class="t-purple">get</span> <span class="t-cyan">funFact</span>() {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="t-purple">return</span> <span class="t-orange">"I ship real products. Not just to-do apps. 🚀"</span>;<br>
      &nbsp;&nbsp;}<br>
      };
    </div>
  </div>

  <!-- STACK -->
  <div class="section-divider">
    <div class="section-divider-line"></div>
    <span class="section-label">// tech.stack</span>
    <div class="section-divider-line"></div>
  </div>

  <div class="skills-grid">
    <div class="skill-card"><span class="skill-icon">⚛️</span><div class="skill-name">React</div></div>
    <div class="skill-card"><span class="skill-icon">🔷</span><div class="skill-name">TypeScript</div></div>
    <div class="skill-card"><span class="skill-icon">⚡</span><div class="skill-name">Vite</div></div>
    <div class="skill-card"><span class="skill-icon">🔥</span><div class="skill-name">Firebase</div></div>
    <div class="skill-card"><span class="skill-icon">🎨</span><div class="skill-name">Tailwind CSS</div></div>
    <div class="skill-card"><span class="skill-icon">🗄️</span><div class="skill-name">Supabase</div></div>
    <div class="skill-card"><span class="skill-icon">🟨</span><div class="skill-name">JavaScript</div></div>
    <div class="skill-card"><span class="skill-icon">🌐</span><div class="skill-name">Next.js</div></div>
    <div class="skill-card"><span class="skill-icon">🐙</span><div class="skill-name">Git & GitHub</div></div>
    <div class="skill-card"><span class="skill-icon">🗃️</span><div class="skill-name">SQL / Oracle</div></div>
    <div class="skill-card"><span class="skill-icon">🤖</span><div class="skill-name">AI APIs</div></div>
    <div class="skill-card"><span class="skill-icon">🚀</span><div class="skill-name">Vercel</div></div>
  </div>

  <!-- PROJECTS -->
  <div class="section-divider">
    <div class="section-divider-line"></div>
    <span class="section-label">// featured.projects</span>
    <div class="section-divider-line"></div>
  </div>

  <div class="projects-grid">
    <div class="project-card v1" onclick="window.open('https://github.com/mna80455-debug/qrify','_blank')">
      <span class="project-emoji">🔗</span>
      <div class="project-name">QRift</div>
      <div class="project-desc">Smart bilingual QR SaaS — dynamic codes, analytics, custom design & pricing tiers</div>
      <div class="project-tags">
        <span class="tag">React</span>
        <span class="tag">Firebase</span>
        <span class="tag cyan">SaaS</span>
      </div>
    </div>

    <div class="project-card v2" onclick="window.open('https://github.com/mna80455-debug/days','_blank')">
      <span class="project-emoji">🌙</span>
      <div class="project-name">أيام / Days</div>
      <div class="project-desc">Arabic mindful daily companion PWA with time-based themes & Life in Weeks</div>
      <div class="project-tags">
        <span class="tag">PWA</span>
        <span class="tag">Firebase</span>
        <span class="tag cyan">Arabic</span>
      </div>
    </div>

    <div class="project-card v3" onclick="window.open('https://menna-portfolio-ruddy.vercel.app/','_blank')">
      <span class="project-emoji">🧠</span>
      <div class="project-name">GradeIQ</div>
      <div class="project-desc">Academic platform with Groq AI, multi-grading systems & bilingual interface</div>
      <div class="project-tags">
        <span class="tag">Groq AI</span>
        <span class="tag">Firebase</span>
        <span class="tag cyan">Bilingual</span>
      </div>
    </div>

    <div class="project-card v4" onclick="window.open('https://github.com/mna80455-debug/invoice-generator','_blank')">
      <span class="project-emoji">🧾</span>
      <div class="project-name">Invoice Generator</div>
      <div class="project-desc">Professional invoice builder with PDF export and clean minimal UI</div>
      <div class="project-tags">
        <span class="tag">React</span>
        <span class="tag">Vite</span>
        <span class="tag cyan">PDF</span>
      </div>
    </div>

    <div class="project-card v5" onclick="window.open('https://menna-portfolio-ruddy.vercel.app/','_blank')">
      <span class="project-emoji">🏛️</span>
      <div class="project-name">Wasl · وصل</div>
      <div class="project-desc">Arabic university employment platform — smart job matching & full academic docs</div>
      <div class="project-tags">
        <span class="tag">Next.js</span>
        <span class="tag">Supabase</span>
        <span class="tag cyan">Arabic</span>
      </div>
    </div>

    <div class="project-card v1" onclick="window.open('https://menna-portfolio-ruddy.vercel.app/','_blank')">
      <span class="project-emoji">🚌</span>
      <div class="project-name">UniRoute</div>
      <div class="project-desc">Smart university transport system — GPS, seat reservations & digital payments</div>
      <div class="project-tags">
        <span class="tag">Next.js</span>
        <span class="tag">Oracle SQL</span>
        <span class="tag cyan">System</span>
      </div>
    </div>
  </div>

  <!-- STATS -->
  <div class="section-divider">
    <div class="section-divider-line"></div>
    <span class="section-label">// github.stats</span>
    <div class="section-divider-line"></div>
  </div>

  <div class="stats-row">
    <div class="stat-card">
      <span class="stat-num">10+</span>
      <div class="stat-label">Projects shipped</div>
    </div>
    <div class="stat-card">
      <span class="stat-num">6+</span>
      <div class="stat-label">Live on Vercel</div>
    </div>
    <div class="stat-card">
      <span class="stat-num">5+</span>
      <div class="stat-label">Tech stacks used</div>
    </div>
    <div class="stat-card">
      <span class="stat-num">2yr</span>
      <div class="stat-label">Building & learning</div>
    </div>
  </div>

  <!-- GITHUB IMAGES -->
  <div style="display:grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 1.5rem;">
    <img src="https://github-readme-stats.vercel.app/api?username=mna80455-debug&show_icons=true&theme=tokyonight&border_radius=12&hide_border=true&bg_color=0D1117&title_color=A855F7&icon_color=22D3EE&count_private=true" style="width:100%; border-radius:12px;" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mna80455-debug&layout=compact&theme=tokyonight&border_radius=12&hide_border=true&bg_color=0D1117&title_color=A855F7" style="width:100%; border-radius:12px;" />
  </div>
  <div style="margin-bottom: 1.5rem;">
    <img src="https://streak-stats.demolab.com?user=mna80455-debug&theme=tokyonight&hide_border=true&border_radius=12&background=0D1117&ring=A855F7&fire=22D3EE&currStreakLabel=A855F7" style="width:100%; border-radius:12px;" />
  </div>

  <!-- FOOTER -->
  <div class="readme-footer">
    <div class="footer-quote">
      <span>// </span>currently building things that matter &nbsp;·&nbsp; one commit at a time 🔮
    </div>
    <div class="btn-row">
      <button class="copy-btn" onclick="sendPrompt('ابعتيلي الكود الكامل لهذا الـ README بصيغة Markdown جاهزة للنسخ على GitHub')">
        <i class="ti ti-brand-github" aria-hidden="true"></i>
        اعطيني كود الـ README كامل ↗
      </button>
      <button class="copy-btn" onclick="sendPrompt('عايزة تعديل على الـ README: ')">
        <i class="ti ti-edit" aria-hidden="true"></i>
        تعديل ↗
      </button>
    </div>
  </div>

</div>

