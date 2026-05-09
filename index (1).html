<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>EcoTrack – Carbon Footprint Calculator</title>
<link href="https://fonts.googleapis.com/css2?family=Cabinet+Grotesk:wght@400;500;700;800;900&family=Satoshi:wght@300;400;500;700&display=swap" rel="stylesheet"/>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
/* ============================================================
   DESIGN TOKENS & RESET
   ============================================================ */
:root {
  --bg-primary: #080f0a;
  --bg-secondary: #0d1a10;
  --bg-card: rgba(13,26,16,0.85);
  --bg-glass: rgba(20,40,24,0.6);
  --green-primary: #22c55e;
  --green-light: #4ade80;
  --green-dim: #16a34a;
  --teal: #14b8a6;
  --blue: #3b82f6;
  --amber: #f59e0b;
  --red: #ef4444;
  --text-primary: #f0fdf4;
  --text-secondary: #86efac;
  --text-muted: #4ade80aa;
  --border: rgba(34,197,94,0.18);
  --border-bright: rgba(34,197,94,0.4);
  --shadow: 0 8px 40px rgba(34,197,94,0.08);
  --shadow-strong: 0 20px 60px rgba(34,197,94,0.15);
  --radius: 16px;
  --radius-sm: 10px;
  --font-display: 'Cabinet Grotesk', sans-serif;
  --font-body: 'Satoshi', sans-serif;
  --transition: 0.3s cubic-bezier(0.4,0,0.2,1);
}
[data-theme="light"] {
  --bg-primary: #f0fdf4;
  --bg-secondary: #dcfce7;
  --bg-card: rgba(240,253,244,0.92);
  --bg-glass: rgba(220,252,231,0.7);
  --text-primary: #052e16;
  --text-secondary: #166534;
  --text-muted: #15803daa;
  --border: rgba(21,128,61,0.2);
  --border-bright: rgba(21,128,61,0.5);
  --shadow: 0 8px 40px rgba(21,128,61,0.1);
  --shadow-strong: 0 20px 60px rgba(21,128,61,0.18);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;font-size:16px}
body{
  font-family:var(--font-body);
  background:var(--bg-primary);
  color:var(--text-primary);
  line-height:1.6;
  overflow-x:hidden;
  transition:background var(--transition), color var(--transition);
}
::selection{background:var(--green-primary);color:#000}
::-webkit-scrollbar{width:6px}
::-webkit-scrollbar-track{background:var(--bg-primary)}
::-webkit-scrollbar-thumb{background:var(--green-dim);border-radius:3px}
h1,h2,h3,h4,h5{font-family:var(--font-display);line-height:1.15;font-weight:800}
a{color:inherit;text-decoration:none}
button{cursor:pointer;font-family:var(--font-body)}
input,select,textarea{font-family:var(--font-body)}
img{max-width:100%;height:auto}

/* ============================================================
   UTILITY CLASSES
   ============================================================ */
.container{max-width:1200px;margin:0 auto;padding:0 24px}
.section{padding:80px 0}
.section-title{font-size:clamp(2rem,4vw,3rem);margin-bottom:12px}
.section-subtitle{color:var(--text-secondary);font-size:1.1rem;margin-bottom:48px;max-width:560px}
.badge{
  display:inline-flex;align-items:center;gap:6px;
  background:rgba(34,197,94,0.1);border:1px solid var(--border-bright);
  color:var(--green-primary);padding:6px 14px;border-radius:99px;
  font-size:0.8rem;font-weight:600;letter-spacing:0.05em;text-transform:uppercase;
  margin-bottom:16px;
}
.badge::before{content:'';width:7px;height:7px;background:var(--green-primary);border-radius:50%;animation:pulse 2s infinite}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:0.5;transform:scale(1.4)}}

/* BUTTONS */
.btn{
  display:inline-flex;align-items:center;gap:8px;
  padding:14px 28px;border-radius:99px;font-size:0.95rem;font-weight:600;
  border:none;transition:all var(--transition);position:relative;overflow:hidden;
}
.btn::after{
  content:'';position:absolute;inset:0;background:rgba(255,255,255,0.1);
  opacity:0;transition:opacity var(--transition);
}
.btn:hover::after{opacity:1}
.btn-primary{background:var(--green-primary);color:#000}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 12px 30px rgba(34,197,94,0.4)}
.btn-outline{background:transparent;color:var(--green-primary);border:1.5px solid var(--green-primary)}
.btn-outline:hover{background:rgba(34,197,94,0.1);transform:translateY(-2px)}
.btn-sm{padding:9px 18px;font-size:0.85rem}

/* CARDS */
.card{
  background:var(--bg-card);
  border:1px solid var(--border);
  border-radius:var(--radius);
  padding:28px;
  backdrop-filter:blur(20px);
  transition:all var(--transition);
  box-shadow:var(--shadow);
}
.card:hover{border-color:var(--border-bright);box-shadow:var(--shadow-strong);transform:translateY(-2px)}

/* GLASS MORPHISM */
.glass{
  background:var(--bg-glass);
  border:1px solid var(--border);
  backdrop-filter:blur(24px);
  border-radius:var(--radius);
}

/* GRID */
.grid-2{display:grid;grid-template-columns:repeat(2,1fr);gap:24px}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:24px}
.grid-4{display:grid;grid-template-columns:repeat(4,1fr);gap:24px}

/* FORM ELEMENTS */
.form-group{margin-bottom:20px}
.form-group label{display:block;font-size:0.88rem;font-weight:600;color:var(--text-secondary);margin-bottom:8px;letter-spacing:0.02em}
.form-control{
  width:100%;padding:12px 16px;
  background:rgba(34,197,94,0.05);
  border:1.5px solid var(--border);
  border-radius:var(--radius-sm);
  color:var(--text-primary);
  font-size:0.95rem;
  transition:all var(--transition);
  outline:none;
}
.form-control:focus{border-color:var(--green-primary);background:rgba(34,197,94,0.08);box-shadow:0 0 0 3px rgba(34,197,94,0.12)}
.form-control::placeholder{color:var(--text-muted)}
select.form-control option{background:var(--bg-secondary);color:var(--text-primary)}

/* PROGRESS BAR */
.progress-bar{background:rgba(34,197,94,0.1);border-radius:99px;height:8px;overflow:hidden}
.progress-fill{height:100%;border-radius:99px;background:linear-gradient(90deg,var(--green-dim),var(--green-primary));transition:width 1s cubic-bezier(0.4,0,0.2,1)}

/* TABS */
.tabs{display:flex;gap:4px;background:rgba(34,197,94,0.06);padding:6px;border-radius:12px;border:1px solid var(--border)}
.tab-btn{
  flex:1;padding:10px 16px;border:none;background:transparent;
  color:var(--text-muted);border-radius:9px;font-size:0.9rem;font-weight:600;
  transition:all var(--transition);
}
.tab-btn.active{background:var(--green-primary);color:#000}
.tab-btn:not(.active):hover{background:rgba(34,197,94,0.1);color:var(--green-light)}
.tab-content{display:none}
.tab-content.active{display:block}

/* ============================================================
   LOADING SCREEN
   ============================================================ */
#loader{
  position:fixed;inset:0;z-index:9999;
  background:var(--bg-primary);
  display:flex;flex-direction:column;align-items:center;justify-content:center;gap:20px;
  transition:opacity 0.6s ease, visibility 0.6s ease;
}
#loader.hidden{opacity:0;visibility:hidden}
.loader-logo{font-family:var(--font-display);font-size:2.2rem;font-weight:900;color:var(--green-primary)}
.loader-ring{
  width:56px;height:56px;border:3px solid rgba(34,197,94,0.15);
  border-top-color:var(--green-primary);border-radius:50%;
  animation:spin 0.9s linear infinite;
}
@keyframes spin{to{transform:rotate(360deg)}}
.loader-text{font-size:0.85rem;color:var(--text-muted);letter-spacing:0.08em;animation:blink 1.4s ease infinite}
@keyframes blink{0%,100%{opacity:0.4}50%{opacity:1}}

/* ============================================================
   NAVBAR
   ============================================================ */
#navbar{
  position:fixed;top:0;left:0;right:0;z-index:999;
  padding:16px 0;
  transition:all var(--transition);
}
#navbar.scrolled{
  background:rgba(8,15,10,0.9);
  backdrop-filter:blur(24px);
  border-bottom:1px solid var(--border);
  padding:10px 0;
}
[data-theme="light"] #navbar.scrolled{background:rgba(240,253,244,0.9)}
.nav-inner{display:flex;align-items:center;justify-content:space-between}
.nav-logo{font-family:var(--font-display);font-size:1.5rem;font-weight:900;color:var(--green-primary)}
.nav-logo span{color:var(--text-primary)}
.nav-links{display:flex;align-items:center;gap:32px}
.nav-links a{font-size:0.9rem;font-weight:500;color:var(--text-secondary);transition:color var(--transition)}
.nav-links a:hover{color:var(--green-primary)}
.nav-actions{display:flex;align-items:center;gap:12px}
.theme-toggle{
  background:rgba(34,197,94,0.1);border:1px solid var(--border);
  color:var(--text-primary);width:40px;height:40px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;font-size:1.1rem;
  transition:all var(--transition);
}
.theme-toggle:hover{background:rgba(34,197,94,0.2);border-color:var(--border-bright)}
.hamburger{display:none;flex-direction:column;gap:5px;background:none;border:none;padding:4px}
.hamburger span{width:24px;height:2px;background:var(--text-primary);border-radius:2px;transition:all var(--transition)}
.mobile-menu{
  display:none;position:fixed;top:72px;left:0;right:0;z-index:998;
  background:var(--bg-secondary);border-bottom:1px solid var(--border);
  padding:20px 24px;flex-direction:column;gap:16px;
  animation:slideDown 0.3s ease;
}
@keyframes slideDown{from{opacity:0;transform:translateY(-10px)}to{opacity:1;transform:translateY(0)}}
.mobile-menu.open{display:flex}
.mobile-menu a{font-size:1rem;font-weight:500;color:var(--text-secondary);padding:8px 0;border-bottom:1px solid var(--border)}

/* ============================================================
   HERO SECTION
   ============================================================ */
