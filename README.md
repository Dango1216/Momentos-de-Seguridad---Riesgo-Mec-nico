<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Riesgo Mecánico — GTC 45</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@3.7.0/dist/tabler-icons.min.css">
<style>
:root {
  --bg:        #0a0f1e;
  --surface:   #111827;
  --surface2:  #1a2236;
  --border:    rgba(99,179,237,0.18);
  --accent1:   #38bdf8;   /* sky blue */
  --accent2:   #34d399;   /* emerald */
  --accent3:   #f59e0b;   /* amber */
  --danger:    #f87171;
  --text:      #f1f5f9;
  --muted:     #94a3b8;
  --subtle:    #cbd5e1;
  --radius:    14px;
  --font-head: 'Syne', sans-serif;
  --font-body: 'DM Sans', sans-serif;
}

*{box-sizing:border-box;margin:0;padding:0;}

body {
  background: var(--bg);
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  font-family: var(--font-body);
  padding: 1rem;
}

/* ── wrapper ── */
.vp {
  width: 100%;
  max-width: 620px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 20px;
  overflow: hidden;
  box-shadow:
    0 0 0 1px rgba(56,189,248,.06),
    0 25px 60px rgba(0,0,0,.55),
    inset 0 1px 0 rgba(255,255,255,.05);
  position: relative;
}

