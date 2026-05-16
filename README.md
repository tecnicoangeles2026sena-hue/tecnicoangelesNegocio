

<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Técnico Ángeles – Administración</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root{--bg:#0b0f1a;--surface:#111827;--surface2:#1a2236;--border:#1e2d45;--accent:#00c9ff;--green:#00ff9d;--red:#ff4d6d;--yellow:#ffbe0b;--purple:#b97cff;--orange:#ff9f1c;--text:#e2e8f0;--muted:#6b7fa3;}
  *{margin:0;padding:0;box-sizing:border-box;}
  body{background:var(--bg);color:var(--text);font-family:'IBM Plex Sans',sans-serif;min-height:100vh;}

  header{background:var(--surface);border-bottom:1px solid var(--border);padding:0 2rem;display:flex;align-items:center;justify-content:space-between;height:64px;position:sticky;top:0;z-index:100;box-shadow:0 2px 20px rgba(0,201,255,.08);}
  .logo{font-family:'Rajdhani',sans-serif;font-size:1.45rem;font-weight:700;letter-spacing:.05em;color:var(--accent);}
  .logo span{color:var(--text);}
  .hpills{display:flex;gap:.7rem;flex-wrap:wrap;}
  .pill{display:flex;align-items:center;gap:.4rem;background:var(--surface2);border:1px solid var(--border);border-radius:6px;padding:.25rem .7rem;font-family:'IBM Plex Mono',monospace;font-size:.72rem;}
  .dot{width:8px;height:8px;border-radius:50%;animation:pu 2s infinite;}
  .dot.g{background:var(--green);box-shadow:0 0 6px var(--green);}
  .dot.r{background:var(--red);box-shadow:0 0 6px var(--red);}
  .dot.a{background:var(--accent);box-shadow:0 0 6px var(--accent);}
  .dot.p{background:var(--purple);box-shadow:0 0 6px var(--purple);}
  .dot.o{background:var(--orange);box-shadow:0 0 6px var(--orange);}
  @keyframes pu{0%,100%{opacity:1}50%{opacity:.4}}

  nav{background:var(--surface);border-bottom:1px solid var(--border);display:flex;overflow-x:auto;padding:0 1.5rem;}
  .ntab{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:.88rem;letter-spacing:.07em;text-transform:uppercase;padding:.78rem 1.1rem;cursor:pointer;border-bottom:3px solid transparent;color:var(--muted);white-space:nowrap;transition:all .2s;user-select:none;}
  .ntab:hover{color:var(--text);}
  .ntab.active{color:var(--accent);border-bottom-color:var(--accent);}

  main{padding:1.5rem 2rem;}
  .panel{display:none;} .panel.active{display:block;}

  .toolbar{display:flex;align-items:center;gap:.8rem;margin-bottom:1.1rem;flex-wrap:wrap;}
  .sbox{display:flex;align-items:center;background:var(--surface2);border:1px solid var(--border);border-radius:6px;padding:0 .8rem;gap:.5rem;flex:1;min-width:180px;}
  .sbox input{background:none;border:none;outline:none;color:var(--text);font-family:'IBM Plex Sans',sans-serif;font-size:.86rem;padding:.58rem 0;width:100%;}

  .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:1rem;margin-bottom:1.4rem;}
  .card{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:1rem 1.1rem;}
  .card-label{font-family:'IBM Plex Mono',monospace;font-size:.66rem;letter-spacing:.1em;text-transform:uppercase;color:var(--muted);margin-bottom:.35rem;}
  .card-val{font-family:'Rajdhani',sans-serif;font-size:1.75rem;font-weight:700;line-height:1;}
  .cv-a{color:var(--accent);} .cv-g{color:var(--green);} .cv-r{color:var(--red);} .cv-p{color:var(--purple);} .cv-o{color:var(--orange);}

  .btn{display:inline-flex;align-items:center;gap:.4rem;font-family:'Rajdhani',sans-serif;font-weight:600;font-size:.83rem;letter-spacing:.06em;text-transform:uppercase;padding:.5rem .95rem;border-radius:6px;cursor:pointer;border:none;transition:all .18s;white-space:nowrap;}
  .bn-a{background:var(--accent);color:#0b0f1a;} .bn-a:hover{background:#33d4ff;box-shadow:0 0 12px rgba(0,201,255,.4);}
  .bn-g{background:var(--green);color:#0b0f1a;} .bn-g:hover{background:#33ffb3;}
  .bn-r{background:var(--red);color:#fff;} .bn-r:hover{background:#ff7090;}
  .bn-p{background:var(--purple);color:#0b0f1a;} .bn-p:hover{background:#caa3ff;}
  .bn-o{background:var(--orange);color:#0b0f1a;} .bn-o:hover{background:#ffb74d;}
  .bn-gh{background:var(--surface2);color:var(--text);border:1px solid var(--border);} .bn-gh:hover{border-color:var(--accent);color:var(--accent);}
  .btn.sm{padding:.26rem .6rem;font-size:.73rem;}

  .tw{background:var(--surface);border:1px solid var(--border);border-radius:10px;overflow:hidden;overflow-x:auto;}
  table{width:100%;border-collapse:collapse;min-width:480px;}
  thead tr{background:var(--surface2);}
  th{font-family:'IBM Plex Mono',monospace;font-size:.67rem;font-weight:500;letter-spacing:.1em;text-transform:uppercase;color:var(--muted);padding:.68rem 1rem;text-align:left;border-bottom:1px solid var(--border);white-space:nowrap;}
  td{padding:.63rem 1rem;font-size:.85rem;border-bottom:1px solid rgba(30,45,69,.5);vertical-align:middle;}
  tr:last-child td{border-bottom:none;}
  tbody tr:hover{background:rgba(0,201,255,.04);}
  .acts{display:flex;gap:.35rem;}

  .bx{display:inline-block;padding:.16rem .52rem;border-radius:4px;font-family:'IBM Plex Mono',monospace;font-size:.72rem;font-weight:500;}
  .bx-a{background:rgba(0,201,255,.12);color:var(--accent);}
  .bx-g{background:rgba(0,255,157,.12);color:var(--green);}
  .bx-r{background:rgba(255,77,109,.12);color:var(--red);}
  .bx-p{background:rgba(185,124,255,.12);color:var(--purple);}
  .bx-y{background:rgba(255,190,11,.12);color:var(--yellow);}
  .bx-o{background:rgba(255,159,28,.12);color:var(--orange);}
  .nm{font-family:'IBM Plex Mono',monospace;}
  .nm.g{color:var(--green);} .nm.r{color:var(--red);} .nm.a{color:var(--accent);} .nm.o{color:var(--orange);}

  /* SALDO BAR */
  .sbar{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:.9rem 1.3rem;margin-bottom:1.1rem;display:flex;gap:2rem;flex-wrap:wrap;align-items:center;}
  .sbar-item{display:flex;flex-direction:column;}
  .sbar-lbl{font-family:'IBM Plex Mono',monospace;font-size:.65rem;letter-spacing:.1em;text-transform:uppercase;color:var(--muted);}
  .sbar-val{font-family:'Rajdhani',sans-serif;font-size:1.35rem;font-weight:700;}

  /* CLIENT CARDS */
  .cgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(255px,1fr));gap:1rem;}
  .ccard{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:1.1rem;transition:border-color .2s;}
  .ccard:hover{border-color:var(--purple);}
  .cname{font-family:'Rajdhani',sans-serif;font-size:1.05rem;font-weight:700;color:var(--purple);margin-bottom:.3rem;}
  .cmeta{font-size:.79rem;color:var(--muted);line-height:1.65;}
  .cmeta span{color:var(--text);}
  .cacts{display:flex;gap:.4rem;margin-top:.85rem;}

  /* DEUDA CARDS */
  .dgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1rem;}
  .dcard{background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:1.1rem;transition:border-color .2s;}
  .dcard:hover{border-color:var(--orange);}
  .dcard.pagado{border-color:rgba(0,255,157,.2);}
  .dname{font-family:'Rajdhani',sans-serif;font-size:1.05rem;font-weight:700;color:var(--orange);margin-bottom:.3rem;}
  .dname.pagado{color:var(--green);}
  .dmeta{font-size:.79rem;color:var(--muted);line-height:1.8;}
  .dmeta span{color:var(--text);}
  .dbar-wrap{margin-top:.7rem;background:var(--surface2);border-radius:4px;height:6px;overflow:hidden;}
  .dbar-fill{height:100%;border-radius:4px;background:var(--orange);transition:width .4s;}
  .dbar-fill.full{background:var(--green);}
  .dacts{display:flex;gap:.4rem;margin-top:.85rem;flex-wrap:wrap;}

  /* PAGOS TABLE */
  .pagos-section{margin-top:.85rem;border-top:1px solid var(--border);padding-top:.65rem;}
  .pagos-title{font-family:'IBM Plex Mono',monospace;font-size:.65rem;letter-spacing:.1em;text-transform:uppercase;color:var(--muted);margin-bottom:.4rem;}
  .pago-row{display:flex;align-items:center;justify-content:space-between;font-size:.78rem;padding:.18rem 0;}
  .pago-row span{color:var(--muted);}
  .pago-row strong{color:var(--green);font-family:'IBM Plex Mono',monospace;}

  /* MODAL */
  .overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.72);z-index:1000;align-items:center;justify-content:center;backdrop-filter:blur(4px);}
  .overlay.open{display:flex;}
  .modal{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.8rem;width:100%;max-width:490px;box-shadow:0 20px 60px rgba(0,0,0,.5);animation:su .22s ease;max-height:92vh;overflow-y:auto;}
  @keyframes su{from{transform:translateY(20px);opacity:0}to{transform:translateY(0);opacity:1}}
  .mtitle{font-family:'Rajdhani',sans-serif;font-size:1.12rem;font-weight:700;letter-spacing:.05em;text-transform:uppercase;margin-bottom:1.3rem;}
  .fr{margin-bottom:.85rem;}
  .fr label{display:block;font-size:.7rem;font-family:'IBM Plex Mono',monospace;color:var(--muted);margin-bottom:.28rem;letter-spacing:.08em;text-transform:uppercase;}
  .fr input,.fr select,.fr textarea{width:100%;background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--text);font-family:'IBM Plex Sans',sans-serif;font-size:.87rem;padding:.55rem .78rem;outline:none;transition:border-color .2s;}
  .fr textarea{resize:vertical;min-height:65px;}
  .fr input:focus,.fr select:focus,.fr textarea:focus{border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,201,255,.1);}
  .fr select option{background:var(--surface2);}
  .fg2{display:grid;grid-template-columns:1fr 1fr;gap:.75rem;}
  .mfoot{display:flex;gap:.75rem;justify-content:flex-end;margin-top:1.3rem;}
  .cmsg{color:var(--text);font-size:.88rem;margin-bottom:1.1rem;line-height:1.6;}
  .cmsg strong{color:var(--red);}
  .empty{text-align:center;padding:2.5rem 1rem;color:var(--muted);font-size:.87rem;}

  /* HISTORIAL PAGOS MODAL */
  .hpago-list{max-height:200px;overflow-y:auto;margin-bottom:.8rem;}
  .hpago-item{display:flex;align-items:center;justify-content:space-between;padding:.45rem .7rem;background:var(--surface2);border-radius:6px;margin-bottom:.3rem;font-size:.82rem;}
  .hpago-item:last-child{margin-bottom:0;}
  .hpago-item .hpi-fecha{color:var(--muted);font-family:'IBM Plex Mono',monospace;font-size:.72rem;}
  .hpago-item .hpi-monto{color:var(--green);font-family:'IBM Plex Mono',monospace;font-weight:500;}
  .hpago-item .hpi-del{background:none;border:none;color:var(--red);cursor:pointer;font-size:.8rem;padding:.1rem .3rem;}

  /* TOAST */
  .tc{position:fixed;bottom:1.4rem;right:1.4rem;z-index:9999;display:flex;flex-direction:column;gap:.45rem;}
  .toast{background:var(--surface2);border-left:3px solid var(--accent);border-radius:6px;padding:.62rem .95rem;font-size:.82rem;box-shadow:0 4px 20px rgba(0,0,0,.4);animation:ti .25s ease;min-width:210px;}
  .toast.ok{border-left-color:var(--green);} .toast.err{border-left-color:var(--red);}
  @keyframes ti{from{transform:translateX(40px);opacity:0}to{transform:translateX(0);opacity:1}}

  /* FILTER ROW */
  .filter-row{display:flex;gap:.6rem;align-items:center;flex-wrap:wrap;margin-bottom:.8rem;}
  .filter-row select{background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--text);font-family:'IBM Plex Sans',sans-serif;font-size:.83rem;padding:.45rem .7rem;outline:none;}
  .filter-row select:focus{border-color:var(--accent);}

  /* LOGIN */
  #login-screen{position:fixed;inset:0;background:var(--bg);z-index:9999;display:flex;align-items:center;justify-content:center;}
  #login-screen.hidden{display:none;}
  .login-box{background:var(--surface);border:1px solid var(--border);border-radius:16px;padding:2.8rem 2.4rem;width:100%;max-width:380px;box-shadow:0 24px 70px rgba(0,0,0,.6);text-align:center;}
  .login-logo{font-family:'Rajdhani',sans-serif;font-size:2rem;font-weight:700;letter-spacing:.06em;color:var(--accent);margin-bottom:.2rem;}
  .login-logo span{color:var(--text);}
  .login-sub{font-family:'IBM Plex Mono',monospace;font-size:.72rem;color:var(--muted);letter-spacing:.12em;text-transform:uppercase;margin-bottom:2rem;}
  .login-icon{font-size:3rem;margin-bottom:1.2rem;display:block;}
  .login-fr{margin-bottom:1rem;text-align:left;}
  .login-fr label{display:block;font-size:.68rem;font-family:'IBM Plex Mono',monospace;color:var(--muted);margin-bottom:.3rem;letter-spacing:.1em;text-transform:uppercase;}
  .login-fr input{width:100%;background:var(--surface2);border:1px solid var(--border);border-radius:8px;color:var(--text);font-family:'IBM Plex Sans',sans-serif;font-size:.95rem;padding:.65rem .9rem;outline:none;transition:border-color .2s;}
  .login-fr input:focus{border-color:var(--accent);box-shadow:0 0 0 3px rgba(0,201,255,.12);}
  .login-btn{width:100%;background:var(--accent);color:#0b0f1a;font-family:'Rajdhani',sans-serif;font-weight:700;font-size:1rem;letter-spacing:.1em;text-transform:uppercase;border:none;border-radius:8px;padding:.75rem;cursor:pointer;transition:all .2s;margin-top:.4rem;}
  .login-btn:hover{background:#33d4ff;box-shadow:0 0 18px rgba(0,201,255,.4);}
  .login-err{color:var(--red);font-size:.8rem;font-family:'IBM Plex Mono',monospace;margin-top:.7rem;min-height:1.1rem;}
  .login-attempts{color:var(--muted);font-size:.72rem;font-family:'IBM Plex Mono',monospace;margin-top:.5rem;}
  #app-wrap{display:none;}
  #app-wrap.visible{display:block;}
  .logout-btn{font-family:'Rajdhani',sans-serif;font-weight:600;font-size:.75rem;letter-spacing:.07em;text-transform:uppercase;background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--muted);padding:.25rem .7rem;cursor:pointer;transition:all .2s;}
  .logout-btn:hover{border-color:var(--red);color:var(--red);}

  @media(max-width:660px){
    header{padding:0 1rem;} main{padding:1rem;} nav{padding:0 .5rem;}
    .ntab{padding:.65rem .75rem;font-size:.78rem;}
    th,td{padding:.52rem .6rem;font-size:.79rem;}
    .hpills{gap:.4rem;} .pill{font-size:.66rem;}
    .fg2{grid-template-columns:1fr;}
    .login-box{padding:2rem 1.4rem;margin:1rem;}
  }
</style>
</head>
<body>

<!-- LOGIN SCREEN -->
<div id="login-screen">
  <div class="login-box">
    <span class="login-icon">🔐</span>
    <div class="login-logo">TÉCNICO<span>ÁNGELES</span></div>
    <div class="login-sub">Panel de Administración</div>
    <div class="login-fr">
      <label>Usuario</label>
      <input type="text" id="login-user" placeholder="Administrador" autocomplete="username">
    </div>
    <div class="login-fr">
      <label>Contraseña</label>
      <input type="password" id="login-pass" placeholder="••••••••••" autocomplete="current-password" onkeydown="if(event.key==='Enter')doLogin()">
    </div>
    <button class="login-btn" onclick="doLogin()">Entrar al Sistema</button>
    <div class="login-err" id="login-err"></div>
    <div class="login-attempts" id="login-attempts"></div>
  </div>
</div>

<!-- APP -->
<div id="app-wrap">

<header>
  <div class="logo">TÉCNICO<span>ÁNGELES</span></div>
  <div class="hpills">
    <div class="pill"><div class="dot g"></div><span id="hp-saldo">Saldo $0</span></div>
    <div class="pill"><div class="dot a"></div><span id="hp-prods">0 Productos</span></div>
    <div class="pill"><div class="dot p"></div><span id="hp-clis">0 Clientes</span></div>
    <div class="pill"><div class="dot o"></div><span id="hp-deudas">$0 por cobrar</span></div>
    <button class="logout-btn" onclick="doLogout()">🔒 Cerrar Sesión</button>
  </div>
</header>

<nav>
  <div class="ntab active" data-tab="inventario">📦 Inventario</div>
  <div class="ntab" data-tab="entradas-inv">📥 Entradas</div>
  <div class="ntab" data-tab="salidas-inv">📤 Salidas</div>
  <div class="ntab" data-tab="finanzas">💰 Ingresos &amp; Egresos</div>
  <div class="ntab" data-tab="clientes">👥 Clientes</div>
  <div class="ntab" data-tab="servicios">🔧 Servicios</div>
  <div class="ntab" data-tab="cobros">💳 Cuentas por Cobrar</div>
</nav>

<main>

<!-- INVENTARIO -->
<div class="panel active" id="panel-inventario">
  <div class="cards">
    <div class="card"><div class="card-label">Productos</div><div class="card-val cv-a" id="cc-prod">0</div></div>
    <div class="card"><div class="card-label">Total Entradas</div><div class="card-val cv-g" id="cc-ei">0</div></div>
    <div class="card"><div class="card-label">Total Salidas</div><div class="card-val cv-r" id="cc-si">0</div></div>
    <div class="card"><div class="card-label">Stock Total</div><div class="card-val cv-a" id="cc-st">0</div></div>
  </div>
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-inv" placeholder="Buscar código o artículo…" oninput="renderInv()"></div>
    <button class="btn bn-a" onclick="openMP()">＋ Nuevo Producto</button>
  </div>
  <div class="tw"><table><thead><tr><th>Código</th><th>Artículo</th><th>Entradas</th><th>Salidas</th><th>Stock</th><th>Acciones</th></tr></thead><tbody id="tb-inv"></tbody></table></div>
</div>

<!-- ENTRADAS INV -->
<div class="panel" id="panel-entradas-inv">
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-ei" placeholder="Buscar…" oninput="renderEI()"></div>
    <button class="btn bn-g" onclick="openMEI()">＋ Registrar Entrada</button>
  </div>
  <div class="tw"><table><thead><tr><th>Código</th><th>Artículo</th><th>Fecha</th><th>Cantidad</th><th>Acciones</th></tr></thead><tbody id="tb-ei"></tbody></table></div>
</div>

<!-- SALIDAS INV -->
<div class="panel" id="panel-salidas-inv">
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-si" placeholder="Buscar…" oninput="renderSI()"></div>
    <button class="btn bn-r" onclick="openMSI()">＋ Registrar Salida</button>
  </div>
  <div class="tw"><table><thead><tr><th>Código</th><th>Artículo</th><th>Fecha</th><th>Cantidad</th><th>Acciones</th></tr></thead><tbody id="tb-si"></tbody></table></div>
</div>

<!-- FINANZAS -->
<div class="panel" id="panel-finanzas">
  <div class="sbar">
    <div class="sbar-item"><div class="sbar-lbl">Total Ingresos</div><div class="sbar-val" style="color:var(--green)" id="fin-ing">$0</div></div>
    <div class="sbar-item"><div class="sbar-lbl">Total Egresos</div><div class="sbar-val" style="color:var(--red)" id="fin-egr">$0</div></div>
    <div class="sbar-item"><div class="sbar-lbl">Saldo Actual</div><div class="sbar-val" id="fin-sal">$0</div></div>
  </div>
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-fin" placeholder="Buscar concepto…" oninput="renderFin()"></div>
    <button class="btn bn-g" onclick="openMFin('ingreso')">＋ Ingreso</button>
    <button class="btn bn-r" onclick="openMFin('egreso')">＋ Egreso</button>
  </div>
  <div class="tw"><table><thead><tr><th>Fecha</th><th>Tipo</th><th>Concepto</th><th>Monto</th><th>Saldo Acum.</th><th>Acciones</th></tr></thead><tbody id="tb-fin"></tbody></table></div>
</div>

<!-- CLIENTES -->
<div class="panel" id="panel-clientes">
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-cli" placeholder="Buscar cliente…" oninput="renderCli()"></div>
    <button class="btn bn-p" onclick="openMCli()">＋ Nuevo Cliente</button>
  </div>
  <div class="cgrid" id="grid-cli"></div>
</div>

<!-- SERVICIOS -->
<div class="panel" id="panel-servicios">
  <div class="cards">
    <div class="card"><div class="card-label">Total Servicios</div><div class="card-val cv-a" id="cc-srv">0</div></div>
    <div class="card"><div class="card-label">Facturado</div><div class="card-val cv-g" id="cc-srv-monto">$0</div></div>
    <div class="card"><div class="card-label">Este Mes</div><div class="card-val cv-p" id="cc-srv-mes">0</div></div>
    <div class="card"><div class="card-label">Pendientes</div><div class="card-val cv-o" id="cc-srv-pend">0</div></div>
  </div>
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-srv" placeholder="Buscar servicio o cliente…" oninput="renderSrv()"></div>
    <select id="fil-srv-mes" onchange="renderSrv()" style="background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--text);font-size:.83rem;padding:.45rem .7rem;outline:none;">
      <option value="">Todos los meses</option>
    </select>
    <select id="fil-srv-est" onchange="renderSrv()" style="background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--text);font-size:.83rem;padding:.45rem .7rem;outline:none;">
      <option value="">Todos</option>
      <option value="pendiente">Pendiente</option>
      <option value="entregado">Entregado</option>
      <option value="garantia">En Garantía</option>
    </select>
    <button class="btn bn-a" onclick="openMSrv()">＋ Nuevo Servicio</button>
  </div>
  <div class="tw"><table><thead><tr><th>Fecha</th><th>Cliente</th><th>Equipo / Descripción</th><th>Valor</th><th>Estado</th><th>Acciones</th></tr></thead><tbody id="tb-srv"></tbody></table></div>
</div>

<!-- CUENTAS POR COBRAR -->
<div class="panel" id="panel-cobros">
  <div class="sbar">
    <div class="sbar-item"><div class="sbar-lbl">Total Deuda</div><div class="sbar-val" style="color:var(--orange)" id="cob-total">$0</div></div>
    <div class="sbar-item"><div class="sbar-lbl">Total Pagado</div><div class="sbar-val" style="color:var(--green)" id="cob-pagado">$0</div></div>
    <div class="sbar-item"><div class="sbar-lbl">Saldo Pendiente</div><div class="sbar-val" style="color:var(--red)" id="cob-pendiente">$0</div></div>
    <div class="sbar-item"><div class="sbar-lbl">Clientes con Deuda</div><div class="sbar-val" style="color:var(--accent)" id="cob-count">0</div></div>
  </div>
  <div class="toolbar">
    <div class="sbox"><svg width="15" height="15" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg><input type="text" id="sq-cob" placeholder="Buscar cliente o descripción…" oninput="renderCob()"></div>
    <select id="fil-cob-est" onchange="renderCob()" style="background:var(--surface2);border:1px solid var(--border);border-radius:6px;color:var(--text);font-size:.83rem;padding:.45rem .7rem;outline:none;">
      <option value="">Todos</option>
      <option value="pendiente">Con saldo pendiente</option>
      <option value="pagado">Cancelados</option>
    </select>
    <button class="btn bn-o" onclick="openMCob()">＋ Nueva Deuda</button>
  </div>
  <div class="dgrid" id="grid-cob"></div>
</div>

</main>

<!-- ===== MODALES ===== -->

<!-- PRODUCTO -->
<div class="overlay" id="m-prod">
  <div class="modal">
    <div class="mtitle" id="m-prod-t" style="color:var(--accent)">Nuevo Producto</div>
    <div class="fr"><label>Código</label><input type="text" id="p-id" placeholder="Ej: AN08"></div>
    <div class="fr"><label>Artículo / Descripción</label><input type="text" id="p-art" placeholder="Nombre del producto"></div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-prod')">Cancelar</button><button class="btn bn-a" onclick="saveProd()">Guardar</button></div>
  </div>
</div>

<!-- ENTRADA INV -->
<div class="overlay" id="m-ei">
  <div class="modal">
    <div class="mtitle" style="color:var(--green)">Registrar Entrada</div>
    <div class="fr"><label>Producto</label><select id="ei-cod"></select></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="ei-fecha"></div>
      <div class="fr"><label>Cantidad</label><input type="number" id="ei-cant" min="1" placeholder="0"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-ei')">Cancelar</button><button class="btn bn-g" onclick="saveEI()">Registrar</button></div>
  </div>
</div>

<!-- SALIDA INV -->
<div class="overlay" id="m-si">
  <div class="modal">
    <div class="mtitle" style="color:var(--red)">Registrar Salida</div>
    <div class="fr"><label>Producto</label><select id="si-cod"></select></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="si-fecha"></div>
      <div class="fr"><label>Cantidad</label><input type="number" id="si-cant" min="1" placeholder="0"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-si')">Cancelar</button><button class="btn bn-r" onclick="saveSI()">Registrar</button></div>
  </div>
</div>

<!-- FINANZAS -->
<div class="overlay" id="m-fin">
  <div class="modal">
    <div class="mtitle" id="m-fin-t" style="color:var(--green)">Registrar Ingreso</div>
    <div class="fr"><label>Concepto</label><input type="text" id="fin-c" placeholder="Descripción del movimiento"></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="fin-f"></div>
      <div class="fr"><label>Monto ($)</label><input type="number" id="fin-m" min="1" placeholder="0"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-fin')">Cancelar</button><button class="btn" id="fin-btn" onclick="saveFin()">Guardar</button></div>
  </div>
</div>

<!-- CLIENTE -->
<div class="overlay" id="m-cli">
  <div class="modal">
    <div class="mtitle" id="m-cli-t" style="color:var(--purple)">Nuevo Cliente</div>
    <div class="fr"><label>Nombre completo</label><input type="text" id="cli-n" placeholder="Ej: Juan Pérez"></div>
    <div class="fg2">
      <div class="fr"><label>Teléfono</label><input type="text" id="cli-t" placeholder="311 234 5678"></div>
      <div class="fr"><label>Correo</label><input type="text" id="cli-e" placeholder="correo@email.com"></div>
    </div>
    <div class="fr"><label>Dirección</label><input type="text" id="cli-d" placeholder="Dirección (opcional)"></div>
    <div class="fr"><label>Notas / Equipo / Servicio</label><textarea id="cli-no" placeholder="Ej: PC con falla en fuente de poder…"></textarea></div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-cli')">Cancelar</button><button class="btn bn-p" onclick="saveCli()">Guardar</button></div>
  </div>
</div>

<!-- EDITAR ENTRADA -->
<div class="overlay" id="m-eei">
  <div class="modal">
    <div class="mtitle" style="color:var(--green)">Editar Entrada</div>
    <div class="fr"><label>Producto</label><select id="eei-cod"></select></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="eei-f"></div>
      <div class="fr"><label>Cantidad</label><input type="number" id="eei-c" min="1"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-eei')">Cancelar</button><button class="btn bn-g" onclick="saveEEI()">Guardar</button></div>
  </div>
</div>

<!-- EDITAR SALIDA -->
<div class="overlay" id="m-esi">
  <div class="modal">
    <div class="mtitle" style="color:var(--red)">Editar Salida</div>
    <div class="fr"><label>Producto</label><select id="esi-cod"></select></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="esi-f"></div>
      <div class="fr"><label>Cantidad</label><input type="number" id="esi-c" min="1"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-esi')">Cancelar</button><button class="btn bn-r" onclick="saveESI()">Guardar</button></div>
  </div>
</div>

<!-- EDITAR FINANZA -->
<div class="overlay" id="m-efin">
  <div class="modal">
    <div class="mtitle" id="m-efin-t" style="color:var(--accent)">Editar Movimiento</div>
    <div class="fr"><label>Concepto</label><input type="text" id="efin-c"></div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="efin-f"></div>
      <div class="fr"><label>Monto ($)</label><input type="number" id="efin-m" min="1"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-efin')">Cancelar</button><button class="btn bn-a" onclick="saveEFin()">Guardar</button></div>
  </div>
</div>

<!-- EDITAR CLIENTE -->
<div class="overlay" id="m-ecli">
  <div class="modal">
    <div class="mtitle" style="color:var(--purple)">Editar Cliente</div>
    <div class="fr"><label>Nombre</label><input type="text" id="ecli-n"></div>
    <div class="fg2">
      <div class="fr"><label>Teléfono</label><input type="text" id="ecli-t"></div>
      <div class="fr"><label>Correo</label><input type="text" id="ecli-e"></div>
    </div>
    <div class="fr"><label>Dirección</label><input type="text" id="ecli-d"></div>
    <div class="fr"><label>Notas / Equipo</label><textarea id="ecli-no"></textarea></div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-ecli')">Cancelar</button><button class="btn bn-p" onclick="saveECli()">Guardar</button></div>
  </div>
</div>

<!-- NUEVO SERVICIO -->
<div class="overlay" id="m-srv">
  <div class="modal">
    <div class="mtitle" id="m-srv-t" style="color:var(--accent)">Nuevo Servicio</div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="srv-f"></div>
      <div class="fr"><label>Estado</label>
        <select id="srv-est">
          <option value="pendiente">Pendiente</option>
          <option value="entregado">Entregado</option>
          <option value="garantia">En Garantía</option>
        </select>
      </div>
    </div>
    <div class="fr"><label>Cliente</label><input type="text" id="srv-cli" placeholder="Nombre del cliente"></div>
    <div class="fr"><label>Equipo / Descripción del trabajo</label><textarea id="srv-desc" placeholder="Ej: Laptop HP – cambio de pantalla, instalación Windows 11…"></textarea></div>
    <div class="fg2">
      <div class="fr"><label>Valor cobrado ($)</label><input type="number" id="srv-val" min="0" placeholder="0"></div>
      <div class="fr"><label>Teléfono (opcional)</label><input type="text" id="srv-tel" placeholder="311 234 5678"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-srv')">Cancelar</button><button class="btn bn-a" onclick="saveSrv()">Guardar</button></div>
  </div>
</div>

<!-- EDITAR SERVICIO -->
<div class="overlay" id="m-esrv">
  <div class="modal">
    <div class="mtitle" style="color:var(--accent)">Editar Servicio</div>
    <div class="fg2">
      <div class="fr"><label>Fecha</label><input type="date" id="esrv-f"></div>
      <div class="fr"><label>Estado</label>
        <select id="esrv-est">
          <option value="pendiente">Pendiente</option>
          <option value="entregado">Entregado</option>
          <option value="garantia">En Garantía</option>
        </select>
      </div>
    </div>
    <div class="fr"><label>Cliente</label><input type="text" id="esrv-cli"></div>
    <div class="fr"><label>Equipo / Descripción</label><textarea id="esrv-desc"></textarea></div>
    <div class="fg2">
      <div class="fr"><label>Valor ($)</label><input type="number" id="esrv-val" min="0"></div>
      <div class="fr"><label>Teléfono</label><input type="text" id="esrv-tel"></div>
    </div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-esrv')">Cancelar</button><button class="btn bn-a" onclick="saveESrv()">Guardar</button></div>
  </div>
</div>

<!-- NUEVA DEUDA -->
<div class="overlay" id="m-cob">
  <div class="modal">
    <div class="mtitle" id="m-cob-t" style="color:var(--orange)">Nueva Cuenta por Cobrar</div>
    <div class="fr"><label>Cliente que debe</label><input type="text" id="cob-cli" placeholder="Nombre del cliente"></div>
    <div class="fr"><label>Descripción del servicio / deuda</label><textarea id="cob-desc" placeholder="Ej: Reparación PC, formateo, cambio de pantalla…"></textarea></div>
    <div class="fg2">
      <div class="fr"><label>Monto Total Deuda ($)</label><input type="number" id="cob-total-i" min="1" placeholder="0"></div>
      <div class="fr"><label>Fecha de la deuda</label><input type="date" id="cob-f"></div>
    </div>
    <div class="fr"><label>Teléfono (opcional)</label><input type="text" id="cob-tel" placeholder="311 234 5678"></div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-cob')">Cancelar</button><button class="btn bn-o" onclick="saveCob()">Guardar</button></div>
  </div>
</div>

<!-- REGISTRAR PAGO -->
<div class="overlay" id="m-pago">
  <div class="modal">
    <div class="mtitle" style="color:var(--green)">Registrar Pago</div>
    <p class="cmsg" id="pago-info" style="color:var(--muted)"></p>
    <div class="fg2">
      <div class="fr"><label>Monto que paga ($)</label><input type="number" id="pago-monto" min="1" placeholder="0"></div>
      <div class="fr"><label>Fecha del pago</label><input type="date" id="pago-f"></div>
    </div>
    <div class="fr"><label>Nota (opcional)</label><input type="text" id="pago-nota" placeholder="Ej: Pago cuota mayo, abono…"></div>
    <div class="hpago-list" id="pago-hist"></div>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-pago')">Cancelar</button><button class="btn bn-g" onclick="savePago()">Registrar Pago</button></div>
  </div>
</div>

<!-- CONFIRM -->
<div class="overlay" id="m-conf">
  <div class="modal">
    <div class="mtitle" style="color:var(--red)">Confirmar Eliminación</div>
    <p class="cmsg" id="conf-msg">¿Eliminar este registro?</p>
    <div class="mfoot"><button class="btn bn-gh" onclick="closeM('m-conf')">Cancelar</button><button class="btn bn-r" onclick="doDel()">Eliminar</button></div>
  </div>
</div>

<div class="tc" id="toasts"></div>

<script>
const SK='ta_adm_v2';
function load(){
  const r=localStorage.getItem(SK);
  if(r) return JSON.parse(r);
  // Migrate from v1 if exists
  const old=localStorage.getItem('ta_adm_v1');
  if(old){
    const o=JSON.parse(old);
    return {...o, srvs:[], cobros:[]};
  }
  return {
    prods:[
      {id:'AN01',art:'Cilicona de la gruesa'},
      {id:'AN02',art:'Cilicona de la finita'},
      {id:'AN03',art:'Disco Duro 250GB'},
      {id:'AN04',art:'Fuente de Poder J&R Power Supply P4-750W Ref:PSU002'},
      {id:'AN05',art:'DVD Writer Model Sf-224'},
      {id:'AN06',art:'Ventirador de CPU Model F6015812LY'},
      {id:'AN07',art:'Ventirador Powmax Model CT8025'},
    ],
    ei:[
      {id:1,cod:'AN02',f:'2026-05-08',c:3},
      {id:2,cod:'AN01',f:'2026-05-08',c:4},
      {id:3,cod:'AN03',f:'2026-05-08',c:2},
      {id:4,cod:'AN04',f:'2026-05-08',c:1},
      {id:5,cod:'AN05',f:'2026-05-08',c:2},
      {id:6,cod:'AN06',f:'2026-05-08',c:1},
      {id:7,cod:'AN07',f:'2026-05-08',c:1},
    ],
    si:[],fin:[],clis:[],srvs:[],cobros:[],nid:8
  };
}
let D=load();
const sv=()=>localStorage.setItem(SK,JSON.stringify(D));
const gP=id=>D.prods.find(p=>p.id===id);
const fD=d=>{if(!d)return'—';const[y,m,dd]=d.split('-');return`${dd}/${m}/${y}`;};
const fMes=d=>{if(!d)return'';const[y,m]=d.split('-');const ns=['Ene','Feb','Mar','Abr','May','Jun','Jul','Ago','Sep','Oct','Nov','Dic'];return`${ns[parseInt(m)-1]} ${y}`;};
const today=()=>new Date().toISOString().split('T')[0];
const fM=n=>'$'+Number(n||0).toLocaleString('es-CO');
const esc=s=>String(s||'').replace(/'/g,"\\'").replace(/"/g,'&quot;');

function stk(cod){
  const e=D.ei.filter(x=>x.cod===cod).reduce((a,x)=>a+x.c,0);
  const s=D.si.filter(x=>x.cod===cod).reduce((a,x)=>a+x.c,0);
  return{e,s,st:e-s};
}

// TABS
document.querySelectorAll('.ntab').forEach(t=>{
  t.addEventListener('click',()=>{
    document.querySelectorAll('.ntab').forEach(x=>x.classList.remove('active'));
    document.querySelectorAll('.panel').forEach(x=>x.classList.remove('active'));
    t.classList.add('active');
    document.getElementById('panel-'+t.dataset.tab).classList.add('active');
    renderAll();
  });
});

// TOAST
function toast(msg,type='ok'){
  const c=document.getElementById('toasts'),el=document.createElement('div');
  el.className=`toast ${type}`;el.textContent=msg;c.appendChild(el);
  setTimeout(()=>{el.style.cssText='opacity:0;transform:translateX(40px);transition:all .3s';setTimeout(()=>el.remove(),300);},2700);
}

// MODAL
const openM=id=>document.getElementById(id).classList.add('open');
const closeM=id=>document.getElementById(id).classList.remove('open');
document.querySelectorAll('.overlay').forEach(o=>o.addEventListener('click',e=>{if(e.target===o)o.classList.remove('open');}));
document.addEventListener('keydown',e=>{if(e.key==='Escape')document.querySelectorAll('.overlay.open').forEach(o=>o.classList.remove('open'));});

// SELECT HELPER
const fillSel=(sid,cur='')=>{document.getElementById(sid).innerHTML=D.prods.map(p=>`<option value="${p.id}"${p.id===cur?' selected':''}>${p.id} – ${p.art}</option>`).join('');};

// HEADER
function updH(){
  const sal=D.fin.reduce((a,f)=>a+(f.t==='i'?f.m:-f.m),0);
  document.getElementById('hp-saldo').textContent='Saldo '+fM(sal);
  document.getElementById('hp-prods').textContent=D.prods.length+' Productos';
  document.getElementById('hp-clis').textContent=D.clis.length+' Clientes';
  // total pendiente por cobrar
  const pend=D.cobros.reduce((a,c)=>{
    const pagado=c.pagos.reduce((x,p)=>x+p.m,0);
    return a+Math.max(0,c.total-pagado);
  },0);
  document.getElementById('hp-deudas').textContent=fM(pend)+' por cobrar';
}

// ===== INVENTARIO =====
function renderInv(){
  const q=document.getElementById('sq-inv').value.toLowerCase();
  const rows=D.prods.filter(p=>!q||p.id.toLowerCase().includes(q)||p.art.toLowerCase().includes(q));
  const tE=D.ei.reduce((a,x)=>a+x.c,0),tS=D.si.reduce((a,x)=>a+x.c,0);
  document.getElementById('cc-prod').textContent=D.prods.length;
  document.getElementById('cc-ei').textContent=tE;
  document.getElementById('cc-si').textContent=tS;
  document.getElementById('cc-st').textContent=tE-tS;
  const tb=document.getElementById('tb-inv');
  if(!rows.length){tb.innerHTML=`<tr><td colspan="6"><div class="empty">No se encontraron productos</div></td></tr>`;return;}
  tb.innerHTML=rows.map(p=>{
    const s=stk(p.id);
    return`<tr>
      <td><span class="bx bx-a">${p.id}</span></td>
      <td>${p.art}</td>
      <td class="nm g">+${s.e}</td><td class="nm r">-${s.s}</td>
      <td>${s.st>0?`<span class="bx bx-g">${s.st}</span>`:`<span class="bx bx-r">${s.st}</span>`}</td>
      <td><div class="acts">
        <button class="btn bn-gh sm" onclick="openEP('${p.id}')">✏️ Editar</button>
        <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('p','${p.id}','${esc(p.art)}')">🗑️</button>
      </div></td>
    </tr>`;
  }).join('');
}
let epId=null;
function openMP(){epId=null;document.getElementById('m-prod-t').textContent='Nuevo Producto';document.getElementById('p-id').value='';document.getElementById('p-art').value='';document.getElementById('p-id').disabled=false;openM('m-prod');}
function openEP(id){const p=gP(id);if(!p)return;epId=id;document.getElementById('m-prod-t').textContent='Editar Producto';document.getElementById('p-id').value=p.id;document.getElementById('p-id').disabled=true;document.getElementById('p-art').value=p.art;openM('m-prod');}
function saveProd(){
  const id=document.getElementById('p-id').value.trim().toUpperCase(),art=document.getElementById('p-art').value.trim();
  if(!id||!art){toast('Completa todos los campos','err');return;}
  if(!epId){if(D.prods.find(p=>p.id===id)){toast('Ese código ya existe','err');return;}D.prods.push({id,art});toast('Producto agregado ✓');}
  else{gP(epId).art=art;toast('Actualizado ✓');}
  sv();renderAll();closeM('m-prod');
}

// ===== ENTRADAS INV =====
function renderEI(){
  const q=document.getElementById('sq-ei').value.toLowerCase();
  const rows=D.ei.filter(e=>{const p=gP(e.cod);return!q||e.cod.toLowerCase().includes(q)||(p&&p.art.toLowerCase().includes(q));});
  const tb=document.getElementById('tb-ei');
  if(!rows.length){tb.innerHTML=`<tr><td colspan="5"><div class="empty">No hay entradas registradas</div></td></tr>`;return;}
  tb.innerHTML=rows.map(e=>{const p=gP(e.cod);return`<tr>
    <td><span class="bx bx-a">${e.cod}</span></td><td>${p?p.art:'—'}</td><td>${fD(e.f)}</td><td class="nm g">+${e.c}</td>
    <td><div class="acts">
      <button class="btn bn-gh sm" onclick="openEEI(${e.id})">✏️</button>
      <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('ei',${e.id},'entrada #${e.id}')">🗑️</button>
    </div></td>
  </tr>`;}).join('');
}
let eiId=null;
function openMEI(){fillSel('ei-cod');document.getElementById('ei-fecha').value=today();document.getElementById('ei-cant').value='';openM('m-ei');}
function saveEI(){const cod=document.getElementById('ei-cod').value,f=document.getElementById('ei-fecha').value,c=parseInt(document.getElementById('ei-cant').value);if(!f||!c||c<1){toast('Completa todos los campos','err');return;}D.ei.push({id:D.nid++,cod,f,c});sv();renderAll();closeM('m-ei');toast('Entrada registrada ✓');}
function openEEI(id){const e=D.ei.find(x=>x.id===id);if(!e)return;eiId=id;fillSel('eei-cod',e.cod);document.getElementById('eei-f').value=e.f;document.getElementById('eei-c').value=e.c;openM('m-eei');}
function saveEEI(){const e=D.ei.find(x=>x.id===eiId);if(!e)return;e.cod=document.getElementById('eei-cod').value;e.f=document.getElementById('eei-f').value;e.c=parseInt(document.getElementById('eei-c').value);sv();renderAll();closeM('m-eei');toast('Actualizado ✓');}

// ===== SALIDAS INV =====
function renderSI(){
  const q=document.getElementById('sq-si').value.toLowerCase();
  const rows=D.si.filter(e=>{const p=gP(e.cod);return!q||e.cod.toLowerCase().includes(q)||(p&&p.art.toLowerCase().includes(q));});
  const tb=document.getElementById('tb-si');
  if(!rows.length){tb.innerHTML=`<tr><td colspan="5"><div class="empty">No hay salidas registradas</div></td></tr>`;return;}
  tb.innerHTML=rows.map(e=>{const p=gP(e.cod);return`<tr>
    <td><span class="bx bx-a">${e.cod}</span></td><td>${p?p.art:'—'}</td><td>${fD(e.f)}</td><td class="nm r">-${e.c}</td>
    <td><div class="acts">
      <button class="btn bn-gh sm" onclick="openESI(${e.id})">✏️</button>
      <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('si',${e.id},'salida #${e.id}')">🗑️</button>
    </div></td>
  </tr>`;}).join('');
}
let siId=null;
function openMSI(){fillSel('si-cod');document.getElementById('si-fecha').value=today();document.getElementById('si-cant').value='';openM('m-si');}
function saveSI(){const cod=document.getElementById('si-cod').value,f=document.getElementById('si-fecha').value,c=parseInt(document.getElementById('si-cant').value);if(!f||!c||c<1){toast('Completa campos','err');return;}const s=stk(cod);if(c>s.st){toast(`Stock insuficiente. Disponible: ${s.st}`,'err');return;}D.si.push({id:D.nid++,cod,f,c});sv();renderAll();closeM('m-si');toast('Salida registrada ✓');}
function openESI(id){const e=D.si.find(x=>x.id===id);if(!e)return;siId=id;fillSel('esi-cod',e.cod);document.getElementById('esi-f').value=e.f;document.getElementById('esi-c').value=e.c;openM('m-esi');}
function saveESI(){const e=D.si.find(x=>x.id===siId);if(!e)return;e.cod=document.getElementById('esi-cod').value;e.f=document.getElementById('esi-f').value;e.c=parseInt(document.getElementById('esi-c').value);sv();renderAll();closeM('m-esi');toast('Actualizado ✓');}

// ===== FINANZAS =====
function renderFin(){
  const q=document.getElementById('sq-fin').value.toLowerCase();
  const rows=D.fin.filter(f=>!q||f.con.toLowerCase().includes(q));
  const ing=D.fin.filter(f=>f.t==='i').reduce((a,f)=>a+f.m,0);
  const egr=D.fin.filter(f=>f.t==='e').reduce((a,f)=>a+f.m,0);
  const sal=ing-egr;
  document.getElementById('fin-ing').textContent=fM(ing);
  document.getElementById('fin-egr').textContent=fM(egr);
  const sv2=document.getElementById('fin-sal');
  sv2.textContent=fM(sal);
  sv2.style.color=sal>=0?'var(--green)':'var(--red)';
  const tb=document.getElementById('tb-fin');
  if(!rows.length){tb.innerHTML=`<tr><td colspan="6"><div class="empty">No hay movimientos registrados</div></td></tr>`;return;}
  let ac=0;const acs={};
  [...D.fin].sort((a,b)=>a.id-b.id).forEach(f=>{ac+=f.t==='i'?f.m:-f.m;acs[f.id]=ac;});
  tb.innerHTML=rows.map(f=>{
    const isI=f.t==='i',a=acs[f.id];
    return`<tr>
      <td>${fD(f.f)}</td>
      <td><span class="bx ${isI?'bx-g':'bx-r'}">${isI?'INGRESO':'EGRESO'}</span></td>
      <td>${f.con}</td>
      <td class="nm ${isI?'g':'r'}">${isI?'+':'-'}${fM(f.m)}</td>
      <td class="nm" style="color:${a>=0?'var(--green)':'var(--red)'}">${fM(a)}</td>
      <td><div class="acts">
        <button class="btn bn-gh sm" onclick="openEFin(${f.id})">✏️</button>
        <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('fin',${f.id},'${esc(f.con)}')">🗑️</button>
      </div></td>
    </tr>`;
  }).join('');
}
let finT='i',finEId=null;
function openMFin(tipo){
  finT=tipo==='ingreso'?'i':'e';
  const isI=finT==='i';
  document.getElementById('m-fin-t').textContent=isI?'Registrar Ingreso':'Registrar Egreso';
  document.getElementById('m-fin-t').style.color=isI?'var(--green)':'var(--red)';
  const btn=document.getElementById('fin-btn');btn.className='btn '+(isI?'bn-g':'bn-r');
  document.getElementById('fin-c').value='';document.getElementById('fin-f').value=today();document.getElementById('fin-m').value='';
  openM('m-fin');
}
function saveFin(){const con=document.getElementById('fin-c').value.trim(),f=document.getElementById('fin-f').value,m=parseFloat(document.getElementById('fin-m').value);if(!con||!f||!m||m<1){toast('Completa todos los campos','err');return;}D.fin.push({id:D.nid++,t:finT,con,f,m});sv();renderAll();closeM('m-fin');toast((finT==='i'?'Ingreso':'Egreso')+' registrado ✓');}
function openEFin(id){const f=D.fin.find(x=>x.id===id);if(!f)return;finEId=id;document.getElementById('m-efin-t').textContent='Editar '+(f.t==='i'?'Ingreso':'Egreso');document.getElementById('efin-c').value=f.con;document.getElementById('efin-f').value=f.f;document.getElementById('efin-m').value=f.m;openM('m-efin');}
function saveEFin(){const f=D.fin.find(x=>x.id===finEId);if(!f)return;f.con=document.getElementById('efin-c').value.trim();f.f=document.getElementById('efin-f').value;f.m=parseFloat(document.getElementById('efin-m').value);sv();renderAll();closeM('m-efin');toast('Actualizado ✓');}

// ===== CLIENTES =====
function renderCli(){
  const q=document.getElementById('sq-cli').value.toLowerCase();
  const rows=D.clis.filter(c=>!q||c.n.toLowerCase().includes(q)||c.t.includes(q)||c.e.toLowerCase().includes(q));
  const grid=document.getElementById('grid-cli');
  if(!rows.length){grid.innerHTML=`<div class="empty" style="grid-column:1/-1">No se encontraron clientes</div>`;return;}
  grid.innerHTML=rows.map(c=>`
    <div class="ccard">
      <div class="cname">👤 ${c.n}</div>
      <div class="cmeta">
        📞 <span>${c.t||'—'}</span><br>
        ✉️ <span>${c.e||'—'}</span><br>
        📍 <span>${c.d||'—'}</span><br>
        ${c.no?`📝 <span>${c.no}</span>`:''}
      </div>
      <div class="cacts">
        <button class="btn bn-gh sm" onclick="openECli(${c.id})">✏️ Editar</button>
        <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('cli',${c.id},'${esc(c.n)}')">🗑️ Borrar</button>
      </div>
    </div>
  `).join('');
}
let cliEId=null;
function openMCli(){cliEId=null;document.getElementById('m-cli-t').textContent='Nuevo Cliente';['cli-n','cli-t','cli-e','cli-d','cli-no'].forEach(x=>document.getElementById(x).value='');openM('m-cli');}
function saveCli(){const n=document.getElementById('cli-n').value.trim();if(!n){toast('Escribe el nombre del cliente','err');return;}D.clis.push({id:D.nid++,n,t:document.getElementById('cli-t').value.trim(),e:document.getElementById('cli-e').value.trim(),d:document.getElementById('cli-d').value.trim(),no:document.getElementById('cli-no').value.trim()});sv();renderAll();closeM('m-cli');toast('Cliente agregado ✓');}
function openECli(id){const c=D.clis.find(x=>x.id===id);if(!c)return;cliEId=id;document.getElementById('ecli-n').value=c.n;document.getElementById('ecli-t').value=c.t;document.getElementById('ecli-e').value=c.e;document.getElementById('ecli-d').value=c.d;document.getElementById('ecli-no').value=c.no;openM('m-ecli');}
function saveECli(){const c=D.clis.find(x=>x.id===cliEId);if(!c)return;c.n=document.getElementById('ecli-n').value.trim();c.t=document.getElementById('ecli-t').value.trim();c.e=document.getElementById('ecli-e').value.trim();c.d=document.getElementById('ecli-d').value.trim();c.no=document.getElementById('ecli-no').value.trim();sv();renderAll();closeM('m-ecli');toast('Actualizado ✓');}

// ===== SERVICIOS =====
function fillMesFil(){
  const sel=document.getElementById('fil-srv-mes');
  const cur=sel.value;
  const meses=[...new Set(D.srvs.map(s=>s.f.substring(0,7)))].sort().reverse();
  sel.innerHTML='<option value="">Todos los meses</option>'+meses.map(m=>{
    const[y,mm]=m.split('-');const ns=['Ene','Feb','Mar','Abr','May','Jun','Jul','Ago','Sep','Oct','Nov','Dic'];
    return`<option value="${m}"${m===cur?' selected':''}>${ns[parseInt(mm)-1]} ${y}</option>`;
  }).join('');
}

function renderSrv(){
  fillMesFil();
  const q=document.getElementById('sq-srv').value.toLowerCase();
  const mes=document.getElementById('fil-srv-mes').value;
  const est=document.getElementById('fil-srv-est').value;
  let rows=[...D.srvs].sort((a,b)=>b.f.localeCompare(a.f));
  if(q) rows=rows.filter(s=>s.cli.toLowerCase().includes(q)||s.desc.toLowerCase().includes(q));
  if(mes) rows=rows.filter(s=>s.f.startsWith(mes));
  if(est) rows=rows.filter(s=>s.est===est);

  const ahora=today().substring(0,7);
  const totalM=D.srvs.filter(s=>s.f.startsWith(ahora)).length;
  const pendM=D.srvs.filter(s=>s.est==='pendiente').length;
  document.getElementById('cc-srv').textContent=D.srvs.length;
  document.getElementById('cc-srv-monto').textContent=fM(D.srvs.reduce((a,s)=>a+(s.val||0),0));
  document.getElementById('cc-srv-mes').textContent=totalM;
  document.getElementById('cc-srv-pend').textContent=pendM;

  const tb=document.getElementById('tb-srv');
  if(!rows.length){tb.innerHTML=`<tr><td colspan="6"><div class="empty">No hay servicios registrados</div></td></tr>`;return;}
  const estBx={pendiente:'bx-y',entregado:'bx-g',garantia:'bx-p'};
  const estLbl={pendiente:'PENDIENTE',entregado:'ENTREGADO',garantia:'GARANTÍA'};
  tb.innerHTML=rows.map(s=>`<tr>
    <td>${fD(s.f)}</td>
    <td><strong>${s.cli}</strong>${s.tel?`<br><span style="color:var(--muted);font-size:.76rem">📞 ${s.tel}</span>`:''}</td>
    <td style="max-width:280px;font-size:.82rem">${s.desc}</td>
    <td class="nm g">${s.val?fM(s.val):'—'}</td>
    <td><span class="bx ${estBx[s.est]||'bx-a'}">${estLbl[s.est]||s.est}</span></td>
    <td><div class="acts">
      <button class="btn bn-gh sm" onclick="openESrv(${s.id})">✏️</button>
      <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('srv',${s.id},'servicio de ${esc(s.cli)}')">🗑️</button>
    </div></td>
  </tr>`).join('');
}

let srvEId=null;
function openMSrv(){
  srvEId=null;
  document.getElementById('m-srv-t').textContent='Nuevo Servicio';
  ['srv-cli','srv-desc','srv-tel'].forEach(x=>document.getElementById(x).value='');
  document.getElementById('srv-val').value='';
  document.getElementById('srv-f').value=today();
  document.getElementById('srv-est').value='pendiente';
  openM('m-srv');
}
function saveSrv(){
  const cli=document.getElementById('srv-cli').value.trim();
  const desc=document.getElementById('srv-desc').value.trim();
  const f=document.getElementById('srv-f').value;
  const est=document.getElementById('srv-est').value;
  const val=parseFloat(document.getElementById('srv-val').value)||0;
  const tel=document.getElementById('srv-tel').value.trim();
  if(!cli||!desc||!f){toast('Cliente, descripción y fecha son requeridos','err');return;}
  D.srvs.push({id:D.nid++,cli,desc,f,est,val,tel});
  sv();renderAll();closeM('m-srv');toast('Servicio registrado ✓');
}
function openESrv(id){
  const s=D.srvs.find(x=>x.id===id);if(!s)return;
  srvEId=id;
  document.getElementById('esrv-cli').value=s.cli;
  document.getElementById('esrv-desc').value=s.desc;
  document.getElementById('esrv-f').value=s.f;
  document.getElementById('esrv-est').value=s.est;
  document.getElementById('esrv-val').value=s.val||'';
  document.getElementById('esrv-tel').value=s.tel||'';
  openM('m-esrv');
}
function saveESrv(){
  const s=D.srvs.find(x=>x.id===srvEId);if(!s)return;
  s.cli=document.getElementById('esrv-cli').value.trim();
  s.desc=document.getElementById('esrv-desc').value.trim();
  s.f=document.getElementById('esrv-f').value;
  s.est=document.getElementById('esrv-est').value;
  s.val=parseFloat(document.getElementById('esrv-val').value)||0;
  s.tel=document.getElementById('esrv-tel').value.trim();
  sv();renderAll();closeM('m-esrv');toast('Servicio actualizado ✓');
}

// ===== COBROS =====
function renderCob(){
  const q=document.getElementById('sq-cob').value.toLowerCase();
  const filEst=document.getElementById('fil-cob-est').value;
  let rows=D.cobros;
  if(q) rows=rows.filter(c=>c.cli.toLowerCase().includes(q)||c.desc.toLowerCase().includes(q));

  const totalDeuda=D.cobros.reduce((a,c)=>a+c.total,0);
  const totalPag=D.cobros.reduce((a,c)=>a+c.pagos.reduce((x,p)=>x+p.m,0),0);
  const pendiente=Math.max(0,totalDeuda-totalPag);
  const conDeuda=D.cobros.filter(c=>{const p=c.pagos.reduce((x,px)=>x+px.m,0);return c.total-p>0;}).length;

  document.getElementById('cob-total').textContent=fM(totalDeuda);
  document.getElementById('cob-pagado').textContent=fM(totalPag);
  document.getElementById('cob-pendiente').textContent=fM(pendiente);
  document.getElementById('cob-count').textContent=conDeuda;

  if(filEst==='pendiente') rows=rows.filter(c=>{const p=c.pagos.reduce((x,px)=>x+px.m,0);return c.total-p>0;});
  else if(filEst==='pagado') rows=rows.filter(c=>{const p=c.pagos.reduce((x,px)=>x+px.m,0);return c.total-p<=0;});

  const grid=document.getElementById('grid-cob');
  if(!rows.length){grid.innerHTML=`<div class="empty" style="grid-column:1/-1">No hay cuentas por cobrar registradas</div>`;return;}
  grid.innerHTML=rows.map(c=>{
    const pagado=c.pagos.reduce((a,p)=>a+p.m,0);
    const saldo=Math.max(0,c.total-pagado);
    const pct=Math.min(100,Math.round(pagado/c.total*100));
    const esPagado=saldo<=0;
    const ultPagos=c.pagos.slice(-2).reverse();
    return`<div class="dcard ${esPagado?'pagado':''}">
      <div class="dname ${esPagado?'pagado':''}">💳 ${c.cli}</div>
      <div class="dmeta">
        📋 <span>${c.desc}</span><br>
        📅 <span>Desde: ${fD(c.f)}</span><br>
        ${c.tel?`📞 <span>${c.tel}</span><br>`:''}
        💰 Total: <span>${fM(c.total)}</span><br>
        ✅ Pagado: <span style="color:var(--green)">${fM(pagado)}</span><br>
        ${esPagado
          ?`<span style="color:var(--green);font-weight:600">✔ CANCELADO</span>`
          :`⏳ Pendiente: <span style="color:var(--red)">${fM(saldo)}</span>`}
      </div>
      <div class="dbar-wrap"><div class="dbar-fill ${esPagado?'full':''}" style="width:${pct}%"></div></div>
      <div style="font-family:'IBM Plex Mono',monospace;font-size:.68rem;color:var(--muted);text-align:right;margin-top:.2rem">${pct}% pagado</div>
      ${ultPagos.length?`<div class="pagos-section">
        <div class="pagos-title">Últimos pagos</div>
        ${ultPagos.map(p=>`<div class="pago-row"><span>${fD(p.f)}${p.nota?' – '+p.nota:''}</span><strong>+${fM(p.m)}</strong></div>`).join('')}
      </div>`:''}
      <div class="dacts">
        ${!esPagado?`<button class="btn bn-g sm" onclick="openMPago(${c.id})">💵 Registrar Pago</button>`:''}
        <button class="btn bn-gh sm" onclick="openMPago(${c.id})">📋 Ver Pagos</button>
        <button class="btn bn-gh sm" onclick="openECob(${c.id})">✏️</button>
        <button class="btn bn-gh sm" style="color:var(--red)" onclick="askD('cob',${c.id},'deuda de ${esc(c.cli)}')">🗑️</button>
      </div>
    </div>`;
  }).join('');
}

let cobEId=null;
function openMCob(){
  cobEId=null;
  ['cob-cli','cob-desc','cob-tel'].forEach(x=>document.getElementById(x).value='');
  document.getElementById('cob-total-i').value='';
  document.getElementById('cob-f').value=today();
  openM('m-cob');
}
function saveCob(){
  const cli=document.getElementById('cob-cli').value.trim();
  const desc=document.getElementById('cob-desc').value.trim();
  const total=parseFloat(document.getElementById('cob-total-i').value);
  const f=document.getElementById('cob-f').value;
  const tel=document.getElementById('cob-tel').value.trim();
  if(!cli||!desc||!total||total<1||!f){toast('Completa todos los campos','err');return;}
  D.cobros.push({id:D.nid++,cli,desc,total,f,tel,pagos:[]});
  sv();renderAll();closeM('m-cob');toast('Deuda registrada ✓');
}
function openECob(id){
  const c=D.cobros.find(x=>x.id===id);if(!c)return;
  cobEId=id;
  document.getElementById('cob-cli').value=c.cli;
  document.getElementById('cob-desc').value=c.desc;
  document.getElementById('cob-total-i').value=c.total;
  document.getElementById('cob-f').value=c.f;
  document.getElementById('cob-tel').value=c.tel||'';
  document.getElementById('m-cob-t').textContent='Editar Cuenta por Cobrar';
  openM('m-cob');
}
// reutilizamos saveCob para editar
const _saveCobOrig=saveCob;
function saveCob(){
  const cli=document.getElementById('cob-cli').value.trim();
  const desc=document.getElementById('cob-desc').value.trim();
  const total=parseFloat(document.getElementById('cob-total-i').value);
  const f=document.getElementById('cob-f').value;
  const tel=document.getElementById('cob-tel').value.trim();
  if(!cli||!desc||!total||total<1||!f){toast('Completa todos los campos','err');return;}
  if(cobEId!==null){
    const c=D.cobros.find(x=>x.id===cobEId);
    if(c){c.cli=cli;c.desc=desc;c.total=total;c.f=f;c.tel=tel;toast('Actualizado ✓');}
    cobEId=null;
    document.getElementById('m-cob-t').textContent='Nueva Cuenta por Cobrar';
  } else {
    D.cobros.push({id:D.nid++,cli,desc,total,f,tel,pagos:[]});
    toast('Deuda registrada ✓');
  }
  sv();renderAll();closeM('m-cob');
}

// PAGOS
let pagoId=null;
function openMPago(id){
  pagoId=id;
  const c=D.cobros.find(x=>x.id===id);if(!c)return;
  const pagado=c.pagos.reduce((a,p)=>a+p.m,0);
  const saldo=Math.max(0,c.total-pagado);
  document.getElementById('pago-info').innerHTML=
    `<strong style="color:var(--orange)">${c.cli}</strong><br>
     Deuda total: ${fM(c.total)} &nbsp;|&nbsp; Pagado: <span style="color:var(--green)">${fM(pagado)}</span> &nbsp;|&nbsp; Pendiente: <span style="color:var(--red)">${fM(saldo)}</span>`;
  document.getElementById('pago-monto').value='';
  document.getElementById('pago-f').value=today();
  document.getElementById('pago-nota').value='';
  // historial
  const hist=document.getElementById('pago-hist');
  if(!c.pagos.length){hist.innerHTML='<div style="color:var(--muted);font-size:.8rem;padding:.3rem 0">Sin pagos registrados aún</div>';}
  else{
    hist.innerHTML=c.pagos.map((p,i)=>`
      <div class="hpago-item">
        <div>
          <div class="hpi-fecha">${fD(p.f)}${p.nota?' – '+p.nota:''}</div>
        </div>
        <div style="display:flex;align-items:center;gap:.5rem">
          <span class="hpi-monto">+${fM(p.m)}</span>
          <button class="hpi-del" onclick="delPago(${id},${i})" title="Eliminar pago">✕</button>
        </div>
      </div>`).join('');
  }
  openM('m-pago');
}
function savePago(){
  const c=D.cobros.find(x=>x.id===pagoId);if(!c)return;
  const m=parseFloat(document.getElementById('pago-monto').value);
  const f=document.getElementById('pago-f').value;
  const nota=document.getElementById('pago-nota').value.trim();
  if(!m||m<1||!f){toast('Ingresa monto y fecha','err');return;}
  const pagado=c.pagos.reduce((a,p)=>a+p.m,0);
  if(pagado+m>c.total){toast(`Excede la deuda. Máximo abono: ${fM(c.total-pagado)}`,'err');return;}
  c.pagos.push({f,m,nota});
  sv();renderCob();openMPago(pagoId);toast('Pago registrado ✓');
}
function delPago(cobId,idx){
  const c=D.cobros.find(x=>x.id===cobId);if(!c)return;
  c.pagos.splice(idx,1);
  sv();renderCob();openMPago(cobId);toast('Pago eliminado');
}

// ===== DELETE =====
let pend=null;
function askD(type,id,label){pend={type,id};document.getElementById('conf-msg').innerHTML=`¿Eliminar <strong>"${label}"</strong>? Esta acción no se puede deshacer.`;openM('m-conf');}
function doDel(){
  if(!pend)return;
  const{type,id}=pend;
  if(type==='p'){D.prods=D.prods.filter(p=>p.id!==id);D.ei=D.ei.filter(e=>e.cod!==id);D.si=D.si.filter(s=>s.cod!==id);toast('Producto eliminado');}
  else if(type==='ei'){D.ei=D.ei.filter(e=>e.id!==id);toast('Entrada eliminada');}
  else if(type==='si'){D.si=D.si.filter(s=>s.id!==id);toast('Salida eliminada');}
  else if(type==='fin'){D.fin=D.fin.filter(f=>f.id!==id);toast('Movimiento eliminado');}
  else if(type==='cli'){D.clis=D.clis.filter(c=>c.id!==id);toast('Cliente eliminado');}
  else if(type==='srv'){D.srvs=D.srvs.filter(s=>s.id!==id);toast('Servicio eliminado');}
  else if(type==='cob'){D.cobros=D.cobros.filter(c=>c.id!==id);toast('Cuenta eliminada');}
  pend=null;sv();renderAll();closeM('m-conf');
}

// ===== LOGIN =====
const ADMIN_USER='administrador';
const ADMIN_PASS='tecnico2026';
const SESSION_KEY='ta_session';
let failCount=0;
let lockUntil=0;

function checkSession(){
  const s=sessionStorage.getItem(SESSION_KEY);
  if(s==='ok'){showApp();}
}

function doLogin(){
  const now=Date.now();
  if(now<lockUntil){
    const secs=Math.ceil((lockUntil-now)/1000);
    document.getElementById('login-err').textContent='Demasiados intentos. Espera '+secs+'s';
    return;
  }
  const u=document.getElementById('login-user').value.trim().toLowerCase();
  const p=document.getElementById('login-pass').value;
  if(u===ADMIN_USER && p===ADMIN_PASS){
    failCount=0;
    sessionStorage.setItem(SESSION_KEY,'ok');
    document.getElementById('login-err').textContent='';
    document.getElementById('login-attempts').textContent='';
    showApp();
  } else {
    failCount++;
    document.getElementById('login-pass').value='';
    if(failCount>=5){
      lockUntil=Date.now()+30000;
      failCount=0;
      document.getElementById('login-err').textContent='Bloqueado 30 segundos por múltiples intentos fallidos.';
    } else {
      const rest=5-failCount;
      document.getElementById('login-err').textContent='Usuario o contraseña incorrectos.';
      document.getElementById('login-attempts').textContent='Intentos restantes: '+rest;
    }
    document.getElementById('login-pass').focus();
  }
}

function showApp(){
  document.getElementById('login-screen').classList.add('hidden');
  document.getElementById('app-wrap').classList.add('visible');
  renderAll();
}

function doLogout(){
  sessionStorage.removeItem(SESSION_KEY);
  document.getElementById('login-screen').classList.remove('hidden');
  document.getElementById('app-wrap').classList.remove('visible');
  document.getElementById('login-user').value='';
  document.getElementById('login-pass').value='';
  document.getElementById('login-err').textContent='';
  document.getElementById('login-attempts').textContent='';
}

function renderAll(){renderInv();renderEI();renderSI();renderFin();renderCli();renderSrv();renderCob();updH();}
checkSession();
</script>
</div><!-- /app-wrap -->
</body>
</html>