#hero{
  min-height:100vh;display:flex;align-items:center;
  position:relative;overflow:hidden;padding-top:90px;
}
.hero-bg{
  position:absolute;inset:0;z-index:0;
  background:
    radial-gradient(ellipse 80% 60% at 50% -10%, rgba(34,197,94,0.18) 0%, transparent 60%),
    radial-gradient(ellipse 40% 40% at 80% 70%, rgba(20,184,166,0.12) 0%, transparent 50%),
    radial-gradient(ellipse 30% 30% at 10% 80%, rgba(59,130,246,0.08) 0%, transparent 50%);
}
.hero-grid{
  position:absolute;inset:0;z-index:0;
  background-image:
    linear-gradient(rgba(34,197,94,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(34,197,94,0.04) 1px, transparent 1px);
  background-size:60px 60px;
  mask-image:radial-gradient(ellipse 80% 80% at center, black 30%, transparent 80%);
}
/* Floating particles */
.particles{position:absolute;inset:0;z-index:0;overflow:hidden}
.particle{
  position:absolute;border-radius:50%;
  background:radial-gradient(circle, rgba(34,197,94,0.6), transparent);
  animation:float var(--dur,8s) ease-in-out infinite;
  animation-delay:var(--delay,0s);
  opacity:0.4;
}
@keyframes float{0%,100%{transform:translateY(0) scale(1)}50%{transform:translateY(-30px) scale(1.1)}}
.hero-content{position:relative;z-index:1;max-width:700px}
.hero-title{font-size:clamp(2.8rem,6vw,5rem);line-height:1.05;margin-bottom:20px}
.hero-title .accent{
  background:linear-gradient(135deg,var(--green-primary),var(--teal));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
}
.hero-desc{font-size:1.15rem;color:var(--text-secondary);margin-bottom:36px;max-width:520px;line-height:1.7}
.hero-actions{display:flex;flex-wrap:wrap;gap:14px;margin-bottom:56px}
.hero-stats{display:flex;flex-wrap:wrap;gap:32px}
.hero-stat{display:flex;flex-direction:column}
.hero-stat-num{font-family:var(--font-display);font-size:1.9rem;font-weight:900;color:var(--green-primary)}
.hero-stat-label{font-size:0.82rem;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.06em}
/* Earth orb */
.hero-orb{
  position:absolute;right:-60px;top:50%;transform:translateY(-50%);
  width:520px;height:520px;z-index:1;
  background:radial-gradient(circle at 35% 35%,
    rgba(34,197,94,0.35) 0%,
    rgba(20,184,166,0.2) 30%,
    rgba(59,130,246,0.15) 60%,
    transparent 80%);
  border-radius:50%;
  box-shadow:
    0 0 60px rgba(34,197,94,0.2),
    0 0 120px rgba(34,197,94,0.1),
    inset 0 0 80px rgba(0,0,0,0.4);
  animation:orbPulse 6s ease-in-out infinite;
  border:1px solid rgba(34,197,94,0.2);
  display:flex;align-items:center;justify-content:center;font-size:200px;
}
@keyframes orbPulse{0%,100%{box-shadow:0 0 60px rgba(34,197,94,0.2),0 0 120px rgba(34,197,94,0.1)}50%{box-shadow:0 0 80px rgba(34,197,94,0.3),0 0 160px rgba(34,197,94,0.15)}}

/* Scroll cue */
.scroll-cue{
  position:absolute;bottom:32px;left:50%;transform:translateX(-50%);
  display:flex;flex-direction:column;align-items:center;gap:6px;
  color:var(--text-muted);font-size:0.75rem;letter-spacing:0.1em;text-transform:uppercase;z-index:1;
}
.scroll-arrow{
  width:1px;height:40px;background:linear-gradient(180deg,var(--green-primary),transparent);
  animation:scrollDown 1.8s ease-in-out infinite;
}
@keyframes scrollDown{0%{transform:scaleY(0);transform-origin:top}50%{transform:scaleY(1);transform-origin:top}50.1%{transform:scaleY(1);transform-origin:bottom}100%{transform:scaleY(0);transform-origin:bottom}}

/* ============================================================
   STATS TICKER
   ============================================================ */
.ticker{
  background:rgba(34,197,94,0.06);
  border-top:1px solid var(--border);border-bottom:1px solid var(--border);
  padding:14px 0;overflow:hidden;
}
.ticker-inner{
  display:flex;gap:60px;white-space:nowrap;
  animation:ticker 30s linear infinite;
}
@keyframes ticker{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.ticker-item{font-size:0.88rem;color:var(--text-secondary);font-weight:500;display:flex;align-items:center;gap:8px}
.ticker-item .dot{color:var(--green-primary)}

/* ============================================================
   AWARENESS SECTION
   ============================================================ */
.awareness-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:24px;margin-top:48px}
.awareness-card{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:28px;position:relative;overflow:hidden;transition:all var(--transition);
}
.awareness-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:3px;
  background:linear-gradient(90deg,var(--green-primary),var(--teal));
}
.awareness-card:hover{transform:translateY(-4px);border-color:var(--border-bright);box-shadow:var(--shadow-strong)}
.awareness-icon{font-size:2.2rem;margin-bottom:16px}
.awareness-card h3{font-size:1.15rem;margin-bottom:10px;color:var(--text-primary)}
.awareness-card p{font-size:0.9rem;color:var(--text-secondary);line-height:1.65}
.awareness-stat{
  display:inline-block;margin-top:14px;
  font-family:var(--font-display);font-size:1.5rem;font-weight:900;
  color:var(--green-primary);
}

/* ============================================================
   CALCULATOR SECTION
   ============================================================ */
#calculator{background:var(--bg-secondary)}
.calc-layout{display:grid;grid-template-columns:1fr 1fr;gap:32px;align-items:start}
.calc-form-wrapper{background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);padding:32px;backdrop-filter:blur(20px)}
.calc-form-wrapper h3{font-size:1.4rem;margin-bottom:24px;color:var(--text-primary)}
.input-group{
  display:grid;grid-template-columns:1fr auto;gap:10px;align-items:end;
}
.input-unit{
  padding:12px 14px;background:rgba(34,197,94,0.08);
  border:1.5px solid var(--border);border-radius:var(--radius-sm);
  color:var(--text-muted);font-size:0.88rem;white-space:nowrap;
}
.calc-btn-row{margin-top:28px;display:flex;gap:12px}
/* Results panel */
.results-panel{display:flex;flex-direction:column;gap:20px}
.result-hero{
  background:linear-gradient(135deg,rgba(34,197,94,0.15),rgba(20,184,166,0.1));
  border:1px solid var(--border-bright);border-radius:var(--radius);
  padding:32px;text-align:center;
}
.result-hero-num{font-family:var(--font-display);font-size:3.5rem;font-weight:900;color:var(--green-primary)}
.result-hero-unit{font-size:1rem;color:var(--text-secondary)}
.result-hero-label{font-size:0.85rem;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.06em;margin-top:4px}
.impact-badge{
  display:inline-block;margin-top:16px;padding:8px 20px;border-radius:99px;
  font-weight:700;font-size:0.9rem;letter-spacing:0.04em;
}
.impact-low{background:rgba(34,197,94,0.2);color:var(--green-light);border:1px solid rgba(34,197,94,0.4)}
.impact-moderate{background:rgba(245,158,11,0.2);color:#fbbf24;border:1px solid rgba(245,158,11,0.4)}
.impact-high{background:rgba(249,115,22,0.2);color:#fb923c;border:1px solid rgba(249,115,22,0.4)}
.impact-critical{background:rgba(239,68,68,0.2);color:#f87171;border:1px solid rgba(239,68,68,0.4)}
.breakdown-list{display:flex;flex-direction:column;gap:12px}
.breakdown-item{display:flex;flex-direction:column;gap:6px}
.breakdown-header{display:flex;justify-content:space-between;align-items:center;font-size:0.88rem}
.breakdown-label{color:var(--text-secondary);font-weight:500}
.breakdown-value{color:var(--text-primary);font-weight:700}
/* Chart */
.chart-wrapper{background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);padding:24px;height:280px;position:relative}

/* ============================================================
   SUGGESTIONS SECTION
   ============================================================ */
.suggestions-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:20px;margin-top:40px}
.suggestion-card{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:24px;display:flex;flex-direction:column;gap:12px;
  transition:all var(--transition);cursor:default;
}
.suggestion-card:hover{transform:translateY(-3px);border-color:var(--border-bright);box-shadow:var(--shadow-strong)}
.suggestion-icon{
  width:48px;height:48px;border-radius:12px;
  background:rgba(34,197,94,0.1);border:1px solid var(--border);
  display:flex;align-items:center;justify-content:center;font-size:1.5rem;
}
.suggestion-card h4{font-size:0.98rem;font-weight:700;color:var(--text-primary)}
.suggestion-card p{font-size:0.85rem;color:var(--text-secondary);line-height:1.6}
.suggestion-impact{
  display:inline-block;font-size:0.75rem;font-weight:600;padding:4px 10px;
  border-radius:99px;background:rgba(34,197,94,0.1);color:var(--green-primary);
  border:1px solid var(--border);margin-top:auto;align-self:flex-start;
}

/* ============================================================
   DASHBOARD SECTION
   ============================================================ */
#dashboard{background:var(--bg-secondary)}
.dash-grid{display:grid;grid-template-columns:280px 1fr;gap:28px;align-items:start}
.dash-sidebar{display:flex;flex-direction:column;gap:16px}
.profile-card{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:24px;text-align:center;
}
.profile-avatar{
  width:72px;height:72px;border-radius:50%;
  background:linear-gradient(135deg,var(--green-primary),var(--teal));
  margin:0 auto 12px;display:flex;align-items:center;justify-content:center;
  font-size:1.8rem;font-weight:800;font-family:var(--font-display);color:#000;
}
.profile-name{font-size:1.1rem;font-weight:700;margin-bottom:4px}
.profile-since{font-size:0.8rem;color:var(--text-muted)}
.profile-badge{
  margin-top:14px;padding:6px 14px;border-radius:99px;
  background:rgba(34,197,94,0.1);color:var(--green-primary);
  font-size:0.8rem;font-weight:600;border:1px solid var(--border);
}
.dash-nav{display:flex;flex-direction:column;gap:4px}
.dash-nav-item{
  padding:10px 14px;border-radius:var(--radius-sm);border:none;background:transparent;
  color:var(--text-secondary);font-size:0.9rem;font-weight:500;text-align:left;
  display:flex;align-items:center;gap:10px;transition:all var(--transition);
}
.dash-nav-item:hover{background:rgba(34,197,94,0.08);color:var(--text-primary)}
.dash-nav-item.active{background:rgba(34,197,94,0.12);color:var(--green-primary)}
.dash-main{display:flex;flex-direction:column;gap:24px}
.dash-kpis{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.kpi-card{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:20px;
}
.kpi-icon{font-size:1.5rem;margin-bottom:10px}
.kpi-value{font-family:var(--font-display);font-size:1.7rem;font-weight:900;color:var(--green-primary)}
.kpi-label{font-size:0.8rem;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.05em}
.kpi-change{font-size:0.82rem;font-weight:600;margin-top:4px}
.kpi-change.up{color:#f87171}
.kpi-change.down{color:var(--green-primary)}
.history-table{width:100%;border-collapse:collapse}
.history-table th{font-size:0.78rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--text-muted);padding:10px 14px;text-align:left;border-bottom:1px solid var(--border)}
.history-table td{padding:12px 14px;font-size:0.9rem;border-bottom:1px solid rgba(34,197,94,0.06)}
.history-table tr:hover td{background:rgba(34,197,94,0.04)}
.history-table .impact-pill{display:inline-block;padding:3px 10px;border-radius:99px;font-size:0.78rem;font-weight:600}
.chart-row{display:grid;grid-template-columns:1fr 1fr;gap:20px}

/* ============================================================
   LEADERBOARD SECTION
   ============================================================ */
.leaderboard-list{display:flex;flex-direction:column;gap:12px;margin-top:40px}
.lb-item{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:18px 24px;display:flex;align-items:center;gap:18px;
  transition:all var(--transition);
}
.lb-item:hover{transform:translateX(4px);border-color:var(--border-bright)}
.lb-rank{
  width:36px;height:36px;border-radius:50%;
  background:rgba(34,197,94,0.1);border:1px solid var(--border);
  display:flex;align-items:center;justify-content:center;
  font-family:var(--font-display);font-weight:900;font-size:0.95rem;color:var(--text-muted);
  flex-shrink:0;
}
.lb-item:nth-child(1) .lb-rank{background:rgba(255,196,0,0.15);color:#ffd700;border-color:rgba(255,196,0,0.3)}
.lb-item:nth-child(2) .lb-rank{background:rgba(192,192,192,0.15);color:#c0c0c0;border-color:rgba(192,192,192,0.3)}
.lb-item:nth-child(3) .lb-rank{background:rgba(205,127,50,0.15);color:#cd7f32;border-color:rgba(205,127,50,0.3)}
.lb-avatar{
  width:44px;height:44px;border-radius:50%;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
  font-weight:800;font-size:1rem;color:#000;font-family:var(--font-display);
}
.lb-info{flex:1}
.lb-name{font-weight:700;font-size:0.98rem;margin-bottom:2px}
.lb-detail{font-size:0.82rem;color:var(--text-muted)}
.lb-score{text-align:right}
.lb-co2{font-family:var(--font-display);font-weight:900;font-size:1.2rem;color:var(--green-primary)}
.lb-co2-label{font-size:0.75rem;color:var(--text-muted)}
.lb-badge{
  display:inline-block;padding:4px 10px;border-radius:99px;
  background:rgba(34,197,94,0.1);color:var(--green-primary);
  font-size:0.75rem;font-weight:600;border:1px solid var(--border);
  margin-top:4px;
}

/* ============================================================
   AUTH SECTION
   ============================================================ */
#auth{background:var(--bg-secondary)}
.auth-layout{display:grid;grid-template-columns:1fr 1fr;gap:48px;align-items:center;min-height:500px}
.auth-info{}
.auth-info h2{font-size:2.4rem;margin-bottom:16px}
.auth-feature{display:flex;align-items:flex-start;gap:12px;margin-bottom:18px}
.auth-feature-icon{
  width:36px;height:36px;border-radius:9px;
  background:rgba(34,197,94,0.1);border:1px solid var(--border);
  display:flex;align-items:center;justify-content:center;font-size:1rem;flex-shrink:0;
}
.auth-feature p{font-size:0.9rem;color:var(--text-secondary);line-height:1.5}
.auth-feature strong{color:var(--text-primary)}
.auth-card{background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);padding:36px;backdrop-filter:blur(20px)}
.auth-tabs{display:flex;gap:0;margin-bottom:28px;background:rgba(34,197,94,0.06);border-radius:10px;padding:5px;border:1px solid var(--border)}
.auth-tab{flex:1;padding:10px;border:none;background:transparent;color:var(--text-muted);font-size:0.9rem;font-weight:600;border-radius:7px;transition:all var(--transition)}
.auth-tab.active{background:var(--green-primary);color:#000}
.auth-tab:not(.active):hover{background:rgba(34,197,94,0.1);color:var(--green-primary)}
.auth-form{display:none;flex-direction:column;gap:0}
.auth-form.active{display:flex}
.remember-row{display:flex;align-items:center;justify-content:space-between;font-size:0.87rem;margin-top:4px;margin-bottom:20px}
.remember-row label{color:var(--text-secondary);display:flex;align-items:center;gap:6px}
.remember-row a{color:var(--green-primary)}
.password-strength{height:4px;border-radius:99px;background:rgba(34,197,94,0.1);margin-top:6px;overflow:hidden}
.password-strength-fill{height:100%;border-radius:99px;transition:all 0.4s ease}

/* ============================================================
   ADMIN PANEL
   ============================================================ */
#admin{background:var(--bg-secondary)}
.admin-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:32px}
.admin-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-bottom:28px}
.admin-stat-card{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);
  padding:20px;display:flex;align-items:center;gap:14px;
}
.admin-stat-icon{width:44px;height:44px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:1.2rem;flex-shrink:0}
.admin-stat-icon.green{background:rgba(34,197,94,0.15)}
.admin-stat-icon.teal{background:rgba(20,184,166,0.15)}
.admin-stat-icon.blue{background:rgba(59,130,246,0.15)}
.admin-stat-icon.amber{background:rgba(245,158,11,0.15)}
.admin-stat-info{}
.admin-stat-num{font-family:var(--font-display);font-size:1.6rem;font-weight:900;color:var(--text-primary)}
.admin-stat-label{font-size:0.8rem;color:var(--text-muted);text-transform:uppercase;letter-spacing:0.05em}
.admin-table-section{background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius);padding:24px;margin-bottom:24px}
.admin-table-section h3{font-size:1.1rem;margin-bottom:20px}
.users-table{width:100%;border-collapse:collapse}
.users-table th{font-size:0.77rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--text-muted);padding:8px 14px;text-align:left;border-bottom:1px solid var(--border)}
.users-table td{padding:11px 14px;font-size:0.88rem;border-bottom:1px solid rgba(34,197,94,0.05)}
.users-table tr:hover td{background:rgba(34,197,94,0.03)}
.user-dot{width:8px;height:8px;border-radius:50%;display:inline-block;margin-right:6px}
.user-dot.active{background:var(--green-primary)}
.user-dot.inactive{background:var(--text-muted)}
.tips-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.tip-item{background:rgba(34,197,94,0.05);border:1px solid var(--border);border-radius:var(--radius-sm);padding:14px;display:flex;align-items:center;gap:10px;font-size:0.88rem}
.tip-item span.emoji{font-size:1.2rem}
.tip-actions{display:flex;gap:8px;margin-left:auto}
.icon-btn{background:none;border:1px solid var(--border);color:var(--text-muted);width:30px;height:30px;border-radius:7px;display:flex;align-items:center;justify-content:center;font-size:0.85rem;transition:all var(--transition)}
.icon-btn:hover{border-color:var(--border-bright);color:var(--text-primary)}

