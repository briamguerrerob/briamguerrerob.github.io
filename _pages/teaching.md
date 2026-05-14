---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,600;1,9..144,300&family=DM+Sans:wght@300;400;500&display=swap');

  :root {
    --pucmm: #003DA5;
    --pucmm-light: #dce8ff;
    --pucmm-mid: #b0c8f5;
    --intec: #c8102e;
    --intec-light: #fde8eb;
    --intec-mid: #f5b0bb;
    --gray-50: #f8f9fa;
    --gray-100: #f0f2f5;
    --gray-200: #e2e6ea;
    --gray-500: #6b7280;
    --gray-800: #1f2937;
    --radius: 14px;
    --shadow: 0 2px 12px rgba(0,0,0,0.07), 0 1px 3px rgba(0,0,0,0.05);
    --shadow-hover: 0 8px 28px rgba(0,0,0,0.12), 0 2px 8px rgba(0,0,0,0.07);
  }

  .teaching-page * { box-sizing: border-box; }

  .teaching-page {
    font-family: 'DM Sans', sans-serif;
    color: var(--gray-800);
    max-width: 860px;
    margin: 0 auto;
    padding: 0 0 4rem;
  }

  /* ── Institution Header ─────────────────────────── */
  .inst-header {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    margin: 2.8rem 0 1.2rem;
    padding-bottom: 0.7rem;
    border-bottom: 2px solid var(--color);
  }
  .inst-header img { height: 30px; width: auto; }
  .inst-header h2 {
    font-family: 'Fraunces', serif;
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--color);
    margin: 0;
    letter-spacing: -0.01em;
  }

  /* ── Course Block ───────────────────────────────── */
  .course-block {
    border: 1.5px solid var(--color-mid);
    border-radius: var(--radius);
    margin-bottom: 1.1rem;
    background: #fff;
    box-shadow: var(--shadow);
    transition: box-shadow 0.25s ease;
    overflow: hidden;
  }
  .course-block:hover { box-shadow: var(--shadow-hover); }

  .course-toggle {
    width: 100%;
    background: none;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.1rem 1.3rem;
    text-align: left;
    gap: 1rem;
    transition: background 0.18s ease;
  }
  .course-toggle:hover { background: var(--color-ultra-light); }

  .course-toggle-left { display: flex; align-items: center; gap: 0.8rem; }

  .course-pill {
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    background: var(--color-light);
    color: var(--color);
    border-radius: 20px;
    padding: 0.22em 0.7em;
    white-space: nowrap;
  }

  .course-title {
    font-family: 'Fraunces', serif;
    font-size: 1.05rem;
    font-weight: 600;
    color: var(--gray-800);
    margin: 0;
    line-height: 1.3;
  }

  .course-chevron {
    width: 22px; height: 22px;
    border-radius: 50%;
    border: 1.5px solid var(--color-mid);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
    transition: transform 0.3s ease, background 0.2s ease;
    color: var(--color);
  }
  .course-block.open .course-chevron {
    transform: rotate(180deg);
    background: var(--color-light);
  }

  .course-body {
    display: none;
    padding: 0 1.3rem 1.2rem;
    animation: fadeSlide 0.22s ease;
  }
  .course-block.open .course-body { display: block; }

  @keyframes fadeSlide {
    from { opacity: 0; transform: translateY(-6px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── Term Accordion ─────────────────────────────── */
  .terms-list { display: flex; flex-direction: column; gap: 0.55rem; }

  .term-item {
    border: 1px solid var(--color-mid);
    border-radius: 10px;
    overflow: hidden;
    background: var(--gray-50);
  }

  .term-toggle {
    width: 100%;
    background: none;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.7rem 1rem;
    text-align: left;
    transition: background 0.18s ease;
  }
  .term-toggle:hover { background: var(--color-ultra-light); }

  .term-toggle-left { display: flex; align-items: center; gap: 0.6rem; }

  .term-badge {
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    background: var(--color);
    color: #fff;
    border-radius: 4px;
    padding: 0.18em 0.55em;
  }

  .term-label {
    font-size: 0.88rem;
    font-weight: 500;
    color: var(--gray-800);
  }

  .term-meta {
    font-size: 0.75rem;
    color: var(--gray-500);
    font-style: italic;
  }

  .term-chevron {
    color: var(--color);
    transition: transform 0.25s ease;
    flex-shrink: 0;
  }
  .term-item.open .term-chevron { transform: rotate(180deg); }

  .term-body {
    display: none;
    padding: 0.3rem 1rem 0.9rem;
    border-top: 1px solid var(--color-mid);
    animation: fadeSlide 0.18s ease;
  }
  .term-item.open .term-body { display: block; }

  /* ── Syllabus link ──────────────────────────────── */
  .syllabus-link {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.8rem;
    color: var(--color);
    text-decoration: none;
    font-weight: 500;
    margin: 0.55rem 0 0.8rem;
    padding: 0.3em 0.75em;
    border: 1px solid var(--color-mid);
    border-radius: 6px;
    background: var(--color-light);
    transition: background 0.18s ease;
  }
  .syllabus-link:hover { background: var(--color-mid); text-decoration: none; }

  /* ── Unit Accordion ─────────────────────────────── */
  .units-list { display: flex; flex-direction: column; gap: 0.35rem; }

  .unit-item {
    border: 1px solid var(--gray-200);
    border-radius: 8px;
    overflow: hidden;
    background: #fff;
  }

  .unit-toggle {
    width: 100%;
    background: none;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.55rem 0.85rem;
    text-align: left;
    gap: 0.5rem;
    transition: background 0.15s ease;
  }
  .unit-toggle:hover { background: var(--gray-100); }

  .unit-num {
    font-size: 0.66rem;
    font-weight: 700;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    color: var(--color);
    background: var(--color-light);
    border-radius: 3px;
    padding: 0.15em 0.45em;
    flex-shrink: 0;
  }

  .unit-name {
    font-size: 0.83rem;
    font-weight: 400;
    color: var(--gray-800);
    flex: 1;
    line-height: 1.35;
  }

  .unit-chevron {
    color: var(--gray-500);
    transition: transform 0.2s ease;
    flex-shrink: 0;
  }
  .unit-item.open .unit-chevron { transform: rotate(180deg); }

  .unit-body {
    display: none;
    padding: 0.4rem 0.85rem 0.65rem;
    border-top: 1px solid var(--gray-200);
    background: var(--gray-50);
    animation: fadeSlide 0.15s ease;
  }
  .unit-item.open .unit-body { display: block; }

  .unit-links { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 0.2rem; }

  .unit-link {
    display: inline-flex;
    align-items: center;
    gap: 0.3rem;
    font-size: 0.78rem;
    color: var(--color);
    text-decoration: none;
    padding: 0.28em 0.65em;
    border: 1px solid var(--color-mid);
    border-radius: 20px;
    background: #fff;
    font-weight: 500;
    transition: background 0.15s ease, border-color 0.15s ease;
  }
  .unit-link:hover {
    background: var(--color-light);
    border-color: var(--color);
    text-decoration: none;
  }

  /* ── Extras (práctica, evaluaciones) ───────────── */
  .extras-section { margin-top: 0.75rem; }

  .extras-group {
    border: 1px dashed var(--gray-200);
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: 0.4rem;
    background: #fff;
  }

  .extras-toggle {
    width: 100%;
    background: none;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.5rem 0.85rem;
    text-align: left;
    transition: background 0.15s ease;
    gap: 0.5rem;
  }
  .extras-toggle:hover { background: var(--gray-100); }

  .extras-label {
    font-size: 0.8rem;
    font-weight: 500;
    color: var(--gray-800);
  }

  .extras-chevron {
    color: var(--gray-500);
    transition: transform 0.2s ease;
    flex-shrink: 0;
  }
  .extras-group.open .extras-chevron { transform: rotate(180deg); }

  .extras-body {
    display: none;
    padding: 0.35rem 0.85rem 0.65rem;
    border-top: 1px dashed var(--gray-200);
    animation: fadeSlide 0.15s ease;
  }
  .extras-group.open .extras-body { display: block; }

  .extras-links { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-top: 0.15rem; }
</style>

<div class="teaching-page">

<!-- ══════════════════════════════════════════════════
     PUCMM
═══════════════════════════════════════════════════ -->

<div class="inst-header" style="--color: #003DA5;">
  <img src="https://briamguerrerob.github.io/images/Logo PUCMM.png" alt="PUCMM">
  <h2>Pontificia Universidad Católica Madre y Maestra</h2>
</div>

<!-- ── Microeconomía I · PUCMM ───────────────────── -->
<div class="course-block" style="
  --color: #003DA5;
  --color-light: #dce8ff;
  --color-mid: #b0c8f5;
  --color-ultra-light: #f0f5ff;
">
  <button class="course-toggle" onclick="toggleBlock(this)">
    <div class="course-toggle-left">
      <span class="course-pill">ECO-232-T</span>
      <span class="course-title">Microeconomía I</span>
    </div>
    <div class="course-chevron">
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
  </button>
  <div class="course-body">
    <div class="terms-list">

      <!-- 2025-2026 Período 3 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2025-26</span>
            <span class="term-label">Período 3</span>
            <span class="term-meta">Profesor</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/micro1_program_pucmm.pdf" target="_blank">
            📄 Programa y calendario
          </a>
          <div class="units-list">
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.0</span>
                <span class="unit-name">Introducción y herramientas matemáticas</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body">
                <div class="unit-links">
                  <a class="unit-link" href="https://briamguerrerob.github.io/files/main_U0_intro_matematica_pucmm.pdf" target="_blank">🖥️ Diapositivas</a>
                </div>
              </div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.1</span>
                <span class="unit-name">Nociones básicas de microeconomía - demanda, oferta y el mercado</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body">
                <div class="unit-links">
                  <a class="unit-link" href="https://briamguerrerob.github.io/files/main_unidad1_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>


<!-- ══════════════════════════════════════════════════
     INTEC
═══════════════════════════════════════════════════ -->

<div class="inst-header" style="--color: #c8102e;">
  <img src="https://briamguerrerob.github.io/images/logo_intec.png" alt="INTEC">
  <h2>Instituto Tecnológico de Santo Domingo (INTEC)</h2>
</div>


<!-- ── Microeconomía I · INTEC ───────────────────── -->
<div class="course-block" style="
  --color: #c8102e;
  --color-light: #fde8eb;
  --color-mid: #f5b0bb;
  --color-ultra-light: #fff5f6;
">
  <button class="course-toggle" onclick="toggleBlock(this)">
    <div class="course-toggle-left">
      <span class="course-pill">ECO351</span>
      <span class="course-title">Microeconomía I</span>
    </div>
    <div class="course-chevron">
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
  </button>
  <div class="course-body">
    <div class="terms-list">

      <!-- 2025-T4 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2025-T4</span>
            <span class="term-label">Trimestre 4, 2025</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/syllabus_micro1.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.1</span>
                <span class="unit-name">El análisis microeconómico y los principios en que se fundamenta</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec1_sem1_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec1_notes_sem1_micro1.pdf" target="_blank">📝 Apuntes</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.2</span>
                <span class="unit-name">La restricción presupuestaria</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec2_sem1_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec2_notes_sem1_micro1.pdf" target="_blank">📝 Apuntes</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.3.1</span>
                <span class="unit-name">Las preferencias (parte I)</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec3_sem2_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.3.2</span>
                <span class="unit-name">Las preferencias (parte II)</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec4_sem2_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.4</span>
                <span class="unit-name">La utilidad</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec5_and_6_sem3_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.5</span>
                <span class="unit-name">La elección del consumidor</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/lec7_and_8_sem4_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.6</span>
                <span class="unit-name">La demanda del consumidor</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem5_and_6_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.7</span>
                <span class="unit-name">Las preferencias reveladas</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem6_and_7_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.8.1</span>
                <span class="unit-name">La ecuación de Slutsky</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem7_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.8.2–9</span>
                <span class="unit-name">Revisión Slutsky y dotaciones iniciales del consumidor</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem7_2_micro1.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.10.1</span>
                <span class="unit-name">Elección intertemporal</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem_8_micro1_slides.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.10.2–11</span>
                <span class="unit-name">Mercados de activos, incertidumbre y activos riesgosos</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem_9_micro1_slides.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
            <div class="unit-item">
              <button class="unit-toggle" onclick="toggleBlock(this)">
                <span class="unit-num">U.12</span>
                <span class="unit-name">Excedente del consumidor y demanda de mercado</span>
                <svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="unit-body"><div class="unit-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/sem_9_micro1_slides2.pdf" target="_blank">🖥️ Diapositivas</a>
              </div></div>
            </div>
          </div>
          <div class="extras-section">
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)">
                <span class="extras-label">📘 Prácticas y guías de ejercicios</span>
                <svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="extras-body"><div class="extras-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps1_sem2_micro1.pdf" target="_blank">Práctica 1</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps2_sem4_micro1.pdf" target="_blank">Práctica 2</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps3_sem7_micro1.pdf" target="_blank">Práctica 3</a>
              </div></div>
            </div>
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)">
                <span class="extras-label">📊 Evaluaciones</span>
                <svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
              </button>
              <div class="extras-body"><div class="extras-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/final_project_micro1.pdf" target="_blank">Proyecto final</a>
              </div></div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>


<!-- ── Microeconomía II · INTEC ──────────────────── -->
<div class="course-block" style="
  --color: #c8102e;
  --color-light: #fde8eb;
  --color-mid: #f5b0bb;
  --color-ultra-light: #fff5f6;
">
  <button class="course-toggle" onclick="toggleBlock(this)">
    <div class="course-toggle-left">
      <span class="course-pill">ECO304</span>
      <span class="course-title">Microeconomía II</span>
    </div>
    <div class="course-chevron">
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
  </button>
  <div class="course-body">
    <div class="terms-list">

      <!-- 2025-T4 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2025-T4</span>
            <span class="term-label">Trimestre 4, 2025</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/syllabus_micro2.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1.1</span><span class="unit-name">Teoría de la demanda</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec1_sem1_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec1_notes_sem1_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1.2</span><span class="unit-name">Las preferencias reveladas</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec2_sem1_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec2_notes_sem1_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.2.1</span><span class="unit-name">La ecuación de Slutsky</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec3_sem2_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec3_notes_sem2_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.2.2</span><span class="unit-name">Revisión Slutsky y dotaciones iniciales del consumidor</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec4_sem2_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec4_notes_sem2_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.3</span><span class="unit-name">Elección intertemporal</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec5_and_6_sem3_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec5_and_6_notes_sem3_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.4</span><span class="unit-name">Teoría de la empresa</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec7_and_8_sem4_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec7_and_8_notes_sem4_micro2.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.5</span><span class="unit-name">Oferta de la empresa y la industria</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec9_and_10_sem5_and_6_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec9_and_10_sem5_and_6_micro2_notes.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.6</span><span class="unit-name">Monopolio, conducta del monopolio y mercado de factores</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec11_and_12_sem7_micro2.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/lec11_and_12_sem7_micro2_notes.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.7</span><span class="unit-name">Oligopolio e intercambio</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/sem_8_micro2_slides.pdf" target="_blank">🖥️ Diapositivas</a><a class="unit-link" href="https://briamguerrerob.github.io/files/sem_8_micro2_notes.pdf" target="_blank">📝 Apuntes</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.8-9</span><span class="unit-name">Introducción a la teoría de juegos y externalidades</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/sem_9_micro2_slides.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.10</span><span class="unit-name">Bienes públicos</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/sem_9_micro2_slides2.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
          </div>
          <div class="extras-section">
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)"><span class="extras-label">📘 Prácticas y guías de ejercicios</span><svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
              <div class="extras-body"><div class="extras-links">
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps1_sem2_micro2.pdf" target="_blank">Práctica 1</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps2_sem4_micro2.pdf" target="_blank">Práctica 2</a>
                <a class="unit-link" href="https://briamguerrerob.github.io/files/ps3_sem7_micro2.pdf" target="_blank">Práctica 3</a>
              </div></div>
            </div>
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)"><span class="extras-label">📊 Evaluaciones</span><svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
              <div class="extras-body"><div class="extras-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/final_project_micro2.pdf" target="_blank">Proyecto final</a></div></div>
            </div>
          </div>
        </div>
      </div>

      <!-- 2026-T1 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2026-T1</span>
            <span class="term-label">Trimestre 1, 2026</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/syllabus_micro2_2026t1.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.0</span><span class="unit-name">Repaso de microeconomía I: teoría del consumidor</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/review_micro1.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1-2</span><span class="unit-name">Tecnología, beneficios y costos (Teoría de la firma I)</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/lec02_sem1_micro2_2026t1.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.2–3</span><span class="unit-name">Curvas de costo, oferta de la firma e industria (Teoría de la firma II)</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U2U3_teoria_firma_II.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.4</span><span class="unit-name">Equilibrio general e intercambio</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U4_equilibrio_general.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.5</span><span class="unit-name">Monopolio, comportamiento del monopolio y mercado de factores</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U5_monopolio.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.6</span><span class="unit-name">Oligopolio</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U6_oligopolio.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.7</span><span class="unit-name">Introducción a la teoría de juegos</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U7_teoria_juegos.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.8</span><span class="unit-name">Información asimétrica</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U8_info_asimetrica.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.9</span><span class="unit-name">Externalidades</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U9_externalidades.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.10</span><span class="unit-name">Bienes públicos</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U10_bienes_publicos.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
          </div>
          <div class="extras-section">
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)"><span class="extras-label">📊 Evaluaciones</span><svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
              <div class="extras-body"><div class="extras-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/asignacion_micro2.pdf" target="_blank">Proyecto final</a></div></div>
            </div>
          </div>
        </div>
      </div>

      <!-- 2026-T2 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2026-T2</span>
            <span class="term-label">Trimestre 2, 2026</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/syllabus_micro2_2026t2.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.0</span><span class="unit-name">Repaso de microeconomía I: teoría del consumidor</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/review_micro1_2026t2.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1-2</span><span class="unit-name">Tecnología, beneficios y costos (Teoría de la firma I)</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U1U2_teoria_firma_I_2026t2.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>


