<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/><meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>OT SecureOps — AI-Driven IR Platform</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
/*═══ RESET ═══*/
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%;overflow:hidden;}

/*═══ TOKENS ═══*/
:root{
  --bg:#05080f; --s1:#0b0f1c; --s2:#111827; --s3:#1a2235; --s4:#212d42;
  --b1:#1e2d42; --b2:#263550; --b3:#2f4060;
  --txt:#cdd9ee; --txt2:#8498b5; --txt3:#4a637a; --txt4:#2d4055;
  --ok:#00d97a; --warn:#ffb31a; --crit:#ff3055; --info:#3d8fff; --purple:#a855f7;
  --t1:#ff3055; --t2:#ff7a1a; --t3:#c8a000;
  --phase-prepare:#3d8fff; --phase-detect:#ffe033; --phase-analyze:#ff9020;
  --phase-contain:#ff3055; --phase-eradicate:#a855f7; --phase-recover:#00d97a; --phase-post:#66aaff;
  --radius:5px; --font-mono:'IBM Plex Mono',monospace; --font-ui:'Inter',sans-serif; --font-display:'Syne',sans-serif;
}

body{font-family:var(--font-ui);background:var(--bg);color:var(--txt);display:flex;flex-direction:column;}

/* scanlines */
body::after{content:'';position:fixed;inset:0;background:repeating-linear-gradient(0deg,transparent,transparent 3px,rgba(0,0,0,.06) 3px,rgba(0,0,0,.06) 4px);pointer-events:none;z-index:9999;}

/*═══ TOPBAR ═══*/
#topbar{
  height:48px;flex-shrink:0;
  display:flex;align-items:center;justify-content:space-between;
  padding:0 20px;
  background:var(--s1);border-bottom:1px solid var(--b1);
  position:relative;z-index:200;
}
.tb-logo{font-family:var(--font-display);font-size:1rem;font-weight:800;letter-spacing:.05em;color:var(--txt);}
.tb-logo span{color:var(--crit);}
.tb-logo small{color:var(--ok);font-size:.7rem;font-weight:400;margin-left:6px;}

.tb-tabs{display:flex;gap:2px;height:100%;}
.tab-btn{
  font-family:var(--font-ui);font-size:.76rem;font-weight:500;
  padding:0 18px;height:100%;border:none;cursor:pointer;
  background:transparent;color:var(--txt3);
  border-bottom:2px solid transparent;
  transition:all .2s;letter-spacing:.02em;
}
.tab-btn:hover{color:var(--txt2);background:rgba(255,255,255,.03);}
.tab-btn.active{color:var(--txt);border-bottom-color:var(--info);}
.tab-btn .tab-badge{
  display:inline-block;margin-left:5px;
  background:var(--crit);color:#fff;
  font-size:.6rem;font-weight:700;
  padding:1px 5px;border-radius:8px;
  animation:badgepulse .9s infinite;
}
@keyframes badgepulse{0%,100%{opacity:1}50%{opacity:.5}}

.tb-right{display:flex;align-items:center;gap:12px;font-size:.72rem;color:var(--txt3);}
.tb-pill{padding:3px 10px;border-radius:3px;border:1px solid;font-size:.65rem;font-weight:600;letter-spacing:.08em;font-family:var(--font-mono);}
.pill-ok{border-color:var(--ok);color:var(--ok);}
.pill-warn{border-color:var(--warn);color:var(--warn);}
.pill-crit{border-color:var(--crit);color:var(--crit);animation:badgepulse .8s infinite;}
.live-dot{width:7px;height:7px;border-radius:50%;background:var(--ok);box-shadow:0 0 6px var(--ok);animation:livep 1.6s infinite;flex-shrink:0;}
@keyframes livep{0%,100%{opacity:1}50%{opacity:.1}}

/*═══ PAGES ═══*/
#pages{flex:1;overflow:hidden;position:relative;}
.page{display:none;height:100%;overflow:hidden;}
.page.active{display:flex;flex-direction:column;}

/*═══ SHARED CARD ═══*/
.card{background:var(--s2);border:1px solid var(--b1);border-radius:var(--radius);padding:14px;}
.card-title{font-size:.65rem;font-weight:600;letter-spacing:.16em;color:var(--txt3);text-transform:uppercase;margin-bottom:10px;font-family:var(--font-mono);}
.card-title span{color:var(--info);}

/*═══ SCROLLABLE AREA ═══*/
.scroll{overflow-y:auto;}
.scroll::-webkit-scrollbar{width:4px;}
.scroll::-webkit-scrollbar-thumb{background:var(--b2);border-radius:2px;}

/*═══ GRID HELPERS ═══*/
.g2{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px;}
.g4{display:grid;grid-template-columns:1fr 1fr 1fr 1fr;gap:10px;}

/*═══ METRIC TILE ═══*/
.metric-tile{
  background:var(--s2);border:1px solid var(--b1);border-radius:var(--radius);
  padding:12px 14px;position:relative;overflow:hidden;
}
.metric-tile::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:var(--mt-color,var(--b2));}
.mt-label{font-size:.65rem;color:var(--txt3);letter-spacing:.12em;text-transform:uppercase;font-family:var(--font-mono);margin-bottom:4px;}
.mt-value{font-size:1.6rem;font-weight:700;font-family:var(--font-display);line-height:1;color:var(--mt-color,var(--txt));}
.mt-sub{font-size:.7rem;color:var(--txt3);margin-top:4px;}
.mt-trend{font-size:.68rem;margin-top:3px;}
.mt-trend.up{color:var(--ok);}
.mt-trend.down{color:var(--crit);}

/*═══ BUTTONS ═══*/
.btn{
  font-family:var(--font-ui);font-size:.74rem;font-weight:600;
  padding:7px 14px;border-radius:var(--radius);border:1px solid;
  cursor:pointer;transition:all .15s;letter-spacing:.03em;
  white-space:nowrap;
}
.btn-primary{background:rgba(61,143,255,.12);border-color:var(--info);color:var(--info);}
.btn-primary:hover{background:rgba(61,143,255,.22);}
.btn-danger{background:rgba(255,48,85,.1);border-color:var(--crit);color:var(--crit);}
.btn-danger:hover{background:rgba(255,48,85,.2);}
.btn-success{background:rgba(0,217,122,.1);border-color:var(--ok);color:var(--ok);}
.btn-success:hover{background:rgba(0,217,122,.2);}
.btn-warn{background:rgba(255,179,26,.1);border-color:var(--warn);color:var(--warn);}
.btn-warn:hover{background:rgba(255,179,26,.2);}
.btn-ghost{background:rgba(255,255,255,.04);border-color:var(--b2);color:var(--txt2);}
.btn-ghost:hover{background:rgba(255,255,255,.08);}
.btn:disabled{opacity:.3;cursor:not-allowed;}
.btn-sm{font-size:.68rem;padding:4px 10px;}
.btn-xs{font-size:.62rem;padding:3px 8px;}

/*═══ BADGE ═══*/
.badge{display:inline-block;font-size:.6rem;font-weight:700;padding:2px 6px;border-radius:3px;font-family:var(--font-mono);letter-spacing:.06em;}
.badge-tp{background:rgba(255,48,85,.15);color:var(--crit);}
.badge-fp{background:rgba(255,179,26,.12);color:var(--warn);}
.badge-pending{background:rgba(61,143,255,.12);color:var(--info);}
.badge-ok{background:rgba(0,217,122,.1);color:var(--ok);}
.badge-closed{background:rgba(74,99,122,.2);color:var(--txt3);}
.badge-t1{background:rgba(255,48,85,.15);color:var(--t1);}
.badge-t2{background:rgba(255,122,26,.12);color:var(--t2);}
.badge-t3{background:rgba(200,160,0,.12);color:var(--t3);}

/*═══ TABLE ═══*/
.tbl{width:100%;border-collapse:collapse;font-size:.78rem;}
.tbl th{font-size:.62rem;font-weight:600;letter-spacing:.1em;color:var(--txt3);text-transform:uppercase;padding:7px 10px;border-bottom:1px solid var(--b1);text-align:left;font-family:var(--font-mono);white-space:nowrap;}
.tbl td{padding:8px 10px;border-bottom:1px solid rgba(255,255,255,.04);vertical-align:middle;}
.tbl tr:hover td{background:rgba(255,255,255,.02);}
.tbl tr:last-child td{border-bottom:none;}

/*═══ PROGRESS BAR ═══*/
.pbar-wrap{background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden;height:5px;}
.pbar-fill{height:100%;border-radius:3px;transition:width .5s ease;}

/*═══ ALERT ITEM ═══*/
.alert-item{
  display:flex;gap:10px;padding:10px 12px;
  border-bottom:1px solid rgba(255,255,255,.04);
  transition:background .15s;
  animation:alertin .3s ease;
}
@keyframes alertin{from{opacity:0;transform:translateX(-8px)}to{opacity:1;transform:none}}
.alert-item:hover{background:rgba(255,255,255,.02);}
.alert-item.pending{border-left:3px solid var(--info);}
.alert-item.tp{border-left:3px solid var(--crit);}
.alert-item.fp{border-left:3px solid var(--warn);}
.alert-item.closed{border-left:3px solid var(--txt4);opacity:.6;}
.ai-dot{width:9px;height:9px;border-radius:50%;flex-shrink:0;margin-top:4px;}

/*═══ PHASE CHIP ═══*/
.phase-chip{
  display:inline-flex;align-items:center;gap:4px;
  font-size:.62rem;font-family:var(--font-mono);font-weight:600;letter-spacing:.07em;
  padding:2px 7px;border-radius:3px;
}

/*═══ TOOLTIP-LIKE INFO ═══*/
.info-box{
  background:rgba(61,143,255,.07);border:1px solid rgba(61,143,255,.2);
  border-radius:var(--radius);padding:8px 10px;
  font-size:.75rem;color:var(--txt2);line-height:1.5;
}
.info-box.warn{background:rgba(255,179,26,.07);border-color:rgba(255,179,26,.2);}
.info-box.ok{background:rgba(0,217,122,.06);border-color:rgba(0,217,122,.2);}
.info-box.crit{background:rgba(255,48,85,.07);border-color:rgba(255,48,85,.2);}

/*═══ DIVIDER ═══*/
.divider{border:none;border-top:1px solid var(--b1);margin:10px 0;}

/*═══ FORM ELEMENTS ═══*/
select,input[type=text],input[type=number]{
  background:var(--s3);border:1px solid var(--b2);border-radius:var(--radius);
  color:var(--txt);font-family:var(--font-ui);font-size:.78rem;
  padding:6px 10px;width:100%;
}
select:focus,input:focus{outline:none;border-color:var(--info);}
label{font-size:.72rem;color:var(--txt2);display:block;margin-bottom:4px;}

/*═══════════════════════════════════
  PAGE 1 — SOC DASHBOARD
═══════════════════════════════════*/
#page-soc{
  display:none;flex-direction:column;
}
#page-soc.active{display:flex;}

#soc-layout{
  flex:1;overflow:hidden;
  display:grid;
  grid-template-columns:1fr 320px;
  grid-template-rows:auto 1fr;
  gap:0;
}

#soc-metrics-bar{
  grid-column:1/-1;
  display:flex;gap:10px;padding:12px;
  border-bottom:1px solid var(--b1);
  background:var(--s1);flex-shrink:0;
}
#soc-metrics-bar .metric-tile{flex:1;padding:10px 12px;}

#soc-main{display:flex;flex-direction:column;border-right:1px solid var(--b1);overflow:hidden;}
#soc-alert-toolbar{
  display:flex;align-items:center;gap:10px;padding:10px 12px;
  border-bottom:1px solid var(--b1);flex-shrink:0;flex-wrap:wrap;
}
#soc-alert-feed{flex:1;overflow-y:auto;}

#soc-side{display:flex;flex-direction:column;overflow:hidden;gap:0;}
#soc-charts{flex:1;overflow-y:auto;padding:12px;display:flex;flex-direction:column;gap:10px;}

/*═══════════════════════════════════
  PAGE 2 — IR LIFECYCLE
═══════════════════════════════════*/
#page-ir{display:none;}
#page-ir.active{display:flex;}

#ir-layout{
  flex:1;overflow:hidden;
  display:grid;
  grid-template-columns:240px 1fr 290px;
}

/* left threat list */
#ir-left{border-right:1px solid var(--b1);display:flex;flex-direction:column;overflow:hidden;background:var(--s1);}
#ir-threat-list{flex:1;overflow-y:auto;}
.ir-threat-item{
  padding:9px 12px;border-bottom:1px solid var(--b1);cursor:pointer;
  position:relative;overflow:hidden;transition:background .15s;
}
.ir-threat-item::before{content:'';position:absolute;left:0;top:0;bottom:0;width:3px;background:var(--tc,var(--txt3));}
.ir-threat-item:hover{background:rgba(255,255,255,.03);}
.ir-threat-item.selected{background:rgba(255,255,255,.05);}
.ir-threat-item.firing{animation:irf .7s infinite;}
@keyframes irf{0%,100%{background:rgba(255,48,85,.05)}50%{background:rgba(255,48,85,.1)}}
.iti-rank{font-size:.6rem;color:var(--tc,var(--txt3));font-family:var(--font-mono);font-weight:600;}
.iti-name{font-size:.8rem;font-weight:600;margin:2px 0;}
.iti-meta{display:flex;gap:6px;align-items:center;flex-wrap:wrap;margin-top:4px;}

/* centre IR */
#ir-centre{display:flex;flex-direction:column;overflow:hidden;}
#ir-phase-pipeline{
  display:flex;border-bottom:1px solid var(--b1);flex-shrink:0;
  background:var(--s1);
}
.ipp{
  flex:1;padding:8px 4px;
  display:flex;flex-direction:column;align-items:center;gap:3px;
  border-right:1px solid var(--b1);position:relative;
  transition:background .3s;
}
.ipp:last-child{border-right:none;}
.ipp.done{background:rgba(0,217,122,.04);}
.ipp.active{background:rgba(255,255,255,.04);}
.ipp-dot{width:6px;height:6px;border-radius:50%;background:var(--txt3);transition:all .3s;}
.ipp.done .ipp-dot{background:var(--ok);}
.ipp.active .ipp-dot{background:var(--pc,var(--info));box-shadow:0 0 8px var(--pc,var(--info));animation:livep 1s infinite;}
.ipp-lbl{font-size:.58rem;font-family:var(--font-mono);font-weight:600;letter-spacing:.08em;color:var(--txt3);transition:color .3s;}
.ipp.done .ipp-lbl{color:var(--ok);}
.ipp.active .ipp-lbl{color:var(--pc,var(--info));}
.ipp-prog{width:75%;height:2px;background:rgba(255,255,255,.06);border-radius:1px;overflow:hidden;}
.ipp-prog-fill{height:100%;border-radius:1px;transition:width .4s ease;}
.ipp.done .ipp-prog-fill{width:100%;background:var(--ok);}

#ir-detail-bar{
  padding:9px 16px;border-bottom:1px solid var(--b1);
  background:var(--s2);flex-shrink:0;
  display:flex;align-items:center;gap:14px;min-height:48px;
}
.idb-phase{font-family:var(--font-display);font-size:1rem;font-weight:800;letter-spacing:.06em;transition:color .3s;}
.idb-desc{font-size:.78rem;color:var(--txt2);flex:1;line-height:1.35;}
.idb-timer{font-family:var(--font-mono);font-size:.7rem;color:var(--txt3);}