/* ============================================================
   CHATBOT
   ============================================================ */
.chatbot-fab{
  position:fixed;bottom:28px;right:28px;z-index:900;
  width:56px;height:56px;border-radius:50%;
  background:linear-gradient(135deg,var(--green-primary),var(--teal));
  border:none;font-size:1.4rem;box-shadow:0 8px 24px rgba(34,197,94,0.35);
  display:flex;align-items:center;justify-content:center;
  transition:all var(--transition);color:#000;
}
.chatbot-fab:hover{transform:scale(1.08);box-shadow:0 12px 30px rgba(34,197,94,0.45)}
.chatbot-panel{
  position:fixed;bottom:96px;right:28px;z-index:900;
  width:340px;max-height:480px;
  background:var(--bg-card);border:1px solid var(--border-bright);border-radius:var(--radius);
  backdrop-filter:blur(24px);box-shadow:var(--shadow-strong);
  display:flex;flex-direction:column;overflow:hidden;
  transition:all 0.4s cubic-bezier(0.4,0,0.2,1);
  transform-origin:bottom right;
}
.chatbot-panel.closed{opacity:0;transform:scale(0.85) translateY(20px);pointer-events:none}
.chatbot-header{
  padding:16px 20px;border-bottom:1px solid var(--border);
  display:flex;align-items:center;justify-content:space-between;
  background:rgba(34,197,94,0.08);
}
.chatbot-title{display:flex;align-items:center;gap:10px;font-weight:700;font-size:0.95rem}
.chatbot-dot{width:8px;height:8px;border-radius:50%;background:var(--green-primary);animation:pulse 2s infinite}
.chatbot-close{background:none;border:none;color:var(--text-muted);font-size:1.1rem;transition:color var(--transition)}
.chatbot-close:hover{color:var(--text-primary)}
.chatbot-messages{flex:1;overflow-y:auto;padding:16px;display:flex;flex-direction:column;gap:12px}
.msg{max-width:85%;border-radius:12px;padding:10px 14px;font-size:0.87rem;line-height:1.55;animation:msgIn 0.3s ease}
@keyframes msgIn{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}
.msg.bot{background:rgba(34,197,94,0.1);border:1px solid var(--border);align-self:flex-start;color:var(--text-primary)}
.msg.user{background:var(--green-primary);color:#000;align-self:flex-end;font-weight:500}
.chatbot-input-row{display:flex;gap:8px;padding:12px 16px;border-top:1px solid var(--border)}
.chatbot-input{
  flex:1;background:rgba(34,197,94,0.06);border:1px solid var(--border);
  border-radius:99px;padding:9px 16px;color:var(--text-primary);font-size:0.87rem;outline:none;
}
.chatbot-input:focus{border-color:var(--green-primary)}
.chatbot-send{
  width:36px;height:36px;border-radius:50%;
  background:var(--green-primary);border:none;color:#000;font-size:0.9rem;
  display:flex;align-items:center;justify-content:center;flex-shrink:0;
  transition:all var(--transition);
}
.chatbot-send:hover{transform:scale(1.08)}

/* ============================================================
   FOOTER
   ============================================================ */
footer{
  background:var(--bg-secondary);border-top:1px solid var(--border);
  padding:56px 0 32px;
}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:40px;margin-bottom:40px}
.footer-brand p{font-size:0.9rem;color:var(--text-secondary);margin-top:12px;max-width:260px;line-height:1.6}
.footer-col h4{font-size:0.88rem;text-transform:uppercase;letter-spacing:0.08em;color:var(--text-muted);margin-bottom:16px}
.footer-col a{display:block;font-size:0.9rem;color:var(--text-secondary);margin-bottom:8px;transition:color var(--transition)}
.footer-col a:hover{color:var(--green-primary)}
.footer-bottom{display:flex;align-items:center;justify-content:space-between;padding-top:28px;border-top:1px solid var(--border)}
.footer-bottom p{font-size:0.85rem;color:var(--text-muted)}
.footer-socials{display:flex;gap:10px}
.social-btn{
  width:36px;height:36px;border-radius:50%;background:rgba(34,197,94,0.08);
  border:1px solid var(--border);display:flex;align-items:center;justify-content:center;
  font-size:0.95rem;color:var(--text-muted);transition:all var(--transition);
}
.social-btn:hover{background:rgba(34,197,94,0.15);border-color:var(--border-bright);color:var(--green-primary)}

/* ============================================================
   ANIMATIONS — FADE IN ON SCROLL
   ============================================================ */
.fade-in{opacity:0;transform:translateY(30px);transition:opacity 0.7s ease,transform 0.7s ease}
.fade-in.visible{opacity:1;transform:translateY(0)}
.slide-left{opacity:0;transform:translateX(-30px);transition:opacity 0.7s ease,transform 0.7s ease}
.slide-left.visible{opacity:1;transform:translateX(0)}
.slide-right{opacity:0;transform:translateX(30px);transition:opacity 0.7s ease,transform 0.7s ease}
.slide-right.visible{opacity:1;transform:translateX(0)}

/* ============================================================
   TOAST NOTIFICATIONS
   ============================================================ */