<!-- ── Macroeconomía I · INTEC ───────────────────── -->
<div class="course-block" style="
  --color: #c8102e;
  --color-light: #fde8eb;
  --color-mid: #f5b0bb;
  --color-ultra-light: #fff5f6;
">
  <button class="course-toggle" onclick="toggleBlock(this)">
    <div class="course-toggle-left">
      <span class="course-pill">ECO305</span>
      <span class="course-title">Macroeconomía I</span>
    </div>
    <div class="course-chevron">
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
  </button>
  <div class="course-body">
    <div class="terms-list">

      <!-- 2026-T2 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2026-T2</span>
            <span class="term-label">Trimestre 2, 2026</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/macro1_syllabus_2026t2.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.0</span><span class="unit-name">Repaso de herramientas matemáticas</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/U0_Repaso_Matematico_2026t2.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1</span><span class="unit-name">Introducción y medición macroeconómica</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/U1_Medicion_2026t2.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>


<!-- ── Macroeconomía II · INTEC ──────────────────── -->
<div class="course-block" style="
  --color: #c8102e;
  --color-light: #fde8eb;
  --color-mid: #f5b0bb;
  --color-ultra-light: #fff5f6;
">
  <button class="course-toggle" onclick="toggleBlock(this)">
    <div class="course-toggle-left">
      <span class="course-pill">ECO306</span>
      <span class="course-title">Macroeconomía II</span>
    </div>
    <div class="course-chevron">
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
  </button>
  <div class="course-body">
    <div class="terms-list">

      <!-- 2026-T1 -->
      <div class="term-item">
        <button class="term-toggle" onclick="toggleBlock(this)">
          <div class="term-toggle-left">
            <span class="term-badge">2026-T1</span>
            <span class="term-label">Trimestre 1, 2026</span>
            <span class="term-meta">Profesor adjunto</span>
          </div>
          <svg class="term-chevron" width="14" height="14" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </button>
        <div class="term-body">
          <a class="syllabus-link" href="https://briamguerrerob.github.io/files/syllabus_macro2_2026t1.pdf" target="_blank">📄 Programa y calendario</a>
          <div class="units-list">
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.0</span><span class="unit-name">Repaso de Macroeconomía I: optimización dinámica</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/review_macro1.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.1</span><span class="unit-name">Incertidumbre, expectativas y métodos de solución DSGE</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/U1_DSGE_Foundations.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.2</span><span class="unit-name">Teoría de ciclos económicos reales (RBC)</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/U2_RBC.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.3</span><span class="unit-name">Rigideces nominales</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U3_rigideces_nominales.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.4</span><span class="unit-name">Modelo nuevo keynesiano</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U4_modelo_NK.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.5</span><span class="unit-name">Política monetaria</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U5_politica_monetaria.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
            <div class="unit-item"><button class="unit-toggle" onclick="toggleBlock(this)"><span class="unit-num">U.6</span><span class="unit-name">Política fiscal y extensiones</span><svg class="unit-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button><div class="unit-body"><div class="unit-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/main_U6_politica_fiscal.pdf" target="_blank">🖥️ Diapositivas</a></div></div></div>
          </div>
          <div class="extras-section">
            <div class="extras-group">
              <button class="extras-toggle" onclick="toggleBlock(this)"><span class="extras-label">📊 Evaluaciones</span><svg class="extras-chevron" width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 4l4 4 4-4" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
              <div class="extras-body"><div class="extras-links"><a class="unit-link" href="https://briamguerrerob.github.io/files/asignacion_macro2.pdf" target="_blank">Proyecto final</a></div></div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>

</div><!-- end .teaching-page -->

<script>
function toggleBlock(btn) {
  const block = btn.parentElement;
  block.classList.toggle('open');
}
</script>
