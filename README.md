[Sitio de ventas](https://github.com/user-attachments/files/27442100/index.13.html)
<Vendiendo es vendiendo
>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Cantadas Mayo 2026 — Team Jarold Barrios</title>
<script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-database.js"></script>
<style>
:root{
  --pri:#0D9488;--prid:#0F766E;--pril:#CCFBF1;
  --hdr:#0F172A;--bg:#0F172A;--card:rgba(255,255,255,0.07);
  --card-solid:#1E293B;--txt:#F1F5F9;--mut:#94A3B8;
  --brd:rgba(255,255,255,0.1);--dan:#EF4444;--suc:#10B981;
  --accent:#6366F1;
}
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;
  background:var(--bg);color:var(--txt);font-size:13px;min-height:100vh;
  background-image:
    radial-gradient(ellipse at 20% 20%, rgba(99,102,241,0.15) 0%, transparent 50%),
    radial-gradient(ellipse at 80% 80%, rgba(13,148,136,0.15) 0%, transparent 50%),
    radial-gradient(ellipse at 50% 50%, rgba(139,92,246,0.08) 0%, transparent 70%);
  background-attachment:fixed;
}
/* HEADER */
.hdr{
  background:rgba(15,23,42,0.95);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(99,102,241,0.3);
  padding:12px 16px;position:sticky;top:0;z-index:100;
  box-shadow:0 4px 24px rgba(0,0,0,0.4);
}
.ht{
  background:linear-gradient(135deg,#818CF8,#0D9488,#6EE7B7);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  font-weight:700;font-size:15px;margin-bottom:3px;
}
.hs{color:var(--mut);font-size:11px;margin-bottom:8px}
.tbar{display:flex;flex-wrap:wrap;gap:3px}
.tb{
  background:transparent;border:1px solid transparent;
  color:var(--mut);padding:6px 12px;font-size:12px;
  border-radius:8px;cursor:pointer;font-family:inherit;transition:all .2s;
}
.tb:hover{background:rgba(255,255,255,0.08);color:var(--txt);border-color:var(--brd)}
.tb.act{background:linear-gradient(135deg,#6366F1,#0D9488);color:#fff;border-color:transparent;font-weight:500;box-shadow:0 2px 12px rgba(99,102,241,0.4)}
/* SALE OVERLAY */
#saleOverlay{position:fixed;inset:0;z-index:9999;display:none;align-items:center;justify-content:center;flex-direction:column;background:rgba(0,0,0,0.85);backdrop-filter:blur(8px)}
#saleOverlay.show{display:flex}
.sale-burst{text-align:center;animation:burstIn .5s cubic-bezier(.175,.885,.32,1.275);background:rgba(255,255,255,0.05);border:1px solid rgba(255,255,255,0.15);border-radius:24px;padding:32px 48px;backdrop-filter:blur(20px)}
.sale-emoji{font-size:72px;display:block;margin-bottom:12px;animation:bounce .6s ease-in-out}
.sale-name{color:#fff;font-size:28px;font-weight:700;margin-bottom:6px}
.sale-detail{color:#A5F3FC;font-size:16px;margin-bottom:4px}
.sale-bill{color:#6EE7B7;font-size:24px;font-weight:700;margin-bottom:16px}
.sale-hint{color:rgba(255,255,255,0.4);font-size:12px}
@keyframes burstIn{0%{transform:scale(0);opacity:0}80%{transform:scale(1.05)}100%{transform:scale(1);opacity:1}}
@keyframes bounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-12px)}}
.cf-wrap{position:fixed;inset:0;pointer-events:none;z-index:9998}
.cf{position:absolute;border-radius:2px;animation:fall linear forwards}
@keyframes fall{0%{transform:translateY(-20px) rotate(0);opacity:1}100%{transform:translateY(105vh) rotate(720deg);opacity:0}}
/* TOAST */
.toast{
  position:fixed;top:80px;left:50%;transform:translateX(-50%);
  background:linear-gradient(135deg,#065F46,#0D9488);
  color:#fff;padding:10px 20px;font-size:13px;font-weight:500;
  border-radius:99px;z-index:200;display:none;
  box-shadow:0 4px 24px rgba(13,148,136,0.5);
  border:1px solid rgba(110,231,183,0.3);
  white-space:nowrap;max-width:90vw;overflow:hidden;text-overflow:ellipsis;
}
.toast.on{display:block;animation:toastIn .3s ease}
@keyframes toastIn{from{transform:translateX(-50%) translateY(-10px);opacity:0}to{transform:translateX(-50%) translateY(0);opacity:1}}
.bdbanner{background:linear-gradient(135deg,#92400E,#F59E0B);color:#fff;padding:10px 16px;text-align:center;font-size:13px;font-weight:600;display:none;box-shadow:0 2px 12px rgba(245,158,11,0.4)}
.bdbanner.on{display:block}
.loading{padding:60px;text-align:center;color:var(--mut);font-size:14px}
main{padding:16px}
.tab{display:none}.tab.act{display:block}
/* CARDS */
.card{
  background:rgba(30,41,59,0.8);
  backdrop-filter:blur(12px);
  border:1px solid var(--brd);
  border-radius:14px;padding:16px;margin-bottom:14px;
  box-shadow:0 4px 24px rgba(0,0,0,0.2);
}
.card-glass{
  background:rgba(255,255,255,0.04);
  backdrop-filter:blur(16px);
  border:1px solid rgba(255,255,255,0.08);
  border-radius:14px;padding:16px;margin-bottom:14px;
}
.ct{font-size:13px;font-weight:600;margin-bottom:10px;color:var(--txt)}
.cs{font-size:11px;color:var(--mut);margin-bottom:8px}
.row{display:flex;gap:14px;flex-wrap:wrap;align-items:flex-start}
.col{flex:1;min-width:0}
.fg{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.fl{display:flex;flex-direction:column;gap:4px;margin-bottom:10px}
label{font-size:11px;color:var(--mut);font-weight:500;letter-spacing:.3px}
input,select,textarea{
  width:100%;padding:8px 11px;
  border:1px solid rgba(255,255,255,0.12);
  border-radius:8px;font-size:12px;font-family:inherit;
  background:rgba(255,255,255,0.06);color:var(--txt);outline:none;transition:all .2s;
}
input:focus,select:focus,textarea:focus{border-color:var(--pri);background:rgba(13,148,136,0.08);box-shadow:0 0 0 2px rgba(13,148,136,0.15)}
input::placeholder{color:var(--mut)}
select option{background:#1E293B;color:var(--txt)}
textarea{resize:vertical;font-family:monospace;line-height:1.65}
.btn{
  padding:8px 14px;border:1px solid var(--brd);
  border-radius:8px;cursor:pointer;font-size:12px;
  font-family:inherit;background:rgba(255,255,255,0.06);
  color:var(--txt);font-weight:500;transition:all .2s;
}
.btn:hover{background:rgba(255,255,255,0.12);border-color:rgba(255,255,255,0.2)}
.sbtn{
  width:100%;padding:11px;border:none;font-size:13px;font-weight:600;
  border-radius:10px;cursor:pointer;font-family:inherit;color:#fff;
  margin-top:6px;transition:all .2s;letter-spacing:.3px;
}
.sbtn:hover{transform:translateY(-1px);box-shadow:0 4px 16px rgba(0,0,0,0.3)}
/* PLAN/TYPE BUTTONS */
.plan-row{display:flex;gap:6px;margin-bottom:10px}
.pb{
  flex:1;padding:9px 4px;text-align:center;font-size:12px;font-weight:600;
  border-radius:8px;cursor:pointer;border:1px solid var(--brd);
  background:rgba(255,255,255,0.05);color:var(--mut);font-family:inherit;transition:all .2s;
}
.pb.s{background:linear-gradient(135deg,rgba(13,148,136,0.3),rgba(99,102,241,0.3));border-color:var(--pri);color:#6EE7B7}
.typb{
  width:100%;text-align:left;padding:9px 13px;margin-bottom:6px;
  font-size:12px;border-radius:8px;cursor:pointer;
  border:1px solid var(--brd);background:rgba(255,255,255,0.04);
  color:var(--mut);font-family:inherit;transition:all .2s;
}
.typb.s{background:linear-gradient(135deg,rgba(13,148,136,0.25),rgba(99,102,241,0.25));border-color:var(--pri);color:#6EE7B7;font-weight:600}
/* KPI */
.krow{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:14px}
.kpi{
  background:rgba(30,41,59,0.9);backdrop-filter:blur(12px);
  border:1px solid var(--brd);border-radius:12px;
  padding:12px 16px;flex:1;min-width:100px;
  transition:transform .2s;
}
.kpi:hover{transform:translateY(-2px)}
.kl{font-size:10px;color:var(--mut);margin-bottom:4px;text-transform:uppercase;letter-spacing:.6px}
.kv{font-size:20px;font-weight:700;background:linear-gradient(135deg,#6EE7B7,#818CF8);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
/* TABLE */
.tbl-w{overflow-x:auto}
table{border-collapse:collapse;width:100%}
th,td{border:1px solid rgba(255,255,255,0.07);padding:4px 6px;text-align:center;font-size:10px;white-space:nowrap}
th{background:rgba(255,255,255,0.05);font-weight:600;color:var(--mut)}
.th-d{background:rgba(15,23,42,0.9);color:#94A3B8;font-weight:600}
.h0{background:rgba(255,255,255,0.03);color:rgba(255,255,255,0.2)}
.hm{background:rgba(254,249,195,0.15);color:#FCD34D;font-weight:600}
.h1{background:rgba(209,250,229,0.12);color:#6EE7B7;font-weight:600}
.h2{background:rgba(110,231,183,0.2);color:#34D399;font-weight:600}
.h3{background:rgba(16,185,129,0.25);color:#10B981;font-weight:600}
.h4{background:rgba(6,95,70,0.4);color:#6EE7B7;font-weight:600}
.tdc{outline:2px solid var(--pri);outline-offset:-1px}
.badge{display:inline-block;padding:2px 8px;border-radius:99px;font-size:10px;font-weight:600}
.bg{background:rgba(16,185,129,0.2);color:#6EE7B7;border:1px solid rgba(16,185,129,0.3)}
.br{background:rgba(239,68,68,0.2);color:#FCA5A5;border:1px solid rgba(239,68,68,0.3)}
/* PODIO */
.podio-wrap{display:flex;flex-direction:column;gap:10px}
.podio-item{
  display:flex;align-items:center;gap:12px;padding:12px 14px;
  border-radius:12px;border:1px solid var(--brd);
  background:rgba(255,255,255,0.04);transition:all .3s;
  animation:slideIn .4s ease both;
}
@keyframes slideIn{from{transform:translateX(-20px);opacity:0}to{transform:translateX(0);opacity:1}}
.podio-item.p1{background:linear-gradient(135deg,rgba(245,158,11,0.15),rgba(252,211,77,0.08));border-color:rgba(245,158,11,0.4)}
.podio-item.p2{background:linear-gradient(135deg,rgba(148,163,184,0.12),rgba(100,116,139,0.06));border-color:rgba(148,163,184,0.3)}
.podio-item.p3{background:linear-gradient(135deg,rgba(217,119,6,0.12),rgba(180,83,9,0.06));border-color:rgba(217,119,6,0.3)}
.podio-medal{width:38px;height:38px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:17px;font-weight:700;flex-shrink:0}
.pm1{background:linear-gradient(135deg,#F59E0B,#FCD34D);box-shadow:0 4px 12px rgba(245,158,11,0.4)}
.pm2{background:linear-gradient(135deg,#9CA3AF,#D1D5DB);box-shadow:0 4px 12px rgba(156,163,175,0.3)}
.pm3{background:linear-gradient(135deg,#D97706,#F59E0B);box-shadow:0 4px 12px rgba(217,119,6,0.3)}
.podio-name{flex:1;font-size:13px;font-weight:600;color:var(--txt)}
.podio-score{font-size:24px;font-weight:700;background:linear-gradient(135deg,#6EE7B7,#818CF8);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.podio-bar-wrap{height:4px;background:rgba(255,255,255,0.1);border-radius:99px;margin-top:4px;overflow:hidden}
.podio-bar{height:100%;border-radius:99px;background:linear-gradient(90deg,var(--pri),var(--accent));transition:width 1s ease}
/* QUARTILE */
.q1{background:rgba(16,185,129,0.2);color:#6EE7B7;padding:2px 7px;border-radius:99px;font-size:9px;font-weight:700;border:1px solid rgba(16,185,129,0.3)}
.q2{background:rgba(234,179,8,0.2);color:#FCD34D;padding:2px 7px;border-radius:99px;font-size:9px;font-weight:700;border:1px solid rgba(234,179,8,0.3)}
.q3{background:rgba(249,115,22,0.2);color:#FDB97D;padding:2px 7px;border-radius:99px;font-size:9px;font-weight:700;border:1px solid rgba(249,115,22,0.3)}
.q4{background:rgba(239,68,68,0.2);color:#FCA5A5;padding:2px 7px;border-radius:99px;font-size:9px;font-weight:700;border:1px solid rgba(239,68,68,0.3)}
.qn{background:rgba(99,102,241,0.2);color:#A5B4FC;padding:2px 7px;border-radius:99px;font-size:9px;font-weight:700;border:1px solid rgba(99,102,241,0.3)}
.new-badge{background:rgba(99,102,241,0.25);color:#A5B4FC;padding:1px 5px;border-radius:99px;font-size:8px;font-weight:700;margin-left:3px;border:1px solid rgba(99,102,241,0.3)}
/* RACE */
.race-wrap{display:flex;flex-direction:column;gap:10px;margin-top:8px}
.race-row{
  display:flex;align-items:center;gap:10px;padding:10px 14px;
  background:rgba(255,255,255,0.04);border-radius:10px;border:1px solid var(--brd);
}
.race-name{width:105px;font-size:11px;font-weight:600;flex-shrink:0;color:var(--txt)}
.race-track{flex:1;height:22px;background:rgba(255,255,255,0.08);border-radius:99px;position:relative;overflow:visible}
.race-fill{height:100%;border-radius:99px;background:linear-gradient(90deg,var(--pri),var(--accent));transition:width .8s cubic-bezier(.175,.885,.32,1.275);position:relative;min-width:0}
.race-car{position:absolute;top:50%;transform:translateY(-50%);font-size:16px;transition:left .8s cubic-bezier(.175,.885,.32,1.275);pointer-events:none}
.race-pct{width:40px;text-align:right;font-size:11px;font-weight:600;color:#6EE7B7}
.race-input{width:50px;padding:4px 6px;font-size:11px;text-align:center;border:1px solid var(--brd);border-radius:6px;background:rgba(255,255,255,0.06);color:var(--txt)}
/* BIRTHDAY */
.bd-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(175px,1fr));gap:10px}
.bd-card{
  background:rgba(255,255,255,0.04);border:1px solid var(--brd);
  border-radius:10px;padding:11px 13px;transition:all .3s;
}
.bd-card.today{border-color:#F59E0B;background:rgba(245,158,11,0.1);animation:bdPulse 2s ease-in-out infinite}
.bd-card.soon{border-color:var(--pri);background:rgba(13,148,136,0.08)}
@keyframes bdPulse{0%,100%{box-shadow:0 0 0 0 rgba(245,158,11,0.4)}50%{box-shadow:0 0 0 8px rgba(245,158,11,0)}}
.bd-name{font-size:12px;font-weight:600;margin-bottom:6px;display:flex;justify-content:space-between;align-items:center;color:var(--txt)}
.bd-tag{background:rgba(245,158,11,0.25);color:#FCD34D;border-radius:99px;padding:1px 7px;font-size:9px;font-weight:600;border:1px solid rgba(245,158,11,0.4)}
.bd-soon-tag{background:rgba(13,148,136,0.25);color:#6EE7B7;border-radius:99px;padding:1px 7px;font-size:9px;font-weight:600}
.bd-inp{display:flex;gap:5px;align-items:center}
.bd-days{font-size:10px;font-weight:600;color:var(--pri);min-width:28px;text-align:right}
.bd-cel{
  background:linear-gradient(135deg,rgba(15,23,42,0.9),rgba(19,78,74,0.9));
  border:1px solid rgba(110,231,183,0.3);border-radius:16px;
  padding:28px;text-align:center;margin-bottom:16px;position:relative;overflow:hidden;
  box-shadow:0 8px 32px rgba(13,148,136,0.2);
}
.bd-fw{position:absolute;font-size:22px;animation:fw 1.5s ease-in-out infinite}
@keyframes fw{0%{transform:scale(0) rotate(0);opacity:1}100%{transform:scale(2.5) rotate(360deg);opacity:0}}
/* PREVIEW BOX */
.pv{
  background:rgba(16,185,129,0.1);border:1px solid rgba(16,185,129,0.25);
  border-radius:8px;padding:10px 13px;font-size:12px;margin-bottom:10px;display:none;
}
.pvg{display:grid;grid-template-columns:1fr 1fr;gap:3px 10px}
.pvl{color:var(--mut)}
.pvv{font-weight:600;color:#6EE7B7}
/* MSG */
.msg{font-size:12px;font-weight:600;padding:8px 12px;border-radius:8px;margin-bottom:10px}
.mok{background:rgba(16,185,129,0.15);color:#6EE7B7;border:1px solid rgba(16,185,129,0.3)}
.merr{background:rgba(239,68,68,0.15);color:#FCA5A5;border:1px solid rgba(239,68,68,0.3)}
/* FILTERS */
.filter-bar{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:14px;align-items:flex-end}
.filter-bar .fl{margin-bottom:0;min-width:110px;flex:1}
td.td-l{text-align:left;padding-left:9px}
/* TICKETS */
.tplcard{border:1px solid var(--brd);border-radius:10px;margin-bottom:10px;overflow:hidden}
.tplh{display:flex;justify-content:space-between;align-items:center;padding:12px 16px;cursor:pointer;background:rgba(255,255,255,0.04);transition:background .2s}
.tplh:hover{background:rgba(255,255,255,0.08)}
.tplt{font-size:13px;font-weight:600;color:var(--txt)}
.tplb{padding:12px 16px;background:rgba(0,0,0,0.2);border-top:1px solid var(--brd);display:none}
.tplb.op{display:block}
.cpbtn{padding:5px 12px;font-size:11px;border-radius:7px;cursor:pointer;font-family:inherit;border:1px solid var(--brd);background:rgba(255,255,255,0.06);color:var(--txt);transition:all .2s}
.cpbtn:hover{background:rgba(255,255,255,0.1)}
.cpbtn.ok{background:rgba(16,185,129,0.2);color:#6EE7B7;border-color:rgba(16,185,129,0.4);font-weight:600}
/* SCROLLBAR */
::-webkit-scrollbar{width:6px;height:6px}
::-webkit-scrollbar-track{background:rgba(255,255,255,0.03)}
::-webkit-scrollbar-thumb{background:rgba(255,255,255,0.15);border-radius:99px}

/* SPLASH SCREEN */
#splash{
  position:fixed;inset:0;z-index:99999;
  background:linear-gradient(135deg,#0F172A 0%,#1E1B4B 40%,#0F2E2B 100%);
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  transition:opacity .8s ease, visibility .8s ease;
}
#splash.hide{opacity:0;visibility:hidden}
.splash-logo{font-size:56px;margin-bottom:16px;animation:splashBounce 1s ease-in-out infinite alternate}
@keyframes splashBounce{from{transform:translateY(0) scale(1)}to{transform:translateY(-10px) scale(1.05)}}
.splash-title{
  font-size:22px;font-weight:700;text-align:center;margin-bottom:10px;
  background:linear-gradient(135deg,#6EE7B7,#818CF8,#6EE7B7);
  background-size:200%;-webkit-background-clip:text;-webkit-text-fill-color:transparent;
  animation:gradShift 3s linear infinite;
}
@keyframes gradShift{0%{background-position:0%}100%{background-position:200%}}
.splash-msg{
  font-size:15px;color:rgba(255,255,255,.7);text-align:center;
  max-width:380px;line-height:1.6;padding:0 24px;
  animation:fadeInUp .6s ease .3s both;
}
@keyframes fadeInUp{from{transform:translateY(20px);opacity:0}to{transform:translateY(0);opacity:1}}
.splash-bar-wrap{width:220px;height:3px;background:rgba(255,255,255,.1);border-radius:99px;margin-top:28px;overflow:hidden}
.splash-bar{height:100%;border-radius:99px;background:linear-gradient(90deg,#6EE7B7,#818CF8);animation:loadBar 2.2s ease forwards}
@keyframes loadBar{0%{width:0%}100%{width:100%}}
.splash-sub{font-size:11px;color:rgba(255,255,255,.3);margin-top:10px;letter-spacing:.5px}

</style>
</head>
<body>

<div id="saleOverlay" onclick="this.classList.remove('show')">
  <div class="cf-wrap" id="cfWrap"></div>
  <div class="sale-burst">
    <span class="sale-emoji" id="saleEmoji">🎯</span>
    <div class="sale-name" id="saleName"></div>
    <div class="sale-detail" id="saleDetail"></div>
    <div class="sale-bill" id="saleBill"></div>
    <div class="sale-hint">Toca para continuar</div>
  </div>
</div>

<div class="hdr">
  <div class="ht">CANTADAS MAYO 2026 &nbsp;|&nbsp; Team Jarold Barrios</div>
  <div class="hs">30 asesores &nbsp;·&nbsp; 7.5h efectivas &nbsp;·&nbsp; Meta: 70/día &nbsp;·&nbsp; Ant: min 3 / obj 5 &nbsp;·&nbsp; Nuevos: 3</div>
  <div class="tbar">
    <button class="tb act" onclick="showTab('form')">Registrar</button>
    <button class="tb" onclick="showTab('cantadas')">Cantadas</button>
    <button class="tb" onclick="showTab('ventas')">Ventas</button>
    <button class="tb" onclick="showTab('esim')">eSIM</button>
    <button class="tb" onclick="showTab('cancel')">Cancelaciones</button>
    <button class="tb" onclick="showTab('tickets')">Tickets</button>
    <button class="tb" onclick="showTab('comisiones')">Comisiones</button>
    <button class="tb" onclick="showTab('cumple')">Cumpleaños</button>
  </div>
</div>

<div id="toast" class="toast"></div>
<div id="bdbanner" class="bdbanner"></div>
<div id="splash">
  <div class="splash-logo">🚀</div>
  <div class="splash-title">Buen día mi mejor elemento</div>
  <div class="splash-msg" id="splashMsg"></div>
  <div class="splash-bar-wrap"><div class="splash-bar"></div></div>
  <div class="splash-sub">Team Jarold Barrios · Mayo 2026</div>
</div>

<div id="app-loading" class="loading">
  <div style="font-size:32px;margin-bottom:12px;animation:bounce 1s ease-in-out infinite">🚀</div>
  <div style="color:#6EE7B7;font-weight:600;font-size:15px;margin-bottom:6px">Conectando con la nube...</div>
  <div style="color:var(--mut);font-size:12px">Team Jarold Barrios · Mayo 2026</div>
</div>
<div id="app-main" style="display:none">
<main>

<div id="tab-form" class="tab act">
<div class="row">
<div class="col" style="max-width:430px">
<div class="card">
  <div class="ct">✍️ Registrar venta cantada</div>
  <div class="fg">
    <div class="fl"><label>Asesor</label><select id="fAdv"></select></div>
    <div class="fl"><label>Día de mayo</label><select id="fDay"></select></div>
  </div>
  <div class="fl"><label>Plan vendido</label><div class="plan-row" id="fPlans"></div></div>
  <div class="fl"><label>Tipo de venta</label><div id="fTypes"></div></div>
  <div class="fl"><label>N. Orden EKIA</label><input id="fEkia" placeholder="Ej: 374492832"></div>
  <div id="fPreview" class="pv"><div class="pvg">
    <span class="pvl">Sin IVA:</span><span class="pvv" id="pvSiva"></span>
    <span class="pvl">Factura:</span><span class="pvv" id="pvBill"></span>
    <span class="pvl">Cuenta:</span><span class="pvv" id="pvCnt"></span>
  </div></div>
  <div id="fMsg"></div>
  <button class="sbtn" style="background:linear-gradient(135deg,#0D9488,#6366F1)" onclick="submitSale()">Registrar venta</button>
</div>
</div>
<div class="col">
<div class="card">
  <div class="ct">Últimas ventas (<span id="salesCount">0</span>)</div>
  <div id="recentSales"></div>
</div>
</div>
</div>
</div>

<div id="tab-cantadas" class="tab">
  <div class="krow" id="kpis"></div>
  <div class="row" style="margin-bottom:14px">
    <div class="col"><div class="card"><div class="ct">🏆 Podio del día</div><div id="podioDia" class="podio-wrap"></div></div></div>
    <div class="col"><div class="card"><div class="ct">🏅 Podio de la semana</div><div id="podioSem" class="podio-wrap"></div></div></div>
  </div>
  <div class="card"><div class="ct">Mapa de calor — generado automáticamente</div><div class="tbl-w" id="heatmap"></div></div>
</div>

<div id="tab-ventas" class="tab">
<div class="card">
  <div class="ct">📋 Registro de ventas</div>
  <div class="filter-bar">
    <div class="fl"><label>Asesor</label><select id="vfAdv"><option value="">Todos</option></select></div>
    <div class="fl"><label>Día</label><select id="vfDay"><option value="">Todos</option></select></div>
    <div class="fl"><label>Plan</label><select id="vfPlan"><option value="">Todos</option></select></div>
    <div class="fl"><label>Tipo</label><select id="vfType"><option value="">Todos</option></select></div>
    <div class="fl"><label>Buscar</label><input id="vfSearch" placeholder="Nombre, EKIA..." oninput="renderVentas()"></div>
    <button class="btn" onclick="clearFilters()" style="align-self:flex-end;margin-bottom:10px">Limpiar</button>
  </div>
  <div class="tbl-w">
    <table><thead><tr>
      <th class="th-d">May</th><th class="th-d">Día</th><th class="th-d">Asesor</th>
      <th class="th-d">Tipo</th><th class="th-d">Plan</th><th class="th-d">Cant</th>
      <th class="th-d">Factura</th><th class="th-d">EKIA</th><th class="th-d">Hora</th><th class="th-d"></th>
    </tr></thead><tbody id="ventasBody"></tbody></table>
  </div>
  <div id="ventasCount" style="font-size:11px;color:var(--mut);margin-top:8px"></div>
</div>
</div>

<div id="tab-esim" class="tab">
<div class="row">
<div class="col" style="max-width:520px">
<div class="card">
  <div class="ct">📱 Registrar venta eSIM</div><div class="cs">* obligatorios</div>
  <div class="fg">
    <div class="fl"><label>* Asesor</label><select id="esAdv"></select></div>
    <div class="fl"><label>* Día</label><select id="esDay"></select></div>
    <div class="fl"><label>* Nombre cliente</label><input id="esCli" placeholder="Nombre completo"></div>
    <div class="fl"><label>Correo</label><input id="esMail" type="email" placeholder="correo@ejemplo.com"></div>
    <div class="fl"><label>Tipo doc</label><select id="esTdoc"><option>CC</option><option>PPT</option><option>CE</option><option>NIT</option></select></div>
    <div class="fl"><label>* Núm. documento</label><input id="esNdoc" placeholder="N. documento"></div>
    <div class="fl"><label>Fecha expedición DD/MM/AAAA</label><input id="esFexp" placeholder="01/01/2020"></div>
    <div class="fl"><label>Operador donante</label><select id="esOp"><option>TIGO</option><option>CLARO</option><option>MOVISTAR</option><option>ETB</option><option>SWIFT</option><option>WOM</option><option>OTRO</option></select></div>
    <div class="fl"><label>Núm. a portar / Línea nueva</label><input id="esNport" placeholder="3001234567 o LINEA NUEVA"></div>
    <div class="fl"><label>Modalidad</label><select id="esMod"><option>POST TO POST</option><option>PRE TO POST</option><option>LINEA NUEVA ESIM</option><option>POSPAGO TO POSPAGO</option><option>PREPAGO TO POSPAGO</option></select></div>
    <div class="fl"><label>Código NIP</label><input id="esNip" placeholder="NIP portabilidad"></div>
    <div class="fl"><label>Modelo equipo</label><input id="esEquipo" placeholder="Ej: iPhone 15 Pro"></div>
    <div class="fl"><label>* N. Llamada / EKIA</label><input id="esEkia" placeholder="N. orden EKIA"></div>
    <div class="fl"><label>N. Pedido</label><input id="esPed" placeholder="Opcional"></div>
  </div>
  <div class="fl"><label>Plan</label><div class="plan-row" id="esPlans"></div></div>
  <div class="fl"><label>Tipo</label><div id="esTypes"></div></div>
  <div id="esMsg"></div>
  <button class="sbtn" style="background:linear-gradient(135deg,#065F46,#0D9488)" onclick="submitEsim()">Registrar eSIM</button>
</div>
</div>
<div class="col" style="min-width:190px">
  <div class="card"><div class="ct">eSIM por asesor (<span id="esimTotal">0</span>)</div><div id="esimCounts"></div></div>
</div>
</div>
<div class="card" style="margin-top:4px">
  <div class="ct">Listado completo eSIM</div>
  <div class="tbl-w">
    <table><thead><tr>
      <th class="th-d">May</th><th class="th-d">Asesor</th><th class="th-d">Cliente</th>
      <th class="th-d">Tipo Doc</th><th class="th-d">N. Doc</th><th class="th-d">Fecha Exp</th>
      <th class="th-d">Correo</th><th class="th-d">Operador</th><th class="th-d">N. Porta</th>
      <th class="th-d">Modalidad</th><th class="th-d">NIP</th><th class="th-d">Plan</th>
      <th class="th-d">Tipo</th><th class="th-d">EKIA</th><th class="th-d">Pedido</th>
      <th class="th-d">Equipo</th><th class="th-d">Hora</th><th class="th-d"></th>
    </tr></thead><tbody id="esimBody"></tbody></table>
  </div>
</div>
</div>

<div id="tab-cancel" class="tab">
<div class="row">
<div class="col" style="max-width:460px">
<div class="card">
  <div class="ct">❌ Registrar cancelación</div>
  <div class="fg">
    <div class="fl"><label>Asesor</label><select id="caAdv"></select></div>
    <div class="fl"><label>Día</label><select id="caDay"></select></div>
    <div class="fl"><label>Nombre cliente</label><input id="caCli" placeholder="Nombre completo"></div>
    <div class="fl"><label>CC cliente</label><input id="caCc" placeholder="N. cédula"></div>
    <div class="fl"><label>N. Pedido</label><input id="caPed" placeholder="N. pedido"></div>
    <div class="fl"><label>Línea de la venta</label><input id="caTel" placeholder="3001234567"></div>
    <div class="fl"><label>Motivo</label>
      <select id="caMot"><option>No recogio en punto</option><option>Devolucion al remitente</option><option>Recogida en punto</option><option>Error facturacion</option><option>Plan errado</option><option>Cambio de ciudad</option><option>Cambio a recogida en punto</option><option>Cliente en mora</option><option>Cupo excedido</option><option>Fraude / LAFT</option><option>PPT sin adjunto</option><option>Otro</option></select>
    </div>
    <div class="fl"><label>Respuesta team</label>
      <select id="caResp"><option>ENVIADA A CANCELAR</option><option>EN REVISION</option><option>PROCEDENTE</option><option>NO PROCEDENTE</option></select>
    </div>
  </div>
  <div id="caMsg"></div>
  <button class="sbtn" style="background:linear-gradient(135deg,#DC2626,#EF4444)" onclick="submitCancel()">Registrar cancelación</button>
</div>
</div>
<div class="col" style="min-width:190px">
  <div class="card"><div class="ct">Cancelaciones por asesor (<span id="cancelTotal">0</span>)</div><div id="cancelCounts"></div></div>
</div>
</div>
<div class="card" style="margin-top:4px">
  <div class="ct">Listado completo cancelaciones</div>
  <div class="tbl-w">
    <table><thead><tr>
      <th class="th-d">May</th><th class="th-d">Asesor</th><th class="th-d">Cliente</th>
      <th class="th-d">CC</th><th class="th-d">Pedido</th><th class="th-d">Línea</th>
      <th class="th-d">Motivo</th><th class="th-d">Respuesta</th><th class="th-d">Hora</th><th class="th-d"></th>
    </tr></thead><tbody id="cancelBody"></tbody></table>
  </div>
</div>
</div>

<div id="tab-tickets" class="tab">
<div class="card" style="margin-bottom:10px"><div class="ct">🎫 Plantillas de tickets</div><div class="cs">Expande, edita los datos del cliente y copia. Al copiar vuelve al original automáticamente.</div></div>
<div id="tplCards"></div>
</div>

<div id="tab-comisiones" class="tab">
<div class="card">
  <div class="ct">🏎️ Carrera de activas</div>
  <div class="cs">Ingresa las activas de cada asesor — el carrito avanza según su progreso</div>
  <div id="raceWrap" class="race-wrap"></div>
</div>
<div class="row" style="margin-top:14px">
  <div class="col">
    <div class="card"><div class="ct">Calculadora de comisiones</div><div class="tbl-w" id="comTable"></div></div>
  </div>
  <div class="col" style="max-width:290px">
    <div class="card">
      <div class="ct">Tabla comisional mayo 2026</div>
      <div class="tbl-w"><table><thead><tr><th class="th-d">Desde</th><th class="th-d">Hasta</th><th class="th-d">%</th><th class="th-d">Min</th><th class="th-d">Max</th></tr></thead><tbody id="comRef"></tbody></table></div>
      <div style="margin-top:8px;font-size:10px;color:var(--mut)">Antiguos: piso $2.300.000 &nbsp;|&nbsp; Nuevos: piso $1.800.000</div>
    </div>
  </div>
</div>
</div>

<div id="tab-cumple" class="tab">
  <div id="bdCel"></div>
  <div class="row" id="cdRow" style="margin-bottom:16px"></div>
  <div class="card"><div class="ct">🎂 Cumpleaños del equipo — ingresa DD/MM</div><div class="bd-grid" id="bdGrid"></div></div>
</div>

</main>
</div>

<script>
const firebaseConfig={
  apiKey:"AIzaSyBgvDMkfiO64EqLZVy0ZySTtrECEhhaO3o",
  authDomain:"seguimiento-team-jarold.firebaseapp.com",
  databaseURL:"https://seguimiento-team-jarold-default-rtdb.firebaseio.com",
  projectId:"seguimiento-team-jarold",
  storageBucket:"seguimiento-team-jarold.firebasestorage.app",
  messagingSenderId:"795965579723",
  appId:"1:795965579723:web:ec961c938c1c8e0984964e"
};

// ── SONIDOS WEB AUDIO API ─────────────────────────────────────────
const AudioCtx=window.AudioContext||window.webkitAudioContext;
let actx=null;
function getACtx(){if(!actx){actx=new AudioCtx();}return actx;}

function playEntrySound(){
  try{
    const ctx=getACtx();
    const notes=[261.63,329.63,392,523.25];
    notes.forEach((freq,i)=>{
      const osc=ctx.createOscillator();
      const gain=ctx.createGain();
      osc.connect(gain);gain.connect(ctx.destination);
      osc.type="sine";osc.frequency.setValueAtTime(freq,ctx.currentTime);
      gain.gain.setValueAtTime(0,ctx.currentTime);
      gain.gain.linearRampToValueAtTime(0.08,ctx.currentTime+i*.15+.05);
      gain.gain.exponentialRampToValueAtTime(0.001,ctx.currentTime+i*.15+.6);
      osc.start(ctx.currentTime+i*.15);
      osc.stop(ctx.currentTime+i*.15+.6);
    });
  }catch(e){}
}

function playSaleSound(){
  try{
    const ctx=getACtx();
    [[523.25,0],[659.25,.1],[783.99,.2],[1046.5,.32]].forEach(([freq,t])=>{
      const osc=ctx.createOscillator();
      const gain=ctx.createGain();
      osc.connect(gain);gain.connect(ctx.destination);
      osc.type="triangle";osc.frequency.setValueAtTime(freq,ctx.currentTime+t);
      gain.gain.setValueAtTime(0,ctx.currentTime+t);
      gain.gain.linearRampToValueAtTime(0.07,ctx.currentTime+t+.04);
      gain.gain.exponentialRampToValueAtTime(0.001,ctx.currentTime+t+.4);
      osc.start(ctx.currentTime+t);
      osc.stop(ctx.currentTime+t+.4);
    });
  }catch(e){}
}

// ── SPLASH ────────────────────────────────────────────────────────
const MSGS=[
  "Hoy es el día para superar tus límites. Cada llamada es una oportunidad de oro — aprovéchala al máximo.",
  "El éxito no es suerte, es el resultado de la disciplina diaria. Arranca con todo desde la primera llamada.",
  "Los campeones no esperan el momento perfecto, lo crean. Hoy tú creas el tuyo.",
  "Cada venta que cierras es un paso más hacia tus metas. ¡Sal a conquistar el día!",
  "La actitud lo es todo. Entra con energía, cierra con resultados.",
  "No hay llamada pequeña — cada cliente es una posibilidad real. ¡Dalo todo hoy!",
  "El mejor momento para vender fue ayer. El segundo mejor momento es ahora.",
  "Tu potencial no tiene límites. Hoy demuéstrale al equipo de qué estás hecho.",
  "Un día brillante empieza con una mentalidad brillante. ¡Vamos con todo!",
  "La diferencia entre ordinario y extraordinario es ese esfuerzo extra. Ponlo hoy."
];

function initSplash(){
  document.getElementById("splashMsg").textContent=MSGS[Math.floor(Math.random()*MSGS.length)];
  setTimeout(()=>{
    playEntrySound();
    setTimeout(()=>{
      document.getElementById("splash").classList.add("hide");
      setTimeout(()=>{
        const sp=document.getElementById("splash");
        if(sp)sp.remove();
      },900);
    },2400);
  },200);
}
initSplash();


// ── DATOS ─────────────────────────────────────────────────────────
const ADV_OLD=["Adriana Lopez","Andrea Camacho","Angelica Diaz","Angie Gomez","Deisy Daza","Genis Garcia","Hellen Eguis","Jader De La Hoz","Jair Sarabia","Jesus Vergara","Jhireth Sanjuanelo","Jose Diaz","Katia Teran","Keiner Barcelo","Kendry Quiroz","Kristian Tellez","Laura Lopez","Liliana Blanco","Lina Sanchez","Melany Rodriguez","Randy Acevedo","Sergio Mira","Valeria Zabaleta","Yerson Sandoval","Yeslin Martinez","Yonadis Pineda","Zharik Gomez"];
const ADV_NEW=["Aleska Agudo","Emily Aviles","Maria Molina"];
const ADV=[...ADV_OLD,...ADV_NEW];
const IS_NEW=new Set(ADV_NEW);
const PLANS=[{l:"$64.990",s:52642},{l:"$54.990",s:44542},{l:"$44.990",s:36442}];
const TYPES=[{v:"portabilidad",l:"Portabilidad",f:1},{v:"linea_nueva",l:"Linea nueva",f:1},{v:"migracion",l:"Migracion (x0.5)",f:.5}];
// Mayo 2026: festivos May 1 y May 18
const WD=[2,4,5,6,7,8,9,11,12,13,14,15,16,19,20,21,22,23,25,26,27,28,29,30];
const SAT=new Set([2,9,16,23,30]);
const WEEKS=[{l:"S1",d:[2]},{l:"Semana 2",d:[4,5,6,7,8,9]},{l:"Semana 3",d:[11,12,13,14,15,16]},{l:"Semana 4",d:[19,20,21,22,23]},{l:"Semana 5",d:[25,26,27,28,29,30]}];
const WC=["#6D28D9","#0369A1","#0D9488","#7C3AED","#0F766E"];
const DN=["Dom","Lun","Mar","Mie","Jue","Vie","Sab"];
const COM=[{f:1800000,t:2299999,p:.15,mn:270000,mx:345000},{f:2300000,t:2699999,p:.16,mn:368000,mx:432000},{f:2700000,t:3099999,p:.17,mn:459000,mx:527000},{f:3100000,t:3499999,p:.18,mn:558000,mx:630000},{f:3500000,t:3899999,p:.19,mn:665000,mx:741000},{f:3900000,t:4299999,p:.20,mn:780000,mx:860000},{f:4300000,t:4699999,p:.21,mn:903000,mx:987000},{f:4700000,t:Infinity,p:.22,mn:1034000,mx:null}];
const META_ACTIVAS=40;
const TPL=[
  {title:"Escalamiento logistico",c:"#818CF8",txt:"# de pedido: \nEstado en Beetrack: \nFecha de ultimo estado: \n# Contacto: \nDireccion: \nComplemento (barrio / referencia): \nCiudad: \nMotivo de escalamiento: "},
  {title:"Cancelacion de venta",c:"#0D9488",txt:"PEDIDO: \nNOMBRE DEL CLIENTE: \nCedula del cliente: \nLinea de telefono de la venta: \nAsesor que solicita: \nMotivo: "},
  {title:"Evidente no aprobado / Risky",c:"#EF4444",txt:"Tipo de servicio: Evidente\nTipologia: VALIDACION DE IDENTIDAD - EVIDENTE - BIOMETRIA\nNombre del cliente: \nNumero de documento: \nTipo de documento: \nTipo de cliente: B2C\nFecha de expedicion: \nFecha de vigencia (solo Extranjero): \nTelefono de contacto: \nCaso con mas de un TT: SI / NO\nN. TT anterior (si aplica): \nCliente en mora: SI / NO\nRealizo Biometria: SI / NO\nOBSERVACION: "},
  {title:"Cupo excedido",c:"#F59E0B",txt:"Nombre del cliente: \nTipo de cliente: B2C\nNumero de documento: \nTipo de documento: CC\nFecha de expedicion: \nFecha de vigencia (solo Extranjero): \nTelefono de contacto: \nCaso con mas de un TT: SI / NO\nN. TT anterior (si aplica): "},
  {title:"LAFT",c:"#0369A1",txt:"1. Nombre del cliente: \n2. Numero de documento: \n3. Tipo de documento: \n4. Tipo de cliente: B2C\n5. Fecha de expedicion: \n6. Fecha de vigencia (solo Extranjero): \n7. Telefono de contacto: \n8. Caso con mas de un TT: SI / NO\n9. N. TT de escalamiento anterior: "},
  {title:"PPT (pasaporte)",c:"#065F46",txt:"Tipo de venta: PPT\nNombre del cliente: \nNumero de pasaporte: \nFecha de expedicion: \nFecha de vigencia: \nNacionalidad: \nTelefono de contacto: \nPlan vendido: \nAsesor: \nNOTA: Adjuntar documento escaneado obligatoriamente."}
];

let db={sales:{},esim:{},cancel:{},activas:{},bdays:{},tpl:{}};
let fP=0,fT="portabilidad",esP=0,esT="portabilidad";
let dbRef,currentTab="form",lastSalesN=0;
const today=(()=>{const n=new Date();return n.getFullYear()===2026&&n.getMonth()===4?n.getDate():5})();

// ── UTILS ─────────────────────────────────────────────────────────
function dow(d){return(5+d-1)%7}
function hrs(d){return SAT.has(d)?4:7.5}
function eHrs(up){return WD.filter(d=>d<=up).reduce((s,d)=>s+hrs(d),0)}
function fCOP(n){if(!n&&n!==0)return"—";return"$"+Math.round(n).toLocaleString("es-CO")}
function hcls(c){if(!c)return"h0";if(c<1)return"hm";if(c<1.5)return"h1";if(c<2.5)return"h2";if(c<3.5)return"h3";return"h4";}
function getCom(b){return COM.find(r=>b>=r.f&&b<=r.t)||null;}
function curWeek(d){return(WEEKS.find(w=>w.d.includes(d))||{d:[]}).d;}
function nextBD(dm){if(!dm||!dm.includes("/"))return null;const[dd,mm]=dm.split("/").map(Number);if(!dd||!mm||mm>12||dd>31)return null;const n=new Date(),y=n.getFullYear();let b=new Date(y,mm-1,dd);if(b<=n)b=new Date(y+1,mm-1,dd);return Math.ceil((b-n)/(864e5));}
function isBDtoday(dm){if(!dm||!dm.includes("/"))return false;const[dd,mm]=dm.split("/").map(Number);const n=new Date();return n.getDate()===dd&&n.getMonth()+1===mm;}
function ts2time(ts){if(!ts)return"";const d=new Date(ts);return d.getHours().toString().padStart(2,"0")+":"+d.getMinutes().toString().padStart(2,"0");}
function toArr(obj){return obj?Object.entries(obj).map(([k,v])=>({...v,_id:k})):[];}
function getFace(v,meta){if(v===0)return"😴";if(v<1)return"😐";const p=v/meta;if(p>=1.5)return"🤩";if(p>=1)return"😄";if(p>=.6)return"🙂";if(p>=.3)return"😕";return"😟";}
function getQBadge(rank,total){const p=rank/total;if(IS_NEW.has(ADV[rank]))return'<span class="qn">Nuevo</span>';if(p<.25)return'<span class="q1">Q1</span>';if(p<.5)return'<span class="q2">Q2</span>';if(p<.75)return'<span class="q3">Q3</span>';return'<span class="q4">Q4</span>';}

function showToast(msg){const t=document.getElementById("toast");t.textContent=msg;t.classList.add("on");setTimeout(()=>t.classList.remove("on"),6000);}
function showMsg(id,txt,ok){const el=document.getElementById(id);if(!el)return;el.innerHTML='<div class="msg '+( ok?"mok":"merr")+'">'+txt+'</div>';setTimeout(()=>{if(el)el.innerHTML="";},3000);}

function showSaleAnim(s){
  document.getElementById("saleName").textContent=s.a;
  document.getElementById("saleDetail").textContent=s.pl+" — "+(s.vc<1?"Migración (0.5)":"1 venta completa")+" — "+s.tp;
  document.getElementById("saleBill").textContent=fCOP(s.bl)+" facturados";
  document.getElementById("saleEmoji").textContent=s.vc<1?"📦":"🎯";
  document.getElementById("saleOverlay").classList.add("show");
  playSaleSound();
  const c=document.getElementById("cfWrap");c.innerHTML="";
  const cols=["#0D9488","#F59E0B","#EF4444","#818CF8","#10B981","#3B82F6","#EC4899","#6EE7B7"];
  for(let i=0;i<90;i++){const d=document.createElement("div");d.className="cf";const size=5+Math.random()*8;d.style.cssText=`left:${Math.random()*100}%;top:-10px;background:${cols[i%cols.length]};width:${size}px;height:${size}px;border-radius:${Math.random()>.5?"50%":"3px"};animation:fall ${1.5+Math.random()*2}s ${Math.random()*.5}s linear forwards;`;c.appendChild(d);}
  setTimeout(()=>document.getElementById("saleOverlay").classList.remove("show"),5500);
}

// ── FIREBASE ──────────────────────────────────────────────────────
function fbPush(path,data){dbRef.child(path).push(data);}
function fbSet(path,val){dbRef.child(path).set(val);}
function fbRemove(path){dbRef.child(path).remove();}

// ── FORMS ─────────────────────────────────────────────────────────
function submitSale(){
  const adv=document.getElementById("fAdv").value;
  const day=parseInt(document.getElementById("fDay").value);
  const ekia=document.getElementById("fEkia").value.trim();
  if(!adv||!day||!ekia){showMsg("fMsg","Completa todos los campos",false);return;}
  const p=PLANS[fP],t=TYPES.find(x=>x.v===fT);
  const sale={a:adv,d:day,pl:p.l,vc:t.f,bl:Math.round(p.s*t.f),tp:fT,ek:ekia,ts:new Date().toISOString()};
  fbPush("sales",sale);
  showSaleAnim(sale);
  showMsg("fMsg","¡Venta registrada!",true);
  document.getElementById("fEkia").value="";
  document.getElementById("fDay").value="";
}
function delSale(id){if(!confirm("¿Eliminar esta venta?"))return;fbRemove("sales/"+id);}

function submitEsim(){
  const adv=document.getElementById("esAdv").value;
  const day=parseInt(document.getElementById("esDay").value);
  const cli=document.getElementById("esCli").value.trim();
  const ndoc=document.getElementById("esNdoc").value.trim();
  const ekia=document.getElementById("esEkia").value.trim();
  if(!adv||!day||!cli||!ndoc||!ekia){showMsg("esMsg","Completa los campos obligatorios (*)",false);return;}
  fbPush("esim",{
    a:adv,d:day,cli,
    mail:document.getElementById("esMail").value,
    tdoc:document.getElementById("esTdoc").value,
    ndoc,
    fexp:document.getElementById("esFexp").value,
    op:document.getElementById("esOp").value,
    nport:document.getElementById("esNport").value,
    mod:document.getElementById("esMod").value,
    nip:document.getElementById("esNip").value,
    equipo:document.getElementById("esEquipo").value,
    plan:PLANS[esP].l,type:esT,ekia,
    ped:document.getElementById("esPed").value,
    ts:new Date().toISOString()
  });
  showMsg("esMsg","¡eSIM registrada!",true);
  ["esCli","esMail","esNdoc","esFexp","esNport","esNip","esEquipo","esEkia","esPed"].forEach(id=>{const el=document.getElementById(id);if(el)el.value="";});
  document.getElementById("esDay").value="";
}
function delEsim(id){fbRemove("esim/"+id);}

function submitCancel(){
  const adv=document.getElementById("caAdv").value;
  const day=parseInt(document.getElementById("caDay").value);
  const cli=document.getElementById("caCli").value.trim();
  const ped=document.getElementById("caPed").value.trim();
  if(!adv||!day||!cli||!ped){showMsg("caMsg","Completa los campos",false);return;}
  fbPush("cancel",{
    a:adv,d:day,cli,
    cc:document.getElementById("caCc").value,
    ped,tel:document.getElementById("caTel").value,
    mot:document.getElementById("caMot").value,
    resp:document.getElementById("caResp").value,
    ts:new Date().toISOString()
  });
  showMsg("caMsg","¡Cancelación registrada!",true);
  ["caCli","caCc","caPed","caTel"].forEach(id=>{const el=document.getElementById(id);if(el)el.value="";});
  document.getElementById("caDay").value="";
}
function delCancel(id){fbRemove("cancel/"+id);}
function updateActivas(a,v){fbSet("activas/"+a.replace(/ /g,"_"),parseInt(v)||0);}
function updateBday(a,v){fbSet("bdays/"+a.replace(/ /g,"_"),v);}
function saveTpl(i,v){fbSet("tpl/"+i,v);}

// ── DERIVED ───────────────────────────────────────────────────────
function derived(){
  const sales=toArr(db.sales);
  const aMap={},aTot={};
  ADV.forEach(a=>{aMap[a]={};aTot[a]={v:0,b:0};WD.forEach(d=>aMap[a][d]=0);});
  sales.forEach(s=>{
    if(aMap[s.a]!==undefined&&aMap[s.a][s.d]!==undefined){aMap[s.a][s.d]+=s.vc;}
    if(aTot[s.a]){aTot[s.a].v+=s.vc;aTot[s.a].b+=s.bl;}
  });
  const srt=[...ADV].sort((a,b)=>aTot[b].v-aTot[a].v);
  const totV=Object.values(aTot).reduce((s,a)=>s+a.v,0);
  const totB=Object.values(aTot).reduce((s,a)=>s+a.b,0);
  const eh=eHrs(today);
  const sph=eh>0?totV/(ADV.length*eh):0;
  return{aMap,aTot,srt,totV,totB,eh,sph};
}

// ── RENDER ────────────────────────────────────────────────────────
function renderAll(){
  renderRecentSales();
  if(currentTab==="cantadas")renderCantadas();
  if(currentTab==="ventas")renderVentas();
  if(currentTab==="esim")renderEsim();
  if(currentTab==="cancel")renderCancel();
  if(currentTab==="comisiones")renderComisiones();
  if(currentTab==="cumple")renderBdays();
  updateBdayBanner();
}

function renderRecentSales(){
  const s=toArr(db.sales).sort((a,b)=>new Date(b.ts)-new Date(a.ts));
  document.getElementById("salesCount").textContent=s.length;
  const el=document.getElementById("recentSales");
  if(!s.length){el.innerHTML='<div style="color:var(--mut);font-size:12px">Sin ventas aún</div>';return;}
  el.innerHTML=s.slice(0,8).map(x=>`
    <div style="display:flex;justify-content:space-between;align-items:flex-start;padding:8px 0;border-bottom:1px solid var(--brd);font-size:11px;gap:6px">
      <div>
        <b style="color:var(--txt)">${x.a.split(" ")[0]}</b>
        <span style="color:var(--mut)"> · May ${x.d} · ${x.pl} · </span>
        <span style="color:${x.vc<1?"#FCD34D":"#6EE7B7"};font-weight:600">${x.vc<1?"½ venta":"1 venta"}</span>
        <br><span style="color:var(--mut)">EKIA: ${x.ek} &nbsp;${fCOP(x.bl)} &nbsp;${ts2time(x.ts)}</span>
      </div>
      <button onclick="delSale('${x._id}')" style="border:none;background:none;color:var(--dan);cursor:pointer;font-size:16px;padding:0;line-height:1">×</button>
    </div>`).join("");
}

function renderPodio(items,id,maxV){
  const el=document.getElementById(id);
  const top3=items.filter(x=>x.v>0).slice(0,3);
  if(!top3.length){el.innerHTML='<div style="color:var(--mut);font-size:12px;padding:12px 0">Sin ventas aún</div>';return;}
  const mc=["pm1","pm2","pm3"],em=["🥇","🥈","🥉"];
  el.innerHTML=top3.map((x,i)=>{
    const pct=maxV>0?(x.v/maxV)*100:0;
    const meta=IS_NEW.has(x.a)?3:5;
    return`<div class="podio-item p${i+1}" style="animation-delay:${i*.1}s">
      <div class="podio-medal ${mc[i]}">${em[i]}</div>
      <div style="flex:1">
        <div class="podio-name">${x.a.split(" ")[0]} ${x.a.split(" ")[1]}${IS_NEW.has(x.a)?'<span class="new-badge">N</span>':""}</div>
        <div class="podio-bar-wrap"><div class="podio-bar" style="width:${pct}%"></div></div>
      </div>
      <div style="text-align:right">
        <div class="podio-score">${x.v%1===0?x.v:x.v.toFixed(1)}</div>
        <div style="font-size:16px">${getFace(x.v,meta)}</div>
      </div>
    </div>`;
  }).join("");
}

function renderCantadas(){
  const{aMap,aTot,srt,totV,totB,eh,sph}=derived();
  document.getElementById("kpis").innerHTML=`
    <div class="kpi" style="border-left:3px solid #818CF8"><div class="kl">Total ventas</div><div class="kv">${totV.toFixed(1)}</div></div>
    <div class="kpi" style="border-left:3px solid #6EE7B7"><div class="kl">Meta diaria</div><div class="kv">70</div></div>
    <div class="kpi" style="border-left:3px solid #0D9488"><div class="kl">SPH equipo</div><div class="kv">${sph.toFixed(2)}</div></div>
    <div class="kpi" style="border-left:3px solid #60A5FA"><div class="kl">Facturación</div><div class="kv" style="font-size:14px">${fCOP(totB)}</div></div>`;
  const tTop=ADV.map(a=>({a,v:aMap[a]?.[today]||0})).sort((a,b)=>b.v-a.v);
  const wd=curWeek(today);
  const wTop=ADV.map(a=>({a,v:wd.reduce((s,d)=>s+(aMap[a]?.[d]||0),0)})).sort((a,b)=>b.v-a.v);
  renderPodio(tTop,"podioDia",tTop[0]?.v||1);
  renderPodio(wTop,"podioSem",wTop[0]?.v||1);

  let h=`<table><thead><tr>
    <th class="th-d" style="text-align:left;min-width:110px;padding-left:8px">Asesor</th>
    <th class="th-d" style="min-width:52px">Q</th>
    <th class="th-d">😊</th>`;
  WEEKS.forEach((w,wi)=>{h+=`<th colspan="${w.d.length+1}" style="background:${WC[wi]};color:#fff;border:1px solid ${WC[wi]}22">${w.l}</th>`;});
  h+=`<th class="th-d">Total</th><th class="th-d">SPH</th><th class="th-d" style="min-width:72px">Factura</th></tr>
  <tr><th></th><th></th><th></th>`;
  WEEKS.forEach((w,wi)=>{
    w.d.forEach(d=>{h+=`<th class="${d===today?"tdc":""}" style="min-width:26px"><div style="font-weight:600">${d}</div><div style="font-size:9px;color:var(--mut)">${DN[dow(d)]}${SAT.has(d)?" 4h":""}</div></th>`;});
    h+=`<th style="color:${WC[wi]}">S${wi+1}</th>`;
  });
  h+=`<th></th><th></th><th></th></tr></thead><tbody>`;

  srt.forEach((a,idx)=>{
    const tot=aTot[a],as=eh>0?tot.v/eh:0;
    const meta=IS_NEW.has(a)?3:5;
    const face=getFace(tot.v,meta*(WD.filter(d=>d<=today).length||1));
    const isNew=IS_NEW.has(a);
    const qbadge=isNew?'<span class="qn">Nuevo</span>':getQBadge(idx,ADV.length);
    const bg=idx%2===0?"rgba(255,255,255,0.03)":"rgba(255,255,255,0.01)";
    h+=`<tr style="background:${bg}">
      <td style="text-align:left;padding:3px 8px;font-weight:600;font-size:10px;color:var(--txt)">${a}${isNew?'<span class="new-badge">N</span>':""}</td>
      <td>${qbadge}</td>
      <td style="font-size:14px">${face}</td>`;
    WEEKS.forEach((w,wi)=>{
      const wt=w.d.reduce((s,d)=>s+(aMap[a]?.[d]||0),0);
      w.d.forEach(d=>{const c=aMap[a]?.[d]||0;h+=`<td class="${hcls(c)}${d===today?" tdc":""}">${c>0?(c%1===0?c:c.toFixed(1)):""}</td>`;});
      h+=`<td style="color:${WC[wi]};font-weight:600;background:${WC[wi]}10">${wt>0?(wt%1===0?wt:wt.toFixed(1)):""}</td>`;
    });
    h+=`<td style="background:rgba(13,148,136,0.15);color:#6EE7B7;font-weight:700">${tot.v>0?(tot.v%1===0?tot.v:tot.v.toFixed(1)):"—"}</td>
        <td style="background:rgba(234,179,8,0.1);color:#FCD34D">${as>0?as.toFixed(2):"—"}</td>
        <td style="background:rgba(96,165,250,0.1);color:#93C5FD;font-size:10px">${tot.b>0?fCOP(tot.b):"—"}</td></tr>`;
  });

  h+=`<tr style="background:rgba(15,23,42,0.9)">
    <td style="text-align:left;padding:3px 8px;font-weight:700;color:#818CF8;font-size:10px" colspan="3">EQUIPO</td>`;
  WEEKS.forEach((w,wi)=>{
    const wt=w.d.reduce((s,d)=>s+ADV.reduce((as,a)=>as+(aMap[a]?.[d]||0),0),0);
    w.d.forEach(d=>{const dt=ADV.reduce((s,a)=>s+(aMap[a]?.[d]||0),0);h+=`<td style="background:${dt>0?WC[wi]+"44":"rgba(255,255,255,0.05)"};color:${dt>0?"#fff":"var(--mut)"}${d===today?";outline:2px solid #6EE7B7;outline-offset:-1px":""}">${dt>0?(dt%1===0?dt:dt.toFixed(1)):""}</td>`;});
    h+=`<td style="background:${WC[wi]};color:#fff;font-weight:700">${wt%1===0?wt:wt.toFixed(1)}</td>`;
  });
  h+=`<td style="background:rgba(13,148,136,0.3);color:#6EE7B7;font-weight:700">${totV%1===0?totV:totV.toFixed(1)}</td>
      <td style="background:rgba(234,179,8,0.2);color:#FCD34D">${sph.toFixed(2)}</td>
      <td style="background:rgba(96,165,250,0.2);color:#93C5FD;font-size:10px">${fCOP(totB)}</td></tr></tbody></table>`;
  document.getElementById("heatmap").innerHTML=h;
}

function renderVentas(){
  const fa=document.getElementById("vfAdv")?.value||"";
  const fd=document.getElementById("vfDay")?.value||"";
  const fp=document.getElementById("vfPlan")?.value||"";
  const ft=document.getElementById("vfType")?.value||"";
  const fs=(document.getElementById("vfSearch")?.value||"").toLowerCase();
  let sales=toArr(db.sales).sort((a,b)=>new Date(b.ts)-new Date(a.ts));
  if(fa)sales=sales.filter(s=>s.a===fa);
  if(fd)sales=sales.filter(s=>s.d==fd);
  if(fp)sales=sales.filter(s=>s.pl===fp);
  if(ft)sales=sales.filter(s=>s.tp===ft);
  if(fs)sales=sales.filter(s=>(s.a||"").toLowerCase().includes(fs)||(s.ek||"").includes(fs));
  const bg0="rgba(255,255,255,0.04)",bg1="rgba(255,255,255,0.02)";
  document.getElementById("ventasBody").innerHTML=sales.map((s,i)=>`<tr style="background:${i%2===0?bg0:bg1}">
    <td style="color:var(--txt)">${s.d||""}</td>
    <td style="color:var(--mut)">${s.d?DN[dow(s.d)]+(SAT.has(s.d)?" 4h":""):""}</td>
    <td class="td-l" style="color:var(--txt)">${s.a||""}${IS_NEW.has(s.a)?'<span class="new-badge">N</span>':""}</td>
    <td><span class="badge" style="${s.tp==="migracion"?"background:rgba(234,179,8,0.2);color:#FCD34D;border-color:rgba(234,179,8,0.3)":"background:rgba(13,148,136,0.2);color:#6EE7B7;border-color:rgba(13,148,136,0.3)"}">${s.tp||""}</span></td>
    <td style="color:var(--txt)">${s.pl||""}</td>
    <td style="font-weight:700;color:${s.vc<1?"#FCD34D":"#6EE7B7"}">${s.vc<1?"0.5":"1"}</td>
    <td style="color:#93C5FD">${fCOP(s.bl)}</td>
    <td style="color:var(--mut)">${s.ek||""}</td>
    <td style="color:var(--mut)">${ts2time(s.ts)}</td>
    <td><button onclick="delSale('${s._id}')" style="border:none;background:none;color:var(--dan);cursor:pointer;font-size:14px;padding:0">×</button></td>
  </tr>`).join("");
  document.getElementById("ventasCount").textContent=sales.length+" registro(s)";
}
function clearFilters(){["vfAdv","vfDay","vfPlan","vfType"].forEach(id=>{const el=document.getElementById(id);if(el)el.value="";});document.getElementById("vfSearch").value="";renderVentas();}

function renderEsim(){
  const es=toArr(db.esim).sort((a,b)=>new Date(b.ts)-new Date(a.ts));
  document.getElementById("esimTotal").textContent=es.length;
  const cnt={};ADV.forEach(a=>cnt[a]=es.filter(e=>e.a===a).length);
  const sby=[...ADV].sort((a,b)=>cnt[b]-cnt[a]).filter(a=>cnt[a]>0);
  const bg0="rgba(255,255,255,0.04)",bg1="rgba(255,255,255,0.02)";
  document.getElementById("esimCounts").innerHTML=sby.length?sby.map((a,i)=>`
    <div style="display:flex;justify-content:space-between;align-items:center;padding:5px 0;border-bottom:1px solid var(--brd);font-size:12px">
      <span><span style="color:var(--mut);font-size:10px;margin-right:4px">${i+1}</span><span style="color:var(--txt)">${a}</span>${IS_NEW.has(a)?'<span class="new-badge">N</span>':""}</span>
      <span class="badge bg">${cnt[a]}</span>
    </div>`).join(""):`<div style="color:var(--mut);font-size:12px">Sin registros</div>`;
  document.getElementById("esimBody").innerHTML=es.map((e,i)=>`<tr style="background:${i%2===0?bg0:bg1}">
    <td>${e.d||""}</td><td class="td-l" style="color:var(--txt)">${e.a||""}</td>
    <td class="td-l">${e.cli||""}</td><td>${e.tdoc||""}</td><td>${e.ndoc||""}</td>
    <td style="color:#6EE7B7">${e.fexp||""}</td>
    <td style="font-size:10px;max-width:110px">${e.mail||""}</td>
    <td>${e.op||""}</td><td>${e.nport||""}</td>
    <td style="font-size:10px">${e.mod||""}</td><td>${e.nip||""}</td>
    <td>${e.plan||""}</td><td>${e.type||""}</td>
    <td style="color:var(--mut)">${e.ekia||""}</td><td style="color:var(--mut)">${e.ped||""}</td>
    <td style="font-size:10px">${e.equipo||""}</td>
    <td style="color:var(--mut)">${ts2time(e.ts)}</td>
    <td><button onclick="delEsim('${e._id}')" style="border:none;background:none;color:var(--dan);cursor:pointer;font-size:14px;padding:0">×</button></td>
  </tr>`).join("");
}

function renderCancel(){
  const ca=toArr(db.cancel).sort((a,b)=>new Date(b.ts)-new Date(a.ts));
  document.getElementById("cancelTotal").textContent=ca.length;
  const cnt={};ADV.forEach(a=>cnt[a]=ca.filter(c=>c.a===a).length);
  const sby=[...ADV].sort((a,b)=>cnt[b]-cnt[a]).filter(a=>cnt[a]>0);
  const bg0="rgba(255,255,255,0.04)",bg1="rgba(255,255,255,0.02)";
  document.getElementById("cancelCounts").innerHTML=sby.length?sby.map((a,i)=>`
    <div style="display:flex;justify-content:space-between;align-items:center;padding:5px 0;border-bottom:1px solid var(--brd);font-size:12px">
      <span><span style="color:var(--mut);font-size:10px;margin-right:4px">${i+1}</span><span style="color:var(--txt)">${a}</span></span>
      <span class="badge br">${cnt[a]}</span>
    </div>`).join(""):`<div style="color:var(--mut);font-size:12px">Sin cancelaciones</div>`;
  document.getElementById("cancelBody").innerHTML=ca.map((c,i)=>`<tr style="background:${i%2===0?bg0:bg1}">
    <td>${c.d||""}</td><td class="td-l" style="color:var(--txt)">${c.a||""}</td>
    <td class="td-l">${c.cli||""}</td><td>${c.cc||""}</td>
    <td>${c.ped||""}</td><td>${c.tel||""}</td>
    <td class="td-l" style="font-size:10px;max-width:120px;white-space:normal">${c.mot||""}</td>
    <td><span class="badge" style="${c.resp==="PROCEDENTE"?"background:rgba(16,185,129,0.2);color:#6EE7B7;border-color:rgba(16,185,129,0.3)":"background:rgba(239,68,68,0.2);color:#FCA5A5;border-color:rgba(239,68,68,0.3)"};font-size:9px">${(c.resp||"").slice(0,14)}</span></td>
    <td style="color:var(--mut)">${ts2time(c.ts)}</td>
    <td><button onclick="delCancel('${c._id}')" style="border:none;background:none;color:var(--dan);cursor:pointer;font-size:14px;padding:0">×</button></td>
  </tr>`).join("");
}

function renderComisiones(){
  const{aTot,srt}=derived();
  const activas=db.activas||{};
  const raceGrad=["#0D9488,#6366F1","#6366F1,#EC4899","#0369A1,#0D9488","#059669,#6366F1","#7C3AED,#0D9488","#F59E0B,#EF4444","#10B981,#818CF8","#EF4444,#F59E0B"];
  const bg0="rgba(255,255,255,0.04)",bg1="rgba(255,255,255,0.02)";

  let raceH="";
  srt.forEach((a,idx)=>{
    const akey=a.replace(/ /g,"_"),act=activas[akey]||0;
    const pct=Math.min((act/META_ACTIVAS)*100,100);
    const grad=raceGrad[idx%raceGrad.length];
    const face=getFace(act,META_ACTIVAS);
    const isNew=IS_NEW.has(a);
    const carPos=Math.min(pct,96);
    raceH+=`<div class="race-row">
      <div class="race-name">${a.split(" ")[0]} ${a.split(" ")[1]}${isNew?'<span class="new-badge">N</span>':""}</div>
      <div style="flex:1;padding:0 10px">
        <div class="race-track">
          <div class="race-fill" style="width:${pct}%;background:linear-gradient(90deg,${grad})"></div>
          <span class="race-car" style="left:calc(${carPos}% - 10px)">${pct>=100?"🏁":"🚗"}</span>
        </div>
      </div>
      <div style="font-size:16px">${face}</div>
      <div class="race-pct">${act}/${META_ACTIVAS}</div>
      <input type="number" min="0" class="race-input" value="${act||""}" placeholder="0" onchange="updateActivas('${a}',this.value)">
    </div>`;
  });
  document.getElementById("raceWrap").innerHTML=raceH;

  const sbg=["rgba(209,250,229,0.15)","rgba(167,243,208,0.2)","rgba(110,231,183,0.2)","rgba(52,211,153,0.25)","rgba(16,185,129,0.3)","rgba(5,150,105,0.35)","rgba(4,120,87,0.4)","rgba(6,95,70,0.45)"];
  const stx=["#6EE7B7","#6EE7B7","#34D399","#34D399","#fff","#fff","#fff","#fff"];
  let h=`<table><thead><tr>${["Asesor","Tipo","Factura","Nivel","%","Base","Com. min","Com. max"].map(c=>`<th class="th-d" style="text-align:left;padding:5px 7px">${c}</th>`).join("")}</tr></thead><tbody>`;
  srt.forEach((a,idx)=>{
    const tot=aTot[a],isNew=IS_NEW.has(a);
    const floor=isNew?1800000:2300000;
    const bEff=tot.b>=floor?tot.b:0;
    const r=bEff>0?getCom(bEff):null;
    const si=r?COM.findIndex(c=>bEff>=c.f&&bEff<=c.t):-1;
    h+=`<tr style="background:${idx%2===0?bg0:bg1}">
      <td style="text-align:left;padding:4px 7px;font-weight:600;font-size:10px;color:var(--txt)">${a}${isNew?'<span class="new-badge">N</span>':""}</td>
      <td><span class="${isNew?"qn":"bg"}" style="font-size:9px">${isNew?"Nuevo":"Antiguo"}</span></td>
      <td style="color:#93C5FD;font-size:10px">${tot.b>0?fCOP(tot.b):"—"}</td>
      <td style="background:${si>=0?sbg[si]:""};color:${si>=0?stx[si]:"var(--mut)"};font-weight:600;font-size:10px">${r?"Nv "+(si+1):"—"}</td>
      <td style="font-weight:700;color:#6EE7B7;font-size:10px">${r?(r.p*100)+"%":"—"}</td>
      <td style="font-size:10px;color:var(--txt)">${r?fCOP(Math.round(bEff*r.p)):"—"}</td>
      <td style="color:#818CF8;font-weight:600;font-size:10px">${r?fCOP(r.mn):"—"}</td>
      <td style="color:#6EE7B7;font-weight:600;font-size:10px">${r?(r.mx?fCOP(r.mx):"Abierto"):"—"}</td></tr>`;
  });
  document.getElementById("comTable").innerHTML=h+`</tbody></table>`;
  document.getElementById("comRef").innerHTML=COM.map((r,i)=>`<tr style="background:${i%2===0?bg0:bg1}">
    <td style="font-size:10px;color:var(--txt)">${fCOP(r.f)}</td>
    <td style="font-size:10px;color:var(--txt)">${r.t===Infinity?"4.700.000+":fCOP(r.t)}</td>
    <td style="font-weight:700;color:#6EE7B7">${r.p*100}%</td>
    <td style="font-size:10px">${fCOP(r.mn)}</td>
    <td style="font-size:10px">${r.mx?fCOP(r.mx):"Abierto"}</td></tr>`).join("");
}

function updateBdayBanner(){
  const bdays=db.bdays||{},bdmap={};
  ADV.forEach(a=>bdmap[a]=bdays[a.replace(/ /g,"_")]||"");
  const todayB=ADV.filter(a=>isBDtoday(bdmap[a]));
  const bn=document.getElementById("bdbanner");
  if(todayB.length){bn.textContent="🎂 HOY es el cumpleaños de: "+todayB.map(a=>a.split(" ")[0]).join(", ")+" — ¡Felicitaciones! 🎉🥳";bn.classList.add("on");}
  else bn.classList.remove("on");
}

function renderBdays(){
  const bdays=db.bdays||{},bdmap={};
  ADV.forEach(a=>bdmap[a]=bdays[a.replace(/ /g,"_")]||"");
  const todayB=ADV.filter(a=>isBDtoday(bdmap[a]));
  const up=ADV.map(a=>({a,dm:bdmap[a],d:nextBD(bdmap[a])})).filter(x=>x.d!==null).sort((a,b)=>a.d-b.d);
  const next=up[0];
  const cel=document.getElementById("bdCel");
  if(todayB.length){
    const fw=["✨","🎊","⭐","💫","🌟","🎈","🎉","🥳","🎂","🌈","🎆","🎇"];
    const cols=["#0D9488","#6D28D9","#F59E0B","#10B981","#EF4444","#0369A1","#EC4899"];
    const fwH=Array.from({length:14},(_,i)=>`<span class="bd-fw" style="left:${Math.random()*88}%;top:${Math.random()*60}%;animation-delay:${i*.18}s;animation-duration:${1.2+Math.random()}s;color:${cols[i%cols.length]}">${fw[i%fw.length]}</span>`).join("");
    cel.innerHTML=`<div class="bd-cel">${fwH}<div style="position:relative;font-size:56px;margin-bottom:10px">🎂</div><div style="position:relative;font-size:28px;font-weight:700;background:linear-gradient(135deg,#6EE7B7,#818CF8);-webkit-background-clip:text;-webkit-text-fill-color:transparent;margin-bottom:8px">${todayB.map(a=>a.split(" ")[0]).join(" y ")}</div><div style="position:relative;font-size:18px;color:#A5F3FC;margin-bottom:4px">¡Feliz Cumpleaños! 🎉🥳</div><div style="position:relative;font-size:13px;color:rgba(255,255,255,.5)">De todo el equipo con mucho cariño ❤️</div></div>`;
  } else cel.innerHTML="";
  const cr=document.getElementById("cdRow");
  if(next){
    cr.innerHTML=`<div class="col" style="max-width:215px"><div class="card" style="border-left:3px solid #F59E0B">
      <div style="font-size:10px;color:var(--mut);text-transform:uppercase;letter-spacing:.5px;margin-bottom:5px">🎂 Próximo cumpleaños</div>
      <div style="font-size:14px;font-weight:600;color:#FCD34D;margin-bottom:4px">${next.a}</div>
      <div style="font-size:38px;font-weight:700;background:linear-gradient(135deg,#F59E0B,#FCD34D);-webkit-background-clip:text;-webkit-text-fill-color:transparent;line-height:1">${next.d===0?"¡HOY! 🎉":next.d+" días"}</div>
      <div style="font-size:11px;color:var(--mut);margin-top:5px">📅 ${next.dm}</div>
    </div></div>`+up.slice(1,4).map(x=>`<div class="col" style="max-width:160px"><div class="card bd-card${x.d<=7?" soon":""}">
      <div style="font-size:10px;color:var(--mut);text-transform:uppercase;margin-bottom:3px">Próximamente</div>
      <div style="font-size:13px;font-weight:600;color:var(--txt)">${x.a.split(" ")[0]} ${x.a.split(" ")[1]}</div>
      <div style="font-size:24px;font-weight:700;color:${x.d<=7?"#FCD34D":"#818CF8"}">${x.d===0?"¡HOY!":x.d+" d"}</div>
      <div style="font-size:11px;color:var(--mut)">${x.dm}</div>
    </div></div>`).join("");
  } else cr.innerHTML='<div style="color:var(--mut);font-size:13px;padding:10px 0">Ingresa los cumpleaños para ver el próximo 🗓️</div>';
  document.getElementById("bdGrid").innerHTML=ADV.map(a=>{
    const dm=bdmap[a],isT=isBDtoday(dm),d=nextBD(dm),isSoon=d!==null&&d<=7&&!isT;
    return`<div class="bd-card${isT?" today":isSoon?" soon":""}">
      <div class="bd-name">${a.split(" ")[0]} ${a.split(" ")[1]}${IS_NEW.has(a)?'<span class="new-badge">N</span>':""} ${isT?'<span class="bd-tag">🎂 HOY</span>':isSoon?'<span class="bd-soon-tag">Pronto</span>':""}</div>
      <div class="bd-inp"><input placeholder="DD/MM" maxlength="5" style="flex:1;font-size:12px;padding:5px 8px;color:var(--txt)" value="${dm}" onchange="updateBday('${a}',this.value)"><span class="bd-days">${d!==null?(d===0?"🎉":d+"d"):""}</span></div>
    </div>`;
  }).join("");
}

function renderTickets(){
  const tpls=db.tpl||{};
  document.getElementById("tplCards").innerHTML=TPL.map((t,i)=>`
    <div class="tplcard">
      <div class="tplh" style="border-left:3px solid ${t.c}" onclick="toggleTpl(${i})">
        <span class="tplt" id="tplarr${i}">▶ ${t.title}</span>
        <button class="cpbtn" id="cpbtn${i}" onclick="event.stopPropagation();copyTpl(${i})">Copiar</button>
      </div>
      <div class="tplb" id="tplb${i}">
        <textarea id="tplta${i}" rows="9" oninput="saveTpl(${i},this.value)">${(tpls[i]||t.txt).replace(/</g,"&lt;")}</textarea>
      </div>
    </div>`).join("");
}
let openTpls=new Set();
function toggleTpl(i){const b=document.getElementById("tplb"+i),a=document.getElementById("tplarr"+i);if(openTpls.has(i)){openTpls.delete(i);b.classList.remove("op");a.innerHTML="▶ "+TPL[i].title;}else{openTpls.add(i);b.classList.add("op");a.innerHTML="▼ "+TPL[i].title;}}
function copyTpl(i){if(!openTpls.has(i))toggleTpl(i);const ta=document.getElementById("tplta"+i),btn=document.getElementById("cpbtn"+i);if(!ta||!btn)return;try{navigator.clipboard.writeText(ta.value);}catch(e){ta.select();document.execCommand("copy");}btn.textContent="¡Copiado!";btn.classList.add("ok");setTimeout(()=>{btn.textContent="Copiar";btn.classList.remove("ok");ta.value=TPL[i].txt;saveTpl(i,TPL[i].txt);},3000);}

function setFP(i){fP=i;refreshBtns();updatePreview();}
function setFT(v){fT=v;refreshBtns();updatePreview();}
function setEsP(i){esP=i;refreshBtns();}
function setEsT(v){esT=v;refreshBtns();}
function refreshBtns(){
  PLANS.forEach((_,i)=>{const el=document.querySelector(`#fPlans .pb:nth-child(${i+1})`);if(el)el.className="pb"+(fP===i?" s":"");});
  TYPES.forEach(t=>{document.querySelectorAll("#fTypes .typb").forEach(el=>{if(el.textContent===t.l)el.className="typb"+(fT===t.v?" s":"");});});
  PLANS.forEach((_,i)=>{const el=document.querySelector(`#esPlans .pb:nth-child(${i+1})`);if(el)el.className="pb"+(esP===i?" s":"");});
  TYPES.forEach(t=>{document.querySelectorAll("#esTypes .typb").forEach(el=>{if(el.textContent===t.l)el.className="typb"+(esT===t.v?" s":"");});});
}
function initBtns(){
  document.getElementById("fPlans").innerHTML=PLANS.map((p,i)=>`<button class="pb" onclick="setFP(${i})">${p.l}</button>`).join("");
  document.getElementById("fTypes").innerHTML=TYPES.map(t=>`<button class="typb" onclick="setFT('${t.v}')">${t.l}</button>`).join("");
  document.getElementById("esPlans").innerHTML=PLANS.map((p,i)=>`<button class="pb" onclick="setEsP(${i})">${p.l}</button>`).join("");
  document.getElementById("esTypes").innerHTML=TYPES.map(t=>`<button class="typb" onclick="setEsT('${t.v}')">${t.l}</button>`).join("");
  refreshBtns();
}
function updatePreview(){
  const p=PLANS[fP],t=TYPES.find(x=>x.v===fT),bill=Math.round(p.s*t.f);
  document.getElementById("pvSiva").textContent=fCOP(p.s);
  document.getElementById("pvBill").textContent=fCOP(bill);
  document.getElementById("pvCnt").textContent=t.f<1?"0.5 venta":"1 venta completa";
  document.getElementById("fPreview").style.display="block";
}
function initSelectors(){
  // CLAVE: value="${a}" separado del texto visible que incluye "(Nuevo)"
  const advH=`<option value="">-- Asesor --</option>`+ADV.map(a=>`<option value="${a}">${a}${IS_NEW.has(a)?" (Nuevo)":""}</option>`).join("");
  const dayH=`<option value="">-- Día --</option>`+WD.map(d=>`<option value="${d}">${String(d).padStart(2,"0")} May — ${DN[dow(d)]}${SAT.has(d)?" (4h)":""}${d===today?" HOY":""}</option>`).join("");
  ["fAdv","esAdv","caAdv"].forEach(id=>{const el=document.getElementById(id);if(el)el.innerHTML=advH;});
  ["fDay","esDay","caDay"].forEach(id=>{const el=document.getElementById(id);if(el)el.innerHTML=dayH;});
  document.getElementById("vfAdv").innerHTML=`<option value="">Todos</option>`+ADV.map(a=>`<option value="${a}">${a}</option>`).join("");
  document.getElementById("vfDay").innerHTML=`<option value="">Todos</option>`+WD.map(d=>`<option value="${d}">${String(d).padStart(2,"0")} May</option>`).join("");
  document.getElementById("vfPlan").innerHTML=`<option value="">Todos</option>`+PLANS.map(p=>`<option>${p.l}</option>`).join("");
  document.getElementById("vfType").innerHTML=`<option value="">Todos</option>`+TYPES.map(t=>`<option value="${t.v}">${t.l}</option>`).join("");
  ["vfAdv","vfDay","vfPlan","vfType"].forEach(id=>{const el=document.getElementById(id);if(el)el.addEventListener("change",renderVentas);});
}
function showTab(name){
  document.querySelectorAll(".tab").forEach(el=>el.classList.remove("act"));
  document.querySelectorAll(".tb").forEach(el=>el.classList.remove("act"));
  document.getElementById("tab-"+name).classList.add("act");
  const tabs=["form","cantadas","ventas","esim","cancel","tickets","comisiones","cumple"];
  const idx=tabs.indexOf(name);if(idx>=0&&document.querySelectorAll(".tb")[idx])document.querySelectorAll(".tb")[idx].classList.add("act");
  currentTab=name;
  if(name==="cantadas")renderCantadas();
  if(name==="ventas")renderVentas();
  if(name==="esim")renderEsim();
  if(name==="cancel")renderCancel();
  if(name==="comisiones")renderComisiones();
  if(name==="cumple")renderBdays();
}
function getQBadge(rank,total){const p=rank/total;if(p<.25)return'<span class="q1">Q1</span>';if(p<.5)return'<span class="q2">Q2</span>';if(p<.75)return'<span class="q3">Q3</span>';return'<span class="q4">Q4</span>';}
function init(){
  firebase.initializeApp(firebaseConfig);
  dbRef=firebase.database().ref("/cantadas_may2026_r");
  let firstLoad=true;
  dbRef.on("value",snap=>{
    const nd=snap.val()||{sales:{},esim:{},cancel:{},activas:{},bdays:{},tpl:{}};
    if(!firstLoad){
      const ns=Object.keys(nd.sales||{}).length;
      if(ns>lastSalesN){
        const arr=Object.values(nd.sales||{}).sort((a,b)=>new Date(b.ts)-new Date(a.ts));
        if(arr[0]){showToast("NUEVA VENTA: "+arr[0].a+" — "+arr[0].pl+" — "+fCOP(arr[0].bl));showSaleAnim(arr[0]);}
      }
      lastSalesN=Object.keys(nd.sales||{}).length;
    } else {lastSalesN=Object.keys(nd.sales||{}).length;firstLoad=false;}
    db=nd;
    document.getElementById("app-loading").style.display="none";
    document.getElementById("app-main").style.display="block";
    renderAll();
  });
  initSelectors();initBtns();updatePreview();renderTickets();
}
init();
</script>
</body>
</html>