.toast-container{position:fixed;bottom:90px;right:28px;z-index:950;display:flex;flex-direction:column;gap:10px}
.toast{
  background:var(--bg-card);border:1px solid var(--border);border-radius:var(--radius-sm);
  padding:12px 18px;font-size:0.88rem;min-width:220px;max-width:300px;
  box-shadow:var(--shadow-strong);backdrop-filter:blur(16px);
  display:flex;align-items:center;gap:10px;
  animation:toastIn 0.4s cubic-bezier(0.4,0,0.2,1);
}
.toast.removing{animation:toastOut 0.4s cubic-bezier(0.4,0,0.2,1) forwards}
@keyframes toastIn{from{opacity:0;transform:translateX(40px)}to{opacity:1;transform:translateX(0)}}
@keyframes toastOut{to{opacity:0;transform:translateX(40px)}}
.toast .toast-icon{font-size:1.1rem}
.toast-success .toast-icon::before{content:'✅'}
.toast-info .toast-icon::before{content:'ℹ️'}

/* ============================================================
   RESPONSIVE
   ============================================================ */
@media(max-width:1024px){
  .calc-layout,.dash-grid,.auth-layout{grid-template-columns:1fr}
  .hero-orb{display:none}
  .footer-grid{grid-template-columns:1fr 1fr}
  .dash-kpis{grid-template-columns:1fr 1fr}
  .admin-stats{grid-template-columns:1fr 1fr}
}
@media(max-width:768px){
  .nav-links,.nav-actions .btn{display:none}
  .hamburger{display:flex}
  .grid-2,.grid-3,.grid-4{grid-template-columns:1fr}
  .hero-stats{gap:20px}
  .chart-row{grid-template-columns:1fr}
  .tips-grid{grid-template-columns:1fr}
  .dash-kpis{grid-template-columns:1fr}
  .admin-stats{grid-template-columns:1fr 1fr}
  .footer-grid{grid-template-columns:1fr}
  .footer-bottom{flex-direction:column;gap:16px;text-align:center}
  .chatbot-panel{width:calc(100vw - 40px);right:20px}
  .section{padding:56px 0}
  .auth-layout{grid-template-columns:1fr}
}
@media(max-width:480px){
  .admin-stats{grid-template-columns:1fr}
  .hero-title{font-size:2.2rem}
}
</style>
</head>
<body>

<!-- ===== LOADER ===== -->
<div id="loader">
  <div class="loader-logo">🌿 EcoTrack</div>
  <div class="loader-ring"></div>
  <div class="loader-text">Calculating Earth's Pulse…</div>
</div>

<!-- ===== NAVBAR ===== -->
<nav id="navbar">
  <div class="container nav-inner">
    <a href="#hero" class="nav-logo">🌿 Eco<span>Track</span></a>
    <div class="nav-links">
      <a href="#hero">Home</a>
      <a href="#calculator">Calculator</a>
      <a href="#dashboard">Dashboard</a>
      <a href="#leaderboard">Leaderboard</a>
      <a href="#awareness">Awareness</a>
      <a href="#auth">Sign In</a>
    </div>
    <div class="nav-actions">
      <button class="theme-toggle" id="themeToggle" title="Toggle theme">🌙</button>
      <a href="#calculator" class="btn btn-primary btn-sm">Calculate Now</a>
      <button class="hamburger" id="hamburger" aria-label="Menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <a href="#hero" onclick="closeMobile()">Home</a>
  <a href="#calculator" onclick="closeMobile()">Calculator</a>
  <a href="#dashboard" onclick="closeMobile()">Dashboard</a>
  <a href="#leaderboard" onclick="closeMobile()">Leaderboard</a>
  <a href="#awareness" onclick="closeMobile()">Awareness</a>
  <a href="#auth" onclick="closeMobile()">Sign In / Register</a>
  <a href="#admin" onclick="closeMobile()">Admin Panel</a>
</div>

<!-- ===== HERO ===== -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="particles" id="particles"></div>
  <div class="container" style="position:relative;z-index:1;width:100%">
    <div class="hero-content">
      <div class="badge">🌍 Environmental Informatics Platform</div>
      <h1 class="hero-title">
        Know Your<br>
        <span class="accent">Carbon Footprint</span><br>
        Act for Earth
      </h1>
      <p class="hero-desc">
        EcoTrack empowers you to calculate, understand, and reduce your personal carbon emissions through intelligent data analysis and actionable eco-friendly recommendations.
      </p>
      <div class="hero-actions">
        <a href="#calculator" class="btn btn-primary">🧮 Calculate Now</a>
        <a href="#awareness" class="btn btn-outline">🌱 Learn More</a>
      </div>
      <div class="hero-stats">
        <div class="hero-stat">
          <span class="hero-stat-num" data-count="36">0</span><span class="hero-stat-num" style="font-size:1.2rem">B+</span>
          <span class="hero-stat-label">Tons CO₂/year global</span>
        </div>
        <div class="hero-stat">
          <span class="hero-stat-num" data-count="1.5">0</span><span class="hero-stat-num" style="font-size:1.2rem">°C</span>
          <span class="hero-stat-label">Temp rise since 1850</span>
        </div>
        <div class="hero-stat">
          <span class="hero-stat-num" data-count="4200">0</span><span class="hero-stat-num" style="font-size:1.2rem">+</span>
          <span class="hero-stat-label">Users tracking today</span>
        </div>
        <div class="hero-stat">
          <span class="hero-stat-num" data-count="78">0</span><span class="hero-stat-num" style="font-size:1.2rem">%</span>
          <span class="hero-stat-label">Reduction achievable</span>
        </div>
      </div>
    </div>
  </div>
  <div class="hero-orb">🌍</div>
  <div class="scroll-cue">
    <span>Scroll</span>
    <div class="scroll-arrow"></div>
  </div>
</section>

<!-- ===== TICKER ===== -->
<div class="ticker">
  <div class="ticker-inner" id="tickerInner"></div>
</div>

<!-- ===== AWARENESS SECTION ===== -->
<section class="section" id="awareness">
  <div class="container">
    <div class="badge fade-in">🔥 Climate Reality</div>
    <h2 class="section-title fade-in">Environmental <span style="color:var(--green-primary)">Awareness</span></h2>
    <p class="section-subtitle fade-in">Understanding the crisis is the first step toward meaningful action.</p>
    <div class="awareness-grid">
      <div class="awareness-card fade-in">
        <div class="awareness-icon">🌡️</div>
        <h3>Global Warming Crisis</h3>
        <p>The Earth's average temperature has risen by 1.2°C since pre-industrial times. Continued emissions could push us past 2°C by 2060, triggering catastrophic feedback loops.</p>
        <span class="awareness-stat">+1.2°C</span>
      </div>
      <div class="awareness-card fade-in" style="transition-delay:0.1s">
        <div class="awareness-icon">🌊</div>
        <h3>Sea Level Rise</h3>
        <p>Global sea levels are rising at 3.6mm per year. At current rates, coastal cities like Mumbai, Miami, and Shanghai face severe flooding by 2050, displacing hundreds of millions.</p>
        <span class="awareness-stat">3.6mm/yr</span>
      </div>
      <div class="awareness-card fade-in" style="transition-delay:0.2s">
        <div class="awareness-icon">🌪️</div>
        <h3>Extreme Weather Events</h3>
        <p>Climate change is intensifying hurricanes, wildfires, droughts, and floods. The frequency of extreme weather events has increased by 5x since 1970.</p>
        <span class="awareness-stat">5× ↑</span>
      </div>
      <div class="awareness-card fade-in" style="transition-delay:0.3s">
        <div class="awareness-icon">🐝</div>
        <h3>Biodiversity Loss</h3>
        <p>We are in the 6th mass extinction event. Species are disappearing 1,000 times faster than natural background rates, threatening entire ecosystems and food chains.</p>
        <span class="awareness-stat">1M Species</span>
      </div>
      <div class="awareness-card fade-in" style="transition-delay:0.4s">
        <div class="awareness-icon">🏭</div>
        <h3>Carbon Emissions</h3>
        <p>Burning fossil fuels releases 36+ billion tons of CO₂ annually. Transport accounts for 16%, buildings 17%, and agriculture 18.4% of global greenhouse gas emissions.</p>
        <span class="awareness-stat">36B Tons</span>
      </div>
      <div class="awareness-card fade-in" style="transition-delay:0.5s">
        <div class="awareness-icon">♻️</div>
        <h3>Circular Economy</h3>
        <p>Moving to a circular economy — reducing, reusing, and recycling — could cut global greenhouse gas emissions by 39%, equivalent to removing 4.5 billion cars from roads.</p>
        <span class="awareness-stat">-39% GHG</span>
      </div>
    </div>
  </div>
</section>