/* subtle grid texture */
.vp::before {
  content:'';
  position:absolute;
  inset:0;
  background-image:
    linear-gradient(rgba(56,189,248,.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(56,189,248,.03) 1px, transparent 1px);
  background-size: 28px 28px;
  pointer-events:none;
  z-index:0;
}

/* glow blob */
.vp::after {
  content:'';
  position:absolute;
  top:-80px; left:50%;
  transform:translateX(-50%);
  width:340px; height:200px;
  background: radial-gradient(ellipse, rgba(56,189,248,.12) 0%, transparent 70%);
  pointer-events:none;
  z-index:0;
}

.screen {
  min-height: 380px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2.5rem 2rem 2rem;
  position: relative;
  z-index: 1;
}

/* ── scenes ── */
.scene {
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  width: 100%;
  animation: fadeUp .45s cubic-bezier(.16,1,.3,1);
}
.scene.active { display: flex; }

@keyframes fadeUp {
  from { opacity:0; transform:translateY(14px); }
  to   { opacity:1; transform:translateY(0); }
}

/* ── logo ── */
.logo-hippo { width:56px; height:40px; margin-bottom:1.1rem; }

/* ── scene icon ── */
.scene-icon {
  width: 60px; height: 60px;
  border-radius: 16px;
  display: flex; align-items: center; justify-content: center;
  margin-bottom: 1rem;
  position: relative;
}
.scene-icon::after {
  content:'';
  position:absolute;
  inset:-1px;
  border-radius:17px;
  background: linear-gradient(135deg, rgba(255,255,255,.15), rgba(255,255,255,.02));
  pointer-events:none;
}
.icon-sky  { background: linear-gradient(135deg,#0369a1,#0ea5e9); box-shadow:0 8px 24px rgba(14,165,233,.3); }
.icon-em   { background: linear-gradient(135deg,#059669,#34d399); box-shadow:0 8px 24px rgba(52,211,153,.25); }
.icon-amb  { background: linear-gradient(135deg,#b45309,#fbbf24); box-shadow:0 8px 24px rgba(251,191,36,.25); }
.icon-red  { background: linear-gradient(135deg,#991b1b,#f87171); box-shadow:0 8px 24px rgba(248,113,113,.25); }
.scene-icon i { font-size:28px; color:#fff; }

/* ── typography ── */
.scene-kicker {
  font-family: var(--font-head);
  font-size: 10.5px;
  font-weight: 700;
  letter-spacing: .12em;
  text-transform: uppercase;
  color: var(--accent1);
  margin-bottom: .35rem;
}

.scene-title {
  font-family: var(--font-head);
  font-size: 20px;
  font-weight: 700;
  color: var(--text);
  line-height: 1.3;
  margin-bottom: .75rem;
  max-width: 500px;
}

.scene-body {
  font-size: 13.5px;
  color: var(--muted);
  line-height: 1.75;
  max-width: 480px;
}
.scene-body strong { color: var(--subtle); }

/* ── ref tag ── */
.ref-tag {
  font-size: 10.5px;
  font-weight: 500;
  color: var(--accent1);
  border: 1px solid rgba(56,189,248,.25);
  background: rgba(56,189,248,.07);
  border-radius: 6px;
  padding: 3px 12px;
  margin-bottom: .9rem;
  display: inline-block;
  backdrop-filter: blur(4px);
}

/* ── pills ── */
.pill-row { display:flex; flex-wrap:wrap; gap:8px; justify-content:center; margin-top:1rem; }
.pill { font-size:12px; font-weight:500; padding:5px 14px; border-radius:20px; }
.pill-sky   { background:rgba(14,165,233,.15);  color:#7dd3fc; border:1px solid rgba(14,165,233,.3); }
.pill-em    { background:rgba(52,211,153,.12);  color:#6ee7b7; border:1px solid rgba(52,211,153,.25); }
.pill-amb   { background:rgba(251,191,36,.12);  color:#fde68a; border:1px solid rgba(251,191,36,.25); }
.pill-red   { background:rgba(248,113,113,.12); color:#fca5a5; border:1px solid rgba(248,113,113,.25); }

/* ── step list ── */
.step-list {
  display:flex; flex-direction:column; gap:10px;
  text-align:left; width:100%; max-width:490px; margin-top:.9rem;
}
.step-row-v { display:flex; align-items:flex-start; gap:12px; }

.snum {
  width:28px; height:28px; border-radius:8px;
  display:flex; align-items:center; justify-content:center;
  font-size:12px; font-weight:700;
  flex-shrink:0; margin-top:1px;
  font-family: var(--font-head);
}
.sn-sky { background:rgba(14,165,233,.2);  color:#7dd3fc; border:1px solid rgba(14,165,233,.3); }
.sn-em  { background:rgba(52,211,153,.18); color:#6ee7b7; border:1px solid rgba(52,211,153,.25); }
.sn-amb { background:rgba(251,191,36,.15); color:#fde68a; border:1px solid rgba(251,191,36,.25); }
.sn-red { background:rgba(248,113,113,.15);color:#fca5a5; border:1px solid rgba(248,113,113,.25); }
.sn-sl  { background:rgba(148,163,184,.12);color:#94a3b8; border:1px solid rgba(148,163,184,.2); }

.stext { font-size:13.5px; color:var(--text);   line-height:1.5; }
.ssub  { font-size:12px;   color:var(--muted);  margin-top:2px; line-height:1.4; }

/* ── rule banner ── */
.rule-banner {
  background: linear-gradient(135deg, rgba(52,211,153,.08), rgba(56,189,248,.06));
  border: 1px solid rgba(52,211,153,.2);
  border-radius: var(--radius);
  padding: 1rem 1.3rem;
  margin-top: 1.2rem;
  max-width: 490px;
  text-align: center;
}
.rule-banner p   { font-size:13px; color:var(--muted); line-height:1.7; }
.rule-banner strong { color:var(--text); }

/* ── error list ── */
.err-list { display:flex; flex-direction:column; gap:9px; text-align:left; width:100%; max-width:490px; margin-top:1rem; }
.err-row  { display:flex; align-items:flex-start; gap:10px; }
.err-dot  {
  width:22px; height:22px; border-radius:6px;
  background:rgba(248,113,113,.15);
  border:1px solid rgba(248,113,113,.3);
  display:flex; align-items:center; justify-content:center;
  flex-shrink:0; margin-top:2px;
}
.err-dot i { font-size:12px; color:var(--danger); }
.err-t { font-size:13.5px; color:var(--text); line-height:1.5; }
.err-s { font-size:12px; color:var(--muted); margin-top:1px; }

/* ── trio cards ── */
.trio { display:grid; grid-template-columns:1fr 1fr 1fr; gap:12px; width:100%; max-width:500px; margin-top:1rem; }
.trio-card {
  background: var(--surface2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 1.1rem .75rem;
  text-align: center;
  transition: transform .2s, border-color .2s;
}
.trio-card:hover { transform:translateY(-2px); border-color:rgba(56,189,248,.35); }
.trio-card i       { font-size:26px; display:block; margin-bottom:9px; }
.trio-title        { font-size:13px; font-weight:600; font-family:var(--font-head); color:var(--text); margin-bottom:4px; }
.trio-sub          { font-size:11px; color:var(--muted); line-height:1.5; }

/* ── progress ── */
.progress-track { height:3px; background:var(--surface2); margin:0; position:relative; z-index:1; }
.progress-fill  { height:100%; background:linear-gradient(90deg,var(--accent1),var(--accent2)); border-radius:2px; transition:width .4s ease; }

/* ── controls ── */
.controls {
  display:flex; align-items:center; justify-content:space-between;
  padding:.85rem 1.4rem;
  border-top:1px solid var(--border);
  background:rgba(10,15,30,.6);
  backdrop-filter:blur(8px);
  position:relative; z-index:1;
}

.ctrl-btn {
  display:flex; align-items:center; gap:6px;
  padding:7px 16px;
  border-radius:9px;
  border:1px solid var(--border);
  background:rgba(255,255,255,.04);
  color:var(--accent1);
  font-size:13px;
  font-family:var(--font-body);
  cursor:pointer;
  transition:background .15s, border-color .15s;
}
.ctrl-btn:hover:not(:disabled) { background:rgba(56,189,248,.1); border-color:rgba(56,189,248,.35); }
.ctrl-btn:disabled { opacity:.3; cursor:default; }
.ctrl-btn i { font-size:15px; }

.play-btn {
  width:42px; height:42px;
  border-radius:50%;
  border:none;
  background:linear-gradient(135deg, var(--accent1), var(--accent2));
  color:#0a0f1e;
  font-size:18px;
  cursor:pointer;
  display:flex; align-items:center; justify-content:center;
  box-shadow:0 4px 16px rgba(56,189,248,.35);
  transition:transform .15s, box-shadow .15s;
}
.play-btn:hover { transform:scale(1.07); box-shadow:0 6px 24px rgba(56,189,248,.5); }

.dot-row { display:flex; gap:6px; align-items:center; }
.dot {
  width:7px; height:7px; border-radius:50%;
  background:var(--surface2);
  border:1px solid var(--border);
  transition:background .2s, transform .2s, width .2s;
}
.dot.on { background:var(--accent1); width:18px; border-radius:4px; border-color:var(--accent1); }

/* ── accessibility ── */
.sr-only { position:absolute; width:1px; height:1px; overflow:hidden; clip:rect(0,0,0,0); white-space:nowrap; }
</style>
</head>
<body>

<h2 class="sr-only">Video interactivo sobre riesgo mecánico según la Guía Técnica Colombiana GTC 45 de 2012.</h2>

<div class="vp">
  <div class="screen">

    <!-- Slide 0: intro -->
    <div class="scene active" id="sc0">
      <svg class="logo-hippo" viewBox="0 0 120 85" xmlns="http://www.w3.org/2000/svg" aria-label="Logo hipopótamo corporativo" role="img">
        <path fill="#38bdf8" d="M110,42 C110,28 100,20 86,20 L80,20 L80,14 C80,11 78,9 75,9 L70,9 C67,9 65,11 65,14 L65,20 L40,20 C22,20 10,32 10,50 C10,62 16,70 26,74 L26,78 C26,80 28,82 30,82 L38,82 C40,82 42,80 42,78 L42,74 L78,74 L78,78 C78,80 80,82 82,82 L90,82 C92,82 94,80 94,78 L94,74 C104,70 110,58 110,42 Z M35,60 C31,60 28,57 28,53 C28,49 31,46 35,46 C39,46 42,49 42,53 C42,57 39,60 35,60 Z M85,60 C81,60 78,57 78,53 C78,49 81,46 85,46 C89,46 92,49 92,53 C92,57 89,60 85,60 Z"/>
      </svg>
      <span class="ref-tag">Guía Técnica Colombiana GTC 45 — 2012</span>
      <div class="scene-kicker">Momento de seguridad mecánico</div>
      <div class="scene-title">Riesgo mecánico: antes de iniciar, analiza y autoriza</div>
      <div class="scene-body">El riesgo mecánico agrupa todos los peligros generados por <strong>máquinas, equipos, herramientas y piezas en movimiento</strong> capaces de causar lesiones al trabajador.</div>
      <div class="pill-row">
        <span class="pill pill-red">Peligro mecánico</span>
        <span class="pill pill-em">Análisis de Trabajo Seguro</span>
        <span class="pill pill-sky">Permiso de Trabajo</span>
      </div>
    </div>

    <!-- Slide 1 -->
    <div class="scene" id="sc1">
      <div class="scene-icon icon-red"><i class="ti ti-alert-triangle" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Peligro mecánico</span>
      <div class="scene-kicker">¿Qué es el riesgo mecánico?</div>
      <div class="scene-title">Factores físicos que pueden lesionar el cuerpo del trabajador</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-red"><i class="ti ti-point" style="font-size:10px;"></i></div><div><div class="stext">Atrapamiento o aplastamiento</div><div class="ssub">Partes del cuerpo atrapadas entre elementos móviles, engranajes o rodillos.</div></div></div>
        <div class="step-row-v"><div class="snum sn-red"><i class="ti ti-point" style="font-size:10px;"></i></div><div><div class="stext">Corte o amputación</div><div class="ssub">Contacto con filos, cuchillas, sierras o bordes cortantes de máquinas o herramientas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-red"><i class="ti ti-point" style="font-size:10px;"></i></div><div><div class="stext">Golpe e impacto por proyección de fragmentos</div><div class="ssub">Piezas o partículas desprendidas a alta velocidad durante operaciones mecánicas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-red"><i class="ti ti-point" style="font-size:10px;"></i></div><div><div class="stext">Punzonamiento o perforación</div><div class="ssub">Contacto con partes punzantes como brocas, agujas o varillas expuestas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-red"><i class="ti ti-point" style="font-size:10px;"></i></div><div><div class="stext">Fricción o abrasión</div><div class="ssub">Contacto con superficies en movimiento que desgastan o queman la piel.</div></div></div>
      </div>
    </div>

    <!-- Slide 2 -->
    <div class="scene" id="sc2">
      <div class="scene-icon icon-em"><i class="ti ti-list-check" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Identificación de peligros</span>
      <div class="scene-kicker">Herramienta 1 — Análisis de Trabajo Seguro</div>
      <div class="scene-title">Analiza el riesgo mecánico paso a paso</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-sky">1</div><div><div class="stext">Describir los pasos de la tarea en el sitio de trabajo</div><div class="ssub">Nunca de memoria. El análisis se hace en el lugar real de ejecución.</div></div></div>
        <div class="step-row-v"><div class="snum sn-em">2</div><div><div class="stext">Identificar el peligro mecánico en cada paso</div><div class="ssub">¿Hay partes móviles expuestas, herramientas sin protección, equipos energizados?</div></div></div>
        <div class="step-row-v"><div class="snum sn-red">3</div><div><div class="stext">Evaluar el nivel de riesgo según la GTC 45</div><div class="ssub">Nivel de deficiencia × nivel de exposición × nivel de consecuencia.</div></div></div>
        <div class="step-row-v"><div class="snum sn-amb">4</div><div><div class="stext">Definir las medidas de control</div><div class="ssub">Eliminación, sustitución, controles de ingeniería, administrativos y EPP.</div></div></div>
        <div class="step-row-v"><div class="snum sn-sl">5</div><div><div class="stext">Firmar y socializar con todo el equipo</div><div class="ssub">Cada trabajador debe leer, entender y firmar.</div></div></div>
      </div>
    </div>

    <!-- Slide 3 -->
    <div class="scene" id="sc3">
      <div class="scene-icon icon-sky"><i class="ti ti-file-certificate" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Controles operacionales</span>
      <div class="scene-kicker">Herramienta 2 — Permiso de Trabajo</div>
      <div class="scene-title">Autorización formal para tareas de alto riesgo mecánico</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-sky">①</div><div><div class="stext">Solicitud formal del ejecutante</div><div class="ssub">Describe la tarea, los peligros mecánicos identificados y adjunta el Análisis de Trabajo Seguro.</div></div></div>
        <div class="step-row-v"><div class="snum sn-em">②</div><div><div class="stext">Inspección del área por SST y el supervisor</div><div class="ssub">Verifican condiciones reales: guardas, bloqueos de energía, estado de herramientas y equipos.</div></div></div>
        <div class="step-row-v"><div class="snum sn-amb">③</div><div><div class="stext">Emisión y firma del permiso</div><div class="ssub">La autoridad competente emite el permiso con vigencia máxima de un turno de trabajo.</div></div></div>
        <div class="step-row-v"><div class="snum sn-sl">④</div><div><div class="stext">Cierre formal del permiso</div><div class="ssub">Al finalizar: área entregada, permiso cerrado, novedades registradas.</div></div></div>
      </div>
      <div class="pill-row">
        <span class="pill pill-red">Trabajo en caliente</span>
        <span class="pill pill-sky">Espacios confinados</span>
        <span class="pill pill-em">Bloqueo y etiquetado de energías</span>
      </div>
    </div>

    <!-- Slide 4 -->
    <div class="scene" id="sc4">
      <div class="scene-icon icon-red"><i class="ti ti-x" aria-hidden="true"></i></div>
      <span class="ref-tag">Errores críticos</span>
      <div class="scene-kicker">Lo que no se debe hacer</div>
      <div class="scene-title">Estos errores generan accidentes por riesgo mecánico</div>
      <div class="err-list">
        <div class="err-row"><div class="err-dot"><i class="ti ti-x"></i></div><div><div class="err-t">Iniciar la tarea antes de que el Permiso de Trabajo sea emitido</div><div class="err-s">Sin autorización formal el peligro mecánico no está controlado.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x"></i></div><div><div class="err-t">Llenar el Análisis de Trabajo Seguro sin inspeccionar el área</div><div class="err-s">Los peligros mecánicos reales se detectan en el sitio, no desde la oficina.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x"></i></div><div><div class="err-t">Retirar guardas o protecciones mecánicas sin autorización</div><div class="err-s">Expone al trabajador directamente al peligro de atrapamiento, corte o proyección.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x"></i></div><div><div class="err-t">No bloquear y etiquetar las fuentes de energía antes de intervenir</div><div class="err-s">Una máquina puede arrancar de forma inesperada si no se aplica el bloqueo de energía.</div></div></div>
      </div>
    </div>

    <!-- Slide 5: cierre -->
    <div class="scene" id="sc5">
      <svg class="logo-hippo" viewBox="0 0 120 85" xmlns="http://www.w3.org/2000/svg" aria-label="Logo hipopótamo corporativo" role="img">
        <path fill="#38bdf8" d="M110,42 C110,28 100,20 86,20 L80,20 L80,14 C80,11 78,9 75,9 L70,9 C67,9 65,11 65,14 L65,20 L40,20 C22,20 10,32 10,50 C10,62 16,70 26,74 L26,78 C26,80 28,82 30,82 L38,82 C40,82 42,80 42,78 L42,74 L78,74 L78,78 C78,80 80,82 82,82 L90,82 C92,82 94,80 94,78 L94,74 C104,70 110,58 110,42 Z M35,60 C31,60 28,57 28,53 C28,49 31,46 35,46 C39,46 42,49 42,53 C42,57 39,60 35,60 Z M85,60 C81,60 78,57 78,53 C78,49 81,46 85,46 C89,46 92,49 92,53 C92,57 89,60 85,60 Z"/>
      </svg>
      <span class="ref-tag">GTC 45 — Jerarquía de controles</span>
      <div class="scene-kicker">Mensaje final</div>
      <div class="scene-title">Controla el riesgo mecánico en 3 pasos</div>
      <div class="trio">
        <div class="trio-card"><i class="ti ti-eye" style="color:#38bdf8;"></i><div class="trio-title">Analiza</div><div class="trio-sub">Elabora el Análisis de Trabajo Seguro en el sitio e identifica el peligro mecánico</div></div>
        <div class="trio-card"><i class="ti ti-file-certificate" style="color:#34d399;"></i><div class="trio-title">Autoriza</div><div class="trio-sub">Solicita el Permiso de Trabajo a tiempo. Sin permiso no hay ejecución</div></div>
        <div class="trio-card"><i class="ti ti-circle-check" style="color:#f59e0b;"></i><div class="trio-title">Ejecuta y cierra</div><div class="trio-sub">Aplica los controles, supervisa la tarea y cierra el permiso al finalizar</div></div>
      </div>
      <div class="rule-banner">
        <p>El minuto que inviertes analizando el riesgo mecánico puede salvar una vida. <strong>Aplica el Plan Operativo Normalizado en cada tarea no rutinaria.</strong></p>
      </div>
    </div>

  </div><!-- /screen -->

  <div class="progress-track"><div class="progress-fill" id="pbar" style="width:0%"></div></div>

  <div class="controls">
    <button class="ctrl-btn" id="prevBtn" onclick="go(-1)" disabled aria-label="Anterior">
      <i class="ti ti-arrow-left"></i> Anterior
    </button>
    <div style="display:flex;flex-direction:column;align-items:center;gap:8px;">
      <button class="play-btn" id="playBtn" onclick="togglePlay()" aria-label="Reproducir">
        <i class="ti ti-player-play" id="playIcon"></i>
      </button>
      <div class="dot-row" id="dots"></div>
    </div>
    <button class="ctrl-btn" id="nextBtn" onclick="go(1)" aria-label="Siguiente">
      Siguiente <i class="ti ti-arrow-right"></i>
    </button>
  </div>
</div>

<script>
const total=6; let cur=0, timer=null, playing=false;

function buildDots(){
  const d=document.getElementById('dots');
  for(let i=0;i<total;i++){
    const s=document.createElement('span');
    s.className='dot'+(i===0?' on':'');
    s.id='d'+i;
    s.style.cursor='pointer';
    s.onclick=()=>{ stopPlay(); show(i); };
    d.appendChild(s);
  }
}
buildDots();

function show(n){
  document.getElementById('sc'+cur).classList.remove('active');
  cur=Math.max(0,Math.min(total-1,n));
  document.getElementById('sc'+cur).classList.add('active');
  for(let i=0;i<total;i++)
    document.getElementById('d'+i).className='dot'+(i===cur?' on':'');
  document.getElementById('prevBtn').disabled=cur===0;
  document.getElementById('nextBtn').disabled=cur===total-1;
  document.getElementById('pbar').style.width=Math.round((cur/(total-1))*100)+'%';
  if(cur===total-1&&playing) stopPlay();
}

function go(d){ show(cur+d); }

function togglePlay(){ playing ? stopPlay() : startPlay(); }

function startPlay(){
  playing=true;
  document.getElementById('playIcon').className='ti ti-player-pause';
  timer=setInterval(()=>{
    if(cur<total-1){ show(cur+1); } else { stopPlay(); }
  },4000);
}

function stopPlay(){
  playing=false;
  clearInterval(timer);
  document.getElementById('playIcon').className='ti ti-player-play';
}
</script>
</body>
</html>