/* triage modal overlay */
#triage-overlay{
  display:none;position:fixed;inset:0;
  background:rgba(0,0,0,.7);z-index:500;
  align-items:center;justify-content:center;
}
#triage-overlay.show{display:flex;}
#triage-modal{
  background:var(--s2);border:1px solid var(--b2);border-radius:8px;
  padding:24px;width:500px;max-width:95vw;
  box-shadow:0 20px 60px rgba(0,0,0,.6);
}
.triage-title{font-family:var(--font-display);font-size:1.1rem;font-weight:700;margin-bottom:6px;}
.triage-desc{font-size:.8rem;color:var(--txt2);line-height:1.5;margin-bottom:16px;}
.triage-options{display:flex;flex-direction:column;gap:8px;margin-bottom:16px;}
.triage-opt{
  padding:10px 14px;border-radius:var(--radius);
  border:1px solid var(--b2);cursor:pointer;transition:all .15s;
  font-size:.8rem;
}
.triage-opt:hover{border-color:var(--info);background:rgba(61,143,255,.07);}
.triage-opt.selected-tp{border-color:var(--crit);background:rgba(255,48,85,.08);}
.triage-opt.selected-fp{border-color:var(--warn);background:rgba(255,179,26,.08);}

#ir-device-bar{
  display:flex;gap:8px;padding:8px 12px;
  border-bottom:1px solid var(--b1);flex-shrink:0;
  overflow-x:auto;background:var(--s1);
}
#ir-device-bar::-webkit-scrollbar{height:3px;}
.idev{
  flex:0 0 auto;min-width:95px;
  background:var(--s2);border:1px solid var(--b1);border-radius:var(--radius);
  padding:7px 10px;transition:border-color .3s;
}
.idev.affected{border-color:var(--crit);animation:idevf .9s infinite;}
@keyframes idevf{0%,100%{box-shadow:none}50%{box-shadow:0 0 10px rgba(255,48,85,.3)}}
.idev.isolated{border-color:var(--purple);}
.idev.recovering{border-color:var(--ok);}
.idev.recovered{border-color:var(--ok);opacity:.7;}
.idev-icon{font-size:.95rem;}
.idev-name{font-size:.68rem;font-weight:600;margin:2px 0;}
.idev-val{font-family:var(--font-mono);font-size:.85rem;font-weight:600;}
.idev-unit{font-size:.58rem;color:var(--txt3);}

#ir-event-feed{flex:1;overflow-y:auto;padding:8px 12px;}
.ir-ev{
  display:flex;gap:8px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,.04);
  animation:evf .25s ease;font-size:.77rem;
}
@keyframes evf{from{opacity:0;transform:translateY(-4px)}to{opacity:1;transform:none}}
.ir-ev-dot{width:7px;height:7px;border-radius:50%;flex-shrink:0;margin-top:4px;}
.ir-ev-time{font-family:var(--font-mono);font-size:.6rem;color:var(--txt3);white-space:nowrap;}
.ir-ev-msg{flex:1;line-height:1.4;}
.ir-ev-detail{font-size:.68rem;color:var(--txt3);margin-top:2px;}

/* right: playbook */
#ir-right{border-left:1px solid var(--b1);display:flex;flex-direction:column;overflow:hidden;background:var(--s1);}
#ir-ioc-panel{padding:10px 12px;border-bottom:1px solid var(--b1);flex-shrink:0;}
.ioc-row{display:flex;justify-content:space-between;padding:3px 0;font-size:.74rem;border-bottom:1px solid rgba(255,255,255,.04);}
.ioc-row:last-child{border-bottom:none;}
.ioc-k{color:var(--txt3);}
.ioc-v{font-family:var(--font-mono);font-size:.68rem;text-align:right;}

#ir-playbook{flex:1;overflow-y:auto;}
.pb-block{padding:8px 12px;border-bottom:1px solid var(--b1);}
.pb-block-hdr{display:flex;align-items:center;gap:7px;margin-bottom:6px;}
.pb-block-name{font-size:.76rem;font-weight:700;font-family:var(--font-mono);}
.pb-step{display:flex;gap:7px;padding:3px 0;font-size:.73rem;line-height:1.4;border-bottom:1px solid rgba(255,255,255,.03);}
.pb-step:last-child{border-bottom:none;}
.pb-step .n{font-family:var(--font-mono);font-size:.6rem;color:var(--txt3);min-width:16px;margin-top:1px;}
.pb-step .t{color:var(--txt2);}
.pb-step.done .n{color:var(--ok);} .pb-step.done .t{color:var(--ok);}
.pb-step.active .n{color:var(--warn);} .pb-step.active .t{color:var(--txt);}

#ir-controls{padding:10px 12px;border-top:1px solid var(--b1);flex-shrink:0;}

/*═══════════════════════════════════
  PAGE 3 — AI ENGINE
═══════════════════════════════════*/
#page-ai{display:none;}
#page-ai.active{display:flex;flex-direction:column;}
#ai-layout{flex:1;overflow:hidden;display:grid;grid-template-columns:260px 1fr;gap:0;}
#ai-left{border-right:1px solid var(--b1);overflow-y:auto;padding:12px;display:flex;flex-direction:column;gap:10px;background:var(--s1);}
#ai-main{overflow-y:auto;padding:12px;display:flex;flex-direction:column;gap:12px;}

.ai-model-card{
  background:var(--s2);border:1px solid var(--b1);border-radius:var(--radius);
  padding:12px;
}
.ai-threat-row{
  display:flex;align-items:center;gap:8px;padding:7px 10px;
  border-bottom:1px solid rgba(255,255,255,.04);cursor:pointer;
  font-size:.77rem;transition:background .15s;
  border-radius:3px;
}
.ai-threat-row:hover{background:rgba(255,255,255,.03);}
.ai-threat-row.selected{background:rgba(61,143,255,.07);border-color:rgba(61,143,255,.2);}
.ai-fp-bar{flex:1;height:5px;background:rgba(255,255,255,.06);border-radius:3px;overflow:hidden;}
.ai-fp-fill{height:100%;border-radius:3px;transition:width .4s;}

/* tuning wizard */
#tuning-wizard{
  background:rgba(255,179,26,.06);
  border:1px solid rgba(255,179,26,.25);
  border-radius:var(--radius);padding:14px;
  display:none;
}
#tuning-wizard.show{display:block;}
.tw-step{display:none;} .tw-step.show{display:block;}

/* fine-tune DB table */
.ftdb-row{display:flex;gap:8px;padding:6px 10px;border-bottom:1px solid rgba(255,255,255,.04);font-size:.74rem;align-items:center;}
.ftdb-row:hover{background:rgba(255,255,255,.02);}

/*═══════════════════════════════════
  PAGE 4 — CISO / CXO
═══════════════════════════════════*/
#page-ciso{display:none;}
#page-ciso.active{display:flex;flex-direction:column;}
#ciso-layout{flex:1;overflow-y:auto;padding:14px;display:flex;flex-direction:column;gap:12px;}

.risk-score-ring{display:flex;align-items:center;gap:20px;}
.risk-score-num{font-family:var(--font-display);font-size:3rem;font-weight:800;line-height:1;}

.compliance-bar{display:flex;flex-direction:column;gap:6px;}
.cb-row{display:flex;align-items:center;gap:10px;font-size:.77rem;}
.cb-label{min-width:120px;color:var(--txt2);}
.cb-pct{min-width:36px;text-align:right;font-family:var(--font-mono);font-size:.72rem;}

.cost-row{display:flex;justify-content:space-between;padding:6px 0;border-bottom:1px solid rgba(255,255,255,.05);font-size:.8rem;}
.cost-row:last-child{border-bottom:none;}
.cost-val{font-family:var(--font-mono);font-weight:600;}
</style>
</head>
<body>

<!-- TOP BAR -->
<div id="topbar">
  <div class="tb-logo">OT<span>Secure</span>Ops <small>AI-DRIVEN IR PLATFORM</small></div>
  <div class="tb-tabs">
    <button class="tab-btn active" onclick="switchPage('soc',this)">
      🔲 SOC Dashboard <span class="tab-badge" id="badge-soc" style="display:none">0</span>
    </button>
    <button class="tab-btn" onclick="switchPage('ir',this)">⚡ IR Lifecycle</button>
    <button class="tab-btn" onclick="switchPage('ai',this)">🤖 AI Engine</button>
    <button class="tab-btn" onclick="switchPage('ciso',this)">📊 CISO / CXO</button>
  </div>
  <div class="tb-right">
    <div class="live-dot"></div>
    <span id="tb-clock" style="font-family:var(--font-mono);font-size:.7rem">--:--:--</span>
    <div class="tb-pill pill-ok" id="tb-status">SECURE</div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     PAGE 1 — SOC DASHBOARD
════════════════════════════════════════════════════ -->
<div class="page active" id="page-soc">
  <div id="soc-layout">
    <!-- Metrics bar -->
    <div id="soc-metrics-bar">
      <div class="metric-tile" style="--mt-color:var(--crit)">
        <div class="mt-label">Active Alerts</div>
        <div class="mt-value" id="m-active-alerts">0</div>
        <div class="mt-sub">Pending triage</div>
      </div>
      <div class="metric-tile" style="--mt-color:var(--warn)">
        <div class="mt-label">MTTD</div>
        <div class="mt-value" id="m-mttd">—</div>
        <div class="mt-sub">Mean Time to Detect</div>
        <div class="mt-trend up" id="m-mttd-trend"></div>
      </div>
      <div class="metric-tile" style="--mt-color:var(--info)">
        <div class="mt-label">MTTR</div>
        <div class="mt-value" id="m-mttr">—</div>
        <div class="mt-sub">Mean Time to Respond</div>
        <div class="mt-trend" id="m-mttr-trend"></div>
      </div>
      <div class="metric-tile" style="--mt-color:var(--ok)">
        <div class="mt-label">Alert Accuracy</div>
        <div class="mt-value" id="m-accuracy">—</div>
        <div class="mt-sub">True Positive Rate</div>
        <div class="mt-trend up" id="m-acc-trend"></div>
      </div>
      <div class="metric-tile" style="--mt-color:var(--purple)">
        <div class="mt-label">System Downtime</div>
        <div class="mt-value" id="m-downtime">0s</div>
        <div class="mt-sub">Cumulative OT downtime</div>
      </div>
      <div class="metric-tile" style="--mt-color:var(--t1)">
        <div class="mt-label">Incident Cost</div>
        <div class="mt-value" id="m-cost">$0</div>
        <div class="mt-sub">Estimated total impact</div>
      </div>
    </div>

    <!-- Alert feed -->
    <div id="soc-main">
      <div id="soc-alert-toolbar">
        <span style="font-size:.72rem;color:var(--txt3);font-family:var(--font-mono)">ALERT QUEUE</span>
        <select id="soc-filter" style="width:130px" onchange="renderAlertFeed()">
          <option value="all">All Alerts</option>
          <option value="pending">Pending</option>
          <option value="tp">True Positive</option>
          <option value="fp">False Positive</option>
          <option value="closed">Closed</option>
        </select>
        <select id="soc-threat-filter" style="width:160px" onchange="renderAlertFeed()">
          <option value="all">All Threats</option>
        </select>
        <button class="btn btn-ghost btn-sm" onclick="renderAlertFeed()">↺ Refresh</button>
        <button class="btn btn-danger btn-sm" id="btn-clear-fp" onclick="clearFPAlerts()">Clear FP Alerts</button>
        <div style="margin-left:auto;font-size:.7rem;color:var(--txt3)">
          Total: <span id="soc-total" style="color:var(--txt)">0</span> &nbsp;|&nbsp;
          TP: <span id="soc-tp-count" style="color:var(--crit)">0</span> &nbsp;|&nbsp;
          FP: <span id="soc-fp-count" style="color:var(--warn)">0</span>
        </div>
      </div>
      <div id="soc-alert-feed" class="scroll"></div>
    </div>

    <!-- Side charts -->
    <div id="soc-side">
      <div id="soc-charts">
        <div class="card">
          <div class="card-title">Alert Volume (24h)</div>
          <canvas id="chart-alert-vol" height="100"></canvas>
        </div>
        <div class="card">
          <div class="card-title">TP vs FP Rate</div>
          <canvas id="chart-tp-fp" height="100"></canvas>
        </div>
        <div class="card">
          <div class="card-title">Cost Over Time ($)</div>
          <canvas id="chart-cost" height="100"></canvas>
        </div>
        <div class="card">
          <div class="card-title">Self-Healing Controls Applied</div>
          <div id="soc-controls-list" style="display:flex;flex-direction:column;gap:5px;"></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     PAGE 2 — IR LIFECYCLE
════════════════════════════════════════════════════ -->
<div class="page" id="page-ir">
  <div id="ir-layout">
    <!-- Left: Threat List -->
    <div id="ir-left">
      <div style="padding:9px 12px;border-bottom:1px solid var(--b1);display:flex;justify-content:space-between;align-items:center;">
        <span style="font-size:.62rem;font-family:var(--font-mono);letter-spacing:.15em;color:var(--txt3)">OT TOP 10</span>
        <span id="ir-active-count" style="font-size:.62rem;color:var(--crit);font-family:var(--font-mono)">0 ACTIVE</span>
      </div>
      <div id="ir-threat-list" class="scroll" style="flex:1;"></div>
    </div>

    <!-- Centre: Phase pipeline + event feed -->
    <div id="ir-centre">
      <div id="ir-phase-pipeline"></div>
      <div id="ir-detail-bar">
        <div>
          <div style="font-size:.6rem;color:var(--txt3);font-family:var(--font-mono);letter-spacing:.12em;margin-bottom:2px">CURRENT PHASE</div>
          <div class="idb-phase" id="idb-phase-name" style="color:var(--phase-prepare)">PREPARATION</div>
        </div>
        <div class="idb-desc" id="idb-phase-desc">System armed. Select a threat scenario and launch to begin simulation.</div>
        <div class="idb-timer">T+ <span id="idb-timer">00:00</span></div>
      </div>
      <div id="ir-device-bar"></div>
      <div id="ir-event-feed" class="scroll" style="flex:1;padding:8px 12px;"></div>
    </div>

    <!-- Right: IOCs + Playbook -->
    <div id="ir-right">
      <div id="ir-ioc-panel">
        <div style="font-size:.6rem;font-family:var(--font-mono);letter-spacing:.15em;color:var(--txt3);margin-bottom:8px">INDICATORS OF COMPROMISE</div>
        <div class="ioc-row"><span class="ioc-k">Threat</span><span class="ioc-v" id="ioc-threat" style="color:var(--txt3)">—</span></div>
        <div class="ioc-row"><span class="ioc-k">Vector</span><span class="ioc-v" id="ioc-vector" style="color:var(--txt3)">—</span></div>
        <div class="ioc-row"><span class="ioc-k">Asset</span><span class="ioc-v" id="ioc-asset" style="color:var(--txt3)">—</span></div>
        <div class="ioc-row"><span class="ioc-k">CVSS</span><span class="ioc-v" id="ioc-cvss" style="color:var(--txt3)">—</span></div>
        <div class="ioc-row"><span class="ioc-k">AI Confidence</span><span class="ioc-v" id="ioc-conf" style="color:var(--txt3)">—</span></div>
        <div class="ioc-row"><span class="ioc-k">Classification</span><span class="ioc-v" id="ioc-class" style="color:var(--txt3)">PENDING</span></div>
        <div class="ioc-row"><span class="ioc-k">IEC 62443</span><span class="ioc-v" id="ioc-iec" style="color:var(--txt3)">—</span></div>
      </div>
      <div style="padding:6px 12px;border-bottom:1px solid var(--b1);flex-shrink:0;">
        <div style="font-size:.6rem;font-family:var(--font-mono);letter-spacing:.15em;color:var(--txt3)">IR PLAYBOOK — NIST SP 800-61</div>
      </div>
      <div id="ir-playbook" class="scroll" style="flex:1;"></div>
      <div id="ir-controls" style="display:flex;flex-direction:column;gap:8px;">
        <select id="ir-attack-sel"></select>
        <div style="display:flex;gap:8px;">
          <button class="btn btn-danger" id="btn-ir-launch" onclick="launchIR()" style="flex:1">⚡ Launch Scenario</button>
          <button class="btn btn-ghost" onclick="resetIR()" style="flex:0 0 auto">↺</button>
        </div>
        <div style="display:flex;align-items:center;gap:8px;font-size:.65rem;color:var(--txt3);">
          <span style="white-space:nowrap">Speed</span>
          <input type="range" id="ir-speed" min="300" max="3000" value="900" step="100" oninput="setIRSpeed(this.value)" style="flex:1;accent-color:var(--info);">
          <span id="ir-speed-lbl">0.9s</span>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- TRIAGE MODAL -->