<!-- ===== CALCULATOR SECTION ===== -->
<section class="section" id="calculator">
  <div class="container">
    <div class="badge fade-in">🧮 Smart Calculator</div>
    <h2 class="section-title fade-in">Carbon Footprint <span style="color:var(--green-primary)">Calculator</span></h2>
    <p class="section-subtitle fade-in">Enter your daily activity details to get a precise estimate of your annual CO₂ emissions.</p>
    <div class="calc-layout">
      <!-- FORM -->
      <div class="calc-form-wrapper slide-left">
        <h3>📋 Activity Input</h3>
        <!-- Electricity -->
        <div class="form-group">
          <label>⚡ Monthly Electricity Consumption</label>
          <div class="input-group">
            <input type="number" class="form-control" id="electricity" placeholder="250" min="0">
            <span class="input-unit">kWh/mo</span>
          </div>
        </div>
        <!-- Vehicle -->
        <div class="form-group">
          <label>🚗 Daily Vehicle Travel Distance</label>
          <div class="input-group">
            <input type="number" class="form-control" id="vehicle" placeholder="30" min="0">
            <span class="input-unit">km/day</span>
          </div>
        </div>
        <!-- Fuel Type -->
        <div class="form-group">
          <label>⛽ Fuel Type</label>
          <select class="form-control" id="fuelType">
            <option value="petrol">Petrol / Gasoline</option>
            <option value="diesel">Diesel</option>
            <option value="cng">CNG (Natural Gas)</option>
            <option value="electric">Electric Vehicle</option>
            <option value="none">No Vehicle</option>
          </select>
        </div>
        <!-- LPG -->
        <div class="form-group">
          <label>🔥 Monthly LPG / Gas Cylinder Usage</label>
          <div class="input-group">
            <input type="number" class="form-control" id="lpg" placeholder="1" min="0" step="0.1">
            <span class="input-unit">cylinders</span>
          </div>
        </div>
        <!-- Flights -->
        <div class="form-group">
          <label>✈️ Annual Flight Distance</label>
          <div class="input-group">
            <input type="number" class="form-control" id="flights" placeholder="5000" min="0">
            <span class="input-unit">km/yr</span>
          </div>
        </div>
        <!-- Waste -->
        <div class="form-group">
          <label>🗑️ Weekly Waste Generation</label>
          <div class="input-group">
            <input type="number" class="form-control" id="waste" placeholder="5" min="0">
            <span class="input-unit">kg/wk</span>
          </div>
        </div>
        <!-- Diet -->
        <div class="form-group">
          <label>🥩 Diet Type</label>
          <select class="form-control" id="diet">
            <option value="meat_heavy">Heavy Meat Eater</option>
            <option value="meat_moderate" selected>Moderate Meat Eater</option>
            <option value="vegetarian">Vegetarian</option>
            <option value="vegan">Vegan</option>
          </select>
        </div>
        <div class="calc-btn-row">
          <button class="btn btn-primary" id="calcBtn" onclick="calculateFootprint()">🧮 Calculate Footprint</button>
          <button class="btn btn-outline" onclick="resetCalc()">↺ Reset</button>
        </div>
      </div>

      <!-- RESULTS -->
      <div class="results-panel slide-right">
        <div class="result-hero" id="resultHero">
          <div class="result-hero-label">Your Annual CO₂ Emissions</div>
          <div class="result-hero-num" id="resultNum">—</div>
          <div class="result-hero-unit" id="resultUnit">Enter your data and click Calculate</div>
          <div id="impactBadge"></div>
        </div>

        <div class="card">
          <h4 style="margin-bottom:18px;font-size:1rem">📊 Emissions Breakdown</h4>
          <div class="breakdown-list" id="breakdownList">
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">⚡ Electricity</span><span class="breakdown-value">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%" id="pb-electricity"></div></div>
            </div>
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">🚗 Transport</span><span class="breakdown-value" id="bv-transport">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%;background:linear-gradient(90deg,#0ea5e9,#3b82f6)" id="pb-transport"></div></div>
            </div>
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">🔥 LPG / Fuel</span><span class="breakdown-value" id="bv-lpg">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%;background:linear-gradient(90deg,#f59e0b,#fbbf24)" id="pb-lpg"></div></div>
            </div>
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">✈️ Aviation</span><span class="breakdown-value" id="bv-flights">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%;background:linear-gradient(90deg,#8b5cf6,#a78bfa)" id="pb-flights"></div></div>
            </div>
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">🗑️ Waste</span><span class="breakdown-value" id="bv-waste">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%;background:linear-gradient(90deg,#ef4444,#f87171)" id="pb-waste"></div></div>
            </div>
            <div class="breakdown-item">
              <div class="breakdown-header"><span class="breakdown-label">🥩 Diet</span><span class="breakdown-value" id="bv-diet">—</span></div>
              <div class="progress-bar"><div class="progress-fill" style="width:0%;background:linear-gradient(90deg,#14b8a6,#2dd4bf)" id="pb-diet"></div></div>
            </div>
          </div>
          <div style="margin-top:16px;text-align:center">
            <span id="bv-electricity" style="display:none"></span>
          </div>
        </div>

        <div class="chart-wrapper">
          <canvas id="pieChart"></canvas>
        </div>

        <button class="btn btn-outline" style="width:100%;justify-content:center" onclick="downloadReport()">📄 Download PDF Report</button>
      </div>
    </div>
  </div>
</section>

<!-- ===== SUGGESTIONS SECTION ===== -->
<section class="section" id="suggestions">
  <div class="container">
    <div class="badge fade-in">💡 Smart Recommendations</div>
    <h2 class="section-title fade-in">Eco-Friendly <span style="color:var(--green-primary)">Suggestions</span></h2>
    <p class="section-subtitle fade-in">Personalised actions to help you slash your carbon footprint — starting today.</p>
    <div class="suggestions-grid" id="suggestionsGrid">
      <!-- Populated by JS -->
    </div>
  </div>
</section>

<!-- ===== DATA VISUALIZATION ===== -->
<section class="section" id="visualization" style="background:var(--bg-secondary)">
  <div class="container">
    <div class="badge fade-in">📈 Data Insights</div>
    <h2 class="section-title fade-in">Emission <span style="color:var(--green-primary)">Visualisation</span></h2>
    <p class="section-subtitle fade-in">Interactive charts comparing your emissions against global and national averages.</p>
    <div class="chart-row fade-in">
      <div class="card">
        <h4 style="margin-bottom:16px">Monthly Trend Comparison</h4>
        <canvas id="barChart" height="220"></canvas>
      </div>
      <div class="card">
        <h4 style="margin-bottom:16px">vs. Global Averages</h4>
        <canvas id="compChart" height="220"></canvas>
      </div>
    </div>
  </div>
</section>

<!-- ===== DASHBOARD ===== -->
<section class="section" id="dashboard">
  <div class="container">
    <div class="badge fade-in">📊 Personal Dashboard</div>
    <h2 class="section-title fade-in">Your <span style="color:var(--green-primary)">Dashboard</span></h2>
    <p class="section-subtitle fade-in">Track your progress, compare months, and celebrate your eco victories.</p>
    <div class="dash-grid fade-in">
      <!-- Sidebar -->
      <div class="dash-sidebar">
        <div class="profile-card">
          <div class="profile-avatar">A</div>
          <div class="profile-name">Alex Sharma</div>
          <div class="profile-since">Member since Jan 2024</div>
          <div class="profile-badge">🌿 Eco Warrior</div>
        </div>
        <div class="card" style="padding:16px">
          <div class="dash-nav">
            <button class="dash-nav-item active">📊 Overview</button>
            <button class="dash-nav-item">📅 History</button>
            <button class="dash-nav-item">🏆 Badges</button>
            <button class="dash-nav-item">⚙️ Settings</button>
            <button class="dash-nav-item" onclick="showToast('Logging out…','info')">🚪 Log Out</button>
          </div>
        </div>
      </div>
      <!-- Main -->
      <div class="dash-main">
        <div class="dash-kpis">
          <div class="kpi-card">
            <div class="kpi-icon">🌿</div>
            <div class="kpi-value">4.2</div>
            <div class="kpi-label">Tons CO₂ / Year</div>
            <div class="kpi-change down">↓ 12% from last month</div>
          </div>
          <div class="kpi-card">
            <div class="kpi-icon">📅</div>
            <div class="kpi-value">12</div>
            <div class="kpi-label">Calculations Made</div>
            <div class="kpi-change down">↑ 3 this week</div>
          </div>
          <div class="kpi-card">
            <div class="kpi-icon">🌳</div>
            <div class="kpi-value">8.4</div>
            <div class="kpi-label">Trees to Offset</div>
            <div class="kpi-change up">Need 2 more</div>
          </div>
        </div>
        <div class="card">
          <h4 style="margin-bottom:16px">📜 Calculation History</h4>
          <table class="history-table">
            <thead>
              <tr>
                <th>Date</th>
                <th>CO₂ (tons/yr)</th>
                <th>Impact Level</th>
                <th>Change</th>
              </tr>
            </thead>
            <tbody id="historyTableBody"></tbody>
          </table>
        </div>
        <div class="chart-row">
          <div class="card">
            <h4 style="margin-bottom:14px">Monthly Emissions</h4>
            <canvas id="dashChart" height="180"></canvas>
          </div>
          <div class="card" style="display:flex;flex-direction:column;gap:12px">
            <h4>🏅 Eco Badges</h4>
            <div id="badgesGrid" style="display:grid;grid-template-columns:1fr 1fr;gap:10px"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== LEADERBOARD ===== -->
<section class="section" id="leaderboard" style="background:var(--bg-secondary)">
  <div class="container">
    <div class="badge fade-in">🏆 Community</div>
    <h2 class="section-title fade-in">Eco <span style="color:var(--green-primary)">Leaderboard</span></h2>
    <p class="section-subtitle fade-in">See how you stack up against other eco-warriors in the community. Lower is better!</p>
    <div class="leaderboard-list fade-in" id="leaderboardList"></div>
  </div>
</section>

<!-- ===== AUTH SECTION ===== -->
<section class="section" id="auth">
  <div class="container">
    <div class="auth-layout">
      <div class="auth-info slide-left">
        <div class="badge">🔐 Join EcoTrack</div>
        <h2>Track Your Journey<br><span style="color:var(--green-primary)">Save the Planet</span></h2>
        <p style="color:var(--text-secondary);margin-bottom:28px;line-height:1.7">Create your account to save calculation history, earn eco badges, join the leaderboard, and get personalised recommendations.</p>
        <div class="auth-feature">
          <div class="auth-feature-icon">📊</div>
          <p><strong>Track over time</strong> — Save every calculation and see your improvement month over month.</p>
        </div>
        <div class="auth-feature">
          <div class="auth-feature-icon">🏆</div>
          <p><strong>Earn badges</strong> — Unlock achievements as you reduce your carbon footprint.</p>
        </div>
        <div class="auth-feature">
          <div class="auth-feature-icon">📄</div>
          <p><strong>Download reports</strong> — Generate detailed PDF reports to share with friends or employers.</p>
        </div>
        <div class="auth-feature">
          <div class="auth-feature-icon">🤖</div>
          <p><strong>AI chatbot</strong> — Get 24/7 personalized eco tips from our embedded assistant.</p>
        </div>
      </div>
      <div class="auth-card slide-right">
        <div class="auth-tabs">
          <button class="auth-tab active" onclick="switchAuth('login')">Sign In</button>
          <button class="auth-tab" onclick="switchAuth('register')">Register</button>
        </div>
        <!-- Login -->
        <div class="auth-form active" id="loginForm">
          <div class="form-group">
            <label>Email Address</label>
            <input type="email" class="form-control" placeholder="you@example.com">
          </div>
          <div class="form-group">
            <label>Password</label>
            <input type="password" class="form-control" placeholder="••••••••" id="loginPass">
          </div>
          <div class="remember-row">
            <label><input type="checkbox"> Remember me</label>
            <a href="#">Forgot password?</a>
          </div>
          <button class="btn btn-primary" style="width:100%;justify-content:center" onclick="handleLogin()">Sign In →</button>
          <div style="text-align:center;margin-top:16px;font-size:0.85rem;color:var(--text-muted)">
            Or continue with
          </div>
          <div style="display:flex;gap:10px;margin-top:12px">
            <button class="btn btn-outline" style="flex:1;justify-content:center;font-size:0.88rem" onclick="showToast('Google OAuth coming soon!','info')">🔑 Google</button>
            <button class="btn btn-outline" style="flex:1;justify-content:center;font-size:0.88rem" onclick="showToast('GitHub OAuth coming soon!','info')">🐙 GitHub</button>
          </div>
        </div>
        <!-- Register -->
        <div class="auth-form" id="registerForm">
          <div class="grid-2" style="gap:12px">
            <div class="form-group" style="margin-bottom:0">
              <label>First Name</label>
              <input type="text" class="form-control" placeholder="Alex">
            </div>
            <div class="form-group" style="margin-bottom:0">
              <label>Last Name</label>
              <input type="text" class="form-control" placeholder="Sharma">
            </div>
          </div>
          <div class="form-group" style="margin-top:16px">
            <label>Email Address</label>
            <input type="email" class="form-control" placeholder="you@example.com">
          </div>
          <div class="form-group">
            <label>Password</label>
            <input type="password" class="form-control" id="regPass" placeholder="Min 8 characters" oninput="updateStrength()">
            <div class="password-strength"><div class="password-strength-fill" id="strengthBar"></div></div>
          </div>
          <div class="form-group">
            <label>Confirm Password</label>
            <input type="password" class="form-control" placeholder="Repeat password">
          </div>
          <div class="form-group">
            <label>Location (City)</label>
            <input type="text" class="form-control" placeholder="Mumbai, India">
          </div>
          <label style="display:flex;align-items:flex-start;gap:10px;font-size:0.85rem;color:var(--text-secondary);margin-bottom:20px;cursor:pointer">
            <input type="checkbox" style="margin-top:3px"> I agree to the Terms of Service and Privacy Policy
          </label>
          <button class="btn btn-primary" style="width:100%;justify-content:center" onclick="handleRegister()">Create Account 🌿</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== ADMIN PANEL ===== -->
