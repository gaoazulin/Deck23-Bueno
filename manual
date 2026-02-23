<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Plano de Manutenção Preventiva — MAC OPUS</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Mono:wght@400;500&family=DM+Sans:wght@300;400;500;600&display=swap');

  :root {
    --bg: #0a0a0a;
    --surface: #111111;
    --surface2: #161616;
    --border: #2a2a2a;
    --border-gold: rgba(196,160,80,0.25);
    --gold: #c4a050;
    --gold-light: #e8c878;
    --gold-dim: #7a6030;
    --text: #e8e4d8;
    --text-dim: #7a7060;
    --text-mid: #a89878;
    --red: #c47858;
    --yellow: #c4a050;
    --green: #7a9868;
    --purple: #8878a8;
    --blue: #6888a8;
    --teal: #589888;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── HEADER ── */
  .header {
    background: linear-gradient(160deg, #0e0c08 0%, #0a0a0a 60%, #0c0e08 100%);
    border-bottom: 1px solid var(--border-gold);
    padding: 48px 56px 40px;
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 420px; height: 420px;
    background: radial-gradient(circle, rgba(196,160,80,0.07) 0%, transparent 65%);
    pointer-events: none;
  }
  .header::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    opacity: 0.4;
  }

  /* LOGO */
  .logo-wrap {
    display: flex; align-items: center; gap: 18px;
    margin-bottom: 36px;
  }
  .logo-mark {
    width: 54px; height: 54px;
    border: 1.5px solid var(--gold);
    border-radius: 4px;
    display: flex; align-items: center; justify-content: center;
    position: relative;
    background: rgba(196,160,80,0.05);
    flex-shrink: 0;
  }
  .logo-mark::before {
    content: '';
    position: absolute; inset: 4px;
    border: 1px solid rgba(196,160,80,0.3);
    border-radius: 2px;
  }
  .logo-m {
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px; font-weight: 600;
    color: var(--gold);
    letter-spacing: -1px;
    line-height: 1;
  }
  .logo-text { display: flex; flex-direction: column; gap: 1px; }
  .logo-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px; font-weight: 600;
    color: var(--gold-light);
    letter-spacing: 0.18em;
    line-height: 1;
    text-transform: uppercase;
  }
  .logo-sub {
    font-size: 10px; font-weight: 400;
    color: var(--text-mid);
    letter-spacing: 0.25em;
    text-transform: uppercase;
    font-family: 'DM Mono', monospace;
  }
  .logo-divider {
    width: 1px; height: 42px;
    background: linear-gradient(to bottom, transparent, var(--border-gold), transparent);
    margin: 0 6px;
  }
  .logo-tagline {
    font-size: 11px; color: var(--text-dim);
    letter-spacing: 0.12em; text-transform: uppercase;
    font-family: 'DM Mono', monospace;
    line-height: 1.6;
  }

  .header-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(196,160,80,0.08);
    border: 1px solid var(--border-gold);
    border-radius: 100px;
    padding: 5px 14px;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--gold-dim);
    letter-spacing: 0.08em;
    margin-bottom: 18px;
    text-transform: uppercase;
  }
  .header-badge::before { content: '◆'; font-size: 7px; color: var(--gold); }

  h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(30px, 4.5vw, 50px);
    font-weight: 300;
    line-height: 1.12;
    color: var(--text);
    margin-bottom: 10px;
    letter-spacing: 0.01em;
  }
  h1 em { color: var(--gold-light); font-style: italic; font-weight: 400; }

  .header-sub {
    color: var(--text-dim);
    font-size: 13px;
    font-weight: 300;
    margin-bottom: 32px;
    max-width: 620px;
    line-height: 1.7;
    letter-spacing: 0.02em;
  }

  .stats-row { display: flex; gap: 16px; flex-wrap: wrap; }
  .stat {
    background: var(--surface2);
    border: 1px solid var(--border-gold);
    border-radius: 6px;
    padding: 14px 22px;
    position: relative; overflow: hidden;
  }
  .stat::after {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold), transparent);
    opacity: 0.5;
  }
  .stat-val {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px; font-weight: 400;
    color: var(--gold-light);
    line-height: 1;
    margin-bottom: 3px;
  }
  .stat-label { font-size: 10px; color: var(--text-dim); text-transform: uppercase; letter-spacing: 0.1em; font-family: 'DM Mono', monospace; }

  /* ── CONTROLS ── */
  .controls {
    padding: 22px 56px;
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    display: flex; gap: 16px; align-items: center; flex-wrap: wrap;
  }
  .search-wrap { position: relative; flex: 1; min-width: 220px; max-width: 380px; }
  .search-wrap svg {
    position: absolute; left: 12px; top: 50%; transform: translateY(-50%);
    color: var(--text-dim); width: 15px; height: 15px;
  }
  input[type="search"] {
    width: 100%; background: var(--bg); border: 1px solid var(--border);
    border-radius: 6px; padding: 9px 12px 9px 36px;
    color: var(--text); font-family: 'DM Sans', sans-serif; font-size: 13px;
    outline: none; transition: border-color 0.2s;
  }
  input[type="search"]::placeholder { color: var(--text-dim); }
  input[type="search"]:focus { border-color: var(--gold); }

  .filter-chips { display: flex; gap: 8px; flex-wrap: wrap; }
  .chip {
    background: var(--bg); border: 1px solid var(--border);
    border-radius: 100px; padding: 6px 14px;
    font-size: 11px; font-weight: 500; color: var(--text-dim);
    cursor: pointer; transition: all 0.18s; white-space: nowrap;
    font-family: 'DM Mono', monospace; letter-spacing: 0.04em;
  }
  .chip:hover { border-color: var(--gold); color: var(--gold); }
  .chip.active {
    background: var(--gold); border-color: var(--gold);
    color: #0a0a0a; font-weight: 600;
  }

  /* ── MAIN ── */
  .main { padding: 32px 56px; }

  .category-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    margin-bottom: 14px;
    overflow: hidden;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .category-block:hover { border-color: var(--border-gold); box-shadow: 0 4px 40px rgba(196,160,80,0.04); }

  .cat-header {
    display: flex; align-items: center; gap: 16px;
    padding: 18px 24px; cursor: pointer;
    background: var(--surface2); transition: background 0.18s;
    user-select: none;
  }
  .cat-header:hover { background: #1a1a1a; }
  .cat-icon {
    width: 36px; height: 36px; border-radius: 6px;
    display: flex; align-items: center; justify-content: center;
    font-size: 16px; flex-shrink: 0;
    border: 1px solid var(--border-gold);
    background: rgba(196,160,80,0.06);
  }
  .cat-info { flex: 1; }
  .cat-name { font-size: 14px; font-weight: 500; color: var(--text); margin-bottom: 2px; letter-spacing: 0.01em; }
  .cat-count { font-size: 11px; color: var(--text-dim); font-family: 'DM Mono', monospace; }
  .cat-chevron { color: var(--gold-dim); transition: transform 0.25s; font-size: 16px; flex-shrink: 0; }
  .cat-header.open .cat-chevron { transform: rotate(90deg); color: var(--gold); }

  .items-table { display: none; }
  .items-table.open { display: block; }

  table { width: 100%; border-collapse: collapse; }
  thead tr { background: rgba(196,160,80,0.04); }
  th {
    padding: 10px 18px;
    font-size: 10px; text-transform: uppercase; letter-spacing: 0.1em;
    color: var(--gold-dim); font-family: 'DM Mono', monospace;
    text-align: left; font-weight: 500;
    border-bottom: 1px solid var(--border);
  }
  td {
    padding: 14px 18px; font-size: 13px; color: var(--text);
    border-bottom: 1px solid rgba(30,30,30,0.8);
    vertical-align: middle; line-height: 1.5;
  }
  tr:last-child td { border-bottom: none; }
  tr:hover td { background: rgba(196,160,80,0.02); }

  /* FREQUENCY BADGES */
  .freq-badge {
    display: inline-flex; align-items: center; gap: 5px;
    padding: 4px 10px; border-radius: 100px;
    font-size: 10.5px; font-family: 'DM Mono', monospace; font-weight: 500;
    white-space: nowrap; border: 1px solid transparent;
  }
  .freq-badge::before { content: ''; width: 5px; height: 5px; border-radius: 50%; background: currentColor; flex-shrink: 0; }

  .freq-diaria     { background: rgba(196,120,88,0.1); color: #c47858; border-color: rgba(196,120,88,0.2); }
  .freq-semanal    { background: rgba(196,160,80,0.1); color: var(--gold); border-color: var(--border-gold); }
  .freq-quinzenal  { background: rgba(200,180,100,0.1); color: #c8b464; border-color: rgba(200,180,100,0.2); }
  .freq-mensal     { background: rgba(232,200,120,0.1); color: var(--gold-light); border-color: rgba(232,200,120,0.2); }
  .freq-bimestral  { background: rgba(180,170,120,0.1); color: #b4aa78; border-color: rgba(180,170,120,0.2); }
  .freq-trimestral { background: rgba(120,152,104,0.1); color: var(--green); border-color: rgba(120,152,104,0.2); }
  .freq-quadrimestral { background: rgba(100,140,100,0.1); color: #88b084; border-color: rgba(100,140,100,0.2); }
  .freq-semestral  { background: rgba(104,136,168,0.1); color: var(--blue); border-color: rgba(104,136,168,0.2); }
  .freq-anual      { background: rgba(136,120,168,0.1); color: var(--purple); border-color: rgba(136,120,168,0.2); }
  .freq-bianual    { background: rgba(88,152,136,0.1); color: var(--teal); border-color: rgba(88,152,136,0.2); }
  .freq-trianual   { background: rgba(100,120,100,0.1); color: #90a888; border-color: rgba(100,120,100,0.2); }

  /* RESPONSIBLE */
  .resp { display: inline-flex; align-items: center; gap: 6px; font-size: 12px; color: var(--text-mid); }
  .resp-dot { width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0; }
  .resp-local  { background: var(--gold); }
  .resp-cap    { background: var(--teal); }
  .resp-espec  { background: var(--purple); }
  .resp-mixed  { background: var(--text-dim); }

  .item-obs { font-size: 11px; color: var(--text-dim); margin-top: 4px; font-style: italic; }

  .cat-hidden, .row-hidden { display: none !important; }

  /* LEGEND */
  .legend {
    display: flex; gap: 24px; flex-wrap: wrap;
    padding: 20px 56px;
    background: var(--surface);
    border-top: 1px solid var(--border-gold);
    margin-top: 8px;
  }
  .legend-item { display: flex; align-items: center; gap: 8px; font-size: 11.5px; color: var(--text-dim); font-family: 'DM Mono', monospace; }
  .legend-dot { width: 7px; height: 7px; border-radius: 50%; flex-shrink: 0; }
  .legend-norm { font-size: 11px; color: var(--text-dim); font-family: 'DM Mono', monospace; margin-left: auto; letter-spacing: 0.04em; }

  .gold-line {
    height: 1px;
    background: linear-gradient(90deg, transparent 0%, var(--gold) 30%, var(--gold) 70%, transparent 100%);
    opacity: 0.15;
    margin: 0 56px;
  }

  @media (max-width: 768px) {
    .header, .controls, .main, .legend { padding-left: 20px; padding-right: 20px; }
    .gold-line { margin: 0 20px; }
    th:nth-child(4), td:nth-child(4) { display: none; }
  }
</style>
</head>
<body>

<div class="header">
  <div class="logo-wrap">
    <div class="logo-mark"><span class="logo-m">M</span></div>
    <div class="logo-text">
      <span class="logo-name">MAC OPUS</span>
      <span class="logo-sub">Setor Bueno · Goiânia</span>
    </div>
    <div class="logo-divider"></div>
    <div class="logo-tagline">Plano de<br>Manutenção Preventiva</div>
  </div>

  <div class="header-badge">Manual das Áreas Comuns · ABNT NBR 5674</div>
  <h1>Manutenção<br><em>Preventiva</em></h1>
  <p class="header-sub">Rua T53 e Rua T27, Qd 87, Setor Bueno, Goiânia-GO.<br>Baseado no Manual das Áreas Comuns REV02 · Normas ABNT NBR 5674, 15575 e 14037.</p>
  <div class="stats-row">
    <div class="stat"><div class="stat-val" id="totalItems">0</div><div class="stat-label">Itens de Manutenção</div></div>
    <div class="stat"><div class="stat-val" id="totalCats">0</div><div class="stat-label">Categorias</div></div>
    <div class="stat"><div class="stat-val" style="font-size:20px;padding-top:4px">ABNT</div><div class="stat-label">NBR 5674 · NBR 15575</div></div>
  </div>
</div>

<div class="controls">
  <div class="search-wrap">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
    <input type="search" id="searchInput" placeholder="Buscar atividade, sistema, responsável…">
  </div>
  <div class="filter-chips">
    <span class="chip active" data-freq="todos">Todos</span>
    <span class="chip" data-freq="diaria">Diária</span>
    <span class="chip" data-freq="semanal">Semanal</span>
    <span class="chip" data-freq="quinzenal">Quinzenal</span>
    <span class="chip" data-freq="mensal">Mensal</span>
    <span class="chip" data-freq="trimestral">Trimestral</span>
    <span class="chip" data-freq="semestral">Semestral</span>
    <span class="chip" data-freq="anual">Anual</span>
  </div>
</div>

<div class="main" id="mainContent"></div>

<div class="gold-line"></div>
<div class="legend">
  <div class="legend-item"><span class="legend-dot" style="background:var(--gold)"></span>Equipe local</div>
  <div class="legend-item"><span class="legend-dot" style="background:var(--teal)"></span>Empresa capacitada</div>
  <div class="legend-item"><span class="legend-dot" style="background:var(--purple)"></span>Empresa especializada</div>
  <div class="legend-item"><span class="legend-dot" style="background:var(--text-dim)"></span>Ver observação</div>
  <span class="legend-norm">ABNT NBR 5674 · NBR 15575 · NBR 14037 · MAC OPUS REV02</span>
</div>

<script>
const data = [
  { id:"hidraulica-agua-potavel", icon:"💧", name:"Instalações Hidráulicas — Água Potável", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar o nível dos reservatórios, o funcionamento das torneiras de boia e a chave de boia para controle de nível",resp:"local"},
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Utilizar e limpar as bombas em sistema de rodízio por meio da chave de alternância no painel elétrico (quando não houver reversão automática)",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar a estanqueidade e a pressão especificada para a válvula redutora de pressão das colunas de água potável",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar funcionalidade do extravasor (ladrão) dos reservatórios, evitando entupimentos por incrustações ou sujeiras",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar mecanismos internos da caixa acoplada",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a estanqueidade dos registros de gaveta",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Abrir e fechar completamente os registros da cobertura (barrilete) para evitar emperramentos",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Limpar e verificar a regulagem dos mecanismos de descarga",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Efetuar manutenção nas bombas de recalque de água potável",resp:"especializada",obs:"Empresa especializada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Limpar os arejadores (bicos removíveis) das torneiras",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar o sistema de pressurização de água: regulagem da pressão, reaperto dos componentes e parametrização dos sistemas elétricos/eletrônicos",resp:"especializada",obs:"Empresa especializada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Limpar os reservatórios e fornecer atestado de potabilidade. Isolar tubulações da válvula redutora durante a limpeza",resp:"especializada",obs:"Empresa especializada. Também quando houver indícios de contaminação"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Limpar os filtros e efetuar revisão nas válvulas redutoras de pressão conforme orientações do fabricante",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a estanqueidade da válvula de descarga, torneira automática e torneira eletrônica (caso haja)",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar as tubulações de água potável para detectar obstruções, corrosão superficial e estanqueidade",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar e, se necessário, substituir os vedantes (courinhos) das torneiras, misturadores e registros de pressão",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar o funcionamento do sistema de aquecimento individual e efetuar limpeza e regulagem conforme legislação vigente",resp:"capacitada",obs:"Empresa capacitada"},
  ]},
  { id:"hidraulica-pluvial", icon:"🌧️", name:"Instalações Hidráulicas — Águas Pluviais, Servidas e Esgoto", items:[
    {freq:"semanal",freqLabel:"Semanal (chuvas intensas) / Mensal",desc:"Verificar e limpar os ralos e grelhas das águas pluviais, calhas e canaletas",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Efetuar limpeza geral nas caixas de esgoto, de gordura e de águas servidas",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Limpar os reservatórios de água não potável e realizar eventual manutenção do revestimento impermeável",resp:"local",obs:"Ou quando detectada alguma obstrução"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Abrir e fechar completamente os registros dos subsolos e cobertura (barrilete), evitando emperramento",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Efetuar manutenção nas bombas de recalque de águas pluviais",resp:"especializada",obs:"Empresa especializada"},
    {freq:"semestral",freqLabel:"Semestral (estiagem) / Semanal (chuvas)",desc:"Verificar se as bombas submersas não estão encostadas no fundo do reservatório",resp:"mixed",obs:"Equipe local / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar as tubulações de captação de água do jardim para detectar raízes que possam destruir ou entupir as tubulações",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar as tubulações de água servida para detectar obstruções, perda de estanqueidade e fixação",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"spa", icon:"🛁", name:"SPA (Hidromassagem)", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Fazer teste de funcionamento conforme instruções do fornecedor",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Limpeza dos dispositivos que impossibilitem a entrada de resíduos na tubulação",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Refazer o rejuntamento das bordas com silicone específico ou mastique",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"incendio-hidrantes", icon:"🔥", name:"Proteção Contra Incêndio — Hidrantes", items:[
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Verificar a existência de vazamento e/ou outros defeitos nas tubulações, válvulas, registros e esguichos dos hidrantes",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar o estado de conservação geral das caixas, esguichos, registros, adaptadores, chaves de engate e puxador do abrigo",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar se os abrigos estão secos e desobstruídos",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Toda mangueira em uso (em prontidão para combate a incêndio) deve ser inspecionada",resp:"especializada",obs:"Empresa especializada"},
    {freq:"quadrimestral",freqLabel:"A cada 4 meses",desc:"Inspeção visual e limpeza das mangueiras e mangotinho",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Realizar inspeção visual e dimensional das mangueiras de incêndio; verificar dificuldade de acoplamento das uniões",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar manutenção com ensaio hidrostático conforme ABNT NBR 12779 e promover identificação individual com nome do executante, data e validade",resp:"mixed",obs:"Empresa capacitada / especializada. Edifício não pode ficar sem mangueiras durante inspeção"},
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Realizar testes e ensaios para determinar as condições de funcionamento do sistema: vazão, bomba de incêndio, alarmes",resp:"especializada",obs:"Brigada de incêndio / empresa especializada"},
  ]},
  { id:"incendio-bomba", icon:"⛽", name:"Proteção Contra Incêndio — Reserva e Bomba de Incêndio", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar o nível dos reservatórios de incêndio e o funcionamento das torneiras de boia",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar a estanqueidade do sistema e acionar a bomba de incêndio (por dreno da tubulação ou botoeira)",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a estanqueidade dos registros de gaveta; abrir e fechar completamente os registros evitando emperramentos",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Efetuar manutenção nas bombas de incêndio",resp:"especializada",obs:"Empresa especializada"},
  ]},
  { id:"incendio-extintores", icon:"🧯", name:"Proteção Contra Incêndio — Extintores", items:[
    {freq:"anual",freqLabel:"Conforme lacre",desc:"Revisar e recarregar os extintores conforme prazo indicado no lacre. Manutenção de 1º, 2º e 3º nível conforme ABNT NBR 12962",resp:"especializada",obs:"Empresa especializada registrada. Ensaio hidrostático a cada 5 anos"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar o estado e, se necessário, substituir as placas de sinalização das áreas de rota de fuga",resp:"local"},
  ]},
  { id:"incendio-detector", icon:"🔊", name:"Proteção Contra Incêndio — Detectores e Alarmes", items:[
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Ensaio funcional de todos os acionadores manuais do sistema, dos comandos e dos painéis repetidores",resp:"mixed",obs:"Equipe local / empresa especializada. Periodicidade máxima: 3 meses"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar um teste operacional em todos os detectores de fumaça e calor",resp:"local"},
  ]},
  { id:"incendio-porta", icon:"🚪", name:"Proteção Contra Incêndio — Porta Corta-fogo", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar o funcionamento automático e de todos os acessórios (fechaduras, dispositivos antipânico, selecionadores, travas). Efetuar limpeza dos alojadores de trincos, piso e batentes",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Lubrificação de todas as partes móveis; verificação da legibilidade dos identificadores; verificação das condições gerais e regulagem ou substituição dos elementos defeituosos",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"incendio-pressurizacao", icon:"💨", name:"Proteção Contra Incêndio — Pressurização de Escada", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Realizar a manutenção dos ventiladores e do gerador que suportam os sistemas de pressurização da escada",resp:"especializada",obs:"Empresa especializada. Manter contrato de manutenção"},
  ]},
  { id:"eletrica", icon:"⚡", name:"Instalações Elétricas", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Limpeza e verificação do estado de conservação de lâmpadas, luminárias e reatores. Substituição ou reparo de componentes queimados/danificados. Verificar oxidação de partes metálicas e integridade dos suportes",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Rever o estado de isolamento dos fios, conexões, interruptores, disjuntores e tomadas externas; verificar e manter estanqueidade das luminárias",resp:"capacitada",obs:"Empresa capacitada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Testar o disjuntor tipo DR apertando o botão. Se ao apertar o botão a energia não for interrompida, trocar o DR",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar o funcionamento da luz piloto de sinalização aérea (Lei 13.133/2015 — obrigatório, sob pena de multa)",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Rever o estado de isolamento das emendas de fios e providenciar correções se necessário",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar e, se necessário, reapertar as conexões do quadro de distribuição",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar o estado dos contatos elétricos (tomadas, interruptores, pontos de luz) e substituir peças com desgaste",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar inspeção termográfica dos sistemas elétricos para visualização de possíveis sobrecargas e temperatura admissível dos componentes",resp:"especializada",obs:"Empresa especializada"},
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Reapertar todas as conexões (tomadas, interruptores, pontos de luz e outros)",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"automacao", icon:"🤖", name:"Automação Predial", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar funcionamento do sistema de automação predial (iluminação das áreas comuns e bombas)",resp:"local",obs:"Manter contrato com empresa especializada credenciada pelo fabricante"},
  ]},
  { id:"gerador", icon:"⚙️", name:"Grupo Gerador", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar, após o uso do equipamento, o nível de óleo combustível e se há obstrução nas entradas e saídas de ventilação",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Efetuar teste de acionamento e funcionamento do sistema do gerador",resp:"local"},
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Inspeção visual do motor do gerador e componentes do sistema (painel de controle, nível de combustível, etc.)",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"quinzenal",freqLabel:"Quinzenal / após cada uso",desc:"Verificar o nível de combustível do reservatório e, se necessário, complementar",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Verificar e, se necessário, efetuar manutenção do catalizador do gerador",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Limpar a cabine/carenagem do gerador",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar o funcionamento do sistema a plena carga, com todas as lâmpadas ligadas, avaliando as operações",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"emergencia", icon:"🔆", name:"Iluminação de Emergência", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar o LED de funcionamento e carga do grupo gerador de emergência",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Efetuar teste de acionamento e funcionamento do sistema de iluminação de emergência",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"quinzenal",freqLabel:"Quinzenal",desc:"Inspeção visual do motor gerador e componentes do sistema",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Efetuar as manutenções previstas no sistema do Grupo Gerador",resp:"especializada",obs:"Empresa especializada"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Fazer teste de funcionamento do sistema de blocos autônomos por 1 hora",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar o funcionamento do sistema a plena carga, com todas as lâmpadas ligadas, avaliando as operações",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"spda", icon:"⚡", name:"SPDA — Sistema de Proteção Contra Descargas Atmosféricas (Para-raios)", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar o status dos Dispositivos de Proteção Contra Surtos (DPS): verde = funcionamento normal",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Inspecionar e apontar visualmente eventuais pontos deteriorados no sistema para realizar a reconstituição necessária",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Inspecionar estruturas conforme ABNT NBR 5419. Atestado de SPDA exigido anualmente",resp:"especializada",obs:"Empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Inspeções completas conforme ABNT NBR 5419. Inclui medição ôhmica com terrômetro calibrado pelo INMETRO",resp:"especializada",obs:"Empresa especializada"},
  ]},
  { id:"seguranca", icon:"📷", name:"Sistema de Segurança — CFTV", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar se as câmeras de segurança estão funcionando adequadamente e se as imagens estão sendo gravadas corretamente",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar o funcionamento de todo o sistema de segurança",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Vistoria completa no sistema instalado e realização de manutenções",resp:"especializada",obs:"Empresa especializada"},
  ]},
  { id:"interfone", icon:"📞", name:"Telefonia e Sistema de Interfones", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar o funcionamento do sistema de interfones conforme instruções do fornecedor",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Vistoria completa no sistema instalado e realização de manutenções",resp:"especializada",obs:"Empresa especializada"},
  ]},
  { id:"elevadores", icon:"🛗", name:"Elevadores e Plataforma Elevatória de Acessibilidade", items:[
    {freq:"mensal",freqLabel:"Contratual (mensal)",desc:"Manutenção preventiva e corretiva obrigatória com empresa especializada autorizada pelo fabricante, conforme ABNT NBR 16083",resp:"especializada",obs:"Obrigatório manter contrato de manutenção. Empresa autorizada pelo fabricante"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Efetuar teste do sistema automático de funcionamento dos elevadores com energia elétrica proveniente dos geradores",resp:"especializada",obs:"Empresa especializada"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Efetuar teste do sistema automático de resgate de passageiros dos elevadores",resp:"especializada",obs:"Empresa especializada"},
  ]},
  { id:"portoes", icon:"🚧", name:"Automação de Portões", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Fazer a manutenção dos sistemas de automação dos portões conforme instruções do fornecedor (motores elétricos, fechaduras elétricas, sensores, controles)",resp:"especializada",obs:"Empresa especializada. Manter contrato de manutenção"},
  ]},
  { id:"arcondicionado", icon:"❄️", name:"Ar Condicionado (Áreas Comuns)", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Ligar o sistema de ar condicionado (manter funcionamento regular)",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Realizar limpeza dos componentes e filtros, mesmo em período de não utilização",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Realizar a manutenção dos ventiladores do sistema de ar condicionado",resp:"especializada",obs:"Empresa especializada"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar se está funcionando corretamente e se as unidades de montagem estão firmemente instaladas",resp:"local"},
  ]},
  { id:"exaustao", icon:"🌀", name:"Sistema de Exaustão Mecânica", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Realizar a manutenção dos ventiladores que compõem os sistemas de exaustão mecânica",resp:"especializada",obs:"Empresa especializada"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Limpeza do aparelho do ventokit",resp:"local"},
  ]},
  { id:"sauna", icon:"🧖", name:"Sauna Úmida", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Fazer a drenagem de água no equipamento (escoar a água abrindo a torneira ou tampão)",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Regular e verificar a calibragem do termostato conforme recomendação do fabricante",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"churrasqueira", icon:"🔥", name:"Churrasqueira para Uso a Carvão", items:[
    {freq:"semanal",freqLabel:"Semanal",desc:"Fazer limpeza geral da churrasqueira (com vassoura ou pano úmido, com a churrasqueira fria; nunca utilize água)",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar os revestimentos e tijolos refratários e, havendo necessidade, providenciar reparos",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"gas", icon:"🔵", name:"Instalações de Gás", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar possível vazamento de gás, a integridade das instalações e se as ventilações permanentes estão livres e desobstruídas",resp:"local",obs:"Também verificar quando sentir cheiro de gás"},
    {freq:"anual",freqLabel:"Anual",desc:"Checkup completo do sistema de gás: verificar funcionamento, limpeza, regulagem e estanqueidade dos equipamentos e tubulações conforme ABNT e normas do Corpo de Bombeiros",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"A cada 5 anos (validade)",desc:"Verificar a validade da mangueira de gás, que tem prazo de cinco anos",resp:"local"},
  ]},
  { id:"impermeabilizacao", icon:"🛡️", name:"Impermeabilização", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade e reconstituir os rejuntamentos internos e externos dos pisos, paredes, peitoris, soleiras, ralos, peças sanitárias, chaminés e grelhas de ventilação",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Inspecionar a camada drenante do jardim; limpar obstruções na tubulação e entupimentos dos ralos ou grelhas",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade dos sistemas de impermeabilização e reconstituir a proteção mecânica, sinais de infiltração ou falhas da impermeabilização expostas",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"esquadrias-madeira", icon:"🪵", name:"Esquadrias de Madeira", items:[
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a existência de fungos, mofos, bolores e focos de insetos e tratar quando necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"No caso de esquadrias envernizadas, realizar tratamento com verniz",resp:"capacitada",obs:"Empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar falhas de vedação e fixação das esquadrias e reconstituir sua integridade; reapertar parafusos aparentes e regular freio e lubrificação",resp:"capacitada",obs:"Empresa capacitada"},
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Verificar e, se necessário, pintar, encerar, envernizar ou executar tratamento recomendado pelo fornecedor das esquadrias de madeira",resp:"mixed",obs:"Equipe local / empresa especializada"},
  ]},
  { id:"esquadrias-ferro", icon:"🔩", name:"Esquadrias de Ferro e Aço", items:[
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar as esquadrias para identificação de pontos de oxidação e, se necessário, proceder reparos",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar e, se necessário, executar serviços com as mesmas especificações da pintura original; verificar vedação e fixação de vidros",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar inspeção das condições de fixação e solidez do guarda-corpo, corrimão e barras, reconstituir onde necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"esquadrias-aluminio", icon:"🔲", name:"Esquadrias de Alumínio", items:[
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Efetuar limpeza geral, regulagem, lubrificação e desobstrução dos drenos nos trilhos inferiores, mecanismos de fechamento e demais componentes",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Reapertar os parafusos aparentes de fechos, fechaduras, puxadores e roldanas; verificar janelas Maxim-ar",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar vedação e fixação dos vidros; verificar a presença de falhas na vedação e fixação nos caixilhos",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar inspeção das condições de fixação e solidez do guarda-corpo, corrimão e barras",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"estrutura", icon:"🏗️", name:"Estrutura (Fundações, Pilares, Vigas, Lajes)", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificar integridade estrutural (fundações, estrutura principal, estruturas periféricas, contenções, arrimos, guarda-corpos, muros de divisa)",resp:"especializada",obs:"Empresa especializada. Garantia estrutural: 5 anos"},
  ]},
  { id:"alvenaria", icon:"🧱", name:"Alvenaria de Vedação e Paredes", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificar integridade estrutural das paredes de vedação, estruturas auxiliares e de cobertura, escadarias, guarda-corpos e telhados",resp:"especializada",obs:"Empresa especializada. Garantia de segurança e integridade: 5 anos"},
  ]},
  { id:"fachada", icon:"🏢", name:"Revestimento Externo e Fachada", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade e reconstituir juntas (frisos), mastiques, rejuntes, borrachas e selantes da fachada. Verificar calafetação, fixação e estado geral de rufos, para-raios, antenas, esquadrias e elementos decorativos",resp:"mixed",obs:"Equipe local / empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade e reconstituir os rejuntamentos externos, peitoris, chaminés e grelhas de ventilação",resp:"mixed",obs:"Equipe local / empresa capacitada / empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Verificar a presença de fissuras, rachaduras, desgastes excessivos com mapeamento de áreas soltas ou com som cavo",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Nos revestimentos externos e fachada: repintura, com lavagem e tratamento de fissuras precedentes",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Antes de cada uso / Anual",desc:"Inspecionar visualmente os pontos de ancoragem da fachada (corrosão, deformação, trincas e desgaste) conforme NBR 16325-1",resp:"mixed",obs:"Antes de cada uso: equipe local. Anual: empresa especializada"},
  ]},
  { id:"revestimento-parede", icon:"🖌️", name:"Revestimento de Paredes e Tetos (Argamassa, Gesso, Forro)", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Repintar os forros dos banheiros e áreas úmidas; verificar a calafetação e fixação de rufos, para-raios, antenas e elementos decorativos",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Revisar a pintura das áreas secas e, se necessário, repintá-las, evitando envelhecimento, perda de brilho e descascamento",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Repintar paredes e tetos das áreas secas",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"revestimento-ceramico", icon:"🔷", name:"Revestimento Cerâmico (Pisos e Paredes)", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificar e, se necessário, efetuar manutenções para manter a estanqueidade do sistema; verificar integridade e reconstituir os rejuntamentos",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"pedras", icon:"💎", name:"Revestimentos de Pedras Naturais (Mármore, Granito)", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"No caso de peças polidas, verificar a integridade do polimento e, se necessário, encerar. Em áreas de circulação intensa, encerar com maior frequência",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a calafetação de rufos, fixação de para-raios, antenas e elementos decorativos. Verificar a integridade e reconstituir rejuntamentos; verificar juntas de dilatação (preencher com mastique, nunca argamassa)",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"assoalho", icon:"🌲", name:"Assoalhos e Deck de Madeira", items:[
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a existência de fungos, mofos, bolores e focos de insetos e tratar quando necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar e, se necessário, refazer a calafetação das juntas dos assoalhos de madeira",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Revisar a camada protetora do deck (verniz, selante etc.) e, se necessária, remover e refazer para retornar ao desempenho inicialmente planejado",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"pinturas", icon:"🎨", name:"Pinturas, Texturas e Vernizes (Interna e Externa)", items:[
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Revisar a pintura das áreas secas e, se necessário, repintá-las, evitando envelhecimento, perda de brilho, descascamento e fissuras",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Repintar paredes e tetos das áreas secas com as mesmas especificações da pintura original",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"trianual",freqLabel:"A cada 3 anos",desc:"Revisar e, se necessário, repintar as áreas externas",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"vidros", icon:"🪟", name:"Vidros", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Nos locais com vidros temperados, efetuar inspeção do funcionamento do sistema de molas e dobradiças e verificar a necessidade de lubrificação",resp:"especializada",obs:"Empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar o desempenho das vedações e fixações dos vidros nos caixilhos",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"quadra", icon:"🏸", name:"Infraestrutura para Prática Recreativa — Quadra", items:[
    {freq:"bimestral",freqLabel:"A cada 2 meses",desc:"Executar a manutenção do jardim próximo à quadra para evitar problemas de drenagem e impedir que raízes se infiltrem sob o piso",resp:"local"},
    {freq:"trimestral",freqLabel:"Trimestral",desc:"Verificar a existência de oxidação das partes metálicas e repintar quando necessário; verificar equipamentos de regulagem, fixação, aperto, folgas e conservação",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Realizar lixamento e aplicação de tintas quando necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Pintar os equipamentos esportivos ou quando a camada de tinta for danificada pelo uso, evitando oxidações",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"bianual",freqLabel:"A cada 2 anos",desc:"Esticar as telas da quadra onde necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"trianual",freqLabel:"A cada 3 anos (ou quando necessário)",desc:"Repintar a superfície de pisos de concreto polido pintado em função do uso da quadra",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
  ]},
  { id:"jardins", icon:"🌿", name:"Jardins", items:[
    {freq:"diaria",freqLabel:"Diária (verão)",desc:"Regar, preferencialmente no início da manhã ou final da tarde, molhando inclusive as folhas",resp:"local"},
    {freq:"diaria",freqLabel:"A cada 2 dias (inverno)",desc:"Regar, preferencialmente no início da manhã ou final da tarde",resp:"local"},
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar o funcionamento dos dispositivos de irrigação",resp:"local"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Executar a manutenção geral do jardim: limpeza, retirada de folhas velhas, galhos secos e detritos",resp:"mixed",obs:"Equipe local / jardineiro qualificado"},
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar e controlar a presença de pragas, ervas daninhas, plantas invasivas, raízes mortas e torrões de terra seca",resp:"mixed",obs:"Equipe local / jardineiro qualificado"},
    {freq:"semestral",freqLabel:"A cada 45 dias (ou quando altura atingir 5cm)",desc:"Cortar a grama e realizar limpeza (remoção de galhos e folhas secas)",resp:"mixed",obs:"Equipe local / jardineiro qualificado"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar o replantio de mudas e a cobertura para grama e jardins com terra adubada, de preferência no inverno",resp:"mixed",obs:"Equipe local / jardineiro qualificado"},
  ]},
  { id:"playground", icon:"🛝", name:"Área de Recreação Infantil (Playground)", items:[
    {freq:"mensal",freqLabel:"Mensal",desc:"Verificar a integridade dos brinquedos: superfícies cortantes, lascas, parafusos soltos, encaixes folgados, rachaduras, partes metálicas oxidadas, descascamento de pintura e falta de componentes",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Realizar vistoria de responsabilidade técnica, verificando todos os requisitos de segurança listados na ABNT NBR 16071-7",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Lixar e pintar com zarcão e tinta à base de esmalte as partes metálicas oxidadas (parafusos, correntes de balanços)",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar, tratar e, se necessário, recuperar as características originais dos brinquedos de madeira",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"piscina", icon:"🏊", name:"Piscina", items:[
    {freq:"diaria",freqLabel:"Diária",desc:"Passar a peneira na água e aspirar sujeiras depositadas no fundo da piscina",resp:"local"},
    {freq:"semanal",freqLabel:"Semanal",desc:"Lavar o filtro da piscina",resp:"local"},
    {freq:"semanal",freqLabel:"Semanal",desc:"Verificar vazamentos e ruídos nas bombas da piscina",resp:"local"},
    {freq:"semanal",freqLabel:"Semanal",desc:"Efetuar retrolavagem e remoção de eventuais eflorescências",resp:"local"},
    {freq:"semanal",freqLabel:"Semanal",desc:"Controlar o pH da água da piscina",resp:"local"},
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a estanqueidade das luminárias submersas da piscina",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar o estado do rejuntamento e a integridade das juntas, cerâmicas, porcelanatos e juntas estruturais; verificar fissuras e revestimentos soltos",resp:"local"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade estrutural dos sistemas de impermeabilização e reconstituir a proteção mecânica, sinais de infiltrações ou falhas da impermeabilização exposta",resp:"local"},
  ]},
  { id:"climatizador-piscina", icon:"🌡️", name:"Climatizadores de Água da Piscina", items:[
    {freq:"anual",freqLabel:"Anual",desc:"Verificação completa do sistema dos climatizadores de água da piscina, seguindo as instruções do manual do fabricante",resp:"mixed",obs:"Equipe local / empresa capacitada"},
  ]},
  { id:"cobertura", icon:"🏛️", name:"Cobertura (Laje Impermeabilizada e Rufos)", items:[
    {freq:"semestral",freqLabel:"Semestral",desc:"Verificar a integridade dos protetores térmicos e efetuar limpeza e reparos para garantir a funcionalidade. Em épocas de chuvas fortes, inspecionar as calhas semanalmente",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a integridade estrutural dos componentes, vedações, fixações e reconstituir e tratar onde necessário",resp:"mixed",obs:"Empresa capacitada / empresa especializada"},
    {freq:"anual",freqLabel:"Anual",desc:"Nas lajes expostas: verificar e eliminar a presença de pragas, ervas daninhas, plantas invasivas e raízes; aplicar herbicida se necessário",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a calafetação e fixação de rufos, calhas, antenas, esquadrias, esticadores, elementos fixadores e isolantes; reconstituir rejuntamentos e juntas de dilatação",resp:"mixed",obs:"Equipe local / empresa capacitada"},
    {freq:"anual",freqLabel:"Anual",desc:"Verificar a presença de danos (rasgos, perfurações, descolamentos e fissuras) na camada impermeabilizante causados por impactos mecânicos ou trânsito de pessoas",resp:"local",obs:"Equipe local / empresa capacitada"},
  ]},
];

function getFreqClass(f) {
  const m={diaria:'freq-diaria',semanal:'freq-semanal',quinzenal:'freq-quinzenal',mensal:'freq-mensal',bimestral:'freq-bimestral',trimestral:'freq-trimestral',quadrimestral:'freq-quadrimestral',semestral:'freq-semestral',anual:'freq-anual',bianual:'freq-bianual',trianual:'freq-trianual'};
  return m[f]||'freq-mensal';
}
function getRespClass(r){return{local:'resp-local',capacitada:'resp-cap',especializada:'resp-espec',mixed:'resp-mixed'}[r]||'resp-mixed';}
function getRespLabel(r){return{local:'Equipe Local',capacitada:'Empresa Capacitada',especializada:'Empresa Especializada',mixed:'Ver observação'}[r]||r;}

function render(){
  const c=document.getElementById('mainContent'); let n=0;
  c.innerHTML=data.map(cat=>{n+=cat.items.length;
    return`<div class="category-block" id="${cat.id}">
      <div class="cat-header" onclick="toggleCat('${cat.id}')">
        <div class="cat-icon">${cat.icon}</div>
        <div class="cat-info">
          <div class="cat-name">${cat.name}</div>
          <div class="cat-count">${cat.items.length} item${cat.items.length>1?'s':''} de manutenção</div>
        </div>
        <span class="cat-chevron">›</span>
      </div>
      <div class="items-table" id="table-${cat.id}">
        <table>
          <thead><tr><th style="width:55%">Atividade</th><th style="width:22%">Periodicidade</th><th style="width:23%">Responsável</th></tr></thead>
          <tbody>${cat.items.map(item=>`
            <tr class="item-row" data-freq="${item.freq}" data-text="${(item.desc+(item.obs||'')).toLowerCase()}">
              <td><div>${item.desc}</div>${item.obs?`<div class="item-obs">ℹ ${item.obs}</div>`:''}</td>
              <td><span class="freq-badge ${getFreqClass(item.freq)}">${item.freqLabel}</span></td>
              <td><span class="resp"><span class="resp-dot ${getRespClass(item.resp)}"></span>${getRespLabel(item.resp)}</span></td>
            </tr>`).join('')}
          </tbody>
        </table>
      </div>
    </div>`;
  }).join('');
  document.getElementById('totalItems').textContent=n;
  document.getElementById('totalCats').textContent=data.length;
}

function toggleCat(id){
  const t=document.getElementById('table-'+id), h=document.querySelector(`#${id} .cat-header`);
  t.classList.toggle('open'); h.classList.toggle('open');
}

let activeFreq='todos', searchText='';
function applyFilters(){
  data.forEach(cat=>{
    const block=document.getElementById(cat.id), rows=block.querySelectorAll('.item-row');
    let any=false;
    rows.forEach(row=>{
      const v=(activeFreq==='todos'||row.dataset.freq===activeFreq)&&(!searchText||row.dataset.text.includes(searchText));
      row.classList.toggle('row-hidden',!v); if(v) any=true;
    });
    block.classList.toggle('cat-hidden',!any);
    if(any&&(activeFreq!=='todos'||searchText)){
      document.getElementById('table-'+cat.id).classList.add('open');
      block.querySelector('.cat-header').classList.add('open');
    }
  });
}

document.addEventListener('DOMContentLoaded',()=>{
  render();
  document.querySelectorAll('.chip').forEach(chip=>{
    chip.addEventListener('click',()=>{
      document.querySelectorAll('.chip').forEach(c=>c.classList.remove('active'));
      chip.classList.add('active'); activeFreq=chip.dataset.freq; applyFilters();
    });
  });
  document.getElementById('searchInput').addEventListener('input',e=>{
    searchText=e.target.value.toLowerCase().trim(); applyFilters();
  });
});
</script>
</body>
</html>