<div id="triage-overlay">
  <div id="triage-modal">
    <div class="triage-title" id="triage-title">🔍 Alert Triage Required</div>
    <div class="triage-desc" id="triage-desc">The AI engine has detected an anomaly. Classify this alert:</div>
    <div class="triage-options" id="triage-options"></div>
    <div id="triage-context" class="info-box" style="margin-bottom:14px;font-size:.74rem;"></div>
    <div style="display:flex;gap:8px;justify-content:flex-end;">
      <button class="btn btn-danger" onclick="classifyAlert('tp')">🚨 True Positive — Launch IR</button>
      <button class="btn btn-warn" onclick="classifyAlert('fp')">⚠ False Positive — Dismiss</button>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     PAGE 3 — AI ENGINE
════════════════════════════════════════════════════ -->
<div class="page" id="page-ai">
  <div id="ai-layout">
    <!-- Left: per-threat AI stats -->
    <div id="ai-left">
      <div style="font-size:.6rem;font-family:var(--font-mono);letter-spacing:.15em;color:var(--txt3);padding:2px 0 8px">AI MODEL — PER THREAT</div>
      <div id="ai-threat-rows"></div>
      <hr class="divider"/>
      <div class="card" style="padding:10px;">
        <div class="card-title">Overall Model Health</div>
        <div class="g2" style="gap:8px;">
          <div class="metric-tile" style="--mt-color:var(--ok);padding:8px;">
            <div class="mt-label" style="font-size:.58rem">TP Rate</div>
            <div class="mt-value" style="font-size:1.2rem" id="ai-global-tpr">—</div>
          </div>
          <div class="metric-tile" style="--mt-color:var(--warn);padding:8px;">
            <div class="mt-label" style="font-size:.58rem">FP Rate</div>
            <div class="mt-value" style="font-size:1.2rem" id="ai-global-fpr">—</div>
          </div>
          <div class="metric-tile" style="--mt-color:var(--info);padding:8px;">
            <div class="mt-label" style="font-size:.58rem">Tuning Events</div>
            <div class="mt-value" style="font-size:1.2rem" id="ai-tune-count">0</div>
          </div>
          <div class="metric-tile" style="--mt-color:var(--purple);padding:8px;">
            <div class="mt-label" style="font-size:.58rem">Controls Added</div>
            <div class="mt-value" style="font-size:1.2rem" id="ai-controls-count">0</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Right: charts + tuning wizard + fine-tune DB -->
    <div id="ai-main">
      <!-- Alert accuracy chart -->
      <div class="card">
        <div class="card-title">Alert Accuracy Over Time — <span id="ai-selected-threat-name">All Threats</span></div>
        <canvas id="chart-ai-accuracy" height="100"></canvas>
      </div>

      <div class="g2">
        <div class="card">
          <div class="card-title">Alert Volume by Threat</div>
          <canvas id="chart-ai-volume" height="120"></canvas>
        </div>
        <div class="card">
          <div class="card-title">FP Rate Trend (rolling)</div>
          <canvas id="chart-ai-fpr" height="120"></canvas>
        </div>
      </div>

      <!-- Tuning Wizard -->
      <div id="tuning-wizard">
        <div style="display:flex;align-items:center;gap:10px;margin-bottom:10px;">
          <span style="font-size:1rem">⚠</span>
          <div>
            <div style="font-size:.85rem;font-weight:700;color:var(--warn)">AI Fine-Tuning Required</div>
            <div style="font-size:.74rem;color:var(--txt2)" id="tuning-reason">High false positive rate detected for <b id="tuning-threat-name">—</b></div>
          </div>
        </div>
        <div class="tw-step show" id="tw-step1">
          <div class="info-box warn" style="margin-bottom:10px;" id="tw-analysis"></div>
          <div style="font-size:.78rem;color:var(--txt2);margin-bottom:8px;">Proposed rule adjustments:</div>
          <div id="tw-proposals" style="display:flex;flex-direction:column;gap:5px;margin-bottom:12px;"></div>
          <div style="display:flex;gap:8px;">
            <button class="btn btn-warn" onclick="applyTuning()">✓ Apply Changes</button>
            <button class="btn btn-ghost" onclick="dismissTuning()">Dismiss</button>
          </div>
        </div>
      </div>

      <!-- Fine-Tune DB -->
      <div class="card">
        <div class="card-title">Fine-Tune Database <span style="color:var(--txt3);font-weight:400">(all tuning events)</span></div>
        <table class="tbl">
          <thead><tr>
            <th>Timestamp</th><th>Threat</th><th>Trigger</th><th>Change Applied</th><th>FP Before</th><th>FP After</th><th>Status</th>
          </tr></thead>
          <tbody id="ftdb-tbody"></tbody>
        </table>
      </div>

      <!-- Per-threat alert history -->
      <div class="card">
        <div class="card-title">Alert History — <span id="ai-hist-threat">Select a threat on the left</span></div>
        <table class="tbl">
          <thead><tr>
            <th>#</th><th>Time</th><th>Threat</th><th>AI Confidence</th><th>Classification</th><th>MTTD</th><th>MTTR</th><th>Cost</th><th>Controls Added</th>
          </tr></thead>
          <tbody id="ai-hist-tbody"></tbody>
        </table>
      </div>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════════════════
     PAGE 4 — CISO / CXO
════════════════════════════════════════════════════ -->
<div class="page" id="page-ciso">
  <div id="ciso-layout">
    <!-- Row 1: Risk + Cost + Compliance -->
    <div class="g3">
      <div class="card">
        <div class="card-title">Organisational Risk Score</div>
        <div class="risk-score-ring">
          <svg width="90" height="90" viewBox="0 0 90 90">
            <circle cx="45" cy="45" r="36" fill="none" stroke="var(--b2)" stroke-width="7"/>
            <circle id="risk-ring" cx="45" cy="45" r="36" fill="none"
              stroke="var(--ok)" stroke-width="7" stroke-linecap="round"
              stroke-dasharray="226.2" stroke-dashoffset="226.2"
              transform="rotate(-90 45 45)" style="transition:all .6s"/>
          </svg>
          <div>
            <div class="risk-score-num" id="ciso-risk-score" style="color:var(--ok)">0</div>
            <div style="font-size:.72rem;color:var(--txt2)">/100 risk score</div>
            <div style="font-size:.7rem;color:var(--txt3);margin-top:2px" id="ciso-risk-label">LOW RISK</div>
          </div>
        </div>
        <div style="margin-top:10px;display:flex;flex-direction:column;gap:5px;" id="ciso-risk-factors"></div>
      </div>

      <div class="card">
        <div class="card-title">Financial Impact</div>
        <div style="display:flex;flex-direction:column;gap:0;">
          <div class="cost-row"><span>Total Incident Cost</span><span class="cost-val" id="ciso-total-cost" style="color:var(--crit)">$0</span></div>
          <div class="cost-row"><span>Production Downtime Cost</span><span class="cost-val" id="ciso-downtime-cost" style="color:var(--warn)">$0</span></div>
          <div class="cost-row"><span>Remediation Labour</span><span class="cost-val" id="ciso-labour-cost" style="color:var(--info)">$0</span></div>
          <div class="cost-row"><span>Regulatory Risk Exposure</span><span class="cost-val" id="ciso-reg-cost" style="color:var(--purple)">$0</span></div>
          <div class="cost-row" style="font-weight:600;border-top:1px solid var(--b2);margin-top:4px;padding-top:8px;">
            <span>Cost Avoided by AI (est.)</span><span class="cost-val" style="color:var(--ok)" id="ciso-avoided">$0</span>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="card-title">Compliance Posture</div>
        <div class="compliance-bar" id="ciso-compliance-bars"></div>
      </div>
    </div>

    <!-- Row 2: KPI metrics -->
    <div class="g4" id="ciso-kpis"></div>

    <!-- Row 3: Trend charts -->
    <div class="g2">
      <div class="card">
        <div class="card-title">Risk Score Trend</div>
        <canvas id="chart-ciso-risk" height="110"></canvas>
      </div>
      <div class="card">
        <div class="card-title">Incident Cost Trend ($)</div>
        <canvas id="chart-ciso-cost" height="110"></canvas>
      </div>
    </div>

    <!-- Row 4: Self-healing controls + recommendations -->
    <div class="g2">
      <div class="card">
        <div class="card-title">Self-Healing Controls Applied</div>
        <table class="tbl" id="ciso-controls-tbl">
          <thead><tr><th>Control</th><th>Triggered By</th><th>Risk ↓</th><th>Status</th><th>Date</th></tr></thead>
          <tbody id="ciso-controls-tbody"></tbody>
        </table>
      </div>
      <div class="card">
        <div class="card-title">AI Recommendations (Pending)</div>
        <div id="ciso-recommendations" style="display:flex;flex-direction:column;gap:8px;"></div>
      </div>
    </div>

    <!-- Row 5: Threat breakdown -->
    <div class="card">
      <div class="card-title">Threat Incident Summary — Board Report View</div>
      <table class="tbl" id="ciso-summary-tbl">
        <thead><tr>
          <th>Threat</th><th>Tier</th><th>Incidents</th><th>TP</th><th>FP</th><th>Accuracy</th><th>Avg MTTD</th><th>Avg MTTR</th><th>Total Cost</th><th>Controls</th><th>Status</th>
        </tr></thead>
        <tbody id="ciso-summary-tbody"></tbody>
      </table>
    </div>
  </div>
</div>

<!-- ═══════════════ JAVASCRIPT ENGINE ═══════════════ -->
<script>
/*═══════════════════════════════════════════════════════════
  OT SecureOps — Full AI-Driven IR Platform Engine
  Pages: SOC Dashboard | IR Lifecycle | AI Engine | CISO/CXO
═══════════════════════════════════════════════════════════*/

// ══ NIST PHASES ══════════════════════════════════════════════
const PHASES=[
  {id:'prepare',   name:'Preparation',   short:'PREP',    color:'#3d8fff'},
  {id:'detect',    name:'Detection',     short:'DETECT',  color:'#ffe033'},
  {id:'analyze',   name:'Analysis',      short:'ANALYZE', color:'#ff9020'},
  {id:'contain',   name:'Containment',   short:'CONTAIN', color:'#ff3055'},
  {id:'eradicate', name:'Eradication',   short:'ERAD',    color:'#a855f7'},
  {id:'recover',   name:'Recovery',      short:'RECOVER', color:'#00d97a'},
  {id:'post',      name:'Post-Incident', short:'POST-IR', color:'#66aaff'},
];

