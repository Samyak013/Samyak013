

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- HERO SECTION — Animated banner with name, subtitle, floating orbs -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=320
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.08)'
}}>

  <style>{`
    @keyframes hero-orb-a { 0%, 100% { transform: translate(0,0); opacity: 0.55; } 50% { transform: translate(40px,-30px); opacity: 0.85; } }
    @keyframes hero-orb-b { 0%, 100% { transform: translate(0,0); opacity: 0.45; } 50% { transform: translate(-35px,25px); opacity: 0.75; } }
    @keyframes hero-orb-c { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-40px); opacity: 0.65; } }
    @keyframes hero-orb-d { 0%, 100% { transform: translate(0,0); opacity: 0.40; } 50% { transform: translate(-20px,-15px); opacity: 0.70; } }
    @keyframes hero-ring { 0%, 100% { opacity: 0.04; } 50% { opacity: 0.14; } }
    @keyframes hero-ring-b { 0%, 100% { opacity: 0.03; } 50% { opacity: 0.10; } }
    @keyframes hero-dot-spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    @keyframes hero-line-scan { 0% { transform: translateY(-320px); } 100% { transform: translateY(320px); } }
    @keyframes hero-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    #ho1 { animation: hero-orb-a 9s ease-in-out infinite; }
    #ho2 { animation: hero-orb-b 12s ease-in-out infinite 0.6s; }
    #ho3 { animation: hero-orb-c 8s ease-in-out infinite 1.5s; }
    #ho4 { animation: hero-orb-d 11s ease-in-out infinite 0.3s; }
    #ho5 { animation: hero-orb-a 10s ease-in-out infinite 2s; }
    #ho6 { animation: hero-orb-b 14s ease-in-out infinite 1s; }
    #hr1 { animation: hero-ring 9s ease-in-out infinite; }
    #hr2 { animation: hero-ring 9s ease-in-out infinite 1.5s; }
    #hr3 { animation: hero-ring-b 9s ease-in-out infinite 3s; }
    #hr4 { animation: hero-ring-b 10s ease-in-out infinite 4.5s; }
    #hdot { animation: hero-dot-spin 24s linear infinite; }
    #hscan { animation: hero-line-scan 6s linear infinite; }
    #hcur { animation: hero-cursor 1.1s step-end infinite; }
  `}</style>

  <svg width="860" height="320" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.50)" />
        <stop offset="60%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.55)" />
        <stop offset="55%" stopColor="rgba(139,92,246,0.15)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.45)" />
        <stop offset="60%" stopColor="rgba(51,102,255,0.10)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.30)" />
        <stop offset="70%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,180,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,180,255,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168,85,247,0.40)" />
        <stop offset="100%" stopColor="rgba(168,85,247,0)" />
      </radialGradient>
      <linearGradient id="hscan-g" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(0,229,255,0)" />
        <stop offset="45%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="50%" stopColor="rgba(0,229,255,0.12)" />
        <stop offset="55%" stopColor="rgba(0,229,255,0.04)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </linearGradient>
    </defs>

    <ellipse id="ho1" cx="120" cy="280" rx="280" ry="200" fill="url(#hg1)" />
    <ellipse id="ho2" cx="740" cy="60"  rx="250" ry="190" fill="url(#hg2)" />
    <ellipse id="ho3" cx="430" cy="310" rx="200" ry="160" fill="url(#hg3)" />
    <ellipse id="ho4" cx="680" cy="290" rx="180" ry="140" fill="url(#hg4)" />
    <ellipse id="ho5" cx="250" cy="40"  rx="220" ry="160" fill="url(#hg5)" />
    <ellipse id="ho6" cx="500" cy="60"  rx="160" ry="130" fill="url(#hg6)" />

    <circle id="hr1" cx="430" cy="160" r="55"  fill="none" stroke="rgba(0,229,255,0.7)" strokeWidth="0.5" />
    <circle id="hr2" cx="430" cy="160" r="100" fill="none" stroke="rgba(139,92,246,0.6)" strokeWidth="0.5" />
    <circle id="hr3" cx="430" cy="160" r="155" fill="none" stroke="rgba(51,102,255,0.5)" strokeWidth="0.4" />
    <circle id="hr4" cx="430" cy="160" r="220" fill="none" stroke="rgba(0,229,255,0.3)" strokeWidth="0.3" />

    <g id="hdot">
      <circle cx="430" cy="105" r="2" fill="rgba(0,229,255,0.6)" />
    </g>

    <rect id="hscan" x="0" y="0" width="860" height="320" fill="url(#hscan-g)" />
  </svg>

  <div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{
      fontSize: 11, letterSpacing: 6, textTransform: 'uppercase',
      color: 'rgba(0,229,255,0.50)', fontWeight: 300, marginBottom: 14
    }}>AI & ML ENGINEER | DATA SCIENTIST</span>

    <span style={{
      fontSize: 52, fontWeight: 800, letterSpacing: -2, lineHeight: 1,
      color: '#ffffff',
      textShadow: '0 0 60px rgba(0,229,255,0.25), 0 0 120px rgba(139,92,246,0.15)'
    }}>Samyak Bagesar</span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 16, gap: 6 }}>
      <span style={{
        fontSize: 15, color: 'rgba(180,190,255,0.70)', fontWeight: 400,
        letterSpacing: 0.5, fontFamily: 'monospace'
      }}>> Business analytics · Power BI · Python · SQL</span>
      <span id="hcur" style={{ fontSize: 15, color: 'rgba(0,229,255,0.7)', fontFamily: 'monospace' }}>_</span>
    </div>

    <div style={{ display: 'flex', gap: 8, marginTop: 24, flexWrap: 'wrap', justifyContent: 'center' }}>
      {['Power BI & Business Intelligence', 'SQL & Data Analytics', 'Python & EDA', 'AI/ML & HPC'].map(function(tag, i) {
        return (
          <span key={i} style={{
            padding: '5px 14px', borderRadius: 100,
            background: 'rgba(0,229,255,0.04)',
            border: '1px solid rgba(0,229,255,0.12)',
            color: 'rgba(0,229,255,0.65)', fontSize: 11, fontWeight: 500, letterSpacing: 0.8
          }}>{tag}</span>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- TECH STACK SECTION — Animated glowing technology cards         -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=380
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes ts-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(30px,-20px); opacity: 0.7; } }
    @keyframes ts-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(-25px,15px); opacity: 0.6; } }
    @keyframes ts-pulse { 0%, 100% { opacity: 0.7; } 50% { opacity: 1; } }
    #tso1 { animation: ts-orb1 10s ease-in-out infinite; }
    #tso2 { animation: ts-orb2 13s ease-in-out infinite 1s; }
    #tso3 { animation: ts-orb1 9s ease-in-out infinite 2s; }
    #tsp1 { animation: ts-pulse 3s ease-in-out infinite; }
    #tsp2 { animation: ts-pulse 3s ease-in-out infinite 0.5s; }
    #tsp3 { animation: ts-pulse 3s ease-in-out infinite 1s; }
    #tsp4 { animation: ts-pulse 3s ease-in-out infinite 1.5s; }
    #tsp5 { animation: ts-pulse 3s ease-in-out infinite 2s; }
    #tsp6 { animation: ts-pulse 3s ease-in-out infinite 0.3s; }
    #tsp7 { animation: ts-pulse 3s ease-in-out infinite 0.8s; }
    #tsp8 { animation: ts-pulse 3s ease-in-out infinite 1.3s; }
    #tsp9 { animation: ts-pulse 3s ease-in-out infinite 1.8s; }
    #tsp10 { animation: ts-pulse 3s ease-in-out infinite 0.2s; }
    #tsp11 { animation: ts-pulse 3s ease-in-out infinite 0.7s; }
    #tsp12 { animation: ts-pulse 3s ease-in-out infinite 1.2s; }
    #tsp13 { animation: ts-pulse 3s ease-in-out infinite 1.7s; }
    #tsp14 { animation: ts-pulse 3s ease-in-out infinite 2.2s; }
    #tsp15 { animation: ts-pulse 3s ease-in-out infinite 0.4s; }
  `}</style>

  <svg width="860" height="380" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <radialGradient id="tsg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.35)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="tsg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.30)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="tsg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(51,102,255,0.30)" />
        <stop offset="100%" stopColor="rgba(51,102,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="tso1" cx="150" cy="300" rx="200" ry="190" fill="url(#tsg1)" />
    <ellipse id="tso2" cx="700" cy="70"  rx="180" ry="160" fill="url(#tsg2)" />
    <ellipse id="tso3" cx="430" cy="320" rx="160" ry="140" fill="url(#tsg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>tech stack</span>

  <div style={{ display: 'flex', flexWrap: 'wrap', gap: 12, justifyContent: 'center', zIndex: 10, maxWidth: 760, padding: '0 20px' }}>
    {[
      { name: 'Python', color: '55,118,171' },
      { name: 'JavaScript', color: '247,223,30' },
      { name: 'TypeScript', color: '0,122,204' },
      { name: 'Java', color: '230,81,0' },
      { name: 'SQL', color: '0,150,136' },
      { name: 'PHP', color: '119,123,180' },
      { name: 'C / C++', color: '74,144,226' },
      { name: 'Linux', color: '245,200,66' },
      { name: 'Networking', color: '98,230,181' },
      { name: 'HPC & Parallel', color: '255,184,107' },
      { name: 'React', color: '97,218,251' },
      { name: 'Tailwind CSS', color: '56,189,248' },
      { name: 'Node.js', color: '104,159,56' },
      { name: 'Express.js', color: '180,190,180' },
      { name: 'REST APIs', color: '255,127,80' },
      { name: 'PostgreSQL', color: '51,103,145' },
      { name: 'MySQL', color: '0,117,143' },
      { name: 'Gemini API', color: '66,133,244' },
      { name: 'GPT-4', color: '116,192,160' },
      { name: 'Scikit-learn', color: '245,140,45' },
      { name: 'Pandas / NumPy', color: '79,134,198' },
      { name: 'Power BI', color: '242,200,0' },
      { name: 'Matplotlib', color: '115,85,124' },
      { name: 'Git', color: '240,80,50' },
    ].map(function(tech, i) {
      return (
        <div key={i} id={'tsp' + (i + 1)} style={{
          display: 'flex', alignItems: 'center', gap: 8,
          padding: '10px 20px', borderRadius: 12,
          background: 'rgba(' + tech.color + ',0.06)',
          border: '1px solid rgba(' + tech.color + ',0.18)',
        }}>
          <div style={{
            width: 8, height: 8, borderRadius: 4,
            background: 'rgba(' + tech.color + ',0.8)',
            boxShadow: '0 0 8px rgba(' + tech.color + ',0.5)'
          }} />
          <span style={{
            fontSize: 13, fontWeight: 500,
            color: 'rgba(255,255,255,0.75)', letterSpacing: 0.3
          }}>{tech.name}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- ABOUT ME SECTION — Terminal-style glassmorphism panel          -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=280
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(51,102,255,0.08)'
}}>

  <style>{`
    @keyframes ab-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.5; } 50% { transform: translate(25px,-18px); opacity: 0.8; } }
    @keyframes ab-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.4; } 50% { transform: translate(-20px,14px); opacity: 0.65; } }
    @keyframes ab-cursor { 0%, 100% { opacity: 1; } 49% { opacity: 1; } 50% { opacity: 0; } 99% { opacity: 0; } }
    @keyframes ab-line-glow { 0%, 100% { opacity: 0.15; } 50% { opacity: 0.35; } }
    #abo1 { animation: ab-orb1 9s ease-in-out infinite; }
    #abo2 { animation: ab-orb2 11s ease-in-out infinite 1.5s; }
    #abcur { animation: ab-cursor 1.1s step-end infinite; }
    #abline { animation: ab-line-glow 4s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="280" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <radialGradient id="abg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.35)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="abg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
    </defs>
    <ellipse id="abo1" cx="80"  cy="230" rx="200" ry="170" fill="url(#abg1)" />
    <ellipse id="abo2" cx="780" cy="70"  rx="180" ry="150" fill="url(#abg2)" />
    <line id="abline" x1="44" y1="70" x2="44" y2="235" stroke="rgba(0,229,255,0.25)" strokeWidth="1" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    justifyContent: 'center', padding: '0 56px', zIndex: 10, gap: 10, flex: 1
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(51,102,255,0.50)', fontWeight: 300, marginBottom: 6
    }}>about</span>

    <span style={{ fontSize: 22, fontWeight: 700, color: '#ffffff', lineHeight: 1.3 }}>
      AI & Data Science engineer building production-grade analytics and AI-integrated products
    </span>

    <span style={{
      fontSize: 14, color: 'rgba(255,255,255,0.50)', lineHeight: 1.7,
      maxWidth: 680
    }}>
      Final-year B.E. Artificial Intelligence & Data Science graduate with 2 peer-reviewed publications and hands-on experience in SQL, Python, Pandas, NumPy, Scikit-learn, and exploratory data analysis. Proficient in Python, JavaScript, TypeScript, React, Node.js, PostgreSQL, and AI/ML integration with Gemini API and GPT-4.

      Built 5 live platforms serving 300+ users, with practical exposure to Linux, networking, cloud deployment, and HPC through C-DAC's Advanced Computing Career programme. Seeking Full-Stack, AI Engineering, and Data Analytics roles.
    </span>

    <div style={{ display: 'flex', alignItems: 'center', marginTop: 8 }}>
      <span style={{ fontSize: 13, color: 'rgba(0,229,255,0.45)', fontFamily: 'monospace' }}>
        {'>'} full-stack engineering · business intelligence · applied AI/ML · HPC
      </span>
      <span id="abcur" style={{ fontSize: 13, color: 'rgba(0,229,255,0.6)', fontFamily: 'monospace', marginLeft: 1 }}>_</span>
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FEATURED PROJECTS — Rich project cards with animated glow borders -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=490
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', flexDirection: 'column', alignItems: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(0,229,255,0.06)', padding: '28px 0'
}}>

  <style>{`
    @keyframes pj-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(35px,-25px); opacity: 0.55; } }
    @keyframes pj-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.25; } 50% { transform: translate(-30px,20px); opacity: 0.5; } }
    @keyframes pj-orb3 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(20px,15px); opacity: 0.5; } }
    @keyframes pj-status { 0%, 100% { opacity: 0.5; } 50% { opacity: 1; } }
    #pjo1 { animation: pj-orb1 10s ease-in-out infinite; }
    #pjo2 { animation: pj-orb2 13s ease-in-out infinite 1s; }
    #pjo3 { animation: pj-orb3 11s ease-in-out infinite 2s; }
    #pjs1 { animation: pj-status 2s ease-in-out infinite; }
    #pjs2 { animation: pj-status 2s ease-in-out infinite 0.4s; }
    #pjs3 { animation: pj-status 2s ease-in-out infinite 0.8s; }
    #pjs4 { animation: pj-status 2s ease-in-out infinite 1.2s; }
    #pjs5 { animation: pj-status 2s ease-in-out infinite 1.6s; }
  `}</style>

  <svg width="860" height="490" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <radialGradient id="pjg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.20)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
      <radialGradient id="pjg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.22)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="pjg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,72,153,0.18)" />
        <stop offset="100%" stopColor="rgba(236,72,153,0)" />
      </radialGradient>
    </defs>
    <ellipse id="pjo1" cx="100" cy="400" rx="220" ry="180" fill="url(#pjg1)" />
    <ellipse id="pjo2" cx="760" cy="100" rx="200" ry="160" fill="url(#pjg2)" />
    <ellipse id="pjo3" cx="430" cy="450" rx="180" ry="140" fill="url(#pjg3)" />
  </svg>

  <span style={{
    fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
    color: 'rgba(0,229,255,0.45)', fontWeight: 300, marginBottom: 20, zIndex: 10
  }}>featured projects</span>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 10, zIndex: 10, width: '100%', padding: '0 28px' }}>
    {[
      {
        title: 'QSR Food Delivery Business Performance Analytics',
        desc: 'Business-focused food-delivery analytics covering revenue, AOV, order growth, cancellations, discounts, and restaurant performance',
        tech: 'Power BI · SQL · Excel',
        color: '0,229,255',
        statusId: 'pjs1'
      },
      {
        title: 'Swiggy Sales & Order Intelligence',
        desc: 'SQL-driven analysis of city, restaurant, category, revenue, AOV, and growth performance with interactive dashboards',
        tech: 'SQL · Power BI · Excel',
        color: '139,92,246',
        statusId: 'pjs2'
      },
      {
        title: 'TechFarm Nexus — Agricultural AI Platform',
        desc: 'EDA on crop, weather, and mandi-price data supporting a rule-based ML crop-recommendation engine; research published at ICATM 2024',
        tech: 'PHP · MySQL · Pandas · NumPy · OpenWeatherMap API',
        color: '51,102,255',
        statusId: 'pjs3'
      },
      {
        title: 'Swasthya Sathi AI — Healthcare Platform',
        desc: 'Multi-role healthcare platform with ABHA record linking, prescription/inventory reporting, and a Gemini-powered multilingual chatbot',
        tech: 'React · TypeScript · Node.js · PostgreSQL · Gemini API',
        color: '236,72,153',
        statusId: 'pjs4'
      },
      {
        title: 'Python Data Analytics & Dashboarding',
        desc: 'Built Python/Tkinter applications and operational analytics dashboards during a remote Python Developer internship, integrating REST APIs',
        tech: 'Python · Pandas · Tkinter · REST APIs',
        color: '168,85,247',
        statusId: 'pjs5'
      }
    ].map(function(project, i) {
      return (
        <div key={i} style={{
          display: 'flex', alignItems: 'center', padding: '14px 20px',
          background: 'rgba(255,255,255,0.02)',
          border: '1px solid rgba(' + project.color + ',0.12)',
          borderRadius: 12, gap: 14
        }}>
          <div id={project.statusId} style={{
            width: 8, height: 8, borderRadius: 4, flexShrink: 0,
            background: 'rgba(' + project.color + ',0.8)',
            boxShadow: '0 0 10px rgba(' + project.color + ',0.4)'
          }} />
          <div style={{ display: 'flex', flexDirection: 'column', gap: 3, flex: 1 }}>
            <span style={{ fontSize: 14, fontWeight: 600, color: '#ffffff', letterSpacing: 0.2 }}>
              {project.title}
            </span>
            <span style={{ fontSize: 11, color: 'rgba(255,255,255,0.40)', lineHeight: 1.4 }}>
              {project.desc}
            </span>
          </div>
          <span style={{
            fontSize: 10, color: 'rgba(' + project.color + ',0.55)',
            fontFamily: 'monospace', letterSpacing: 0.3, textAlign: 'right',
            flexShrink: 0, maxWidth: 200
          }}>{project.tech}</span>
        </div>
      );
    })}
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- GITHUB STATS — Cohesive themed statistics                      -->
<!-- ═══════════════════════════════════════════════════════════════ -->

