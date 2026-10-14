<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>SDRRM · Mataasnakahoy Senior High School</title>
<meta name="description" content="School Disaster Risk Reduction and Management organization of Mataasnakahoy Senior High School.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#ffffff; --bg2:#f4f4f4; --card:#ffffff; --fg:#111111; --muted:#6b6b6b; --line:#e2e2e2;
  --accent:#800020; --accent-fg:#ffffff; --accent-soft:#f6e9ec; --shadow:0 10px 30px rgba(0,0,0,.08);
  --serif:'Playfair Display',Georgia,'Times New Roman',serif;
  --sans:'Inter',system-ui,-apple-system,'Segoe UI',Roboto,Arial,sans-serif;
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#0b0b0b; --bg2:#141414; --card:#171717; --fg:#f2f2f2; --muted:#9a9a9a; --line:#2a2a2a;
    --accent:#c0304f; --accent-soft:#2a1017; --shadow:0 10px 30px rgba(0,0,0,.5);
  }
}
:root[data-theme="dark"]{
  --bg:#0b0b0b; --bg2:#141414; --card:#171717; --fg:#f2f2f2; --muted:#9a9a9a; --line:#2a2a2a;
  --accent:#c0304f; --accent-soft:#2a1017; --shadow:0 10px 30px rgba(0,0,0,.5);
}
*,*::before,*::after{box-sizing:inherit}
html{scroll-behavior:smooth;scroll-padding-top:calc(env(safe-area-inset-top,0px) + 72px)}
body{margin:0;background:var(--bg);color:var(--fg);font-family:var(--sans);line-height:1.6;-webkit-font-smoothing:antialiased}
img,svg,canvas{max-width:100%}
a{color:inherit}
h1,h2,h3{font-family:var(--serif);line-height:1.15;margin:0 0 .5em}
p{margin:0 0 1em}
.wrap{width:min(1120px,100% - 40px);margin-inline:auto}
section{padding:96px 0;border-top:1px solid var(--line)}
section.alt{background:var(--bg2)}
.eyebrow{font-size:.75rem;letter-spacing:.2em;text-transform:uppercase;color:var(--accent);font-weight:600;margin-bottom:12px;display:flex;align-items:center;gap:10px}
.eyebrow::before{content:"";width:28px;height:2px;background:var(--accent)}
.sec-title{font-size:clamp(2rem,4vw,3rem)}
.lead{color:var(--muted);max-width:60ch;font-size:1.05rem}
.btn{display:inline-flex;align-items:center;gap:8px;padding:12px 22px;border-radius:2px;border:1px solid var(--fg);background:transparent;color:var(--fg);font:600 .9rem var(--sans);cursor:pointer;text-decoration:none;transition:.2s}
.btn:hover{background:var(--fg);color:var(--bg)}
.btn.primary{background:var(--accent);border-color:var(--accent);color:#fff}
.btn.primary:hover{filter:brightness(1.15);background:var(--accent);color:#fff}
.btn.sm{padding:8px 14px;font-size:.8rem}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
 
/* NAV */
header.nav{position:sticky;top:0;z-index:50;background:color-mix(in srgb,var(--bg) 88%,transparent);backdrop-filter:blur(10px);border-bottom:1px solid var(--line);padding-top:env(safe-area-inset-top,0px)}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;height:64px}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none;font-weight:700;letter-spacing:.08em}
.logo{width:34px;height:34px;background:var(--accent);color:#fff;display:grid;place-items:center;font:800 .8rem var(--serif);border-radius:2px}
.brand small{display:block;font-weight:500;color:var(--muted);letter-spacing:.04em;font-size:.65rem;line-height:1}
.nav ul{display:flex;gap:4px;list-style:none;margin:0;padding:0}
.nav ul a{display:block;padding:8px 12px;font-size:.85rem;text-decoration:none;color:var(--muted);border-bottom:2px solid transparent;transition:.2s}
.nav ul a:hover,.nav ul a.active{color:var(--fg);border-color:var(--accent)}
.nav-tools{display:flex;gap:8px;align-items:center}
.icon-btn{width:38px;height:38px;border:1px solid var(--line);background:transparent;color:var(--fg);cursor:pointer;border-radius:2px;display:grid;place-items:center;font-size:1rem}
.icon-btn:hover{border-color:var(--accent);color:var(--accent)}
#menuBtn{display:none}
@media (max-width:900px){
  #menuBtn{display:grid}
  .nav ul{position:absolute;top:100%;left:0;right:0;background:var(--bg);flex-direction:column;border-bottom:1px solid var(--line);padding:8px 20px 16px;display:none}
  .nav ul.open{display:flex}
  .nav ul a{padding:12px 0}
}
 
/* HERO */
.hero{padding:110px 0 90px;border-top:0;position:relative;overflow:hidden}
.hero::after{content:"";position:absolute;right:-120px;top:-120px;width:460px;height:460px;border-radius:50%;background:var(--accent);opacity:.08}
.hero h1{font-size:clamp(2.6rem,7vw,5.4rem);max-width:14ch;letter-spacing:-.02em}
.hero h1 em{color:var(--accent);font-style:normal}
.hero .lead{margin:20px 0 32px;font-size:1.15rem}
.cta{display:flex;gap:12px;flex-wrap:wrap}
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:0;margin-top:72px;border:1px solid var(--line);background:var(--card)}
.stat{padding:24px;border-right:1px solid var(--line)}
.stat:last-child{border-right:0}
.stat b{display:block;font:700 2.2rem var(--serif);color:var(--accent)}
.stat span{font-size:.8rem;color:var(--muted);text-transform:uppercase;letter-spacing:.1em}
 
/* ABOUT */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:start;margin-top:32px}
.pillars{display:grid;gap:0;border:1px solid var(--line);background:var(--card)}
.pillar{padding:22px 24px;border-bottom:1px solid var(--line);display:flex;gap:18px}
.pillar:last-child{border:0}
.pillar i{font:700 1.4rem var(--serif);color:var(--accent);font-style:normal;min-width:34px}
.pillar h3{font:600 1rem var(--sans);margin:0 0 4px}
.pillar p{margin:0;color:var(--muted);font-size:.92rem}
@media (max-width:800px){.about-grid{grid-template-columns:1fr;gap:32px}}
 
