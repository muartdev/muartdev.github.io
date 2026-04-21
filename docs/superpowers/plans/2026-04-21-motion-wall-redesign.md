# Motion-Led Editorial Portfolio Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rebuild the broken portfolio draft into a cleaner single-file editorial site with a typographic motion hero and a stable textured proof wall.

**Architecture:** Keep everything inside `index.html`, but treat it as three focused systems: design tokens and layout CSS, semantic single-page markup, and a lightweight i18n/theme/reveal script. Replace the mascot experiment entirely and rebuild the hero/proof wall around stronger proportions and mobile-safe width rules.

**Tech Stack:** Static HTML, CSS, vanilla JavaScript, Google Fonts

---

### Task 1: Reset the Hero Architecture

**Files:**
- Modify: `index.html`
- Test: `index.html` in browser, translation key check via `node -e`

- [ ] **Step 1: Remove the mascot-specific CSS and replace it with a cleaner hero system**

```css
.hero {
  display: grid;
  gap: 22px;
}

.hero-grid {
  display: grid;
  gap: 18px;
}

.hero-kicker {
  color: var(--accent-signal);
  font-size: 0.78rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
}

.hero-title-row {
  display: flex;
  align-items: end;
  gap: 14px;
  flex-wrap: wrap;
}

.motion-rail {
  overflow: hidden;
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}
```

- [ ] **Step 2: Replace the mascot markup with a typographic hero**

```html
<section class="hero" id="top">
  <div class="hero-grid reveal">
    <div class="hero-kicker" data-i18n="hero.kicker">shipping thoughtful systems</div>

    <div class="hero-title-row">
      <h1 class="hero-name">Murat</h1>
      <span class="hero-role" data-i18n="hero.role">product engineer</span>
    </div>

    <p class="hero-lead" data-i18n="hero.text1" data-i18n-html>...</p>
  </div>

  <div class="motion-rail reveal" aria-hidden="true">
    <div class="motion-rail-track">
      <span>shipping across iOS / web / backend</span>
    </div>
  </div>
</section>
```

- [ ] **Step 3: Add lightweight CSS-only motion for the rail**

```css
.motion-rail-track {
  display: inline-flex;
  gap: 28px;
  white-space: nowrap;
  animation: signal-drift 18s linear infinite;
}

@keyframes signal-drift {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}
```

- [ ] **Step 4: Run the translation key check**

Run:

```bash
node -e "const fs=require('fs'); const html=fs.readFileSync('index.html','utf8'); const attr=[...html.matchAll(/data-i18n=\"([^\"]+)\"/g)].map(m=>m[1]); const en=html.match(/en:\s*\{([\s\S]*?)\n\s*\},\n\s*tr:/)[1]; const tr=html.match(/tr:\s*\{([\s\S]*?)\n\s*\}\n\s*\};/)[1]; const keys=s=>new Set([...s.matchAll(/\"([^\"]+)\"\s*:/g)].map(m=>m[1])); console.log(JSON.stringify({missingEn:[...new Set(attr.filter(k=>!keys(en).has(k)))],missingTr:[...new Set(attr.filter(k=>!keys(tr).has(k)))]},null,2));"
```

Expected:

```json
{
  "missingEn": [],
  "missingTr": []
}
```

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "Rebuild portfolio hero layout"
```

### Task 2: Rebuild the Proof Wall and Page Rhythm

**Files:**
- Modify: `index.html`
- Test: `index.html` in browser, `git diff --check`

- [ ] **Step 1: Replace the broken wall layout rules with mobile-safe breakout sizing**

```css
.proof-wall-section {
  width: min(1040px, calc(100vw - 28px));
  margin: 0 auto;
}

.proof-wall {
  padding: 26px 22px;
  border-radius: 24px;
  overflow: hidden;
}

.wall-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 28px 18px;
}
```

- [ ] **Step 2: Recompose the proof wall content as a curated text board**

```html
<section class="proof-wall-section reveal" aria-labelledby="wallTitle">
  <div class="proof-wall">
    <div class="wall-head">
      <span class="wall-label" id="wallTitle" data-i18n="wall.label">selected signals</span>
      <p class="wall-copy" data-i18n="wall.meta">real products / iOS / web / backend</p>
    </div>

    <div class="wall-grid">
      <article class="wall-mark wall-mark-xl"><strong>MindShelf</strong><span>...</span></article>
      <article class="wall-mark"><strong>Softmendil</strong><span>...</span></article>
    </div>
  </div>
</section>
```

- [ ] **Step 3: Restore calm section rhythm below the wall**

```css
section + section {
  margin-top: 72px;
}

.section-note,
.item-desc,
.contact-copy {
  max-width: 60ch;
}
```

- [ ] **Step 4: Run formatting safety check**

Run:

```bash
git diff --check
```

Expected:

```text
no output
```

- [ ] **Step 5: Commit**

```bash
git add index.html
git commit -m "Rebuild textured proof wall layout"
```

### Task 3: Finalize i18n, theme behavior, and responsive polish

**Files:**
- Modify: `index.html`
- Test: `index.html` in browser, `git status --short`

- [ ] **Step 1: Update translation keys for the new hero and wall copy**

```js
en: {
  "hero.kicker": "shipping thoughtful systems",
  "wall.label": "selected signals",
  "wall.meta": "real products / iOS / web / backend"
}
```

- [ ] **Step 2: Keep theme and language toggles unchanged while removing dead mascot logic**

```js
document.getElementById("langToggle")?.addEventListener("click", toggleLanguage);
document.getElementById("themeToggle")?.addEventListener("click", toggleTheme);
initTheme();
initLanguage();
initReveal();
initActiveNav();
```

- [ ] **Step 3: Add small-screen rules so the hero and wall never overflow**

```css
@media (max-width: 640px) {
  .hero-title-row,
  .cta-group,
  .proof {
    gap: 10px;
  }

  .wall-grid {
    grid-template-columns: 1fr;
  }
}
```

- [ ] **Step 4: Run final checks**

Run:

```bash
git status --short
```

Expected:

```text
M index.html
M docs/superpowers/plans/2026-04-21-motion-wall-redesign.md
```

- [ ] **Step 5: Commit**

```bash
git add index.html docs/superpowers/plans/2026-04-21-motion-wall-redesign.md
git commit -m "Finalize editorial portfolio redesign"
```