<p align="center">

![](https://github-readme-stats.vercel.app/api?username=Samyak013&show_icons=true&theme=transparent&hide_border=true&title_color=62e6b5&text_color=b7c9c2&icon_color=ffb86b&bg_color=00000000)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Samyak013&layout=compact&theme=transparent&hide_border=true&title_color=62e6b5&text_color=b7c9c2&bg_color=00000000)

</p>

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CURRENT FOCUS — What I'm building and exploring                -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=220
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden',
  borderRadius: 20, border: '1px solid rgba(139,92,246,0.08)'
}}>

  <style>{`
    @keyframes cf-orb1 { 0%, 100% { transform: translate(0,0); opacity: 0.35; } 50% { transform: translate(25px,-18px); opacity: 0.6; } }
    @keyframes cf-orb2 { 0%, 100% { transform: translate(0,0); opacity: 0.3; } 50% { transform: translate(-20px,14px); opacity: 0.55; } }
    @keyframes cf-dot { 0%, 100% { opacity: 0.4; } 50% { opacity: 1; } }
    #cfo1 { animation: cf-orb1 10s ease-in-out infinite; }
    #cfo2 { animation: cf-orb2 12s ease-in-out infinite 1s; }
    #cfd1 { animation: cf-dot 2.5s ease-in-out infinite; }
    #cfd2 { animation: cf-dot 2.5s ease-in-out infinite 0.4s; }
    #cfd3 { animation: cf-dot 2.5s ease-in-out infinite 0.8s; }
    #cfd4 { animation: cf-dot 2.5s ease-in-out infinite 1.2s; }
    #cfd5 { animation: cf-dot 2.5s ease-in-out infinite 1.6s; }
    #cfd6 { animation: cf-dot 2.5s ease-in-out infinite 2.0s; }
  `}</style>

  <svg width="860" height="220" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <radialGradient id="cfg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.30)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
      <radialGradient id="cfg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(0,229,255,0.25)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="cfo1" cx="120" cy="190" rx="200" ry="150" fill="url(#cfg1)" />
    <ellipse id="cfo2" cx="740" cy="50"  rx="180" ry="140" fill="url(#cfg2)" />
  </svg>

  <div style={{
    position: 'relative', display: 'flex', flexDirection: 'column',
    padding: '24px 40px', zIndex: 10, flex: 1, justifyContent: 'center'
  }}>
    <span style={{
      fontSize: 11, letterSpacing: 5, textTransform: 'uppercase',
      color: 'rgba(139,92,246,0.50)', fontWeight: 300, marginBottom: 16
    }}>currently exploring</span>

    <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
      {[
        { label: 'Business Intelligence & Power BI', color: '0,229,255', id: 'cfd1' },
        { label: 'SQL Analytics & Data Modeling', color: '139,92,246', id: 'cfd2' },
        { label: 'Python EDA & Data Science', color: '51,102,255', id: 'cfd3' },
        { label: 'AI/ML Applications', color: '236,72,153', id: 'cfd4' },
        { label: 'High Performance Computing', color: '168,85,247', id: 'cfd5' },
        { label: 'Operational Dashboards', color: '0,180,255', id: 'cfd6' },
      ].map(function(item, i) {
        return (
          <div key={i} style={{
            display: 'flex', alignItems: 'center', gap: 8,
            padding: '8px 16px', borderRadius: 10,
            background: 'rgba(' + item.color + ',0.04)',
            border: '1px solid rgba(' + item.color + ',0.12)'
          }}>
            <div id={item.id} style={{
              width: 6, height: 6, borderRadius: 3,
              background: 'rgba(' + item.color + ',0.9)',
              boxShadow: '0 0 8px rgba(' + item.color + ',0.5)'
            }} />
            <span style={{
              fontSize: 12, color: 'rgba(255,255,255,0.60)',
              fontWeight: 500, letterSpacing: 0.3
            }}>{item.label}</span>
          </div>
        );
      })}
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- CAREER SIGNAL — Experience, education, achievements, and proof -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=860 height=560
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', flexDirection: 'column', fontFamily: 'Inter, sans-serif',
  position: 'relative', overflow: 'hidden', borderRadius: 20,
  border: '1px solid rgba(98,230,181,0.18)', padding: '28px 0'
}}>

  <style>{`
    @keyframes cs-pulse { 0%, 100% { opacity: 0.45; } 50% { opacity: 1; } }
    @keyframes cs-drift { 0%, 100% { transform: translate(0,0); opacity: 0.28; } 50% { transform: translate(30px,-20px); opacity: 0.55; } }
    #csp1 { animation: cs-pulse 2.8s ease-in-out infinite; }
    #csp2 { animation: cs-pulse 2.8s ease-in-out infinite 0.6s; }
    #csp3 { animation: cs-pulse 2.8s ease-in-out infinite 1.2s; }
    #csp4 { animation: cs-pulse 2.8s ease-in-out infinite 1.8s; }
    #csg1 { animation: cs-drift 12s ease-in-out infinite; }
    #csg2 { animation: cs-drift 15s ease-in-out infinite 1s; }
  `}</style>

  <svg width="860" height="560" style={{ position: 'absolute', top: 0, left: 0, filter: 'saturate(1.2) brightness(1.08)' }}>
    <defs>
      <radialGradient id="csgg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(98,230,181,0.28)" />
        <stop offset="100%" stopColor="rgba(98,230,181,0)" />
      </radialGradient>
      <radialGradient id="csgg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(255,184,107,0.26)" />
        <stop offset="100%" stopColor="rgba(255,184,107,0)" />
      </radialGradient>
    </defs>
    <ellipse id="csg1" cx="80" cy="500" rx="250" ry="190" fill="url(#csgg1)" />
    <ellipse id="csg2" cx="800" cy="80" rx="220" ry="170" fill="url(#csgg2)" />
  </svg>

  <div style={{ position: 'relative', zIndex: 10, padding: '0 34px', display: 'flex', flexDirection: 'column', gap: 12 }}>
    <span style={{ fontSize: 11, letterSpacing: 5, textTransform: 'uppercase', color: 'rgba(98,230,181,0.85)', fontWeight: 600 }}>career signal</span>
    <span style={{ fontSize: 22, fontWeight: 750, color: '#ffffff', letterSpacing: 0.2 }}>Experience, education & proof of work</span>
    <span style={{ fontSize: 12, color: 'rgba(220,240,234,0.62)', lineHeight: 1.5 }}>A practical track record across business analytics, Python automation, AI/ML, and high-performance computing.</span>
  </div>

  <div style={{ position: 'relative', zIndex: 10, display: 'flex', flexDirection: 'column', gap: 9, padding: '16px 34px 0' }}>
    {[
      { title: 'C-DAC Mumbai (Juhu)', role: 'HPC ACC Course with Work-Based Learning', meta: 'Jul 2026 – Present', detail: 'Linux & OS · Networks & Interconnects · Python & C++ · C & Data Structures', color: '98,230,181', id: 'csp1' },
      { title: 'Pythonic Labs', role: 'Python Developer Intern', meta: 'Mar 2025 – Apr 2025 · Remote', detail: '3–5 GUI applications · 5 dashboards · 4 REST APIs · 40% less data entry · 60% faster reporting', color: '255,184,107', id: 'csp2' },
      { title: 'University of Mumbai', role: 'B.E. Artificial Intelligence & Data Science', meta: 'Nov 2022 – May 2026 · 7.75 / 10 CGPA', detail: 'Applied analytics, data science, AI/ML, and research-led problem solving', color: '78,168,222', id: 'csp3' }
    ].map(function(item, i) {
      return (
        <div key={i} style={{ display: 'flex', alignItems: 'center', gap: 14, padding: '12px 16px', background: 'rgba(255,255,255,0.045)', border: '1px solid rgba(' + item.color + ',0.24)', borderRadius: 12 }}>
          <div id={item.id} style={{ width: 8, height: 8, borderRadius: 4, flexShrink: 0, background: 'rgba(' + item.color + ',0.95)', boxShadow: '0 0 12px rgba(' + item.color + ',0.7)' }} />
          <div style={{ display: 'flex', flexDirection: 'column', gap: 3, flex: 1 }}>
            <span style={{ fontSize: 13, fontWeight: 700, color: '#ffffff' }}>{item.title} <span style={{ color: 'rgba(220,240,234,0.62)', fontWeight: 500 }}>· {item.role}</span></span>
            <span style={{ fontSize: 10, color: 'rgba(' + item.color + ',0.9)', fontFamily: 'monospace' }}>{item.meta}</span>
            <span style={{ fontSize: 10, color: 'rgba(220,240,234,0.58)', lineHeight: 1.35 }}>{item.detail}</span>
          </div>
        </div>
      );
    })}
  </div>

  <div style={{ position: 'relative', zIndex: 10, display: 'flex', gap: 10, padding: '14px 34px 0' }}>
    <div style={{ flex: 1, padding: '12px 14px', background: 'rgba(98,230,181,0.07)', border: '1px solid rgba(98,230,181,0.2)', borderRadius: 12 }}>
      <span style={{ display: 'block', fontSize: 10, letterSpacing: 2, textTransform: 'uppercase', color: 'rgba(98,230,181,0.85)', marginBottom: 7 }}>achievements</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.68)', lineHeight: 1.45 }}>HackUp 2026 lead organizer · Innovathon 2025 runner-up · ICATM 2024 first author · PaperNova co-author · Aavishkar semi-finalist ×2</span>
    </div>
    <div style={{ flex: 1, padding: '12px 14px', background: 'rgba(255,184,107,0.07)', border: '1px solid rgba(255,184,107,0.2)', borderRadius: 12 }}>
      <span style={{ display: 'block', fontSize: 10, letterSpacing: 2, textTransform: 'uppercase', color: 'rgba(255,184,107,0.9)', marginBottom: 7 }}>certifications</span>
      <span style={{ fontSize: 10, color: 'rgba(255,255,255,0.68)', lineHeight: 1.45 }}>Python Full Stack + DSA · Cursa AI Masterclass · Neo4j Certified Professional · CEH + PRO</span>
    </div>
  </div>
