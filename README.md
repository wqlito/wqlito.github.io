<!DOCTYPE html>
<html lang="es-AR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, maximum-scale=1.0, user-scalable=no">
<meta name="theme-color" content="#F4F5F8" media="(prefers-color-scheme: light)">
<meta name="theme-color" content="#0A0A0C" media="(prefers-color-scheme: dark)">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Finanzas">
<link rel="manifest" href='data:application/manifest+json,{"name":"Mis Finanzas","short_name":"Finanzas","start_url":".","display":"standalone","background_color":"%230A0A0C","theme_color":"%230A0A0C","icons":[{"src":"data:image/svg+xml,%3Csvg xmlns=%27http://www.w3.org/2000/svg%27 viewBox=%270 0 192 192%27%3E%3Crect width=%27192%27 height=%27192%27 rx=%2242%27 fill=%27%230A6CFF%27/%3E%3Ctext x=%2796%27 y=%27128%27 font-size=%27104%27 text-anchor=%27middle%27 fill=%27white%27 font-family=%27Arial%27%3E%24%3C/text%3E%3C/svg%3E","sizes":"192x192","type":"image/svg+xml"}]}'>
<title>Mis Finanzas</title>
<style>
  :root{
    --bg:#F4F5F8; --card:#FFFFFF; --card-border:rgba(17,24,39,0.06);
    --text:#15171C; --text-2:#6B7180; --text-3:#A2A7B3;
    --sep:rgba(17,24,39,0.07);
    --accent:#0A6CFF; --accent-fill:rgba(10,108,255,0.10);
    --green:#1EA672; --green-2:#22B67F; --red:#E5484D; --tether:#26A17B; --amber:#E8890C;
    --fill:rgba(120,124,138,0.09); --fill-2:rgba(120,124,138,0.16);
    --sheet:#FFFFFF; --scrim:rgba(20,22,28,0.32);
    --nav:rgba(255,255,255,0.72); --nav-border:rgba(17,24,39,0.07);
    --shadow:0 1px 2px rgba(17,24,39,0.04), 0 6px 24px rgba(17,24,39,0.06);
    --shadow-lg:0 12px 44px rgba(17,24,39,0.10);
    --shadow-sheet:0 -20px 60px rgba(17,24,39,0.18);
    --glow-1:rgba(120,150,255,0.16); --glow-2:rgba(180,140,255,0.10); --glow-3:rgba(140,210,255,0.10);
    --radius:22px; --radius-sm:15px;
  }
  html[data-theme="dark"]{
    --bg:#0A0A0C; --card:#151518; --card-border:rgba(255,255,255,0.07);
    --text:#F3F4F6; --text-2:#9599A3; --text-3:#5F626C; --sep:rgba(255,255,255,0.08);
    --accent:#3B8CFF; --accent-fill:rgba(59,140,255,0.16);
    --green:#2DBB84; --green-2:#33C98E; --red:#FF5B60; --tether:#2DBB84; --amber:#F5A623;
    --fill:rgba(140,144,158,0.14); --fill-2:rgba(140,144,158,0.22);
    --sheet:#161619; --scrim:rgba(0,0,0,0.55);
    --nav:rgba(24,24,28,0.68); --nav-border:rgba(255,255,255,0.09);
    --shadow:0 1px 2px rgba(0,0,0,0.4), 0 6px 24px rgba(0,0,0,0.45);
    --shadow-lg:0 16px 50px rgba(0,0,0,0.6); --shadow-sheet:0 -20px 60px rgba(0,0,0,0.6);
    --glow-1:rgba(70,100,220,0.20); --glow-2:rgba(150,90,240,0.12); --glow-3:rgba(60,160,240,0.12);
  }
  @media (prefers-color-scheme: dark){ html:not([data-theme="light"]){
    --bg:#0A0A0C; --card:#151518; --card-border:rgba(255,255,255,0.07);
    --text:#F3F4F6; --text-2:#9599A3; --text-3:#5F626C; --sep:rgba(255,255,255,0.08);
    --accent:#3B8CFF; --accent-fill:rgba(59,140,255,0.16);
    --green:#2DBB84; --green-2:#33C98E; --red:#FF5B60; --tether:#2DBB84; --amber:#F5A623;
    --fill:rgba(140,144,158,0.14); --fill-2:rgba(140,144,158,0.22);
    --sheet:#161619; --scrim:rgba(0,0,0,0.55);
    --nav:rgba(24,24,28,0.68); --nav-border:rgba(255,255,255,0.09);
    --shadow:0 1px 2px rgba(0,0,0,0.4), 0 6px 24px rgba(0,0,0,0.45);
    --shadow-lg:0 16px 50px rgba(0,0,0,0.6); --shadow-sheet:0 -20px 60px rgba(0,0,0,0.6);
    --glow-1:rgba(70,100,220,0.20); --glow-2:rgba(150,90,240,0.12); --glow-3:rgba(60,160,240,0.12);
  }}

  *{box-sizing:border-box; -webkit-tap-highlight-color:transparent;}
  html,body{margin:0; padding:0;}
  body{font-family:-apple-system,BlinkMacSystemFont,"SF Pro Text","SF Pro Display","Inter","Segoe UI",Roboto,system-ui,sans-serif;
    background:var(--bg); color:var(--text); -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    font-size:17px; line-height:1.35; letter-spacing:-0.011em; min-height:100vh;
    padding-bottom:calc(108px + env(safe-area-inset-bottom)); transition:background .4s ease, color .4s ease;}
  body::before{content:""; position:fixed; inset:0; z-index:-1; pointer-events:none;
    background:radial-gradient(120% 70% at 15% -8%, var(--glow-1), transparent 55%),radial-gradient(90% 60% at 92% 4%, var(--glow-2), transparent 52%),radial-gradient(140% 90% at 50% 118%, var(--glow-3), transparent 60%);}
  .app{max-width:580px; margin:0 auto; padding:0 18px;}
  button{font-family:inherit; cursor:pointer; border:none; background:none; color:inherit;}
  input,select,textarea{font-family:inherit; font-size:17px;}
  ::-webkit-scrollbar{display:none;}

  .topbar{display:flex; align-items:center; justify-content:space-between; padding:calc(env(safe-area-inset-top) + 20px) 2px 4px; gap:12px;}
  .topbar .tt{min-width:0; display:flex; align-items:center; gap:10px;}
  .topbar h1{font-size:32px; line-height:1.04; font-weight:800; letter-spacing:-0.025em; margin:0;}
  .header-actions{display:flex; gap:9px; align-items:center; flex-shrink:0;}
  .icon-btn{width:38px; height:38px; border-radius:50%; display:flex; align-items:center; justify-content:center; background:var(--card); border:1px solid var(--card-border); color:var(--accent); box-shadow:var(--shadow); transition:transform .15s ease;}
  .icon-btn:active{transform:scale(.9);}
  .icon-btn svg{width:19px; height:19px;} .add-btn svg{width:21px; height:21px;}
  .icon-btn.neutral{color:var(--text-2);}
  .back-btn{display:inline-flex; align-items:center; gap:3px; color:var(--accent); font-size:17px; font-weight:600; padding:6px 2px;}
  .back-btn svg{width:20px; height:20px;}

  .view{display:none; animation:viewIn .34s cubic-bezier(.32,.72,0,1);}
  .view.active{display:block;}
  @keyframes viewIn{from{opacity:0; transform:translateY(8px);} to{opacity:1; transform:translateY(0);}}

  .hero{padding:20px 4px 6px;}
  .status-pill{display:inline-flex; align-items:center; gap:8px; margin-bottom:16px; background:var(--card); border:1px solid var(--card-border); border-radius:999px; padding:6px 10px 6px 12px; font-size:13px; font-weight:600; color:var(--text-2); box-shadow:var(--shadow); transition:transform .15s ease;}
  .status-pill:active{transform:scale(.96);}
  .status-pill .live{width:7px; height:7px; border-radius:50%; background:var(--green-2); box-shadow:0 0 0 3px rgba(34,182,127,.18);}
  .status-pill .live.stale{background:var(--amber); box-shadow:0 0 0 3px rgba(245,166,35,.18);}
  .status-pill b{color:var(--text); font-weight:750;}
  .status-pill .rfr{width:15px; height:15px; opacity:.7;}
  .hero .label{color:var(--text-2); font-size:15px; font-weight:600; margin-bottom:8px;}
  .hero .balance{font-size:52px; font-weight:800; letter-spacing:-0.035em; line-height:0.98; font-variant-numeric:tabular-nums;}
  .hero .balance .cents{font-size:28px; color:var(--text-2); font-weight:700;}
  .hero .sub{margin-top:16px; display:flex; gap:9px; flex-wrap:wrap;}
  .pill{display:inline-flex; align-items:center; gap:7px; background:var(--card); border:1px solid var(--card-border); border-radius:999px; padding:8px 14px; font-size:13.5px; font-weight:600; box-shadow:var(--shadow); color:var(--text-2);}
  .pill b{font-weight:750; color:var(--text); font-variant-numeric:tabular-nums;}
  .pill.tether b{color:var(--tether);}
  .dot{width:8px; height:8px; border-radius:50%;} .dot.g{background:var(--green-2);} .dot.r{background:var(--red);} .dot.t{background:var(--tether);}

  .quick{display:grid; grid-template-columns:repeat(3,1fr); gap:11px; margin:22px 0 8px;}
  .quick button{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius-sm); padding:15px 8px; display:flex; flex-direction:column; align-items:center; gap:9px; box-shadow:var(--shadow); font-size:13px; font-weight:650; transition:transform .15s ease;}
  .quick button:active{transform:scale(.95);}
  .q-ico{width:42px; height:42px; border-radius:13px; display:flex; align-items:center; justify-content:center; flex-shrink:0;}
  .q-ico svg{width:21px; height:21px; color:#fff;}
  .q-ico.in{background:var(--green);} .q-ico.out{background:var(--red);} .q-ico.conv{background:var(--tether);}

  .section-head{display:flex; align-items:baseline; justify-content:space-between; margin:28px 4px 12px;}
  .section-head h2{font-size:21px; font-weight:750; letter-spacing:-0.02em; margin:0;}
  .section-head .link{color:var(--accent); font-size:15px; font-weight:600;}

  .list{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius); box-shadow:var(--shadow); overflow:hidden;}
  .row{display:flex; align-items:center; gap:14px; padding:13px 16px; position:relative; transition:background .12s ease;}
  .row:active{background:var(--fill);}
  .row + .row::before{content:""; position:absolute; top:0; left:62px; right:0; height:1px; background:var(--sep);}
  .row .ico{width:40px; height:40px; border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:19px; flex-shrink:0;}
  .row .mid{flex:1; min-width:0;} .row .title{font-size:16px; font-weight:600; white-space:nowrap; overflow:hidden; text-overflow:ellipsis;}
  .row .meta{font-size:13px; color:var(--text-2); margin-top:1px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis;}
  .row .amt{font-size:16px; font-weight:700; font-variant-numeric:tabular-nums; white-space:nowrap; letter-spacing:-0.01em; text-align:right;}
  .row .amt .amt2{font-size:12px; font-weight:600; color:var(--text-3); margin-top:1px;}
  .amt.in{color:var(--green);}
  .chevron{color:var(--text-3); width:14px; height:14px; flex-shrink:0;}
  .tag{font-size:11px; font-weight:700; padding:2px 7px; border-radius:6px; background:var(--fill-2); color:var(--text-2);}
  .tag.fijo{background:var(--accent-fill); color:var(--accent);}

  .stat-card{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius); box-shadow:var(--shadow); padding:18px 20px; margin-bottom:15px;}
  .stat-card .label{color:var(--text-2); font-size:14px; font-weight:600;}
  .stat-card .big{font-size:32px; font-weight:800; letter-spacing:-0.03em; margin-top:5px; font-variant-numeric:tabular-nums;}
  .stat-card .note{color:var(--text-2); font-size:13.5px; font-weight:500; margin-top:8px;}
  .stat-2{display:grid; grid-template-columns:1fr 1fr; gap:13px; margin-bottom:15px;}
  .stat-2 .stat-card{margin-bottom:0; padding:16px 17px;} .stat-2 .big{font-size:23px;}
  .wallet-pills{display:flex; flex-wrap:wrap; gap:9px; margin:2px 4px 20px;}

  .acct-scroll{display:flex; gap:12px; overflow-x:auto; padding:2px 4px 6px; margin:0 -4px; scroll-snap-type:x mandatory;}
  .acct-card{flex:0 0 auto; min-width:150px; background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius-sm); box-shadow:var(--shadow); padding:14px 16px; scroll-snap-align:start; transition:transform .15s ease;}
  .acct-card:active{transform:scale(.97);}
  .acct-card .ah{display:flex; align-items:center; gap:8px; font-size:13.5px; font-weight:650; color:var(--text-2);}
  .acct-card .ah .e{font-size:17px;}
  .acct-card .ab{font-size:22px; font-weight:800; letter-spacing:-0.02em; margin-top:8px; font-variant-numeric:tabular-nums;}
  .acct-card .ap{font-size:12.5px; color:var(--text-3); font-weight:600; margin-top:2px;}
  .acct-card.add{display:flex; align-items:center; justify-content:center; color:var(--text-2); min-width:60px; font-size:26px; border-style:dashed;}

  .seg{display:flex; background:var(--fill); border-radius:12px; padding:3px; gap:3px; margin:0 0 16px;}
  .seg button{flex:1; padding:9px 0; border-radius:9px; font-size:14px; font-weight:600; color:var(--text); transition:all .22s ease;}
  .seg button.on{background:var(--card); box-shadow:0 1px 4px rgba(0,0,0,.12); font-weight:700;}
  html[data-theme="dark"] .seg button.on{background:#3A3A40;}
  @media (prefers-color-scheme: dark){ html:not([data-theme="light"]) .seg button.on{background:#3A3A40;} }

  .chips{display:flex; flex-wrap:wrap; gap:8px; margin:2px 0 6px;}
  .chip{display:inline-flex; align-items:center; gap:6px; background:var(--fill); border:1px solid transparent; border-radius:999px; padding:8px 13px; font-size:14px; font-weight:600; color:var(--text); transition:all .18s ease;}
  .chip.on{background:var(--accent-fill); border-color:var(--accent); color:var(--accent);}

  .empty{text-align:center; padding:48px 24px; color:var(--text-2);}
  .empty .e-ico{width:64px; height:64px; margin:0 auto 15px; border-radius:20px; background:var(--card); border:1px solid var(--card-border); box-shadow:var(--shadow); display:flex; align-items:center; justify-content:center;}
  .empty .e-ico svg{width:29px; height:29px; color:var(--text-3);}
  .empty h3{font-size:19px; font-weight:750; color:var(--text); margin:0 0 5px;}
  .empty p{font-size:15px; margin:0 auto; max-width:270px;}
  .group-label{font-size:13px; font-weight:650; color:var(--text-2); margin:22px 6px 9px; display:flex; justify-content:space-between;}

  .tabbar{position:fixed; left:0; right:0; bottom:0; z-index:40; display:flex; justify-content:center; padding:0 12px calc(16px + env(safe-area-inset-bottom)); pointer-events:none;}
  .tabbar .inner{pointer-events:auto; display:flex; align-items:center; gap:2px; background:var(--nav); backdrop-filter:saturate(180%) blur(26px); -webkit-backdrop-filter:saturate(180%) blur(26px); border:1px solid var(--nav-border); border-radius:999px; padding:6px; box-shadow:var(--shadow-lg);}
  .tab{display:flex; align-items:center; color:var(--text-2); border-radius:999px; padding:11px; transition:all .34s cubic-bezier(.32,.72,0,1);}
  .tab svg{width:22px; height:22px; flex-shrink:0;}
  .tab span{font-size:13.5px; font-weight:650; max-width:0; overflow:hidden; white-space:nowrap; opacity:0; transition:all .34s cubic-bezier(.32,.72,0,1);}
  .tab:active{transform:scale(.92);}
  .tab.on{color:var(--accent); background:var(--accent-fill); padding:11px 15px 11px 12px;}
  .tab.on span{max-width:130px; opacity:1; margin-left:7px;}

  .scrim{position:fixed; inset:0; background:var(--scrim); opacity:0; pointer-events:none; transition:opacity .3s ease; z-index:50; backdrop-filter:blur(2px);}
  .scrim.show{opacity:1; pointer-events:auto;}
  .sheet{position:fixed; left:0; right:0; bottom:0; z-index:60; background:var(--sheet); border-radius:26px 26px 0 0; box-shadow:var(--shadow-sheet); border-top:1px solid var(--nav-border); transform:translateY(102%); transition:transform .44s cubic-bezier(.32,.72,0,1); max-width:580px; margin:0 auto; max-height:93vh; overflow-y:auto; padding-bottom:env(safe-area-inset-bottom);}
  .sheet.show{transform:translateY(0);}
  .grabber{width:38px; height:5px; border-radius:3px; background:var(--fill-2); margin:10px auto 0;}
  .sheet-head{display:flex; align-items:center; justify-content:space-between; padding:12px 22px 6px;}
  .sheet-head .cancel{color:var(--accent); font-size:17px; font-weight:400;}
  .sheet-head .save{color:var(--accent); font-size:17px; font-weight:700;}
  .sheet-head .save:disabled{color:var(--text-3);}
  .sheet-head h3{font-size:17px; font-weight:750; margin:0;}
  .sheet-body{padding:14px 22px 30px;}

  .amount-field{text-align:center; padding:14px 0 20px;}
  .amount-field .cur{font-size:30px; font-weight:600; color:var(--text-2); vertical-align:18px;}
  .amount-field input{border:none; background:none; text-align:center; width:100%; font-size:54px; font-weight:800; letter-spacing:-0.035em; color:var(--text); outline:none; font-variant-numeric:tabular-nums; padding:0;}
  .amount-field input::placeholder{color:var(--text-3);}
  .amount-field.income input{color:var(--green);} .amount-field.expense input{color:var(--red);} .amount-field.tether input{color:var(--tether);}
  .calc-line{text-align:center; color:var(--text-2); font-size:15px; font-weight:600; margin:-8px 0 18px; font-variant-numeric:tabular-nums;}

  .field{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius-sm); box-shadow:var(--shadow); margin-bottom:14px; overflow:hidden;}
  .field .f-row{display:flex; align-items:center; padding:13px 16px; gap:12px; min-height:50px;}
  .field .f-row + .f-row{border-top:1px solid var(--sep);}
  .field label{font-size:16px; font-weight:500; color:var(--text); flex-shrink:0; min-width:82px;}
  .field input, .field select, .field textarea{border:none; background:none; outline:none; flex:1; color:var(--text); text-align:right; font-size:16px; padding:0;}
  .field textarea{text-align:left; resize:none; min-height:22px; line-height:1.4;}
  .field input::placeholder, .field textarea::placeholder{color:var(--text-3);}
  .fieldwrap-label{font-size:13px; font-weight:650; color:var(--text-2); margin:20px 6px 9px;}

  .cat-grid{display:grid; grid-template-columns:repeat(4,1fr); gap:12px; margin:6px 0 16px;}
  .cat{display:flex; flex-direction:column; align-items:center; gap:7px; padding:2px 0; transition:transform .12s ease;}
  .cat:active{transform:scale(.9);}
  .cat .c-ico{width:52px; height:52px; border-radius:16px; display:flex; align-items:center; justify-content:center; font-size:24px; transition:box-shadow .2s ease;}
  .cat.sel .c-ico{box-shadow:0 0 0 3px var(--sheet), 0 0 0 5.5px var(--accent);}
  .cat span{font-size:11.5px; color:var(--text-2); font-weight:500; text-align:center; max-width:100%; overflow:hidden; text-overflow:ellipsis; white-space:nowrap;}
  .cat.sel span{color:var(--text); font-weight:650;}
  .cat.add .c-ico{background:var(--fill); color:var(--text-2); border:1px dashed var(--card-border);}

  .btn-primary{width:100%; background:var(--accent); color:#fff; font-size:16px; font-weight:650; padding:15px; border-radius:14px; margin-top:8px; transition:transform .15s ease;}
  .btn-primary:active{transform:scale(.98);}
  .btn-soft{width:100%; background:var(--fill); color:var(--text); font-size:16px; font-weight:650; padding:15px; border-radius:14px; margin-top:10px;}
  .btn-danger{width:100%; background:var(--fill); color:var(--red); font-size:16px; font-weight:650; padding:15px; border-radius:14px; margin-top:12px; transition:transform .15s ease;}
  .btn-danger:active{transform:scale(.98);}

  .paid-toggle{width:29px; height:29px; border-radius:50%; border:2px solid var(--text-3); display:flex; align-items:center; justify-content:center; flex-shrink:0; transition:all .2s ease;}
  .paid-toggle.on{background:var(--green); border-color:var(--green);}
  .paid-toggle svg{width:16px; height:16px; color:#fff; opacity:0; transition:opacity .2s ease;}
  .paid-toggle.on svg{opacity:1;}
  .settled{opacity:.5;} .settled .title{text-decoration:line-through;}
  .switch{width:51px; height:31px; border-radius:999px; background:var(--fill-2); position:relative; transition:background .25s ease; flex-shrink:0;}
  .switch.on{background:var(--green);}
  .switch .knob{position:absolute; top:2px; left:2px; width:27px; height:27px; border-radius:50%; background:#fff; box-shadow:0 1px 3px rgba(0,0,0,.3); transition:transform .25s cubic-bezier(.32,.72,0,1);}
  .switch.on .knob{transform:translateX(20px);}

  /* charts */
  .chart-card{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius); box-shadow:var(--shadow); padding:18px 18px 14px; margin-bottom:15px;}
  .chart-card h3{font-size:16px; font-weight:700; margin:0 0 14px;}
  .bar-row{display:flex; align-items:center; gap:11px; margin-bottom:12px;}
  .bar-row .bl{width:30px; height:30px; border-radius:9px; display:flex; align-items:center; justify-content:center; font-size:15px; flex-shrink:0;}
  .bar-row .bmid{flex:1; min-width:0;}
  .bar-row .bt{display:flex; justify-content:space-between; font-size:13.5px; font-weight:600; margin-bottom:5px;}
  .bar-row .bt .bv{font-variant-numeric:tabular-nums; color:var(--text-2);}
  .bar-track{height:8px; border-radius:4px; background:var(--fill); overflow:hidden;}
  .bar-fill{height:100%; border-radius:4px; transition:width .5s cubic-bezier(.32,.72,0,1);}
  .prog-over .bar-fill{background:var(--red)!important;}
  .prog-over .bv{color:var(--red)!important;}

  .menu-list{background:var(--card); border:1px solid var(--card-border); border-radius:var(--radius); box-shadow:var(--shadow); overflow:hidden; margin-bottom:15px;}
  .menu-item{display:flex; align-items:center; gap:14px; padding:15px 16px; position:relative; transition:background .12s ease;}
  .menu-item:active{background:var(--fill);}
  .menu-item + .menu-item::before{content:""; position:absolute; top:0; left:56px; right:0; height:1px; background:var(--sep);}
  .menu-item .mi-ico{width:30px; height:30px; border-radius:9px; display:flex; align-items:center; justify-content:center; flex-shrink:0;}
  .menu-item .mi-ico svg{width:17px; height:17px; color:#fff;}
  .menu-item .mt{flex:1; font-size:16px; font-weight:600;}
  .menu-item .ms{font-size:14px; color:var(--text-3); font-weight:500;}

  @media (prefers-reduced-motion: reduce){ *{animation:none !important; transition:none !important;} }
</style>
</head>
<body>
<div class="app">
  <!-- INICIO -->
  <section class="view active" id="view-inicio">
    <div class="topbar"><div class="tt"><h1>Inicio</h1></div>
      <div class="header-actions"><button class="icon-btn neutral" id="themeBtn"></button><button class="icon-btn add-btn" onclick="openTxSheet()"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <div class="hero">
      <button class="status-pill" onclick="openDollarSheet()"><span class="live" id="rateDot"></span><span id="ratePill">Dólar blue</span><svg class="rfr" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 2v6h-6M3 12a9 9 0 0 1 15-6.7L21 8M3 22v-6h6M21 12a9 9 0 0 1-15 6.7L3 16"/></svg></button>
      <div class="label">Patrimonio en pesos</div>
      <div class="balance" id="heroBalance">$0</div>
      <div class="sub">
        <span class="pill tether"><span class="dot t"></span>En USDT <b id="heroUsdt">US$0</b></span>
        <span class="pill"><span class="dot g"></span>En pesos <b id="heroPesos">$0</b></span>
      </div>
    </div>
    <div class="quick">
      <button onclick="openTxSheet('ingreso')"><span class="q-ico in"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round"><path d="M12 19V5M5 12l7-7 7 7"/></svg></span>Ingreso</button>
      <button onclick="openTxSheet('gasto')"><span class="q-ico out"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round"><path d="M12 5v14M5 12l7 7 7-7"/></svg></span>Gasto</button>
      <button onclick="openTransferSheet()"><span class="q-ico conv"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="M17 2l4 4-4 4M21 6H7M7 22l-4-4 4-4M3 18h14"/></svg></span>Convertir</button>
    </div>
    <div class="section-head"><h2>Cuentas</h2><button class="link" onclick="openSub('cuentas')">Gestionar</button></div>
    <div class="acct-scroll" id="acctScroll"></div>
    <div id="dueAlerts"></div>
    <div class="section-head"><h2>Últimos movimientos</h2><button class="link" onclick="switchTab('movimientos')">Ver todos</button></div>
    <div id="recentList"></div>
  </section>

  <!-- MOVIMIENTOS -->
  <section class="view" id="view-movimientos">
    <div class="topbar"><div class="tt"><h1>Movimientos</h1></div>
      <div class="header-actions"><button class="icon-btn add-btn" onclick="openTxSheet()"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <div class="field" style="margin-top:14px; margin-bottom:12px"><div class="f-row"><svg viewBox="0 0 24 24" width="18" height="18" fill="none" stroke="var(--text-3)" stroke-width="2" stroke-linecap="round"><circle cx="11" cy="11" r="7"/><path d="m21 21-4.3-4.3"/></svg><input id="txSearch" placeholder="Buscar por detalle o categoría" style="text-align:left" oninput="render()"></div></div>
    <div class="seg" id="txFilter">
      <button class="on" data-f="todos" onclick="setTxFilter('todos')">Todos</button>
      <button data-f="ingreso" onclick="setTxFilter('ingreso')">Ingresos</button>
      <button data-f="gasto" onclick="setTxFilter('gasto')">Gastos</button>
      <button data-f="fijo" onclick="setTxFilter('fijo')">Fijos</button>
    </div>
    <div class="chips" id="rangeChips" style="margin-bottom:8px">
      <button class="chip on" data-r="mes" onclick="setRange('mes')">Este mes</button>
      <button class="chip" data-r="prev" onclick="setRange('prev')">Mes pasado</button>
      <button class="chip" data-r="anio" onclick="setRange('anio')">Este año</button>
      <button class="chip" data-r="todo" onclick="setRange('todo')">Todo</button>
    </div>
    <div id="txList"></div>
  </section>

  <!-- ANALISIS -->
  <section class="view" id="view-analisis">
    <div class="topbar"><div class="tt"><h1>Análisis</h1></div></div>
    <div class="stat-2" style="margin-top:18px">
      <div class="stat-card"><div class="label">Ingresos del mes</div><div class="big" style="color:var(--green)" id="anIn">$0</div></div>
      <div class="stat-card"><div class="label">Gastos del mes</div><div class="big" id="anOut">$0</div></div>
    </div>
    <div class="chart-card"><h3>Gastos por categoría · este mes</h3><div id="catChart"></div></div>
    <div class="chart-card"><h3>Ingresos vs gastos · últimos 6 meses</h3><div id="monthChart"></div></div>
    <div class="section-head"><h2>Presupuestos</h2><button class="link" onclick="openBudgetSheet()">Agregar</button></div>
    <div id="budgetList"></div>
  </section>

  <!-- USDT -->
  <section class="view" id="view-usdt">
    <div class="topbar"><div class="tt"><h1>USDT</h1></div>
      <div class="header-actions"><button class="icon-btn add-btn" onclick="openTransferSheet('conv')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <div class="stat-card" style="margin-top:18px">
      <div class="label">Tenés en USDT</div><div class="big" style="color:var(--tether)" id="usdtBalance">US$0</div>
      <div class="note" id="usdtValue"></div>
    </div>
    <div class="stat-2">
      <div class="stat-card"><div class="label">Cobrado en P2P</div><div class="big" style="color:var(--green)" id="p2pTotal">$0</div></div>
      <div class="stat-card"><div class="label">Comprado</div><div class="big" id="boughtTotal">$0</div></div>
    </div>
    <div id="walletBreak"></div>
    <div class="section-head"><h2>Conversiones</h2></div>
    <div id="convList"></div>
  </section>

  <!-- MAS -->
  <section class="view" id="view-mas">
    <div class="topbar"><div class="tt"><h1>Más</h1></div></div>
    <div class="menu-list" style="margin-top:18px">
      <div class="menu-item" onclick="openSub('cuentas')"><span class="mi-ico" style="background:#0A6CFF"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 7a2 2 0 0 1 2-2h14a1 1 0 0 1 1 1v3H4"/><path d="M3 7v10a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/><circle cx="17" cy="13.5" r="1.2"/></svg></span><div class="mt">Cuentas y billeteras</div><svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>
      <div class="menu-item" onclick="openSub('fijos')"><span class="mi-ico" style="background:#5856D6"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 2l4 4-4 4M3 11V9a4 4 0 0 1 4-4h14M7 22l-4-4 4-4M21 13v2a4 4 0 0 1-4 4H3"/></svg></span><div class="mt">Fijos y recurrentes</div><svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>
      <div class="menu-item" onclick="openSub('deudas')"><span class="mi-ico" style="background:#E8890C"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="9" cy="8" r="3.2"/><path d="M3.5 20a5.5 5.5 0 0 1 11 0"/><path d="M17 8h4M19 6v4"/></svg></span><div class="mt">Deudas</div><svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>
      <div class="menu-item" onclick="openSub('categorias')"><span class="mi-ico" style="background:#00C7BE"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="7" height="7" rx="2"/><rect x="14" y="3" width="7" height="7" rx="2"/><rect x="3" y="14" width="7" height="7" rx="2"/><rect x="14" y="14" width="7" height="7" rx="2"/></svg></span><div class="mt">Categorías</div><svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>
      <div class="menu-item" onclick="openSub('backup')"><span class="mi-ico" style="background:#1EA672"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4M7 10l5 5 5-5M12 15V3"/></svg></span><div class="mt">Respaldo y datos</div><svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>
    </div>
    <div id="installWrap"></div>
    <p style="text-align:center; color:var(--text-3); font-size:13px; margin-top:24px">Mis Finanzas · datos guardados en este dispositivo</p>
  </section>

  <!-- SUB: CUENTAS -->
  <section class="view" id="view-cuentas">
    <div class="topbar"><div class="tt"><button class="back-btn" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="m15 6-6 6 6 6"/></svg>Más</button></div>
      <div class="header-actions"><button class="icon-btn add-btn" onclick="openAccountSheet()"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <h1 style="font-size:30px; font-weight:800; letter-spacing:-0.025em; margin:8px 2px 16px">Cuentas</h1>
    <div id="accountList"></div>
  </section>

  <!-- SUB: FIJOS -->
  <section class="view" id="view-fijos">
    <div class="topbar"><div class="tt"><button class="back-btn" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="m15 6-6 6 6 6"/></svg>Más</button></div></div>
    <h1 style="font-size:30px; font-weight:800; letter-spacing:-0.025em; margin:8px 2px 16px">Fijos y recurrentes</h1>
    <div class="stat-2">
      <div class="stat-card"><div class="label">Gastos fijos</div><div class="big" id="fixedTotal">$0</div><div class="note" id="fixedPaidLabel"></div></div>
      <div class="stat-card"><div class="label">Ingresos recurrentes</div><div class="big" style="color:var(--green)" id="recurTotal">$0</div><div class="note" id="recurPaidLabel"></div></div>
    </div>
    <div class="section-head"><h2>Gastos fijos</h2><button class="link" onclick="openFixedSheet()">Agregar</button></div>
    <div id="fixedList"></div>
    <div class="section-head"><h2>Ingresos recurrentes</h2><button class="link" onclick="openRecurSheet()">Agregar</button></div>
    <div id="recurList"></div>
  </section>

  <!-- SUB: DEUDAS -->
  <section class="view" id="view-deudas">
    <div class="topbar"><div class="tt"><button class="back-btn" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="m15 6-6 6 6 6"/></svg>Más</button></div>
      <div class="header-actions"><button class="icon-btn add-btn" onclick="openDebtSheet()"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <h1 style="font-size:30px; font-weight:800; letter-spacing:-0.025em; margin:8px 2px 16px">Deudas</h1>
    <div class="stat-2">
      <div class="stat-card"><div class="label">Te deben</div><div class="big" style="color:var(--green)" id="debtOwedTotal">$0</div></div>
      <div class="stat-card"><div class="label">Debés</div><div class="big" style="color:var(--red)" id="debtOweTotal">$0</div></div>
    </div>
    <div id="debtList"></div>
  </section>

  <!-- SUB: CATEGORIAS -->
  <section class="view" id="view-categorias">
    <div class="topbar"><div class="tt"><button class="back-btn" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="m15 6-6 6 6 6"/></svg>Más</button></div>
      <div class="header-actions"><button class="icon-btn add-btn" onclick="openCatSheet('gasto')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round"><path d="M12 5v14M5 12h14"/></svg></button></div>
    </div>
    <h1 style="font-size:30px; font-weight:800; letter-spacing:-0.025em; margin:8px 2px 16px">Categorías</h1>
    <div class="section-head"><h2>Gastos</h2></div><div id="catListGasto"></div>
    <div class="section-head"><h2>Ingresos</h2></div><div id="catListIngreso"></div>
  </section>

  <!-- SUB: BACKUP -->
  <section class="view" id="view-backup">
    <div class="topbar"><div class="tt"><button class="back-btn" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"><path d="m15 6-6 6 6 6"/></svg>Más</button></div></div>
    <h1 style="font-size:30px; font-weight:800; letter-spacing:-0.025em; margin:8px 2px 6px">Respaldo y datos</h1>
    <p style="color:var(--text-2); font-size:15px; margin:0 2px 18px">Tus datos viven en este dispositivo. Descargá un respaldo cada tanto para no perder nada.</p>
    <button class="btn-primary" onclick="exportJSON()">Descargar respaldo (.json)</button>
    <button class="btn-soft" onclick="document.getElementById('importFile').click()">Restaurar desde archivo</button>
    <button class="btn-soft" onclick="exportCSV()">Exportar movimientos (.csv)</button>
    <input type="file" id="importFile" accept="application/json,.json" style="display:none" onchange="importJSON(this)">
    <div id="backupInfo" style="text-align:center; color:var(--text-3); font-size:13.5px; margin-top:16px"></div>
    <button class="btn-danger" style="margin-top:26px" onclick="wipeAll()">Borrar todos los datos</button>
  </section>
</div>

<!-- NAV -->
<nav class="tabbar"><div class="inner">
  <button class="tab on" data-tab="inicio" onclick="switchTab('inicio')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 10.5 12 3l9 7.5"/><path d="M5 9.5V21h14V9.5"/></svg><span>Inicio</span></button>
  <button class="tab" data-tab="movimientos" onclick="switchTab('movimientos')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 3v14m0 0-4-4m4 4 4-4M7 21V7m0 0-4 4m4-4 4 4"/></svg><span>Movimientos</span></button>
  <button class="tab" data-tab="analisis" onclick="switchTab('analisis')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 20V10M10 20V4M16 20v-7M22 20H2"/></svg><span>Análisis</span></button>
  <button class="tab" data-tab="usdt" onclick="switchTab('usdt')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v10M8.5 10h7M9 14h6"/></svg><span>USDT</span></button>
  <button class="tab" data-tab="mas" onclick="switchTab('mas')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><circle cx="5" cy="12" r="1.4"/><circle cx="12" cy="12" r="1.4"/><circle cx="19" cy="12" r="1.4"/></svg><span>Más</span></button>
</div></nav>

<div class="scrim" id="scrim" onclick="closeSheet()"></div>
<div class="sheet" id="sheet"><div class="grabber"></div><div id="sheetContent"></div></div>

<datalist id="walletList"><option value="Lemon"></option><option value="Mercado Pago"></option><option value="Belo"></option><option value="Binance"></option><option value="Prex"></option><option value="Brubank"></option><option value="Naranja X"></option><option value="Ualá"></option><option value="Astropay"></option><option value="Efectivo"></option><option value="Banco"></option></datalist>

<script>
"use strict";
const KEY="mifinanzas-v3";
let state=null, memFallback=null, txFilter="todos", txRange="mes", installEvent=null;

/* ---------- Storage ---------- */
async function loadState(){
  let raw=null;
  try{ if(window.storage&&window.storage.get){ const r=await window.storage.get(KEY); if(r&&r.value) raw=r.value; } else if(memFallback) raw=memFallback; }catch(e){}
  state = raw?normalize(JSON.parse(raw)):normalize({});
  if(!state.accounts.length){
    state.accounts=[
      {id:uid(),name:"USDT",currency:"USDT",emoji:"🪙",color:"#26A17B"},
      {id:uid(),name:"Efectivo",currency:"ARS",emoji:"💵",color:"#34C759"},
      {id:uid(),name:"Mercado Pago",currency:"ARS",emoji:"💳",color:"#00B1EA"}
    ];
    await saveState();
  }
}
async function saveState(){ const j=JSON.stringify(state); memFallback=j; try{ if(window.storage&&window.storage.set) await window.storage.set(KEY,j); }catch(e){} }
function normalize(s){
  return {
    accounts:arr(s.accounts), transactions:arr(s.transactions), transfers:arr(s.transfers),
    fixed:arr(s.fixed), recur:arr(s.recur), debts:arr(s.debts),
    budgets:s.budgets&&typeof s.budgets==="object"?s.budgets:{},
    customCats:{gasto:arr(s.customCats&&s.customCats.gasto), ingreso:arr(s.customCats&&s.customCats.ingreso)},
    settings:Object.assign({theme:"auto", dollar:{type:"blue",compra:0,venta:0,updated:null,manual:0}}, s.settings||{})
  };
}
function arr(x){ return Array.isArray(x)?x:[]; }
function uid(){ return Date.now().toString(36)+Math.random().toString(36).slice(2,7); }

/* ---------- Utils ---------- */
const nf=new Intl.NumberFormat("es-AR",{minimumFractionDigits:0,maximumFractionDigits:2});
function round2(n){ return Math.round((n+Number.EPSILON)*100)/100; }
function fmt(n){ return "$"+nf.format(round2(n)); }
function fmtUsd(n){ return "US$"+nf.format(round2(n)); }
function fmtC(n,cur){ return cur==="USDT"?fmtUsd(n):fmt(n); }
function fmtHero(n){ const neg=n<0,a=Math.abs(n),s=nf.format(round2(a)).split(","); const c=s[1]?'<span class="cents">,'+s[1]+'</span>':''; return (neg?"-$":"$")+s[0]+c; }
function monthKey(d){ const x=new Date(d); return x.getFullYear()+"-"+(x.getMonth()+1); }
function nowMonth(){ const x=new Date(); return x.getFullYear()+"-"+(x.getMonth()+1); }
function todayISO(){ return new Date().toISOString().slice(0,10); }
function addMonths(iso,k){ const d=new Date(iso+"T00:00:00"); d.setMonth(d.getMonth()+k); return d.toISOString().slice(0,10); }
function fmtDate(iso){ const d=new Date(iso+"T00:00:00"),t=new Date();t.setHours(0,0,0,0); const df=Math.round((t-d)/86400000); if(df===0)return "Hoy"; if(df===1)return "Ayer"; return d.toLocaleDateString("es-AR",{day:"numeric",month:"short"}); }
function monthLabel(y,m){ return new Date(y,m,1).toLocaleDateString("es-AR",{month:"short"}).replace(".",""); }
function esc(s){ return (s||"").replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c])); }
function parseAmt(v){ if(v===0)return 0; if(!v)return 0; let s=String(v).trim().replace(/[^\d.,]/g,""); if(!s)return 0; if(s.includes(",")) return parseFloat(s.replace(/\./g,"").replace(",","."))||0; if(s.includes(".")){ const p=s.split("."); const g=p.slice(1).every(x=>x.length===3); if(p.length>2||(p.length===2&&g)) return parseFloat(s.replace(/\./g,""))||0; return parseFloat(s)||0; } return parseFloat(s)||0; }
function byDate(a,b){ return (a.date<b.date?1:a.date>b.date?-1:(a.id<b.id?1:-1)); }
const sum=(a,k)=>a.reduce((x,t)=>x+(t[k]||0),0);

/* ---------- Categorías ---------- */
const DEF={
  gasto:[{n:"Comida",e:"🍽️",c:"#FF9500"},{n:"Súper",e:"🛒",c:"#34C759"},{n:"Transporte",e:"🚗",c:"#0A6CFF"},{n:"Servicios",e:"💡",c:"#FFC400"},{n:"Alquiler",e:"🏠",c:"#5856D6"},{n:"Ocio",e:"🎬",c:"#FF2D55"},{n:"Salud",e:"⚕️",c:"#E5484D"},{n:"Suscrip.",e:"📱",c:"#AF52DE"},{n:"Compras",e:"🛍️",c:"#00C7BE"},{n:"Educación",e:"📚",c:"#30B0C7"},{n:"Impuestos",e:"🧾",c:"#8E8E93"},{n:"Cripto",e:"🪙",c:"#26A17B"},{n:"Otros",e:"📦",c:"#98989F"}],
  ingreso:[{n:"Sueldo",e:"💼",c:"#34C759"},{n:"Freelance",e:"💻",c:"#0A6CFF"},{n:"Ventas",e:"🏷️",c:"#00C7BE"},{n:"Cripto",e:"🪙",c:"#26A17B"},{n:"Reintegro",e:"↩️",c:"#5856D6"},{n:"Regalo",e:"🎁",c:"#FF2D55"},{n:"Otros",e:"➕",c:"#98989F"}]
};
function catList(type){ return [...DEF[type], ...state.customCats[type]]; }
function catInfo(type,name){ return catList(type).find(c=>c.n===name)||{n:name||"Otros",e:"📦",c:"#98989F"}; }
function tint(hex){ hex=hex||"#98989F"; const r=parseInt(hex.slice(1,3),16),g=parseInt(hex.slice(3,5),16),b=parseInt(hex.slice(5,7),16); return `rgba(${r},${g},${b},0.15)`; }

/* ---------- Cuentas / balances ---------- */
function acc(id){ return state.accounts.find(a=>a.id===id); }
function accCurrency(id){ const a=acc(id); return a?a.currency:"ARS"; }
function accountBalance(id){
  let b=0;
  state.transactions.forEach(t=>{ if(t.accountId===id) b+= t.kind==="ingreso"?t.amount:-t.amount; });
  state.transfers.forEach(tr=>{ if(tr.fromId===id) b-=tr.fromAmount; if(tr.toId===id) b+=tr.toAmount; });
  return round2(b);
}
function usdtTotal(){ return round2(sum(state.accounts.filter(a=>a.currency==="USDT").map(a=>({v:accountBalance(a.id)})),"v")); }
function pesosTotal(){ return round2(sum(state.accounts.filter(a=>a.currency==="ARS").map(a=>({v:accountBalance(a.id)})),"v")); }
function getRate(){ const d=state.settings.dollar; return d.manual>0?d.manual:(d.venta||d.compra||0); }
function patrimonioPesos(){ return round2(pesosTotal()+usdtTotal()*getRate()); }

/* ---------- P2P / conversiones ---------- */
function conversions(){ return state.transfers.filter(t=>accCurrency(t.fromId)==="USDT"&&accCurrency(t.toId)==="ARS"); }
function purchases(){ return state.transfers.filter(t=>accCurrency(t.fromId)==="ARS"&&accCurrency(t.toId)==="USDT"); }
function p2pTotal(){ return sum(conversions(),"toAmount"); }
function boughtTotal(){ return sum(purchases(),"fromAmount"); }

/* ---------- Rango / filtros ---------- */
function inRange(iso){
  const d=new Date(iso+"T00:00:00"), now=new Date();
  if(txRange==="todo") return true;
  if(txRange==="mes") return d.getFullYear()===now.getFullYear()&&d.getMonth()===now.getMonth();
  if(txRange==="prev"){ const p=new Date(now.getFullYear(),now.getMonth()-1,1); return d.getFullYear()===p.getFullYear()&&d.getMonth()===p.getMonth(); }
  if(txRange==="anio") return d.getFullYear()===now.getFullYear();
  return true;
}

/* ---------- Iconos ---------- */
const IC_WALLET='<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M3 7a2 2 0 0 1 2-2h13a1 1 0 0 1 1 1v2"/><path d="M3 7v10a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-6a2 2 0 0 0-2-2H4"/><circle cx="16" cy="13" r="1.3"/></svg>';
const IC_REPEAT='<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M17 2l4 4-4 4M3 11V9a4 4 0 0 1 4-4h14M7 22l-4-4 4-4M21 13v2a4 4 0 0 1-4 4H3"/></svg>';
const IC_PEOPLE='<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="9" cy="8" r="3.2"/><path d="M3.5 20a5.5 5.5 0 0 1 11 0"/><path d="M17 8h4M19 6v4"/></svg>';
const IC_COIN='<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 7v10M8.5 10h7M9 14h6"/></svg>';
const IC_CHART='<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M4 20V10M10 20V4M16 20v-7M22 20H2"/></svg>';
function empty(icon,title,text){ return `<div class="empty"><div class="e-ico">${icon}</div><h3>${title}</h3><p>${text}</p></div>`; }

/* ---------- Filas ---------- */
function txRow(t){
  const ci=catInfo(t.kind,t.category), cur=accCurrency(t.accountId), a=acc(t.accountId);
  const sign=t.kind==="ingreso"?"+":"-", cls=t.kind==="ingreso"?"in":"";
  const fijo=t.expenseType==="fijo"?'<span class="tag fijo">Fijo</span> ':"";
  return `<div class="row" onclick="editTx('${t.id}')"><div class="ico" style="background:${tint(ci.c)}">${ci.e}</div>
    <div class="mid"><div class="title">${esc(t.note||ci.n)}</div><div class="meta">${fijo}${esc(ci.n)}${a?' · '+esc(a.name):''} · ${fmtDate(t.date)}</div></div>
    <div class="amt ${cls}">${sign}${fmtC(t.amount,cur)}</div>
    <svg class="chevron" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="m9 6 6 6-6 6"/></svg></div>`;
}
function transferRow(tr){
  const fa=acc(tr.fromId), ta=acc(tr.toId), conv=accCurrency(tr.fromId)!==accCurrency(tr.toId);
  return `<div class="row" onclick="editTransfer('${tr.id}')"><div class="ico" style="background:${tint('#26A17B')}; color:var(--tether)"><svg viewBox="0 0 24 24" width="19" height="19" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 2l4 4-4 4M21 6H7M7 22l-4-4 4-4M3 18h14"/></svg></div>
    <div class="mid"><div class="title">${conv?"Conversión":"Transferencia"}</div><div class="meta">${fa?esc(fa.name):"?"} → ${ta?esc(ta.name):"?"}${conv?" · cotiz. "+fmt(tr.rate):""} · ${fmtDate(tr.date)}</div></div>
    <div class="amt">${fmtC(tr.toAmount,accCurrency(tr.toId))}<div class="amt2">-${fmtC(tr.fromAmount,accCurrency(tr.fromId))}</div></div></div>`;
}
function fixedRow(f){
  const ci=catInfo("gasto",f.category), paid=isDoneThisMonth("fixed",f.id), cur=accCurrency(f.accountId);
  return `<div class="row"><div class="ico" style="background:${tint(ci.c)}">${ci.e}</div>
    <div class="mid" onclick="editFixed('${f.id}')"><div class="title">${esc(f.name)}</div><div class="meta">${esc(ci.n)}${f.dueDay?' · vence '+f.dueDay:''} · ${fmtC(f.amount,cur)}</div></div>
    <div class="paid-toggle ${paid?'on':''}" onclick="toggleDone('fixed','${f.id}')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg></div></div>`;
}
function recurRow(f){
  const ci=catInfo("ingreso",f.category), done=isDoneThisMonth("recur",f.id), cur=accCurrency(f.accountId);
  return `<div class="row"><div class="ico" style="background:${tint(ci.c)}">${ci.e}</div>
    <div class="mid" onclick="editRecur('${f.id}')"><div class="title">${esc(f.name)}</div><div class="meta">${esc(ci.n)}${f.dueDay?' · día '+f.dueDay:''} · ${fmtC(f.amount,cur)}</div></div>
    <div class="paid-toggle ${done?'on':''}" onclick="toggleDone('recur','${f.id}')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg></div></div>`;
}
function debtRow(d){
  const ini=(d.person||"?").trim().slice(0,1).toUpperCase(), col=d.direction==="meDeben"?"var(--green)":"var(--red)", sign=d.direction==="meDeben"?"+":"-";
  return `<div class="row ${d.settled?'settled':''}"><div class="ico" style="background:${d.direction==='meDeben'?tint('#1EA672'):tint('#E5484D')}; font-weight:700; font-size:16px; color:${col}">${esc(ini)}</div>
    <div class="mid" onclick="editDebt('${d.id}')"><div class="title">${esc(d.person)}</div><div class="meta">${d.note?esc(d.note)+' · ':''}${fmtDate(d.date)}${d.settled?' · saldada':''}</div></div>
    <div class="amt" style="color:${d.settled?'var(--text-3)':col}">${sign}${fmtC(d.amount,d.currency||"ARS")}</div>
    <div class="paid-toggle ${d.settled?'on':''}" onclick="toggleDebt('${d.id}')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg></div></div>`;
}

/* ---------- Recurrentes: hecho este mes ---------- */
function isDoneThisMonth(kind,id){ const m=nowMonth(); const key=kind==="fixed"?"fixedId":"recurId"; return state.transactions.some(t=>t[key]===id&&monthKey(t.date)===m); }
async function toggleDone(kind,id){
  const list=kind==="fixed"?state.fixed:state.recur, f=list.find(x=>x.id===id); if(!f) return; const m=nowMonth(); const key=kind==="fixed"?"fixedId":"recurId";
  if(isDoneThisMonth(kind,id)){ state.transactions=state.transactions.filter(t=>!(t[key]===id&&monthKey(t.date)===m)); }
  else{ let d=todayISO(); const now=new Date(); if(f.dueDay) d=new Date(now.getFullYear(),now.getMonth(),Math.min(f.dueDay,28)).toISOString().slice(0,10);
    const tx={id:uid(),kind:kind==="fixed"?"gasto":"ingreso",amount:f.amount,accountId:f.accountId,category:f.category,expenseType:kind==="fixed"?"fijo":null,note:f.name,date:d}; tx[key]=id; state.transactions.push(tx); }
  await saveState(); render();
}

/* ---------- Charts (SVG puro) ---------- */
function catChartHTML(){
  const m=nowMonth();
  const gastos=state.transactions.filter(t=>t.kind==="gasto"&&accCurrency(t.accountId)==="ARS"&&monthKey(t.date)===m);
  if(!gastos.length) return '<p style="color:var(--text-2); font-size:14px; margin:4px 0">Sin gastos en pesos este mes.</p>';
  const by={}; gastos.forEach(t=>{ by[t.category]=(by[t.category]||0)+t.amount; });
  const entries=Object.entries(by).sort((a,b)=>b[1]-a[1]).slice(0,6); const max=entries[0][1];
  return entries.map(([cat,v])=>{ const ci=catInfo("gasto",cat); const w=Math.max(4,Math.round(v/max*100));
    return `<div class="bar-row"><div class="bl" style="background:${tint(ci.c)}">${ci.e}</div><div class="bmid"><div class="bt"><span>${esc(ci.n)}</span><span class="bv">${fmt(v)}</span></div><div class="bar-track"><div class="bar-fill" style="width:${w}%; background:${ci.c}"></div></div></div></div>`;
  }).join("");
}
function monthChartHTML(){
  const now=new Date(), months=[];
  for(let i=5;i>=0;i--){ const d=new Date(now.getFullYear(),now.getMonth()-i,1); months.push({y:d.getFullYear(),m:d.getMonth()}); }
  const data=months.map(mm=>{ const k=mm.y+"-"+(mm.m+1);
    const ing=sum(state.transactions.filter(t=>t.kind==="ingreso"&&accCurrency(t.accountId)==="ARS"&&monthKey(t.date)===k),"amount");
    const gas=sum(state.transactions.filter(t=>t.kind==="gasto"&&accCurrency(t.accountId)==="ARS"&&monthKey(t.date)===k),"amount");
    return {label:monthLabel(mm.y,mm.m),ing,gas}; });
  const max=Math.max(1,...data.map(d=>Math.max(d.ing,d.gas)));
  const W=100/6;
  let bars="";
  data.forEach((d,i)=>{ const x=i*W; const hi=d.ing/max*70, hg=d.gas/max*70;
    bars+=`<rect x="${x+W*0.18}" y="${78-hi}" width="${W*0.28}" height="${Math.max(0.5,hi)}" rx="1.5" fill="var(--green)"/>`;
    bars+=`<rect x="${x+W*0.52}" y="${78-hg}" width="${W*0.28}" height="${Math.max(0.5,hg)}" rx="1.5" fill="var(--red)"/>`;
    bars+=`<text x="${x+W*0.5}" y="90" font-size="4.4" text-anchor="middle" fill="var(--text-3)" font-weight="600">${d.label}</text>`;
  });
  return `<svg viewBox="0 0 100 94" style="width:100%; height:170px; overflow:visible">${bars}</svg>
  <div style="display:flex; gap:16px; justify-content:center; font-size:13px; color:var(--text-2); font-weight:600; margin-top:4px"><span><span class="dot g" style="display:inline-block; margin-right:5px"></span>Ingresos</span><span><span class="dot r" style="display:inline-block; margin-right:5px"></span>Gastos</span></div>`;
}
function budgetListHTML(){
  const cats=Object.keys(state.budgets); if(!cats.length) return empty(IC_CHART,"Sin presupuestos","Poné un tope mensual por categoría y seguí cuánto llevás gastado.");
  const m=nowMonth();
  return `<div class="list">`+cats.map(cat=>{ const ci=catInfo("gasto",cat); const bud=state.budgets[cat];
    const spent=sum(state.transactions.filter(t=>t.kind==="gasto"&&accCurrency(t.accountId)==="ARS"&&t.category===cat&&monthKey(t.date)===m),"amount");
    const pct=Math.min(100,Math.round(spent/bud*100)); const over=spent>bud;
    return `<div class="row" style="display:block; padding:14px 16px" onclick="openBudgetSheet('${esc(cat)}')"><div class="bar-row ${over?'prog-over':''}" style="margin-bottom:0"><div class="bl" style="background:${tint(ci.c)}">${ci.e}</div><div class="bmid"><div class="bt"><span>${esc(ci.n)}</span><span class="bv">${fmt(spent)} / ${fmt(bud)}</span></div><div class="bar-track"><div class="bar-fill" style="width:${Math.max(3,pct)}%; background:${over?'var(--red)':ci.c}"></div></div></div></div></div>`;
  }).join("")+`</div>`;
}

/* ---------- Render ---------- */
function render(){
  if(!state) return;
  // hero
  document.getElementById("heroBalance").innerHTML=fmtHero(patrimonioPesos());
  document.getElementById("heroUsdt").textContent=fmtUsd(usdtTotal());
  document.getElementById("heroPesos").textContent=fmt(pesosTotal());
  const d=state.settings.dollar, rate=getRate();
  const dot=document.getElementById("rateDot"), rp=document.getElementById("ratePill");
  const stale=isStale(d.updated);
  dot.className="live"+(stale?" stale":"");
  rp.innerHTML= rate? `Dólar ${d.type} <b>${fmt(rate)}</b>` : "Tocá para poner el dólar";
  // cuentas
  document.getElementById("acctScroll").innerHTML=state.accounts.map(a=>{ const b=accountBalance(a.id); const val=a.currency==="USDT"&&rate?`≈ ${fmt(b*rate)}`:(a.currency==="USDT"?"":""); 
    return `<div class="acct-card" onclick="openAccountSheet('${a.id}')"><div class="ah"><span class="e">${a.emoji||"💳"}</span>${esc(a.name)}</div><div class="ab" style="color:${a.currency==='USDT'?'var(--tether)':'var(--text)'}">${fmtC(b,a.currency)}</div><div class="ap">${val||("&nbsp;")}</div></div>`;
  }).join("")+`<div class="acct-card add" onclick="openAccountSheet()">+</div>`;
  // due alerts
  document.getElementById("dueAlerts").innerHTML=dueAlertsHTML();
  // recientes (todos los movimientos + transfers mezclados)
  const feed=allMovements().slice(0,6);
  document.getElementById("recentList").innerHTML=feed.length?`<div class="list">${feed.map(renderFeed).join("")}</div>`:empty(IC_WALLET,"Sin movimientos","Tocá + para registrar el primero.");
  // movimientos
  renderMovList();
  // analisis
  document.getElementById("anIn").textContent=fmt(sum(state.transactions.filter(t=>t.kind==="ingreso"&&accCurrency(t.accountId)==="ARS"&&monthKey(t.date)===nowMonth()),"amount"));
  document.getElementById("anOut").textContent=fmt(sum(state.transactions.filter(t=>t.kind==="gasto"&&accCurrency(t.accountId)==="ARS"&&monthKey(t.date)===nowMonth()),"amount"));
  document.getElementById("catChart").innerHTML=catChartHTML();
  document.getElementById("monthChart").innerHTML=monthChartHTML();
  document.getElementById("budgetList").innerHTML=budgetListHTML();
  // usdt
  const ut=usdtTotal();
  document.getElementById("usdtBalance").textContent=fmtUsd(ut);
  document.getElementById("usdtValue").textContent=rate?`≈ ${fmt(ut*rate)} · dólar ${d.type} ${fmt(rate)}`:"Cargá el dólar para ver el valor en pesos";
  document.getElementById("p2pTotal").textContent=fmt(p2pTotal());
  document.getElementById("boughtTotal").textContent=fmt(boughtTotal());
  const byW={}; conversions().forEach(c=>{ const ta=acc(c.toId); const w=ta?ta.name:"?"; byW[w]=(byW[w]||0)+c.toAmount; });
  const we=Object.entries(byW).sort((a,b)=>b[1]-a[1]);
  document.getElementById("walletBreak").innerHTML=we.length?`<div class="group-label" style="margin-top:2px"><span>Cobrado por billetera</span></div><div class="wallet-pills">${we.map(([w,v])=>`<span class="pill">${esc(w)} <b>${fmt(v)}</b></span>`).join("")}</div>`:"";
  const conv=[...state.transfers].sort(byDate);
  document.getElementById("convList").innerHTML=conv.length?`<div class="list">${conv.map(transferRow).join("")}</div>`:empty(IC_COIN,"Sin conversiones","Convertí USDT a pesos (P2P) o comprá USDT.");
  // fijos
  document.getElementById("fixedTotal").textContent=fmt(sum(state.fixed.filter(f=>accCurrency(f.accountId)==="ARS"),"amount"));
  const fp=state.fixed.filter(f=>isDoneThisMonth("fixed",f.id)).length;
  document.getElementById("fixedPaidLabel").textContent=state.fixed.length?`${fp}/${state.fixed.length} pagados`:"";
  document.getElementById("fixedList").innerHTML=state.fixed.length?`<div class="list">${state.fixed.map(fixedRow).join("")}</div>`:empty(IC_REPEAT,"Sin gastos fijos","Alquiler, servicios, suscripciones…");
  document.getElementById("recurTotal").textContent=fmt(sum(state.recur.filter(f=>accCurrency(f.accountId)==="ARS"),"amount"));
  const rp2=state.recur.filter(f=>isDoneThisMonth("recur",f.id)).length;
  document.getElementById("recurPaidLabel").textContent=state.recur.length?`${rp2}/${state.recur.length} cobrados`:"";
  document.getElementById("recurList").innerHTML=state.recur.length?`<div class="list">${state.recur.map(recurRow).join("")}</div>`:empty(IC_REPEAT,"Sin recurrentes","Sueldo, cobros mensuales…");
  // deudas
  const dval=d=>(d.currency==="USDT"?d.amount*getRate():d.amount);
  document.getElementById("debtOwedTotal").textContent=fmt(state.debts.filter(x=>x.direction==="meDeben"&&!x.settled).reduce((a,d)=>a+dval(d),0));
  document.getElementById("debtOweTotal").textContent=fmt(state.debts.filter(x=>x.direction==="debo"&&!x.settled).reduce((a,d)=>a+dval(d),0));
  const owed=state.debts.filter(x=>x.direction==="meDeben").sort(debtSort), owe=state.debts.filter(x=>x.direction==="debo").sort(debtSort);
  let dh=""; if(!state.debts.length) dh=empty(IC_PEOPLE,"Sin deudas","Anotá quién te debe o a quién le debés."); else{ if(owed.length) dh+=`<div class="group-label"><span>Te deben</span></div><div class="list">${owed.map(debtRow).join("")}</div>`; if(owe.length) dh+=`<div class="group-label"><span>Debés</span></div><div class="list">${owe.map(debtRow).join("")}</div>`; }
  document.getElementById("debtList").innerHTML=dh;
  // cuentas (sub)
  document.getElementById("accountList").innerHTML=`<div class="list">`+state.accounts.map(a=>`<div class="row" onclick="openAccountSheet('${a.id}')"><div class="ico" style="background:${tint(a.color)}">${a.emoji||"💳"}</div><div class="mid"><div class="title">${esc(a.name)}</div><div class="meta">${a.currency}</div></div><div class="amt" style="color:${a.currency==='USDT'?'var(--tether)':'var(--text)'}">${fmtC(accountBalance(a.id),a.currency)}</div></div>`).join("")+`</div>`;
  // categorias
  document.getElementById("catListGasto").innerHTML=catManageHTML("gasto");
  document.getElementById("catListIngreso").innerHTML=catManageHTML("ingreso");
  // backup info
  const cnt=state.transactions.length+state.transfers.length;
  document.getElementById("backupInfo").textContent=`${cnt} movimientos · ${state.accounts.length} cuentas · ${state.debts.length} deudas`;
  // install
  document.getElementById("installWrap").innerHTML = installEvent?`<button class="btn-primary" onclick="doInstall()">Instalar como app</button>`:"";
  renderThemeBtn();
}
function debtSort(a,b){ return (a.settled?1:0)-(b.settled?1:0)||(a.date<b.date?1:-1); }
function catManageHTML(type){ const custom=state.customCats[type];
  const rows=[...DEF[type].map(c=>({...c,def:true})),...custom.map(c=>({...c,def:false}))];
  return `<div class="list">`+rows.map(c=>`<div class="row"><div class="ico" style="background:${tint(c.c)}">${c.e}</div><div class="mid"><div class="title">${esc(c.n)}</div><div class="meta">${c.def?"Predeterminada":"Personalizada"}</div></div>${c.def?"":`<button class="paid-toggle" style="border-color:var(--red); color:var(--red)" onclick="delCat('${type}','${esc(c.n)}')"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M18 6 6 18M6 6l12 12"/></svg></button>`}</div>`).join("")+`</div>`;
}

/* ---------- Feed combinado ---------- */
function allMovements(){ return [...state.transactions.map(t=>({kind:"tx",date:t.date,id:t.id,obj:t})),...state.transfers.map(t=>({kind:"tr",date:t.date,id:t.id,obj:t}))].sort(byDate); }
function renderFeed(x){ return x.kind==="tx"?txRow(x.obj):transferRow(x.obj); }
function renderMovList(){
  const q=(document.getElementById("txSearch").value||"").toLowerCase().trim();
  let items=allMovements().filter(x=>inRange(x.date));
  if(txFilter==="ingreso") items=items.filter(x=>x.kind==="tx"&&x.obj.kind==="ingreso");
  else if(txFilter==="gasto") items=items.filter(x=>x.kind==="tx"&&x.obj.kind==="gasto");
  else if(txFilter==="fijo") items=items.filter(x=>x.kind==="tx"&&x.obj.expenseType==="fijo");
  if(q) items=items.filter(x=>{ if(x.kind!=="tx") return "conversion transferencia".includes(q); const t=x.obj; const ci=catInfo(t.kind,t.category); return (t.note||"").toLowerCase().includes(q)||ci.n.toLowerCase().includes(q); });
  const el=document.getElementById("txList");
  if(!items.length){ el.innerHTML=empty(IC_WALLET,"Nada por acá","No hay movimientos con estos filtros."); return; }
  // agrupar por mes
  const g={}; items.forEach(x=>{ const dd=new Date(x.date+"T00:00:00"); const k=dd.toLocaleDateString("es-AR",{month:"long",year:"numeric"}); (g[k]=g[k]||[]).push(x); });
  el.innerHTML=Object.entries(g).map(([label,its])=>`<div class="group-label"><span>${label.replace(/^\w/,c=>c.toUpperCase())}</span></div><div class="list">${its.map(renderFeed).join("")}</div>`).join("");
}
function dueAlertsHTML(){
  const now=new Date(), day=now.getDate();
  const due=state.fixed.filter(f=>!isDoneThisMonth("fixed",f.id)&&f.dueDay).map(f=>({f,over:f.dueDay<day,soon:f.dueDay>=day&&f.dueDay-day<=5}));
  const rel=due.filter(x=>x.over||x.soon).sort((a,b)=>a.f.dueDay-b.f.dueDay);
  if(!rel.length) return "";
  return `<div class="section-head"><h2>Próximos vencimientos</h2></div><div class="list">`+rel.slice(0,4).map(({f,over})=>{ const ci=catInfo("gasto",f.category);
    return `<div class="row" onclick="switchTab('mas');setTimeout(()=>openSub('fijos'),10)"><div class="ico" style="background:${tint(ci.c)}">${ci.e}</div><div class="mid"><div class="title">${esc(f.name)}</div><div class="meta" style="color:${over?'var(--red)':'var(--amber)'}">${over?'Vencido':'Vence'} el ${f.dueDay}</div></div><div class="amt">${fmtC(f.amount,accCurrency(f.accountId))}</div></div>`;
  }).join("")+`</div>`;
}

/* ---------- Nav ---------- */
function showScreen(id,activeTab){ document.querySelectorAll(".view").forEach(v=>v.classList.remove("active")); const el=document.getElementById(id); if(el) el.classList.add("active"); document.querySelectorAll(".tab").forEach(t=>t.classList.toggle("on",t.dataset.tab===activeTab)); window.scrollTo(0,0); }
function switchTab(tab){ showScreen("view-"+tab,tab); }
function openSub(name){ showScreen("view-"+name,"mas"); }
function setTxFilter(f){ txFilter=f; document.querySelectorAll("#txFilter button").forEach(b=>b.classList.toggle("on",b.dataset.f===f)); renderMovList(); }
function setRange(r){ txRange=r; document.querySelectorAll("#rangeChips .chip").forEach(b=>b.classList.toggle("on",b.dataset.r===r)); renderMovList(); }

/* ---------- Sheet base ---------- */
const scrim=document.getElementById("scrim"), sheetEl=document.getElementById("sheet"), sheetContent=document.getElementById("sheetContent");
function setSheet(html){ sheetContent.innerHTML=html; }
function openSheet(html){ setSheet(html); scrim.classList.add("show"); requestAnimationFrame(()=>sheetEl.classList.add("show")); document.body.style.overflow="hidden"; }
function closeSheet(){ sheetEl.classList.remove("show"); scrim.classList.remove("show"); document.body.style.overflow=""; }
function acctChips(cur,curId,handler,filter){ const list=state.accounts.filter(a=>!filter||a.currency===filter); return `<div class="chips">${list.map(a=>`<button class="chip ${a.id===curId?'on':''}" data-acc="${a.id}" onclick="${handler}('${a.id}')">${a.emoji||"💳"} ${esc(a.name)}</button>`).join("")}</div>`; }

/* ---------- Movimiento ---------- */
let draft=null;
function defaultAccount(cur){ const a=state.accounts.find(x=>x.currency===(cur||"ARS")); return a?a.id:(state.accounts[0]&&state.accounts[0].id); }
function buildTxSheet(){
  const isIn=draft.kind==="ingreso", cur=accCurrency(draft.accountId);
  const cats=catList(draft.kind).map(c=>`<div class="cat ${draft.category===c.n?'sel':''}" data-cat="${c.n}" onclick="pickCat('${c.n}')"><div class="c-ico" style="background:${tint(c.c)}">${c.e}</div><span>${c.n}</span></div>`).join("")
    +`<div class="cat add" onclick="openCatSheet('${draft.kind}',true)"><div class="c-ico">+</div><span>Nueva</span></div>`;
  const expSeg=!isIn?`<div class="fieldwrap-label">Tipo de gasto</div><div class="seg" id="expSeg"><button class="${draft.expenseType==='variable'?'on':''}" data-exp="variable" onclick="setExp('variable')">Variable</button><button class="${draft.expenseType==='fijo'?'on':''}" data-exp="fijo" onclick="setExp('fijo')">Fijo</button></div>`:"";
  const cuotas=!isIn&&!draft.id?`<div class="field"><div class="f-row"><label>Cuotas</label><input type="number" min="1" max="60" value="${draft.cuotas||1}" oninput="draft.cuotas=this.value"></div></div>`:"";
  return `<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>${draft.id?'Editar':(isIn?'Nuevo ingreso':'Nuevo gasto')}</h3><button class="save" id="txSave" onclick="saveTx()">Guardar</button></div>
  <div class="sheet-body">
    <div class="seg"><button class="${isIn?'':'on'}" onclick="setTxKind('gasto')">Gasto</button><button class="${isIn?'on':''}" onclick="setTxKind('ingreso')">Ingreso</button></div>
    <div class="amount-field ${isIn?'income':'expense'}"><span class="cur" id="curSym">${cur==="USDT"?"US$":"$"}</span><input id="amtInput" inputmode="decimal" placeholder="0" value="${draft.amount}" oninput="draft.amount=this.value;updateTxSave()"></div>
    <div class="fieldwrap-label">Cuenta</div>${acctChips(cur,draft.accountId,"pickAccount")}
    <div class="fieldwrap-label">Categoría</div><div class="cat-grid" id="catGrid">${cats}</div>
    ${expSeg}${cuotas}
    <div class="field"><div class="f-row"><label>Detalle</label><input placeholder="Opcional" value="${esc(draft.note)}" oninput="draft.note=this.value"></div><div class="f-row"><label>Fecha</label><input type="date" value="${draft.date}" onchange="draft.date=this.value"></div></div>
    ${draft.id?'<button class="btn-danger" onclick="deleteTx()">Eliminar movimiento</button>':''}
  </div>`;
}
function openTxSheet(forceKind,editing){ draft=editing?{...editing}:{id:null,kind:forceKind||"gasto",amount:"",accountId:defaultAccount("ARS"),category:"",expenseType:"variable",note:"",date:todayISO(),cuotas:1}; openSheet(buildTxSheet()); updateTxSave(); if(!draft.id) setTimeout(()=>{const a=document.getElementById("amtInput"); if(a)a.focus();},320); }
function setTxKind(k){ draft.kind=k; draft.expenseType=k==="gasto"?(draft.expenseType||"variable"):null; draft.category=""; setSheet(buildTxSheet()); updateTxSave(); }
function setExp(e){ draft.expenseType=e; document.querySelectorAll("#expSeg button").forEach(b=>b.classList.toggle("on",b.dataset.exp===e)); }
function pickCat(n){ draft.category=n; document.querySelectorAll("#catGrid .cat").forEach(el=>el.classList.toggle("sel",el.dataset.cat===n)); updateTxSave(); }
function pickAccount(id){ draft.accountId=id; document.querySelectorAll(".chips [data-acc]").forEach(el=>el.classList.toggle("on",el.dataset.acc===id)); const s=document.getElementById("curSym"); if(s) s.textContent=accCurrency(id)==="USDT"?"US$":"$"; }
function updateTxSave(){ const b=document.getElementById("txSave"); if(b) b.disabled=!(parseAmt(draft.amount)>0&&draft.category&&draft.accountId); }
async function saveTx(){
  const amount=parseAmt(draft.amount); if(!(amount>0)||!draft.category||!draft.accountId) return;
  if(draft.id){ const i=state.transactions.findIndex(t=>t.id===draft.id); if(i>=0) state.transactions[i]={...state.transactions[i],kind:draft.kind,amount,accountId:draft.accountId,category:draft.category,expenseType:draft.kind==="gasto"?draft.expenseType:null,note:(draft.note||"").trim(),date:draft.date}; }
  else{ const n=Math.max(1,Math.min(60,parseInt(draft.cuotas)||1));
    if(n>1&&draft.kind==="gasto"){ const per=round2(amount/n); const g=uid(); for(let i=0;i<n;i++){ state.transactions.push({id:uid(),kind:"gasto",amount:per,accountId:draft.accountId,category:draft.category,expenseType:draft.expenseType,note:((draft.note||catInfo("gasto",draft.category).n))+` (${i+1}/${n})`,date:addMonths(draft.date,i),group:g}); } }
    else state.transactions.push({id:uid(),kind:draft.kind,amount,accountId:draft.accountId,category:draft.category,expenseType:draft.kind==="gasto"?draft.expenseType:null,note:(draft.note||"").trim(),date:draft.date});
  }
  await saveState(); render(); closeSheet();
}
function editTx(id){ const t=state.transactions.find(x=>x.id===id); if(t) openTxSheet(null,t); }
async function deleteTx(){ if(!draft.id) return; state.transactions=state.transactions.filter(t=>t.id!==draft.id); await saveState(); render(); closeSheet(); }

/* ---------- Transferencia / Conversión ---------- */
let tdraft=null;
function buildTransferSheet(){
  const fromCur=accCurrency(tdraft.fromId), toCur=accCurrency(tdraft.toId), conv=fromCur!==toCur;
  return `<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>${tdraft.id?'Editar':(conv?'Conversión':'Transferir')}</h3><button class="save" onclick="saveTransfer()">Guardar</button></div>
  <div class="sheet-body">
    <div class="fieldwrap-label">Desde</div>${acctChips(null,tdraft.fromId,"pickFrom")}
    <div class="fieldwrap-label">Hacia</div>${acctChips(null,tdraft.toId,"pickTo")}
    <div class="amount-field tether"><span class="cur">${fromCur==="USDT"?"US$":"$"}</span><input id="tAmt" inputmode="decimal" placeholder="0" value="${tdraft.fromAmount}" oninput="tdraft.fromAmount=this.value;calcT()"></div>
    <div class="calc-line" id="tCalc"></div>
    ${conv?`<div class="field"><div class="f-row"><label>Cotización</label><input id="tRate" inputmode="decimal" placeholder="Precio x USDT en $" value="${tdraft.rate||''}" oninput="tdraft.rate=this.value;calcT()"></div></div>`:""}
    <div class="field"><div class="f-row"><label>Fecha</label><input type="date" value="${tdraft.date}" onchange="tdraft.date=this.value"></div><div class="f-row"><label>Nota</label><input placeholder="Opcional" value="${esc(tdraft.note)}" oninput="tdraft.note=this.value"></div></div>
    ${tdraft.id?'<button class="btn-danger" onclick="deleteTransfer()">Eliminar</button>':''}
  </div>`;
}
function openTransferSheet(mode,editing){
  if(editing){ tdraft={...editing}; }
  else{ const usdt=state.accounts.find(a=>a.currency==="USDT"), ars=state.accounts.find(a=>a.currency==="ARS");
    tdraft={id:null, fromId:(mode==="conv"&&usdt?usdt.id:(usdt?usdt.id:(state.accounts[0]&&state.accounts[0].id))), toId:(ars?ars.id:(state.accounts[1]&&state.accounts[1].id)), fromAmount:"", rate:getRate()||"", note:"", date:todayISO()}; }
  openSheet(buildTransferSheet()); calcT(); if(!tdraft.id) setTimeout(()=>{const a=document.getElementById("tAmt"); if(a)a.focus();},320);
}
function pickFrom(id){ tdraft.fromId=id; setSheet(buildTransferSheet()); calcT(); }
function pickTo(id){ tdraft.toId=id; setSheet(buildTransferSheet()); calcT(); }
function calcT(){ const el=document.getElementById("tCalc"); if(!el) return; const conv=accCurrency(tdraft.fromId)!==accCurrency(tdraft.toId); const amt=parseAmt(tdraft.fromAmount);
  if(conv){ const r=parseAmt(tdraft.rate); if(amt>0&&r>0){ const to=accCurrency(tdraft.toId)==="ARS"?amt*r:amt/r; el.textContent="Equivale a "+fmtC(round2(to),accCurrency(tdraft.toId)); } else el.textContent="Ingresá monto y cotización"; }
  else el.textContent= amt>0? "Movés "+fmtC(amt,accCurrency(tdraft.fromId)) : "Monto a transferir";
}
async function saveTransfer(){
  if(tdraft.fromId===tdraft.toId){ alert("Elegí dos cuentas distintas."); return; }
  const amt=parseAmt(tdraft.fromAmount); if(!(amt>0)){ alert("Poné un monto."); return; }
  const conv=accCurrency(tdraft.fromId)!==accCurrency(tdraft.toId); let toAmount=amt, rate=0;
  if(conv){ rate=parseAmt(tdraft.rate); if(!(rate>0)){ alert("Poné la cotización."); return; } toAmount=round2(accCurrency(tdraft.toId)==="ARS"?amt*rate:amt/rate); }
  const data={fromId:tdraft.fromId,toId:tdraft.toId,fromAmount:amt,toAmount,rate,note:(tdraft.note||"").trim(),date:tdraft.date};
  if(tdraft.id){ const i=state.transfers.findIndex(x=>x.id===tdraft.id); if(i>=0) state.transfers[i]={...state.transfers[i],...data}; }
  else state.transfers.push({id:uid(),...data});
  await saveState(); render(); closeSheet();
}
function editTransfer(id){ const t=state.transfers.find(x=>x.id===id); if(t) openTransferSheet(null,t); }
async function deleteTransfer(){ if(!tdraft.id) return; state.transfers=state.transfers.filter(x=>x.id!==tdraft.id); await saveState(); render(); closeSheet(); }

/* ---------- Fijos / Recurrentes ---------- */
let fdraft=null, fkind="fixed";
function buildFRSheet(){
  const isFixed=fkind==="fixed", type=isFixed?"gasto":"ingreso";
  const cats=catList(type).map(c=>`<div class="cat ${fdraft.category===c.n?'sel':''}" data-cat="${c.n}" onclick="pickFCat('${c.n}')"><div class="c-ico" style="background:${tint(c.c)}">${c.e}</div><span>${c.n}</span></div>`).join("");
  return `<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>${fdraft.id?'Editar':(isFixed?'Nuevo gasto fijo':'Nuevo recurrente')}</h3><button class="save" onclick="saveFR()">Guardar</button></div>
  <div class="sheet-body">
    <div class="amount-field ${isFixed?'expense':'income'}"><span class="cur">${accCurrency(fdraft.accountId)==="USDT"?"US$":"$"}</span><input id="fAmt" inputmode="decimal" placeholder="0" value="${fdraft.amount}" oninput="fdraft.amount=this.value"></div>
    <div class="field"><div class="f-row"><label>Nombre</label><input id="fName" placeholder="${isFixed?'Alquiler, Netflix…':'Sueldo, cobro…'}" value="${esc(fdraft.name)}" oninput="fdraft.name=this.value"></div><div class="f-row"><label>Día</label><input type="number" min="1" max="31" placeholder="Día del mes" value="${fdraft.dueDay}" oninput="fdraft.dueDay=this.value"></div></div>
    <div class="fieldwrap-label">Cuenta</div>${acctChips(null,fdraft.accountId,"pickFAcc")}
    <div class="fieldwrap-label">Categoría</div><div class="cat-grid">${cats}</div>
    ${fdraft.id?'<button class="btn-danger" onclick="deleteFR()">Eliminar</button>':''}
  </div>`;
}
function openFixedSheet(editing){ fkind="fixed"; fdraft=editing?{...editing}:{id:null,name:"",amount:"",accountId:defaultAccount("ARS"),category:"Servicios",dueDay:""}; openSheet(buildFRSheet()); if(!fdraft.id) setTimeout(()=>{const e=document.getElementById("fName"); if(e)e.focus();},320); }
function openRecurSheet(editing){ fkind="recur"; fdraft=editing?{...editing}:{id:null,name:"",amount:"",accountId:defaultAccount("ARS"),category:"Sueldo",dueDay:""}; openSheet(buildFRSheet()); if(!fdraft.id) setTimeout(()=>{const e=document.getElementById("fName"); if(e)e.focus();},320); }
function pickFCat(n){ fdraft.category=n; document.querySelectorAll(".cat-grid .cat").forEach(el=>el.classList.toggle("sel",el.dataset.cat===n)); }
function pickFAcc(id){ fdraft.accountId=id; document.querySelectorAll(".chips [data-acc]").forEach(el=>el.classList.toggle("on",el.dataset.acc===id)); }
async function saveFR(){
  const amount=parseAmt(fdraft.amount); if(!(amount>0)||!(fdraft.name||"").trim()){ alert("Poné nombre y monto."); return; }
  const day=fdraft.dueDay?Math.min(31,Math.max(1,parseInt(fdraft.dueDay))):"";
  const data={name:fdraft.name.trim(),amount,accountId:fdraft.accountId,category:fdraft.category,dueDay:day};
  const list=fkind==="fixed"?state.fixed:state.recur;
  if(fdraft.id){ const i=list.findIndex(f=>f.id===fdraft.id); if(i>=0) list[i]={...list[i],...data}; }
  else list.push({id:uid(),...data});
  await saveState(); render(); closeSheet();
}
function editFixed(id){ fkind="fixed"; const f=state.fixed.find(x=>x.id===id); if(f) openFixedSheet(f); }
function editRecur(id){ fkind="recur"; const f=state.recur.find(x=>x.id===id); if(f) openRecurSheet(f); }
async function deleteFR(){ if(!fdraft.id) return; const key=fkind==="fixed"?"fixedId":"recurId"; state.transactions=state.transactions.filter(t=>t[key]!==fdraft.id); if(fkind==="fixed") state.fixed=state.fixed.filter(f=>f.id!==fdraft.id); else state.recur=state.recur.filter(f=>f.id!==fdraft.id); await saveState(); render(); closeSheet(); }

/* ---------- Deudas ---------- */
let ddraft=null;
function buildDebtSheet(){ const md=ddraft.direction==="meDeben";
  return `<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>${ddraft.id?'Editar deuda':'Nueva deuda'}</h3><button class="save" onclick="saveDebt()">Guardar</button></div>
  <div class="sheet-body">
    <div class="seg" id="dirSeg"><button class="${md?'on':''}" data-dir="meDeben" onclick="setDir('meDeben')">Me deben</button><button class="${md?'':'on'}" data-dir="debo" onclick="setDir('debo')">Yo debo</button></div>
    <div class="seg" id="curSeg"><button class="${ddraft.currency==='ARS'?'on':''}" data-cur="ARS" onclick="setDCur('ARS')">Pesos</button><button class="${ddraft.currency==='USDT'?'on':''}" data-cur="USDT" onclick="setDCur('USDT')">USDT</button></div>
    <div class="amount-field ${md?'income':'expense'}" id="dWrap"><span class="cur" id="dCur">${ddraft.currency==='USDT'?'US$':'$'}</span><input id="dAmt" inputmode="decimal" placeholder="0" value="${ddraft.amount}" oninput="ddraft.amount=this.value"></div>
    <div class="field"><div class="f-row"><label>Persona</label><input id="dPerson" placeholder="Nombre" value="${esc(ddraft.person)}" oninput="ddraft.person=this.value"></div><div class="f-row"><label>Motivo</label><input placeholder="Opcional" value="${esc(ddraft.note)}" oninput="ddraft.note=this.value"></div><div class="f-row"><label>Fecha</label><input type="date" value="${ddraft.date}" onchange="ddraft.date=this.value"></div></div>
    ${ddraft.id?'<button class="btn-danger" onclick="deleteDebt()">Eliminar deuda</button>':''}
  </div>`;
}
function openDebtSheet(editing){ ddraft=editing?{...editing}:{id:null,direction:"meDeben",currency:"ARS",person:"",amount:"",note:"",date:todayISO(),settled:false}; openSheet(buildDebtSheet()); if(!ddraft.id) setTimeout(()=>{const e=document.getElementById("dPerson"); if(e)e.focus();},320); }
function setDir(d){ ddraft.direction=d; document.querySelectorAll("#dirSeg button").forEach(b=>b.classList.toggle("on",b.dataset.dir===d)); const w=document.getElementById("dWrap"); if(w){ w.classList.toggle("income",d==="meDeben"); w.classList.toggle("expense",d==="debo"); } }
function setDCur(c){ ddraft.currency=c; document.querySelectorAll("#curSeg button").forEach(b=>b.classList.toggle("on",b.dataset.cur===c)); const s=document.getElementById("dCur"); if(s) s.textContent=c==="USDT"?"US$":"$"; }
async function saveDebt(){ const amount=parseAmt(ddraft.amount); if(!(amount>0)||!(ddraft.person||"").trim()){ alert("Poné nombre y monto."); return; }
  const data={direction:ddraft.direction,currency:ddraft.currency,person:ddraft.person.trim(),amount,note:(ddraft.note||"").trim(),date:ddraft.date};
  if(ddraft.id){ const i=state.debts.findIndex(x=>x.id===ddraft.id); if(i>=0) state.debts[i]={...state.debts[i],...data}; }
  else state.debts.push({id:uid(),...data,settled:false});
  await saveState(); render(); closeSheet();
}
function editDebt(id){ const d=state.debts.find(x=>x.id===id); if(d) openDebtSheet(d); }
async function toggleDebt(id){ const d=state.debts.find(x=>x.id===id); if(d){ d.settled=!d.settled; await saveState(); render(); } }
async function deleteDebt(){ if(!ddraft.id) return; state.debts=state.debts.filter(x=>x.id!==ddraft.id); await saveState(); render(); closeSheet(); }

/* ---------- Cuentas ---------- */
let adraft=null;
const EMOJIS=["💵","🪙","💳","🏦","💰","📱","🐧","🍋","🔵","⭐"];
function buildAccountSheet(){
  const emo=EMOJIS.map(e=>`<button class="chip ${adraft.emoji===e?'on':''}" onclick="adraft.emoji='${e}';document.querySelectorAll('#emoRow .chip').forEach((b,i)=>b.classList.toggle('on',b.textContent==='${e}'))" style="font-size:18px">${e}</button>`).join("");
  return `<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>${adraft.id?'Editar cuenta':'Nueva cuenta'}</h3><button class="save" onclick="saveAccount()">Guardar</button></div>
  <div class="sheet-body">
    <div class="field"><div class="f-row"><label>Nombre</label><input id="aName" placeholder="Lemon, Banco, Efectivo…" value="${esc(adraft.name)}" oninput="adraft.name=this.value"></div></div>
    <div class="fieldwrap-label">Moneda</div><div class="seg" id="aCurSeg"><button class="${adraft.currency==='ARS'?'on':''}" data-c="ARS" onclick="setACur('ARS')">Pesos</button><button class="${adraft.currency==='USDT'?'on':''}" data-c="USDT" onclick="setACur('USDT')">USDT</button></div>
    <div class="fieldwrap-label">Ícono</div><div class="chips" id="emoRow">${emo}</div>
    ${adraft.id?`<div class="fieldwrap-label">Saldo actual: ${fmtC(accountBalance(adraft.id),adraft.currency)}</div><button class="btn-danger" onclick="deleteAccount()">Eliminar cuenta</button>`:''}
  </div>`;
}
function openAccountSheet(id){ const a=id?acc(id):null; adraft=a?{...a}:{id:null,name:"",currency:"ARS",emoji:"💳",color:"#0A6CFF"}; openSheet(buildAccountSheet()); if(!adraft.id) setTimeout(()=>{const e=document.getElementById("aName"); if(e)e.focus();},320); }
function setACur(c){ adraft.currency=c; document.querySelectorAll("#aCurSeg button").forEach(b=>b.classList.toggle("on",b.dataset.c===c)); }
async function saveAccount(){ if(!(adraft.name||"").trim()){ alert("Poné un nombre."); return; }
  if(adraft.id){ const i=state.accounts.findIndex(a=>a.id===adraft.id); if(i>=0) state.accounts[i]={...state.accounts[i],name:adraft.name.trim(),currency:adraft.currency,emoji:adraft.emoji}; }
  else state.accounts.push({id:uid(),name:adraft.name.trim(),currency:adraft.currency,emoji:adraft.emoji,color:adraft.color});
  await saveState(); render(); closeSheet();
}
async function deleteAccount(){ if(!adraft.id) return;
  const used=state.transactions.some(t=>t.accountId===adraft.id)||state.transfers.some(t=>t.fromId===adraft.id||t.toId===adraft.id);
  if(used&&!confirm("Esta cuenta tiene movimientos. Si la borrás, esos movimientos quedan sin cuenta. ¿Seguir?")) return;
  state.accounts=state.accounts.filter(a=>a.id!==adraft.id); await saveState(); render(); closeSheet();
}

/* ---------- Categorías ---------- */
let cdraft=null;
const CAT_EMOJIS=["🍽️","🛒","🚗","💡","🏠","🎬","⚕️","📱","🛍️","📚","🧾","🪙","✈️","🎁","💪","🐶","☕","🎮","💅","🎓","🏋️","🎸","➕"];
const CAT_COLORS=["#FF9500","#34C759","#0A6CFF","#FFC400","#5856D6","#FF2D55","#E5484D","#AF52DE","#00C7BE","#30B0C7","#26A17B","#8E8E93"];
function openCatSheet(type,fromTx){ cdraft={type,name:"",emoji:"🏷️",color:"#0A6CFF",fromTx:!!fromTx};
  const emo=CAT_EMOJIS.map(e=>`<button class="chip ${cdraft.emoji===e?'on':''}" onclick="cdraft.emoji='${e}';document.querySelectorAll('#cEmo .chip').forEach(b=>b.classList.toggle('on',b.textContent==='${e}'))" style="font-size:18px">${e}</button>`).join("");
  const col=CAT_COLORS.map(c=>`<button class="chip ${cdraft.color===c?'on':''}" onclick="cdraft.color='${c}';document.querySelectorAll('#cCol .chip').forEach(b=>b.classList.toggle('on',b.dataset.c==='${c}'))" data-c="${c}" style="background:${c}; width:34px; height:34px; padding:0; border-radius:50%"></button>`).join("");
  openSheet(`<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>Nueva categoría</h3><button class="save" onclick="saveCat()">Guardar</button></div>
  <div class="sheet-body"><div class="field"><div class="f-row"><label>Nombre</label><input id="cName" placeholder="Nombre" oninput="cdraft.name=this.value"></div></div>
  <div class="fieldwrap-label">Ícono</div><div class="chips" id="cEmo">${emo}</div>
  <div class="fieldwrap-label">Color</div><div class="chips" id="cCol">${col}</div></div>`);
  setTimeout(()=>{const e=document.getElementById("cName"); if(e)e.focus();},320);
}
async function saveCat(){ const n=(cdraft.name||"").trim(); if(!n){ alert("Poné un nombre."); return; }
  if(catList(cdraft.type).some(c=>c.n.toLowerCase()===n.toLowerCase())){ alert("Ya existe una categoría con ese nombre."); return; }
  state.customCats[cdraft.type].push({n,e:cdraft.emoji,c:cdraft.color}); await saveState();
  const wasFromTx=cdraft.fromTx, type=cdraft.type; closeSheet(); render();
  if(wasFromTx&&draft){ draft.category=n; openSheet(buildTxSheet()); updateTxSave(); }
}
async function delCat(type,name){ if(!confirm("¿Borrar la categoría \""+name+"\"? Los movimientos que la usan se quedan con el nombre.")) return; state.customCats[type]=state.customCats[type].filter(c=>c.n!==name); await saveState(); render(); }

/* ---------- Presupuestos ---------- */
let bdraft=null;
function openBudgetSheet(cat){ bdraft={cat:cat||"", amount: cat&&state.budgets[cat]?String(state.budgets[cat]):""};
  const cats=DEF.gasto.concat(state.customCats.gasto).map(c=>`<div class="cat ${bdraft.cat===c.n?'sel':''}" data-cat="${c.n}" onclick="pickBCat('${c.n}')"><div class="c-ico" style="background:${tint(c.c)}">${c.e}</div><span>${c.n}</span></div>`).join("");
  openSheet(`<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Cancelar</button><h3>Presupuesto mensual</h3><button class="save" onclick="saveBudget()">Guardar</button></div>
  <div class="sheet-body"><div class="amount-field expense"><span class="cur">$</span><input id="bAmt" inputmode="decimal" placeholder="0" value="${bdraft.amount}" oninput="bdraft.amount=this.value"></div>
  <div class="fieldwrap-label">Categoría</div><div class="cat-grid" id="bGrid">${cats}</div>
  ${cat?'<button class="btn-danger" onclick="delBudget()">Quitar presupuesto</button>':''}</div>`);
}
function pickBCat(n){ bdraft.cat=n; document.querySelectorAll("#bGrid .cat").forEach(el=>el.classList.toggle("sel",el.dataset.cat===n)); }
async function saveBudget(){ const a=parseAmt(bdraft.amount); if(!(a>0)||!bdraft.cat){ alert("Elegí categoría y monto."); return; } state.budgets[bdraft.cat]=a; await saveState(); render(); closeSheet(); }
async function delBudget(){ if(bdraft.cat) delete state.budgets[bdraft.cat]; await saveState(); render(); closeSheet(); }

/* ---------- Dólar ---------- */
function isStale(iso){ if(!iso) return true; return (Date.now()-new Date(iso).getTime())>1000*60*60*12; }
function openDollarSheet(){ const d=state.settings.dollar;
  openSheet(`<div class="sheet-head"><button class="cancel" onclick="closeSheet()">Listo</button><h3>Cotización del dólar</h3><span style="width:44px"></span></div>
  <div class="sheet-body">
    <div class="fieldwrap-label">Tipo de dólar</div>
    <div class="seg" id="dTypeSeg">${["blue","cripto","bolsa","oficial"].map(t=>`<button class="${d.type===t?'on':''}" data-t="${t}" onclick="setDollarType('${t}')">${t==="bolsa"?"MEP":t.charAt(0).toUpperCase()+t.slice(1)}</button>`).join("")}</div>
    <button class="btn-primary" id="dFetchBtn" onclick="refreshDollar()">Actualizar automático</button>
    <div id="dFetchInfo" style="text-align:center; color:var(--text-2); font-size:14px; margin-top:12px">${d.venta?("Última: compra "+fmt(d.compra)+" · venta "+fmt(d.venta)+(d.updated?" · "+fmtDate(d.updated.slice(0,10)):"")):"Todavía no se actualizó"}</div>
    <div class="fieldwrap-label">O poné el valor a mano</div>
    <div class="field"><div class="f-row"><label>Manual</label><input id="dManual" inputmode="decimal" placeholder="Precio x dólar" value="${d.manual||''}" oninput="setManual(this.value)"></div></div>
    <p style="color:var(--text-3); font-size:13px; text-align:center">Se usa para valuar tus USDT en pesos.</p>
  </div>`);
}
function setDollarType(t){ state.settings.dollar.type=t; document.querySelectorAll("#dTypeSeg button").forEach(b=>b.classList.toggle("on",b.dataset.t===t)); saveState(); }
async function setManual(v){ state.settings.dollar.manual=parseAmt(v); await saveState(); render(); }
async function refreshDollar(){ const info=document.getElementById("dFetchInfo"), btn=document.getElementById("dFetchBtn");
  if(btn) btn.textContent="Actualizando…";
  const ok=await fetchDollar();
  if(btn) btn.textContent="Actualizar automático";
  const d=state.settings.dollar;
  if(info) info.textContent= ok? ("Actualizado: compra "+fmt(d.compra)+" · venta "+fmt(d.venta)) : "No se pudo conectar. Poné el valor a mano.";
  render();
}
async function fetchDollar(){ try{ const t=state.settings.dollar.type||"blue"; const r=await fetch("https://dolarapi.com/v1/dolares/"+t,{cache:"no-store"}); if(!r.ok) throw 0; const j=await r.json(); state.settings.dollar.compra=j.compra||0; state.settings.dollar.venta=j.venta||0; state.settings.dollar.updated=new Date().toISOString(); await saveState(); return true; }catch(e){ return false; } }

/* ---------- Backup ---------- */
function download(name,content,type){ try{ const blob=new Blob([content],{type}); const url=URL.createObjectURL(blob); const a=document.createElement("a"); a.href=url; a.download=name; document.body.appendChild(a); a.click(); setTimeout(()=>{document.body.removeChild(a); URL.revokeObjectURL(url);},100); }catch(e){ alert("No se pudo descargar en este entorno."); } }
function exportJSON(){ download("finanzas-"+todayISO()+".json", JSON.stringify(state,null,2), "application/json"); }
function exportCSV(){
  const rows=[["fecha","tipo","monto","moneda","cuenta","categoria","detalle"]];
  state.transactions.forEach(t=>{ const a=acc(t.accountId); rows.push([t.date,t.kind,t.amount,accCurrency(t.accountId),a?a.name:"",t.category,(t.note||"").replace(/"/g,"'")]); });
  state.transfers.forEach(t=>{ const f=acc(t.fromId),to=acc(t.toId); rows.push([t.date,"transferencia",t.fromAmount,accCurrency(t.fromId),(f?f.name:"")+"→"+(to?to.name:""),"",""]); });
  const csv=rows.map(r=>r.map(c=>`"${c}"`).join(",")).join("\n");
  download("movimientos-"+todayISO()+".csv","\ufeff"+csv,"text/csv");
}
function importJSON(input){ const file=input.files&&input.files[0]; if(!file) return; const rd=new FileReader();
  rd.onload=async()=>{ try{ const data=JSON.parse(rd.result); if(!data||typeof data!=="object") throw 0; if(!confirm("Esto reemplaza todos los datos actuales por los del archivo. ¿Seguir?")) return; state=normalize(data); await saveState(); render(); switchTab("inicio"); alert("Datos restaurados."); }catch(e){ alert("El archivo no es un respaldo válido."); } input.value=""; };
  rd.readAsText(file);
}
async function wipeAll(){ if(!confirm("¿Borrar TODOS los datos? Esto no se puede deshacer.")) return; if(!confirm("Última confirmación: se borra todo.")) return; state=normalize({}); state.accounts=[{id:uid(),name:"USDT",currency:"USDT",emoji:"🪙",color:"#26A17B"},{id:uid(),name:"Efectivo",currency:"ARS",emoji:"💵",color:"#34C759"}]; await saveState(); render(); switchTab("inicio"); }

/* ---------- PWA ---------- */
function doInstall(){ if(installEvent){ installEvent.prompt(); installEvent=null; render(); } }

/* ---------- Tema ---------- */
function prefersDark(){ try{ return !!(window.matchMedia&&window.matchMedia("(prefers-color-scheme: dark)").matches); }catch(e){ return false; } }
function isDark(){ return document.documentElement.getAttribute("data-theme")==="dark"||(state.settings.theme==="auto"&&prefersDark()); }
function applyTheme(){ const t=state.settings.theme,h=document.documentElement; if(t==="auto") h.removeAttribute("data-theme"); else h.setAttribute("data-theme",t); renderThemeBtn(); }
function renderThemeBtn(){ const b=document.getElementById("themeBtn"); if(!b) return; b.innerHTML=isDark()?'<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="4.2"/><path d="M12 2v2.5M12 19.5V22M2 12h2.5M19.5 12H22M4.9 4.9l1.8 1.8M17.3 17.3l1.8 1.8M19.1 4.9l-1.8 1.8M6.7 17.3l-1.8 1.8"/></svg>':'<svg viewBox="0 0 24 24" fill="currentColor" stroke="none"><path d="M21 12.8A9 9 0 1 1 11.2 3a7 7 0 0 0 9.8 9.8z"/></svg>'; }
async function toggleTheme(){ state.settings.theme=isDark()?"light":"dark"; applyTheme(); await saveState(); }

/* ---------- Init ---------- */
(async function init(){
  await loadState();
  applyTheme();
  document.getElementById("themeBtn").addEventListener("click", toggleTheme);
  try{ const mq=window.matchMedia&&window.matchMedia("(prefers-color-scheme: dark)"); if(mq&&mq.addEventListener) mq.addEventListener("change",()=>{ if(state.settings.theme==="auto") renderThemeBtn(); }); }catch(e){}
  window.addEventListener("beforeinstallprompt",e=>{ e.preventDefault(); installEvent=e; try{render();}catch(_){} });
  render();
  if(isStale(state.settings.dollar.updated)) fetchDollar().then(ok=>{ if(ok) render(); });
})();
</script>
</body>
</html>