// ══ OT TOP 10 THREATS ════════════════════════════════════════
const THREATS=[
 {id:'t1',rank:1,tier:1,name:'Unknown Assets & Unmanaged External Access',short:'Unknown Assets',
  color:'#ff3055',cvss:9.1,iec:'IEC 62443-2-1 SR 7.8',
  attackType:'ROGUE DEVICE / UNAUTH ACCESS',
  vector:'Unauthorised Remote Access',surface:'External VPN / Jump Host',
  downtimeMin:15,baseCost:18000,
  // AI detection: higher zScore threshold = more sensitive, lower = less FP
  aiConfig:{zThreshold:2.2,spikeThreshold:0.35,baseTPRate:0.88,baseFPRate:0.18},
  devices:['plc-01','hmi-01'],
  attackSim:s=>{ s.value+=rnd(40,120); },
  phases:{
    detect: ['Asset discovery scan detects unlisted device (MAC: DE:AD:BE:EF:00:01)',
             'Rogue VPN session in firewall logs — source: 185.220.x.x',
             'AI Z-score=3.8 on PLC polling frequency (threshold: 2.2)',
             'Alert: Unrecognised device active on OT VLAN 20',
             'SIEM auto-raises P1 incident ticket #IR-001'],
    analyze:['Rogue device mapped to physical port SW1/Gi0/12',
             'Device has Modbus write access to PLC Unit 01',
             'Attacker IP: 185.220.101.47 — TOR exit node confirmed',
             'Supplier remote-access schedule: NOT in approved window',
             'Classification: External threat actor via compromised vendor account'],
    contain:['Block rogue MAC DE:AD:BE:EF:00:01 at switch ACL',
             'Terminate VPN session — tunnel ID 7743 killed',
             'Disable all unmanaged remote-access accounts (12 accounts)',
             'Enable port security: max 1 MAC per OT switch port',
             'Notify CISO and OT plant manager — escalation sent'],
    eradicate:['Remove rogue device from site — physical decommission',
               'Revoke all unmanaged external credentials in PAM vault',
               'Deploy NAC policy: 802.1X required on all OT ports',
               'Patch jump-host CVE-2024-1234 (priv escalation)',
               'Update allowed-device whitelist in NAC platform'],
    recover:['Re-verify all active PLC/HMI connections — 6 devices OK',
             'Restore device inventory in CMDB — asset register updated',
             'Re-enable approved vendor access with MFA enforced',
             '48hr elevated monitoring period activated',
             'Update firewall rule baseline — 3 new ACL rules added'],
    post:   ['Document unknown asset discovery timeline in incident report',
             'IOCs shared with FS-ISAC (IPs, MAC, TTP fingerprint)',
             'Mandate quarterly OT asset audits — next: 2025-04-01',
             'IEC 62443-2-1 asset register updated with 1 new device class',
             'Self-healing control applied: Auto-block on new MAC detection']
  }
 },
 {id:'t2',rank:2,tier:1,name:'Devices with Known Vulnerabilities',short:'Known CVEs',
  color:'#ff3055',cvss:8.8,iec:'IEC 62443-2-3 SR 7.6',
  attackType:'CVE EXPLOITATION (RCE)',
  vector:'Remote Code Execution via CVE',surface:'SCADA Server / Historian',
  downtimeMin:45,baseCost:42000,
  aiConfig:{zThreshold:2.5,spikeThreshold:0.45,baseTPRate:0.93,baseFPRate:0.09},
  devices:['scada-01','historian-01'],
  attackSim:s=>{ s.value=rnd(0.1,0.8); },
  phases:{
    detect: ['IDS signature match: Shellshock exploit payload (CVE-2024-6387)',
             'SCADA server CPU: 99% — anomaly Z-score=4.1',
             'Historian DB write errors: 847 in last 60 seconds',
             'AI detects memory scraping pattern on SCADA process list',
             'EDR agent raises quarantine event on scada-svr-01'],
    analyze:['Confirmed CVE-2024-6387 (OpenSSH RCE) — patch level: 2022',
             'Exploit success confirmed via /tmp/.[hidden] backdoor',
             'Lateral movement: SCADA → Engineering WS (SMB pass-the-hash)',
             'Attacker intent: process value manipulation (no exfil detected)',
             'Safety impact assessment: SAFE — ESD not triggered'],
    contain:['SCADA server network-isolated at OT DMZ firewall',
             'Manual/local control activated on all affected PLCs',
             'C2 IP 91.108.56.22 blocked at perimeter (2 rules added)',
             'Remote historian replication suspended',
             'Process safety engineer on-site for manual monitoring'],
    eradicate:['Emergency patch CVE-2024-6387 applied (OpenSSH 9.8)',
               'SCADA server re-imaged from 2025-01-15 gold image',
               'Persistence removed: cron job, /tmp/.cache backdoor',
               'All historian nodes scanned — no lateral spread confirmed',
               'Service account credentials rotated (12 accounts)'],
    recover:  ['SCADA restored from verified clean backup (integrity hash OK)',
               'Process setpoints validated vs physical pressure gauges',
               'Historian replication re-enabled with integrity monitoring',
               'Engineering WS returned under EDR with new agent policy',
               '72hr elevated monitoring period — 2 analysts on watch'],
    post:     ['CVE incident report filed — NIST NVD reference added',
               'OT patch SLA established: Critical=7d, High=30d, Med=90d',
               'Virtual patching via IPS rule deployed for SCADA segment',
               'ICS-CERT advisory subscription activated for all 47 assets',
               'Self-healing: Auto-patch workflow triggered for OpenSSH class']
  }
 },
 {id:'t3',rank:3,tier:1,name:'Inadequate Supply Chain Management',short:'Supply Chain',
  color:'#ff3055',cvss:9.4,iec:'IEC 62443-2-4 SR 7.10',
  attackType:'TROJANISED FIRMWARE',
  vector:'Malicious Firmware via Vendor Portal',surface:'RTU Field Units',
  downtimeMin:90,baseCost:75000,
  aiConfig:{zThreshold:2.0,spikeThreshold:0.5,baseTPRate:0.79,baseFPRate:0.26},
  devices:['rtu-01','sensor-net'],
  attackSim:s=>{ s.value+=rnd(20,80); s.value*=rnd(1.5,2.5); },
  phases:{
    detect: ['Firmware integrity check FAIL on RTU-01 (SHA256 mismatch)',
             'Unexpected outbound beacon: rtu-01 → 45.142.212.100:8443',
             'Vendor update hash mismatch vs published checksum (PGP verify fail)',
             'AI: RTU command frequency +340% above baseline Z-score=4.8',
             'Threat intel feed alert: Vendor XYZ portal compromised 72hrs ago'],
    analyze:['Firmware binary extracted and reverse-engineered (Ghidra)',
             'Backdoor identified: hardcoded C2 beacon every 300s',
             'Affected scope: RTU-01, RTU-02, sensor-net (3 devices received update)',
             'Vendor confirmation: update server compromised via CVE-2024-9999',
             'Physical process impact: RTU output values were manipulated for 4hrs'],
    contain:['RTU-01 and RTU-02 rolled back to firmware v2.1.4 (last known-good)',
             'C2 domains blocked at DNS and firewall (2 domains, 3 IPs)',
             'All vendor remote access suspended — 0 active sessions',
             'Advisory sent to 14 peer operators using same vendor equipment',
             'Out-of-band SCADA monitoring activated for field devices'],
    eradicate:['Clean firmware flashed to all 3 affected RTUs',
               'All default and vendor-set credentials changed (8 devices)',
               'Firmware signing verification process implemented',
               'Vendor update server isolated pending forensic handover',
               'Backdoor C2 persistence removed from all field endpoints'],
    recover:  ['RTU process values verified against physical flow meters',
               'Sensor network communications restored with integrity checks',
               'Vendor remote access re-enabled with enhanced session monitoring',
               'Digital signature verification mandatory on all future updates',
               'SBOM (Software Bill of Materials) updated — 3 new entries'],
    post:     ['Incident reported to ICS-CERT as supply chain event (SC-2025-001)',
               'Vendor demanded to provide incident report within 72hrs',
               'Firmware supply-chain security policy published — v1.0',
               'Firmware hash verification added to Change Management workflow',
               'Self-healing: Automated firmware integrity scan every 6hrs added']
  }
 },
 {id:'t4',rank:4,tier:1,name:'Loss of Availability (OT DoS)',short:'Availability Attack',
  color:'#ff3055',cvss:8.6,iec:'IEC 62443-3-3 SR 7.1',
  attackType:'OT NETWORK FLOOD / DoS',
  vector:'PROFINET/Modbus Protocol Flood',surface:'OT Network Segment',
  downtimeMin:120,baseCost:95000,
  aiConfig:{zThreshold:1.8,spikeThreshold:0.6,baseTPRate:0.96,baseFPRate:0.07},
  devices:['plc-01','hmi-01','rtu-01'],
  attackSim:s=>{ s.value=rnd(0,0.4); },
  phases:{
    detect: ['OT VLAN bandwidth: 99.7% — threshold breached (normal: 40%)',
             'PLC heartbeat timeouts: 3 devices unreachable for >30s',
             'HMI loses real-time data feed — display frozen',
             'Process historian gaps detected: 847 missing data points',
             'AI: simultaneous Z-score anomaly across ALL 6 monitored devices'],
    analyze:['Flood source identified: compromised HMI on OT VLAN',
             'Protocol: Modbus broadcast storm — 48,000 requests/sec',
             'Safety systems not affected — ESD on hardwired backup',
             'Production downtime: 120 minutes — $95,000 estimated loss',
             'Parallel exfil check: no data leaving OT boundary'],
    contain:['OT network traffic shaping: rate limit 1000 pkt/s enforced',
             'Compromised HMI isolated at Layer 2 (VLAN reassignment)',
             'PLCs switched to local autonomous fallback mode',
             'Emergency shutdown procedure NOT required — process stable',
             'Flood source MAC blocked: AA:BB:CC:DD:EE:FF'],
    eradicate:['HMI re-imaged — malware (Triton-variant) removed',
               'Modbus broadcast whitelist deployed at OT firewall',
               'Protocol stack vulnerability patched (Modbus TCP stack overflow)',
               'Additional DMZ zone created: HMI segment isolated from PLC VLAN',
               'Modbus/PROFINET deep packet inspection enabled'],
    recover:  ['OT network restored incrementally — 6 segments validated',
               'All PLC setpoints and process state verified by engineers',
               'Historian data collection restarted — backfill complete',
               'HMI displays validated — all 12 screens showing live data',
               'Safety system integrity checks passed — ESD reset confirmed'],
    post:     ['Production loss report: $95,000 — root cause: OT flat network',
               'Network topology redesign commissioned — budget $45,000',
               'OT network segmentation per IEC 62443-3-2 initiated',
               'Redundant OT network paths approved — implementation Q2',
               'Self-healing: Auto rate-limit on OT VLAN flood detection added']
  }
 },
 {id:'t5',rank:5,tier:2,name:'Insufficient Access Control',short:'Access Control Failure',
  color:'#ff7a1a',cvss:8.1,iec:'IEC 62443-3-3 SR 1.1',
  attackType:'LATERAL MOVEMENT',
  vector:'Credential Stuffing / Pass-the-Hash',surface:'IT/OT DMZ Boundary',
  downtimeMin:20,baseCost:22000,
  aiConfig:{zThreshold:2.3,spikeThreshold:0.4,baseTPRate:0.85,baseFPRate:0.22},
  devices:['hmi-01','scada-01'],
  attackSim:s=>{ s.value+=rnd(15,45); },
  phases:{
    detect: ['Failed logins: 847/min on HMI-Terminal-01 (threshold: 10/min)',
             'Successful auth with shared password "Scada2020!" on 3 accounts',
             'IT → OT DMZ crossing: workstation IT-PC-023 → OT VLAN 20',
             'SCADA login from IP 10.0.5.47 (non-engineering-workstation)',
             'AI: user behaviour anomaly — 03:47 UTC, weekend, unusual location'],
    analyze:['Compromised credential source: phishing email 6 days prior',
             'Lateral movement path: IT → IDMZ → OT HMI → SCADA',
             'Attacker access scope: HMI read/write, SCADA read-only',
             'No setpoint changes detected — reconnaissance only',
             'OT AD backdoor account found: svc_backup_old (inactive 2 years)'],
    contain:['Force password reset on all 47 OT accounts',
             'Terminate all 12 active OT remote sessions',
             'Account lockout enforced: 5 failed attempts → 30min lock',
             'Compromised NTLM hashes invalidated via krbtgt rotation',
             'MFA enforced immediately for all OT system logins'],
    eradicate:['Backdoor account svc_backup_old removed from AD',
               'All compromised Kerberos tickets revoked (golden ticket check)',
               'PAM (CyberArk) deployed for all OT privileged accounts',
               'Just-in-time access implemented for OT maintenance windows',
               'Default vendor passwords removed from 23 OT devices'],
    recover:  ['Normal OT user access restored with new credentials + MFA',
               'Role-based access permissions re-validated — 12 roles reviewed',
               'Privileged session recording activated (CyberArk PSM)',
               'MFA rollout verified on all 8 OT workstations',
               'Access control matrix updated in CMDB'],
    post:     ['All 47 OT accounts audited — 8 stale accounts removed',
               'Quarterly access review process mandated — next: 2025-04-01',
               'Deception technology deployed: honeypot PLC on OT VLAN',
               'OT operators completed phishing + credential hygiene training',
               'Self-healing: Auto-lock on after-hours OT login attempts added']
  }
 },
 {id:'t6',rank:6,tier:2,name:'Missing Incident Detection / Reaction',short:'No Detection Capability',
  color:'#ff7a1a',cvss:7.8,iec:'IEC 62443-2-1 SR 6.2',
  attackType:'APT LONG DWELL (200+ DAYS)',
  vector:'Advanced Persistent Threat',surface:'Engineering Workstation',
  downtimeMin:5,baseCost:140000,
  aiConfig:{zThreshold:3.0,spikeThreshold:0.3,baseTPRate:0.72,baseFPRate:0.32},
  devices:['eng-ws','historian-01'],
  attackSim:s=>{ s.value+=rnd(5,18); },
  phases:{
    detect: ['Threat hunt discovers RAT (Emotet variant) on eng-ws-002',
             'Historian: subtle process setpoint drift — 0.3% daily over 47 days',
             'AI retrospective: anomaly pattern detected 47 days ago — missed',
             'C2 beaconing: eng-ws → 185.220.x.x every 3600s (DNS exfil)',
             'Peer intel: OT-sector APT campaign (SANDWORM) confirmed active'],
    analyze:['Initial compromise: spear-phish 207 days ago — dwell 207 days',
             'APT accessed: process schematics, P&ID diagrams, credential store',
             'C2 infrastructure: 3 domains, 2 fast-flux IPs extracted',
             'Attacker target: mapping facility for future sabotage operation',
             'Historian data integrity: 3 setpoints modified — all minor, process-safe'],
    contain:['Engineering workstation isolated immediately',
             'APT C2 IPs/domains blocked at all 4 egress firewall points',
             'Compromised account svc_eng_001 suspended',
             'Full packet capture activated on OT segment — 10Gbps tap deployed',
             '24/7 SOC monitoring activated for OT segment (Tier 3 analyst)'],
    eradicate:['RAT and 4 persistence mechanisms removed (reg keys, schtask, dll)',
               'Eng workstation re-imaged from clean gold image',
               'All 34 credentials from dwell period rotated',
               'OT NDR (Darktrace) deployed across 3 OT network segments',
               'Application whitelisting (Carbon Black) deployed on all OT hosts'],
    recover:  ['Engineering WS rebuilt with hardened image + EDR + AppWhitelist',
               'All process setpoints audited vs physical plant records',
               'Continuous OT monitoring platform active — baseline learning 7d',
               'ICS protocol anomaly detection enabled (Claroty)',
               'Historian data integrity validated — 3 corrections made'],
    post:     ['Full threat hunt commissioned — 14-day scope across OT/IT',
               'OT-specific SIEM (LogRhythm) procurement approved ($120k)',
               '24/7 OT-SOC established — 3 FTE analysts dedicated to OT',
               'IR runbooks created for all 10 OT threat scenarios',
               'Self-healing: Automated behavioural baselining added for all OT hosts']
  }
 },
 {id:'t7',rank:7,tier:2,name:'Broken Zones and Conduits Design',short:'Broken Segmentation',
  color:'#ff7a1a',cvss:8.3,iec:'IEC 62443-3-2 SR 5.1',
  attackType:'ZONE BOUNDARY BREACH',
  vector:'Flat Network Traversal',surface:'OT/IT Network Boundary',
  downtimeMin:30,baseCost:35000,
  aiConfig:{zThreshold:2.1,spikeThreshold:0.45,baseTPRate:0.87,baseFPRate:0.15},
  devices:['plc-01','rtu-01','sensor-net'],
  attackSim:s=>{ s.value+=rnd(30,90); },
  phases:{
    detect: ['Cross-zone traffic: Zone 3 (DMZ) → Zone 1 (PLC) — policy violation',
             'PLC receives Modbus write from unauthorised source: 10.20.30.44',
             'Firewall log: conduit policy violated — 847 rule hits in 60s',
             'AI: lateral scan pattern across OT VLANs — 6 subnets probed',
             'NIDS: Modbus write command from non-HMI source (coil register 0x0001)'],
    analyze:['Network map: actual topology differs from documented design',
             'Missing IDMZ between IT network and OT Level 2',
             'Unauthorised commands: 3 Modbus write operations to PLC coil outputs',
             'Process impact: MINOR — Pump 3 cycled on/off twice (no damage)',
             'Attacker pivot: IT laptop → IT server → flat OT network'],
    contain:['Emergency VLAN isolation: OT Zone 1 and Zone 2 segmented',
             'Cross-zone traffic blocked at core switch (VLAN ACL)',
             'Modbus restricted to authorised source IPs only (whitelist: 3 IPs)',
             'Emergency manual control activated for Pump 3',
             'OT firewall emergency rules deployed (22 ACL entries added)'],
    eradicate:['OT network redesigned per IEC 62443-3-2 zone model',
               'Dedicated OT firewall deployed at Zone 1/2 boundary (Fortinet OT)',
               'Industrial DMZ (IDMZ) created between IT and OT Level 2',
               'Implicit trust relationships removed — zero trust OT model',
               'Application-layer Modbus DPI filtering enabled on OT firewall'],
    recover:  ['Inter-zone comms restored via hardened IDMZ conduits',
               'PLC states verified post-isolation — all setpoints nominal',
               'HMI data feeds re-enabled through IDMZ Modbus proxy',
               'New firewall rules tested in staging — 0 false blocks',
               'Network topology diagrams updated — v3.1 released'],
    post:     ['IEC 62443-3-2 zone risk assessment commissioned (£25k)',
               'Purdue Model-aligned architecture document published — v1.0',
               'Conduit security policy defined and reviewed quarterly',
               'Continuous network topology monitoring via Claroty deployed',
               'Self-healing: Auto-VLAN quarantine on zone policy violation added']
  }
 },
 {id:'t8',rank:8,tier:2,name:'Missing Awareness (Human Factor)',short:'Spear Phishing',
  color:'#ff7a1a',cvss:7.5,iec:'IEC 62443-2-1 SR 2.4',
  attackType:'SPEAR PHISHING / USB DROP',
  vector:'Phishing Email → Macro Execution',surface:'Engineering Workstation',
  downtimeMin:25,baseCost:28000,
  aiConfig:{zThreshold:2.4,spikeThreshold:0.38,baseTPRate:0.82,baseFPRate:0.24},
  devices:['eng-ws','hmi-01'],
  attackSim:s=>{ s.value+=rnd(10,35); },
  phases:{
    detect: ['Email gateway: macro-enabled Excel opened by engineer J.Smith',
             'EDR: PowerShell spawned from EXCEL.EXE — suspicious child process',
             'USB mass storage inserted on air-gapped eng-ws-003 at 14:32',
             'AI: new process "svchost32.exe" outside application whitelist',
             'Credential harvester "Mimikatz" detected in process memory dump'],
    analyze:['Phishing email: from spoofed vendor@siemens-update[.]com',
             'Engineer clicked attachment: "PLC_Firmware_Update_v4.2.xlsx"',
             'USB malware spread to 1 adjacent OT host (auto-run disabled — blocked)',
             'HMI login from engineer credentials 4hrs after phishing event',
             'Engineer interview: "I thought it was a real Siemens email"'],
    contain:['Engineer workstation isolated — disconnected from OT network',
             'Phishing domain siemens-update[.]com blocked company-wide (DNS sinkhole)',
             'USB ports disabled on all 23 OT workstations via GPO',
             'Forced logout of all active OT sessions for compromised user',
             'Company-wide phishing alert sent to all 450 staff'],
    eradicate:['Malware and 3 persistence mechanisms removed',
               'Workstation re-imaged with hardened gold image',
               'Compromised credentials revoked — new credentials issued with MFA',
               'All IOCs blocked at perimeter (2 IPs, 1 domain, 1 file hash)',
               'Email sandboxing (Proofpoint) deployed for all OT staff inboxes'],
    recover:  ['Workstation rebuilt with approved software + AppWhitelist',
               'Engineer re-enrolled with MFA-protected OT domain account',
               'USB device control solution deployed company-wide (DLP)',
               'No process changes confirmed during compromise period',
               'All 23 OT workstations hardened — USB boot disabled in BIOS'],
    post:     ['Mandatory phishing awareness training — all 450 staff (2hrs)',
               'Simulated phishing campaign scheduled quarterly',
               'OT-specific Acceptable Use Policy published and signed',
               'USB policy enforced — hardware write-blockers deployed',
               'Self-healing: Auto-isolate workstation on macro execution in OT zone']
  }
 },
 {id:'t9',rank:9,tier:2,name:'Insecure ICS Protocols',short:'Insecure Protocols',
  color:'#ff7a1a',cvss:8.0,iec:'IEC 62443-3-3 SR 3.1',
  attackType:'MODBUS REPLAY / DNP3 SPOOF',
  vector:'Protocol Replay Attack',surface:'OT Fieldbus / Modbus TCP',
  downtimeMin:40,baseCost:48000,
  aiConfig:{zThreshold:1.9,spikeThreshold:0.55,baseTPRate:0.91,baseFPRate:0.12},
  devices:['plc-01','rtu-01'],
  attackSim:s=>{ s.value=s.value>50?rnd(0,8):rnd(90,160); },
  phases:{
    detect: ['IDS: Modbus replay sequence detected — duplicate transaction IDs 0x1A2B',
             'PLC coil output changes without corresponding HMI command in historian',
             'DNP3 traffic from source 10.20.30.99 (not in authorised master list)',
             'AI: PLC register write frequency 840% above baseline Z-score=4.2',
             'Process engineer alarm: Valve V-104 opened without operator action'],
    analyze:['Packet capture: Modbus replay — 847 duplicate frames in 60s',
             'MITM confirmed: attacker positioned on OT VLAN via compromised switch',
             'Affected registers: coil 0x0001 (Pump 1), coil 0x0004 (Valve V-104)',
             'Physical impact: Pump 1 cavitated for 22min — minor bearing wear',
             'No Modbus authentication exists — protocol designed in 1979'],
    contain:['Modbus write permissions disabled — PLC in read-only mode',
             'All PLCs forced to manual/local control',
             'Unauthorised Modbus master 10.20.30.99 blocked at OT firewall',
             'Strict source IP filtering on all RTU polling requests',
             'Process safety engineer on site — manual valve V-104 closed'],
    eradicate:['OT firewall Modbus DPI deployed — whitelist-only write commands',
               'Modbus/TCP authentication (Modbus Security RFC) implemented',
               'DNP3 replaced with DNP3-SA (Secure Authentication v5) on all RTUs',
               'Sequence number validation added at OT application firewall',
               'Serial Modbus isolated onto dedicated media converter (no IP bridge)'],
    recover:  ['PLC setpoints restored to validated values — process engineer sign-off',
               'HMI control re-enabled through authenticated Modbus channel',
               'All RTU output states verified vs physical pressure/flow readings',
               'Historian polling restarted with protocol anomaly monitoring',
               'Protocol conformance test suite executed — all 8 devices passed'],
    post:     ['Legacy protocol register published — 34 protocols documented',
               'Protocol security upgrade roadmap created — 3 year timeline',
               'Protocol whitelist deployed on all 4 OT firewalls',
               'OPC-UA Security evaluation commissioned — migration 2026',
               'Self-healing: Automatic Modbus read-only mode on anomalous write pattern']
  }
 },
 {id:'t10',rank:10,tier:3,name:'Missing Hardening',short:'Missing Hardening',
  color:'#c8a000',cvss:7.2,iec:'IEC 62443-3-3 SR 7.6',
  attackType:'DEFAULT CONFIG EXPLOITATION',
  vector:'Default Credentials / Open Services',surface:'PLC Web Interface / SSH',
  downtimeMin:10,baseCost:12000,
  aiConfig:{zThreshold:2.6,spikeThreshold:0.35,baseTPRate:0.80,baseFPRate:0.27},
  devices:['plc-01','hmi-01','scada-01'],
  attackSim:s=>{ s.value+=rnd(8,28); },
  phases:{
    detect: ['Vulnerability scanner: PLC web server active on port 80 (unexpected)',
             'Login successful with default admin:admin on SCADA web console',
             'Nmap discovery: 23 open ports on SCADA server (policy: max 3)',
             'AI: configuration change on PLC-01 without change management ticket',
             'SSH brute-force succeeded: vendor default key accepted on HMI'],
    analyze:['23 unnecessary services identified: FTP, Telnet, HTTP, SNMP v1, RDP',
             'Default credentials active on 7 of 8 monitored OT devices',
             'Attacker actions: read process config, download ladder logic backup',
             'CIS ICS Benchmark gap analysis: 67% non-compliant',
             'No device hardening performed since commissioning in 2019'],
    contain:['PLC web server disabled immediately (service stopped)',
             'All default credentials changed on 7 affected devices',
             'Unexpected ports blocked at OT firewall — 20 rules added',
             'Telnet/FTP disabled on all OT devices via vendor CLI',
             'Most-exposed devices (SCADA, HMI) isolated for hardening sprint'],
    eradicate:['CIS Benchmark hardening applied to all 8 OT devices',
               'All unnecessary services and software removed (23 services disabled)',
               'Host-based firewall enabled on SCADA server (Windows Firewall GPO)',
               'Change management mandatory for all OT configuration changes',
               'Audit logging enabled on all 8 OT devices — central SIEM ingestion'],
    recover:  ['Hardened baseline configuration deployed and verified',
               'Process functionality tested post-hardening — all OK',
               'Only required network services re-enabled (3 per device max)',
               'Nessus scan post-hardening: 0 critical, 2 medium findings',
               'Hardened configuration baseline stored in CMDB'],
    post:     ['Automated hardening compliance scanning (Tenable.ot) deployed',
               'OT Device Hardening Standard v1.0 published',
               'Vendor hardening checklist mandatory at commissioning',
               'Quarterly CIS Benchmark compliance audit scheduled',
               'Self-healing: Auto-disable default credentials on device join']
  }
 },
];