</div>
```

<!-- ═══════════════════════════════════════════════════════════════ -->
<!-- SOCIAL LINKS — Custom SocialMediaButton components             -->
<!-- ═══════════════════════════════════════════════════════════════ -->

```aura width=130 height=44 link="https://github.com/Samyak013" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgPjxwYXRoIGZpbGw9IiNlOGVlZjgiIGQ9Ik0xMiAuNUM1Ljg2LjUuNSA1Ljg2LjUgMTJjMCA1LjI1IDMuNCA5LjcgOC4xMiAxMS4yOC42LjExLjgyLS4yNi44Mi0uNTggMC0uMjgtLjAyLTEuMjMtLjAyLTIuMjMtMy4wMi41Ni0zLjgzLS43NC00LjA4LTEuNC0uMTQtLjM1LS43My0xLjQxLTEuMjUtMS42OS0uNDMtLjIzLTEuMDQtLjgtLjAxLS44MS45Ni0uMDIgMS42NS44OCAxLjg4IDEuMjYgMS4xIDEuODUgMi44NSAxLjMzIDMuNTQgMS4wMS4xMS0uNzkuNDItMS4zNC43Ni0xLjY0LTIuNjYtLjMxLTUuNDUtMS4zMy01LjQ1LTUuOTIgMC0xLjMxLjQ3LTIuMzggMS4yNC0zLjIyLS4xMi0uMzEtLjU0LTEuNTQuMTItMy4yIDAgMCAxLjAxLS4zMiAzLjMgMS4yMy45Ni0uMjcgMS45OS0uNCAzLjAxLS40czIuMDUuMTQgMy4wMi40YzIuMjgtMS41NSAzLjI5LTEuMjMgMy4yOS0xLjIzLjY2IDEuNjYuMjQgMi44OS4xMiAzLjIuNzcuODQgMS4yMyAxLjkxIDEuMjMgMy4yMiAwIDQuNjEtMi44IDUuNjItNS40OCA1LjkyLjQzLjM3LjgxIDEuMS44MSAyLjIyIDAgMS42LS4wMiAyLjg5LS4wMiAzLjI5IDAgLjMyLjIyLjY5LjgzLjU3QTExLjUgMTEuNSAwIDAgMCAyMy41IDEyQzIzLjUgNS44NiAxOC4xNC41IDEyIC41WiIvPjwvc3ZnPg=="
  text="GitHub"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={130}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#00e5ff' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#8b5cf6' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#00e5ff' },
  ]}
  iconSize="18"