<section class="section" id="admin" style="background:var(--bg-primary)">
  <div class="container">
    <div class="admin-header">
      <div>
        <div class="badge">⚙️ Admin Access</div>
        <h2 class="section-title" style="margin-bottom:0">Admin <span style="color:var(--green-primary)">Panel</span></h2>
      </div>
      <button class="btn btn-outline btn-sm" onclick="showToast('Admin session refreshed','info')">🔄 Refresh</button>
    </div>
    <div class="admin-stats">
      <div class="admin-stat-card fade-in">
        <div class="admin-stat-icon green">👤</div>
        <div class="admin-stat-info">
          <div class="admin-stat-num">4,218</div>
          <div class="admin-stat-label">Registered Users</div>
        </div>
      </div>
      <div class="admin-stat-card fade-in" style="transition-delay:0.1s">
        <div class="admin-stat-icon teal">🧮</div>
        <div class="admin-stat-info">
          <div class="admin-stat-num">31,490</div>
          <div class="admin-stat-label">Total Calculations</div>
        </div>
      </div>
      <div class="admin-stat-card fade-in" style="transition-delay:0.2s">
        <div class="admin-stat-icon blue">🌿</div>
        <div class="admin-stat-info">
          <div class="admin-stat-num">128k</div>
          <div class="admin-stat-label">Tons CO₂ Tracked</div>
        </div>
      </div>
      <div class="admin-stat-card fade-in" style="transition-delay:0.3s">
        <div class="admin-stat-icon amber">⚡</div>
        <div class="admin-stat-info">
          <div class="admin-stat-num">98.4%</div>
          <div class="admin-stat-label">Uptime This Month</div>
        </div>
      </div>
    </div>
    <div class="admin-table-section fade-in">
      <h3>👤 Registered Users</h3>
      <table class="users-table">
        <thead>
          <tr>
            <th>Name</th>
            <th>Email</th>
            <th>Location</th>
            <th>CO₂ (ton/yr)</th>
            <th>Status</th>
            <th>Joined</th>
          </tr>
        </thead>
        <tbody id="usersTableBody"></tbody>
      </table>
    </div>
    <div class="admin-table-section fade-in">
      <h3>💡 Environmental Tips Manager</h3>
      <div class="tips-grid" id="tipsGrid"></div>
      <button class="btn btn-outline btn-sm" style="margin-top:16px" onclick="showToast('Tip added successfully!','success')">+ Add New Tip</button>
    </div>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="nav-logo" style="font-size:1.6rem">🌿 Eco<span style="color:var(--text-primary)">Track</span></div>
        <p>An Environmental Informatics platform helping individuals and organizations understand, track, and reduce their carbon footprint through intelligent data analysis.</p>
      </div>
      <div class="footer-col">
        <h4>Platform</h4>
        <a href="#calculator">Calculator</a>
        <a href="#dashboard">Dashboard</a>
        <a href="#leaderboard">Leaderboard</a>
        <a href="#visualization">Analytics</a>
      </div>
      <div class="footer-col">
        <h4>Resources</h4>
        <a href="#awareness">Climate Facts</a>
        <a href="#suggestions">Eco Tips</a>
        <a href="#">Blog</a>
        <a href="#">Research</a>
      </div>
      <div class="footer-col">
        <h4>Company</h4>
        <a href="#">About Us</a>
        <a href="#">Privacy Policy</a>
        <a href="#">Terms of Service</a>
        <a href="#auth">Contact</a>
      </div>
    </div>
    <div class="footer-bottom">
      <p>© 2025 EcoTrack. Built with 💚 for a sustainable future.</p>
      <div class="footer-socials">
        <a class="social-btn" href="#" title="Twitter">𝕏</a>
        <a class="social-btn" href="#" title="LinkedIn">in</a>
        <a class="social-btn" href="#" title="GitHub">⌥</a>
        <a class="social-btn" href="#" title="Instagram">📷</a>
      </div>
    </div>
  </div>
</footer>

<!-- ===== CHATBOT ===== -->
<button class="chatbot-fab" onclick="toggleChatbot()" title="Eco Assistant">🤖</button>
<div class="chatbot-panel closed" id="chatbotPanel">
  <div class="chatbot-header">
    <div class="chatbot-title">
      <div class="chatbot-dot"></div>
      EcoBot — AI Assistant
    </div>
    <button class="chatbot-close" onclick="toggleChatbot()">✕</button>
  </div>
  <div class="chatbot-messages" id="chatMessages">
    <div class="msg bot">👋 Hi! I'm <strong>EcoBot</strong>, your personal environmental advisor.<br><br>Ask me about:<br>• Carbon footprint tips<br>• Climate facts<br>• How to reduce emissions<br>• Eco-friendly lifestyle</div>
  </div>
  <div class="chatbot-input-row">
    <input class="chatbot-input" id="chatInput" placeholder="Ask an eco question…" onkeydown="if(event.key==='Enter')sendChat()">
    <button class="chatbot-send" onclick="sendChat()">➤</button>
  </div>
</div>

<!-- ===== TOAST CONTAINER ===== -->
<div class="toast-container" id="toastContainer"></div>

<!-- ===== JAVASCRIPT ===== -->
<script>
/* ============================================================
   LOADER
   ============================================================ */
window.addEventListener('load', () => {
  setTimeout(() => {
    document.getElementById('loader').classList.add('hidden');
    initAnimations();
    initCharts();
    initParticles();
    populateLeaderboard();
    populateHistory();
    populateBadges();
    populateAdminUsers();
    populateTips();
    populateSuggestions(null); // default suggestions
    initTicker();
    animateCounters();
  }, 1400);
});

/* ============================================================
   THEME TOGGLE
   ============================================================ */
const themeToggle = document.getElementById('themeToggle');
themeToggle.addEventListener('click', () => {
  const html = document.documentElement;
  const isDark = html.getAttribute('data-theme') === 'dark';
  html.setAttribute('data-theme', isDark ? 'light' : 'dark');
  themeToggle.textContent = isDark ? '☀️' : '🌙';
  // Re-init charts for theme
  setTimeout(() => initCharts(), 100);
});

/* ============================================================
   NAVBAR SCROLL
   ============================================================ */
window.addEventListener('scroll', () => {
  document.getElementById('navbar').classList.toggle('scrolled', window.scrollY > 60);
});

/* ============================================================
   HAMBURGER
   ============================================================ */
document.getElementById('hamburger').addEventListener('click', () => {
  document.getElementById('mobileMenu').classList.toggle('open');
});
function closeMobile() { document.getElementById('mobileMenu').classList.remove('open'); }

/* ============================================================
   PARTICLES
   ============================================================ */
function initParticles() {
  const container = document.getElementById('particles');
  for (let i = 0; i < 18; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random() * 80 + 20;
    p.style.cssText = `
      width:${size}px;height:${size}px;
      left:${Math.random()*100}%;top:${Math.random()*100}%;
      --dur:${Math.random()*8+6}s;--delay:-${Math.random()*8}s;
    `;
    container.appendChild(p);
  }
}

/* ============================================================
   TICKER
   ============================================================ */
function initTicker() {
  const items = [
    '🌡️ 2024 was the hottest year on record',
    '🌊 Arctic ice shrinks by 13% per decade',
    '🏭 Energy sector causes 34% of global CO₂',
    '🚗 Transport adds 8B tons CO₂ annually',
    '🌳 18M hectares of forest lost each year',
    '♻️ Recycling saves 700M tons of CO₂/yr',
    '☀️ Solar power grew 33% in 2023',
    '🌿 Plant-based diet cuts food emissions by 70%',
  ];
  const double = [...items, ...items];
  document.getElementById('tickerInner').innerHTML =
    double.map(t => `<div class="ticker-item"><span class="dot">●</span>${t}</div>`).join('');
}

/* ============================================================
   COUNTER ANIMATION
   ============================================================ */
function animateCounters() {
  document.querySelectorAll('[data-count]').forEach(el => {
    const target = parseFloat(el.dataset.count);
    const isFloat = target % 1 !== 0;
    let current = 0;
    const step = target / 60;
    const interval = setInterval(() => {
      current = Math.min(current + step, target);
      el.textContent = isFloat ? current.toFixed(1) : Math.floor(current).toLocaleString();
      if (current >= target) clearInterval(interval);
    }, 25);
  });
}

/* ============================================================
   SCROLL ANIMATIONS
   ============================================================ */
function initAnimations() {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) { e.target.classList.add('visible'); }
    });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-in, .slide-left, .slide-right').forEach(el => observer.observe(el));
}

/* ============================================================
   EMISSION FACTORS (kg CO₂ per unit)
   ============================================================ */
const FACTORS = {
  electricity: 0.82,     // kg CO₂ per kWh (India grid average)
  vehicle: {
    petrol:   0.21,      // kg CO₂ per km
    diesel:   0.25,
    cng:      0.11,
    electric: 0.05,
    none:     0
  },
  lpg:   14.9,           // kg CO₂ per cylinder (14.2 kg LPG)
  flight: 0.255,         // kg CO₂ per km (economy class)
  waste:  0.52,          // kg CO₂ per kg waste
  diet: {
    meat_heavy:   3300,
    meat_moderate:2000,
    vegetarian:   1200,
    vegan:        800
  }
};

let lastResult = null;
let pieChartInstance = null;