// ══ OT DEVICES ═══════════════════════════════════════════════
const DEVICES=[
  {id:'plc-01',      name:'PLC Unit 01',       icon:'⚙',  unit:'Hz',    normal:[48,52],   color:'#3d8fff'},
  {id:'hmi-01',      name:'HMI Terminal',      icon:'🖥',  unit:'req/s', normal:[1,8],     color:'#ffe033'},
  {id:'scada-01',    name:'SCADA Server',      icon:'🖧',  unit:'CPU%',  normal:[15,55],   color:'#ff9020'},
  {id:'rtu-01',      name:'RTU Field Unit',    icon:'📡',  unit:'mA',    normal:[4,20],    color:'#ff3055'},
  {id:'historian-01',name:'Process Historian', icon:'💾',  unit:'WPS',   normal:[10,80],   color:'#a855f7'},
  {id:'eng-ws',      name:'Engineering WS',    icon:'💻',  unit:'CPU%',  normal:[10,60],   color:'#00d97a'},
  {id:'sensor-net',  name:'Sensor Network',    icon:'🔌',  unit:'V',     normal:[220,240], color:'#66aaff'},
  {id:'firewall-ot', name:'OT Firewall',       icon:'🛡',  unit:'pkt/s', normal:[100,800], color:'#ff7a1a'},
];

// ══ GLOBAL STATE ═════════════════════════════════════════════
const G={
  // alert store: each entry = {id,threatId,time,status:'pending'|'tp'|'fp'|'closed',
  //   aiConf,mttd,mttr,cost,downtime,phase,controls,isLegitimate}
  alerts:[],
  // per-threat AI model state
  aiModels:{},  // threatId → {zThreshold,spikeThreshold,tpCount,fpCount,tuneCount,history[]}
  // self-healing controls
  controls:[],  // [{id,name,threat,trigger,riskDelta,status:'pending'|'applied',date}]
  // fine-tune DB
  ftDB:[],      // [{ts,threatId,trigger,change,fpBefore,fpAfter,status}]
  // metrics
  metrics:{
    totalAlerts:0, tpAlerts:0, fpAlerts:0,
    mttdSum:0, mttrSum:0, mttdCount:0, mttrCount:0,
    totalCost:0, totalDowntime:0,
    riskScore:10,
  },
  // chart data history (rolling 20 ticks)
  chartData:{
    alertVol:Array(20).fill(0),
    tpRate:Array(20).fill(0),
    fpRate:Array(20).fill(0),
    cost:Array(20).fill(0),
    risk:Array(20).fill(10),
  },
  // device simulation state
  ds:{},
  // IR state
  ir:{
    active:false, threat:null, phaseIdx:0,
    phaseStart:Date.now(), incidentStart:null,
    pbBlockIdx:0, pbStepIdx:0,
    pendingAlert:null,  // alert waiting triage
    autoPlayIdx:0,
  },
  // tuning wizard state
  tuning:{show:false, threatId:null},
  // selected threat for AI page
  aiSelectedThreat:null,
  // CISO time series
  cisoSeries:{risk:[],cost:[],ts:[]},
  irSpeed:900,
  tickInt:null,
};

// Init device state
DEVICES.forEach(d=>{
  G.ds[d.id]={
    value:rnd(...d.normal),
    history:Array(20).fill(0).map(()=>rnd(...d.normal)),
    status:'ok',affected:false,isolated:false,recovering:false,recovered:false,
  };
});

// Init AI models
THREATS.forEach(t=>{
  G.aiModels[t.id]={
    zThreshold:t.aiConfig.zThreshold,
    spikeThreshold:t.aiConfig.spikeThreshold,
    tpCount:0, fpCount:0, tuneCount:0,
    tpRate:t.aiConfig.baseTPRate,
    fpRate:t.aiConfig.baseFPRate,
    history:[], // [{ts,classification,conf,mttd,mttr,cost}]
    lastFPStreak:0,
  };
});

// ══ CHART INSTANCES ══════════════════════════════════════════
let charts={};
function mkChart(id,type,labels,datasets,opts={}){
  const ctx=document.getElementById(id);
  if(!ctx) return null;
  if(charts[id]) charts[id].destroy();
  charts[id]=new Chart(ctx,{
    type, data:{labels,datasets},
    options:{
      responsive:true,animation:{duration:200},
      plugins:{legend:{labels:{color:'#4a637a',font:{size:10}}},...(opts.plugins||{})},
      scales:{
        x:{ticks:{color:'#4a637a',font:{size:9}},grid:{color:'rgba(255,255,255,.04)'},...(opts.xScale||{})},
        y:{ticks:{color:'#4a637a',font:{size:9}},grid:{color:'rgba(255,255,255,.04)'},...(opts.yScale||{})},
        ...(opts.scales||{})
      },
      ...opts,
    }
  });
  return charts[id];
}
function updateChart(id,newData){
  if(!charts[id]) return;
  newData.forEach((d,i)=>{ if(charts[id].data.datasets[i]) charts[id].data.datasets[i].data=d; });
  charts[id].update('none');
}

const TS20=()=>Array(20).fill('').map((_,i)=>i===19?'now':`-${19-i}`);

function initCharts(){
  mkChart('chart-alert-vol','line',TS20(),[
    {label:'Alert Volume',data:[...G.chartData.alertVol],borderColor:'#3d8fff',backgroundColor:'rgba(61,143,255,.08)',fill:true,tension:.4,pointRadius:1,borderWidth:1.5}
  ]);
  mkChart('chart-tp-fp','line',TS20(),[
    {label:'TP Rate %',data:[...G.chartData.tpRate],borderColor:'#00d97a',tension:.4,pointRadius:1,borderWidth:1.5,fill:false},
    {label:'FP Rate %',data:[...G.chartData.fpRate],borderColor:'#ffb31a',tension:.4,pointRadius:1,borderWidth:1.5,fill:false},
  ]);
  mkChart('chart-cost','line',TS20(),[
    {label:'Cost $',data:[...G.chartData.cost],borderColor:'#ff3055',backgroundColor:'rgba(255,48,85,.07)',fill:true,tension:.4,pointRadius:1,borderWidth:1.5}
  ]);
  mkChart('chart-ai-accuracy','line',TS20(),[
    {label:'AI Accuracy %',data:Array(20).fill(0),borderColor:'#00d97a',tension:.4,pointRadius:2,borderWidth:2,fill:false},
    {label:'FP Rate %',data:Array(20).fill(0),borderColor:'#ffb31a',tension:.4,pointRadius:2,borderWidth:1.5,fill:false,borderDash:[3,3]},
  ]);
  mkChart('chart-ai-volume','bar',THREATS.map(t=>t.short.substring(0,10)),[
    {label:'Alerts',data:THREATS.map(()=>0),backgroundColor:THREATS.map(t=>t.color+'99'),borderColor:THREATS.map(t=>t.color),borderWidth:1}
  ],{plugins:{legend:{display:false}}});
  mkChart('chart-ai-fpr','line',TS20(),[
    {label:'FP Rate (rolling)',data:Array(20).fill(0),borderColor:'#ffb31a',tension:.4,pointRadius:1,borderWidth:1.5,fill:false},
  ],{plugins:{legend:{display:false}}});
  mkChart('chart-ciso-risk','line',TS20(),[
    {label:'Risk Score',data:[...G.chartData.risk],borderColor:'#ff3055',backgroundColor:'rgba(255,48,85,.08)',fill:true,tension:.4,pointRadius:2,borderWidth:2}
  ]);
  mkChart('chart-ciso-cost','line',TS20(),[
    {label:'Cost $',data:[...G.chartData.cost],borderColor:'#ff7a1a',backgroundColor:'rgba(255,122,26,.07)',fill:true,tension:.4,pointRadius:2,borderWidth:2}
  ]);
}

// ══ PAGE SWITCHING ════════════════════════════════════════════
function switchPage(id,btn){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(`page-${id}`).classList.add('active');
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  if(btn) btn.classList.add('active');
  if(id==='ai') renderAIPage();
  if(id==='ciso') renderCISOPage();
}

// ══ TOPBAR CLOCK ═════════════════════════════════════════════
setInterval(()=>{
  document.getElementById('tb-clock').textContent=new Date().toLocaleTimeString();
},1000);

// ══ ALERT SYSTEM ═════════════════════════════════════════════
let alertIdCounter=0;
function createAlert(threatId, isLegitimate){
  const t=THREATS.find(x=>x.id===threatId);
  const m=G.aiModels[threatId];
  // AI confidence: higher for TP, lower for FP
  const aiConf=isLegitimate
    ? Math.min(99,Math.round(75+Math.random()*22))
    : Math.round(35+Math.random()*30);
  const alert={
    id:`ALT-${String(++alertIdCounter).padStart(4,'0')}`,
    threatId, isLegitimate,
    time:new Date(),
    status:'pending',
    aiConf,
    phase:'detect',
    mttd:null, mttr:null, cost:null, downtime:null,
    controls:[],
    classification:null,
  };
  G.alerts.unshift(alert);
  G.metrics.totalAlerts++;
  updateSOCBadge();
  renderAlertFeed();
  updateSOCMetrics();
  updateAICharts();
  return alert;
}

function classifyAlert(type){
  const overlay=document.getElementById('triage-overlay');
  const alert=G.ir.pendingAlert;
  if(!alert) return;
  overlay.classList.remove('show');
  alert.status=type;
  alert.classification=type;
  const t=THREATS.find(x=>x.id===alert.threatId);
  const m=G.aiModels[alert.threatId];

  if(type==='tp'){
    G.metrics.tpAlerts++;
    m.tpCount++; m.fpRate=Math.max(0.02,m.fpRate-0.03); m.tpRate=Math.min(0.99,m.tpRate+0.01);
    m.lastFPStreak=0;
    document.getElementById('ioc-class').textContent='TRUE POSITIVE';
    document.getElementById('ioc-class').style.color='var(--crit)';
    // continue IR lifecycle
    continueIRAfterTriage(true);
  } else {
    G.metrics.fpAlerts++;
    m.fpCount++; m.lastFPStreak++;
    m.fpRate=Math.min(0.95,m.fpRate+0.04); m.tpRate=Math.max(0.4,m.tpRate-0.02);
    alert.status='fp';
    document.getElementById('ioc-class').textContent='FALSE POSITIVE';
    document.getElementById('ioc-class').style.color='var(--warn)';
    irAddEvent('detect',`⚠ Alert classified as FALSE POSITIVE by analyst`,
      `AI confidence was ${alert.aiConf}% — threshold review recommended`);
    // Check if FP streak triggers tuning
    if(m.lastFPStreak>=2) suggestTuning(alert.threatId);
    else {
      // legitimate activity — run briefly then close
      irAddEvent('post',`ℹ Legitimate activity confirmed — no further action`,
        `Pattern added to AI baseline for fine-tuning consideration`);
      resetIR();
    }
    updateSOCBadge();
    renderAlertFeed();
  }
  updateSOCMetrics();
  updateAICharts();
}