/>
```

```aura width=140 height=44 link="https://www.linkedin.com/in/samyak-bagesar/" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgPjxwYXRoIGZpbGw9IiNiOGQ0ZjAiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDUuNDU1djYuMjg2ek01LjMzNyA3LjQzM2EyLjA2MiAyLjA2MiAwIDAgMS0yLjA2My0yLjA2NSAyLjA2NCAyLjA2NCAwIDEgMSA0LjEyNiAwIDIuMDYyIDIuMDYyIDAgMCAxLTIuMDYzIDIuMDY1em0xLjc4MiAxMy4wMTlIMy41NTVWOWgzLjU2NHYxMS40NTJ6TTIyLjIyNSAwSDEuNzcxQy43OTIgMCAwIC43NzQgMCAxLjcyOXYyMC41NDJDMCAyMy4yMjcuNzkyIDI0IDEuNzcxIDI0aDIwLjQ1MUMyMy4yIDI0IDI0IDIzLjIyNyAyNCAyMi4yNzFWMS43MjlDMjQgLjc3NCAyMy4yIDAgMjIuMjIyIDBoLjAwM3oiLz48L3N2Zz4="
  text="LinkedIn"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={140}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#0A66C2' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#00e5ff' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#0A66C2' },
  ]}
  iconSize="18"
