[video_riesgo_mecanico_GTC45_corporativo.html](https://github.com/user-attachments/files/27577725/video_riesgo_mecanico_GTC45_corporativo.html)
# Momentos-de-Seguridad---Riesgo-Mec-nico
<style>
*{box-sizing:border-box;margin:0;padding:0;}
.vp{width:100%;font-family:var(--font-sans);background:#006633;border-radius:var(--border-radius-lg);overflow:hidden;}
.screen{min-height:360px;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:2.5rem 2rem;position:relative;}
.scene{display:none;flex-direction:column;align-items:center;justify-content:center;text-align:center;width:100%;animation:fadeIn 0.5s ease;}
.scene.active{display:flex;}
@keyframes fadeIn{from{opacity:0;transform:translateY(8px);}to{opacity:1;transform:translateY(0);}}

.logo-hippo{width:56px;height:40px;margin-bottom:1rem;}

.scene-icon{width:68px;height:68px;border-radius:50%;display:flex;align-items:center;justify-content:center;margin-bottom:1rem;}
.icon-dark{background:#006633;}
.icon-blue{background:#000BAF;}
.icon-red{background:#9a1c1c;}
.icon-mid{background:#00B140;}
.scene-icon i{font-size:34px;}
.ic-w{color:#E7E6E6;}
.ic-b{color:#20CEFA;}
.ic-g{color:#00E365;}

.scene-kicker{font-size:11px;font-weight:500;letter-spacing:0.1em;color:#00E365;text-transform:uppercase;margin-bottom:0.4rem;}
.scene-title{font-size:20px;font-weight:500;color:#ffffff;line-height:1.3;margin-bottom:0.75rem;max-width:520px;}
.scene-body{font-size:13px;color:#9FE1CB;line-height:1.7;max-width:500px;}
.scene-body strong{color:#ffffff;}

.ref-tag{font-size:11px;color:#20CEFA;border:0.5px solid #00B140;border-radius:4px;padding:2px 10px;margin-bottom:0.9rem;display:inline-block;background:#005229;}

.pill-row{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:1rem;}
.pill{font-size:12px;font-weight:500;padding:5px 14px;border-radius:20px;}
.pill-green{background:#00B140;color:#ffffff;}
.pill-blue{background:#000BAF;color:#20CEFA;}
.pill-dark{background:#006633;color:#00E365;border:0.5px solid #00B140;}
.pill-red{background:#7a1515;color:#fca5a5;}

.step-list{display:flex;flex-direction:column;gap:9px;text-align:left;width:100%;max-width:490px;margin-top:0.9rem;}
.step-row-v{display:flex;align-items:flex-start;gap:12px;}
.snum{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:500;flex-shrink:0;margin-top:1px;}
.sn-g{background:#00B140;color:#ffffff;}
.sn-b{background:#000BAF;color:#20CEFA;}
.sn-c{background:#005229;color:#00E365;}
.sn-r{background:#7a1515;color:#fca5a5;}
.sn-gr{background:#404040;color:#E7E6E6;}
.stext{font-size:13px;color:#ffffff;line-height:1.5;}
.ssub{font-size:12px;color:#9FE1CB;margin-top:2px;line-height:1.4;}

.rule-banner{background:#005229;border:0.5px solid #00B140;border-radius:8px;padding:0.9rem 1.2rem;margin-top:1.2rem;max-width:490px;text-align:center;}
.rule-banner p{font-size:13px;color:#9FE1CB;line-height:1.6;}
.rule-banner strong{color:#ffffff;}

.err-list{display:flex;flex-direction:column;gap:8px;text-align:left;width:100%;max-width:490px;margin-top:1rem;}
.err-row{display:flex;align-items:flex-start;gap:10px;}
.err-dot{width:22px;height:22px;border-radius:50%;background:#7a1515;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:2px;}
.err-dot i{font-size:13px;color:#fca5a5;}
.err-t{font-size:13px;color:#ffffff;line-height:1.5;}
.err-s{font-size:12px;color:#9FE1CB;margin-top:1px;}

.trio{display:grid;grid-template-columns:1fr 1fr 1fr;gap:12px;width:100%;max-width:500px;margin-top:1rem;}
.trio-card{background:#005229;border:0.5px solid #00B140;border-radius:8px;padding:1rem 0.75rem;text-align:center;}
.trio-card i{font-size:26px;display:block;margin-bottom:8px;}
.trio-title{font-size:13px;font-weight:500;color:#ffffff;margin-bottom:4px;}
.trio-sub{font-size:11px;color:#9FE1CB;line-height:1.4;}

.controls{display:flex;align-items:center;justify-content:space-between;padding:0.85rem 1.25rem;border-top:0.5px solid #00B140;background:#004d26;}
.ctrl-btn{display:flex;align-items:center;gap:6px;padding:7px 16px;border-radius:8px;border:0.5px solid #00B140;background:transparent;color:#00E365;font-size:13px;cursor:pointer;transition:background 0.15s;}
.ctrl-btn:hover{background:#005229;}
.ctrl-btn:disabled{opacity:0.3;cursor:default;}
.ctrl-btn i{font-size:16px;}
.play-btn{width:40px;height:40px;border-radius:50%;border:0.5px solid #00E365;background:#00B140;color:#ffffff;font-size:18px;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:background 0.15s;}
.play-btn:hover{background:#006633;}
.dot-row{display:flex;gap:6px;align-items:center;}
.dot{width:7px;height:7px;border-radius:50%;background:#006633;border:0.5px solid #00B140;transition:background 0.2s,transform 0.2s;}
.dot.on{background:#00E365;transform:scale(1.3);}
.progress-track{height:3px;background:#005229;margin:0 1.25rem;}
.progress-fill{height:100%;background:#00E365;border-radius:2px;transition:width 0.4s;}
</style>

<h2 class="sr-only">Video interactivo sobre riesgo mecánico según la Guía Técnica Colombiana GTC 45 de 2012, con identidad visual corporativa.</h2>

<div class="vp">
  <div class="screen">

    <div class="scene active" id="sc0">
      <svg class="logo-hippo" viewBox="0 0 120 85" xmlns="http://www.w3.org/2000/svg" aria-label="Logo hipopótamo corporativo" role="img">
        <path fill="#ffffff" d="M110,42 C110,28 100,20 86,20 L80,20 L80,14 C80,11 78,9 75,9 L70,9 C67,9 65,11 65,14 L65,20 L40,20 C22,20 10,32 10,50 C10,62 16,70 26,74 L26,78 C26,80 28,82 30,82 L38,82 C40,82 42,80 42,78 L42,74 L78,74 L78,78 C78,80 80,82 82,82 L90,82 C92,82 94,80 94,78 L94,74 C104,70 110,58 110,42 Z M35,60 C31,60 28,57 28,53 C28,49 31,46 35,46 C39,46 42,49 42,53 C42,57 39,60 35,60 Z M85,60 C81,60 78,57 78,53 C78,49 81,46 85,46 C89,46 92,49 92,53 C92,57 89,60 85,60 Z"/>
      </svg>
      <span class="ref-tag">Guía Técnica Colombiana GTC 45 — 2012</span>
      <div class="scene-kicker">Momento de seguridad mecánico</div>
      <div class="scene-title">Riesgo mecánico: antes de iniciar, analiza y autoriza</div>
      <div class="scene-body">El riesgo mecánico agrupa todos los peligros generados por <strong>máquinas, equipos, herramientas y piezas en movimiento</strong> capaces de causar lesiones al trabajador.</div>
      <div class="pill-row">
        <span class="pill pill-red">Peligro mecánico</span>
        <span class="pill pill-dark">Análisis de Trabajo Seguro</span>
        <span class="pill pill-blue">Permiso de Trabajo</span>
      </div>
    </div>

    <div class="scene" id="sc1">
      <div class="scene-icon icon-red"><i class="ti ti-alert-triangle ic-w" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Peligro mecánico</span>
      <div class="scene-kicker">¿Qué es el riesgo mecánico?</div>
      <div class="scene-title">Factores físicos que pueden lesionar el cuerpo del trabajador</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-r"><i class="ti ti-point" style="font-size:10px;" aria-hidden="true"></i></div><div><div class="stext">Atrapamiento o aplastamiento</div><div class="ssub">Partes del cuerpo atrapadas entre elementos móviles, engranajes o rodillos.</div></div></div>
        <div class="step-row-v"><div class="snum sn-r"><i class="ti ti-point" style="font-size:10px;" aria-hidden="true"></i></div><div><div class="stext">Corte o amputación</div><div class="ssub">Contacto con filos, cuchillas, sierras o bordes cortantes de máquinas o herramientas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-r"><i class="ti ti-point" style="font-size:10px;" aria-hidden="true"></i></div><div><div class="stext">Golpe e impacto por proyección de fragmentos</div><div class="ssub">Piezas o partículas desprendidas a alta velocidad durante operaciones mecánicas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-r"><i class="ti ti-point" style="font-size:10px;" aria-hidden="true"></i></div><div><div class="stext">Punzonamiento o perforación</div><div class="ssub">Contacto con partes punzantes como brocas, agujas o varillas expuestas.</div></div></div>
        <div class="step-row-v"><div class="snum sn-r"><i class="ti ti-point" style="font-size:10px;" aria-hidden="true"></i></div><div><div class="stext">Fricción o abrasión</div><div class="ssub">Contacto con superficies en movimiento que desgastan o queman la piel.</div></div></div>
      </div>
    </div>

    <div class="scene" id="sc2">
      <div class="scene-icon icon-mid"><i class="ti ti-list-check ic-w" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Identificación de peligros</span>
      <div class="scene-kicker">Herramienta 1 — Análisis de Trabajo Seguro</div>
      <div class="scene-title">Analiza el riesgo mecánico paso a paso</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-b">1</div><div><div class="stext">Describir los pasos de la tarea en el sitio de trabajo</div><div class="ssub">Nunca de memoria. El análisis se hace en el lugar real de ejecución.</div></div></div>
        <div class="step-row-v"><div class="snum sn-g">2</div><div><div class="stext">Identificar el peligro mecánico en cada paso</div><div class="ssub">¿Hay partes móviles expuestas, herramientas sin protección, equipos energizados?</div></div></div>
        <div class="step-row-v"><div class="snum sn-r">3</div><div><div class="stext">Evaluar el nivel de riesgo según la GTC 45</div><div class="ssub">Nivel de deficiencia × nivel de exposición × nivel de consecuencia.</div></div></div>
        <div class="step-row-v"><div class="snum sn-c">4</div><div><div class="stext">Definir las medidas de control</div><div class="ssub">Eliminación, sustitución, controles de ingeniería, administrativos y equipos de protección personal.</div></div></div>
        <div class="step-row-v"><div class="snum sn-gr">5</div><div><div class="stext">Firmar y socializar con todo el equipo</div><div class="ssub">Cada trabajador que participa en la tarea debe leer, entender y firmar.</div></div></div>
      </div>
    </div>

    <div class="scene" id="sc3">
      <div class="scene-icon icon-blue"><i class="ti ti-file-certificate ic-b" aria-hidden="true"></i></div>
      <span class="ref-tag">GTC 45 — Controles operacionales</span>
      <div class="scene-kicker">Herramienta 2 — Permiso de Trabajo</div>
      <div class="scene-title">Autorización formal para tareas de alto riesgo mecánico</div>
      <div class="step-list">
        <div class="step-row-v"><div class="snum sn-b">①</div><div><div class="stext">Solicitud formal del ejecutante</div><div class="ssub">Describe la tarea, los peligros mecánicos identificados y adjunta el Análisis de Trabajo Seguro.</div></div></div>
        <div class="step-row-v"><div class="snum sn-g">②</div><div><div class="stext">Inspección del área por Seguridad y Salud en el Trabajo y el supervisor</div><div class="ssub">Verifican condiciones reales: guardas, bloqueos de energía, estado de herramientas y equipos.</div></div></div>
        <div class="step-row-v"><div class="snum sn-c">③</div><div><div class="stext">Emisión y firma del permiso</div><div class="ssub">La autoridad competente emite el permiso con vigencia máxima de un turno de trabajo.</div></div></div>
        <div class="step-row-v"><div class="snum sn-gr">④</div><div><div class="stext">Cierre formal del permiso</div><div class="ssub">Al finalizar: área entregada, permiso cerrado, novedades registradas.</div></div></div>
      </div>
      <div class="pill-row">
        <span class="pill pill-red">Trabajo en caliente</span>
        <span class="pill pill-blue">Espacios confinados</span>
        <span class="pill pill-dark">Bloqueo y etiquetado de energías</span>
      </div>
    </div>

    <div class="scene" id="sc4">
      <div class="scene-icon icon-red"><i class="ti ti-x ic-w" aria-hidden="true"></i></div>
      <span class="ref-tag">Errores críticos</span>
      <div class="scene-kicker">Lo que no se debe hacer</div>
      <div class="scene-title">Estos errores generan accidentes por riesgo mecánico</div>
      <div class="err-list">
        <div class="err-row"><div class="err-dot"><i class="ti ti-x" aria-hidden="true"></i></div><div><div class="err-t">Iniciar la tarea antes de que el Permiso de Trabajo sea emitido</div><div class="err-s">Sin autorización formal el peligro mecánico no está controlado.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x" aria-hidden="true"></i></div><div><div class="err-t">Llenar el Análisis de Trabajo Seguro sin inspeccionar el área</div><div class="err-s">Los peligros mecánicos reales se detectan en el sitio, no desde la oficina.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x" aria-hidden="true"></i></div><div><div class="err-t">Retirar guardas o protecciones mecánicas sin autorización</div><div class="err-s">Expone al trabajador directamente al peligro de atrapamiento, corte o proyección.</div></div></div>
        <div class="err-row"><div class="err-dot"><i class="ti ti-x" aria-hidden="true"></i></div><div><div class="err-t">No bloquear y etiquetar las fuentes de energía antes de intervenir</div><div class="err-s">Una máquina puede arrancar de forma inesperada si no se aplica el bloqueo de energía.</div></div></div>
      </div>
    </div>

    <div class="scene" id="sc5">
      <svg class="logo-hippo" viewBox="0 0 120 85" xmlns="http://www.w3.org/2000/svg" aria-label="Logo hipopótamo corporativo" role="img">
        <path fill="#ffffff" d="M110,42 C110,28 100,20 86,20 L80,20 L80,14 C80,11 78,9 75,9 L70,9 C67,9 65,11 65,14 L65,20 L40,20 C22,20 10,32 10,50 C10,62 16,70 26,74 L26,78 C26,80 28,82 30,82 L38,82 C40,82 42,80 42,78 L42,74 L78,74 L78,78 C78,80 80,82 82,82 L90,82 C92,82 94,80 94,78 L94,74 C104,70 110,58 110,42 Z M35,60 C31,60 28,57 28,53 C28,49 31,46 35,46 C39,46 42,49 42,53 C42,57 39,60 35,60 Z M85,60 C81,60 78,57 78,53 C78,49 81,46 85,46 C89,46 92,49 92,53 C92,57 89,60 85,60 Z"/>
      </svg>
      <span class="ref-tag">GTC 45 — Jerarquía de controles</span>
      <div class="scene-kicker">Mensaje final</div>
      <div class="scene-title">Controla el riesgo mecánico en 3 pasos</div>
      <div class="trio">
        <div class="trio-card"><i class="ti ti-eye" style="color:#20CEFA;" aria-hidden="true"></i><div class="trio-title">Analiza</div><div class="trio-sub">Elabora el Análisis de Trabajo Seguro en el sitio e identifica el peligro mecánico</div></div>
        <div class="trio-card"><i class="ti ti-file-certificate" style="color:#00E365;" aria-hidden="true"></i><div class="trio-title">Autoriza</div><div class="trio-sub">Solicita el Permiso de Trabajo a tiempo. Sin permiso no hay ejecución</div></div>
        <div class="trio-card"><i class="ti ti-circle-check" style="color:#00B140;" aria-hidden="true"></i><div class="trio-title">Ejecuta y cierra</div><div class="trio-sub">Aplica los controles, supervisa la tarea y cierra el permiso al finalizar</div></div>
      </div>
      <div class="rule-banner" style="margin-top:1.2rem;"><p>El minuto que inviertes analizando el riesgo mecánico puede salvar una vida. <strong>Aplica el Plan Operativo Normalizado en cada tarea no rutinaria.</strong></p></div>
    </div>

  </div>

  <div class="progress-track"><div class="progress-fill" id="pbar" style="width:0%"></div></div>

  <div class="controls">
    <button class="ctrl-btn" id="prevBtn" onclick="go(-1)" disabled aria-label="Anterior"><i class="ti ti-arrow-left" aria-hidden="true"></i> Anterior</button>
    <div style="display:flex;flex-direction:column;align-items:center;gap:8px;">
      <button class="play-btn" id="playBtn" onclick="togglePlay()" aria-label="Reproducir"><i class="ti ti-player-play" id="playIcon" aria-hidden="true"></i></button>
      <div class="dot-row" id="dots"></div>
    </div>
    <button class="ctrl-btn" id="nextBtn" onclick="go(1)" aria-label="Siguiente">Siguiente <i class="ti ti-arrow-right" aria-hidden="true"></i></button>
  </div>
</div>

<script>
const total=6;let cur=0,timer=null,playing=false;
function buildDots(){const d=document.getElementById('dots');for(let i=0;i<total;i++){const s=document.createElement('span');s.className='dot'+(i===0?' on':'');s.id='d'+i;d.appendChild(s);}}
buildDots();
function show(n){document.getElementById('sc'+cur).classList.remove('active');cur=Math.max(0,Math.min(total-1,n));document.getElementById('sc'+cur).classList.add('active');for(let i=0;i<total;i++)document.getElementById('d'+i).className='dot'+(i===cur?' on':'');document.getElementById('prevBtn').disabled=cur===0;document.getElementById('nextBtn').disabled=cur===total-1;document.getElementById('pbar').style.width=Math.round((cur/(total-1))*100)+'%';if(cur===total-1&&playing)stopPlay();}
function go(d){show(cur+d);}
function togglePlay(){playing?stopPlay():startPlay();}
function startPlay(){playing=true;document.getElementById('playIcon').className='ti ti-player-pause';timer=setInterval(()=>{if(cur<total-1){show(cur+1);}else{stopPlay();}},4000);}
function stopPlay(){playing=false;clearInterval(timer);document.getElementById('playIcon').className='ti ti-player-play';}
</script>