function continueIRAfterTriage(isTP){
  const alert=G.ir.pendingAlert;
  if(!isTP||!alert) return;
  const t=G.ir.threat;
  const s=G.irSpeed;
  const detectionTime=Date.now()-G.ir.incidentStart;
  alert.mttd=Math.round(detectionTime/1000);
  G.metrics.mttdSum+=alert.mttd; G.metrics.mttdCount++;

  // Mark devices affected
  t.devices.forEach(id=>{ if(G.ds[id]) G.ds[id].affected=true; });

  irSetPhase(2); // move to Analysis
  irRunPhaseSteps('analyze',s*0.8,()=>{
    irSetPhase(3);
    irRunPhaseSteps('contain',s*0.75,()=>{
      // physically contain devices
      t.devices.forEach(id=>{ if(G.ds[id]){G.ds[id].isolated=true;G.ds[id].affected=false;} });
      irSetPhase(4);
      irRunPhaseSteps('eradicate',s*0.7,()=>{
        irSetPhase(5);
        t.devices.forEach(id=>{
          if(G.ds[id]){G.ds[id].isolated=false;G.ds[id].recovering=true;}
        });
        irRunPhaseSteps('recover',s*0.8,()=>{
          // fully recover devices
          t.devices.forEach(id=>{
            if(G.ds[id]){
              G.ds[id].recovering=false;G.ds[id].recovered=true;
              const dev=DEVICES.find(d=>d.id===id);
              if(dev) G.ds[id].value=rnd(...dev.normal);
            }
          });
          irSetPhase(6);
          irRunPhaseSteps('post',s*0.7,()=>{
            // finalize incident
            const totalTime=Math.round((Date.now()-G.ir.incidentStart)/1000);
            alert.mttr=totalTime;
            alert.cost=t.baseCost+Math.round(Math.random()*t.baseCost*0.3);
            alert.downtime=t.downtimeMin*60+Math.round(Math.random()*300);
            alert.status='closed';
            G.metrics.mttrSum+=totalTime; G.metrics.mttrCount++;
            G.metrics.totalCost+=alert.cost;
            G.metrics.totalDowntime+=alert.downtime;
            // self-healing control
            applySelfHealingControl(t, alert);
            const mttrStr=fmtTime(totalTime);
            irAddEvent('post',`🟢 INCIDENT CLOSED — ${t.short}`,
              `MTTR: ${mttrStr} · Cost: $${fmtNum(alert.cost)} · Downtime: ${fmtTime(alert.downtime)}`);
            // log to AI model history
            G.aiModels[t.id].history.push({
              ts:new Date().toLocaleString(),
              classification:'TP',
              conf:alert.aiConf,
              mttd:alert.mttd,
              mttr:alert.mttr,
              cost:alert.cost,
              controls:alert.controls.length,
            });
            G.ir.active=false;
            document.getElementById('btn-ir-launch').disabled=false;
            document.getElementById('ir-active-count').textContent='0 ACTIVE';
            updateSOCMetrics();
            updateAICharts();
            renderCISOPage();
            renderAlertFeed();
          });
        });
      });
    });
  });
}

// ══ SELF-HEALING CONTROLS ════════════════════════════════════
const CONTROL_TEMPLATES={
  't1':['Auto-block on new unregistered MAC address detection',
        'Mandatory MFA for all external VPN sessions to OT'],
  't2':['Auto-patch workflow for critical CVEs on OT assets',
        'Virtual patching IPS rule auto-deploy on new CVE alert'],
  't3':['Automated firmware integrity check every 6 hours',
        'Mandatory code-signing verification for all OT firmware'],
  't4':['Auto rate-limit OT VLAN on flood detection (>5000 pkt/s)',
        'Automatic failover to manual control on network saturation'],
  't5':['Auto-lock OT account on after-hours login attempt',
        'Auto-enforce MFA re-auth after 4hrs idle in OT systems'],
  't6':['Automated behavioral baseline refresh every 24hrs',
        'Auto-alert on 30-day dormant C2 beacon pattern (APT hunting)'],
  't7':['Auto-VLAN quarantine on zone policy violation detection',
        'Automatic firewall ACL generation on cross-zone anomaly'],
  't8':['Auto-isolate workstation on macro execution in OT domain',
        'Auto-disable USB ports on malware detection alert'],
  't9':['Auto read-only mode on anomalous Modbus write pattern',
        'Auto-block Modbus master on replay sequence detection'],
  't10':['Auto-disable default credentials on new device network join',
         'Auto-service audit on configuration change without ticket'],
};

function applySelfHealingControl(threat, alert){
  const templates=CONTROL_TEMPLATES[threat.id]||[];
  const ctrl={
    id:`CTRL-${String(G.controls.length+1).padStart(3,'0')}`,
    name:templates[G.controls.filter(c=>c.threat===threat.id).length%templates.length]||'Auto-harden policy updated',
    threat:threat.id, threatShort:threat.short,
    trigger:`Incident ${alert.id}`,
    riskDelta:-Math.round(3+Math.random()*7),
    status:'applied',
    date:new Date().toLocaleDateString(),
  };
  G.controls.push(ctrl);
  alert.controls.push(ctrl.name);
  // adjust risk score
  G.metrics.riskScore=Math.max(5,Math.min(95,
    G.metrics.riskScore + (G.metrics.tpAlerts>0?5:-2) + ctrl.riskDelta
  ));
  renderSOCControls();
  updateCISOCharts();
}

// ══ AI TUNING ════════════════════════════════════════════════
function suggestTuning(threatId){
  const t=THREATS.find(x=>x.id===threatId);
  const m=G.aiModels[threatId];
  G.tuning={show:true, threatId};
  const fp=Math.round(m.fpRate*100);
  const proposed=[
    `Raise Z-score detection threshold: ${m.zThreshold.toFixed(1)} → ${(m.zThreshold+0.3).toFixed(1)} (less sensitive to minor noise)`,
    `Add time-of-day whitelist: suppress alerts during maintenance windows 02:00–04:00`,
    `Require corroboration: alert only if 2+ indicators fire simultaneously`,
    `Add ${t.short} legitimate-activity fingerprint to baseline model`,
  ];
  document.getElementById('tuning-threat-name').textContent=t.short;
  document.getElementById('tw-analysis').innerHTML=
    `<b>FP streak: ${m.lastFPStreak} consecutive false positives</b> for <b>${t.short}</b>.<br>
    Current FP rate: ${fp}% (threshold for auto-suggestion: >40%).<br>
    These alerts may represent <b>legitimate operational activity</b> being misclassified.<br>
    Proposed adjustments to reduce noise while maintaining detection coverage:`;
  const propEl=document.getElementById('tw-proposals');
  propEl.innerHTML=proposed.map(p=>`<div class="info-box" style="padding:6px 10px;font-size:.73rem;margin-bottom:0">• ${p}</div>`).join('');
  document.getElementById('tuning-wizard').classList.add('show');
  irAddEvent('analyze',`🔧 AI TUNING SUGGESTED — ${t.short}`,
    `FP streak: ${m.lastFPStreak} · FP rate: ${fp}% · Review tuning recommendations on AI Engine page`);
  if(document.getElementById('page-ai').classList.contains('active')) renderAIPage();
}

function applyTuning(){
  const threatId=G.tuning.threatId;
  const m=G.aiModels[threatId];
  const t=THREATS.find(x=>x.id===threatId);
  const fpBefore=+(m.fpRate*100).toFixed(1);
  m.zThreshold=+(m.zThreshold+0.3).toFixed(2);
  m.spikeThreshold=+(m.spikeThreshold+0.05).toFixed(2);
  m.fpRate=Math.max(0.03,m.fpRate-0.15);
  m.tpRate=Math.min(0.99,m.tpRate+0.03);
  m.lastFPStreak=0;
  m.tuneCount++;
  const fpAfter=+(m.fpRate*100).toFixed(1);
  G.ftDB.unshift({
    ts:new Date().toLocaleString(),
    threatId, threatShort:t.short,
    trigger:`FP streak ≥ ${m.lastFPStreak+2}`,
    change:`Z-threshold +0.3, spike +0.05, add maintenance window whitelist`,
    fpBefore:`${fpBefore}%`, fpAfter:`${fpAfter}%`,
    status:'applied',
  });
  document.getElementById('tuning-wizard').classList.remove('show');
  G.tuning.show=false;
  irAddEvent('post',`✅ AI MODEL FINE-TUNED — ${t.short}`,
    `FP rate: ${fpBefore}% → ${fpAfter}% · Z-threshold raised to ${m.zThreshold} · Baseline updated`);
  updateAICharts();
  renderAIPage();
  if(G.ir.active===false) resetIR();
}

function dismissTuning(){
  document.getElementById('tuning-wizard').classList.remove('show');
  G.tuning.show=false;
  if(G.ir.active===false) resetIR();
}

// ══ IR LIFECYCLE ═════════════════════════════════════════════
function buildIRThreatList(){
  const el=document.getElementById('ir-threat-list');
  el.innerHTML='';
  const select=document.getElementById('ir-attack-sel');
  select.innerHTML='';
  const threatFilter=document.getElementById('soc-threat-filter');
  threatFilter.innerHTML='<option value="all">All Threats</option>';
  THREATS.forEach(t=>{
    // threat list item
    const div=document.createElement('div');
    div.className='ir-threat-item'+(G.ir.threat&&G.ir.threat.id===t.id?' selected':'')+(G.ir.active&&G.ir.threat&&G.ir.threat.id===t.id?' firing':'');
    div.style.setProperty('--tc',t.color);
    div.id=`iti-${t.id}`;
    div.onclick=()=>{ document.getElementById('ir-attack-sel').value=t.id; };
    const tierLabel=t.tier===1?'CRITICAL':t.tier===2?'HIGH':'MEDIUM';
    const tierCls=t.tier===1?'badge-t1':t.tier===2?'badge-t2':'badge-t3';
    const m=G.aiModels[t.id];
    const fpPct=Math.round(m.fpRate*100);
    div.innerHTML=`
      <div class="iti-rank">#${t.rank} — ${t.attackType}</div>
      <div style="font-size:.8rem;font-weight:600;margin:2px 0;line-height:1.2">${t.short}</div>
      <div class="iti-meta">
        <span class="badge ${tierCls}">${tierLabel}</span>
        <span style="font-size:.62rem;color:var(--txt3)">CVSSv3: ${t.cvss}</span>
        <span style="font-size:.62rem;color:${fpPct>30?'var(--warn)':'var(--ok)'}">FP: ${fpPct}%</span>
      </div>`;
    el.appendChild(div);
    // select option
    const opt=document.createElement('option');
    opt.value=t.id; opt.textContent=`#${t.rank} — ${t.short}`;
    select.appendChild(opt);
    // threat filter
    const fopt=document.createElement('option');
    fopt.value=t.id; fopt.textContent=t.short;
    threatFilter.appendChild(fopt);
  });
}

function buildIRPipeline(){
  const el=document.getElementById('ir-phase-pipeline');
  el.innerHTML='';
  PHASES.forEach((p,i)=>{
    const div=document.createElement('div');
    div.className='ipp'; div.id=`ipp-${p.id}`;
    div.style.setProperty('--pc',p.color);
    div.innerHTML=`<div class="ipp-dot"></div>
      <div class="ipp-lbl">${p.short}</div>
      <div class="ipp-prog"><div class="ipp-prog-fill" id="ippf-${p.id}" style="background:${p.color}"></div></div>`;
    el.appendChild(div);
  });
  irSetPhase(0);
}

function buildIRDeviceBar(){
  const el=document.getElementById('ir-device-bar');
  el.innerHTML='';
  DEVICES.forEach(d=>{
    const s=G.ds[d.id];
    const div=document.createElement('div');
    div.className='idev'; div.id=`idev-${d.id}`;
    div.innerHTML=`<div class="idev-icon">${d.icon}</div>
      <div class="idev-name">${d.name}</div>
      <div class="idev-val" id="ival-${d.id}" style="color:${d.color}">${s.value.toFixed(1)}</div>
      <div class="idev-unit">${d.unit}</div>`;
    el.appendChild(div);
  });
}

function irSetPhase(idx){
  G.ir.phaseIdx=idx;
  G.ir.phaseStart=Date.now();
  G.ir.pbBlockIdx=0; G.ir.pbStepIdx=0;
  PHASES.forEach((p,i)=>{
    const el=document.getElementById(`ipp-${p.id}`);
    const fill=document.getElementById(`ippf-${p.id}`);
    if(!el) return;
    el.classList.remove('active','done');
    if(i<idx){el.classList.add('done');if(fill)fill.style.width='100%';}
    else if(i===idx){
      el.classList.add('active');
      if(fill){fill.style.width='0%';}
      // animate
      let pr=0; const iv=setInterval(()=>{
        pr=Math.min(pr+1,100); if(fill)fill.style.width=pr+'%';
        if(pr>=100)clearInterval(iv);
      },35);
    } else {if(fill)fill.style.width='0%';}
  });
  const p=PHASES[idx];
  document.getElementById('idb-phase-name').textContent=p.name.toUpperCase();
  document.getElementById('idb-phase-name').style.color=p.color;
  document.getElementById('idb-phase-desc').textContent=G.ir.threat?p.desc:PHASES[0].desc;
  document.getElementById('tb-status').textContent=idx>=3&&idx<=4?'INCIDENT ACTIVE':idx>=5?'RECOVERING':'MONITORING';
  document.getElementById('tb-status').className='tb-pill '+(idx>=3&&idx<=4?'pill-crit':idx>=5?'pill-warn':'pill-ok');
}

function irRunPhaseSteps(phaseKey, interval, onDone){
  const t=G.ir.threat;
  if(!t) return onDone();
  const steps=t.phases[phaseKey]||[];
  const phaseObj=PHASES.find(p=>p.id===phaseKey);
  let i=0;
  const go=()=>{
    if(i>=steps.length){ onDone(); return; }
    irAddEvent(phaseKey, steps[i]);
    irBuildPlaybook(phaseKey, i);
    updateIRDeviceBar();
    i++;
    setTimeout(go,interval);
  };
  go();
}

function irAddEvent(phaseId, msg, detail){
  const p=PHASES.find(x=>x.id===phaseId)||PHASES[G.ir.phaseIdx];
  const feed=document.getElementById('ir-event-feed');
  const div=document.createElement('div');
  div.className='ir-ev';
  const tname=G.ir.threat?G.ir.threat.attackType:'SYSTEM';
  div.innerHTML=`
    <div class="ir-ev-dot" style="background:${p.color}"></div>
    <div style="flex:1">
      <div style="display:flex;align-items:center;gap:7px;margin-bottom:2px;flex-wrap:wrap">
        <span class="ir-ev-time">${new Date().toLocaleTimeString()}</span>
        <span class="phase-chip" style="background:${p.color}22;color:${p.color}">${p.short}</span>
        ${G.ir.threat?`<span style="font-size:.62rem;color:var(--txt3);font-style:italic">${tname}</span>`:''}
      </div>
      <div class="ir-ev-msg">${msg}</div>
      ${detail?`<div class="ir-ev-detail">${detail}</div>`:''}
    </div>`;
  feed.prepend(div);
  while(feed.children.length>100)feed.removeChild(feed.lastChild);
}