/>
```

```aura width=140 height=44 link="https://leetcode.com/u/Samyak1321/" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgPjxwYXRoIGZpbGw9IiNmZmZmZmYiIGQ9Ik0xMy4zIDEuOWExLjYgMS42IDAgMSAwLTIuMiAyLjJsMS40IDEuNGMtNC4yIDEuMS03LjMgNC44LTcuMyA5LjFhOS4xIDkuMSAwIDAgMCAxNy4zIDMuN2gxLjlhMS42IDEuNiAwIDEgMCAwLTMuMmgtMS44YzAtMy4zLTIuMS02LjItNS4xLTcuMWwtMS40LTEuNGMyLjQtMS44IDUuNS0yLjggOC45LTIuOGgxLjZhMS42IDEuNiAwIDEgMCAwLTMuMkgxNyBjLTEuMyAwLTIuNS4xLTMuNy4zTDEzLjMgMS45Wk0xMS44IDYuOGEyIDIgMCAxIDAgMCA0IDIgMiAwIDAgMCAwLTRabTAgNi44YTIgMiAwIDEgMCAwIDQgMiAyIDAgMCAwIDAtNFoiLz48L3N2Zz4="
  text="LeetCode"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={140}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#FFA116' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#8b5cf6' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#FFA116' },
  ]}
  iconSize="18"
