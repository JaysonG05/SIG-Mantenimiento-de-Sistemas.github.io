<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mantenimiento de Sistemas — Caso Chamilo Offline</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Literata:ital,opsz,wght@0,7..72,400;0,7..72,500;0,7..72,600;1,7..72,400&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EDEFE8;
    --paper-2:#E2E5DC;
    --ink:#12261C;
    --ink-soft:#3B4B41;
    --signal:#2FAE7A;
    --signal-dim:#B7D9C9;
    --copper:#C9812E;
    --teal:#2B5D63;
    --line:#c7ccc0;
    --card:#F7F8F3;
    --danger:#B5432A;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Literata', serif; line-height:1.65;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.mono,.eyebrow,nav,.tag,.btn,.card-h,.node-label{font-family:'Space Grotesk',sans-serif;}
  .mono, .term{font-family:'JetBrains Mono', monospace;}

  /* subtle grid backdrop like graph paper / field notebook */
  .grid-bg{
    background-image:
      linear-gradient(var(--line) 1px, transparent 1px),
      linear-gradient(90deg, var(--line) 1px, transparent 1px);
    background-size: 34px 34px;
    background-position: -1px -1px;
    opacity:0.35;
    position:absolute; inset:0; pointer-events:none;
  }

  nav{
    position:sticky; top:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:16px 6vw; background:rgba(237,239,232,0.88); backdrop-filter:blur(6px);
    border-bottom:1px solid var(--line);
  }
  .brand{display:flex; align-items:center; gap:10px; font-weight:700; letter-spacing:0.02em; font-size:15px;}
  .brand .dot{width:9px;height:9px;border-radius:50%;background:var(--signal); box-shadow:0 0 0 0 rgba(47,174,122,.6); animation:ping 2.2s infinite;}
  @keyframes ping{
    0%{box-shadow:0 0 0 0 rgba(47,174,122,.55);}
    70%{box-shadow:0 0 0 8px rgba(47,174,122,0);}
    100%{box-shadow:0 0 0 0 rgba(47,174,122,0);}
  }
  nav a{color:var(--ink-soft); text-decoration:none; font-size:13px; margin-left:22px;}
  nav a:hover{color:var(--copper);}
  .nav-links{display:flex;}
  @media (max-width:780px){ .nav-links{display:none;} }

  section{padding:96px 6vw; position:relative; max-width:1180px; margin:0 auto;}
  .eyebrow{
    display:inline-flex; align-items:center; gap:8px;
    font-size:12px; letter-spacing:0.14em; text-transform:uppercase;
    color:var(--teal); font-weight:600; margin-bottom:18px;
  }
  .eyebrow::before{content:'';width:22px;height:1px;background:var(--copper);}
  h2{font-size:clamp(28px,3.6vw,42px); margin:0 0 22px; font-weight:600; letter-spacing:-0.01em;}
  p{max-width:74ch; color:var(--ink-soft); font-size:17px;}
  .lead{font-size:19px; max-width:80ch;}

  /* HERO */
  .hero{
    min-height:92vh; display:flex; align-items:center; padding-top:60px; overflow:hidden;
  }
  .hero-grid{display:grid; grid-template-columns:1.1fr 1fr; gap:48px; align-items:center; width:100%;}
  @media (max-width:900px){ .hero-grid{grid-template-columns:1fr;} }
  .hero h1{
    font-size:clamp(38px,5.6vw,64px); line-height:1.03; margin:0 0 20px; font-weight:700; letter-spacing:-0.02em;
  }
  .hero h1 em{font-style:normal; color:var(--teal); position:relative;}
  .hero-sub{font-size:18px; color:var(--ink-soft); max-width:52ch; margin-bottom:30px;}
  .case-pill{
    display:inline-flex; align-items:center; gap:10px; background:var(--card); border:1px solid var(--line);
    border-radius:100px; padding:8px 16px 8px 8px; font-size:13px; margin-bottom:12px;
  }
  .case-pill.copper{ margin-bottom:26px; }
  .case-pill .badge{background:var(--ink); color:var(--paper); border-radius:100px; padding:4px 10px; font-size:11px; font-weight:700;}
  .case-pill .badge.copper-badge{background:var(--copper); color:#2b1a05;}
  .cta-row{display:flex; gap:14px; flex-wrap:wrap;}
  .btn{
    border:1px solid var(--ink); background:var(--ink); color:var(--paper); padding:12px 22px; border-radius:8px;
    font-size:14px; font-weight:600; cursor:pointer; text-decoration:none; display:inline-block;
    transition:transform .15s ease, background .15s ease;
  }
  .btn:hover{transform:translateY(-2px); background:var(--teal);}
  .btn.ghost{background:transparent; color:var(--ink); border:1px solid var(--ink);}
  .btn.ghost:hover{background:var(--ink); color:var(--paper);}

  /* NETWORK DIAGRAM (signature element) */
  .netbox{position:relative; aspect-ratio:1/1; max-width:460px; margin:0 auto;}
  .netbox svg{width:100%; height:100%; overflow:visible;}
  .link-line{stroke:var(--signal-dim); stroke-width:2; fill:none;}
  .link-pulse{stroke:var(--signal); stroke-width:2.4; fill:none; stroke-dasharray:8 240; stroke-linecap:round;
    animation:flow 3.6s linear infinite;}
  @keyframes flow{ to{ stroke-dashoffset:-248; } }
  .node{fill:var(--card); stroke:var(--ink); stroke-width:1.4;}
  .node-server{fill:var(--ink);}
  .node-label{font-size:9px; fill:var(--ink-soft); font-weight:600;}
  .pulse-dot{fill:var(--signal); opacity:0; animation:appear 3.6s linear infinite;}

  /* TIPOS DE SISTEMAS */
  .sys-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(210px,1fr)); gap:16px; margin-top:34px;}
  .sys-card{
    background:var(--card); border:1px solid var(--line); border-radius:12px; padding:22px;
    transition:transform .2s ease, box-shadow .2s ease; position:relative;
  }
  .sys-card:hover{transform:translateY(-4px); box-shadow:0 10px 26px rgba(18,38,28,0.08);}
  .sys-card h3{font-size:16px; margin:0 0 8px; font-weight:600;}
  .sys-card p{font-size:14.5px; margin:0; max-width:none;}
  .sys-card.highlight{border-color:var(--signal); background:linear-gradient(180deg, rgba(47,174,122,0.08), var(--card) 40%);}
  .sys-card.highlight::after{
    content:'CASO REAL · CHAMILO'; position:absolute; top:-10px; right:16px; background:var(--signal); color:#08231a;
    font-family:'JetBrains Mono',monospace; font-size:10px; font-weight:700; padding:3px 8px; border-radius:5px; letter-spacing:.05em;
  }
  .sys-card.highlight-copper{border-color:var(--copper); background:linear-gradient(180deg, rgba(201,129,46,0.10), var(--card) 40%);}
  .sys-card.highlight-copper::after{
    content:'CASO REAL · TECNIFIX'; position:absolute; top:-10px; right:16px; background:var(--copper); color:#2b1a05;
    font-family:'JetBrains Mono',monospace; font-size:10px; font-weight:700; padding:3px 8px; border-radius:5px; letter-spacing:.05em;
  }

  /* TIMELINE */
  .timeline{margin-top:50px; position:relative;}
  .timeline-track{
    display:grid; grid-template-columns:repeat(4,1fr); gap:0; position:relative;
  }
  .timeline-track::before{
    content:''; position:absolute; top:17px; left:0; right:0; height:2px; background:var(--line); z-index:0;
  }
  .t-step{position:relative; z-index:1; padding-right:18px;}
  .t-num{
    width:36px; height:36px; border-radius:50%; background:var(--paper); border:2px solid var(--ink);
    display:flex; align-items:center; justify-content:center; font-family:'JetBrains Mono',monospace; font-weight:700; font-size:13px;
    margin-bottom:16px;
  }
  .t-step.active .t-num{background:var(--signal); border-color:var(--signal); color:#08231a;}
  .t-step.copper-step .t-num{background:var(--copper); border-color:var(--copper); color:#2b1a05;}
  .eyebrow.copper-eyebrow{color:var(--copper);}
  .eyebrow.copper-eyebrow::before{background:var(--teal);}
  .t-step h4{font-size:14.5px; margin:0 0 6px; font-weight:600;}
  .t-step p{font-size:13.5px; margin:0;}
  @media (max-width:820px){ .timeline-track{grid-template-columns:1fr; gap:28px;} .timeline-track::before{display:none;} }

  /* MAINTENANCE CARDS */
  .maint-grid{display:grid; grid-template-columns:repeat(2,1fr); gap:20px; margin-top:36px;}
  @media (max-width:780px){ .maint-grid{grid-template-columns:1fr;} }
  .maint-card{
    background:var(--card); border:1px solid var(--line); border-radius:14px; padding:26px; position:relative; overflow:hidden;
  }
  .maint-card .tag{
    display:inline-block; font-size:11px; letter-spacing:.08em; text-transform:uppercase; font-weight:700;
    padding:4px 10px; border-radius:6px; margin-bottom:14px;
  }
  .tag.correctivo{background:#F3D9CF; color:#7A2E15;}
  .tag.adaptativo{background:#D9E6D2; color:#33501F;}
  .tag.perfectivo{background:#D3E3E4; color:#1F4547;}
  .tag.preventivo{background:#EDE0C4; color:#6B4C10;}
  .maint-card h3{font-size:19px; margin:0 0 10px;}
  .maint-card p{font-size:14.5px;}
  .term{
    margin-top:14px; background:#0E1B14; color:#8FE3B7; padding:14px; border-radius:8px; font-size:12px;
    overflow-x:auto; white-space:pre; line-height:1.55;
  }
  .term .warn{color:#F0A868;}
  .mini-case{
    margin-top:14px; padding-top:14px; border-top:1px dashed var(--line);
    font-size:13.5px !important; color:var(--ink-soft);
  }
  .mini-case strong{color:var(--copper);}

  /* PROBLEMAS */
  .prob-list{margin-top:34px; display:flex; flex-direction:column; gap:0;}
  .prob-item{
    display:grid; grid-template-columns:44px 1fr; gap:18px; padding:22px 0; border-bottom:1px solid var(--line);
  }
  .prob-item:first-child{border-top:1px solid var(--line);}
  .prob-num{font-family:'JetBrains Mono',monospace; color:var(--copper); font-weight:700; font-size:15px;}
  .prob-item h4{margin:0 0 6px; font-size:16.5px; font-weight:600; display:flex; align-items:center; gap:10px; flex-wrap:wrap;}
  .prob-item p{margin:0; font-size:14.5px;}
  .case-tag{
    font-family:'JetBrains Mono',monospace; font-size:9.5px; font-weight:700; letter-spacing:.06em; text-transform:uppercase;
    background:var(--signal-dim); color:#0d3d29; padding:2px 8px; border-radius:5px;
  }
  .case-tag.copper{ background:#F0DAB9; color:#5c3c0c; }

  /* VIDEO */
  .video-wrap{
    margin-top:34px; border-radius:16px; overflow:hidden; border:1px solid var(--line);
    aspect-ratio:16/9; background:#0E1B14;
  }
  .video-wrap iframe{width:100%; height:100%; border:0; display:block;}

  /* AUDIO */
  .audio-card{
    margin-top:34px; background:var(--ink); color:var(--paper); border-radius:16px; padding:32px;
    display:grid; grid-template-columns:auto 1fr auto; align-items:center; gap:24px;
  }
  @media (max-width:700px){ .audio-card{grid-template-columns:1fr; text-align:center;} }
  .play-btn{
    width:58px; height:58px; border-radius:50%; border:2px solid var(--signal); background:transparent; color:var(--signal);
    font-size:20px; cursor:pointer; display:flex; align-items:center; justify-content:center; transition:background .15s;
  }
  .play-btn:hover{background:rgba(47,174,122,0.15);}
  .bars{display:flex; align-items:center; gap:4px; height:36px;}
  .bars span{
    width:4px; background:var(--signal); border-radius:2px; height:6px; opacity:0.65;
    transition:height .1s ease;
  }
  .audio-label{font-size:12px; color:#9db4a7; font-family:'JetBrains Mono',monospace;}

  footer{
    padding:56px 6vw 40px; border-top:1px solid var(--line); font-size:13px; color:var(--ink-soft);
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:14px;
  }
  .fade-up{opacity:0; transform:translateY(18px); transition:opacity .6s ease, transform .6s ease;}
  .fade-up.in{opacity:1; transform:translateY(0);}
</style>
</head>
<body>

<nav>
  <div class="brand"><span class="dot"></span> SIG · Mantenimiento de Sistemas</div>
  <div class="nav-links">
    <a href="#tipos">Tipos de sistemas</a>
    <a href="#ciclo">Ciclo de vida</a>
    <a href="#tipos-mant">Mantenimiento</a>
    <a href="#problemas">Problemas</a>
    <a href="#caso">Video</a>
  </div>
</nav>

<section class="hero">
  <div class="hero-grid">
    <div>
      <div class="case-pill"><span class="badge">CASO REAL 1</span> Chamilo 2.0.2 offline · Laragon · LAN · Bocas del Toro</div>
      <div class="case-pill copper"><span class="badge copper-badge">CASO REAL 2</span> Tecnifix · React · Supabase · Changuinola</div>
      <h1>Mantener un sistema<br><em>es lo que lo mantiene vivo.</em></h1>
      <p class="hero-sub">El ciclo de vida, las técnicas, la importancia y los tipos de mantenimiento de sistemas, explicados a partir de dos proyectos reales: un LMS sin Internet en un aula rural, y una plataforma web de técnicos a domicilio — ambos desarrollados por el autor.</p>
      <div class="cta-row">
        <a href="#tipos" class="btn">Explorar el caso →</a>
        <a href="#caso" class="btn ghost">Ver video</a>
      </div>
    </div>
    <div class="netbox" aria-hidden="true">
      <svg viewBox="0 0 300 300">
        <g id="lines"></g>
        <circle class="node node-server" cx="150" cy="150" r="20"></circle>
        <text x="150" y="154" text-anchor="middle" font-size="9" fill="#EDEFE8" font-family="JetBrains Mono" font-weight="700">SRV</text>
        <g id="nodes"></g>
      </svg>
    </div>
  </div>
</section>

<section id="tipos">
  <div class="eyebrow fade-up">A · Mantenimiento de sistemas</div>
  <h2 class="fade-up">2.1 Tipos de sistemas</h2>
  <p class="lead fade-up">Antes de mantener algo hay que saber qué es. Los sistemas de información se agrupan según la función que cumplen — y, cada vez más, según si dependen o no de una conexión permanente a Internet.</p>
  <div class="sys-grid">
    <div class="sys-card fade-up"><h3>TPS</h3><p>Procesamiento de transacciones: ventas, inventario, matrícula — operaciones diarias y repetitivas.</p></div>
    <div class="sys-card fade-up"><h3>MIS / DSS</h3><p>Información gerencial y soporte a decisiones: convierten datos operativos en reportes útiles.</p></div>
    <div class="sys-card fade-up"><h3>ERP</h3><p>Sistemas empresariales que integran múltiples procesos administrativos en una sola plataforma.</p></div>
    <div class="sys-card fade-up"><h3>Embebidos / tiempo real</h3><p>Operan dentro de hardware específico, con restricciones estrictas de tiempo de respuesta.</p></div>
    <div class="sys-card highlight fade-up">
      <h3>LMS local (Chamilo)</h3>
      <p>Sistema de gestión de aprendizaje reclasificado de "cliente-servidor en la nube" a <strong>sistema local de red LAN</strong>: una laptop con Laragon sirve a 196 estudiantes sin Internet.</p>
    </div>
    <div class="sys-card highlight-copper fade-up">
      <h3>Marketplace en línea (Tecnifix)</h3>
      <p>Sistema transaccional de tipo mercado: React + Node/Express + Supabase conectan clientes y técnicos de Changuinola con geolocalización, catálogos y <strong>pagos electrónicos</strong> — el polo opuesto de Chamilo: centralizado y dependiente de conexión.</p>
    </div>
  </div>
</section>

<section id="ciclo">
  <div class="eyebrow fade-up">A · Mantenimiento de sistemas</div>
  <h2 class="fade-up">2.2 Cambios durante el ciclo de vida</h2>
  <p class="lead fade-up">Ningún sistema real avanza en línea recta por planificación → análisis → diseño → implementación → pruebas → mantenimiento. Los requisitos cambian en el camino. Así se reordenó el proyecto Chamilo cuando pasó de un despliegue en línea a uno completamente offline:</p>
  <div class="timeline">
    <div class="eyebrow fade-up" style="margin-bottom:10px;">Chamilo 2.0.2 offline</div>
    <div class="timeline-track">
      <div class="t-step active fade-up">
        <div class="t-num">01</div>
        <h4>Planificación y carga de datos</h4>
        <p>Creación de 7 grupos y registro de 196 estudiantes dentro de Chamilo.</p>
      </div>
      <div class="t-step active fade-up">
        <div class="t-num">02</div>
        <h4>Configuración del servidor portátil</h4>
        <p>Laragon levanta Apache, MySQL y Symfony en una laptop, sin depender de la nube.</p>
      </div>
      <div class="t-step active fade-up">
        <div class="t-num">03</div>
        <h4>Despliegue de la red LAN</h4>
        <p>IP estática al servidor; los estudiantes se conectan por navegador, sin Internet.</p>
      </div>
      <div class="t-step active fade-up">
        <div class="t-num">04</div>
        <h4>Pruebas de estrés y validación</h4>
        <p>Acceso concurrente simulado para medir rendimiento del procesador y del router.</p>
      </div>
    </div>

    <div class="eyebrow fade-up copper-eyebrow" style="margin:44px 0 10px;">Tecnifix</div>
    <div class="timeline-track">
      <div class="t-step active copper-step fade-up">
        <div class="t-num">01</div>
        <h4>Diagnóstico de necesidades</h4>
        <p>Observación directa de cómo se contrata "boca en boca" a los técnicos en Changuinola.</p>
      </div>
      <div class="t-step active copper-step fade-up">
        <div class="t-num">02</div>
        <h4>Diseño de arquitectura</h4>
        <p>React + Node/Express + Supabase, con RLS y esquema relacional en PostgreSQL.</p>
      </div>
      <div class="t-step active copper-step fade-up">
        <div class="t-num">03</div>
        <h4>Implementación del MVP</h4>
        <p>A mitad de esta fase, el técnico pasó de ofrecer un solo servicio a una relación muchos-a-muchos con categorías.</p>
      </div>
      <div class="t-step active copper-step fade-up">
        <div class="t-num">04</div>
        <h4>Evaluación de viabilidad</h4>
        <p>Prueba piloto con técnicos y usuarios reales de la zona.</p>
      </div>
    </div>
  </div>
</section>

<section id="tipos-mant">
  <div class="eyebrow fade-up">A · Mantenimiento de sistemas</div>
  <h2 class="fade-up">2.3 Actividades o tipos de mantenimiento</h2>
  <p class="lead fade-up">La norma ISO/IEC 14764 distingue cuatro tipos. Los cuatro aparecen, con evidencia real, tanto en el servidor rural de Bocas del Toro como en la plataforma en línea de Changuinola.</p>
  <div class="maint-grid">
    <div class="maint-card fade-up">
      <span class="tag correctivo">Correctivo</span>
      <h3>Corrige defectos ya presentes</h3>
      <p>El log real del servidor Laragon, durante la carga de los 196 estudiantes, mostró funciones obsoletas de Chamilo ejecutándose sobre PHP moderno:</p>
      <div class="term">Deprecated: trim(): Passing null to parameter #1
($string) of type string is deprecated
  groupmanager.lib.php on line 2329
<span class="warn">Deprecated: usort(): Returning bool from
comparison function is deprecated</span>
  table_sort.class.php on line 240</div>
      <p class="mini-case"><strong>Tecnifix:</strong> conflictos reales entre políticas RLS que impedían al administrador editar perfiles de técnicos, y errores de compatibilidad con el cliente v2 de Supabase.</p>
    </div>
    <div class="maint-card fade-up">
      <span class="tag adaptativo">Adaptativo</span>
      <h3>Adapta el sistema a un nuevo entorno</h3>
      <p>Chamilo fue pensado para la nube. Reconfigurar PHP, MySQL y Symfony en Laragon para que corriera completamente offline, sobre una sola laptop, es mantenimiento adaptativo puro.</p>
      <p class="mini-case"><strong>Tecnifix:</strong> arquitectura adaptada a conectividad limitada, con capacidades offline mediante caché local para las zonas de Changuinola con conexión inestable.</p>
    </div>
    <div class="maint-card fade-up">
      <span class="tag perfectivo">Perfectivo</span>
      <h3>Mejora sin que exista una falla</h3>
      <p>Tras las pruebas de estrés con los 7 grupos conectados a la vez, se ajustó el caché para lograr navegación fluida — el sistema ya funcionaba, solo se optimizó.</p>
      <p class="mini-case"><strong>Tecnifix:</strong> rediseño de técnico–categoría de uno-a-uno a muchos-a-muchos, y recibos en PDF con numeración automática CP-AAAA-NNNNN.</p>
    </div>
    <div class="maint-card fade-up">
      <span class="tag preventivo">Preventivo</span>
      <h3>Actúa antes del problema</h3>
      <p>Asignar una IP estática a la laptop-servidor y parametrizar la seguridad básica del router, antes de que existieran conflictos de red o accesos no autorizados.</p>
      <p class="mini-case"><strong>Tecnifix:</strong> políticas RLS que limitan permisos elevados solo al rol admin, y contrato digital con hash SHA-256 + IP + timestamp como evidencia preventiva ante disputas.</p>
    </div>
  </div>
</section>

<section id="problemas">
  <div class="eyebrow fade-up">A · Mantenimiento de sistemas</div>
  <h2 class="fade-up">2.4 Problemas de mantenimiento</h2>
  <p class="lead fade-up">Mantener un sistema no es solo un tema de código. Los propios autores de ambos proyectos documentan limitaciones reales del entorno:</p>
  <div class="prob-list">
    <div class="prob-item fade-up">
      <div class="prob-num">01</div>
      <div><h4>Sin acceso remoto <span class="case-tag">Chamilo</span></h4><p>La red es estrictamente local: cualquier falla exige presencia física en un sitio de difícil acceso como Bocas del Toro.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">02</div>
      <div><h4>Dependencia eléctrica <span class="case-tag">Chamilo</span></h4><p>Un solo servidor portátil sostiene a los 196 usuarios; un corte de energía prolongado detiene toda la plataforma.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">03</div>
      <div><h4>Personal técnico reducido <span class="case-tag">Chamilo</span></h4><p>La baja competencia digital docente incrementa la carga de mantenimiento correctivo diario.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">04</div>
      <div><h4>Deuda técnica acumulada <span class="case-tag">Chamilo</span></h4><p>Las funciones obsoletas de PHP seguirán apareciendo con cada actualización del lenguaje mientras el código base no se actualice.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">05</div>
      <div><h4>Pruebas limitadas a pocos usuarios <span class="case-tag copper">Tecnifix</span></h4><p>Los propios autores señalan la necesidad de ampliar las pruebas con más usuarios reales antes de escalar la plataforma.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">06</div>
      <div><h4>Validación de fotos poco robusta <span class="case-tag copper">Tecnifix</span></h4><p>La calidad de las fotos de comprobantes o certificados depende de la fuente original, lo que exige revisión manual adicional.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">07</div>
      <div><h4>Conectividad variable <span class="case-tag copper">Tecnifix</span></h4><p>En zonas de baja conectividad de Changuinola, el tiempo de carga de la aplicación puede variar de forma notable.</p></div>
    </div>
    <div class="prob-item fade-up">
      <div class="prob-num">08</div>
      <div><h4>Mantenimiento continuo pendiente <span class="case-tag copper">Tecnifix</span></h4><p>Los autores mismos recomiendan documentar cada versión con rigor y fortalecer las pruebas de seguridad como trabajo futuro.</p></div>
    </div>
  </div>
</section>

<section id="caso">
  <div class="eyebrow fade-up">Recurso audiovisual</div>
  <h2 class="fade-up">El ciclo de vida, en video</h2>
  <p class="lead fade-up">Un repaso visual del ciclo de vida de desarrollo de software — la base teórica detrás de las cuatro fases que también vivió el proyecto Chamilo.</p>
  <div class="video-wrap fade-up">
    <iframe src="https://youtu.be/TLVDBAo1aEY" title="Ciclo de vida de desarrollo de software" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>

  <div class="audio-card fade-up">
    <button class="play-btn" id="playBtn" aria-label="Reproducir sonido de red">▶</button>
    <div>
      <div style="font-weight:600; margin-bottom:4px;">Pulso de una red LAN activa</div>
      <div class="audio-label">SIMULACIÓN · 196 dispositivos sincronizando con el servidor local</div>
    </div>
    <div class="bars" id="bars"></div>
  </div>
</section>

<footer>
  <div>© 2026 Jayson O. Grant — Proyecto Final, Ingeniería de Software Aplicada 2 · UTP</div>
  <div>Casos reales: Guerra, Grant &amp; Caballero, «Chamilo 2.0.2 offline» · Mitre, Selva &amp; Grant, «Tecnifix» —JIC 2026< /div>
</footer>

<script>
  // scroll reveal
  const els = document.querySelectorAll('.fade-up');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target);} });
  }, {threshold:0.15});
  els.forEach(el=>io.observe(el));

  // network diagram build
  (function(){
    const svgLines = document.getElementById('lines');
    const svgNodes = document.getElementById('nodes');
    const cx=150, cy=150, r=112, n=7;
    for(let i=0;i<n;i++){
      const a = (i/n)*Math.PI*2 - Math.PI/2;
      const x = cx + r*Math.cos(a);
      const y = cy + r*Math.sin(a);
      const line = document.createElementNS('http://www.w3.org/2000/svg','path');
      const d = `M ${cx} ${cy} L ${x} ${y}`;
      line.setAttribute('d', d);
      line.setAttribute('class','link-line');
      svgLines.appendChild(line);
      const pulse = document.createElementNS('http://www.w3.org/2000/svg','path');
      pulse.setAttribute('d', d);
      pulse.setAttribute('class','link-pulse');
      pulse.style.animationDelay = (i*0.45)+'s';
      svgLines.appendChild(pulse);

      const node = document.createElementNS('http://www.w3.org/2000/svg','circle');
      node.setAttribute('cx', x); node.setAttribute('cy', y); node.setAttribute('r', 13);
      node.setAttribute('class','node');
      svgNodes.appendChild(node);
      const label = document.createElementNS('http://www.w3.org/2000/svg','text');
      label.setAttribute('x', x); label.setAttribute('y', y+3.5);
      label.setAttribute('text-anchor','middle'); label.setAttribute('class','node-label');
      label.textContent = 'G'+(i+1);
      svgNodes.appendChild(label);
    }
  })();

  // synthesized LAN "pulse" audio via WebAudio, no external files
  (function(){
    let ctx, playing=false, timer;
    const btn = document.getElementById('playBtn');
    const barsWrap = document.getElementById('bars');
    const barCount = 24;
    for(let i=0;i<barCount;i++){
      const s = document.createElement('span');
      barsWrap.appendChild(s);
    }
    const bars = barsWrap.querySelectorAll('span');

    function beep(freq, dur){
      const o = ctx.createOscillator();
      const g = ctx.createGain();
      o.type = 'sine';
      o.frequency.value = freq;
      g.gain.value = 0.0001;
      o.connect(g).connect(ctx.destination);
      const t = ctx.currentTime;
      g.gain.exponentialRampToValueAtTime(0.05, t+0.01);
      g.gain.exponentialRampToValueAtTime(0.0001, t+dur);
      o.start(t); o.stop(t+dur+0.02);
    }

    function tick(){
      const freq = 520 + Math.random()*260;
      beep(freq, 0.09);
      bars.forEach(b=>{ b.style.height = (6 + Math.random()*30) + 'px'; });
      timer = setTimeout(tick, 260 + Math.random()*180);
    }

    function stopVisual(){
      bars.forEach(b=>{ b.style.height = '6px'; });
    }

    btn.addEventListener('click', ()=>{
      if(!ctx) ctx = new (window.AudioContext || window.webkitAudioContext)();
      if(!playing){
        ctx.resume();
        playing = true;
        btn.textContent = '❚❚';
        tick();
      } else {
        playing = false;
        btn.textContent = '▶';
        clearTimeout(timer);
        stopVisual();
      }
    });
  })();
</script>
</body>
</html>