/* PROJECTS */
.filters{display:flex;flex-wrap:wrap;gap:8px;margin:28px 0 32px}
.chip{padding:8px 16px;border:1px solid var(--line);background:transparent;color:var(--muted);font:500 .82rem var(--sans);cursor:pointer;border-radius:100px;transition:.2s}
.chip:hover{border-color:var(--fg);color:var(--fg)}
.chip.on{background:var(--accent);border-color:var(--accent);color:#fff}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(310px,1fr));gap:20px}
.card{background:var(--card);border:1px solid var(--line);padding:28px;display:flex;flex-direction:column;gap:10px;transition:.25s;position:relative;cursor:pointer;text-align:left;font:inherit;color:inherit}
.card:hover{transform:translateY(-4px);box-shadow:var(--shadow);border-color:var(--accent)}
.card .tag{font-size:.7rem;letter-spacing:.14em;text-transform:uppercase;color:var(--accent);font-weight:600}
.card h3{font-size:1.45rem;margin:0}
.card .sub{font-weight:500;font-size:.9rem}
.card p{color:var(--muted);font-size:.92rem;margin:0;flex:1}
.card .more{font-size:.82rem;font-weight:600;margin-top:8px}
.card .num{position:absolute;top:22px;right:24px;font:700 2.2rem var(--serif);color:var(--line)}
.card.hide{display:none}
 
/* MODAL */
dialog{border:1px solid var(--line);background:var(--card);color:var(--fg);padding:0;width:min(640px,calc(100% - 32px));max-height:calc(100% - 48px);overflow:auto;box-shadow:var(--shadow)}
dialog::backdrop{background:rgba(0,0,0,.6)}
.modal-h{padding:32px 32px 20px;border-bottom:1px solid var(--line);border-top:5px solid var(--accent)}
.modal-h h3{font-size:1.9rem;margin:6px 0 4px}
.modal-b{padding:24px 32px 32px}
.modal-b ul{padding-left:18px;color:var(--muted)}
.modal-b li{margin-bottom:6px}
.x{position:absolute;top:14px;right:14px;background:var(--bg);z-index:2}
 
/* MAP */
.map-layout{display:grid;grid-template-columns:2fr 1fr;gap:24px;margin-top:32px}
.map-box{border:1px solid var(--line);background:var(--card);padding:12px;overflow-x:auto}
.map-box svg{width:100%;min-width:560px;height:auto;display:block}
.room{fill:var(--bg2);stroke:var(--fg);stroke-width:1.5;cursor:pointer;transition:.2s}
.room:hover,.room.sel{fill:var(--accent);stroke:var(--accent)}
.room.sel~text,.maplabel{pointer-events:none}
.maplabel{font:600 11px var(--sans);fill:var(--fg);text-anchor:middle}
.group:hover .maplabel,.group.sel .maplabel{fill:#fff}
.route{fill:none;stroke:var(--accent);stroke-width:3;stroke-dasharray:8 7;display:none;animation:dash 1s linear infinite}
.show-routes .route{display:block}
@keyframes dash{to{stroke-dashoffset:-30}}
.panel{border:1px solid var(--line);background:var(--card);padding:24px;align-self:start}
.panel h3{font-size:1.4rem}
.panel .toggle{display:flex;align-items:center;gap:10px;margin:16px 0;font-size:.9rem;cursor:pointer}
.legend{list-style:none;padding:0;margin:16px 0 0;font-size:.82rem;color:var(--muted)}
.legend li{display:flex;gap:8px;align-items:center;margin-bottom:6px}
.legend span{width:14px;height:14px;display:inline-block}
@media (max-width:860px){.map-layout{grid-template-columns:1fr}}
 
/* E-READY */
.ready-grid{display:grid;grid-template-columns:1fr 1fr;gap:48px;margin-top:32px;align-items:center}
.qr-card{background:#fff;color:#000;padding:28px;border:1px solid var(--line);text-align:center;max-width:340px;margin-inline:auto;box-shadow:var(--shadow)}
.qr-card canvas{width:100%;height:auto;image-rendering:pixelated;display:block}
.qr-card b{display:block;margin-top:14px;letter-spacing:.2em;font-size:.75rem}
.qr-card b span{color:#800020}
.field{display:flex;flex-direction:column;gap:6px;margin-bottom:16px}
.field label{font-size:.78rem;font-weight:600;letter-spacing:.08em;text-transform:uppercase;color:var(--muted)}
.field input,.field select,.field textarea{padding:12px 14px;border:1px solid var(--line);background:var(--card);color:var(--fg);font:inherit;border-radius:2px;width:100%}
.field input:focus,.field select:focus,.field textarea:focus{outline:2px solid var(--accent);border-color:var(--accent)}
.err{color:var(--accent);font-size:.8rem;min-height:1em}
.hotlines{list-style:none;padding:0;margin:20px 0 0;border:1px solid var(--line);background:var(--card)}
.hotlines li{padding:12px 16px;border-bottom:1px solid var(--line);display:flex;justify-content:space-between;font-size:.9rem}
.hotlines li:last-child{border:0}
.hotlines b{color:var(--accent)}
@media (max-width:800px){.ready-grid{grid-template-columns:1fr}}
 
/* GO BAG */
.bag-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px;margin-top:32px}
.bag-cat{border:1px solid var(--line);background:var(--card);padding:20px}
.bag-cat h3{font:700 .78rem var(--sans);letter-spacing:.14em;text-transform:uppercase;color:var(--accent);margin-bottom:12px}
.bag-cat label{display:flex;gap:10px;align-items:flex-start;font-size:.9rem;margin-bottom:8px;cursor:pointer}
.bag-cat input{accent-color:var(--accent);margin-top:4px;width:16px;height:16px}
.bag-cat input:checked+span{text-decoration:line-through;color:var(--muted)}
.progress{margin-top:28px;display:flex;align-items:center;gap:16px;flex-wrap:wrap}
.bar{flex:1;min-width:200px;height:8px;background:var(--line);position:relative}
.bar i{position:absolute;inset:0 auto 0 0;width:0;background:var(--accent);transition:width .4s}
#bagText{font-weight:600;font-size:.9rem;min-width:140px}
 
/* VOLCANO */
.volcano-box{margin-top:32px;border:1px solid var(--line);background:#0b0b0b;position:relative}
#volcano{display:block;width:100%;height:auto;aspect-ratio:16/8}
.v-controls{display:flex;flex-wrap:wrap;gap:12px;align-items:center;padding:14px 16px;background:var(--card);border-top:1px solid var(--line)}
.v-controls label{font-size:.82rem;color:var(--muted);display:flex;gap:8px;align-items:center}
.v-controls input[type=range]{accent-color:var(--accent)}
.v-info{position:absolute;left:14px;top:14px;color:#fff;font-size:.8rem;background:rgba(0,0,0,.55);padding:10px 14px;max-width:240px;border-left:3px solid #c0304f}
 
/* SCHEDULE */
.tabs{display:flex;gap:0;border-bottom:1px solid var(--line);margin-top:28px;overflow-x:auto}
.tab{padding:14px 22px;background:none;border:0;border-bottom:3px solid transparent;font:600 .88rem var(--sans);color:var(--muted);cursor:pointer;white-space:nowrap}
.tab.on{color:var(--fg);border-color:var(--accent)}
.tabpane{display:none;padding-top:28px}
.tabpane.on{display:block}
.table-wrap{overflow-x:auto;border:1px solid var(--line);background:var(--card)}
table{width:100%;border-collapse:collapse;font-size:.92rem;min-width:520px}
th,td{padding:14px 18px;text-align:left;border-bottom:1px solid var(--line)}
th{font-size:.72rem;letter-spacing:.12em;text-transform:uppercase;color:var(--muted);background:var(--bg2)}
tr:last-child td{border:0}
td b{color:var(--accent)}
.countdown{display:flex;gap:12px;margin:0 0 24px;flex-wrap:wrap}
.cd{border:1px solid var(--line);background:var(--card);padding:14px 20px;min-width:92px;text-align:center}
.cd b{display:block;font:700 2rem var(--serif);color:var(--accent)}
.cd span{font-size:.7rem;text-transform:uppercase;letter-spacing:.12em;color:var(--muted)}
.steps{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px;margin-top:24px}
.step{border:1px solid var(--line);padding:18px;background:var(--card)}
.step b{display:block;font:700 1.6rem var(--serif);color:var(--accent)}
.note{font-size:.8rem;color:var(--muted);margin-top:14px}
 
/* JOIN */
.join-grid{display:grid;grid-template-columns:1fr 1fr;gap:56px;margin-top:32px}
.success{display:none;border:1px solid var(--accent);background:var(--accent-soft);padding:20px;margin-top:16px}
@media (max-width:800px){.join-grid{grid-template-columns:1fr;gap:32px}}
 
footer{background:#0b0b0b;color:#cfcfcf;padding:56px 0 32px;border-top:4px solid #800020}
footer .wrap{display:grid;grid-template-columns:2fr 1fr 1fr;gap:32px}
footer h4{color:#fff;font-size:.78rem;letter-spacing:.14em;text-transform:uppercase;margin:0 0 12px}
footer a{display:block;color:#a8a8a8;text-decoration:none;font-size:.9rem;padding:3px 0}
footer a:hover{color:#fff}
footer .copy{grid-column:1/-1;border-top:1px solid #2a2a2a;padding-top:20px;font-size:.78rem;color:#7a7a7a}
@media (max-width:700px){footer .wrap{grid-template-columns:1fr}}
 
#toast{position:fixed;left:50%;bottom:calc(24px + env(safe-area-inset-bottom,0px));transform:translate(-50%,30px);background:var(--fg);color:var(--bg);padding:12px 22px;font-size:.88rem;opacity:0;pointer-events:none;transition:.3s;z-index:100}
#toast.show{opacity:1;transform:translate(-50%,0)}
.reveal{opacity:0;transform:translateY(24px);transition:.7s}
.reveal.in{opacity:1;transform:none}
#toTop{position:fixed;right:20px;bottom:calc(20px + env(safe-area-inset-bottom,0px));background:var(--accent);color:#fff;border:0;width:44px;height:44px;cursor:pointer;opacity:0;pointer-events:none;transition:.3s;z-index:40;font-size:1.1rem}
#toTop.show{opacity:1;pointer-events:auto}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important;scroll-behavior:auto!important}.reveal{opacity:1;transform:none}}
</style>
</head>
<body>
 
<header class="nav">
  <div class="wrap">
    <a href="#home" class="brand"><span class="logo">SD</span><span>SDRRM<small>Mataasnakahoy SHS</small></span></a>
    <ul id="navList">
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#escape">Map</a></li>
      <li><a href="#eready">E-Ready</a></li>
      <li><a href="#handa">Go Bag</a></li>
      <li><a href="#volcano-sec">Volcano</a></li>
      <li><a href="#schedule">Schedule</a></li>
      <li><a href="#join">Join</a></li>
    </ul>
    <div class="nav-tools">
      <button class="icon-btn" id="themeBtn" aria-label="Toggle dark mode">◐</button>
      <button class="icon-btn" id="menuBtn" aria-label="Open menu" aria-expanded="false">☰</button>
    </div>
  </div>
</header>
 
<main>
<section class="hero" id="home">
  <div class="wrap">
    <div class="eyebrow">School Disaster Risk Reduction &amp; Management</div>
    <h1>Be ready. Be safe. Be <em>SDRRM.</em></h1>
    <p class="lead">The SDRRM organization of Mataasnakahoy Senior High School builds a culture of preparedness through awareness, training, innovation, and creative advocacy — because every learner deserves to be safe.</p>
    <div class="cta">
      <a href="#projects" class="btn primary">Explore Projects →</a>
      <a href="#schedule" class="btn">View Schedule</a>
    </div>
    <div class="stats">
      <div class="stat"><b data-count="9">0</b><span>Programs</span></div>
      <div class="stat"><b data-count="52">0</b><span>Weekly lectures / yr</span></div>
      <div class="stat"><b data-count="4">0</b><span>Drills per year</span></div>
      <div class="stat"><b data-count="100" data-suffix="%">0</b><span>Commitment</span></div>
    </div>
  </div>
</section>
 
<section id="about" class="alt">
  <div class="wrap">
    <div class="eyebrow">About us</div>
    <h2 class="sec-title">Preparedness is a habit, not an event.</h2>
    <div class="about-grid">
      <div>
        <p class="lead">SDRRM is the student-led arm of the school's disaster risk reduction and management efforts. We turn the four thematic areas of DRRM into everyday action: practical skills, clear plans, creative campaigns, and community care.</p>
        <p class="lead">From go bags to rescue lectures, from spoken poetry to 3D exhibits, our programs make safety something every student can understand, practice, and share.</p>
      </div>
      <div class="pillars">
        <div class="pillar"><i>01</i><div><h3>Prevention &amp; Mitigation</h3><p>Identifying hazards on campus and reducing risks before they become emergencies.</p></div></div>
        <div class="pillar"><i>02</i><div><h3>Preparedness</h3><p>Go bags, evacuation maps, drills, and training so everyone knows what to do.</p></div></div>
        <div class="pillar"><i>03</i><div><h3>Response</h3><p>Basic rescue, first aid, and coordination skills for the critical first minutes.</p></div></div>
        <div class="pillar"><i>04</i><div><h3>Recovery &amp; Rehabilitation</h3><p>Helping our school community bounce back stronger and wiser.</p></div></div>
      </div>
    </div>
  </div>
</section>
 
<section id="projects">
  <div class="wrap">
    <div class="eyebrow">Our programs</div>
    <h2 class="sec-title">Projects &amp; activities</h2>
    <p class="lead">Nine programs, one mission. Filter by focus area and select any card for details.</p>
    <div class="filters" id="filters" role="tablist" aria-label="Filter projects"></div>
    <div class="grid" id="projGrid"></div>
  </div>
</section>
 
<section id="escape" class="alt">
  <div class="wrap">
    <div class="eyebrow">Project ESCAPE</div>
    <h2 class="sec-title">Campus evacuation map</h2>
    <p class="lead">An interactive map of Mataasnakahoy Senior High School. Select a building for details and toggle evacuation routes to the assembly area.</p>
    <div class="map-layout" id="mapLayout">
      <div class="map-box">
        <svg viewBox="0 0 800 520" role="img" aria-label="Schematic map of the school campus">
          <rect x="4" y="4" width="792" height="512" fill="none" stroke="currentColor" stroke-opacity=".25" stroke-dasharray="4 4"/>
          <!-- road -->
          <rect x="0" y="470" width="800" height="50" fill="currentColor" fill-opacity=".08"/>
          <text x="400" y="500" class="maplabel" style="opacity:.5">NATIONAL / BARANGAY ROAD</text>
          <!-- rooms -->
          <g class="group" data-room="admin"><rect class="room" x="40" y="40" width="170" height="90"/><text class="maplabel" x="125" y="90">Admin Building</text></g>
          <g class="group" data-room="bldga"><rect class="room" x="240" y="40" width="200" height="70"/><text class="maplabel" x="340" y="80">Classroom Bldg A</text></g>
          <g class="group" data-room="bldgb"><rect class="room" x="470" y="40" width="200" height="70"/><text class="maplabel" x="570" y="80">Classroom Bldg B</text></g>
          <g class="group" data-room="clinic"><rect class="room" x="700" y="40" width="70" height="70"/><text class="maplabel" x="735" y="80">Clinic</text></g>
          <g class="group" data-room="court"><rect class="room" x="40" y="170" width="220" height="130"/><text class="maplabel" x="150" y="240">Covered Court</text></g>
          <g class="group" data-room="canteen"><rect class="room" x="40" y="330" width="140" height="80"/><text class="maplabel" x="110" y="375">Canteen</text></g>
          <g class="group" data-room="field"><rect class="room" x="320" y="170" width="450" height="240" style="fill:var(--accent-soft)"/><text class="maplabel" x="545" y="285" style="font-size:14px">OPEN FIELD · ASSEMBLY AREA</text></g>
          <g class="group" data-room="gate"><rect class="room" x="340" y="430" width="120" height="30"/><text class="maplabel" x="400" y="450">Main Gate</text></g>
          <!-- routes -->
          <path class="route" d="M125 130 L125 150 L290 150 L290 240 L320 240"/>
          <path class="route" d="M340 110 L340 150 L400 150 L400 170"/>
          <path class="route" d="M570 110 L570 170"/>
          <path class="route" d="M735 110 L735 170"/>
          <path class="route" d="M260 235 L320 235" style="display:none"/>
          <path class="route" d="M110 330 L110 420 L330 420 L330 380 L350 380"/>
          <text x="760" y="505" class="maplabel" style="text-anchor:end;opacity:.5;font-size:9px">N ↑</text>
        </svg>
      </div>
      <aside class="panel">
        <h3 id="roomName">Select a location</h3>
        <p id="roomInfo" style="color:var(--muted)">Click any building on the map to see its role during an emergency.</p>
        <label class="toggle"><input type="checkbox" id="routeToggle" style="accent-color:var(--accent);width:18px;height:18px"> Show evacuation routes</label>
        <ul class="legend">
          <li><span style="background:var(--accent-soft);border:1px solid var(--fg)"></span> Assembly area</li>
          <li><span style="border-top:3px dashed var(--accent);height:0"></span> Evacuation route</li>
        </ul>
        <p class="note">Schematic only — adjust building positions to match the official school floor plan.</p>
      </aside>
    </div>
  </div>
</section>
 
<section id="eready">
  <div class="wrap">
    <div class="eyebrow">Project E-READY</div>
    <h2 class="sec-title">Scan. Learn. Respond.</h2>
    <p class="lead">A QR code that puts emergency information in every pocket. Paste the link to your SDRRM resources and a scannable code is generated instantly.</p>
    <div class="ready-grid">
      <div class="qr-card">
        <canvas id="qr" width="300" height="300" aria-label="QR code"></canvas>
        <b>SCAN · <span>E-READY</span></b>
      </div>
      <div>
        <div class="field">
          <label for="qrUrl">Link to encode</label>
          <input id="qrUrl" type="url" placeholder="https://example.com/sdrrm">
          <div class="err" id="qrErr"></div>
        </div>
        <div class="cta"><button class="btn primary" id="qrGen">Generate QR</button><button class="btn" id="qrCopy">Copy link</button></div>
        <ul class="hotlines">
          <li><span>National Emergency Hotline</span><b>911</b></li>
          <li><span>Philippine Red Cross</span><b>143</b></li>
          <li><span>Bureau of Fire Protection</span><b>(Local station)</b></li>
          <li><span>School SDRRM Coordinator</span><b>Add number</b></li>
        </ul>
      </div>
    </div>
  </div>
</section>
 
<section id="handa" class="alt">
  <div class="wrap">
    <div class="eyebrow">Project HANDA</div>
    <h2 class="sec-title">Build your go bag</h2>
    <p class="lead">A go bag should be ready before the alarm sounds. Tick off each item as you pack it. Your progress is remembered on this device.</p>
    <div class="bag-grid" id="bagGrid"></div>
    <div class="progress">
      <div class="bar"><i id="bagBar"></i></div>
      <div id="bagText">0 of 0 packed</div>
      <button class="btn sm" id="bagReset">Reset</button>
    </div>
  </div>
</section>
 
<section id="volcano-sec">
  <div class="wrap">
    <div class="eyebrow">Project 3D Innovation Exhibit</div>
    <h2 class="sec-title">Volcano, up close</h2>
    <p class="lead">A digital twin of our volcano exhibit. Trigger an eruption, adjust its intensity, and peek inside the cone to see how magma rises.</p>
    <div class="volcano-box">
      <canvas id="volcano" width="1000" height="500"></canvas>
      <div class="v-info" id="vInfo">Press <b>Erupt</b> to simulate an eruption.</div>
      <div class="v-controls">
        <button class="btn primary sm" id="vErupt">🌋 Erupt</button>
        <button class="btn sm" id="vSection">Cross-section: Off</button>
        <label>Intensity <input type="range" id="vPower" min="1" max="10" value="5"></label>
      </div>
    </div>
  </div>
</section>
 
<section id="schedule" class="alt">
  <div class="wrap">
    <div class="eyebrow">Schedules</div>
    <h2 class="sec-title">Training &amp; drills</h2>
    <div class="tabs" role="tablist">
      <button class="tab on" data-tab="drill">Earthquake Drill</button>
      <button class="tab" data-tab="weekly">Weekly Rescue Lecture</button>
      <button class="tab" data-tab="workshop">Basic Training Workshop</button>
    </div>
 
    <div class="tabpane on" id="tab-drill">
      <h3>Earthquake Drill — 2nd Week</h3>
      <div class="countdown" id="countdown" aria-live="polite"></div>
      <div class="table-wrap"><table>
        <thead><tr><th>Day</th><th>Activity</th><th>Time</th></tr></thead>
        <tbody id="drillRows"></tbody>
      </table></div>
      <div class="steps">
        <div class="step"><b>1</b>DROP to your hands and knees.</div>
        <div class="step"><b>2</b>COVER your head and neck under a sturdy desk.</div>
        <div class="step"><b>3</b>HOLD ON until the shaking stops.</div>
        <div class="step"><b>4</b>EVACUATE calmly to the assembly area.</div>
      </div>
      <p class="note">Drill date is set to the 2nd week of the month in the script (<code>DRILL_DATE</code>). Update it to match the official school calendar.</p>
    </div>
 
    <div class="tabpane" id="tab-weekly">
      <h3>Weekly SDRRM Basic Rescue Lecture &amp; Training</h3>
      <p class="lead" style="margin-bottom:20px">Every Friday · 3:00 – 4:30 PM · Designated SDRRM room / school grounds</p>
      <div class="table-wrap"><table>
        <thead><tr><th>Week</th><th>Topic</th><th>Skill focus</th></tr></thead>
        <tbody>
          <tr><td><b>Week 1</b></td><td>Hazards &amp; Risk Mapping</td><td>Identify campus hazards</td></tr>
          <tr><td><b>Week 2</b></td><td>Knots, Lashing &amp; Rope Basics</td><td>Square, bowline, clove hitch</td></tr>
          <tr><td><b>Week 3</b></td><td>Basic First Aid &amp; Bandaging</td><td>Wounds, fractures, splints</td></tr>
          <tr><td><b>Week 4</b></td><td>Victim Carries &amp; Improvised Stretcher</td><td>Fireman's, two-hand seat, blanket</td></tr>
        </tbody>
      </table></div>
      <p class="note">Topics repeat monthly with progressively advanced drills.</p>
    </div>
 
    <div class="tabpane" id="tab-workshop">
      <h3>SDRRM Basic Training Workshop</h3>
      <p class="lead" style="margin-bottom:20px">An orientation for new members and class representatives.</p>
      <div class="table-wrap"><table>
        <thead><tr><th>Module</th><th>Content</th><th>Duration</th></tr></thead>
        <tbody>
          <tr><td><b>1</b></td><td>Introduction to DRRM &amp; school hazards</td><td>1 hr</td></tr>
          <tr><td><b>2</b></td><td>Emergency communication &amp; incident reporting</td><td>1 hr</td></tr>
          <tr><td><b>3</b></td><td>First aid, CPR awareness &amp; basic rescue</td><td>2 hrs</td></tr>
          <tr><td><b>4</b></td><td>Fire safety &amp; extinguisher use</td><td>1 hr</td></tr>
          <tr><td><b>5</b></td><td>Evacuation drill simulation</td><td>1 hr</td></tr>
        </tbody>
      </table></div>
    </div>
  </div>
</section>
 
<section id="join">
  <div class="wrap">
    <div class="eyebrow">Get involved</div>
    <h2 class="sec-title">Join the SDRRM team</h2>
    <div class="join-grid">
      <div>
        <p class="lead">Whether you love writing, filming, building, or leading, there's a place for you. Tell us where you'd like to help.</p>
        <p class="lead">Contest participants, trainees, and volunteers are all welcome.</p>
      </div>
      <form id="joinForm" novalidate onsubmit="return false">
        <div class="field"><label for="jName">Full name</label><input id="jName" autocomplete="name"><div class="err" id="eName"></div></div>
        <div class="field"><label for="jSec">Grade &amp; section</label><input id="jSec" placeholder="e.g. 12 – STEM A"><div class="err" id="eSec"></div></div>
        <div class="field"><label for="jProj">I'm interested in</label>
          <select id="jProj"></select></div>
        <div class="field"><label for="jMsg">Message (optional)</label><textarea id="jMsg" rows="3"></textarea></div>
        <button class="btn primary" id="jSend" type="button">Submit application</button>
        <div class="success" id="jOk"></div>
      </form>
    </div>
  </div>
</section>
</main>
 
<footer>
  <div class="wrap">
    <div><h4>SDRRM · Mataasnakahoy SHS</h4><p style="color:#8a8a8a;max-width:42ch;font-size:.9rem">Student-led disaster risk reduction and management. Prepared today, safer tomorrow.</p></div>
    <div><h4>Explore</h4><a href="#projects">Projects</a><a href="#escape">Evacuation map</a><a href="#schedule">Schedules</a></div>
    <div><h4>Connect</h4><a href="#join">Join us</a><a href="#eready">Emergency hotlines</a></div>
    <div class="copy">© <span id="yr"></span> SDRRM Organization · Mataasnakahoy Senior High School. All rights reserved.</div>
  </div>
</footer>
 
<dialog id="modal">
  <button class="icon-btn x" id="mClose" aria-label="Close">✕</button>
  <div class="modal-h"><div class="eyebrow" id="mTag"></div><h3 id="mTitle"></h3><div id="mSub" style="color:var(--muted)"></div></div>
  <div class="modal-b"><p id="mDesc"></p><ul id="mList"></ul><a class="btn primary sm" id="mGo" href="#">Go to section</a></div>
</dialog>
 
<div id="toast" role="status"></div>
<button id="toTop" aria-label="Back to top">↑</button>
 
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcode-generator/1.4.4/qrcode.min.js"></script>
<script>
(function(){
'use strict';
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];
const store={get(k){try{return localStorage.getItem(k)}catch(e){return null}},set(k,v){try{localStorage.setItem(k,v)}catch(e){}}};
function toast(msg){const t=$('#toast');t.textContent=msg;t.classList.add('show');clearTimeout(toast.t);toast.t=setTimeout(()=>t.classList.remove('show'),2400)}
 
/* ===== CONFIG ===== */
// Second week of the next drill month (edit to match the school calendar)
function secondWeekMonday(y,m){const d=new Date(y,m,1);const first=(8-d.getDay())%7||7; // first Monday
  const firstMon=new Date(y,m,1+((8-d.getDay())%7));return new Date(y,m,firstMon.getDate()+7,8,0,0)}
const DRILL_DATE=new Date(2026,10,11,9,0,0); // Wed, 11 Nov 2026, 9:00 AM
 
/* ===== Theme / nav ===== */
const root=document.documentElement;
const saved=store.get('sdrrm-theme'); if(saved) root.dataset.theme=saved;
$('#themeBtn').onclick=()=>{
  const dark=getComputedStyle(root).getPropertyValue('--bg').trim()==='#0b0b0b';
  root.dataset.theme=dark?'light':'dark'; store.set('sdrrm-theme',root.dataset.theme);
};
const menuBtn=$('#menuBtn'),navList=$('#navList');
menuBtn.onclick=()=>{const o=navList.classList.toggle('open');menuBtn.setAttribute('aria-expanded',o)};
$$('#navList a').forEach(a=>a.onclick=()=>{navList.classList.remove('open');menuBtn.setAttribute('aria-expanded',false)});
$('#yr').textContent=new Date().getFullYear();
 
/* ===== Scroll effects ===== */
const toTop=$('#toTop');
addEventListener('scroll',()=>toTop.classList.toggle('show',scrollY>600),{passive:true});
toTop.onclick=()=>scrollTo({top:0,behavior:'smooth'});
const secs=$$('main section[id]'), links=$$('#navList a');
const spy=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){links.forEach(l=>l.classList.toggle('active',l.getAttribute('href')==='#'+e.target.id))}}),{rootMargin:'-40% 0px -55% 0px'});
secs.forEach(s=>spy.observe(s));
const rev=new IntersectionObserver(es=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');rev.unobserve(e.target)}}),{threshold:.1});
function observeReveals(){$$('.reveal:not(.in)').forEach(el=>rev.observe(el))}
['.pillar','.bag-cat','.step','.stat'].forEach(s=>$$(s).forEach(el=>el.classList.add('reveal')));
 
/* counters */
const cio=new IntersectionObserver(es=>es.forEach(e=>{if(!e.isIntersecting)return;cio.unobserve(e.target);
  const el=e.target,end=+el.dataset.count,suf=el.dataset.suffix||'';let n=0;const step=Math.max(1,Math.ceil(end/40));
  const iv=setInterval(()=>{n=Math.min(end,n+step);el.textContent=n+suf;if(n>=end)clearInterval(iv)},30)}));
$$('[data-count]').forEach(el=>cio.observe(el));
 
/* ===== Projects ===== */
const PROJECTS=[
 {id:'sigla',cat:'Awareness',tag:'Project',title:'SIGLA',sub:'SDRRM Awareness and Advocacy Campaign',desc:'A school-wide campaign that sparks awareness of hazards and everyday safety habits through posters, announcements, class-to-class talks, and social media.',list:['Classroom-to-classroom advocacy talks','Posters, infographics, and campus signage','Social media safety series','Partnerships with barangay and LGU DRRM offices'],go:'#about'},
 {id:'handa',cat:'Preparedness',tag:'Project',title:'HANDA',sub:'Go Bag Implementation',desc:'Every learner and classroom is encouraged to keep a go bag ready with essentials for the first 72 hours of an emergency.',list:['Standard go bag checklist','Classroom go bag inspection','Packing demonstrations','Family preparedness take-home guide'],go:'#handa'},
 {id:'escape',cat:'Preparedness',tag:'Project',title:'ESCAPE',sub:'Map of Mataasnakahoy Senior High School',desc:'A clear evacuation map of the campus showing exits, routes, assembly areas, and safe zones — for posting in every room.',list:['Evacuation routes per building','Designated assembly area','Hazard and safe-zone markings','Interactive digital map on this site'],go:'#escape'},
 {id:'eready',cat:'Preparedness',tag:'Project',title:'E-READY',sub:'QR Code Emergency Information',desc:'Scannable QR codes placed around campus linking learners to emergency procedures, contacts, and the evacuation map.',list:['Instant access to hotlines','Step-by-step response guides','QR codes at classrooms and hallways','Easily updated links'],go:'#eready'},
 {id:'volcano',cat:'Innovation',tag:'Exhibit',title:'3D Innovation Exhibit',sub:'Volcano',desc:'A hands-on 3D volcano model that explains how eruptions happen and what hazards communities should prepare for.',list:['Cross-section of magma chamber and vent','Eruption demonstration','Hazard explanations: ashfall, lahar, lava','Interactive digital version on this site'],go:'#volcano-sec'},
 {id:'tinig',cat:'Contests',tag:'Project',title:'TINIG',sub:'SDRRM Spoken Poetry Contest',desc:'Learners lend their voice to disaster awareness through original spoken poetry on resilience, safety, and community.',list:['Original pieces in Filipino or English','Judged on content, delivery, and impact','Open to all grade levels','Top performers featured at school events'],go:'#join'},
 {id:'vision',cat:'Contests',tag:'Project',title:'VISION / ACTION',sub:'SDRRM Video Film Contest',desc:'Short films that tell stories of preparedness and response. Capture the vision, then put it into action.',list:['Short films on disaster themes','Teams of students with adviser guidance','Judged on message, creativity, and production','Screening night for the school community'],go:'#join'},
 {id:'workshop',cat:'Training',tag:'Training',title:'Basic Training Workshop',sub:'SDRRM Basic Training Workshop',desc:'A foundational workshop that equips members with core DRRM knowledge and hands-on response skills.',list:['DRRM fundamentals','First aid and basic rescue','Fire safety','Evacuation simulation'],go:'#schedule',tab:'workshop'},
 {id:'weekly',cat:'Training',tag:'Training',title:'Weekly Rescue Lecture',sub:'Weekly SDRRM Basic Rescue Lecture and Training',desc:'A weekly session that builds practical rescue skills step by step, from knots to victim carries.',list:['Every Friday afternoon','Lecture followed by practice','Progressive skill levels','Certificates of participation'],go:'#schedule',tab:'weekly'},
 {id:'drill',cat:'Training',tag:'Drill',title:'Earthquake Drill',sub:'2nd Week Schedule',desc:'A school-wide earthquake drill in the 2nd week of the month: drop, cover, hold, then orderly evacuation to the assembly area.',list:['Pre-drill briefing','Drop, Cover, and Hold','Evacuation and headcount','Post-drill evaluation'],go:'#schedule',tab:'drill'}
];
const cats=['All',...new Set(PROJECTS.map(p=>p.cat))];
const fEl=$('#filters'), grid=$('#projGrid');
cats.forEach((c,i)=>{const b=document.createElement('button');b.className='chip'+(i?'':' on');b.textContent=c;b.onclick=()=>{$$('.chip',fEl).forEach(x=>x.classList.toggle('on',x===b));$$('.card',grid).forEach(card=>card.classList.toggle('hide',c!=='All'&&card.dataset.cat!==c))};fEl.appendChild(b)});
PROJECTS.forEach((p,i)=>{
  const c=document.createElement('button');c.className='card reveal';c.dataset.cat=p.cat;
  c.innerHTML=`<span class="num">${String(i+1).padStart(2,'0')}</span><span class="tag">${p.cat}</span><h3>${p.title}</h3><span class="sub">${p.sub}</span><p>${p.desc}</p><span class="more">Learn more →</span>`;
  c.onclick=()=>openModal(p);grid.appendChild(c);
});
const modal=$('#modal');
function openModal(p){
  $('#mTag').textContent=p.cat;$('#mTitle').textContent=p.title;$('#mSub').textContent=p.sub;$('#mDesc').textContent=p.desc;
  $('#mList').innerHTML=p.list.map(x=>`<li>${x}</li>`).join('');
  const go=$('#mGo');go.href=p.go;go.onclick=()=>{modal.close();if(p.tab)setTab(p.tab)};
  modal.showModal();
}
$('#mClose').onclick=()=>modal.close();
modal.addEventListener('click',e=>{if(e.target===modal)modal.close()});
const sel=$('#jProj');sel.innerHTML=PROJECTS.map(p=>`<option>${p.title} – ${p.sub}</option>`).join('');
observeReveals();
 
/* ===== Map ===== */
const ROOMS={
 admin:['Administration Building','Command post during emergencies. Houses the principal\'s office, records, and the SDRRM coordinator\'s desk.'],
 bldga:['Classroom Building A','Evacuate by the nearest stairway, ground floor first. Teachers take attendance at the assembly area.'],
 bldgb:['Classroom Building B','Use the east exit and proceed directly to the open field. Do not use elevators or crowded stairwells.'],
 clinic:['School Clinic','First aid station. Injured learners are brought here for initial care before referral.'],
 court:['Covered Court','Alternate shelter in case of rain or heat. Check overhead structures after earthquakes before use.'],
 canteen:['Canteen','Shut off gas and power before leaving. Staff lead occupants through the south route.'],
 field:['Open Field · Assembly Area','Primary assembly point. Away from buildings, wires, and trees. Headcount is conducted by section.'],
 gate:['Main Gate','Exit point for evacuation off campus and for emergency vehicles. Keep clear at all times.']
};
$$('.group[data-room]').forEach(g=>{
  g.tabIndex=0;g.setAttribute('role','button');g.setAttribute('aria-label',ROOMS[g.dataset.room][0]);
  const pick=()=>{$$('.group').forEach(x=>x.classList.remove('sel'));$$('.room').forEach(x=>x.classList.remove('sel'));g.classList.add('sel');$('.room',g).classList.add('sel');
    $('#roomName').textContent=ROOMS[g.dataset.room][0];$('#roomInfo').textContent=ROOMS[g.dataset.room][1]};
  g.onclick=pick;g.onkeydown=e=>{if(e.key==='Enter'||e.key===' '){e.preventDefault();pick()}};
});
$('#routeToggle').onchange=e=>$('#mapLayout').classList.toggle('show-routes',e.target.checked);
 
/* ===== QR ===== */
const qrCanvas=$('#qr'),qctx=qrCanvas.getContext('2d');
function drawQR(text){
  if(typeof qrcode==='undefined'){qctx.fillStyle='#fff';qctx.fillRect(0,0,300,300);qctx.fillStyle='#800020';qctx.font='14px sans-serif';qctx.fillText('QR library unavailable',70,150);return false}
  const qr=qrcode(0,'M');qr.addData(text);qr.make();
  const n=qr.getModuleCount(),size=300,q=2,cell=size/(n+q*2);
  qctx.fillStyle='#fff';qctx.fillRect(0,0,size,size);qctx.fillStyle='#000';
  for(let r=0;r<n;r++)for(let c=0;c<n;c++)if(qr.isDark(r,c))qctx.fillRect(Math.round((c+q)*cell),Math.round((r+q)*cell),Math.ceil(cell),Math.ceil(cell));
  return true;
}
const qrUrl=$('#qrUrl');
qrUrl.value='https://example.com/sdrrm-mataasnakahoy';
function genQR(){
  const v=qrUrl.value.trim();
  if(!v){$('#qrErr').textContent='Please enter a link or text.';return}
  $('#qrErr').textContent='';
  try{ if(drawQR(v)) toast('QR code generated') }catch(e){$('#qrErr').textContent='That text is too long for a QR code.'}
}
$('#qrGen').onclick=genQR;
qrUrl.addEventListener('keydown',e=>{if(e.key==='Enter')genQR()});
$('#qrCopy').onclick=()=>{const v=qrUrl.value.trim();if(!v)return;
  (navigator.clipboard?navigator.clipboard.writeText(v):Promise.reject()).then(()=>toast('Link copied')).catch(()=>{qrUrl.select();toast('Press Ctrl/Cmd+C to copy')})};
window.addEventListener('load',genQR);
genQR();
 
/* ===== Go bag ===== */
const BAG={
 'Water & Food':['Drinking water (1 L+)','Ready-to-eat food / biscuits','Energy bars or candy','Reusable water bottle'],
 'First Aid':['First aid kit','Face masks','Alcohol / sanitizer','Personal medicines','Whistle'],
 'Tools & Light':['Flashlight','Extra batteries','Power bank','Battery or crank radio','Multi-tool / knife'],
 'Documents & Comfort':['Copy of IDs / school ID','Emergency contact list','Cash in small bills','Change of clothes','Blanket / raincoat']
};
const bagGrid=$('#bagGrid');let bagState={};try{bagState=JSON.parse(store.get('sdrrm-bag')||'{}')}catch(e){}
let total=0;
Object.entries(BAG).forEach(([cat,items])=>{
  const d=document.createElement('div');d.className='bag-cat reveal';d.innerHTML=`<h3>${cat}</h3>`;
  items.forEach(it=>{total++;const l=document.createElement('label');const id=cat+'|'+it;
    l.innerHTML=`<input type="checkbox"><span>${it}</span>`;const cb=$('input',l);cb.checked=!!bagState[id];
    cb.onchange=()=>{bagState[id]=cb.checked;store.set('sdrrm-bag',JSON.stringify(bagState));updBag(true)};d.appendChild(l)});
  bagGrid.appendChild(d);
});
let doneShown=false;
function updBag(fromUser){const n=$$('input',bagGrid).filter(c=>c.checked).length;
  $('#bagBar').style.width=(n/total*100)+'%';$('#bagText').textContent=`${n} of ${total} packed`;
  if(n===total&&fromUser&&!doneShown){doneShown=true;toast('🎒 Your go bag is ready!')} if(n<total)doneShown=false}
$('#bagReset').onclick=()=>{bagState={};store.set('sdrrm-bag','{}');$$('input',bagGrid).forEach(c=>c.checked=false);updBag();toast('Checklist reset')};
updBag();observeReveals();
 
/* ===== Volcano ===== */
(function(){
  const cv=$('#volcano'),ctx=cv.getContext('2d'),W=cv.width,H=cv.height;
  const base=H-40,topY=190,cx=W/2,craterW=70;
  let particles=[],smoke=[],erupting=0,section=false,t=0;
  const info=$('#vInfo');
  function spawn(power){
    for(let i=0;i<4+power*2;i++){
      const a=-Math.PI/2+(Math.random()-.5)*(.5+power*.04),s=5+Math.random()*power*1.3;
      particles.push({x:cx+(Math.random()-.5)*craterW*.6,y:topY,vx:Math.cos(a)*s,vy:Math.sin(a)*s,life:1,r:2+Math.random()*3});
    }
    smoke.push({x:cx+(Math.random()-.5)*30,y:topY-10,vx:(Math.random()-.5)*1.2,vy:-1-Math.random()*power*.2,r:14,life:1});
  }
  function drawCone(){
    ctx.fillStyle='#3a3a3a';ctx.beginPath();ctx.moveTo(cx-380,base);ctx.lineTo(cx-craterW/2,topY);ctx.lineTo(cx+craterW/2,topY);ctx.lineTo(cx+380,base);ctx.closePath();ctx.fill();
    ctx.fillStyle='#2b2b2b';ctx.beginPath();ctx.moveTo(cx,topY);ctx.lineTo(cx+craterW/2,topY);ctx.lineTo(cx+380,base);ctx.lineTo(cx+60,base);ctx.closePath();ctx.fill();
    ctx.fillStyle='#800020';ctx.beginPath();ctx.ellipse(cx,topY,craterW/2,7,0,0,7);ctx.fill();
    // ground
    ctx.fillStyle='#1b1b1b';ctx.fillRect(0,base,W,H-base);
    if(section){
      ctx.save();ctx.beginPath();ctx.moveTo(cx-380,base);ctx.lineTo(cx-craterW/2,topY);ctx.lineTo(cx+craterW/2,topY);ctx.lineTo(cx+380,base);ctx.closePath();ctx.clip();
      ctx.fillStyle='#d9d9d9';ctx.fillRect(0,0,W,H);
      ctx.strokeStyle='#999';for(let y=topY+30;y<base;y+=26){ctx.beginPath();ctx.moveTo(0,y);ctx.lineTo(W,y);ctx.stroke()}
      const g=ctx.createLinearGradient(0,topY,0,base);g.addColorStop(0,'#ff8a3d');g.addColorStop(1,'#800020');
      ctx.fillStyle=g;ctx.fillRect(cx-16,topY,32,base-topY-30);
      ctx.beginPath();ctx.ellipse(cx,base-30,120,34,0,0,7);ctx.fill();
      ctx.restore();
      ctx.fillStyle='#fff';ctx.font='600 13px Inter,sans-serif';
      ctx.fillText('Crater',cx+50,topY-12);ctx.fillText('Vent',cx+30,topY+90);ctx.fillText('Magma chamber',cx+130,base-24);
    }
  }
  function frame(){
    t++;ctx.clearRect(0,0,W,H);
    const sky=ctx.createLinearGradient(0,0,0,H);sky.addColorStop(0,'#0b0b0b');sky.addColorStop(1,erupting?'#3a0a14':'#242424');
    ctx.fillStyle=sky;ctx.fillRect(0,0,W,H);
    const p=+$('#vPower').value;
    if(erupting>0){spawn(p);erupting--;if(!erupting)info.innerHTML='Eruption subsiding. Always follow evacuation orders from authorities.'}
    smoke=smoke.filter(s=>s.life>0);smoke.forEach(s=>{s.x+=s.vx;s.y+=s.vy;s.r+=.5;s.life-=.006;ctx.fillStyle=`rgba(150,150,150,${s.life*.35})`;ctx.beginPath();ctx.arc(s.x,s.y,s.r,0,7);ctx.fill()});
    drawCone();
    particles=particles.filter(q=>q.life>0&&q.y<base);
    particles.forEach(q=>{q.x+=q.vx;q.y+=q.vy;q.vy+=.16;q.life-=.008;ctx.fillStyle=`rgba(${q.life>.5?255:192},${Math.round(80+q.life*100)},40,${q.life})`;ctx.beginPath();ctx.arc(q.x,q.y,q.r,0,7);ctx.fill()});
    if(erupting&&!section){ctx.fillStyle=`rgba(255,120,40,${.12+.08*Math.sin(t/3)})`;ctx.beginPath();ctx.arc(cx,topY,60+p*6,0,7);ctx.fill()}
    requestAnimationFrame(frame);
  }
  $('#vErupt').onclick=()=>{erupting=140;info.innerHTML='<b>Eruption!</b> Hazards include ashfall, pyroclastic flows, lava, and lahar. Evacuate away from the danger zone.'};
  $('#vSection').onclick=e=>{section=!section;e.target.textContent='Cross-section: '+(section?'On':'Off');info.textContent=section?'Magma rises from the chamber through the vent and exits at the crater.':'Press Erupt to simulate an eruption.'};
  frame();
})();
 
/* ===== Schedule ===== */
function setTab(name){$$('.tab').forEach(t=>t.classList.toggle('on',t.dataset.tab===name));$$('.tabpane').forEach(p=>p.classList.toggle('on',p.id==='tab-'+name))}
$$('.tab').forEach(t=>t.onclick=()=>setTab(t.dataset.tab));
const mon=new Date(DRILL_DATE);mon.setDate(mon.getDate()-((mon.getDay()+6)%7));
const DRILL=[
 ['Monday','Orientation & hazard review in classrooms','7:30 AM'],
 ['Tuesday','Evacuation route walk-through (per section)','10:00 AM'],
 ['Wednesday','<b>Earthquake drill: Drop, Cover, Hold &amp; Evacuate</b>','9:00 AM'],
 ['Thursday','Post-drill evaluation & feedback','1:00 PM'],
 ['Friday','Recognition of best-performing sections','3:00 PM']
];
$('#drillRows').innerHTML=DRILL.map((r,i)=>{const d=new Date(mon);d.setDate(mon.getDate()+i);
  return `<tr><td><b>${r[0]}</b><br><small style="color:var(--muted)">${d.toLocaleDateString('en-PH',{month:'short',day:'numeric'})}</small></td><td>${r[1]}</td><td>${r[2]}</td></tr>`}).join('');
function tick(){
  let diff=DRILL_DATE-new Date();const el=$('#countdown');
  if(diff<=0){el.innerHTML='<div class="cd" style="min-width:220px"><b>✓</b><span>Drill date has passed</span></div>';return}
  const d=Math.floor(diff/864e5),h=Math.floor(diff%864e5/36e5),m=Math.floor(diff%36e5/6e4),s=Math.floor(diff%6e4/1e3);
  el.innerHTML=[[d,'Days'],[h,'Hours'],[m,'Mins'],[s,'Secs']].map(x=>`<div class="cd"><b>${String(x[0]).padStart(2,'0')}</b><span>${x[1]}</span></div>`).join('');
}
tick();setInterval(tick,1000);
 
/* ===== Join form ===== */
$('#jSend').onclick=()=>{
  const n=$('#jName').value.trim(),s=$('#jSec').value.trim();let ok=true;
  $('#eName').textContent=n.length<3?(ok=false,'Please enter your full name.'):'';
  $('#eSec').textContent=!s?(ok=false,'Please enter your grade & section.'):'';
  if(!ok)return;
  const box=$('#jOk');box.style.display='block';
  box.innerHTML=`<b>Thank you, ${n.replace(/</g,'&lt;')}!</b><br>Your interest in <i>${sel.value.replace(/</g,'&lt;')}</i> has been noted. An SDRRM officer will reach out to ${s.replace(/</g,'&lt;')} soon.`;
  toast('Application submitted');$('#joinForm').reset();
};
})();
</script>
</body>
</html>