function calculateFootprint() {
  const elec    = parseFloat(document.getElementById('electricity').value) || 0;
  const vehicle = parseFloat(document.getElementById('vehicle').value)     || 0;
  const fuel    = document.getElementById('fuelType').value;
  const lpg     = parseFloat(document.getElementById('lpg').value)         || 0;
  const flights  = parseFloat(document.getElementById('flights').value)    || 0;
  const waste   = parseFloat(document.getElementById('waste').value)       || 0;
  const diet    = document.getElementById('diet').value;

  // Annual emissions (kg CO₂)
  const co2Electricity = elec * 12 * FACTORS.electricity;
  const co2Transport   = vehicle * 365 * FACTORS.vehicle[fuel];
  const co2LPG         = lpg * 12 * FACTORS.lpg;
  const co2Flights     = flights * FACTORS.flight;
  const co2Waste       = waste * 52 * FACTORS.waste;
  const co2Diet        = FACTORS.diet[diet];

  const total = co2Electricity + co2Transport + co2LPG + co2Flights + co2Waste + co2Diet;
  const tons  = (total / 1000).toFixed(2);

  // Impact level
  let level, cls;
  if (total < 2000)      { level = '🌿 Low Impact';      cls = 'impact-low'; }
  else if (total < 5000) { level = '⚠️ Moderate Impact'; cls = 'impact-moderate'; }
  else if (total < 9000) { level = '🔥 High Impact';     cls = 'impact-high'; }
  else                   { level = '🚨 Critical Impact';  cls = 'impact-critical'; }

  // Update UI
  document.getElementById('resultNum').textContent = tons;
  document.getElementById('resultUnit').textContent = `tons CO₂/year  (${Math.round(total).toLocaleString()} kg/yr)`;
  document.getElementById('impactBadge').innerHTML = `<div class="impact-badge ${cls}">${level}</div>`;

  // Breakdown
  const breakdown = {
    electricity: co2Electricity,
    transport:   co2Transport,
    lpg:         co2LPG,
    flights:     co2Flights,
    waste:       co2Waste,
    diet:        co2Diet
  };

  const ids = ['electricity','transport','lpg','flights','waste','diet'];
  ids.forEach(id => {
    const val = breakdown[id];
    const pct = total > 0 ? (val / total * 100).toFixed(0) : 0;
    const valEl = document.getElementById(`bv-${id}`);
    const pbEl  = document.getElementById(`pb-${id}`);
    if (valEl) valEl.textContent = `${Math.round(val).toLocaleString()} kg`;
    if (pbEl)  pbEl.style.width  = pct + '%';
  });
  // electricity breakdown header
  document.querySelector('#breakdownList .breakdown-item .breakdown-header .breakdown-value').textContent =
    `${Math.round(co2Electricity).toLocaleString()} kg`;

  // Pie chart
  updatePieChart([co2Electricity, co2Transport, co2LPG, co2Flights, co2Waste, co2Diet]);

  // Save result
  lastResult = { total, tons, breakdown, level };
  saveToHistory(tons, level, cls);
  populateSuggestions(total);
  showToast(`Footprint calculated: ${tons} tons CO₂/yr`, 'success');
}

function resetCalc() {
  ['electricity','vehicle','lpg','flights','waste'].forEach(id => {
    const el = document.getElementById(id);
    if (el) el.value = '';
  });
  document.getElementById('resultNum').textContent = '—';
  document.getElementById('resultUnit').textContent = 'Enter your data and click Calculate';
  document.getElementById('impactBadge').innerHTML = '';
}

/* ============================================================
   CHARTS
   ============================================================ */
function getChartColors() {
  return {
    green: 'rgba(34,197,94,0.85)',
    teal:  'rgba(20,184,166,0.85)',
    blue:  'rgba(59,130,246,0.85)',
    amber: 'rgba(245,158,11,0.85)',
    red:   'rgba(239,68,68,0.85)',
    violet:'rgba(139,92,246,0.85)',
    gridColor: 'rgba(34,197,94,0.08)',
    textColor: getComputedStyle(document.documentElement).getPropertyValue('--text-secondary').trim() || '#86efac',
  };
}

let barChartInst, compChartInst, dashChartInst;

function initCharts() {
  const c = getChartColors();
  const font = { family: "'Satoshi', sans-serif", size: 11 };
  const defaultOpts = {
    responsive: true, maintainAspectRatio: true,
    plugins: { legend: { labels: { color: c.textColor, font, boxWidth: 12 } } },
    scales: {
      x: { ticks: { color: c.textColor, font }, grid: { color: c.gridColor } },
      y: { ticks: { color: c.textColor, font }, grid: { color: c.gridColor } }
    }
  };

  // Bar chart (monthly trend)
  const barCtx = document.getElementById('barChart');
  if (barChartInst) barChartInst.destroy();
  barChartInst = new Chart(barCtx, {
    type: 'bar',
    data: {
      labels: ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'],
      datasets: [
        {
          label: 'Your Emissions (kg)',
          data: [380,355,420,390,360,340,330,305,290,280,265,260],
          backgroundColor: c.green, borderRadius: 6
        },
        {
          label: 'India Avg (kg)',
          data: [480,480,480,480,480,480,480,480,480,480,480,480],
          backgroundColor: 'rgba(255,255,255,0.1)', borderRadius: 6
        }
      ]
    },
    options: defaultOpts
  });

  // Comparison chart
  const compCtx = document.getElementById('compChart');
  if (compChartInst) compChartInst.destroy();
  compChartInst = new Chart(compCtx, {
    type: 'bar',
    data: {
      labels: ['You','India Avg','World Avg','USA Avg','EU Avg'],
      datasets: [{
        label: 'Tons CO₂/year',
        data: [4.2, 1.9, 4.8, 14.5, 6.8],
        backgroundColor: [c.green, c.teal, c.blue, c.red, c.amber],
        borderRadius: 8
      }]
    },
    options: { ...defaultOpts, plugins: { ...defaultOpts.plugins, legend: { display: false } } }
  });

  // Dashboard chart
  const dashCtx = document.getElementById('dashChart');
  if (dashChartInst) dashChartInst.destroy();
  dashChartInst = new Chart(dashCtx, {
    type: 'line',
    data: {
      labels: ['Jan','Feb','Mar','Apr','May','Jun'],
      datasets: [{
        label: 'CO₂ (tons)',
        data: [5.1, 4.8, 4.6, 4.4, 4.3, 4.2],
        borderColor: c.green,
        backgroundColor: 'rgba(34,197,94,0.08)',
        fill: true, tension: 0.4,
        pointBackgroundColor: c.green, pointRadius: 4
      }]
    },
    options: { ...defaultOpts, scales: { ...defaultOpts.scales, y: { ...defaultOpts.scales.y, min: 3, max: 6 } } }
  });
}

function updatePieChart(data) {
  const ctx = document.getElementById('pieChart');
  if (pieChartInstance) pieChartInstance.destroy();
  const c = getChartColors();
  pieChartInstance = new Chart(ctx, {
    type: 'doughnut',
    data: {
      labels: ['Electricity','Transport','LPG','Aviation','Waste','Diet'],
      datasets: [{
        data,
        backgroundColor: [c.green, c.blue, c.amber, c.violet, c.red, c.teal],
        borderWidth: 2,
        borderColor: 'rgba(0,0,0,0.3)',
        hoverOffset: 8
      }]
    },
    options: {
      responsive: true, maintainAspectRatio: true,
      cutout: '60%',
      plugins: {
        legend: {
          position: 'bottom',
          labels: { color: c.textColor, font: { family: "'Satoshi',sans-serif", size: 11 }, boxWidth: 12, padding: 14 }
        }
      }
    }
  });
}

/* ============================================================
   SUGGESTIONS
   ============================================================ */
const ALL_SUGGESTIONS = [
  { icon:'🚌', title:'Use Public Transport', desc:'Switch from private car to bus or metro for daily commutes. Saves up to 2.4 tons CO₂/year.', impact:'High Impact', threshold:3000 },
  { icon:'💡', title:'Switch to LED Bulbs', desc:'LED bulbs use 75% less energy than incandescent bulbs and last 25× longer.', impact:'Medium Impact', threshold:0 },
  { icon:'☀️', title:'Install Solar Panels', desc:'Rooftop solar can eliminate up to 90% of your electricity-related emissions.', impact:'Very High Impact', threshold:2000 },
  { icon:'🌱', title:'Plant More Trees', desc:'A single tree absorbs ~22 kg CO₂/year. Plant trees or support reforestation projects.', impact:'Medium Impact', threshold:0 },
  { icon:'♻️', title:'Reduce & Recycle Waste', desc:'Composting organic waste and recycling can cut waste emissions by up to 40%.', impact:'Medium Impact', threshold:1000 },
  { icon:'✈️', title:'Reduce Air Travel', desc:'One transatlantic flight emits more CO₂ than a month of driving. Consider alternatives.', impact:'High Impact', threshold:4000 },
  { icon:'🥦', title:'Adopt a Plant-Based Diet', desc:'Switching to vegetarian diet cuts food-related emissions by 40%. Even one meat-free day helps.', impact:'High Impact', threshold:0 },
  { icon:'🌡️', title:'Smart Thermostat', desc:'Adjusting your home temperature by 2°C reduces heating/cooling energy use by 10-15%.', impact:'Medium Impact', threshold:0 },
  { icon:'🚰', title:'Reduce Water Heating', desc:'Hot water accounts for ~18% of home energy use. Shorter showers and lower heater temps help.', impact:'Low Impact', threshold:0 },
  { icon:'🛒', title:'Buy Local & Seasonal', desc:'Local produce has 50× less transport emissions. Shop at farmers markets when possible.', impact:'Medium Impact', threshold:0 },
  { icon:'🔋', title:'Electric Vehicle Switch', desc:'EVs produce 3× less lifecycle CO₂ than petrol cars, especially with renewable electricity.', impact:'Very High Impact', threshold:5000 },
  { icon:'🏠', title:'Insulate Your Home', desc:'Proper insulation can cut heating and cooling costs by 30% and reduce emissions significantly.', impact:'High Impact', threshold:2500 },
];

function populateSuggestions(totalEmissions) {
  const grid = document.getElementById('suggestionsGrid');
  let shown = totalEmissions === null
    ? ALL_SUGGESTIONS.slice(0, 8)
    : ALL_SUGGESTIONS.filter(s => s.threshold <= totalEmissions || totalEmissions > 3000).slice(0, 9);

  grid.innerHTML = shown.map(s => `
    <div class="suggestion-card fade-in visible">
      <div class="suggestion-icon">${s.icon}</div>
      <h4>${s.title}</h4>
      <p>${s.desc}</p>
      <span class="suggestion-impact">${s.impact}</span>
    </div>
  `).join('');
}

/* ============================================================
   LEADERBOARD
   ============================================================ */
const LB_DATA = [
  { name:'Priya Patel',    loc:'Pune, IN',   co2:1.2, badge:'🌳 Tree Hugger',   color:'#22c55e' },
  { name:'Marco Rossi',    loc:'Milan, IT',  co2:1.8, badge:'⚡ Solar Star',     color:'#14b8a6' },
  { name:'Yuki Tanaka',    loc:'Tokyo, JP',  co2:2.1, badge:'🚲 Green Commuter', color:'#3b82f6' },
  { name:'Emma Wilson',    loc:'London, UK', co2:2.4, badge:'♻️ Zero Waster',    color:'#f59e0b' },
  { name:'Carlos García',  loc:'Madrid, ES', co2:2.7, badge:'🌱 Eco Starter',    color:'#8b5cf6' },
  { name:'Amira Hassan',   loc:'Cairo, EG',  co2:3.0, badge:'☀️ Solar Adopter',  color:'#ef4444' },
  { name:'Alex Sharma',    loc:'Mumbai, IN', co2:4.2, badge:'📊 Data Tracker',   color:'#06b6d4' },
];

function populateLeaderboard() {
  document.getElementById('leaderboardList').innerHTML = LB_DATA.map((u, i) => `
    <div class="lb-item">
      <div class="lb-rank">${i + 1}</div>
      <div class="lb-avatar" style="background:${u.color}">${u.name[0]}</div>
      <div class="lb-info">
        <div class="lb-name">${u.name}</div>
        <div class="lb-detail">📍 ${u.loc}</div>
        <span class="lb-badge">${u.badge}</span>
      </div>
      <div class="lb-score">
        <div class="lb-co2">${u.co2}</div>
        <div class="lb-co2-label">tons CO₂/yr</div>
      </div>
    </div>
  `).join('');
}