/>
```

```aura width=120 height=44 link="mailto:samyakbagesar@gmail.com" inline align=center
<SocialMediaButton
  icon="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgPjxwYXRoIGZpbGw9IiNmZWNhY2EiIGQ9Ik0yIDdoMjBMMTIgMTMuNSAyIDdaIi8+PHBhdGggZmlsbD0iI2ZiNzE4NSIgZD0iTTIgOWwxMCA2IDEwLTZ2OWEyIDIgMCAwIDEtMiAySDRhMiAyIDAgMCAxLTItMlY5WiIvPjwvc3ZnPg=="
  text="Email"
  backgroundColor="#0a0a12"
  textColor="#c0c8e0"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#EA4335' },
    { offset: '20%', color: '#111122' },
    { offset: '50%', color: '#ec4899' },
    { offset: '80%', color: '#111122' },
    { offset: '100%', color: '#EA4335' },
  ]}
  iconSize="18"
/>
```

<p align="center">
  <strong>Kalyan, Maharashtra</strong> · <a href="tel:+918928575445">+91-8928575445</a>
</p>

<!-- ═══════════════════════════════════════════════════════════════════ -->
<!-- FOOTER — Animated scanline + terminal aesthetic                    -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

```aura width=860 height=80
<div style={{
  width: '100%', height: '100%', background: '#071c1b',
  display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center',
  fontFamily: 'Inter, sans-serif', position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(0,229,255,0.05)'
}}>

  <style>{`
    @keyframes ft-scan { 0% { transform: translateY(-80px); } 100% { transform: translateY(80px); } }
    @keyframes ft-pulse { 0%, 100% { opacity: 0.3; } 50% { opacity: 0.7; } }
    @keyframes ft-orb { 0%, 100% { transform: translate(0,0); opacity: 0.25; } 50% { transform: translate(30px,-10px); opacity: 0.45; } }
    #ftscan { animation: ft-scan 4s linear infinite; }
    #ftd1 { animation: ft-pulse 3s ease-in-out infinite; }
    #ftd2 { animation: ft-pulse 3s ease-in-out infinite 1s; }
    #ftd3 { animation: ft-pulse 3s ease-in-out infinite 2s; }
    #ftorb1 { animation: ft-orb 8s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="80" style={{ position: 'absolute', top: 0, left: 0, filter: 'hue-rotate(75deg) saturate(1.18) brightness(1.08)' }}>
    <defs>
      <linearGradient id="fsg" x1="0" y1="0" x2="0" y2="1">
        <stop offset="0%" stopColor="rgba(0,229,255,0)" />
        <stop offset="45%" stopColor="rgba(0,229,255,0.03)" />
        <stop offset="50%" stopColor="rgba(0,229,255,0.08)" />
        <stop offset="55%" stopColor="rgba(0,229,255,0.03)" />
        <stop offset="100%" stopColor="rgba(0,229,255,0)" />
      </linearGradient>
      <radialGradient id="ftg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(139,92,246,0.25)" />
        <stop offset="100%" stopColor="rgba(139,92,246,0)" />
      </radialGradient>
    </defs>

    <line x1="0" y1="1" x2="860" y2="1" stroke="rgba(0,229,255,0.06)" strokeWidth="1" />

    <ellipse id="ftorb1" cx="430" cy="40" rx="300" ry="60" fill="url(#ftg1)" />
    <rect id="ftscan" x="0" y="0" width="860" height="80" fill="url(#fsg)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 6, zIndex: 10 }}>
    <div id="ftd1" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(0,229,255,0.6)' }} />
    <div id="ftd2" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(139,92,246,0.6)' }} />
    <div id="ftd3" style={{ width: 4, height: 4, borderRadius: 2, background: 'rgba(236,72,153,0.6)' }} />
  </div>

  <span style={{
    fontSize: 11, color: 'rgba(255,255,255,0.20)', letterSpacing: 3,
    fontWeight: 300, marginTop: 8, zIndex: 10
  }}>samyak bagesar · analytics · ai/ml · data science</span>
</div>
```
