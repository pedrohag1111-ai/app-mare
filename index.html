<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Maré — diário de identidade de gênero</title>

<!-- Configurações PWA (Instalação no Celular) -->
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#FAF6F1">
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="Maré">

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=Karla:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap');

  * { box-sizing: border-box; }
  html, body { margin: 0; padding: 0; font-family: 'Karla', system-ui, sans-serif; user-select: none; }
  button { font: inherit; }

  .font-display { font-family: 'Fraunces', Georgia, serif; }
  .font-mono { font-family: 'JetBrains Mono', monospace; }

  .bg-layer { position: fixed; inset: 0; }
  #bg-new { z-index: 0; }
  #bg-old { z-index: 1; pointer-events: none; opacity: 0; }

  #content-wrap { position: relative; z-index: 2; min-height: 100vh; transition: color .5s ease; }
  .wrap { max-width: 640px; margin: 0 auto; padding: 32px 20px 96px; }

  header .top-row { display: flex; align-items: center; gap: 12px; }
  .app-icon { width: 34px; height: 34px; border-radius: 60% 40% 55% 45% / 55% 45% 60% 40%; flex-shrink: 0; }
  header h1 { font-size: 24px; line-height: 1; margin: 0; }
  header .subtitle { font-size: 12px; margin: 4px 0 0; }

  .ribbon { display: flex; align-items: flex-end; gap: 6px; overflow-x: auto; padding-bottom: 4px; margin-top: 20px; }
  .ribbon-dot { width: 16px; height: 16px; border-radius: 999px; flex: 0 0 auto; cursor: pointer; transition: transform .2s ease; border: none; padding: 0; }
  .ribbon-dot:hover { transform: scale(1.15); }

  nav.tabs { display: flex; gap: 4px; padding: 4px; border-radius: 12px; margin: 24px 0; }
  nav.tabs button { flex: 1; display: flex; align-items: center; justify-content: center; gap: 6px; padding: 8px 0; border: none; border-radius: 8px; font-size: 14px; font-weight: 500; cursor: pointer; background: transparent; }

  .reminder-banner { display: flex; align-items: center; gap: 8px; border-radius: 12px; padding: 10px 12px; margin-bottom: 16px; font-size: 12px; }

  .date-row { display: flex; align-items: baseline; justify-content: space-between; margin-bottom: 16px; }
  .date-num { font-size: 36px; margin: 0; }
  .weekday { font-size: 14px; margin: 2px 0 0; }
  .back-today { font-size: 12px; padding: 6px 12px; border-radius: 999px; background: transparent; cursor: pointer; }

  .hint { font-size: 14px; margin: 0 0 12px; }

  .swatch-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 6px; margin-bottom: 20px; }
  .swatch-btn { display: flex; flex-direction: column; align-items: center; gap: 6px; padding: 10px 2px; border-radius: 16px; cursor: pointer; background: #fff; transition: transform .18s ease; border-width: 2px; border-style: solid; }
  .swatch-btn:hover { transform: translateY(-2px); }
  .swatch-btn:active { transform: scale(.97); }
  .drop { border-radius: 60% 40% 55% 45% / 55% 45% 60% 40%; width: 26px; height: 26px; }
  .swatch-label { font-size: 10px; font-weight: 500; text-align: center; line-height: 1.15; }

  textarea#note-input { width: 100%; border-radius: 12px; padding: 12px; font-size: 14px; resize: none; margin-bottom: 16px; font-family: 'Karla', sans-serif; border-width: 1.5px; border-style: solid; }

  .action-row { display: flex; align-items: center; gap: 12px; }
  .btn-save { flex: 1; display: flex; align-items: center; justify-content: center; gap: 8px; padding: 12px; border-radius: 12px; font-weight: 600; font-size: 14px; border: none; cursor: pointer; }
  .btn-delete { padding: 12px; border-radius: 12px; cursor: pointer; background: transparent; display: flex; align-items: center; justify-content: center; border-width: 1.5px; border-style: solid; }
  .storage-err { font-size: 12px; margin-top: 12px; color: #B8628F; }

  .settings-card { margin-top: 24px; border-radius: 16px; padding: 16px; background: #fff; border-width: 1.5px; border-style: solid; }
  .hormone-today-row { display: flex; align-items: center; justify-content: space-between; border-radius: 12px; padding: 10px 12px; margin-bottom: 16px; }
  .settings-row { display: flex; align-items: center; justify-content: space-between; }
  .settings-label { font-size: 14px; font-weight: 500; display: flex; align-items: center; gap: 8px; }
  .settings-sub { margin-top: 16px; padding-top: 16px; border-top-width: 1px; border-top-style: solid; }
  .settings-time-row { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
  .settings-time-label { font-size: 12px; }
  input#time-input { font-family: 'JetBrains Mono', monospace; font-size: 14px; border-radius: 8px; padding: 4px 8px; border-width: 1.5px; border-style: solid; }
  .settings-note { font-size: 12px; line-height: 1.5; margin: 0; }

  .toggle { width: 40px; height: 23px; border-radius: 999px; position: relative; border: none; cursor: pointer; flex-shrink: 0; transition: background-color .2s ease; }
  .toggle .knob { position: absolute; top: 2.5px; width: 18px; height: 18px; border-radius: 50%; background: #fff; transition: left .2s ease; box-shadow: 0 1px 2px rgba(0,0,0,.2); }

  .cal-nav { display: flex; align-items: center; justify-content: space-between; margin-bottom: 16px; }
  .cal-nav button { width: 32px; height: 32px; border-radius: 999px; background: transparent; cursor: pointer; display: flex; align-items: center; justify-content: center; border-width: 1px; border-style: solid; }
  .cal-title { font-size: 18px; }
  .cal-weekdays { display: grid; grid-template-columns: repeat(7, 1fr); margin-bottom: 8px; gap: 8px; }
  .cal-weekdays span { text-align: center; font-size: 12px; font-weight: 600; }
  
  .cal-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 8px; }
  .cal-cell-wrapper { position: relative; aspect-ratio: 1 / 1; width: 100%; }
  .cal-cell { width: 100%; height: 100%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: 600; cursor: pointer; border-radius: 12px; padding: 0; margin: 0; transition: transform 0.15s ease, box-shadow 0.15s ease; }
  .cal-cell:hover { transform: translateY(-2px); }
  
  .cal-legend { display: flex; align-items: center; gap: 16px; flex-wrap: wrap; margin-top: 20px; }
  .legend-item { display: flex; align-items: center; gap: 6px; }
  .legend-dot { width: 9px; height: 9px; border-radius: 999px; }
  .legend-label { font-size: 12px; }

  .range-row { display: flex; gap: 8px; margin-bottom: 20px; }
  .chip { font-size: 12px; font-weight: 500; padding: 6px 12px; border-radius: 999px; cursor: pointer; border-width: 1px; border-style: solid; background: #fff; }
  .empty-state { border-radius: 16px; padding: 24px; text-align: center; font-size: 14px; border-width: 1.5px; border-style: dashed; background: #fff; }
  .spectrum-bar { height: 22px; border-radius: 999px; overflow: hidden; display: flex; margin-bottom: 24px; border-width: 1px; border-style: solid; }
  .stat-row { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
  .stat-dot { width: 10px; height: 10px; border-radius: 999px; flex-shrink: 0; }
  .stat-label { font-size: 14px; width: 112px; flex-shrink: 0; }
  .stat-track { flex: 1; height: 8px; border-radius: 999px; overflow: hidden; }
  .stat-fill { height: 100%; border-radius: 999px; }
  .stat-value { font-family: 'JetBrains Mono', monospace; font-size: 12px; width: 56px; text-align: right; flex-shrink: 0; }
  .stat-total { font-size: 12px; margin-top: 20px; }
  .reset-section { margin-top: 40px; padding-top: 20px; border-top-width: 1px; border-top-style: solid; }
  .reset-section button { background: none; border: none; cursor: pointer; font-size: 12px; }

  .loading-screen { min-height: 100vh; display: flex; align-items: center; justify-content: center; background: #FAF6F1; }
  .spinner { width: 28px; height: 28px; border: 3px solid #EAE1D8; border-top-color: #8A8094; border-radius: 50%; animation: spin 0.8s linear infinite; }
  @keyframes spin { to { transform: rotate(360deg); } }

  @media (prefers-reduced-motion: reduce) {
    .swatch-btn, .ribbon-dot, .toggle, .toggle .knob, .cal-cell { transition: none !important; }
  }
</style>
</head>
<body>

<div id="loading" class="loading-screen"><div class="spinner"></div></div>

<div id="bg-new" class="bg-layer"></div>
<div id="bg-old" class="bg-layer"></div>
<div id="content-wrap" style="display:none;">
  <div class="wrap" id="app"></div>
</div>

<script>
/* ---------- Fallback para LocalStorage Nativo ---------- */
if (!window.storage) {
  window.storage = {
    get: (key) => Promise.resolve({ value: localStorage.getItem(key) }),
    set: (key, value) => Promise.resolve(localStorage.setItem(key, value)),
    remove: (key) => Promise.resolve(localStorage.removeItem(key))
  };
}

/* ---------- data ---------- */
const IDENTITIES = [
  { id: "feminino",  label: "Feminino",       color: "#F0A8C4", deep: "#C15F8F" },
  { id: "agenero",   label: "Agênero",        color: "#FFFFFF", deep: "#8A8094", border: "#D9D0C5", textDark: true },
  { id: "bigenero",  label: "Bigênero",       color: "#BE93DE", deep: "#7E4FAE" },
  { id: "neutro",    label: "Neutro/Outros",  color: "#3D3846", deep: "#3D3846" },
  { id: "masculino", label: "Masculino",      color: "#7FAADB", deep: "#4779AE" },
];

const DEFAULT_INK = "#2E2440";
const DEFAULT_INK_SOFT = "#8A8094";
const DEFAULT_PAPER = "#FAF6F1";
const DEFAULT_PAPER_LINE = "#EAE1D8";
const GOLD = "#C9A24B";

const THEMES = {
  default: {
    mode: "light", backgroundColor: DEFAULT_PAPER,
    backgroundImage: "radial-gradient(circle at 15% 20%, rgba(240,168,196,0.10), transparent 45%), radial-gradient(circle at 85% 15%, rgba(127,170,219,0.10), transparent 45%), radial-gradient(circle at 50% 92%, rgba(190,147,222,0.10), transparent 50%)",
    ink: DEFAULT_INK, inkSoft: DEFAULT_INK_SOFT, paperLine: DEFAULT_PAPER_LINE, surface: "#F0E9E1",
  },
  feminino: {
    mode: "light", backgroundColor: "#FDF1F5",
    backgroundImage: "radial-gradient(circle at 18% 12%, rgba(255,255,255,0.85), transparent 38%), radial-gradient(circle at 82% 22%, rgba(251,216,228,0.9), transparent 45%), radial-gradient(circle at 28% 88%, rgba(246,198,216,0.75), transparent 50%), linear-gradient(165deg, #FFF4F8, #FBDCE7)",
    ink: "#6B3550", inkSoft: "#B98CA0", paperLine: "#F3D3E1", surface: "#F9DDE9",
  },
  agenero: {
    mode: "light", backgroundColor: "#FFFFFF",
    backgroundImage: "repeating-linear-gradient(0deg, rgba(46,36,64,0.035) 0px, rgba(46,36,64,0.035) 1px, transparent 1px, transparent 64px), repeating-linear-gradient(90deg, rgba(46,36,64,0.035) 0px, rgba(46,36,64,0.035) 1px, transparent 1px, transparent 64px)",
    ink: "#33303A", inkSoft: "#9B96A0", paperLine: "#E6E2DC", surface: "#F2EFEA",
  },
  bigenero: {
    mode: "light", backgroundColor: "#EFE3F7",
    backgroundImage: "linear-gradient(125deg, #CFE0F5 0%, #D9C7EE 35%, #E9C9DE 65%, #F3D3E1 100%)",
    ink: "#3B2A55", inkSoft: "#8D7BA8", paperLine: "#DDCBEE", surface: "#EAD9F5",
  },
  neutro: {
    mode: "dark", backgroundColor: "#221F29",
    backgroundImage: "radial-gradient(circle at 15% 20%, rgba(255,255,255,0.45) 0px, rgba(255,255,255,0.45) 1px, transparent 1.5px), radial-gradient(circle at 78% 15%, rgba(255,255,255,0.35) 0px, rgba(255,255,255,0.35) 1px, transparent 1.5px), radial-gradient(circle at 50% 70%, rgba(255,255,255,0.3) 0px, rgba(255,255,255,0.3) 1px, transparent 1.5px), linear-gradient(180deg, #2B2733, #201D28)",
    ink: "#F3EFE9", inkSoft: "#B7AFC0", paperLine: "rgba(255,255,255,0.16)", surface: "rgba(255,255,255,0.08)",
  },
  masculino: {
    mode: "light", backgroundColor: "#EAF2FA",
    backgroundImage: "repeating-linear-gradient(0deg, rgba(31,53,80,0.05) 0px, rgba(31,53,80,0.05) 1px, transparent 1px, transparent 40px), repeating-linear-gradient(90deg, rgba(31,53,80,0.05) 0px, rgba(31,53,80,0.05) 1px, transparent 1px, transparent 40px), linear-gradient(160deg, #DCEAF7, #B9D4EE)",
    ink: "#1F3550", inkSoft: "#6E8FAD", paperLine: "#CFE0F0", surface: "#DCEAF8",
  },
};

const WEEKDAYS = ["D","S","T","Q","Q","S","S"];
const MONTHS = ["Janeiro","Fevereiro","Março","Abril","Maio","Junho","Julho","Agosto","Setembro","Outubro","Novembro","Dezembro"];

const ICONS = {
  bell: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 8a6 6 0 0 1 12 0c0 7 3 9 3 9H3s3-2 3-9"/><path d="M10.3 21a1.94 1.94 0 0 0 3.4 0"/></svg>',
  book: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>',
  calendar: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>',
  bars: '<svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 3v18h18"/><rect x="7" y="12" width="3" height="6"/><rect x="12" y="8" width="3" height="10"/><rect x="17" y="5" width="3" height="13"/></svg>',
  chevronLeft: '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15 18l-6-6 6-6"/></svg>',
  chevronRight: '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 18l6-6-6-6"/></svg>',
  trash: '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 6h18M8 6V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2m3 0-1 14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2L4 6"/></svg>',
  check: '<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 6 9 17l-5-5"/></svg>',
  pill: '<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m10.5 20.5 10-10a4.95 4.95 0 1 0-7-7l-10 10a4.95 4.95 0 1 0 7 7Z"/><path d="m8.5 8.5 7 7"/></svg>',
};

/* ---------- state ---------- */
const state = {
  entries: {},
  settings: { usesHormones: false, reminderEnabled: false, reminderTime: "08:00" },
  tab: "hoje",
  selectedDate: startOfDay(new Date()),
  draftIdentity: null,
  draftNote: "",
  draftHormone: false,
  savedFlash: false,
  calMonth: new Date().getMonth(),
  calYear: new Date().getFullYear(),
  range: 30,
  confirmingReset: false,
  storageError: false,
};
const themeState = { displayId: "default", prevId: null };

/* ---------- helpers ---------- */
function ident(id){ return IDENTITIES.find(i => i.id === id); }
function dateKey(d){
  const y = d.getFullYear(), m = String(d.getMonth()+1).padStart(2,"0"), day = String(d.getDate()).padStart(2,"0");
  return `${y}-${m}-${day}`;
}
function startOfDay(d){ const c = new Date(d); c.setHours(0,0,0,0); return c; }
function esc(s){ const d = document.createElement("div"); d.textContent = s ?? ""; return d.innerHTML; }
function currentThemeId(){ return state.draftIdentity && THEMES[state.draftIdentity] ? state.draftIdentity : "default"; }

/* ---------- persistence ---------- */
function loadAll(){
  Promise.all([
    window.storage.get("entries").catch(() => null),
    window.storage.get("settings").catch(() => null),
  ]).then(([e, s]) => {
    if (e && e.value) { try { state.entries = JSON.parse(e.value); } catch(err){} }
    if (s && s.value) { try { state.settings = { ...state.settings, ...JSON.parse(s.value) }; } catch(err){} }
    syncDraftFromSelected();
    updateTheme(currentThemeId());
    document.getElementById("loading").style.display = "none";
    document.getElementById("content-wrap").style.display = "block";
    render();
  });
}
function persistEntries(){
  state.storageError = false;
  window.storage.set("entries", JSON.stringify(state.entries)).catch(() => {
    state.storageError = true;
    render();
  });
}
function persistSettings(){
  window.storage.set("settings", JSON.stringify(state.settings)).catch(() => {});
}

/* ---------- theme crossfade ---------- */
function applyThemeLayers(){
  const bgNew = document.getElementById("bg-new");
  const bgOld = document.getElementById("bg-old");
  const t = THEMES[themeState.displayId];
  bgNew.style.backgroundColor = t.backgroundColor;
  bgNew.style.backgroundImage = t.backgroundImage;
  if (themeState.prevId) {
    const p = THEMES[themeState.prevId];
    bgOld.style.transition = "none";
    bgOld.style.backgroundColor = p.backgroundColor;
    bgOld.style.backgroundImage = p.backgroundImage;
    bgOld.style.opacity = "1";
    void bgOld.offsetWidth; // force reflow
    bgOld.style.transition = "opacity 900ms ease";
    bgOld.style.opacity = "0";
  } else {
    bgOld.style.transition = "none";
    bgOld.style.opacity = "0";
  }
  document.getElementById("content-wrap").style.color = t.ink;
}
function updateTheme(id){
  if (id === themeState.displayId) return;
  themeState.prevId = themeState.displayId;
  themeState.displayId = id;
  applyThemeLayers();
}

/* ---------- actions ---------- */
function syncDraftFromSelected(){
  const k = dateKey(state.selectedDate);
  const existing = state.entries[k];
  state.draftIdentity = existing ? existing.identity : null;
  state.draftNote = existing ? (existing.note || "") : "";
  state.draftHormone = existing ? !!existing.hormone : false;
}
function selectDate(iso){
  state.selectedDate = startOfDay(new Date(iso));
  syncDraftFromSelected();
  state.tab = "hoje";
  updateTheme(currentThemeId());
  render();
}
function goToday(){ selectDate(startOfDay(new Date()).toISOString()); }
function setTab(id){ state.tab = id; render(); }
function toggleIdentity(id){
  state.draftIdentity = state.draftIdentity === id ? null : id;
  updateTheme(currentThemeId());
  render();
}
function saveEntry(){
  if (!state.draftIdentity) return;
  const k = dateKey(state.selectedDate);
  state.entries[k] = { identity: state.draftIdentity, note: state.draftNote.trim(), hormone: !!state.draftHormone, ts: Date.now() };
  persistEntries();
  state.savedFlash = true;
  render();
  setTimeout(() => { state.savedFlash = false; render(); }, 1400);
}
function deleteEntry(){
  const k = dateKey(state.selectedDate);
  if (!state.entries[k]) return;
  delete state.entries[k];
  persistEntries();
  syncDraftFromSelected();
  updateTheme(currentThemeId());
  render();
}
function resetAll(){ state.entries = {}; persistEntries(); state.confirmingReset = false; render(); }
function updateSettings(patch){ Object.assign(state.settings, patch); persistSettings(); render(); }
function prevMonth(){ state.calMonth--; if (state.calMonth < 0){ state.calMonth = 11; state.calYear--; } render(); }
function nextMonth(){ state.calMonth++; if (state.calMonth > 11){ state.calMonth = 0; state.calYear++; } render(); }
function setRange(r){ state.range = r; render(); }

function reminderDue(){
  if (!state.settings.reminderEnabled) return false;
  const todayKey = dateKey(startOfDay(new Date()));
  if (state.entries[todayKey]) return false;
  const [h, m] = state.settings.reminderTime.split(":").map(Number);
  const now = new Date();
  return now.getHours() > h || (now.getHours() === h && now.getMinutes() >= m);
}

/* ---------- render ---------- */
function render(){
  const theme = THEMES[themeState.displayId];
  const INK = theme.ink, INK_SOFT = theme.inkSoft, PAPER_LINE = theme.paperLine, SURFACE = theme.surface;
  const ON_INK = theme.backgroundColor;
  const today = startOfDay(new Date());
  const isToday = dateKey(state.selectedDate) === dateKey(today);

  let html = "";
  html += renderHeader(INK, INK_SOFT, PAPER_LINE);
  html += renderNav(SURFACE, INK, INK_SOFT);
  if (state.tab === "hoje") html += renderHoje(INK, INK_SOFT, ON_INK, isToday, today);
  if (state.tab === "calendario") html += renderCalendario(INK_SOFT);
  if (state.tab === "estatisticas") html += renderEstatisticas(INK, INK_SOFT, ON_INK);

  document.getElementById("app").innerHTML = html;
}

function renderHeader(INK, INK_SOFT, PAPER_LINE){
  const grad = IDENTITIES.map(i => i.color).join(", ");
  const today = startOfDay(new Date());
  let ribbon = "";
  for (let i = 13; i >= 0; i--){
    const d = new Date(today); d.setDate(d.getDate() - i);
    const k = dateKey(d);
    const entry = state.entries[k];
    const info = entry ? ident(entry.identity) : null;
    const bg = info ? info.color : "transparent";
    const border = info ? (info.border ? `1.5px solid ${info.border}` : "none") : `1.5px dashed ${PAPER_LINE}`;
    ribbon += `<button class="ribbon-dot" data-action="select-date" data-date="${d.toISOString()}" title="${d.getDate()}/${d.getMonth()+1}${info ? " · " + info.label : ""}" style="background:${bg};border:${border};"></button>`;
  }
  return `
    <header>
      <div class="top-row">
        <div class="app-icon" style="background: linear-gradient(135deg, ${grad}); border: 1px solid ${PAPER_LINE};"></div>
        <div>
          <h1 class="font-display" style="color:${INK};">Maré</h1>
          <p class="subtitle" style="color:${INK_SOFT};">um diário para acompanhar como seu gênero se sente, dia após dia</p>
        </div>
      </div>
      <div class="ribbon">${ribbon}</div>
    </header>`;
}

function renderNav(SURFACE, INK, INK_SOFT){
  const tabs = [
    { id: "hoje", label: "Hoje", icon: ICONS.book },
    { id: "calendario", label: "Calendário", icon: ICONS.calendar },
    { id: "estatisticas", label: "Estatísticas", icon: ICONS.bars },
  ];
  const buttons = tabs.map(t => {
    const active = state.tab === t.id;
    const bg = active ? "#FFFFFF" : "transparent";
    const color = active ? DEFAULT_INK : INK_SOFT;
    const shadow = active ? "0 1px 3px rgba(46,36,64,0.08)" : "none";
    return `<button data-action="set-tab" data-id="${t.id}" style="background:${bg};color:${color};box-shadow:${shadow};">${t.icon}${t.label}</button>`;
  }).join("");
  return `<nav class="tabs" style="background:${SURFACE};">${buttons}</nav>`;
}

function renderHoje(INK, INK_SOFT, ON_INK, isToday, today){
  let out = '<section>';

  if (reminderDue()){
    out += `<div class="reminder-banner" style="background:#FFFFFF;border:1.5px solid ${DEFAULT_PAPER_LINE};">
      <span style="color:${DEFAULT_INK};display:flex;">${ICONS.bell}</span>
      <span style="color:${DEFAULT_INK};">Lembrete: hora de cuidar de você — não esqueça dos hormônios 💊</span>
    </div>`;
  }

  const weekdayStr = state.selectedDate.toLocaleDateString("pt-BR", { weekday: "long", month: "long" });
  out += `<div class="date-row">
    <div>
      <p class="font-display date-num" style="color:${INK};">${state.selectedDate.getDate()}</p>
      <p class="weekday" style="color:${INK_SOFT};">${isToday ? "Hoje · " : ""}${esc(weekdayStr)}</p>
    </div>
    ${!isToday ? `<button class="back-today" data-action="go-today" style="color:${GOLD};border:1px solid ${GOLD};">voltar para hoje</button>` : ""}
  </div>`;

  out += `<p class="hint" style="color:${INK_SOFT};">Como seu gênero se sentiu? <span style="opacity:.7;">(toque de novo para desmarcar)</span></p>`;

  out += '<div class="swatch-grid">';
  IDENTITIES.forEach(it => {
    const selected = state.draftIdentity === it.id;
    const cardBg = selected ? `${it.deep}1F` : "#FFFFFF";
    const cardBorder = selected ? it.deep : DEFAULT_PAPER_LINE;
    const dropBorder = it.border ? it.border : `${it.deep}33`;
    const boxShadow = selected ? `0 0 0 3px ${it.deep}33` : "none";
    const labelColor = selected ? it.deep : DEFAULT_INK_SOFT;
    out += `<button class="swatch-btn" data-action="toggle-identity" data-id="${it.id}" style="background:${cardBg};border-color:${cardBorder};">
      <span class="drop" style="background:${it.color};border:1.5px solid ${dropBorder};box-shadow:${boxShadow};"></span>
      <span class="swatch-label" style="color:${labelColor};">${esc(it.label)}</span>
    </button>`;
  });
  out += '</div>';

  if (state.settings.usesHormones){
    const hOn = state.draftHormone;
    out += `<div class="hormone-today-row" style="background:#FFFFFF;border:1.5px solid ${DEFAULT_PAPER_LINE};">
      <span style="font-size:13px;color:${DEFAULT_INK};display:flex;align-items:center;gap:6px;">${ICONS.pill} Usei hormônio hoje</span>
      <button class="toggle" data-action="toggle-hormone-today" style="background:${hOn ? DEFAULT_INK : DEFAULT_PAPER_LINE};" aria-label="Usei hormônio hoje">
        <span class="knob" style="left:${hOn ? "19px" : "2.5px"};"></span>
      </button>
    </div>`;
  }

  out += `<p class="hint" style="font-size:14px;margin-bottom:8px;color:${INK_SOFT};">Alguma nota para o dia? <span style="opacity:.7;">(opcional)</span></p>`;
  out += `<textarea id="note-input" rows="4" placeholder="Como foi, o que percebeu, o que ajudou..." style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK};">${esc(state.draftNote)}</textarea>`;

  const canSave = !!state.draftIdentity;
  const saveBg = canSave ? INK : DEFAULT_PAPER_LINE;
  const saveColor = canSave ? ON_INK : DEFAULT_INK_SOFT;
  out += `<div class="action-row">
    <button class="btn-save" data-action="save-entry" style="background:${saveBg};color:${saveColor};cursor:${canSave ? "pointer" : "not-allowed"};">
      ${state.savedFlash ? ICONS.check + " Salvo" : "Salvar dia"}
    </button>`;
  if (state.entries[dateKey(state.selectedDate)]){
    out += `<button class="btn-delete" data-action="delete-entry" style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK_SOFT};" aria-label="Apagar registro do dia">${ICONS.trash}</button>`;
  }
  out += '</div>';

  if (state.storageError){
    out += `<p class="storage-err">Não consegui salvar agora. Tente novamente em instantes.</p>`;
  }

  /* settings card */
  const hormOn = state.settings.usesHormones;
  const remOn = state.settings.reminderEnabled;
  out += `<div class="settings-card" style="border-color:${DEFAULT_PAPER_LINE};">
    <div class="settings-row">
      <span class="settings-label" style="color:${DEFAULT_INK};">${ICONS.bell} Uso hormônios</span>
      <button class="toggle" data-action="toggle-hormones" style="background:${hormOn ? DEFAULT_INK : DEFAULT_PAPER_LINE};" aria-label="Uso hormônios">
        <span class="knob" style="left:${hormOn ? "19px" : "2.5px"};"></span>
      </button>
    </div>`;
  if (hormOn){
    out += `<div class="settings-sub" style="border-color:${DEFAULT_PAPER_LINE};">
      <div class="settings-row" style="margin-bottom:12px;">
        <span style="font-size:14px;color:${DEFAULT_INK};">Lembrete diário</span>
        <button class="toggle" data-action="toggle-reminder" style="background:${remOn ? DEFAULT_INK : DEFAULT_PAPER_LINE};" aria-label="Ativar lembrete diário">
          <span class="knob" style="left:${remOn ? "19px" : "2.5px"};"></span>
        </button>
      </div>`;
    if (remOn){
      out += `<div class="settings-time-row">
        <span class="settings-time-label" style="color:${DEFAULT_INK_SOFT};">Horário</span>
        <input type="time" id="time-input" value="${state.settings.reminderTime}" style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK};background:#FFFFFF;" />
      </div>
      <p class="settings-note" style="color:${DEFAULT_INK_SOFT};">
        A Maré lembrará você assim que abrir o app após o horário selecionado.
      </p>`;
    }
    out += `</div>`;
  }
  out += `</div>`;

  out += '</section>';
  return out;
}

function renderCalendario(INK_SOFT){
  const first = new Date(state.calYear, state.calMonth, 1);
  const startWeekday = first.getDay();
  const daysInMonth = new Date(state.calYear, state.calMonth + 1, 0).getDate();
  const today = startOfDay(new Date());

  let cells = "";
  for (let i = 0; i < startWeekday; i++) cells += '<div class="cal-cell-wrapper"></div>';
  for (let d = 1; d <= daysInMonth; d++){
    const date = new Date(state.calYear, state.calMonth, d);
    const k = dateKey(date);
    const entry = state.entries[k];
    const info = entry ? ident(entry.identity) : null;
    const isSel = dateKey(state.selectedDate) === k;
    const isTod = dateKey(today) === k;
    const bg = info ? info.color : "#FFFFFF";
    const color = info ? (info.textDark ? DEFAULT_INK : "#FFFFFF") : DEFAULT_INK_SOFT;
    let border;
    let boxShadow = "0 2px 4px rgba(0,0,0,0.03)";

    if (isSel) {
      border = `2.5px solid ${DEFAULT_INK}`;
      boxShadow = "0 2px 8px rgba(0,0,0,0.12)";
    } else if (isTod) {
      border = `2px solid ${GOLD}`;
    } else if (info && info.border) {
      border = `1.5px solid ${info.border}`;
    } else {
      border = `1.5px solid ${DEFAULT_PAPER_LINE}`;
    }

    const showHormoneBadge = state.settings.usesHormones && entry && entry.hormone;
    const badgeIcon = '<svg width="8" height="8" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><path d="m10.5 20.5 10-10a4.95 4.95 0 1 0-7-7l-10 10a4.95 4.95 0 1 0 7 7Z"/><path d="m8.5 8.5 7 7"/></svg>';
    const badge = showHormoneBadge
      ? `<span style="position:absolute;top:-4px;right:-4px;width:15px;height:15px;border-radius:50%;background:#FFFFFF;display:flex;align-items:center;justify-content:center;box-shadow:0 1px 3px rgba(0,0,0,0.25);pointer-events:none;color:${GOLD};z-index:2;">${badgeIcon}</span>`
      : "";
    cells += `<div class="cal-cell-wrapper">
      <button class="cal-cell" data-action="select-date" data-date="${date.toISOString()}" style="background:${bg};color:${color};border:${border};box-shadow:${boxShadow};">${d}</button>
      ${badge}
    </div>`;
  }

  const weekdayLabels = WEEKDAYS.map(w => `<span style="color:${DEFAULT_INK_SOFT};">${w}</span>`).join("");
  const legend = IDENTITIES.map(it => {
    const border = it.border ? `1px solid ${it.border}` : "none";
    return `<div class="legend-item">
      <span class="legend-dot" style="background:${it.color};border:${border};"></span>
      <span class="legend-label" style="color:${DEFAULT_INK_SOFT};">${esc(it.label)}</span>
    </div>`;
  }).join("") + (state.settings.usesHormones
    ? `<div class="legend-item">
        <span class="legend-dot" style="background:#FFFFFF;border:1px solid ${DEFAULT_PAPER_LINE};display:flex;align-items:center;justify-content:center;color:${GOLD};">
          <svg width="6" height="6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"><path d="m10.5 20.5 10-10a4.95 4.95 0 1 0-7-7l-10 10a4.95 4.95 0 1 0 7 7Z"/><path d="m8.5 8.5 7 7"/></svg>
        </span>
        <span class="legend-label" style="color:${DEFAULT_INK_SOFT};">Uso de hormônio</span>
      </div>`
    : "");

  return `<section>
    <div class="cal-nav">
      <button data-action="prev-month" style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK_SOFT};" aria-label="Mês anterior">${ICONS.chevronLeft}</button>
      <div class="cal-title font-display">${MONTHS[state.calMonth]} ${state.calYear}</div>
      <button data-action="next-month" style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK_SOFT};" aria-label="Próximo mês">${ICONS.chevronRight}</button>
    </div>
    <div class="cal-weekdays">${weekdayLabels}</div>
    <div class="cal-grid">${cells}</div>
    <div class="cal-legend">${legend}</div>
  </section>`;
}

function renderEstatisticas(INK, INK_SOFT, ON_INK){
  const ranges = [ { id: 7, label: "7 dias" }, { id: 30, label: "30 dias" }, { id: 90, label: "90 dias" }, { id: "all", label: "Tudo" } ];
  const chips = ranges.map(r => {
    const active = state.range === r.id;
    const bg = active ? INK : "#FFFFFF";
    const color = active ? ON_INK : DEFAULT_INK_SOFT;
    const border = active ? INK : DEFAULT_PAPER_LINE;
    return `<button class="chip" data-action="set-range" data-id="${r.id}" style="background:${bg};color:${color};border-color:${border};">${r.label}</button>`;
  }).join("");

  const today = startOfDay(new Date());
  const counts = { feminino: 0, agenero: 0, bigenero: 0, neutro: 0, masculino: 0 };
  let total = 0;
  Object.entries(state.entries).forEach(([k, v]) => {
    if (state.range !== "all"){
      const d = new Date(k + "T00:00:00");
      const diffDays = Math.round((today - d) / 86400000);
      if (diffDays < 0 || diffDays >= state.range) return;
    }
    if (counts[v.identity] !== undefined){ counts[v.identity]++; total++; }
  });

  let out = `<section><div class="range-row">${chips}</div>`;

  if (total === 0){
    out += `<div class="empty-state" style="border-color:${DEFAULT_PAPER_LINE};color:${DEFAULT_INK_SOFT};">
      Ainda não há registros nesse período. Volte para a aba "Hoje" e comece a anotar.
    </div>`;
  } else {
    const SEPARATOR = "rgba(255,255,255,0.75)";
    let bar = "";
    IDENTITIES.forEach(it => {
      const pct = total ? (counts[it.id] / total) * 100 : 0;
      if (pct === 0) return;
      bar += `<div style="width:${pct}%;background:${it.color};border-right:1px solid ${SEPARATOR};" title="${esc(it.label)}: ${Math.round(pct)}%"></div>`;
    });
    out += `<div class="spectrum-bar" style="border-color:${DEFAULT_PAPER_LINE};">${bar}</div>`;

    let rows = "";
    IDENTITIES.forEach(it => {
      const count = counts[it.id];
      const pct = total ? Math.round((count / total) * 100) : 0;
      rows += `<div class="stat-row">
        <span class="stat-dot" style="background:${it.color};${it.border ? `border:1px solid ${it.border};` : ""}"></span>
        <span class="stat-label" style="color:${INK};">${esc(it.label)}</span>
        <div class="stat-track" style="background:${THEMES[themeState.displayId].surface};">
          <div class="stat-fill" style="width:${pct}%;background:${it.color};"></div>
        </div>
        <span class="stat-value" style="color:${INK_SOFT};">${count} · ${pct}%</span>
      </div>`;
    });
    out += rows;
    out += `<p class="stat-total" style="color:${INK_SOFT};">${total} ${total === 1 ? "dia registrado" : "dias registrados"} no período.</p>`;
  }

  out += `<div class="reset-section" style="border-color:${DEFAULT_PAPER_LINE};">`;
  if (!state.confirmingReset){
    out += `<button data-action="ask-reset" style="color:${INK_SOFT};">Apagar todos os dados</button>`;
  } else {
    out += `<div style="font-size:12px;display:flex;align-items:center;gap:12px;color:${INK_SOFT};">
      <span>Isso apaga todo o histórico. Tem certeza?</span>
      <button data-action="confirm-reset" style="color:#B8628F;font-weight:600;">Sim, apagar</button>
      <button data-action="cancel-reset">Cancelar</button>
    </div>`;
  }
  out += `</div></section>`;
  return out;
}

/* ---------- events (delegated) ---------- */
document.getElementById("app").addEventListener("click", (e) => {
  const el = e.target.closest("[data-action]");
  if (!el) return;
  const action = el.dataset.action;
  const id = el.dataset.id;
  const date = el.dataset.date;
  switch (action){
    case "select-date": selectDate(date); break;
    case "go-today": goToday(); break;
    case "set-tab": setTab(id); break;
    case "toggle-identity": toggleIdentity(id); break;
    case "save-entry": saveEntry(); break;
    case "delete-entry": deleteEntry(); break;
    case "toggle-hormones": updateSettings({ usesHormones: !state.settings.usesHormones }); break;
    case "toggle-hormone-today": state.draftHormone = !state.draftHormone; render(); break;
    case "toggle-reminder": updateSettings({ reminderEnabled: !state.settings.reminderEnabled }); break;
    case "prev-month": prevMonth(); break;
    case "next-month": nextMonth(); break;
    case "set-range": setRange(id === "all" ? "all" : Number(id)); break;
    case "ask-reset": state.confirmingReset = true; render(); break;
    case "confirm-reset": resetAll(); break;
    case "cancel-reset": state.confirmingReset = false; render(); break;
  }
});
document.getElementById("app").addEventListener("input", (e) => {
  if (e.target.id === "note-input") state.draftNote = e.target.value;
});
document.getElementById("app").addEventListener("change", (e) => {
  if (e.target.id === "time-input") updateSettings({ reminderTime: e.target.value });
});

/* ---------- boot ---------- */
loadAll();
</script>
</body>
</html>