function irBuildPlaybook(activePhase, stepIdx){
  const t=G.ir.threat;
  const el=document.getElementById('ir-playbook');
  if(!el) return;
  if(!t){el.innerHTML='<div style="padding:12px;font-size:.75rem;color:var(--txt3)">Select a scenario to view the playbook.</div>';return;}
  el.innerHTML='';
  const phaseKeys=['detect','analyze','contain','eradicate','recover','post'];
  const activeIdx=phaseKeys.indexOf(activePhase);
  phaseKeys.forEach((key,bi)=>{
    const steps=t.phases[key]||[];
    const phaseObj=PHASES.find(p=>p.id===key)||PHASES[1+bi];
    const isDone=bi<activeIdx;
    const isActive=bi===activeIdx;
    const block=document.createElement('div');
    block.className='pb-block';
    block.innerHTML=`<div class="pb-block-hdr">
      <div style="width:14px;height:14px;border-radius:3px;background:${isDone?'rgba(0,217,122,.15)':isActive?phaseObj.color+'22':'rgba(255,255,255,.04)'};display:flex;align-items:center;justify-content:center;font-size:.65rem">
        ${isDone?`<span style="color:var(--ok)">✓</span>`:isActive?`<span style="color:${phaseObj.color}">▶</span>`:'<span style="color:var(--txt3)">○</span>'}
      </div>
      <div class="pb-block-name" style="color:${isDone?'var(--ok)':isActive?phaseObj.color:'var(--txt3)'}">${phaseObj.name.toUpperCase()}</div>
    </div>
    ${steps.map((s,si)=>{
      const done=isDone||(isActive&&si<stepIdx);
      const active=isActive&&si===stepIdx;
      return `<div class="pb-step ${done?'done':active?'active':''}">
        <span class="n">${done?'✓':active?'▸':(si+1).toString().padStart(2,'0')}</span>
        <span class="t">${s}</span>
      </div>`;
    }).join('')}`;
    el.appendChild(block);
  });
}

function updateIRDeviceBar(){
  DEVICES.forEach(d=>{
    const s=G.ds[d.id];
    const card=document.getElementById(`idev-${d.id}`);
    const val=document.getElementById(`ival-${d.id}`);
    if(!card) return;
    val.textContent=s.value.toFixed(1);
    card.className='idev';
    if(s.recovered)card.classList.add('recovered');
    else if(s.recovering)card.classList.add('recovering');
    else if(s.isolated)card.classList.add('isolated');
    else if(s.affected)card.classList.add('affected');
  });
}

// ══ LAUNCH IR SCENARIO ═══════════════════════════════════════
function launchIR(){
  if(G.ir.active) return;
  const sel=document.getElementById('ir-attack-sel').value;
  const t=THREATS.find(x=>x.id===sel);
  if(!t) return;
  G.ir.active=true; G.ir.threat=t; G.ir.incidentStart=Date.now();
  document.getElementById('btn-ir-launch').disabled=true;
  document.getElementById('ir-active-count').textContent='1 ACTIVE';
  buildIRThreatList();

  // Create alert (pending triage)
  const alert=createAlert(t.id, true); // all launched scenarios are real attacks
  G.ir.pendingAlert=alert;

  // Detection phase first
  irSetPhase(1);
  const s=G.irSpeed;
  setTimeout(()=>{
    irRunPhaseSteps('detect',s*0.6,()=>{
      // after detection steps, show triage modal
      setTimeout(()=>showTriageModal(t, alert), 300);
    });
  },s*0.5);

  // Update IOCs
  document.getElementById('ioc-threat').textContent=t.name;
  document.getElementById('ioc-threat').style.color=t.color;
  document.getElementById('ioc-vector').textContent=t.vector;
  document.getElementById('ioc-vector').style.color='var(--crit)';
  document.getElementById('ioc-asset').textContent=t.devices.map(id=>DEVICES.find(d=>d.id===id)?.name||id).join(', ');
  document.getElementById('ioc-cvss').textContent=t.cvss;
  document.getElementById('ioc-cvss').style.color=t.cvss>=9?'var(--crit)':'var(--warn)';
  document.getElementById('ioc-conf').textContent=`${alert.aiConf}% (AI Engine)`;
  document.getElementById('ioc-conf').style.color=alert.aiConf>70?'var(--crit)':'var(--warn)';
  document.getElementById('ioc-iec').textContent=t.iec;

  irAddEvent('prepare',`🔴 SCENARIO: ${t.name}`,`Attack type: ${t.attackType} · CVSSv3: ${t.cvss}`);
}

function showTriageModal(t, alert){
  const overlay=document.getElementById('triage-overlay');
  const m=G.aiModels[t.id];
  document.getElementById('triage-title').textContent=`🔍 Alert Triage — ${t.short}`;
  document.getElementById('triage-desc').innerHTML=
    `AI Engine has raised alert <b>${alert.id}</b> for <b>${t.name}</b>.<br>
    AI Confidence: <b style="color:${alert.aiConf>70?'var(--crit)':'var(--warn)'}">${alert.aiConf}%</b> &nbsp;|&nbsp; 
    Historical FP rate for this threat: <b style="color:${m.fpRate>0.3?'var(--warn)':'var(--ok)'}">${Math.round(m.fpRate*100)}%</b><br>
    Classify this alert to determine the IR response:`;
  document.getElementById('triage-context').innerHTML=
    `<b>Attack Vector:</b> ${t.vector}<br>
    <b>Affected Assets:</b> ${t.devices.map(id=>DEVICES.find(d=>d.id===id)?.name||id).join(', ')}<br>
    <b>CVSS Score:</b> ${t.cvss} · <b>IEC Reference:</b> ${t.iec}<br>
    <b>AI Reasoning:</b> Z-score exceeded ${m.zThreshold.toFixed(1)}σ threshold, spike amplitude >40%. ${m.fpRate>0.25?`⚠ Note: ${Math.round(m.fpRate*100)}% historical FP rate — exercise caution.`:'Pattern consistent with known attack signature.'}`;
  overlay.classList.add('show');
}

function resetIR(){
  G.ir.active=false; G.ir.threat=null; G.ir.phaseIdx=0;
  G.ir.pbBlockIdx=0; G.ir.pbStepIdx=0; G.ir.pendingAlert=null;
  DEVICES.forEach(d=>{
    G.ds[d.id].affected=false;G.ds[d.id].isolated=false;
    G.ds[d.id].recovering=false;G.ds[d.id].recovered=false;
  });
  document.getElementById('btn-ir-launch').disabled=false;
  document.getElementById('ir-active-count').textContent='0 ACTIVE';
  document.getElementById('triage-overlay').classList.remove('show');
  buildIRThreatList();
  buildIRPipeline();
  buildIRDeviceBar();
  irBuildPlaybook('detect',0);
  ['ioc-threat','ioc-vector','ioc-asset','ioc-cvss','ioc-conf','ioc-class','ioc-iec'].forEach(id=>{
    const el=document.getElementById(id);
    if(el){el.textContent='—';el.style.color='var(--txt3)';}
  });
  irAddEvent('prepare','🔵 System reset. Ready for next scenario.','');
}

function setIRSpeed(v){
  G.irSpeed=parseInt(v);
  document.getElementById('ir-speed-lbl').textContent=(v/1000).toFixed(1)+'s';
}

// ══ SOC ALERT FEED ════════════════════════════════════════════
function renderAlertFeed(){
  const filter=document.getElementById('soc-filter')?.value||'all';
  const tFilter=document.getElementById('soc-threat-filter')?.value||'all';
  let alerts=[...G.alerts];
  if(filter!=='all') alerts=alerts.filter(a=>a.status===filter);
  if(tFilter!=='all') alerts=alerts.filter(a=>a.threatId===tFilter);
  const feed=document.getElementById('soc-alert-feed');
  if(!feed) return;
  const tp=G.alerts.filter(a=>a.status==='tp'||a.status==='closed'&&a.classification==='tp').length;
  const fp=G.alerts.filter(a=>a.status==='fp').length;
  document.getElementById('soc-total').textContent=G.alerts.length;
  document.getElementById('soc-tp-count').textContent=tp;
  document.getElementById('soc-fp-count').textContent=fp;
  document.getElementById('m-active-alerts').textContent=G.alerts.filter(a=>a.status==='pending').length;
  const badge=document.getElementById('badge-soc');
  const pendingCount=G.alerts.filter(a=>a.status==='pending').length;
  badge.style.display=pendingCount>0?'':'none';
  badge.textContent=pendingCount;
  feed.innerHTML='';
  if(alerts.length===0){
    feed.innerHTML='<div style="padding:20px;text-align:center;font-size:.8rem;color:var(--txt3)">No alerts match the current filter.</div>';
    return;
  }
  alerts.forEach(a=>{
    const t=THREATS.find(x=>x.id===a.threatId)||{short:'Unknown',color:'var(--txt3)',tier:1};
    const div=document.createElement('div');
    div.className=`alert-item ${a.status}`;
    const statusBadge=a.status==='pending'?'<span class="badge badge-pending">PENDING</span>':
      a.status==='tp'||a.classification==='tp'?'<span class="badge badge-tp">TRUE POS</span>':
      a.status==='fp'?'<span class="badge badge-fp">FALSE POS</span>':
      '<span class="badge badge-closed">CLOSED</span>';
    div.innerHTML=`
      <div class="ai-dot" style="background:${t.color}"></div>
      <div style="flex:1;min-width:0">
        <div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap;margin-bottom:3px">
          <span style="font-family:var(--font-mono);font-size:.68rem;color:var(--txt3)">${a.id}</span>
          ${statusBadge}
          <span class="badge ${t.tier===1?'badge-t1':t.tier===2?'badge-t2':'badge-t3'}">#${t.rank||'?'} ${t.short}</span>
          <span style="font-size:.68rem;color:${a.aiConf>70?'var(--crit)':'var(--warn)'}">AI: ${a.aiConf}%</span>
          <span style="margin-left:auto;font-size:.68rem;color:var(--txt3)">${a.time.toLocaleTimeString()}</span>
        </div>
        <div style="font-size:.78rem;line-height:1.35">${t.name||'Unknown Threat'}</div>
        <div style="display:flex;gap:12px;margin-top:4px;font-size:.7rem;color:var(--txt3);flex-wrap:wrap">
          ${a.mttd!==null?`<span>MTTD: <b style="color:var(--txt2)">${fmtTime(a.mttd)}</b></span>`:''}
          ${a.mttr!==null?`<span>MTTR: <b style="color:var(--txt2)">${fmtTime(a.mttr)}</b></span>`:''}
          ${a.cost!==null?`<span>Cost: <b style="color:var(--warn)">$${fmtNum(a.cost)}</b></span>`:''}
          ${a.downtime!==null?`<span>Downtime: <b style="color:var(--purple)">${fmtTime(a.downtime)}</b></span>`:''}
          ${a.controls.length?`<span>Controls: <b style="color:var(--ok)">${a.controls.length} applied</b></span>`:''}
        </div>
      </div>`;
    feed.appendChild(div);
  });
}

function clearFPAlerts(){
  G.alerts=G.alerts.filter(a=>a.status!=='fp');
  renderAlertFeed();
}

function updateSOCBadge(){
  const count=G.alerts.filter(a=>a.status==='pending').length;
  const badge=document.getElementById('badge-soc');
  if(badge){badge.style.display=count>0?'':'none';badge.textContent=count;}
}

// ══ SOC METRICS ═══════════════════════════════════════════════
function updateSOCMetrics(){
  const m=G.metrics;
  const mttd=m.mttdCount>0?fmtTime(Math.round(m.mttdSum/m.mttdCount)):'—';
  const mttr=m.mttrCount>0?fmtTime(Math.round(m.mttrSum/m.mttrCount)):'—';
  const tp=m.tpAlerts; const fp=m.fpAlerts; const total=tp+fp;
  const acc=total>0?Math.round(tp/total*100)+'%':'—';
  document.getElementById('m-mttd').textContent=mttd;
  document.getElementById('m-mttr').textContent=mttr;
  document.getElementById('m-accuracy').textContent=acc;
  document.getElementById('m-cost').textContent='$'+fmtNum(m.totalCost);
  document.getElementById('m-downtime').textContent=fmtTime(m.totalDowntime);
  // chart data push
  G.chartData.alertVol.push(G.metrics.totalAlerts); G.chartData.alertVol.shift();
  const tpr=total>0?Math.round(tp/total*100):0;
  const fpr=total>0?Math.round(fp/total*100):0;
  G.chartData.tpRate.push(tpr); G.chartData.tpRate.shift();
  G.chartData.fpRate.push(fpr); G.chartData.fpRate.shift();
  G.chartData.cost.push(m.totalCost); G.chartData.cost.shift();
  G.chartData.risk.push(m.riskScore); G.chartData.risk.shift();
  updateChart('chart-alert-vol',[G.chartData.alertVol]);
  updateChart('chart-tp-fp',[G.chartData.tpRate,G.chartData.fpRate]);
  updateChart('chart-cost',[G.chartData.cost]);
  updateChart('chart-ciso-risk',[G.chartData.risk]);
  updateChart('chart-ciso-cost',[G.chartData.cost]);
}

function renderSOCControls(){
  const el=document.getElementById('soc-controls-list');
  if(!el) return;
  el.innerHTML='';
  G.controls.slice(-6).reverse().forEach(c=>{
    const div=document.createElement('div');
    div.style.cssText='padding:6px 8px;background:rgba(0,217,122,.06);border:1px solid rgba(0,217,122,.15);border-radius:4px;font-size:.73rem;display:flex;gap:8px;align-items:center;';
    div.innerHTML=`<span style="color:var(--ok)">✓</span><span style="flex:1">${c.name}</span><span style="color:var(--txt3);font-size:.65rem">${c.date}</span>`;
    el.appendChild(div);
  });
  if(G.controls.length===0) el.innerHTML='<div style="font-size:.75rem;color:var(--txt3);padding:4px">No controls applied yet. Run an IR scenario to see self-healing in action.</div>';
}