/* ============================================================
   HISTORY
   ============================================================ */
let historyData = [
  { date:'Jun 2025', co2:4.2, level:'Moderate', cls:'impact-moderate' },
  { date:'May 2025', co2:4.8, level:'Moderate', cls:'impact-moderate' },
  { date:'Apr 2025', co2:5.2, level:'High',     cls:'impact-high' },
  { date:'Mar 2025', co2:5.6, level:'High',     cls:'impact-high' },
  { date:'Feb 2025', co2:5.1, level:'High',     cls:'impact-high' },
];

function populateHistory() {
  document.getElementById('historyTableBody').innerHTML = historyData.map((h, i) => {
    const prev = historyData[i + 1];
    const change = prev ? ((h.co2 - prev.co2) / prev.co2 * 100).toFixed(1) : '—';
    const arrow = change !== '—' ? (parseFloat(change) < 0 ? '↓' : '↑') : '';
    const col = change !== '—' ? (parseFloat(change) < 0 ? 'var(--green-primary)' : '#f87171') : '';
    return `
      <tr>
        <td>${h.date}</td>
        <td><strong>${h.co2}</strong> ton/yr</td>
        <td><span class="history-table impact-pill ${h.cls}">${h.level}</span></td>
        <td style="color:${col};font-weight:600">${arrow} ${change !== '—' ? Math.abs(change) + '%' : '—'}</td>
      </tr>
    `;
  }).join('');
}

function saveToHistory(tons, level, cls) {
  const now = new Date().toLocaleDateString('en-US', { month:'short', year:'numeric' });
  historyData.unshift({ date: now, co2: parseFloat(tons), level: level.replace(/[^a-zA-Z\s]/g, '').trim(), cls });
  historyData = historyData.slice(0, 8);
  populateHistory();
}

/* ============================================================
   BADGES
   ============================================================ */
const BADGES = [
  { icon:'🌿', name:'First Step', earned:true },
  { icon:'🌳', name:'Tree Hugger', earned:true },
  { icon:'☀️', name:'Solar Star', earned:false },
  { icon:'🚲', name:'Green Commuter', earned:true },
  { icon:'♻️', name:'Zero Waster', earned:false },
  { icon:'🌊', name:'Ocean Guard', earned:false },
];
function populateBadges() {
  document.getElementById('badgesGrid').innerHTML = BADGES.map(b => `
    <div style="background:${b.earned ? 'rgba(34,197,94,0.1)' : 'rgba(255,255,255,0.04)'};border:1px solid ${b.earned ? 'var(--border-bright)' : 'var(--border)'};border-radius:10px;padding:12px;text-align:center;opacity:${b.earned ? 1 : 0.4}">
      <div style="font-size:1.5rem">${b.icon}</div>
      <div style="font-size:0.75rem;font-weight:600;color:${b.earned ? 'var(--text-primary)' : 'var(--text-muted)'};margin-top:4px">${b.name}</div>
    </div>
  `).join('');
}

/* ============================================================
   ADMIN DATA
   ============================================================ */
const ADMIN_USERS = [
  { name:'Priya Patel',  email:'priya@example.com',  loc:'Pune, IN',   co2:1.2, status:'active',   joined:'Jan 2024' },
  { name:'Marco Rossi',  email:'marco@example.com',  loc:'Milan, IT',  co2:1.8, status:'active',   joined:'Feb 2024' },
  { name:'Yuki Tanaka',  email:'yuki@example.com',   loc:'Tokyo, JP',  co2:2.1, status:'active',   joined:'Mar 2024' },
  { name:'Emma Wilson',  email:'emma@example.com',   loc:'London, UK', co2:2.4, status:'inactive', joined:'Nov 2023' },
  { name:'Alex Sharma',  email:'alex@example.com',   loc:'Mumbai, IN', co2:4.2, status:'active',   joined:'Jan 2024' },
];
function populateAdminUsers() {
  document.getElementById('usersTableBody').innerHTML = ADMIN_USERS.map(u => `
    <tr>
      <td><strong>${u.name}</strong></td>
      <td>${u.email}</td>
      <td>${u.loc}</td>
      <td>${u.co2} ton/yr</td>
      <td><span class="user-dot ${u.status}"></span>${u.status}</td>
      <td>${u.joined}</td>
    </tr>
  `).join('');
}

const ADMIN_TIPS = [
  '🌿 Plant trees to offset carbon',
  '💡 Use LED lighting everywhere',
  '🚰 Fix leaking faucets to save water',
  '☀️ Install solar panels for clean energy',
  '♻️ Compost kitchen waste',
  '🚌 Take public transport daily',
  '🥦 Eat more plant-based meals',
  '🔋 Use rechargeable batteries',
];
function populateTips() {
  document.getElementById('tipsGrid').innerHTML = ADMIN_TIPS.map(t => `
    <div class="tip-item">
      <span class="emoji">${t.split(' ')[0]}</span>
      <span>${t.split(' ').slice(1).join(' ')}</span>
      <div class="tip-actions">
        <button class="icon-btn" onclick="showToast('Tip edited!','info')">✏️</button>
        <button class="icon-btn" onclick="showToast('Tip deleted!','info')">🗑️</button>
      </div>
    </div>
  `).join('');
}

/* ============================================================
   AUTH
   ============================================================ */
function switchAuth(tab) {
  document.querySelectorAll('.auth-tab').forEach((t, i) => {
    t.classList.toggle('active', (i === 0 && tab === 'login') || (i === 1 && tab === 'register'));
  });
  document.getElementById('loginForm').classList.toggle('active', tab === 'login');
  document.getElementById('registerForm').classList.toggle('active', tab === 'register');
}
function handleLogin() {
  showToast('Welcome back, Alex! 🌿', 'success');
}
function handleRegister() {
  showToast('Account created! Check your email 📧', 'success');
}
function updateStrength() {
  const pass = document.getElementById('regPass').value;
  const bar  = document.getElementById('strengthBar');
  let score = 0;
  if (pass.length >= 8) score++;
  if (/[A-Z]/.test(pass))  score++;
  if (/[0-9]/.test(pass))  score++;
  if (/[^A-Za-z0-9]/.test(pass)) score++;
  const pct = score * 25;
  const colors = ['', '#ef4444', '#f59e0b', '#22c55e', '#14b8a6'];
  bar.style.width  = pct + '%';
  bar.style.background = colors[score] || 'transparent';
}

/* ============================================================
   CHATBOT (AI-powered via Anthropic API)
   ============================================================ */
let chatbotOpen = false;
let chatHistory = [];

function toggleChatbot() {
  chatbotOpen = !chatbotOpen;
  document.getElementById('chatbotPanel').classList.toggle('closed', !chatbotOpen);
}

async function sendChat() {
  const input = document.getElementById('chatInput');
  const msg   = input.value.trim();
  if (!msg) return;
  input.value = '';
  appendMsg(msg, 'user');
  chatHistory.push({ role: 'user', content: msg });

  const typing = appendMsg('…', 'bot');

  try {
    const res = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: 'claude-sonnet-4-20250514',
        max_tokens: 1000,
        system: `You are EcoBot, a friendly and knowledgeable environmental AI assistant embedded in the EcoTrack carbon footprint calculator platform. 
        You help users understand climate change, reduce their carbon footprint, and live more sustainably.
        Keep responses concise (2-4 sentences), practical, and encouraging. Use emojis sparingly. 
        Focus on actionable tips, emission facts, and positive reinforcement.`,
        messages: chatHistory
      })
    });
    const data = await res.json();
    const reply = data.content?.find(c => c.type === 'text')?.text || 'Sorry, I couldn\'t process that. Please try again!';
    typing.remove();
    appendMsg(reply, 'bot');
    chatHistory.push({ role: 'assistant', content: reply });
  } catch(e) {
    typing.remove();
    const fallbacks = [
      '🌿 Great question! Reducing your car journeys by just 10% can cut transport emissions significantly.',
      '💡 Switching all bulbs to LEDs is one of the easiest wins — saves up to 75% lighting energy.',
      '☀️ Solar panels typically pay back their carbon cost in 1-4 years and last 25+ years!',
      '🥦 Going meat-free just once a week saves ~350 kg CO₂ per person per year.',
    ];
    appendMsg(fallbacks[Math.floor(Math.random() * fallbacks.length)], 'bot');
  }
}

function appendMsg(text, type) {
  const msgs = document.getElementById('chatMessages');
  const div  = document.createElement('div');
  div.className = `msg ${type}`;
  div.innerHTML = text;
  msgs.appendChild(div);
  msgs.scrollTop = msgs.scrollHeight;
  return div;
}

/* ============================================================
   DOWNLOAD REPORT
   ============================================================ */
function downloadReport() {
  if (!lastResult) {
    showToast('Please calculate your footprint first!', 'info');
    return;
  }
  const content = `
ECOTRACK — CARBON FOOTPRINT REPORT
====================================
Date: ${new Date().toLocaleDateString('en-IN', { dateStyle: 'full' })}

ANNUAL EMISSIONS SUMMARY
Total CO₂: ${lastResult.tons} tons/year (${Math.round(lastResult.total).toLocaleString()} kg/year)
Impact Level: ${lastResult.level}

BREAKDOWN
-----------
Electricity:  ${Math.round(lastResult.breakdown.electricity).toLocaleString()} kg CO₂/year
Transport:    ${Math.round(lastResult.breakdown.transport).toLocaleString()} kg CO₂/year
LPG / Gas:    ${Math.round(lastResult.breakdown.lpg).toLocaleString()} kg CO₂/year
Aviation:     ${Math.round(lastResult.breakdown.flights).toLocaleString()} kg CO₂/year
Waste:        ${Math.round(lastResult.breakdown.waste).toLocaleString()} kg CO₂/year
Diet:         ${Math.round(lastResult.breakdown.diet).toLocaleString()} kg CO₂/year

COMPARISON
-----------
Your footprint:   ${lastResult.tons} tons/year
India Average:    1.9 tons/year
World Average:    4.8 tons/year
USA Average:      14.5 tons/year

TOP RECOMMENDATIONS
-------------------
1. Switch to public transport or electric vehicle
2. Install rooftop solar panels
3. Reduce meat consumption
4. Compost waste and recycle
5. Use energy-efficient appliances

Generated by EcoTrack — Track. Reduce. Thrive.
https://ecotrack.earth
  `.trim();
  const blob = new Blob([content], { type: 'text/plain' });
  const url  = URL.createObjectURL(blob);
  const a    = document.createElement('a');
  a.href     = url;
  a.download = `EcoTrack_Report_${new Date().toISOString().split('T')[0]}.txt`;
  a.click();
  URL.revokeObjectURL(url);
  showToast('Report downloaded! 📄', 'success');
}

/* ============================================================
   TOAST
   ============================================================ */
function showToast(message, type = 'info') {
  const container = document.getElementById('toastContainer');
  const toast = document.createElement('div');
  toast.className = `toast toast-${type}`;
  toast.innerHTML = `<span class="toast-icon"></span>${message}`;
  container.appendChild(toast);
  setTimeout(() => {
    toast.classList.add('removing');
    setTimeout(() => toast.remove(), 400);
  }, 3200);
}
</script>
</body>
</html>