// ══ AI PAGE ═══════════════════════════════════════════════════
function renderAIPage(){
  const el=document.getElementById('ai-threat-rows');
  if(!el) return;
  el.innerHTML='';
  let totalTP=0,totalFP=0,totalTune=0;
  THREATS.forEach(t=>{
    const m=G.aiModels[t.id];
    totalTP+=m.tpCount; totalFP+=m.fpCount; totalTune+=m.tuneCount;
    const fp=Math.round(m.fpRate*100);
    const tp=Math.round(m.tpRate*100);
    const total=m.tpCount+m.fpCount;
    const row=document.createElement('div');
    row.className='ai-threat-row'+(G.aiSelectedThreat===t.id?' selected':'');
    row.onclick=()=>{ G.aiSelectedThreat=t.id; renderAIPage(); };
    row.innerHTML=`
      <div style="min-width:18px;font-size:.65rem;color:${t.color};font-family:var(--font-mono)">#${t.rank}</div>
      <div style="flex:1;min-width:0">
        <div style="font-size:.76rem;font-weight:600;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${t.short}</div>
        <div class="ai-fp-bar" style="margin-top:4px">
          <div class="ai-fp-fill" style="width:${fp}%;background:${fp>30?'var(--warn)':'var(--ok)'}"></div>
        </div>
      </div>
      <div style="text-align:right;min-width:52px">
        <div style="font-size:.68rem;color:${tp>80?'var(--ok)':'var(--warn)'}">TP: ${tp}%</div>
        <div style="font-size:.68rem;color:${fp>30?'var(--warn)':'var(--txt3)'}">FP: ${fp}%</div>
        <div style="font-size:.6rem;color:var(--txt3)">${total} alerts</div>
      </div>`;
    el.appendChild(row);
  });
  document.getElementById('ai-global-tpr').textContent=totalTP+totalFP>0?Math.round(totalTP/(totalTP+totalFP)*100)+'%':'—';
  document.getElementById('ai-global-fpr').textContent=totalTP+totalFP>0?Math.round(totalFP/(totalTP+totalFP)*100)+'%':'—';
  document.getElementById('ai-tune-count').textContent=totalTune;
  document.getElementById('ai-controls-count').textContent=G.controls.length;
  // fine-tune DB
  const tbody=document.getElementById('ftdb-tbody');
  if(tbody){
    tbody.innerHTML='';
    if(G.ftDB.length===0){
      tbody.innerHTML='<tr><td colspan="7" style="text-align:center;color:var(--txt3);padding:12px">No tuning events yet. Trigger false positive streaks to see AI fine-tuning in action.</td></tr>';
    } else {
      G.ftDB.forEach(r=>{
        const tr=document.createElement('tr');
        tr.innerHTML=`<td style="font-family:var(--font-mono);font-size:.68rem">${r.ts}</td>
          <td>${r.threatShort}</td><td style="font-size:.72rem;color:var(--warn)">${r.trigger}</td>
          <td style="font-size:.72rem">${r.change}</td>
          <td style="font-family:var(--font-mono);color:var(--crit)">${r.fpBefore}</td>
          <td style="font-family:var(--font-mono);color:var(--ok)">${r.fpAfter}</td>
          <td><span class="badge badge-ok">${r.status}</span></td>`;
        tbody.appendChild(tr);
      });
    }
  }
  // alert history
  const selT=G.aiSelectedThreat?THREATS.find(x=>x.id===G.aiSelectedThreat):null;
  document.getElementById('ai-hist-threat').textContent=selT?selT.short:'Select a threat on the left';
  const histTbody=document.getElementById('ai-hist-tbody');
  if(histTbody){
    const model=selT?G.aiModels[selT.id]:null;
    const hist=model?model.history:[];
    if(hist.length===0){
      histTbody.innerHTML='<tr><td colspan="9" style="text-align:center;color:var(--txt3);padding:12px">No history yet for this threat. Run a scenario to generate data.</td></tr>';
    } else {
      histTbody.innerHTML='';
      hist.forEach((h,i)=>{
        const tr=document.createElement('tr');
        tr.innerHTML=`<td style="font-family:var(--font-mono);font-size:.68rem">${i+1}</td>
          <td style="font-size:.68rem">${h.ts}</td>
          <td>${selT?.short}</td>
          <td style="font-family:var(--font-mono);color:${h.conf>70?'var(--crit)':'var(--warn)'}">${h.conf}%</td>
          <td><span class="badge ${h.classification==='TP'?'badge-tp':'badge-fp'}">${h.classification}</span></td>
          <td>${fmtTime(h.mttd)}</td><td>${fmtTime(h.mttr)}</td>
          <td style="color:var(--warn)">$${fmtNum(h.cost)}</td>
          <td style="color:var(--ok)">${h.controls}</td>`;
        histTbody.appendChild(tr);
      });
    }
  }
  updateAICharts();
}

function updateAICharts(){
  // volume by threat
  const vols=THREATS.map(t=>G.aiModels[t.id].tpCount+G.aiModels[t.id].fpCount);
  updateChart('chart-ai-volume',[vols]);
  // accuracy over time for selected threat
  const m=G.aiSelectedThreat?G.aiModels[G.aiSelectedThreat]:null;
  if(m&&m.history.length>1){
    const tpArr=m.history.map((_,i)=>{
      const sub=m.history.slice(0,i+1);
      const tp=sub.filter(x=>x.classification==='TP').length;
      return Math.round(tp/sub.length*100);
    });
    const fpArr=m.history.map((_,i)=>{
      const sub=m.history.slice(0,i+1);
      const fp=sub.filter(x=>x.classification==='FP').length;
      return Math.round(fp/sub.length*100);
    });
    const labels=m.history.map((h,i)=>`#${i+1}`);
    if(charts['chart-ai-accuracy']){
      charts['chart-ai-accuracy'].data.labels=labels;
      charts['chart-ai-accuracy'].data.datasets[0].data=tpArr;
      charts['chart-ai-accuracy'].data.datasets[1].data=fpArr;
      charts['chart-ai-accuracy'].update('none');
    }
  }
  // FP rate rolling
  const allModels=THREATS.map(t=>G.aiModels[t.id]);
  const avgFP=allModels.reduce((a,m)=>a+m.fpRate,0)/allModels.length;
  G.chartData.fpRate.push(Math.round(avgFP*100));
  G.chartData.fpRate.shift();
  updateChart('chart-ai-fpr',[G.chartData.fpRate]);
}

// ══ CISO PAGE ════════════════════════════════════════════════
function renderCISOPage(){
  const m=G.metrics;
  // Risk score ring
  const risk=m.riskScore;
  const ring=document.getElementById('risk-ring');
  const circumference=226.2;
  ring.style.strokeDashoffset=circumference*(1-risk/100);
  const rColor=risk>70?'#ff3055':risk>40?'#ffb31a':'#00d97a';
  ring.style.stroke=rColor;
  document.getElementById('ciso-risk-score').textContent=Math.round(risk);
  document.getElementById('ciso-risk-score').style.color=rColor;
  document.getElementById('ciso-risk-label').textContent=risk>70?'HIGH RISK':risk>40?'MODERATE RISK':'LOW RISK';

  // Risk factors
  const rfEl=document.getElementById('ciso-risk-factors');
  if(rfEl){
    const factors=[
      {label:'Unresolved incidents',val:G.alerts.filter(a=>a.status==='pending').length,crit:3},
      {label:'Active threats',val:G.ir.active?1:0,crit:1},
      {label:'Controls gap',val:Math.max(0,10-G.controls.length),crit:5},
      {label:'AI FP rate',val:Math.round(Object.values(G.aiModels).reduce((a,m)=>a+m.fpRate,0)/THREATS.length*100)+'%',crit:null},
    ];
    rfEl.innerHTML=factors.map(f=>`
      <div style="display:flex;justify-content:space-between;font-size:.74rem;padding:3px 0;border-bottom:1px solid rgba(255,255,255,.05)">
        <span style="color:var(--txt2)">${f.label}</span>
        <span style="color:${f.crit&&f.val>=f.crit?'var(--crit)':'var(--ok)'};font-family:var(--font-mono)">${f.val}</span>
      </div>`).join('');
  }
  // Costs
  const downCost=Math.round(m.totalDowntime/60*2500); // $2500/min OT downtime
  const labourCost=G.alerts.filter(a=>a.status==='closed'||a.classification==='tp').length*4500;
  const regRisk=Math.round(m.totalCost*0.15);
  const avoided=Math.round(G.controls.length*18000+G.metrics.tpAlerts*12000);
  document.getElementById('ciso-total-cost').textContent='$'+fmtNum(m.totalCost);
  document.getElementById('ciso-downtime-cost').textContent='$'+fmtNum(downCost);
  document.getElementById('ciso-labour-cost').textContent='$'+fmtNum(labourCost);
  document.getElementById('ciso-reg-cost').textContent='$'+fmtNum(regRisk);
  document.getElementById('ciso-avoided').textContent='$'+fmtNum(avoided);
  // Compliance
  const compBars=document.getElementById('ciso-compliance-bars');
  if(compBars){
    const controls=G.controls.length;
    const comps=[
      {label:'IEC 62443 L1',pct:Math.min(100,40+controls*6),color:'var(--info)'},
      {label:'IEC 62443 L2',pct:Math.min(100,20+controls*5),color:'var(--warn)'},
      {label:'NIST CSF',pct:Math.min(100,55+m.tpAlerts*4),color:'var(--ok)'},
      {label:'ISO 27001',pct:Math.min(100,35+controls*5),color:'var(--purple)'},
      {label:'NIS2 Directive',pct:Math.min(100,30+controls*7+m.tpAlerts*3),color:'var(--info)'},
    ];
    compBars.innerHTML=comps.map(c=>`
      <div class="cb-row">
        <span class="cb-label">${c.label}</span>
        <div class="pbar-wrap" style="flex:1">
          <div class="pbar-fill" style="width:${c.pct}%;background:${c.color}"></div>
        </div>
        <span class="cb-pct" style="color:${c.color}">${Math.round(c.pct)}%</span>
      </div>`).join('');
  }
  // KPIs
  const kpiEl=document.getElementById('ciso-kpis');
  if(kpiEl){
    const tp=m.tpAlerts; const fp=m.fpAlerts; const total=tp+fp;
    const acc=total>0?Math.round(tp/total*100):0;
    const kpis=[
      {label:'Total Incidents',val:m.tpAlerts,color:'var(--crit)',sub:'Confirmed TP'},
      {label:'AI Accuracy',val:acc+'%',color:'var(--ok)',sub:'Alert precision'},
      {label:'Avg MTTD',val:m.mttdCount>0?fmtTime(Math.round(m.mttdSum/m.mttdCount)):'—',color:'var(--warn)',sub:'Detection speed'},
      {label:'Avg MTTR',val:m.mttrCount>0?fmtTime(Math.round(m.mttrSum/m.mttrCount)):'—',color:'var(--info)',sub:'Response speed'},
    ];
    kpiEl.innerHTML=kpis.map(k=>`
      <div class="metric-tile" style="--mt-color:${k.color}">
        <div class="mt-label">${k.label}</div>
        <div class="mt-value">${k.val}</div>
        <div class="mt-sub">${k.sub}</div>
      </div>`).join('');
  }
  // Controls table
  const ctbody=document.getElementById('ciso-controls-tbody');
  if(ctbody){
    if(G.controls.length===0){
      ctbody.innerHTML='<tr><td colspan="5" style="color:var(--txt3);text-align:center;padding:12px">No self-healing controls applied yet.</td></tr>';
    } else {
      ctbody.innerHTML=G.controls.map(c=>`<tr>
        <td style="font-size:.77rem">${c.name}</td>
        <td><span class="badge badge-tp">${c.threatShort}</span></td>
        <td style="color:var(--ok);font-family:var(--font-mono)">${c.riskDelta}pts</td>
        <td><span class="badge badge-ok">APPLIED</span></td>
        <td style="font-size:.68rem;color:var(--txt3)">${c.date}</td>
      </tr>`).join('');
    }
  }
  // Recommendations
  const recEl=document.getElementById('ciso-recommendations');
  if(recEl){
    const recs=[];
    if(G.controls.length<5) recs.push({icon:'🛡',text:'Deploy 5+ self-healing controls to reduce risk score by ~35 points',urgency:'warn'});
    if(m.tpAlerts===0) recs.push({icon:'⚡',text:'Run at least 3 IR scenarios to generate baseline metrics for board reporting',urgency:'info'});
    const highFP=THREATS.filter(t=>G.aiModels[t.id].fpRate>0.35);
    if(highFP.length>0) recs.push({icon:'🤖',text:`AI fine-tuning needed: ${highFP.map(t=>t.short).join(', ')} have >35% FP rate`,urgency:'warn'});
    if(m.riskScore>50) recs.push({icon:'🔴',text:'Risk score >50: immediate board escalation recommended per NIS2 Article 20',urgency:'crit'});
    recs.push({icon:'📋',text:'Schedule quarterly OT penetration test and IEC 62443-3-2 zone assessment',urgency:'info'});
    recEl.innerHTML=recs.map(r=>`
      <div class="info-box ${r.urgency}" style="padding:8px 10px">
        <span>${r.icon}</span> <span style="font-size:.76rem">${r.text}</span>
      </div>`).join('');
  }
  // Summary table
  const stbody=document.getElementById('ciso-summary-tbody');
  if(stbody){
    stbody.innerHTML='';
    THREATS.forEach(t=>{
      const model=G.aiModels[t.id];
      const th=model.history;
      const alerts=th.length;
      const tpH=th.filter(x=>x.classification==='TP').length;
      const fpH=th.filter(x=>x.classification==='FP').length;
      const acc=alerts>0?Math.round(tpH/alerts*100)+'%':'—';
      const avgMttd=th.length>0?fmtTime(Math.round(th.reduce((a,x)=>a+(x.mttd||0),0)/th.length)):'—';
      const avgMttr=th.length>0?fmtTime(Math.round(th.reduce((a,x)=>a+(x.mttr||0),0)/th.length)):'—';
      const totalCost=th.reduce((a,x)=>a+(x.cost||0),0);
      const ctrlCount=G.controls.filter(c=>c.threat===t.id).length;
      const tierClass=t.tier===1?'badge-t1':t.tier===2?'badge-t2':'badge-t3';
      const status=tpH>0?'<span class="badge badge-ok">REMEDIATED</span>':'<span class="badge badge-closed">NO INCIDENTS</span>';
      const tr=document.createElement('tr');
      tr.innerHTML=`
        <td style="font-size:.77rem;font-weight:500">${t.short}</td>
        <td><span class="badge ${tierClass}">T${t.tier}</span></td>
        <td style="font-family:var(--font-mono);text-align:center">${alerts}</td>
        <td style="font-family:var(--font-mono);color:var(--crit);text-align:center">${tpH}</td>
        <td style="font-family:var(--font-mono);color:var(--warn);text-align:center">${fpH}</td>
        <td style="font-family:var(--font-mono);color:${acc!=='—'&&parseInt(acc)>80?'var(--ok)':'var(--warn)'}">${acc}</td>
        <td style="font-family:var(--font-mono)">${avgMttd}</td>
        <td style="font-family:var(--font-mono)">${avgMttr}</td>
        <td style="font-family:var(--font-mono);color:var(--warn)">${totalCost>0?'$'+fmtNum(totalCost):'—'}</td>
        <td style="color:var(--ok);text-align:center">${ctrlCount}</td>
        <td>${status}</td>`;
      stbody.appendChild(tr);
    });
  }
  updateCISOCharts();
}

function updateCISOCharts(){
  updateChart('chart-ciso-risk',[G.chartData.risk]);
  updateChart('chart-ciso-cost',[G.chartData.cost]);
}

// ══ DEVICE SIMULATION TICK ════════════════════════════════════
function simTick(){
  DEVICES.forEach(d=>{
    const s=G.ds[d.id];
    const [lo,hi]=d.normal;
    let delta=(Math.random()-.5)*(hi-lo)*.08;
    if(s.affected&&!s.isolated&&G.ir.threat) G.ir.threat.attackSim(s);
    if(s.isolated) delta=(Math.random()-.5)*(hi-lo)*.01;
    if(s.recovering){ const tgt=rnd(lo,hi); delta=(tgt-s.value)*.1; }
    s.value=Math.max(0,+(s.value+delta).toFixed(2));
    s.history.push(s.value);
    if(s.history.length>20)s.history.shift();
  });
  updateIRDeviceBar();
  // Phase timer
  if(G.ir.active){
    const e=Math.floor((Date.now()-G.ir.phaseStart)/1000);
    const m=String(Math.floor(e/60)).padStart(2,'0');
    const ss=String(e%60).padStart(2,'0');
    document.getElementById('idb-timer').textContent=`${m}:${ss}`;
  }
}

// ══ HELPER FUNCTIONS ═════════════════════════════════════════
function rnd(lo,hi){return +(lo+Math.random()*(hi-lo)).toFixed(2);}
function fmtTime(s){
  if(!s&&s!==0)return'—';
  if(s<60)return s+'s';
  if(s<3600)return Math.floor(s/60)+'m'+String(s%60).padStart(2,'0')+'s';
  return Math.floor(s/3600)+'h'+String(Math.floor((s%3600)/60)).padStart(2,'0')+'m';
}
function fmtNum(n){if(!n)return'0';if(n>=1000000)return(n/1000000).toFixed(1)+'M';if(n>=1000)return(n/1000).toFixed(1)+'k';return n.toString();}

// ══ BOOT SEQUENCE ════════════════════════════════════════════
buildIRThreatList();
buildIRPipeline();
buildIRDeviceBar();
irBuildPlaybook('detect',0);
initCharts();
renderAlertFeed();
renderSOCControls();
irAddEvent('prepare','🟢 OT SecureOps Platform online — 8 ICS assets monitored',
  'NIST SP 800-61 Rev.2 · IEC 62443 · AI anomaly detection armed · All 10 OT threat scenarios loaded');
irAddEvent('prepare','📋 Select any of the 10 OT threat scenarios and click Launch Scenario',
  'Analyst triage modal will appear after detection phase — classify as TP or FP to direct the IR response');

G.tickInt=setInterval(simTick, 800);

</script>
</body>
</html>
