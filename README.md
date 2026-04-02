[UD4_Guardianes_v4_FINAL (9).html](https://github.com/user-attachments/files/26450089/UD4_Guardianes_v4_FINAL.9.html)[Uploading UD4_Guardianes_v4_FINAL <!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UD4 | ONCE NOS ENTRENA | Guardianes de Hawkins</title>
<link href="https://fonts.googleapis.com/css2?family=Creepster&family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --red: #c0392b;
  --red-dark: #7b241c;
  --red-glow: #e74c3c;
  --blue: #1a6fa0;
  --blue-light: #3498db;
  --cyan: #00d4ff;
  --green: #00ff88;
  --yellow: #f39c12;
  --orange: #e67e22;
  --purple: #8e44ad;
  --dark: #0a0a0f;
  --dark2: #111118;
  --dark3: #1a1a2e;
  --panel: #12121f;
  --panel2: #1e1e33;
  --text: #e8e8f0;
  --text-dim: #8888aa;
  --border: #2a2a4a;
  --glow-red: 0 0 20px rgba(192,57,43,0.6);
  --glow-cyan: 0 0 20px rgba(0,212,255,0.5);
  --glow-green: 0 0 20px rgba(0,255,136,0.5);
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  background: var(--dark);
  color: var(--text);
  font-family: 'Nunito', sans-serif;
  min-height: 100vh;
  overflow-x: hidden;
}

/* NOISE TEXTURE */
body::before {
  content:'';
  position:fixed; inset:0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
  pointer-events:none;
  z-index:0;
}

/* HEADER */
.header {
  position: relative;
  text-align: center;
  padding: 30px 20px 20px;
  background: linear-gradient(180deg, #0d0010 0%, var(--dark) 100%);
  border-bottom: 2px solid var(--red);
  box-shadow: 0 4px 30px rgba(192,57,43,0.4);
  overflow: hidden;
}

.header::before {
  content: '';
  position: absolute;
  top: -50px; left: 50%;
  transform: translateX(-50%);
  width: 600px; height: 300px;
  background: radial-gradient(ellipse, rgba(192,57,43,0.2) 0%, transparent 70%);
  pointer-events: none;
}

.header-eyebrow {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: var(--red-glow);
  letter-spacing: 4px;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.header-title {
  font-family: 'Creepster', cursive;
  font-size: clamp(28px, 6vw, 56px);
  color: var(--red-glow);
  text-shadow: 0 0 30px rgba(231,76,60,0.8), 0 0 60px rgba(231,76,60,0.4);
  letter-spacing: 3px;
  line-height: 1;
}

.header-sub {
  font-family: 'Orbitron', sans-serif;
  font-size: clamp(10px, 2vw, 14px);
  color: var(--cyan);
  letter-spacing: 2px;
  margin-top: 6px;
  text-shadow: var(--glow-cyan);
}

.christmas-lights {
  display: flex;
  justify-content: center;
  gap: 18px;
  margin-top: 15px;
  flex-wrap: wrap;
}

.light {
  width: 14px; height: 18px;
  border-radius: 3px 3px 6px 6px;
  animation: flicker 2s infinite;
  box-shadow: 0 0 8px currentColor;
}
.l1{color:#ff4444;background:#ff4444;animation-delay:0s}
.l2{color:#44ff44;background:#44ff44;animation-delay:0.3s}
.l3{color:#4444ff;background:#4444ff;animation-delay:0.6s}
.l4{color:#ffff44;background:#ffff44;animation-delay:0.9s}
.l5{color:#ff44ff;background:#ff44ff;animation-delay:1.2s}
.l6{color:#44ffff;background:#44ffff;animation-delay:1.5s}
.l7{color:#ff8800;background:#ff8800;animation-delay:1.8s}

@keyframes flicker {
  0%,100%{opacity:1} 50%{opacity:0.3} 75%{opacity:0.9}
}

/* TABS */
.tabs-wrapper {
  position: sticky;
  top: 0;
  z-index: 100;
  background: var(--dark2);
  border-bottom: 1px solid var(--border);
  box-shadow: 0 2px 20px rgba(0,0,0,0.8);
}

.tabs {
  display: flex;
  overflow-x: auto;
  scrollbar-width: none;
  max-width: 1200px;
  margin: 0 auto;
}

.tab-btn {
  flex-shrink: 0;
  padding: 14px 18px;
  background: none;
  border: none;
  border-bottom: 3px solid transparent;
  color: var(--text-dim);
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.3s;
  white-space: nowrap;
}

.tab-btn:hover { color: var(--cyan); }
.tab-btn.active {
  color: var(--red-glow);
  border-bottom-color: var(--red-glow);
  text-shadow: var(--glow-red);
}

/* MAIN CONTENT */
.main {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.section { display: none; }
.section.active { display: block; }

/* PANEL */
.panel {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 20px;
  margin-bottom: 20px;
  position: relative;
  overflow: hidden;
}

.panel::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  right: 0; height: 2px;
  background: linear-gradient(90deg, transparent, var(--red-glow), transparent);
  opacity: 0.6;
}

.panel-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 13px;
  font-weight: 700;
  color: var(--cyan);
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.panel-title .icon { font-size: 18px; }

/* HEALTH BARS */
.hp-section {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  margin-bottom: 20px;
}

@media(max-width:600px){ .hp-section { grid-template-columns: 1fr; } }

.hp-card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 18px;
  position: relative;
  overflow: hidden;
}

.hp-card.vecna {
  border-color: rgba(192,57,43,0.5);
  background: linear-gradient(135deg, #120808, var(--panel));
}
.hp-card.grupo {
  border-color: rgba(0,212,255,0.3);
  background: linear-gradient(135deg, #051218, var(--panel));
}

.hp-name {
  font-family: 'Orbitron', sans-serif;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 2px;
  margin-bottom: 5px;
}

.hp-card.vecna .hp-name { color: var(--red-glow); }
.hp-card.grupo .hp-name { color: var(--cyan); }

.hp-subtitle {
  font-size: 11px;
  color: var(--text-dim);
  margin-bottom: 10px;
  font-family: 'Share Tech Mono', monospace;
}

.hp-bar-track {
  height: 18px;
  border-radius: 9px;
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.1);
  overflow: hidden;
  position: relative;
}

.hp-bar-fill {
  height: 100%;
  border-radius: 9px;
  transition: width 1s ease;
  position: relative;
  overflow: hidden;
}

.hp-bar-fill::after {
  content: '';
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(90deg, transparent, transparent 10px, rgba(255,255,255,0.1) 10px, rgba(255,255,255,0.1) 11px);
}

.hp-card.vecna .hp-bar-fill { background: linear-gradient(90deg, var(--red-dark), var(--red-glow)); }
.hp-card.grupo .hp-bar-fill { background: linear-gradient(90deg, var(--blue), var(--cyan)); }

.hp-value {
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  color: var(--text-dim);
  margin-top: 6px;
  text-align: right;
}

.hp-btns {
  display: flex;
  gap: 8px;
  margin-top: 10px;
}

.hp-btn {
  flex: 1;
  padding: 6px;
  border: 1px solid;
  border-radius: 5px;
  background: transparent;
  cursor: pointer;
  font-family: 'Orbitron', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1px;
  transition: all 0.2s;
}

.hp-card.vecna .hp-btn { border-color: var(--red-glow); color: var(--red-glow); }
.hp-card.vecna .hp-btn:hover { background: var(--red-dark); }
.hp-card.grupo .hp-btn { border-color: var(--cyan); color: var(--cyan); }
.hp-card.grupo .hp-btn:hover { background: rgba(0,212,255,0.1); }

/* XP BAR */
.xp-section {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 15px 20px;
  margin-bottom: 20px;
}

.xp-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 8px;
}

.xp-label {
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  color: var(--yellow);
  letter-spacing: 2px;
}

.xp-count {
  font-family: 'Share Tech Mono', monospace;
  font-size: 14px;
  color: var(--yellow);
}

.xp-track {
  height: 12px;
  background: rgba(255,255,255,0.05);
  border-radius: 6px;
  overflow: hidden;
}

.xp-fill {
  height: 100%;
  background: linear-gradient(90deg, var(--yellow), var(--orange));
  border-radius: 6px;
  transition: width 0.8s ease;
  box-shadow: 0 0 10px rgba(243,156,18,0.5);
}

.xp-btns {
  display: flex;
  gap: 8px;
  margin-top: 10px;
  flex-wrap: wrap;
}

.xp-add-btn {
  padding: 5px 12px;
  border: 1px solid var(--yellow);
  border-radius: 5px;
  background: transparent;
  color: var(--yellow);
  font-family: 'Orbitron', sans-serif;
  font-size: 9px;
  cursor: pointer;
  transition: all 0.2s;
}
.xp-add-btn:hover { background: rgba(243,156,18,0.2); }

/* SESIONES */
.sessions-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 16px;
}

.session-card {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 18px;
  position: relative;
  transition: all 0.3s;
  cursor: pointer;
}

.session-card:hover {
  border-color: rgba(0,212,255,0.4);
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0,0,0,0.5);
}

.session-card.locked {
  opacity: 0.5;
  cursor: not-allowed;
}
.session-card.locked:hover { transform: none; border-color: var(--border); }

.session-card.completed {
  border-color: rgba(0,255,136,0.4);
  background: linear-gradient(135deg, rgba(0,50,30,0.3), var(--panel2));
}

.session-num {
  font-family: 'Orbitron', sans-serif;
  font-size: 9px;
  color: var(--text-dim);
  letter-spacing: 2px;
  margin-bottom: 4px;
}

.session-name {
  font-family: 'Orbitron', sans-serif;
  font-size: 12px;
  font-weight: 700;
  color: var(--cyan);
  margin-bottom: 8px;
  line-height: 1.3;
}

.session-desc {
  font-size: 12px;
  color: var(--text-dim);
  line-height: 1.5;
  margin-bottom: 12px;
}

.session-character {
  display: flex;
  align-items: center;
  gap: 10px;
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 8px;
  padding: 10px;
  margin-bottom: 10px;
}

.char-avatar {
  width: 48px; height: 48px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  border: 2px solid;
  flex-shrink: 0;
}

.char-info { flex: 1; }

.char-name {
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  margin-bottom: 2px;
}

.char-power {
  font-size: 11px;
  color: var(--text-dim);
  line-height: 1.3;
}

.power-badge {
  display: inline-block;
  padding: 2px 8px;
  border-radius: 3px;
  font-family: 'Orbitron', sans-serif;
  font-size: 8px;
  font-weight: 700;
  letter-spacing: 1px;
  margin-top: 4px;
}

.session-oa {
  font-size: 11px;
  color: var(--text-dim);
}

.session-oa strong {
  color: var(--yellow);
  font-family: 'Share Tech Mono', monospace;
}

.session-badge {
  position: absolute;
  top: 12px; right: 12px;
  width: 28px; height: 28px;
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 14px;
}

.lock-icon { font-size: 14px; }

.session-xp {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: var(--yellow);
  margin-top: 8px;
}

/* RETOS */
.retos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 16px;
}

.reto-card {
  background: var(--panel2);
  border-radius: 10px;
  padding: 18px;
  border-left: 4px solid;
  position: relative;
  overflow: hidden;
}

.reto-card.nivel-1 { border-color: var(--green); }
.reto-card.nivel-2 { border-color: var(--yellow); }
.reto-card.nivel-3 { border-color: var(--red-glow); }

.reto-level {
  display: inline-block;
  padding: 2px 10px;
  border-radius: 3px;
  font-family: 'Orbitron', sans-serif;
  font-size: 8px;
  font-weight: 700;
  letter-spacing: 2px;
  margin-bottom: 8px;
}
.nivel-1 .reto-level { background: rgba(0,255,136,0.15); color: var(--green); border: 1px solid var(--green); }
.nivel-2 .reto-level { background: rgba(243,156,18,0.15); color: var(--yellow); border: 1px solid var(--yellow); }
.nivel-3 .reto-level { background: rgba(231,76,60,0.15); color: var(--red-glow); border: 1px solid var(--red-glow); }

.reto-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 12px;
  font-weight: 700;
  color: var(--text);
  margin-bottom: 6px;
}

.reto-desc {
  font-size: 12px;
  color: var(--text-dim);
  line-height: 1.5;
  margin-bottom: 10px;
}

.reto-reward {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: var(--yellow);
}

.reto-check {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-top: 10px;
}

.reto-checkbox {
  width: 20px; height: 20px;
  appearance: none;
  border: 2px solid var(--border);
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.2s;
  position: relative;
  flex-shrink: 0;
}

.reto-checkbox:checked {
  background: var(--green);
  border-color: var(--green);
}

.reto-checkbox:checked::after {
  content: '✓';
  position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%,-50%);
  color: white;
  font-size: 12px;
  font-weight: 700;
}

.reto-check label {
  font-size: 11px;
  color: var(--text-dim);
  cursor: pointer;
}

/* PERSONAJES */
.chars-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 16px;
}

.char-card {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 20px;
  text-align: center;
  transition: all 0.3s;
  position: relative;
  overflow: hidden;
}

.char-card.unlocked {
  border-color: rgba(0,212,255,0.3);
  box-shadow: 0 0 20px rgba(0,212,255,0.1);
}

.char-card.locked-char {
  opacity: 0.4;
}
.char-card.unlocked {
  filter: none !important;
  -webkit-filter: none !important;
  opacity: 1 !important;
}

.char-big-avatar {
  width: 80px; height: 80px;
  border-radius: 50%;
  margin: 0 auto 12px;
  display: flex; align-items: center; justify-content: center;
  font-size: 36px;
  border: 3px solid;
  position: relative;
}

.char-card.unlocked .char-big-avatar {
  animation: pulse-glow 2s infinite;
}

@keyframes pulse-glow {
  0%,100% { box-shadow: 0 0 10px currentColor; }
  50% { box-shadow: 0 0 25px currentColor; }
}

.char-card-name {
  font-family: 'Orbitron', sans-serif;
  font-size: 14px;
  font-weight: 700;
  margin-bottom: 4px;
}

.char-card-session {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--text-dim);
  margin-bottom: 10px;
}

.char-card-power-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  margin-bottom: 6px;
}

.char-card-power-desc {
  font-size: 12px;
  color: var(--text-dim);
  line-height: 1.5;
  margin-bottom: 10px;
}

.char-card-bonus {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 6px;
  padding: 8px;
  font-size: 11px;
  line-height: 1.5;
}

.char-unlock-tag {
  display: inline-block;
  padding: 3px 10px;
  border-radius: 20px;
  font-family: 'Orbitron', sans-serif;
  font-size: 8px;
  font-weight: 700;
  letter-spacing: 1px;
  margin-top: 8px;
}

/* REFLEXIONES */
.reflection-area {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 20px;
  margin-bottom: 16px;
}

.reflection-session-select {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin-bottom: 15px;
}

.ref-sess-btn {
  padding: 6px 14px;
  border: 1px solid var(--border);
  border-radius: 5px;
  background: transparent;
  color: var(--text-dim);
  font-family: 'Orbitron', sans-serif;
  font-size: 9px;
  cursor: pointer;
  transition: all 0.2s;
}

.ref-sess-btn.active, .ref-sess-btn:hover {
  border-color: var(--cyan);
  color: var(--cyan);
  background: rgba(0,212,255,0.08);
}

.ref-prompts {
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-bottom: 15px;
}

.ref-prompt {
  background: rgba(255,255,255,0.03);
  border-left: 3px solid var(--red-glow);
  border-radius: 0 6px 6px 0;
  padding: 8px 12px;
  font-size: 12px;
  color: var(--text-dim);
  cursor: pointer;
  transition: all 0.2s;
}

.ref-prompt:hover {
  background: rgba(192,57,43,0.1);
  color: var(--text);
}

.ref-textarea {
  width: 100%;
  min-height: 120px;
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 12px;
  color: var(--text);
  font-family: 'Nunito', sans-serif;
  font-size: 13px;
  resize: vertical;
  transition: border-color 0.2s;
}

.ref-textarea:focus {
  outline: none;
  border-color: rgba(0,212,255,0.4);
}

.ref-actions {
  display: flex;
  gap: 10px;
  margin-top: 12px;
  flex-wrap: wrap;
}

.btn-primary {
  padding: 10px 20px;
  background: linear-gradient(135deg, var(--red-dark), var(--red-glow));
  border: none;
  border-radius: 6px;
  color: white;
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.2s;
  box-shadow: 0 4px 15px rgba(192,57,43,0.3);
}
.btn-primary:hover { transform: translateY(-1px); box-shadow: 0 6px 20px rgba(192,57,43,0.5); }

.btn-secondary {
  padding: 10px 20px;
  background: transparent;
  border: 1px solid var(--cyan);
  border-radius: 6px;
  color: var(--cyan);
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.2s;
}
.btn-secondary:hover { background: rgba(0,212,255,0.1); }

.saved-reflections {
  margin-top: 20px;
}

.saved-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 11px;
  color: var(--text-dim);
  letter-spacing: 2px;
  margin-bottom: 12px;
}

.reflection-entry {
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 14px;
  margin-bottom: 10px;
  position: relative;
}

.ref-entry-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 8px;
}

.ref-entry-session {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--cyan);
}

.ref-entry-date {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--text-dim);
}

.ref-entry-text {
  font-size: 13px;
  color: var(--text);
  line-height: 1.6;
}

.ref-delete {
  position: absolute;
  top: 10px; right: 10px;
  background: transparent;
  border: none;
  color: var(--text-dim);
  cursor: pointer;
  font-size: 14px;
  transition: color 0.2s;
}
.ref-delete:hover { color: var(--red-glow); }

/* AUTOEVALUACIÓN */
.autoeval-grid {
  display: grid;
  gap: 15px;
}

.autoeval-item {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 16px;
}

.autoeval-oa {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--yellow);
  margin-bottom: 4px;
}

.autoeval-desc {
  font-size: 13px;
  color: var(--text);
  margin-bottom: 12px;
  line-height: 1.4;
}

.stars-row {
  display: flex;
  align-items: center;
  gap: 12px;
}

.stars {
  display: flex;
  gap: 4px;
}

.star-btn {
  font-size: 24px;
  background: none;
  border: none;
  cursor: pointer;
  transition: transform 0.1s;
  filter: grayscale(1) brightness(0.5);
}
.star-btn.active { filter: none; }
.star-btn:hover { transform: scale(1.2); }

.stars-label {
  font-size: 11px;
  color: var(--text-dim);
  font-family: 'Share Tech Mono', monospace;
}

.diana-wrapper {
  margin-top: 20px;
}

.diana-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 12px;
  color: var(--cyan);
  margin-bottom: 15px;
  text-align: center;
}

.diana-svg-container {
  display: flex;
  justify-content: center;
}

/* OA SECTION */
.oa-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 15px;
}

.oa-card {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 10px;
  padding: 16px;
  border-left: 4px solid var(--yellow);
}

.oa-code {
  font-family: 'Orbitron', sans-serif;
  font-size: 10px;
  font-weight: 700;
  color: var(--yellow);
  letter-spacing: 2px;
  margin-bottom: 6px;
}

.oa-text {
  font-size: 13px;
  color: var(--text);
  line-height: 1.5;
}

.oa-session-tag {
  display: inline-block;
  margin-top: 8px;
  padding: 2px 8px;
  background: rgba(0,212,255,0.1);
  border: 1px solid rgba(0,212,255,0.3);
  border-radius: 3px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--cyan);
}

/* MISIÓN FINAL */
.final-mission {
  background: linear-gradient(135deg, #0d0005, #050010);
  border: 1px solid var(--red-glow);
  border-radius: 12px;
  padding: 30px;
  text-align: center;
  position: relative;
  overflow: hidden;
  box-shadow: inset 0 0 60px rgba(192,57,43,0.1), var(--glow-red);
  margin-bottom: 20px;
}

.final-mission::before {
  content: '';
  position: absolute;
  inset: 0;
  background: repeating-linear-gradient(
    -45deg,
    transparent,
    transparent 20px,
    rgba(192,57,43,0.03) 20px,
    rgba(192,57,43,0.03) 21px
  );
}

.final-icon { font-size: 48px; margin-bottom: 10px; }

.final-title {
  font-family: 'Creepster', cursive;
  font-size: 32px;
  color: var(--red-glow);
  text-shadow: 0 0 20px rgba(231,76,60,0.8);
  margin-bottom: 10px;
}

.final-desc {
  font-size: 14px;
  color: var(--text-dim);
  line-height: 1.7;
  max-width: 700px;
  margin: 0 auto 20px;
}

.progress-gate {
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 15px;
  margin-top: 20px;
  text-align: left;
}

.gate-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 11px;
  color: var(--cyan);
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.gate-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 6px 0;
  border-bottom: 1px solid rgba(255,255,255,0.05);
  font-size: 12px;
  color: var(--text-dim);
}
.gate-item:last-child { border-bottom: none; }
.gate-item.met { color: var(--green); }
.gate-item .gate-icon { font-size: 16px; }

/* INSIGNIA HOPPER */
.insignia-preview {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  margin: 20px auto;
}

.hexagon {
  width: 120px;
  height: 120px;
  background: linear-gradient(135deg, var(--red-dark), var(--red-glow));
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 48px;
  box-shadow: 0 0 30px rgba(192,57,43,0.5);
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%,100%{ transform: translateY(0); }
  50%{ transform: translateY(-8px); }
}

.insignia-name {
  font-family: 'Creepster', cursive;
  font-size: 20px;
  color: var(--red-glow);
  text-shadow: var(--glow-red);
}

.insignia-power {
  font-size: 13px;
  color: var(--text-dim);
  text-align: center;
  font-style: italic;
}

/* TOAST */
.toast {
  position: fixed;
  bottom: 30px; right: 30px;
  background: var(--panel);
  border: 1px solid var(--green);
  border-radius: 8px;
  padding: 14px 20px;
  font-family: 'Orbitron', sans-serif;
  font-size: 11px;
  color: var(--green);
  box-shadow: var(--glow-green);
  transform: translateX(200px);
  opacity: 0;
  transition: all 0.4s;
  z-index: 9999;
  max-width: 280px;
}

.toast.show {
  transform: translateX(0);
  opacity: 1;
}

/* FLIP BADGE */
.flip-badge-wrap {
  perspective: 600px;
  width: 120px; height: 120px;
  cursor: pointer;
  margin: 0 auto;
}
.flip-badge-inner {
  position: relative;
  width: 100%; height: 100%;
  transform-style: preserve-3d;
  transition: transform 0.6s cubic-bezier(0.4,0,0.2,1);
}
.flip-badge-wrap.flipped .flip-badge-inner { transform: rotateY(180deg); }
.flip-front, .flip-back {
  position: absolute; inset: 0;
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  border-radius: 0;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column; gap: 6px;
}
.flip-front {
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  background: linear-gradient(135deg, var(--red-dark), var(--red-glow));
  font-size: 48px;
  box-shadow: 0 0 30px rgba(192,57,43,0.5);
  animation: float 3s ease-in-out infinite;
}
.flip-back {
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  background: linear-gradient(135deg, #0a0a1a, #1a0a2e);
  border: none;
  transform: rotateY(180deg);
  padding: 20px 10px;
  text-align: center;
}
.flip-back-title {
  font-family: 'Orbitron', sans-serif;
  font-size: 7px;
  font-weight: 700;
  color: var(--cyan);
  letter-spacing: 1px;
  margin-bottom: 4px;
}
.flip-back-power {
  font-size: 9px;
  color: var(--text);
  line-height: 1.3;
  font-style: italic;
}
.flip-hint {
  font-family: 'Share Tech Mono', monospace;
  font-size: 9px;
  color: var(--text-dim);
  margin-top: 4px;
  letter-spacing: 1px;
}

/* Avatar option hover */
.av-opt:hover { transform: scale(1.08); }

::-webkit-scrollbar { width: 6px; height: 6px; }
::-webkit-scrollbar-track { background: var(--dark2); }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 3px; }

/* INTRO SECTION */
.intro-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 20px;
}
@media(max-width:700px){ .intro-grid { grid-template-columns: 1fr; } }

.narrative-box {
  background: linear-gradient(135deg, rgba(192,57,43,0.05), transparent);
  border: 1px solid rgba(192,57,43,0.3);
  border-radius: 10px;
  padding: 20px;
}

.narrative-box h3 {
  font-family: 'Creepster', cursive;
  font-size: 22px;
  color: var(--red-glow);
  margin-bottom: 12px;
  text-shadow: var(--glow-red);
}

.narrative-box p {
  font-size: 13px;
  color: var(--text-dim);
  line-height: 1.7;
  margin-bottom: 10px;
}

.stats-mini {
  display: grid;
  gap: 10px;
}

.stat-chip {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 12px;
  text-align: center;
}

.stat-chip-val {
  font-family: 'Orbitron', sans-serif;
  font-size: 24px;
  font-weight: 900;
  color: var(--cyan);
}

.stat-chip-label {
  font-size: 10px;
  color: var(--text-dim);
  font-family: 'Share Tech Mono', monospace;
  margin-top: 2px;
}

/* ACTIVE POWER BANNER */
.active-power {
  background: linear-gradient(135deg, rgba(0,212,255,0.05), transparent);
  border: 1px solid rgba(0,212,255,0.3);
  border-radius: 8px;
  padding: 12px 16px;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 12px;
}

.active-power-icon { font-size: 24px; }
.active-power-title { font-family: 'Orbitron', sans-serif; font-size: 10px; color: var(--cyan); margin-bottom: 2px; }
.active-power-desc { color: var(--text-dim); }

/* KPSI */
.kpsi-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 12px;
  margin-top: 15px;
}

.kpsi-card {
  background: var(--panel2);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 14px;
  text-align: center;
}

.kpsi-emoji { font-size: 28px; margin-bottom: 6px; }
.kpsi-label {
  font-family: 'Orbitron', sans-serif;
  font-size: 9px;
  font-weight: 700;
  letter-spacing: 1px;
  margin-bottom: 4px;
}
.kpsi-desc {
  font-size: 11px;
  color: var(--text-dim);
}

.kpsi-select {
  width: 100%;
  margin-top: 10px;
  background: rgba(255,255,255,0.05);
  border: 1px solid var(--border);
  border-radius: 5px;
  color: var(--text);
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  padding: 5px;
  cursor: pointer;
}

.kpsi-select:focus { outline: none; border-color: var(--cyan); }

</style>
</head>
<body>

<!-- TOAST -->
<div class="toast" id="toast">✅ GUARDADO</div>

<!-- HEADER -->
<div class="header">
  <div class="header-eyebrow">🔒 ARCHIVO CLASIFICADO — HAWKINS LAB · UD4 · 5º EP</div>
  <div class="header-title">⚡ ONCE NOS ENTRENA ⚡</div>
  <div class="header-sub">ESTAR EN FORMA PARA CUIDAR AL GRUPO · GUARDIANES DE HAWKINS</div>
  <div class="christmas-lights">
    <div class="light l1"></div><div class="light l2"></div><div class="light l3"></div>
    <div class="light l4"></div><div class="light l5"></div><div class="light l6"></div>
    <div class="light l7"></div><div class="light l1"></div><div class="light l2"></div>
    <div class="light l3"></div><div class="light l4"></div><div class="light l5"></div>
    <div class="light l6"></div><div class="light l7"></div>
  </div>
</div>

<!-- TABS -->
<div class="tabs-wrapper">
  <div style="display:flex;align-items:center;max-width:1200px;margin:0 auto">
    <button onclick="document.getElementById('tabs-row').scrollBy({left:-160,behavior:'smooth'})" style="flex-shrink:0;width:28px;height:44px;background:transparent;border:none;border-right:1px solid var(--border);color:var(--text-dim);font-size:20px;cursor:pointer">&#8249;</button>
    <div style="display:flex;overflow-x:auto;scrollbar-width:none;flex:1" id="tabs-row">
    <button class="tab-btn active" onclick="showSection('mision',this)">🎯 MISIÓN</button>
    <button class="tab-btn" onclick="showSection('estado',this)">❤️ ESTADO</button>
    <button class="tab-btn" onclick="showSection('sesiones',this)">📋 SESIONES</button>
    <button class="tab-btn" onclick="showSection('retos',this)">⚔️ RETOS</button>
    <button class="tab-btn" onclick="showSection('personajes',this)">👥 GUARDIANES</button>
    <button class="tab-btn" onclick="showSection('reflexiones',this)">📓 REFLEXIONES</button>
    <button class="tab-btn" onclick="showSection('autoeval',this)">⭐ AUTOEVALUACIÓN</button>
    <button class="tab-btn" onclick="showSection('podcast',this)">🎙️ PODCAST</button>
    <button class="tab-btn" onclick="showSection('ia',this)">🤖 LAB HAWKINS</button>
    <button class="tab-btn" onclick="showSection('exhibicion',this)" style="color:var(--yellow)">📺 EXHIBICIÓN</button>
    <button class="tab-btn" onclick="showSection('final',this)">🔴 RETO FINAL</button>
    </div>
    <button onclick="document.getElementById('tabs-row').scrollBy({left:160,behavior:'smooth'})" style="flex-shrink:0;width:28px;height:44px;background:transparent;border:none;border-left:1px solid var(--border);color:var(--text-dim);font-size:20px;cursor:pointer">&#8250;</button>
  </div>
</div>

<div class="main">

<!-- =================== MISIÓN =================== -->
<div class="section active" id="section-mision">

  <div id="active-power-banner" class="active-power" style="display:none">
    <div class="active-power-icon" id="apb-icon">🌟</div>
    <div>
      <div class="active-power-title">PODER ACTIVO EN ESTA SESIÓN</div>
      <div class="active-power-desc" id="apb-desc">...</div>
    </div>
  </div>

  <div class="intro-grid">
    <div class="narrative-box">
      <h3>📡 TRANSMISIÓN DE ONCE</h3>
      <p>Guardianes… VECNA se está fortaleciendo. Ha encontrado una grieta en el Mundo al Revés: <strong>el sedentarismo y los hábitos destructivos</strong> de quienes aún no conocen el poder de su propio cuerpo.</p>
      <p>Once ha enviado un mensaje urgente desde el laboratorio de Hawkins: solo un grupo en plena forma física puede enfrentarse a él y sobrevivir. Pero no se trata solo de ser rápido o fuerte… se trata de <strong>comprender cómo funciona tu motor interior y cuidarlo</strong>.</p>
      <p>Vuestra misión: entrenar durante 8 sesiones, desbloquear a los Guardianes, debilitar a VECNA y crear un <strong>Podcast Guardián</strong> que inspire a todo el alumnado de primero a cuidarse, moverse y sentirse bien.</p>
      <p style="color: var(--red-glow); font-family: 'Share Tech Mono', monospace; font-size:12px; margin-top:15px;">⚠️ RECUERDA: Completad todas las sesiones para acceder al Reto Final contra VECNA.</p>
    </div>

    <div class="stats-mini">
      <div class="stat-chip">
        <div class="stat-chip-val">8</div>
        <div class="stat-chip-label">SESIONES</div>
      </div>
      <div class="stat-chip">
        <div class="stat-chip-val" id="stat-xp">0</div>
        <div class="stat-chip-label">XP TOTAL</div>
      </div>
      <div class="stat-chip">
        <div class="stat-chip-val" id="stat-retos">0</div>
        <div class="stat-chip-label">RETOS COMPLETADOS</div>
      </div>
      <div class="stat-chip">
        <div class="stat-chip-val" id="stat-chars">0</div>
        <div class="stat-chip-label">GUARDIANES DESBLOQUEADOS</div>
      </div>
    </div>
  </div>

  <div class="panel" style="margin-top:20px">
    <div class="panel-title"><span class="icon">🏅</span> INSIGNIA DE ESTA UD</div>
    <div class="insignia-preview">
      <div class="flip-badge-wrap" id="flip-hopper" onclick="this.classList.toggle('flipped')" title="¡Tócame para ver el superpoder!">
        <div class="flip-badge-inner">
          <div class="flip-front">🔥</div>
          <div class="flip-back">
            <div class="flip-back-title">⚡ SUPERPODER</div>
            <div class="flip-back-power">"Tu motor nunca se apaga. La determinación es tu escudo."</div>
          </div>
        </div>
      </div>
      <div class="flip-hint">👆 Toca la insignia</div>
      <div class="insignia-name">INSIGNIA HOPPER</div>
      <div class="insignia-power">"Tu motor nunca se apaga"</div>
      <div style="margin-top:10px; font-size:12px; color:var(--text-dim); text-align:center; max-width:400px">
        Al completar esta UD recibirás la Insignia Hopper en tu Manual del Guardián y en el mapa del Mundo al Revés del gimnasio. <strong>¡Un paso más para derrotar a VECNA!</strong>
      </div>
    </div>
  </div>

  <div class="panel">
    <div class="panel-title"><span class="icon">🎙️</span> PRODUCTO FINAL: PODCAST GUARDIÁN</div>
    <p style="font-size:13px; color:var(--text-dim); line-height:1.7; margin-bottom:15px">
      Al final de las 8 sesiones, el grupo creará un <strong>Podcast Guardián</strong> con 4 episodios. Cada episodio narra un aspecto de vuestro entrenamiento: beneficios del ejercicio, mitos del cuerpo, gestión emocional ante el error, y resolución de conflictos. Este podcast se difundirá al alumnado de 1º para inspirarles.
    </p>
    <div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(160px,1fr)); gap:10px">
      <div style="background:rgba(192,57,43,0.1); border:1px solid rgba(192,57,43,0.3); border-radius:8px; padding:12px; text-align:center">
        <div style="font-size:20px; margin-bottom:4px">🎙️</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow); margin-bottom:4px">EP. 1</div>
        <div style="font-size:11px; color:var(--text-dim)">¿Qué es estar en forma de verdad?</div>
      </div>
      <div style="background:rgba(192,57,43,0.1); border:1px solid rgba(192,57,43,0.3); border-radius:8px; padding:12px; text-align:center">
        <div style="font-size:20px; margin-bottom:4px">💪</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow); margin-bottom:4px">EP. 2</div>
        <div style="font-size:11px; color:var(--text-dim)">Fuerza, flexibilidad y sensaciones</div>
      </div>
      <div style="background:rgba(192,57,43,0.1); border:1px solid rgba(192,57,43,0.3); border-radius:8px; padding:12px; text-align:center">
        <div style="font-size:20px; margin-bottom:4px">😤</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow); margin-bottom:4px">EP. 3</div>
        <div style="font-size:11px; color:var(--text-dim)">Los errores también enseñan</div>
      </div>
      <div style="background:rgba(192,57,43,0.1); border:1px solid rgba(192,57,43,0.3); border-radius:8px; padding:12px; text-align:center">
        <div style="font-size:20px; margin-bottom:4px">🛡️</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow); margin-bottom:4px">EP. 4</div>
        <div style="font-size:11px; color:var(--text-dim)">Nuestra vacuna contra el conflicto</div>
      </div>
    </div>
  </div>

</div>

<!-- =================== ESTADO =================== -->
<div class="section" id="section-estado">

  <div class="hp-section">
    <div class="hp-card vecna">
      <div class="hp-name">💀 VECNA</div>
      <div class="hp-subtitle">Vida actual del enemigo</div>
      <div class="hp-bar-track">
        <div class="hp-bar-fill" id="vecna-bar" style="width:100%"></div>
      </div>
      <div class="hp-value" id="vecna-value">100 / 100</div>
      <div class="hp-btns">
        <button class="hp-btn" onclick="changeHP('vecna',-10)">⚔️ -10 HP</button>
        <button class="hp-btn" onclick="changeHP('vecna',-5)">🗡️ -5 HP</button>
        <button class="hp-btn" onclick="changeHP('vecna',+5)">☠️ +5 HP</button>
      </div>
      <div style="margin-top:12px; font-size:11px; color:var(--text-dim)">
        Cada sesión completada, reto superado y reflexión guardada debilita a VECNA. ¡Reducidlo a 0!
      </div>
    </div>

    <div class="hp-card grupo" style="border-color:rgba(0,255,136,0.3); background:linear-gradient(135deg,#050f08,var(--panel))">
      <div class="hp-name" style="color:var(--green)">⚡ MI GUARDIÁN PERSONAL</div>
      <div class="hp-subtitle" style="margin-bottom:12px">Elige tu personaje y personaliza tu avatar</div>

      <!-- Avatar selector -->
      <div id="avatar-selector" style="display:grid; grid-template-columns:repeat(4,1fr); gap:6px; margin-bottom:12px">
        <div class="av-opt" data-char="hopper" onclick="selectAvatar('hopper')" title="Hopper" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">💀</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">HOPPER</div>
        </div>
        <div class="av-opt" data-char="once" onclick="selectAvatar('once')" title="Once" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">🌪️</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">ONCE</div>
        </div>
        <div class="av-opt" data-char="dustin" onclick="selectAvatar('dustin')" title="Dustin" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">⚙️</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">DUSTIN</div>
        </div>
        <div class="av-opt" data-char="max" onclick="selectAvatar('max')" title="Max" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">🎶</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">MAX</div>
        </div>
        <div class="av-opt" data-char="lucas" onclick="selectAvatar('lucas')" title="Lucas" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">🧭</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">LUCAS</div>
        </div>
        <div class="av-opt" data-char="will" onclick="selectAvatar('will')" title="Will" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">🔥</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">WILL</div>
        </div>
        <div class="av-opt" data-char="mike" onclick="selectAvatar('mike')" title="Mike" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">📻</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">MIKE</div>
        </div>
        <div class="av-opt" data-char="steve" onclick="selectAvatar('steve')" title="Steve" style="cursor:pointer; border:2px solid var(--border); border-radius:8px; padding:6px; text-align:center; transition:all 0.2s; background:var(--panel2)">
          <div style="font-size:22px">🦸</div><div style="font-size:8px; color:var(--text-dim); font-family:'Orbitron',sans-serif; margin-top:2px">STEVE</div>
        </div>
      </div>

      <!-- Name input -->
      <div style="margin-bottom:10px">
        <input id="avatar-name-input" type="text" maxlength="30" placeholder="Nombre del grupo..." style="width:100%; background:rgba(0,255,136,0.05); border:1px solid rgba(0,255,136,0.3); border-radius:6px; padding:7px 10px; color:var(--green); font-family:'Orbitron',sans-serif; font-size:10px; letter-spacing:1px; outline:none;" oninput="updateAvatarName(this.value)">
      </div>

      <!-- Avatar display -->
      <div style="display:flex; align-items:center; gap:12px; background:rgba(0,255,136,0.04); border:1px solid rgba(0,255,136,0.15); border-radius:8px; padding:10px; margin-bottom:10px">
        <div id="avatar-display" style="font-size:36px; width:54px; height:54px; border-radius:50%; display:flex; align-items:center; justify-content:center; border:3px solid var(--green); background:rgba(0,255,136,0.08); flex-shrink:0; animation:pulse-glow 2s infinite; color:var(--green)">💀</div>
        <div style="flex:1">
          <div id="avatar-name-display" style="font-family:'Orbitron',sans-serif; font-size:11px; font-weight:700; color:var(--green); margin-bottom:4px">NOMBRE DEL GRUPO</div>
          <div id="avatar-power-display" style="font-size:10px; color:var(--text-dim)">Determinación — "Nunca te rindes"</div>
        </div>
      </div>

      <!-- Fuerza bar -->
      <div style="margin-bottom:4px; display:flex; justify-content:space-between; align-items:center">
        <span style="font-family:'Orbitron',sans-serif; font-size:9px; font-weight:700; color:var(--green); letter-spacing:1px">⚡ FUERZA</span>
        <span id="fuerza-value" style="font-family:'Share Tech Mono',monospace; font-size:11px; color:var(--green)">0 / 100</span>
      </div>
      <div class="hp-bar-track">
        <div class="hp-bar-fill" id="fuerza-bar" style="width:0%; background:linear-gradient(90deg,#00882b,var(--green))"></div>
      </div>
      <div style="font-size:10px; color:var(--text-dim); margin-top:6px">La fuerza aumenta con cada sesión completada, reto superado y reflexión guardada</div>
    </div>
  </div>

  <div class="xp-section">
    <div class="xp-header">
      <div class="xp-label">⚡ EXPERIENCIA GUARDIANA (XP)</div>
      <div class="xp-count" id="xp-display">0 / 500 XP</div>
    </div>
    <div class="xp-track">
      <div class="xp-fill" id="xp-bar" style="width:0%"></div>
    </div>
    <div class="xp-btns" style="display:none"></div>
    <div style="margin-top:12px; text-align:right">
      <button onclick="resetAll()" style="padding:6px 14px; background:transparent; border:1px solid rgba(192,57,43,0.5); border-radius:5px; color:rgba(192,57,43,0.7); font-family:'Orbitron',sans-serif; font-size:9px; cursor:pointer; letter-spacing:1px; transition:all 0.2s" onmouseover="this.style.borderColor='var(--red-glow)';this.style.color='var(--red-glow)'" onmouseout="this.style.borderColor='rgba(192,57,43,0.5)';this.style.color='rgba(192,57,43,0.7)'">🔄 REINICIAR TODO</button>
    </div>
  </div>

  <div class="panel">
    <div class="panel-title"><span class="icon">📊</span> PROGRESO DE SESIONES</div>
    <div style="display:grid; grid-template-columns:repeat(7,1fr); gap:8px; margin-top:10px">
      <div id="prog-s1" class="session-prog" onclick="toggleSessionProg(1)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S1</div>
        <div style="font-size:18px">🎙️</div>
      </div>
      <div id="prog-s2" class="session-prog" onclick="toggleSessionProg(2)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S2</div>
        <div style="font-size:18px">💪</div>
      </div>
      <div id="prog-s3" class="session-prog" onclick="toggleSessionProg(3)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S3</div>
        <div style="font-size:18px">🏃</div>
      </div>
      <div id="prog-s4" class="session-prog" onclick="toggleSessionProg(4)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S4</div>
        <div style="font-size:18px">😤</div>
      </div>
      <div id="prog-s5" class="session-prog" onclick="toggleSessionProg(5)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S5</div>
        <div style="font-size:18px">🛡️</div>
      </div>
      <div id="prog-s6" class="session-prog" onclick="toggleSessionProg(6)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S6</div>
        <div style="font-size:18px">🎵</div>
      </div>
      <div id="prog-s7" class="session-prog" onclick="toggleSessionProg(7)" style="background:var(--panel2); border:2px solid var(--border); border-radius:8px; padding:10px; text-align:center; cursor:pointer; transition:all 0.3s">
        <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim)">S7</div>
        <div style="font-size:18px">🏆</div>
      </div>
    </div>
    <div style="font-size:11px; color:var(--text-dim); margin-top:10px; text-align:center">Pulsa cada sesión para marcarla como completada</div>
  </div>

</div>

<!-- =================== SESIONES =================== -->
<div class="section" id="section-sesiones">
  <div class="sessions-grid">

    <!-- S1 -->
    <div class="session-card completed" id="scard-1" style="cursor:pointer" onclick="togglePanel('s1',event)">
      <div class="session-badge" style="background:rgba(0,255,136,0.1); border:1px solid var(--green)">🎙️</div>
      <div class="session-num">SESIÓN 1 · KPSI INICIAL <span id="s1-arrow" style="font-size:11px; color:var(--green); margin-left:6px">▼ VER DETALLE</span></div>
      <div class="session-name">¡QUE COMIENCE EL ENTRENAMIENTO DEL GUARDIÁN!</div>
      <div class="session-desc">Podcast de AF y salud, KPSI de retos motrices y grabación del primer episodio. ¿Qué sabéis ya sobre estar en forma?</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#e74c3c; background:rgba(231,76,60,0.1)">💀</div>
        <div class="char-info">
          <div class="char-name" style="color:#e74c3c">🔓 SE DESBLOQUEA: HOPPER</div>
          <div class="char-power">Poder: <strong>Determinación</strong> — "Nunca te rindes, siempre hay un camino"</div>
          <div class="power-badge" style="background:rgba(231,76,60,0.15); color:#e74c3c; border:1px solid #e74c3c">ACTIVO EN S2</div>
        </div>
      </div>
      <div class="session-xp">📊 KPSI inicial · 🎙️ Episodio 1 · ⚡ +20 XP base</div>

      <div id="s1-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ JUEGOS Y RETOS DE LA SESIÓN</div>
        <div style="display:grid; gap:10px; margin-bottom:16px">
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🫀 El Pulso Guardián</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Localiza tu pulso en la muñeca o cuello. Cuéntalo durante 15 segundos y multiplica por 4. Compáralo con el de dos compañeros/as. ¿Quién tiene el corazón más tranquilo? ¿Por qué creéis que hay diferencias?</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s1r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s1r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">📋 KPSI Guardián</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Completa el KPSI inicial en la sección Autoevaluación (columna INICIO). Sé honesto/a: no hay respuestas buenas ni malas. ¡Es tu punto de partida como Guardián/a!</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s1r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s1r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🧠 El Debate del Motor</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">En grupos de 4, debatid durante 3 min: <em>"¿Qué creéis que pasa en vuestro cuerpo cuando hacéis ejercicio?"</em> Cada grupo expone su hipótesis. El profe contrasta con la realidad. ¿Cuántas habéis acertado?</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s1r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s1r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow)">NIVEL 3 — ÉLITE 🔥</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🎙️ Apertura del Podcast — El Gancho</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Grabad la intro del Episodio 1: presentad el podcast con nombre, misión y una pregunta que enganche al oyente de 1º. Ej: <em>"¿Sabéis lo que le pasa a vuestro corazón cuando corréis? Hoy os lo contamos…"</em> Duración: 30–45 segundos.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s1r4" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)"><label for="s1r4" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
        </div>
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--red-glow); letter-spacing:2px; margin-bottom:12px">🎙️ EPISODIO 1 DEL PODCAST — QUÉ INCLUIR</div>
        <div style="background:linear-gradient(135deg,rgba(192,57,43,0.08),transparent); border:1px solid rgba(192,57,43,0.3); border-radius:10px; padding:16px">
          <div style="font-family:'Orbitron',sans-serif; font-size:12px; font-weight:700; margin-bottom:4px">🫀 "¿Qué es estar en forma de verdad?"</div>
          <div style="font-size:11px; color:var(--text-dim); margin-bottom:12px; font-style:italic">Duración: 3–4 min · Grabación grupal</div>
          <div style="display:grid; gap:8px">
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">1</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Presentación del podcast y del equipo</div><div style="font-size:11px; color:var(--text-dim)">Nombre del grupo, misión de la UD y bienvenida al oyente. Gancho inicial con una pregunta retadora.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">2</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">3 beneficios del ejercicio para la salud</div><div style="font-size:11px; color:var(--text-dim)">Explicad cada beneficio con vuestras palabras y un ejemplo real de vuestra vida. No leáis una lista — contadlo como si le hablarais a un amigo.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">3</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Resultados del debate del motor</div><div style="font-size:11px; color:var(--text-dim)">¿Qué creíais que pasaba en el cuerpo al hacer ejercicio? ¿Qué sorprendió al grupo? Contad al menos una cosa que no sabíais.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">4</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Cierre y adelanto del próximo episodio</div><div style="font-size:11px; color:var(--text-dim)">Despedida del episodio y anuncio de lo que viene: <em>"En el próximo episodio vamos a descubrir de qué estamos hechos: fuerza, flexibilidad y lo que el cuerpo siente…"</em></div></div></div>
          </div>
          <div style="margin-top:12px; padding:8px 12px; background:rgba(0,212,255,0.08); border:1px solid rgba(0,212,255,0.25); border-radius:6px">
            <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--cyan); margin-bottom:4px">💡 CONSEJO GUARDIÁN</div>
            <div style="font-size:11px; color:var(--text-dim)">Antes de grabar, ensayad una vez en voz alta. Repartid quién habla en cada parte. El KPSI que habéis rellenado hoy os dará pistas de qué contar.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- S2 -->
    <div class="session-card" id="scard-2" style="cursor:pointer" onclick="toggleS2Panel(event)">
      <div class="session-badge" style="background:rgba(0,212,255,0.1); border:1px solid var(--cyan)">💪</div>
      <div class="session-num">SESIÓN 2 · EP. PODCAST 2 <span id="s2-arrow" style="font-size:11px; color:var(--cyan); margin-left:6px; transition:transform 0.3s; display:inline-block">▼ VER DETALLE</span></div>
      <div class="session-name">ONCE ANALIZA AL GRUPO: ¿DE QUÉ ESTAMOS HECHOS?</div>
      <div class="session-desc">Retos de fuerza y flexibilidad con registro de sensaciones corporales. Grabación del segundo episodio del podcast.</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#3498db; background:rgba(52,152,219,0.1)">🌪️</div>
        <div class="char-info">
          <div class="char-name" style="color:#3498db">🔓 SE DESBLOQUEA: ONCE</div>
          <div class="char-power">Poder: <strong>Telekinesia</strong> — "Puedes mover los obstáculos con tu mente"</div>
          <div class="power-badge" style="background:rgba(52,152,219,0.15); color:#3498db; border:1px solid #3498db">ACTIVO EN S3</div>
        </div>
      </div>
      <div class="session-xp">🎙️ Episodio 2 · 💪 Retos de fuerza · ⚡ +25 XP</div>
      <div style="margin-top:8px; font-size:11px; padding:6px 10px; background:rgba(231,76,60,0.1); border-radius:5px; border:1px solid rgba(231,76,60,0.3); color:var(--red-glow)">
        🔴 PODER HOPPER ACTIVO: Si demuestras determinación ante el fracaso → 2x XP
      </div>

      <!-- PANEL DESPLEGABLE S2 -->
      <div id="s2-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">

        <!-- JUEGOS Y RETOS -->
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ JUEGOS Y RETOS DE LA SESIÓN</div>

        <div style="display:grid; gap:10px; margin-bottom:16px">

          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green); letter-spacing:1px">NIVEL 1 — EXPLORADOR</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🧘 Test de Flexibilidad Guardián</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Realiza el test de flexibilidad en parejas (toe-touch y mariposa). Registra tu resultado inicial en el diario. ¿Eres más flexible que tu compañero/a? ¿Por qué crees que es así?</div>
            <div style="display:flex; align-items:center; gap:8px">
              <input type="checkbox" class="reto-checkbox" id="s2r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)">
              <label for="s2r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label>
            </div>
          </div>

          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green); letter-spacing:1px">NIVEL 1 — EXPLORADOR</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🫀 Registro de Sensaciones Corporales</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Después de cada reto de fuerza, para 30 segundos y escribe en tu Mood Meter cómo se siente tu cuerpo (fatiga, calor, tensión muscular…). ¿Tu cuerpo te da señales? ¿Las escuchas?</div>
            <div style="display:flex; align-items:center; gap:8px">
              <input type="checkbox" class="reto-checkbox" id="s2r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)">
              <label for="s2r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label>
            </div>
          </div>

          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow); letter-spacing:1px">NIVEL 2 — GUARDIÁN</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">💪 Circuito de Fuerza: Las Estaciones de Hawkins</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:6px">5 estaciones rotativas (2 min c/u). Elige la intensidad que puedas mantener con buena técnica:</div>
            <div style="display:grid; gap:4px; margin-bottom:8px">
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟢 <strong>Básico:</strong> Apoyos de rodillas, flexión parcial de brazos</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟡 <strong>Medio:</strong> Plancha completa 20s, sentadillas con peso corporal</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🔴 <strong>Avanzado:</strong> Plancha lateral, sentadilla búlgara, fondos</div>
            </div>
            <div style="display:flex; align-items:center; gap:8px">
              <input type="checkbox" class="reto-checkbox" id="s2r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)">
              <label for="s2r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label>
            </div>
          </div>

          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow); letter-spacing:1px">NIVEL 2 — GUARDIÁN</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🤸 El Reto de la Elasticidad</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">En grupos de 3: uno hace el estiramiento, los otros observan y dan feedback técnico. ¿Qué músculos trabaja? ¿La postura es correcta? El observador tiene el poder de Hopper: si da buen feedback sin rendirse → 2x XP.</div>
            <div style="display:flex; align-items:center; gap:8px">
              <input type="checkbox" class="reto-checkbox" id="s2r4" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)">
              <label for="s2r4" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label>
            </div>
          </div>

          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; align-items:flex-start; margin-bottom:6px">
              <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow); letter-spacing:1px">NIVEL 3 — ÉLITE 🔥</div>
              <div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div>
            </div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🎙️ Captura tu Hallazgo para el Podcast</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Durante la sesión, identifica UN momento en que tu cuerpo te sorprendió (positiva o negativamente). Grábalo en audio (15–30 seg) describiendo qué pasó y qué aprendiste. Ese fragmento irá en el Episodio 2.</div>
            <div style="display:flex; align-items:center; gap:8px">
              <input type="checkbox" class="reto-checkbox" id="s2r5" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)">
              <label for="s2r5" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label>
            </div>
          </div>
        </div>

        <!-- PODCAST EP2 -->
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--red-glow); letter-spacing:2px; margin-bottom:12px">🎙️ EPISODIO 2 DEL PODCAST — QUÉ INCLUIR</div>

        <div style="background:linear-gradient(135deg,rgba(192,57,43,0.08),transparent); border:1px solid rgba(192,57,43,0.3); border-radius:10px; padding:16px">
          <div style="font-family:'Orbitron',sans-serif; font-size:12px; font-weight:700; color:var(--text); margin-bottom:4px">💪 "Fuerza, flexibilidad y lo que siente el cuerpo"</div>
          <div style="font-size:11px; color:var(--text-dim); margin-bottom:12px; font-style:italic">Duración orientativa: 3–5 minutos · Grabación en grupos</div>

          <div style="display:grid; gap:8px">
            <div style="display:flex; gap:10px; align-items:flex-start">
              <div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-family:'Orbitron',sans-serif; font-size:9px; font-weight:700; color:white; flex-shrink:0; margin-top:1px">1</div>
              <div>
                <div style="font-size:12px; font-weight:700; margin-bottom:2px">Presentación del episodio</div>
                <div style="font-size:11px; color:var(--text-dim)">Presentad el episodio con el nombre en clave del grupo y el título. Ej: <em>"Bienvenidos al Episodio 2 del Podcast Guardián. Hoy descubrimos de qué estamos hechos…"</em></div>
              </div>
            </div>
            <div style="display:flex; gap:10px; align-items:flex-start">
              <div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-family:'Orbitron',sans-serif; font-size:9px; font-weight:700; color:white; flex-shrink:0; margin-top:1px">2</div>
              <div>
                <div style="font-size:12px; font-weight:700; margin-bottom:2px">¿Qué trabajamos hoy?</div>
                <div style="font-size:11px; color:var(--text-dim)">Explicad con vuestras palabras qué es la fuerza y la flexibilidad y por qué son importantes para la salud. Usad ejemplos reales de lo que habéis sentido durante los retos.</div>
              </div>
            </div>
            <div style="display:flex; gap:10px; align-items:flex-start">
              <div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-family:'Orbitron',sans-serif; font-size:9px; font-weight:700; color:white; flex-shrink:0; margin-top:1px">3</div>
              <div>
                <div style="font-size:12px; font-weight:700; margin-bottom:2px">El momento que mi cuerpo me sorprendió 🎯</div>
                <div style="font-size:11px; color:var(--text-dim)">Cada miembro del grupo comparte en 15–20 segundos: <em>"Lo que más me sorprendió de mi cuerpo hoy fue…"</em> (aquí van los fragmentos del Reto Élite).</div>
              </div>
            </div>
            <div style="display:flex; gap:10px; align-items:flex-start">
              <div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-family:'Orbitron',sans-serif; font-size:9px; font-weight:700; color:white; flex-shrink:0; margin-top:1px">4</div>
              <div>
                <div style="font-size:12px; font-weight:700; margin-bottom:2px">Mensaje para el alumnado de 1º</div>
                <div style="font-size:11px; color:var(--text-dim)">Terminar con un consejo breve y directo dirigido a los más pequeños: <em>"Si tuviéramos que daros un consejo sobre cuidar vuestra fuerza y flexibilidad, sería…"</em></div>
              </div>
            </div>
          </div>

          <div style="margin-top:12px; padding:8px 12px; background:rgba(0,212,255,0.08); border:1px solid rgba(0,212,255,0.25); border-radius:6px">
            <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--cyan); margin-bottom:4px">💡 CONSEJO GUARDIÁN</div>
            <div style="font-size:11px; color:var(--text-dim)">Grabad desde un lugar tranquilo. Podéis leer un guion pero intentad que suene natural. Si alguien comete un error hablando → ¡no paréis! Los errores también enseñan (eso lo trabajaréis en el Ep. 3).</div>
          </div>
        </div>

      </div>
    </div>

    <!-- S3 -->
    <div class="session-card" id="scard-3" style="cursor:pointer" onclick="togglePanel('s3',event)">
      <div class="session-badge" style="background:rgba(243,156,18,0.1); border:1px solid var(--yellow)">🏃</div>
      <div class="session-num">SESIÓN 3 · Q-SORT <span id="s3-arrow" style="font-size:11px; color:var(--yellow); margin-left:6px">▼ VER DETALLE</span></div>
      <div class="session-name">EL ENTRENAMIENTO DE LA RESISTENCIA DEL GUARDIÁN</div>
      <div class="session-desc">Retos de resistencia y desmontaje de mitos sobre el cuerpo mediante Q-Sort. ¿Verdad o mito sobre el ejercicio?</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#f39c12; background:rgba(243,156,18,0.1)">⚡</div>
        <div class="char-info">
          <div class="char-name" style="color:#f39c12">🔓 SE DESBLOQUEA: DUSTIN</div>
          <div class="char-power">Poder: <strong>Ingenio</strong> — "Encuentra la solución donde nadie más la ve"</div>
          <div class="power-badge" style="background:rgba(243,156,18,0.15); color:#f39c12; border:1px solid #f39c12">ACTIVO EN S4</div>
        </div>
      </div>
      <div class="session-xp">📊 Q-Sort (5%) · 🏃 Resistencia · ⚡ +30 XP</div>
      <div style="margin-top:8px; font-size:11px; padding:6px 10px; background:rgba(52,152,219,0.1); border-radius:5px; border:1px solid rgba(52,152,219,0.3); color:#3498db">
        🌪️ PODER ONCE ACTIVO: Si usas estrategias creativas → 2x XP
      </div>
      <div id="s3-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ JUEGOS Y RETOS DE LA SESIÓN</div>
        <div style="display:grid; gap:10px; margin-bottom:16px">
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">📋 Cazamitos Express</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Se reparten 10 tarjetas con afirmaciones sobre el ejercicio (5 verdaderas, 5 falsas). Individualmente las clasificas en MITO o REALIDAD. Después se contrastan en pareja. ¿Cuántas acertaste?</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s3r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s3r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🏃 Circuito de Resistencia: El Portal</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:6px">4 estaciones de 3 minutos. Elige tu nivel de intensidad:</div>
            <div style="display:grid; gap:4px; margin-bottom:8px">
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟢 <strong>Básico:</strong> Marcha continua, trote suave alrededor del espacio</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟡 <strong>Medio:</strong> Carrera continua 3 min, cambio de ritmo en señal</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🔴 <strong>Avanzado:</strong> Intervals: 30s rápido / 30s recuperación x3</div>
            </div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s3r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s3r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🃏 Q-Sort: ¿Verdad o mentira del Upside Down?</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">En grupos de 3, ordenáis 8 afirmaciones sobre salud y ejercicio en una escala del "Totalmente mito" al "Totalmente cierto". Cada grupo debe justificar las 2 tarjetas más extremas. El Poder de Once: si propones un argumento creativo y original → 2x XP.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s3r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s3r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow)">NIVEL 3 — ÉLITE 🔥</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🔬 Contrasta con la Experiencia</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Elige 1 mito desmontado hoy y graba un audio de 20 segundos explicando por qué es falso usando lo que sentiste en el circuito de resistencia. Es decir: contrastáis el mito con vuestra propia experiencia corporal de hoy.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s3r4" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)"><label for="s3r4" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
        </div>
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--red-glow); letter-spacing:2px; margin-bottom:12px">🎙️ NOTA PODCAST — MATERIAL PARA EL EP. 2</div>
        <div style="background:rgba(243,156,18,0.08); border:1px solid rgba(243,156,18,0.3); border-radius:8px; padding:14px">
          <div style="font-size:12px; color:var(--text-dim); line-height:1.7">Esta sesión no tiene episodio propio, pero el <strong style="color:var(--yellow)">Q-Sort</strong> genera material clave para completar el Episodio 2: el fragmento de "mitos desmontados con experiencia propia" va directo al podcast. Guardad los audios del Reto Élite.</div>
        </div>
      </div>
    </div>

    <!-- S4 -->
    <div class="session-card" id="scard-4" style="cursor:pointer" onclick="togglePanel('s4',event)">
      <div class="session-badge" style="background:rgba(142,68,173,0.1); border:1px solid var(--purple)">😤</div>
      <div class="session-num">SESIÓN 4 · DIANA AUTOEVALUACIÓN <span id="s4-arrow" style="font-size:11px; color:var(--purple); margin-left:6px">▼ VER DETALLE</span></div>
      <div class="session-name">LOS ERRORES TAMBIÉN ENSEÑAN</div>
      <div class="session-desc">Gestión emocional ante el error en ejercicios de fuerza y velocidad. Grabación del tercer episodio del podcast.</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#8e44ad; background:rgba(142,68,173,0.1)">🎶</div>
        <div class="char-info">
          <div class="char-name" style="color:#8e44ad">🔓 SE DESBLOQUEA: MAX</div>
          <div class="char-power">Poder: <strong>Resiliencia</strong> — "Kate Bush te recuerda que puedes levantarte"</div>
          <div class="power-badge" style="background:rgba(142,68,173,0.15); color:#8e44ad; border:1px solid #8e44ad">ACTIVO EN S5</div>
        </div>
      </div>
      <div class="session-xp">🎙️ Episodio 3 · 😤 Gestión emocional · ⚡ +35 XP</div>
      <div style="margin-top:8px; font-size:11px; padding:6px 10px; background:rgba(243,156,18,0.1); border-radius:5px; border:1px solid rgba(243,156,18,0.3); color:#f39c12">
        ⚡ PODER DUSTIN ACTIVO: Si propones soluciones ingeniosas → 2x XP
      </div>
      <div id="s4-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ JUEGOS Y RETOS DE LA SESIÓN</div>
        <div style="display:grid; gap:10px; margin-bottom:16px">
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">😤 Mood Meter del Error</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Cada vez que fallas en un ejercicio de fuerza o velocidad, para 10 segundos y anota en el Mood Meter (alta/baja energía × agradable/desagradable) dónde estás emocionalmente. Identifica al menos 3 momentos distintos durante la sesión.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s4r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s4r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">💪 Circuito de Fuerza + Velocidad con Protocolo</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:6px">3 estaciones de fuerza y 2 de velocidad. Antes de cada estación, el grupo decide su nivel. Cuando alguien falla, el grupo aplica el "Protocolo del Error": <em>nombrar lo que pasó → proponer solución → reintentar.</em></div>
            <div style="display:grid; gap:4px; margin-bottom:8px">
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟢 <strong>Básico:</strong> Sentadillas lentas, carrera corta 10m</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟡 <strong>Medio:</strong> Burpees sin salto, carrera de ida y vuelta</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🔴 <strong>Avanzado:</strong> Burpees completos, sprint + cambio de dirección</div>
            </div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s4r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s4r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🎯 Diana de Autoevaluación</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Al final de la sesión, completa la Diana de Autoevaluación en la sección correspondiente. Valora honestamente tu gestión emocional de hoy. El Poder de Dustin activo: si propones una estrategia original de gestión → 2x XP.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s4r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s4r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow)">NIVEL 3 — ÉLITE 🔥</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🎙️ Captura el Momento del Error para el Podcast</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Graba un audio de 20–30 seg describiendo un error real de hoy: qué pasó, qué sentiste y cómo lo superaste. Sé honesto/a — los oyentes de 1º necesitan saber que equivocarse es parte del aprendizaje.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s4r4" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)"><label for="s4r4" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
        </div>
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--red-glow); letter-spacing:2px; margin-bottom:12px">🎙️ EPISODIO 3 DEL PODCAST — QUÉ INCLUIR</div>
        <div style="background:linear-gradient(135deg,rgba(192,57,43,0.08),transparent); border:1px solid rgba(192,57,43,0.3); border-radius:10px; padding:16px">
          <div style="font-family:'Orbitron',sans-serif; font-size:12px; font-weight:700; margin-bottom:4px">😤 "Los errores también enseñan"</div>
          <div style="font-size:11px; color:var(--text-dim); margin-bottom:12px; font-style:italic">Duración: 3–5 min · Grabación grupal</div>
          <div style="display:grid; gap:8px">
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">1</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Presentación del episodio</div><div style="font-size:11px; color:var(--text-dim)">Breve recap del episodio 2 y entrada al tema: <em>"Hoy vamos a hablar de algo que nadie quiere reconocer: los errores. Y os vamos a demostrar que son nuestros mejores maestros."</em></div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">2</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Los momentos del Mood Meter</div><div style="font-size:11px; color:var(--text-dim)">Cada miembro del grupo cuenta brevemente las 3 emociones que registró. ¿Coincidisteis? ¿Hubo diferencias dentro del grupo?</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">3</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Los audios del error real 🎤</div><div style="font-size:11px; color:var(--text-dim)">Insertar aquí los fragmentos del Reto Élite: cada uno comparte su momento de error y superación. Esto es el núcleo del episodio.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">4</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Mensaje final para los de 1º</div><div style="font-size:11px; color:var(--text-dim)"><em>"Si os equivocáis en clase de EF, recordad que…"</em> — Un mensaje corto, directo y desde la experiencia de hoy.</div></div></div>
          </div>
          <div style="margin-top:12px; padding:8px 12px; background:rgba(0,212,255,0.08); border:1px solid rgba(0,212,255,0.25); border-radius:6px">
            <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--cyan); margin-bottom:4px">💡 CONSEJO GUARDIÁN</div>
            <div style="font-size:11px; color:var(--text-dim)">Este episodio es el más humano y poderoso del podcast. No editéis los momentos de vacilación o nerviosismo al hablar — eso también es autenticidad.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- S5 -->
    <div class="session-card" id="scard-5" style="cursor:pointer" onclick="togglePanel('s5',event)">
      <div class="session-badge" style="background:rgba(0,255,136,0.1); border:1px solid var(--green)">🛡️</div>
      <div class="session-num">SESIÓN 5 · LC EVALUACIÓN <span id="s5-arrow" style="font-size:11px; color:var(--green); margin-left:6px">▼ VER DETALLE</span></div>
      <div class="session-name">EL VIRUS DEL CONFLICTO: CREANDO NUESTRA VACUNA</div>
      <div class="session-desc">Simulación de conflictos en retos de flexibilidad y creación de pautas de seguridad. Grabación del cuarto episodio.</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#00ff88; background:rgba(0,255,136,0.1)">🧭</div>
        <div class="char-info">
          <div class="char-name" style="color:#00ff88">🔓 SE DESBLOQUEA: LUCAS</div>
          <div class="char-power">Poder: <strong>Liderazgo</strong> — "Guía al grupo hacia la salida del Mundo al Revés"</div>
          <div class="power-badge" style="background:rgba(0,255,136,0.15); color:#00ff88; border:1px solid #00ff88">ACTIVO EN S6</div>
        </div>
      </div>
      <div class="session-xp">🎙️ Episodio 4 · 🛡️ Vacuna conflictos · ⚡ +40 XP</div>
      <div style="margin-top:8px; font-size:11px; padding:6px 10px; background:rgba(142,68,173,0.1); border-radius:5px; border:1px solid rgba(142,68,173,0.3); color:#8e44ad">
        🎶 PODER MAX ACTIVO: Si te recuperas de una dificultad → 2x XP
      </div>
      <div id="s5-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ JUEGOS Y RETOS DE LA SESIÓN</div>
        <div style="display:grid; gap:10px; margin-bottom:16px">
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🛡️ El Mapa de Seguridad</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Antes de empezar, en parejas identificáis 3 situaciones que podrían ser peligrosas en los retos de flexibilidad (ej: forzar una postura, reírse de alguien). Las escribís y proponéis su norma de seguridad. El profe valida.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s5r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s5r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🧘 Circuito de Flexibilidad con Rol</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:6px">3 estaciones de flexibilidad por parejas. Un rol activo (hace el estiramiento) y un rol observador (da feedback). Rotáis cada 2 min. El Poder de Max: si alguien supera una dificultad con actitud positiva → 2x XP.</div>
            <div style="display:grid; gap:4px; margin-bottom:8px">
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟢 <strong>Básico:</strong> Estiramiento isquiotibiales sentado, apertura de cadera</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟡 <strong>Medio:</strong> Estiramiento con asistencia suave del compañero</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🔴 <strong>Avanzado:</strong> FNP simplificado: contraer 6s → relajar → profundizar</div>
            </div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s5r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s5r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">⚔️ Simulación del Conflicto</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">El profe introduce una situación de conflicto simulada (ej: "alguien se ríe de que no llegas al suelo"). El grupo identifica el problema, propone una pauta de resolución y la aplica. Se evalúa con la Lista de Cotejo.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s5r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s5r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow)">NIVEL 3 — ÉLITE 🔥</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">💉 Nuestra Vacuna: La Pauta del Grupo</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">El grupo elabora cooperativamente una "Vacuna Anti-Conflicto": una lista de 3 pautas propias (no copiadas) que aplicaréis en la UD. La presentáis en voz alta y grabáis el fragmento para el Episodio 4.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s5r4" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)"><label for="s5r4" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
        </div>
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--red-glow); letter-spacing:2px; margin-bottom:12px">🎙️ EPISODIO 4 DEL PODCAST — QUÉ INCLUIR</div>
        <div style="background:linear-gradient(135deg,rgba(192,57,43,0.08),transparent); border:1px solid rgba(192,57,43,0.3); border-radius:10px; padding:16px">
          <div style="font-family:'Orbitron',sans-serif; font-size:12px; font-weight:700; margin-bottom:4px">🛡️ "Nuestra vacuna contra el conflicto"</div>
          <div style="font-size:11px; color:var(--text-dim); margin-bottom:12px; font-style:italic">Duración: 3–5 min · Grabación grupal</div>
          <div style="display:grid; gap:8px">
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">1</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Presentación y contexto</div><div style="font-size:11px; color:var(--text-dim)">¿Por qué surgen conflictos cuando hacemos ejercicio? Una reflexión breve y honesta del grupo.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">2</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Medidas de seguridad del grupo</div><div style="font-size:11px; color:var(--text-dim)">Las 3 normas de seguridad que identificasteis al inicio de la sesión. Explicad con ejemplos por qué son importantes.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">3</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">La estrategia que usamos</div><div style="font-size:11px; color:var(--text-dim)">Contad el conflicto simulado y cómo lo resolvisteis. <em>"Cuando pasó X, nosotros hicimos Y porque Z..."</em></div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:var(--red-dark); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:white; flex-shrink:0">4</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">La Vacuna Anti-Conflicto 💉</div><div style="font-size:11px; color:var(--text-dim)">Presentad vuestras 3 pautas propias al oyente de 1º de forma directa y aplicable.</div></div></div>
          </div>
          <div style="margin-top:12px; padding:8px 12px; background:rgba(0,212,255,0.08); border:1px solid rgba(0,212,255,0.25); border-radius:6px">
            <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--cyan); margin-bottom:4px">💡 CONSEJO GUARDIÁN</div>
            <div style="font-size:11px; color:var(--text-dim)">Este episodio se evalúa con Lista de Cotejo. Aseguraos de que aparezcan explícitamente: 1 estrategia de resolución de conflictos + al menos 1 medida de seguridad.</div>
          </div>
        </div>
      </div>
    </div>

    <!-- S6-7 -->
    <div class="session-card" id="scard-6" style="cursor:pointer" onclick="togglePanel('s6',event)">
      <div class="session-badge" style="background:rgba(231,76,60,0.1); border:1px solid var(--red-glow)">🏆</div>
      <div class="session-num">SESIONES 6-7 · RETO FINAL <span id="s6-arrow" style="font-size:11px; color:var(--red-glow); margin-left:6px">▼ VER DETALLE</span></div>
      <div class="session-name">EL PASO FINAL: DAR FORMA A NUESTRO MENSAJE</div>
      <div class="session-desc">Circuito de condición física, entrevistas grupales y difusión del podcast final al alumnado del primer ciclo. ¡Es la hora!</div>
      <div class="session-character">
        <div class="char-avatar" style="border-color:#e74c3c; background:rgba(231,76,60,0.1)">🔥</div>
        <div class="char-info">
          <div class="char-name" style="color:#e74c3c">🔓 SE DESBLOQUEA: WILL</div>
          <div class="char-power">Poder: <strong>Empatía</strong> — "Sientes lo que el grupo necesita antes de que lo digan"</div>
          <div class="power-badge" style="background:rgba(231,76,60,0.15); color:#e74c3c; border:1px solid #e74c3c">PODER FINAL</div>
        </div>
      </div>
      <div class="session-xp">🏆 Circuito final + Podcast completo · ⚡ +80 XP</div>
      <div style="margin-top:8px; font-size:11px; padding:6px 10px; background:rgba(0,255,136,0.1); border-radius:5px; border:1px solid rgba(0,255,136,0.3); color:#00ff88">
        🧭 PODER LUCAS ACTIVO: Si liderás a compañeros/as → 2x XP
      </div>
      <div id="s6-panel" style="display:none; margin-top:16px; border-top:1px solid var(--border); padding-top:16px">
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">⚔️ SESIÓN 6 — CIRCUITO FINAL DE CONDICIÓN FÍSICA</div>
        <div style="display:grid; gap:10px; margin-bottom:16px">
          <div style="background:rgba(0,255,136,0.06); border:1px solid rgba(0,255,136,0.2); border-left:4px solid var(--green); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green)">NIVEL 1 — EXPLORADOR</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+20 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">📈 Compara tu Progreso</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Repite los mismos tests de la S1 (pulso en reposo, test de flexibilidad). Compara los resultados con los de la primera sesión. ¿Ha cambiado algo? Anótalo en el diario — es tu evidencia de mejora para el OA 2.3.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s6r1" onclick="event.stopPropagation()" onchange="onRetoCheck(this,20)"><label for="s6r1" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(243,156,18,0.06); border:1px solid rgba(243,156,18,0.2); border-left:4px solid var(--yellow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--yellow)">NIVEL 2 — GUARDIÁN</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+35 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🏋️ Circuito Completo: Las 6 Estaciones del Guardián</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:6px">6 estaciones (2 min c/u): fuerza, flexibilidad, resistencia, velocidad, coordinación y pausa de reflexión. Cada guardián elige su nivel. El Poder de Lucas activo: quien ayude o guíe a otro guardián → 2x XP.</div>
            <div style="display:grid; gap:4px; margin-bottom:8px">
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟢 <strong>Básico:</strong> Versiones modificadas de todos los ejercicios</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🟡 <strong>Medio:</strong> Versiones estándar con buen control técnico</div>
              <div style="font-size:11px; padding:4px 8px; background:rgba(255,255,255,0.03); border-radius:4px">🔴 <strong>Avanzado:</strong> Versiones de mayor intensidad o complejidad</div>
            </div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s6r2" onclick="event.stopPropagation()" onchange="onRetoCheck(this,35)"><label for="s6r2" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
          <div style="background:rgba(231,76,60,0.06); border:1px solid rgba(231,76,60,0.2); border-left:4px solid var(--red-glow); border-radius:8px; padding:12px">
            <div style="display:flex; justify-content:space-between; margin-bottom:6px"><div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--red-glow)">NIVEL 3 — ÉLITE 🔥</div><div style="font-family:'Share Tech Mono',monospace; font-size:9px; color:var(--yellow)">+50 XP</div></div>
            <div style="font-weight:700; font-size:13px; margin-bottom:4px">🎙️ Entrevistas del Podcast Final</div>
            <div style="font-size:12px; color:var(--text-dim); margin-bottom:8px">Durante o tras el circuito, cada miembro responde en audio a: <em>"¿Qué aprendiste sobre tu cuerpo en esta UD? ¿Qué cambiarías de tus hábitos?"</em> Estos fragmentos forman el cierre del Podcast Guardián completo.</div>
            <div style="display:flex; align-items:center; gap:8px"><input type="checkbox" class="reto-checkbox" id="s6r3" onclick="event.stopPropagation()" onchange="onRetoCheck(this,50)"><label for="s6r3" style="font-size:11px; color:var(--text-dim); cursor:pointer" onclick="event.stopPropagation()">Completado ✓</label></div>
          </div>
        </div>
        <div style="font-family:'Orbitron',sans-serif; font-size:10px; color:var(--cyan); letter-spacing:2px; margin-bottom:12px">📢 SESIÓN 7 — DIFUSIÓN DEL PODCAST</div>
        <div style="background:rgba(0,212,255,0.06); border:1px solid rgba(0,212,255,0.25); border-radius:8px; padding:14px; margin-bottom:16px">
          <div style="display:grid; gap:8px">
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:rgba(0,212,255,0.2); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:var(--cyan); flex-shrink:0">1</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Montaje final del podcast grupal</div><div style="font-size:11px; color:var(--text-dim)">Revisad y ordenad los 4 episodios. Añadid la intro, los cierres de cada episodio y las entrevistas finales. Escuchadlo completo en grupo antes de difundirlo.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:rgba(0,212,255,0.2); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:var(--cyan); flex-shrink:0">2</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Coevaluación grupal</div><div style="font-size:11px; color:var(--text-dim)">Cada grupo escucha el podcast de otro grupo y completa la rúbrica de un solo punto. Feedback constructivo y específico.</div></div></div>
            <div style="display:flex; gap:10px; align-items:flex-start"><div style="min-width:22px; height:22px; background:rgba(0,212,255,0.2); border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:9px; font-weight:700; color:var(--cyan); flex-shrink:0">3</div><div><div style="font-size:12px; font-weight:700; margin-bottom:2px">Difusión al alumnado de 1º ciclo</div><div style="font-size:11px; color:var(--text-dim)">El podcast se comparte con los cursos de 1º. Si es posible, una delegación del grupo lo presenta en directo. ¡VECNA ha sido derrotado!</div></div></div>
          </div>
        </div>
        <div style="background:linear-gradient(135deg,rgba(192,57,43,0.1),transparent); border:1px solid var(--red-glow); border-radius:10px; padding:16px; text-align:center">
          <div style="font-size:32px; margin-bottom:6px">🔥</div>
          <div style="font-family:'Creepster',cursive; font-size:20px; color:var(--red-glow); text-shadow:var(--glow-red); margin-bottom:6px">¡INSIGNIA HOPPER DESBLOQUEADA!</div>
          <div style="font-size:12px; color:var(--text-dim)">Al completar esta sesión y difundir el podcast, la clase obtiene la Insignia Hopper. Pegadla en el mapa del Mundo al Revés del gimnasio. <strong>VECNA ha perdido un fragmento de su poder.</strong></div>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- =================== RETOS =================== -->
<div class="section" id="section-retos">
  <div style="margin-bottom:20px">
    <p style="font-size:13px; color:var(--text-dim); line-height:1.6">Los retos se activan durante las sesiones. Marca los que vayas superando para ganar XP y debilitar a VECNA. Hay tres niveles de dificultad — ¡elige el tuyo!</p>
  </div>

  <div style="margin-bottom:15px; font-family:'Orbitron',sans-serif; font-size:11px; color:var(--cyan); letter-spacing:2px">⚔️ NIVEL 1 — EXPLORADOR DEL UPSIDE DOWN</div>
  <div class="retos-grid">
    <div class="reto-card nivel-1">
      <div class="reto-level">NIVEL 1</div>
      <div class="reto-title">🫀 El Pulso Guardián</div>
      <div class="reto-desc">Localiza y mide tu pulso en reposo. Compáralo con el de un/a compañero/a. ¿Quién tiene el corazón más tranquilo?</div>
      <div class="reto-reward">🏅 Recompensa: +20 XP · -5 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r1" onchange="onRetoCheck(this,20)">
        <label for="r1">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-1">
      <div class="reto-level">NIVEL 1</div>
      <div class="reto-title">🧘 Flexibilidad del Guardián</div>
      <div class="reto-desc">Realiza el test de flexibilidad y registra en tu diario tu nivel inicial. ¿Puedes mejorar en la siguiente sesión?</div>
      <div class="reto-reward">🏅 Recompensa: +20 XP · -5 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r2" onchange="onRetoCheck(this,20)">
        <label for="r2">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-1">
      <div class="reto-level">NIVEL 1</div>
      <div class="reto-title">📋 Cazamitos</div>
      <div class="reto-desc">En el Q-Sort, identifica al menos 3 mitos sobre el ejercicio físico y los rechazas con un argumento propio.</div>
      <div class="reto-reward">🏅 Recompensa: +20 XP · -5 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r3" onchange="onRetoCheck(this,20)">
        <label for="r3">Marcar como completado</label>
      </div>
    </div>
  </div>

  <div style="margin:20px 0 15px; font-family:'Orbitron',sans-serif; font-size:11px; color:var(--yellow); letter-spacing:2px">⚔️ NIVEL 2 — GUARDIÁN EN ENTRENAMIENTO</div>
  <div class="retos-grid">
    <div class="reto-card nivel-2">
      <div class="reto-level">NIVEL 2</div>
      <div class="reto-title">🏃 Resistencia del Portal</div>
      <div class="reto-desc">Completa el circuito de resistencia sin parar más de 10 segundos. Registra cómo te has sentido al acabar.</div>
      <div class="reto-reward">🏅 Recompensa: +35 XP · -10 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r4" onchange="onRetoCheck(this,35)">
        <label for="r4">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-2">
      <div class="reto-level">NIVEL 2</div>
      <div class="reto-title">😤 El Protocolo del Error</div>
      <div class="reto-desc">Cuando te equivocas en un ejercicio, describís en voz alta qué salió mal y propones una solución. Sin rendirse.</div>
      <div class="reto-reward">🏅 Recompensa: +35 XP · -10 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r5" onchange="onRetoCheck(this,35)">
        <label for="r5">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-2">
      <div class="reto-level">NIVEL 2</div>
      <div class="reto-title">🤝 La Vacuna del Conflicto</div>
      <div class="reto-desc">En la simulación de conflictos, identifica el problema, propone una pauta y la aplica con éxito junto al grupo.</div>
      <div class="reto-reward">🏅 Recompensa: +35 XP · -10 HP Vecna</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r6" onchange="onRetoCheck(this,35)">
        <label for="r6">Marcar como completado</label>
      </div>
    </div>
  </div>

  <div style="margin:20px 0 15px; font-family:'Orbitron',sans-serif; font-size:11px; color:var(--red-glow); letter-spacing:2px">⚔️ NIVEL 3 — GUARDIÁN ÉLITE</div>
  <div class="retos-grid">
    <div class="reto-card nivel-3">
      <div class="reto-level">NIVEL 3 🔥</div>
      <div class="reto-title">🎙️ Voz Guardiana</div>
      <div class="reto-desc">Propones y grabas un fragmento del podcast donde explicas con tus propias palabras al menos 2 beneficios del ejercicio para la salud mental y física.</div>
      <div class="reto-reward">🏅 Recompensa: +50 XP · -15 HP Vecna · 🏆 Emblema Voz</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r7" onchange="onRetoCheck(this,50)">
        <label for="r7">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-3">
      <div class="reto-level">NIVEL 3 🔥</div>
      <div class="reto-title">💡 Diseña tu Estación</div>
      <div class="reto-desc">Diseñas y lideras una estación del circuito final con consignas claras, opciones de intensidad y feedback para tus compañeros/as.</div>
      <div class="reto-reward">🏅 Recompensa: +50 XP · -15 HP Vecna · 🏆 Emblema Líder</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r8" onchange="onRetoCheck(this,50)">
        <label for="r8">Marcar como completado</label>
      </div>
    </div>
    <div class="reto-card nivel-3">
      <div class="reto-level">NIVEL 3 🔥</div>
      <div class="reto-title">🌟 Mejora Personal Documentada</div>
      <div class="reto-desc">Demuestras con evidencias (datos, grabaciones o reflexiones) al menos 2 mejoras personales en capacidades físicas entre la sesión 1 y la 6-7.</div>
      <div class="reto-reward">🏅 Recompensa: +50 XP · -15 HP Vecna · 🏆 Emblema Progreso</div>
      <div class="reto-check">
        <input type="checkbox" class="reto-checkbox" id="r9" onchange="onRetoCheck(this,50)">
        <label for="r9">Marcar como completado</label>
      </div>
    </div>
  </div>
</div>

<!-- =================== PERSONAJES =================== -->
<div class="section" id="section-personajes">
  <p style="font-size:13px; color:var(--text-dim); margin-bottom:20px; line-height:1.6">Desbloquea a los Guardianes superando cada sesión. Sus poderes se activan en la sesión siguiente: si el grupo muestra ese poder, ¡obtiene el doble de XP!</p>

  <div class="chars-grid">

    <div class="char-card unlocked" id="char-hopper">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #e74c3c;background:rgba(231,76,60,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;animation:pulse-glow 2s infinite;color:#e74c3c">💀</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #e74c3c;background:rgba(231,76,60,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#e74c3c;line-height:1.2;font-style:italic">"Nunca te rindes"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#e74c3c">HOPPER</div>
      <div class="char-card-session" style="color:var(--green)">✅ DESBLOQUEADO — Sesión 1</div>
      <div class="char-card-power-title" style="color:#e74c3c">⚡ PODER: DETERMINACIÓN</div>
      <div class="char-card-power-desc">"Nunca te rindes. Siempre hay un camino, aunque el Upside Down lo haya cubierto todo."</div>
      <div class="char-card-bonus">🔴 <strong>Bonus S2:</strong> Determinación ante el cansancio → <strong>2x XP</strong></div>
      <div class="char-unlock-tag" style="background:rgba(0,255,136,0.15); color:var(--green); border:1px solid var(--green)">DESBLOQUEADO</div>
    </div>

    <div class="char-card locked-char" id="char-once">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #3498db;background:rgba(52,152,219,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;color:#3498db">🌪️</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #3498db;background:rgba(52,152,219,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#3498db;line-height:1.2;font-style:italic">"Tu mente mueve obstáculos"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#3498db">ONCE</div>
      <div class="char-card-session">🔒 Se desbloquea al completar S2</div>
      <div class="char-card-power-title" style="color:#3498db">⚡ PODER: TELEKINESIA</div>
      <div class="char-card-power-desc">"Puedes mover los obstáculos con tu mente. El cuerpo te obedece cuando el pensamiento es claro."</div>
      <div class="char-card-bonus">🌪️ <strong>Bonus S3:</strong> Estrategias creativas → <strong>2x XP</strong></div>
      <div class="char-unlock-tag" id="once-tag" style="background:rgba(255,255,255,0.05); color:var(--text-dim); border:1px solid var(--border)">🔒 BLOQUEADO</div>
    </div>

    <div class="char-card locked-char" id="char-dustin">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #f39c12;background:rgba(243,156,18,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;color:#f39c12">⚙️</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #f39c12;background:rgba(243,156,18,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#f39c12;line-height:1.2;font-style:italic">"Ves lo que otros no ven"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#f39c12">DUSTIN</div>
      <div class="char-card-session">🔒 Se desbloquea al completar S3</div>
      <div class="char-card-power-title" style="color:#f39c12">⚡ PODER: INGENIO</div>
      <div class="char-card-power-desc">"Encuentra la solución donde nadie más la ve. Los mitos sobre el ejercicio no tienen ningún poder sobre ti."</div>
      <div class="char-card-bonus">⚙️ <strong>Bonus S4:</strong> Soluciones ingeniosas → <strong>2x XP</strong></div>
      <div class="char-unlock-tag" id="dustin-tag" style="background:rgba(255,255,255,0.05); color:var(--text-dim); border:1px solid var(--border)">🔒 BLOQUEADO</div>
    </div>

    <div class="char-card locked-char" id="char-max">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #8e44ad;background:rgba(142,68,173,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;color:#8e44ad">🎶</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #8e44ad;background:rgba(142,68,173,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#8e44ad;line-height:1.2;font-style:italic">"Siempre puedes levantarte"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#8e44ad">MAX</div>
      <div class="char-card-session">🔒 Se desbloquea al completar S4</div>
      <div class="char-card-power-title" style="color:#8e44ad">⚡ PODER: RESILIENCIA</div>
      <div class="char-card-power-desc">"Running Up That Hill — Kate Bush te recuerda que siempre puedes levantarte. El error no te define."</div>
      <div class="char-card-bonus">🎶 <strong>Bonus S5:</strong> Actitud positiva ante dificultades → <strong>2x XP</strong></div>
      <div class="char-unlock-tag" id="max-tag" style="background:rgba(255,255,255,0.05); color:var(--text-dim); border:1px solid var(--border)">🔒 BLOQUEADO</div>
    </div>

    <div class="char-card locked-char" id="char-lucas">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #00ff88;background:rgba(0,255,136,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;color:#00ff88">🧭</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #00ff88;background:rgba(0,255,136,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#00ff88;line-height:1.2;font-style:italic">"Guías al grupo a la salida"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#00ff88">LUCAS</div>
      <div class="char-card-session">🔒 Se desbloquea al completar S5</div>
      <div class="char-card-power-title" style="color:#00ff88">⚡ PODER: LIDERAZGO</div>
      <div class="char-card-power-desc">"Guías al grupo hacia la salida. Siempre sabes quién necesita ayuda y cómo dársela."</div>
      <div class="char-card-bonus">🧭 <strong>Bonus S6-7:</strong> Liderazgo en el podcast → <strong>2x XP</strong></div>
      <div class="char-unlock-tag" id="lucas-tag" style="background:rgba(255,255,255,0.05); color:var(--text-dim); border:1px solid var(--border)">🔒 BLOQUEADO</div>
    </div>

    <div class="char-card locked-char" id="char-will">
      <div style="perspective:400px; margin:0 auto 12px; width:80px; height:80px; cursor:pointer" onclick="this.querySelector('.char-flip-inner').style.transform = this.querySelector('.char-flip-inner').style.transform === 'rotateY(180deg)' ? '' : 'rotateY(180deg)'">
        <div class="char-flip-inner" style="position:relative;width:100%;height:100%;transform-style:preserve-3d;transition:transform 0.6s;border-radius:50%">
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:50%;border:3px solid #e74c3c;background:rgba(231,76,60,0.1);display:flex;align-items:center;justify-content:center;font-size:36px;color:#e74c3c">🔥</div>
          <div style="position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;transform:rotateY(180deg);border-radius:50%;border:3px solid #e74c3c;background:rgba(231,76,60,0.2);display:flex;align-items:center;justify-content:center;padding:6px;text-align:center">
            <div style="font-size:8px;color:#e74c3c;line-height:1.2;font-style:italic">"La empatía derrota a VECNA"</div>
          </div>
        </div>
      </div>
      <div style="font-size:8px;color:var(--text-dim);font-family:'Share Tech Mono',monospace;margin-bottom:6px">👆 toca el icono</div>
      <div class="char-card-name" style="color:#e74c3c">WILL</div>
      <div class="char-card-session">🔒 Se desbloquea al completar S6-7 (RETO FINAL)</div>
      <div class="char-card-power-title" style="color:#e74c3c">⚡ PODER: EMPATÍA</div>
      <div class="char-card-power-desc">"Sientes lo que el grupo necesita antes de que lo digan. La empatía es el arma más poderosa contra VECNA."</div>
      <div class="char-card-bonus">🔥 <strong>Poder del cierre:</strong> ¡VECNA ha sido debilitado definitivamente!</div>
      <div class="char-unlock-tag" id="will-tag" style="background:rgba(255,255,255,0.05); color:var(--text-dim); border:1px solid var(--border)">🔒 BLOQUEADO — RETO FINAL</div>
    </div>

  </div>
</div>

<!-- =================== REFLEXIONES =================== -->
<div class="section" id="section-reflexiones">

  <div class="reflection-area">
    <div class="panel-title" style="margin-bottom:15px"><span class="icon">📡</span> DIARIO DEL GUARDIÁN</div>

    <div style="font-size:12px; color:var(--text-dim); margin-bottom:15px">Selecciona la sesión sobre la que quieres reflexionar:</div>

    <div class="reflection-session-select">
      <button class="ref-sess-btn active" onclick="selectRefSession(this,'Sesión 1')">S1</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'Sesión 2')">S2</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'Sesión 3')">S3</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'Sesión 4')">S4</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'Sesión 5')">S5</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'Sesión 6-7')">S6-7</button>
      <button class="ref-sess-btn" onclick="selectRefSession(this,'General')">GENERAL</button>
    </div>

    <div style="font-size:11px; color:var(--text-dim); margin-bottom:10px; font-family:'Share Tech Mono',monospace">💡 PREGUNTAS DETONADOR — Pulsa una para insertarla:</div>

    <div class="ref-prompts">
      <div class="ref-prompt" onclick="insertPrompt(this)">¿Qué descubrí sobre mi cuerpo hoy que no sabía antes?</div>
      <div class="ref-prompt" onclick="insertPrompt(this)">¿Qué emoción sentí cuando me equivoqué y cómo la gestioné?</div>
      <div class="ref-prompt" onclick="insertPrompt(this)">¿Qué haré de forma diferente en la próxima sesión?</div>
      <div class="ref-prompt" onclick="insertPrompt(this)">¿Cómo contribuí al bienestar del grupo hoy?</div>
      <div class="ref-prompt" onclick="insertPrompt(this)">¿Qué mito sobre el ejercicio desmontamos hoy y cómo?</div>
    </div>

    <textarea class="ref-textarea" id="ref-input" placeholder="Escribe aquí tu reflexión como Guardián/a... Esta es tu zona segura. VECNA no puede leer el Diario del Guardián."></textarea>

    <div class="ref-actions">
      <button class="btn-primary" onclick="saveReflection()">💾 GUARDAR EN EL DIARIO</button>
      <button class="btn-secondary" onclick="clearReflection()">🗑️ BORRAR BORRADOR</button>
    </div>
  </div>

  <div class="saved-reflections">
    <div class="saved-title">📂 REFLEXIONES GUARDADAS — ARCHIVO PERSONAL</div>
    <div id="reflections-list">
      <div style="font-size:12px; color:var(--text-dim); text-align:center; padding:20px">Aún no hay reflexiones guardadas. ¡Escribe la primera entrada de tu Diario Guardián!</div>
    </div>
  </div>

</div>

<!-- =================== AUTOEVALUACIÓN =================== -->
<div class="section" id="section-autoeval">

  <div class="panel">
    <div class="panel-title"><span class="icon">🔍</span> KPSI GUARDIÁN — Antes y Después</div>

    <!-- Member selector -->
    <div style="margin-bottom:16px">
      <div style="font-family:'Orbitron',sans-serif;font-size:10px;color:var(--cyan);letter-spacing:2px;margin-bottom:10px">👤 SELECCIONA EL MIEMBRO DEL GRUPO</div>
      <div style="display:flex;gap:8px;flex-wrap:wrap">
        <button class="kpsi-member-btn active" id="kmbtn1" onclick="selectKPSIMember(1,this)" style="padding:8px 16px;background:rgba(0,212,255,0.15);border:2px solid var(--cyan);border-radius:6px;color:var(--cyan);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">MIEMBRO 1</button>
        <button class="kpsi-member-btn" id="kmbtn2" onclick="selectKPSIMember(2,this)" style="padding:8px 16px;background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:6px;color:var(--text-dim);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">MIEMBRO 2</button>
        <button class="kpsi-member-btn" id="kmbtn3" onclick="selectKPSIMember(3,this)" style="padding:8px 16px;background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:6px;color:var(--text-dim);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">MIEMBRO 3</button>
        <button class="kpsi-member-btn" id="kmbtn4" onclick="selectKPSIMember(4,this)" style="padding:8px 16px;background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:6px;color:var(--text-dim);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">MIEMBRO 4</button>
        <button class="kpsi-member-btn" id="kmbtn5" onclick="selectKPSIMember(5,this)" style="padding:8px 16px;background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:6px;color:var(--text-dim);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">MIEMBRO 5</button>
        <button class="kpsi-member-btn" id="kmbtnG" onclick="selectKPSIMember('G',this)" style="padding:8px 16px;background:rgba(255,255,255,0.03);border:2px solid var(--yellow);border-radius:6px;color:var(--yellow);font-family:'Orbitron',sans-serif;font-size:9px;cursor:pointer;transition:all 0.2s">GRUPAL</button>
      </div>
      <div id="kpsi-member-label" style="font-family:'Share Tech Mono',monospace;font-size:10px;color:var(--cyan);margin-top:8px">Rellenando KPSI de: MIEMBRO 1</div>
    </div>

    <p style="font-size:12px; color:var(--text-dim); margin-bottom:16px">Completa la columna <strong style="color:var(--cyan)">INICIO</strong> en la Sesión 1. Al finalizar la UD rellena la columna <strong style="color:var(--green)">FINAL</strong> para ver tu evolución como Guardián.</p>

    <!-- Leyenda niveles -->
    <div style="display:grid; grid-template-columns:repeat(4,1fr); gap:8px; margin-bottom:20px">
      <div style="background:rgba(231,76,60,0.08); border:1px solid rgba(231,76,60,0.3); border-radius:7px; padding:8px; text-align:center">
        <div style="font-size:20px; margin-bottom:3px">🤷</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:8px; font-weight:700; color:var(--red-glow); letter-spacing:1px; margin-bottom:2px">NIVEL 1</div>
        <div style="font-size:10px; color:var(--text-dim)">No lo sé</div>
      </div>
      <div style="background:rgba(243,156,18,0.08); border:1px solid rgba(243,156,18,0.3); border-radius:7px; padding:8px; text-align:center">
        <div style="font-size:20px; margin-bottom:3px">🤔</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:8px; font-weight:700; color:var(--yellow); letter-spacing:1px; margin-bottom:2px">NIVEL 2</div>
        <div style="font-size:10px; color:var(--text-dim)">Lo he oído</div>
      </div>
      <div style="background:rgba(0,212,255,0.08); border:1px solid rgba(0,212,255,0.3); border-radius:7px; padding:8px; text-align:center">
        <div style="font-size:20px; margin-bottom:3px">💡</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:8px; font-weight:700; color:var(--cyan); letter-spacing:1px; margin-bottom:2px">NIVEL 3</div>
        <div style="font-size:10px; color:var(--text-dim)">Lo sé y lo explico</div>
      </div>
      <div style="background:rgba(0,255,136,0.08); border:1px solid rgba(0,255,136,0.3); border-radius:7px; padding:8px; text-align:center">
        <div style="font-size:20px; margin-bottom:3px">🌟</div>
        <div style="font-family:'Orbitron',sans-serif; font-size:8px; font-weight:700; color:var(--green); letter-spacing:1px; margin-bottom:2px">NIVEL 4</div>
        <div style="font-size:10px; color:var(--text-dim)">Lo enseño</div>
      </div>
    </div>

    <!-- Cabecera tabla -->
    <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; padding:8px 12px; background:rgba(255,255,255,0.04); border-radius:6px; margin-bottom:6px">
      <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--text-dim); letter-spacing:1px">CONTENIDO / HABILIDAD</div>
      <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--cyan); text-align:center; letter-spacing:1px">🔵 INICIO</div>
      <div style="font-family:'Orbitron',sans-serif; font-size:9px; color:var(--green); text-align:center; letter-spacing:1px">🌟 FINAL</div>
    </div>

    <!-- Bloque A: Condición física y salud -->
    <div style="font-family:'Share Tech Mono',monospace; font-size:10px; color:var(--yellow); letter-spacing:1px; padding:6px 12px; background:rgba(243,156,18,0.06); border-radius:5px; margin:10px 0 6px">▸ BLOQUE A — CONDICIÓN FÍSICA Y SALUD</div>

    <div style="display:grid; gap:6px; margin-bottom:14px">
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">¿Qué es estar en forma de manera saludable?</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k1i',this.value); updateKPSIArrow('k1')">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k1f',this.value); updateKPSIArrow('k1')">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Diferencia entre fuerza, resistencia y flexibilidad</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k2i',this.value); updateKPSIArrow('k2')">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k2f',this.value); updateKPSIArrow('k2')">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Beneficios del ejercicio para la salud (al menos 3)</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k3i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k3f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Distingo mitos de realidades sobre el ejercicio</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k4i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k4f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
    </div>

    <!-- Bloque D: Emocional -->
    <div style="font-family:'Share Tech Mono',monospace; font-size:10px; color:var(--purple); letter-spacing:1px; padding:6px 12px; background:rgba(142,68,173,0.06); border-radius:5px; margin:10px 0 6px">▸ BLOQUE D — GESTIÓN EMOCIONAL Y CONFLICTOS</div>

    <div style="display:grid; gap:6px; margin-bottom:14px">
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Identifico mis emociones durante el ejercicio</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k5i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k5f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Gestiono el error y el fracaso sin bloquearme</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k6i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k6f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Resuelvo conflictos de forma constructiva en clase</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k7i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k7f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
    </div>

    <!-- Bloque Podcast -->
    <div style="font-family:'Share Tech Mono',monospace; font-size:10px; color:var(--red-glow); letter-spacing:1px; padding:6px 12px; background:rgba(192,57,43,0.06); border-radius:5px; margin:10px 0 6px">▸ BLOQUE PODCAST — COMUNICACIÓN Y DIVULGACIÓN</div>

    <div style="display:grid; gap:6px; margin-bottom:16px">
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Soy capaz de comunicar lo que aprendo en voz alta</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k8i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k8f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
      <div style="display:grid; grid-template-columns:1fr 110px 110px; gap:8px; align-items:center; padding:10px 12px; background:rgba(255,255,255,0.02); border:1px solid var(--border); border-radius:7px">
        <span style="font-size:12px">Puedo colaborar y organizar una tarea en grupo</span>
        <select class="kpsi-select" style="text-align:center" onchange="saveKPSI('k9i',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
        <select class="kpsi-select" style="text-align:center; border-color:rgba(0,255,136,0.3)" onchange="saveKPSI('k9f',this.value)">
          <option value="">—</option><option>🤷 Nv.1</option><option>🤔 Nv.2</option><option>💡 Nv.3</option><option>🌟 Nv.4</option>
        </select>
      </div>
    </div>

    <!-- Botón guardar + resultado visual -->
    <div style="display:flex; gap:10px; flex-wrap:wrap; align-items:center">
      <button class="btn-primary" onclick="saveKPSIFull()">💾 GUARDAR KPSI</button>
      <div id="kpsi-result" style="font-family:'Share Tech Mono',monospace; font-size:12px; color:var(--text-dim)"></div>
    </div>
  </div>

  <div class="panel">
    <div class="panel-title"><span class="icon">⭐</span> DIANA AUTOEVALUACIÓN — Por OA</div>
    <p style="font-size:12px; color:var(--text-dim); margin-bottom:20px">Valora del 1 al 4 tu nivel en cada Objetivo de Aprendizaje al final de cada sesión. 1 = Necesito mejorar | 4 = Guardián Élite</p>

    <div class="autoeval-grid">

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 1.1</div>
        <div class="autoeval-desc">Identifico y explico al menos 3 beneficios del ejercicio para la salud</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa11">
            <button class="star-btn" onclick="setStar('oa11',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa11',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa11',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa11',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa11">Sin valorar</span>
        </div>
      </div>

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 1.3</div>
        <div class="autoeval-desc">Identifico y aplico al menos 3 medidas de seguridad</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa13">
            <button class="star-btn" onclick="setStar('oa13',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa13',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa13',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa13',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa13">Sin valorar</span>
        </div>
      </div>

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 1.4</div>
        <div class="autoeval-desc">Identifico y refiero estrategias usadas para resolver conflictos</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa14">
            <button class="star-btn" onclick="setStar('oa14',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa14',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa14',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa14',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa14">Sin valorar</span>
        </div>
      </div>

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 2.1</div>
        <div class="autoeval-desc">Organizo un mensaje divulgativo sobre AF saludable para el podcast</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa21">
            <button class="star-btn" onclick="setStar('oa21',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa21',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa21',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa21',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa21">Sin valorar</span>
        </div>
      </div>

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 2.3</div>
        <div class="autoeval-desc">Muestro al menos 2 evidencias de mejora personal en capacidades físicas</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa23">
            <button class="star-btn" onclick="setStar('oa23',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa23',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa23',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa23',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa23">Sin valorar</span>
        </div>
      </div>

      <div class="autoeval-item">
        <div class="autoeval-oa">OA 3.1</div>
        <div class="autoeval-desc">Identifico y gestiono al menos 3 emociones surgidas durante la práctica</div>
        <div class="stars-row">
          <div class="stars" id="stars-oa31">
            <button class="star-btn" onclick="setStar('oa31',1)">⭐</button>
            <button class="star-btn" onclick="setStar('oa31',2)">⭐</button>
            <button class="star-btn" onclick="setStar('oa31',3)">⭐</button>
            <button class="star-btn" onclick="setStar('oa31',4)">⭐</button>
          </div>
          <span class="stars-label" id="label-oa31">Sin valorar</span>
        </div>
      </div>

    </div>

    <div style="margin-top:20px">
      <button class="btn-primary" onclick="saveAutoeval()">💾 GUARDAR AUTOEVALUACIÓN</button>
    </div>

    <!-- DIANA VISUAL -->
    <div class="diana-wrapper">
      <div class="diana-title">🎯 DIANA DE PROGRESO GUARDIÁN</div>
      <div class="diana-svg-container">
        <svg id="diana-svg" viewBox="0 0 320 320" width="300" height="300" xmlns="http://www.w3.org/2000/svg">
          <!-- Rings -->
          <circle cx="160" cy="160" r="140" fill="rgba(192,57,43,0.05)" stroke="rgba(192,57,43,0.2)" stroke-width="1"/>
          <circle cx="160" cy="160" r="105" fill="rgba(243,156,18,0.05)" stroke="rgba(243,156,18,0.2)" stroke-width="1"/>
          <circle cx="160" cy="160" r="70" fill="rgba(0,212,255,0.05)" stroke="rgba(0,212,255,0.2)" stroke-width="1"/>
          <circle cx="160" cy="160" r="35" fill="rgba(0,255,136,0.1)" stroke="rgba(0,255,136,0.3)" stroke-width="1"/>
          <!-- Lines -->
          <line x1="160" y1="20" x2="160" y2="300" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
          <line x1="20" y1="160" x2="300" y2="160" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
          <line x1="61" y1="61" x2="259" y2="259" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
          <line x1="259" y1="61" x2="61" y2="259" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
          <line x1="160" y1="20" x2="160" y2="300" stroke="rgba(255,255,255,0.05)"/>
          <!-- Labels -->
          <text x="160" y="12" text-anchor="middle" fill="#f39c12" font-size="9" font-family="monospace">OA 1.1</text>
          <text x="302" y="164" text-anchor="start" fill="#00d4ff" font-size="9" font-family="monospace">OA 1.3</text>
          <text x="160" y="316" text-anchor="middle" fill="#e74c3c" font-size="9" font-family="monospace">OA 2.1</text>
          <text x="12" y="164" text-anchor="end" fill="#00ff88" font-size="9" font-family="monospace">OA 3.1</text>
          <!-- Data polygon -->
          <polygon id="diana-polygon" points="160,125 185,160 160,195 135,160" fill="rgba(0,212,255,0.2)" stroke="var(--cyan)" stroke-width="2"/>
          <!-- Center -->
          <circle cx="160" cy="160" r="4" fill="var(--cyan)"/>
        </svg>
      </div>
    </div>
  </div>
</div>

<!-- =================== RETO FINAL =================== -->
<div class="section" id="section-final">

  <div class="final-mission">
    <div class="final-icon">🔴</div>
    <div class="final-title">CONFRONTACIÓN CON VECNA</div>
    <div class="final-desc">
      El momento ha llegado, Guardianes. Habéis entrenado, habéis aprendido, habéis fallado y os habéis levantado. Ahora VECNA espera en el Mundo al Revés. Solo un podcast guardián completo, lleno de verdad y de corazón, puede detenerle definitivamente. <strong>¿Estáis preparados?</strong>
    </div>

    <div style="font-family:'Share Tech Mono',monospace; font-size:13px; color:var(--red-glow); margin-bottom:10px">
      ⚠️ NECESITÁIS COMPLETAR TODOS LOS REQUISITOS PARA ACCEDER AL RETO FINAL
    </div>

    <div class="progress-gate">
      <div class="gate-title">🔒 REQUISITOS DE ACCESO AL RETO FINAL</div>
      <div class="gate-item" id="gate1"><span class="gate-icon">🔲</span> Al menos 4 sesiones completadas</div>
      <div class="gate-item" id="gate2"><span class="gate-icon">🔲</span> Al menos 3 retos superados</div>
      <div class="gate-item" id="gate3"><span class="gate-icon">🔲</span> Al menos 2 reflexiones guardadas</div>
      <div class="gate-item" id="gate4"><span class="gate-icon">🔲</span> KPSI inicial completado</div>
      <div class="gate-item" id="gate5"><span class="gate-icon">🔲</span> Al menos 4 Guardianes desbloqueados</div>
      <div class="gate-item" id="gate6"><span class="gate-icon">🔲</span> Al menos 200 XP acumulados</div>
    </div>
  </div>

  <div class="panel">
    <div class="panel-title"><span class="icon">🎙️</span> EL PODCAST GUARDIÁN — ESTRUCTURA FINAL</div>
    <p style="font-size:13px; color:var(--text-dim); line-height:1.7; margin-bottom:20px">El Podcast Guardián es vuestro arma definitiva. Se difundirá al alumnado del primer ciclo para inspirarles. Debe contener los 4 episodios grabados a lo largo de la UD.</p>

    <div style="display:grid; gap:12px">
      <div style="display:flex; align-items:center; gap:15px; padding:15px; background:rgba(255,255,255,0.03); border-radius:8px; border:1px solid rgba(0,212,255,0.2)">
        <div style="font-size:32px">🎙️</div>
        <div>
          <div style="font-family:'Orbitron',sans-serif; font-size:11px; color:var(--cyan); margin-bottom:4px">EPISODIO 1 · SESIÓN 1</div>
          <div style="font-size:13px; font-weight:700; margin-bottom:4px">¿Qué es estar en forma de verdad?</div>
          <div style="font-size:12px; color:var(--text-dim)">Al menos 3 beneficios del ejercicio para la salud</div>
        </div>
        <input type="checkbox" class="reto-checkbox" id="pod1" style="margin-left:auto; flex-shrink:0" onchange="updateGates()">
      </div>
      <div style="display:flex; align-items:center; gap:15px; padding:15px; background:rgba(255,255,255,0.03); border-radius:8px; border:1px solid rgba(0,212,255,0.2)">
        <div style="font-size:32px">💪</div>
        <div>
          <div style="font-family:'Orbitron',sans-serif; font-size:11px; color:var(--cyan); margin-bottom:4px">EPISODIO 2 · SESIÓN 2</div>
          <div style="font-size:13px; font-weight:700; margin-bottom:4px">Fuerza, flexibilidad y lo que siente el cuerpo</div>
          <div style="font-size:12px; color:var(--text-dim)">Mitos y realidades del ejercicio</div>
        </div>
        <input type="checkbox" class="reto-checkbox" id="pod2" style="margin-left:auto; flex-shrink:0" onchange="updateGates()">
      </div>
      <div style="display:flex; align-items:center; gap:15px; padding:15px; background:rgba(255,255,255,0.03); border-radius:8px; border:1px solid rgba(0,212,255,0.2)">
        <div style="font-size:32px">😤</div>
        <div>
          <div style="font-family:'Orbitron',sans-serif; font-size:11px; color:var(--cyan); margin-bottom:4px">EPISODIO 3 · SESIÓN 4</div>
          <div style="font-size:13px; font-weight:700; margin-bottom:4px">Los errores también enseñan</div>
          <div style="font-size:12px; color:var(--text-dim)">3 emociones surgidas y cómo las gestionamos</div>
        </div>
        <input type="checkbox" class="reto-checkbox" id="pod3" style="margin-left:auto; flex-shrink:0" onchange="updateGates()">
      </div>
      <div style="display:flex; align-items:center; gap:15px; padding:15px; background:rgba(255,255,255,0.03); border-radius:8px; border:1px solid rgba(0,212,255,0.2)">
        <div style="font-size:32px">🛡️</div>
        <div>
          <div style="font-family:'Orbitron',sans-serif; font-size:11px; color:var(--cyan); margin-bottom:4px">EPISODIO 4 · SESIÓN 5</div>
          <div style="font-size:13px; font-weight:700; margin-bottom:4px">Nuestra vacuna contra el conflicto</div>
          <div style="font-size:12px; color:var(--text-dim)">Estrategia de resolución de conflictos</div>
        </div>
        <input type="checkbox" class="reto-checkbox" id="pod4" style="margin-left:auto; flex-shrink:0" onchange="updateGates()">
      </div>
    </div>
  </div>

  <div class="panel">
    <div class="panel-title"><span class="icon">🏆</span> RECOMPENSA FINAL</div>
    <div style="text-align:center; padding:10px">
      <div class="flip-badge-wrap" id="flip-final" onclick="this.classList.toggle('flipped')" title="¡Toca para ver el superpoder!" style="margin:0 auto 15px">
        <div class="flip-badge-inner">
          <div class="flip-front">🔥</div>
          <div class="flip-back">
            <div class="flip-back-title">⚡ SUPERPODER</div>
            <div class="flip-back-power">"Tu motor nunca se apaga. La determinación es tu escudo."</div>
          </div>
        </div>
      </div>
      <div style="font-family:'Creepster',cursive; font-size:24px; color:var(--red-glow); text-shadow:var(--glow-red); margin-bottom:8px">INSIGNIA HOPPER DESBLOQUEADA</div>
      <div style="font-size:13px; color:var(--text-dim); margin-bottom:15px">"Tu motor nunca se apaga"</div>
      <div style="font-size:12px; color:var(--text-dim); line-height:1.7">
        Al completar la UD, la clase recibe la <strong>Insignia Hopper</strong> en el mapa del Mundo al Revés del gimnasio.<br>
        VECNA pierde un fragmento de su poder. <strong>La siguiente batalla se acerca...</strong>
      </div>
    </div>
  </div>

</div>


<!-- MAPA -->
<div class="section" id="section-mapa" style="display:none!important">
  <div class="panel" style="text-align:center;margin-bottom:14px">
    <div class="panel-title" style="justify-content:center"><span class="icon">🗺️</span> MAPA DEL MUNDO AL REVÉS</div>
    <p style="font-size:12px;color:var(--text-dim)">Cada sesión completada ilumina una zona. Derrota a VECNA en 8 sesiones.</p>
  </div>
  <div style="max-width:700px;margin:0 auto">
    <svg viewBox="0 0 700 420" xmlns="http://www.w3.org/2000/svg" style="width:100%;border-radius:12px;border:1px solid var(--border)">
      <rect width="700" height="420" fill="#05020a"/>
      <g stroke="rgba(80,0,120,0.1)" stroke-width="1">
        <line x1="0" y1="84" x2="700" y2="84"/><line x1="0" y1="168" x2="700" y2="168"/><line x1="0" y1="252" x2="700" y2="252"/><line x1="0" y1="336" x2="700" y2="336"/>
        <line x1="140" y1="0" x2="140" y2="420"/><line x1="280" y1="0" x2="280" y2="420"/><line x1="420" y1="0" x2="420" y2="420"/><line x1="560" y1="0" x2="560" y2="420"/>
      </g>
      <path d="M0,420 Q90,370 180,350 Q300,330 400,390 Q500,420 620,360 L700,370 L700,420Z" fill="rgba(0,40,0,0.4)"/>
      <ellipse id="mz1" cx="90"  cy="325" rx="70" ry="50" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz2" cx="210" cy="185" rx="75" ry="56" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz3" cx="345" cy="315" rx="66" ry="48" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz4" cx="465" cy="145" rx="80" ry="60" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz5" cx="595" cy="270" rx="70" ry="52" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz6" cx="160" cy="78"  rx="75" ry="46" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <ellipse id="mz7" cx="555" cy="72"  rx="92" ry="50" fill="rgba(20,0,40,0.7)" stroke="rgba(80,0,120,0.4)" stroke-width="1.5" style="transition:all 0.8s"/>
      <text id="mzt1" x="90"  y="329" text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S1</text>
      <text id="mzt2" x="210" y="189" text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S2</text>
      <text id="mzt3" x="345" y="319" text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S3</text>
      <text id="mzt4" x="465" y="149" text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S4</text>
      <text id="mzt5" x="595" y="274" text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S5</text>
      <text id="mzt6" x="160" y="82"  text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S6</text>
      <text id="mzt7" x="555" y="76"  text-anchor="middle" fill="rgba(180,100,255,0.5)" font-size="10" font-family="monospace">S7</text>
      <ellipse cx="350" cy="210" rx="46" ry="36" fill="rgba(120,0,0,0.5)" stroke="rgba(231,76,60,0.7)" stroke-width="2" stroke-dasharray="5,3"/>
      <text x="350" y="205" text-anchor="middle" font-size="20">&#128128;</text>
      <text x="350" y="222" text-anchor="middle" fill="rgba(231,76,60,0.8)" font-size="9" font-family="monospace">VECNA</text>
    </svg>
  </div>
  <div id="mapa-leyenda" style="display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:7px;margin-top:12px;max-width:700px;margin-left:auto;margin-right:auto"></div>
</div>

<!-- PODCAST -->
<div class="section" id="section-podcast">
  <div class="panel" style="margin-bottom:14px">
    <div class="panel-title"><span class="icon">🎙️</span> ESTUDIO DE GRABACIÓN GUARDIÁN</div>
    <p style="font-size:12px;color:var(--text-dim);line-height:1.6">Grabad los episodios directamente. Requiere <strong style="color:var(--yellow)">HTTPS</strong> para el micrófono — sube el archivo a <a href="https://app.netlify.com/drop" target="_blank" style="color:var(--cyan)">Netlify Drop</a>.</p>
  </div>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:8px;margin-bottom:16px">
    <div id="epbtn1" onclick="selectEp(1,this)" style="background:rgba(192,57,43,0.15);border:2px solid var(--red-glow);border-radius:8px;padding:10px;text-align:center;cursor:pointer"><div style="font-size:18px;margin-bottom:3px">🎙️</div><div style="font-family:'Orbitron',sans-serif;font-size:8px;color:var(--red-glow)">EP. 1</div><div style="font-size:9px;color:var(--text-dim);margin-top:2px">Estar en forma</div></div>
    <div id="epbtn2" onclick="selectEp(2,this)" style="background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:8px;padding:10px;text-align:center;cursor:pointer"><div style="font-size:18px;margin-bottom:3px">💪</div><div style="font-family:'Orbitron',sans-serif;font-size:8px;color:var(--cyan)">EP. 2</div><div style="font-size:9px;color:var(--text-dim);margin-top:2px">Fuerza y flexibilidad</div></div>
    <div id="epbtn3" onclick="selectEp(3,this)" style="background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:8px;padding:10px;text-align:center;cursor:pointer"><div style="font-size:18px;margin-bottom:3px">😤</div><div style="font-family:'Orbitron',sans-serif;font-size:8px;color:var(--cyan)">EP. 3</div><div style="font-size:9px;color:var(--text-dim);margin-top:2px">Los errores enseñan</div></div>
    <div id="epbtn4" onclick="selectEp(4,this)" style="background:rgba(255,255,255,0.03);border:2px solid var(--border);border-radius:8px;padding:10px;text-align:center;cursor:pointer"><div style="font-size:18px;margin-bottom:3px">🛡️</div><div style="font-family:'Orbitron',sans-serif;font-size:8px;color:var(--cyan)">EP. 4</div><div style="font-size:9px;color:var(--text-dim);margin-top:2px">Vacuna al conflicto</div></div>
  </div>
  <div style="background:var(--panel2);border:1px solid var(--border);border-radius:12px;padding:22px;text-align:center;max-width:480px;margin:0 auto">
    <div id="rec-ep-title" style="font-family:'Orbitron',sans-serif;font-size:10px;color:var(--red-glow);margin-bottom:14px;letter-spacing:1px">EP. 1 SELECCIONADO</div>
    <canvas id="rec-canvas" width="420" height="52" style="width:100%;border-radius:6px;background:rgba(0,0,0,0.4);margin-bottom:12px;display:block"></canvas>
    <div id="rec-timer" style="font-family:'Share Tech Mono',monospace;font-size:38px;color:var(--text);margin-bottom:16px;letter-spacing:4px">00:00</div>
    <div style="display:flex;gap:10px;justify-content:center;margin-bottom:14px">
      <button id="btn-rec" onclick="toggleRecord()" style="padding:12px 26px;background:linear-gradient(135deg,var(--red-dark),var(--red-glow));border:none;border-radius:8px;color:white;font-family:'Orbitron',sans-serif;font-size:11px;font-weight:700;cursor:pointer;letter-spacing:1px">🔴 GRABAR</button>
      <button id="btn-stop" onclick="stopRecord()" disabled style="padding:12px 26px;background:rgba(255,255,255,0.04);border:1px solid var(--border);border-radius:8px;color:var(--text-dim);font-family:'Orbitron',sans-serif;font-size:11px;cursor:not-allowed;letter-spacing:1px">⏹ PARAR</button>
    </div>
    <div id="rec-list" style="text-align:left"></div>
  </div>
</div>

<!-- IA -->
<div class="section" id="section-ia">
  <div class="panel" style="margin-bottom:14px">
    <div class="panel-title"><span class="icon">🤖</span> LABORATORIO HAWKINS — IA GUARDIANA</div>
    <p style="font-size:12px;color:var(--text-dim);line-height:1.6">Pregunta cualquier duda sobre salud, ejercicio o emociones. Responde en clave Stranger Things. Funciona sin conexión también.</p>
  </div>
  <div id="ia-chat" style="background:var(--panel2);border:1px solid var(--border);border-radius:12px;padding:14px;min-height:260px;max-height:380px;overflow-y:auto;margin-bottom:12px">
    <div style="display:flex;gap:9px;align-items:flex-start;margin-bottom:10px">
      <div style="font-size:20px;flex-shrink:0">🔬</div>
      <div style="background:rgba(0,212,255,0.07);border:1px solid rgba(0,212,255,0.2);border-radius:0 8px 8px 8px;padding:10px 13px;font-size:12px;color:var(--text);line-height:1.6;max-width:82%">
        Guardianes... el Laboratorio Hawkins esta en linea. Podeis preguntarme sobre frecuencia cardiaca, mitos del ejercicio, emociones o habitos saludables. <strong>Que necesita saber el grupo?</strong>
      </div>
    </div>
  </div>
  <div style="display:flex;gap:8px">
    <input id="ia-input" type="text" placeholder="Escribe tu pregunta al Laboratorio..." onkeydown="if(event.key==='Enter')sendIA()" style="flex:1;background:rgba(255,255,255,0.04);border:1px solid var(--border);border-radius:8px;padding:11px;color:var(--text);font-family:'Nunito',sans-serif;font-size:13px;outline:none">
    <button onclick="sendIA()" style="padding:11px 18px;background:linear-gradient(135deg,#001a3a,var(--blue));border:1px solid var(--cyan);border-radius:8px;color:var(--cyan);font-family:'Orbitron',sans-serif;font-size:10px;font-weight:700;cursor:pointer;white-space:nowrap;letter-spacing:1px">ENVIAR</button>
  </div>
  <div style="font-size:10px;color:var(--text-dim);margin-top:7px;font-family:'Share Tech Mono',monospace">IA generativa — Contrasta siempre con tu profe Guardian</div>
</div>

<!-- EXHIBICION -->
<div class="section" id="section-exhibicion">
  <div class="panel" style="text-align:center">
    <div class="panel-title" style="justify-content:center"><span class="icon">📺</span> MODO EXHIBICION — PANTALLA DE CLASE</div>
    <p style="font-size:13px;color:var(--text-dim);margin-bottom:20px;line-height:1.7">Proyecta en pantalla completa: VECNA, fuerza, XP, sesiones y Guardianes desbloqueados.</p>
    <button onclick="abrirExhibicion()" style="padding:15px 38px;background:linear-gradient(135deg,#2a1500,var(--yellow));border:none;border-radius:10px;color:#000;font-family:'Orbitron',sans-serif;font-size:13px;font-weight:900;cursor:pointer;letter-spacing:2px;box-shadow:0 0 28px rgba(243,156,18,0.4)">PANTALLA COMPLETA</button>
    <div style="margin-top:22px;padding-top:18px;border-top:1px solid var(--border)">
      <div style="font-family:'Orbitron',sans-serif;font-size:10px;color:var(--cyan);letter-spacing:2px;margin-bottom:10px">CODIGO QR</div>
      <p style="font-size:12px;color:var(--text-dim);margin-bottom:12px">Genera un QR para que el alumnado acceda desde su movil.</p>
      <input id="qr-url" type="text" placeholder="Pega aqui la URL de la herramienta..." style="width:100%;max-width:400px;background:rgba(255,255,255,0.04);border:1px solid var(--border);border-radius:6px;padding:9px;color:var(--text);font-size:12px;outline:none;display:block;margin:0 auto 10px">
      <button onclick="generarQR()" style="padding:9px 22px;background:transparent;border:1px solid var(--cyan);border-radius:6px;color:var(--cyan);font-family:'Orbitron',sans-serif;font-size:10px;cursor:pointer;letter-spacing:1px">GENERAR QR</button>
      <div id="qr-output" style="margin-top:14px"></div>
    </div>
  </div>
</div>
</div><!-- /main -->

<script>
// =================== STATE ===================
let state = {
  vecnaHP: 100,
  fuerza: 0,
  xp: 0,
  sessions: [false,false,false,false,false,false,false],
  retosCompleted: 0,
  reflections: [],
  chars: { once:false, dustin:false, max:false, lucas:false, will:false },
  stars: {},
  kpsi: {},
  avatarChar: 'hopper',
  avatarName: ''
};

// Load from localStorage
try { const s = localStorage.getItem('ud4_state'); if(s) state = {...state,...JSON.parse(s)}; } catch(e){}

function save() {
  try { localStorage.setItem('ud4_state', JSON.stringify(state)); } catch(e){}
}

// =================== INIT ===================
window.onload = function() {
  updateVecnaBar();
  updateFuerzaBar();
  updateXPBar();
  updateStats();
  renderReflections();
  restoreStars();
  restoreKPSI();
  updateGates();
  updateSessionProgUI();
  updateCharUnlocks();
  restoreAvatar();
};

// =================== TABS ===================
function showSection(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('section-'+id).classList.add('active');
  if(btn) btn.classList.add('active');
  updateGates();
  if(id === 'personajes') updateCharUnlocks();
}

// =================== HP ===================
function changeHP(who, delta) {
  if(who === 'vecna') {
    state.vecnaHP = Math.max(0, Math.min(100, state.vecnaHP + delta));
    updateVecnaBar();
    if(state.vecnaHP <= 0) showToast('🔥 ¡¡VECNA DERROTADO!! ¡GUARDIANES ÉLITE!');
  } else if(who === 'fuerza') {
    state.fuerza = Math.max(0, Math.min(100, state.fuerza + delta));
    updateFuerzaBar();
  }
  save();
  if(who === 'vecna') showToast(delta < 0 ? '⚔️ ¡VECNA debilitado!' : '☠️ VECNA se fortalece');
}

function updateVecnaBar() {
  const pct = state.vecnaHP;
  document.getElementById('vecna-bar').style.width = pct + '%';
  document.getElementById('vecna-value').textContent = pct + ' / 100';
}

function updateFuerzaBar() {
  const pct = Math.min(100, state.fuerza || 0);
  const bar = document.getElementById('fuerza-bar');
  const val = document.getElementById('fuerza-value');
  if(bar) bar.style.width = pct + '%';
  if(val) val.textContent = pct + ' / 100';
}

// =================== AVATAR ===================
const avatarData = {
  hopper: { emoji:'💀', color:'#e74c3c', power:'Determinación — "Nunca te rindes, siempre hay un camino"' },
  once:   { emoji:'🌪️', color:'#3498db', power:'Telekinesia — "Puedes mover los obstáculos con tu mente"' },
  dustin: { emoji:'⚙️', color:'#f39c12', power:'Ingenio — "Encuentra la solución donde nadie más la ve"' },
  max:    { emoji:'🎶', color:'#8e44ad', power:'Resiliencia — "Siempre puedes levantarte, el error no te define"' },
  lucas:  { emoji:'🧭', color:'#00ff88', power:'Liderazgo — "Siempre sabes quién necesita ayuda y cómo dársela"' },
  will:   { emoji:'🔥', color:'#e74c3c', power:'Empatía — "Sientes lo que el grupo necesita antes de que lo digan"' },
  mike:   { emoji:'📻', color:'#00d4ff', power:'Estrategia — "Tu mente es tu mayor arma contra el Mundo al Revés"' },
  steve:  { emoji:'🦸', color:'#f39c12', power:'Valentía — "Siempre da la cara por el grupo, pase lo que pase"' }
};

function selectAvatar(char) {
  state.avatarChar = char;
  save();
  renderAvatar();
  // Highlight selected
  document.querySelectorAll('.av-opt').forEach(el => {
    const isSelected = el.dataset.char === char;
    el.style.borderColor = isSelected ? (avatarData[char]?.color || 'var(--green)') : 'var(--border)';
    el.style.background = isSelected ? `rgba(0,255,136,0.1)` : 'var(--panel2)';
  });
  showToast('⚡ Avatar: ' + char.toUpperCase() + ' seleccionado');
}

function updateAvatarName(val) {
  state.avatarName = val;
  save();
  const nd = document.getElementById('avatar-name-display');
  if(nd) nd.textContent = val.trim() ? val.trim().toUpperCase() : 'NOMBRE DEL GRUPO';
}

function renderAvatar() {
  const char = state.avatarChar || 'hopper';
  const data = avatarData[char] || avatarData.hopper;
  const disp = document.getElementById('avatar-display');
  const pow = document.getElementById('avatar-power-display');
  const nd = document.getElementById('avatar-name-display');
  if(disp) { disp.textContent = data.emoji; disp.style.borderColor = data.color; disp.style.color = data.color; }
  if(pow) pow.textContent = data.power;
  if(nd) nd.textContent = (state.avatarName || '').trim().toUpperCase() || 'NOMBRE DEL GRUPO';
}

function restoreAvatar() {
  renderAvatar();
  const ni = document.getElementById('avatar-name-input');
  if(ni) ni.value = state.avatarName || '';
  // Restore selection highlight
  const char = state.avatarChar || 'hopper';
  document.querySelectorAll('.av-opt').forEach(el => {
    const isSelected = el.dataset.char === char;
    el.style.borderColor = isSelected ? (avatarData[char]?.color || 'var(--green)') : 'var(--border)';
    el.style.background = isSelected ? 'rgba(0,255,136,0.1)' : 'var(--panel2)';
  });
}

// =================== XP ===================
function addXP(amount) {
  state.xp = Math.min(500, state.xp + amount);
  updateXPBar();
  updateStats();
  save();
  showToast('⚡ +' + amount + ' XP GUARDIANO');
}

function updateXPBar() {
  const pct = (state.xp / 500) * 100;
  document.getElementById('xp-bar').style.width = pct + '%';
  document.getElementById('xp-display').textContent = state.xp + ' / 500 XP';
  document.getElementById('stat-xp').textContent = state.xp;
}

// =================== STATS ===================
function updateStats() {
  const sessComp = state.sessions.filter(Boolean).length;
  document.getElementById('stat-retos').textContent = state.retosCompleted || 0;
  const charCount = [state.chars.once,state.chars.dustin,state.chars.max,state.chars.lucas,state.chars.will].filter(Boolean).length + 1;
  document.getElementById('stat-chars').textContent = charCount;
}

// =================== SESSIONS ===================
function toggleSessionProg(n) {
  state.sessions[n-1] = !state.sessions[n-1];
  updateSessionProgUI();
  updateCharUnlocks();
  // Progressive VECNA damage: S1=8,S2=10,S3=12,S4=14,S5=16,S6=18,S7=22 → total 100
  const sessionDmg = [4,4,4,4,4,4,4];
  if(state.sessions[n-1]) {
    addXP(20);
    changeHP('vecna', -sessionDmg[n-1]);
    state.fuerza = Math.min(100, (state.fuerza||0) + 10);
    updateFuerzaBar();
    save();
    if(state.vecnaHP <= 0) showToast('🔥 ¡¡VECNA HA SIDO DERROTADO!! ¡GUARDIANES ÉLITE!');
  } else {
    changeHP('vecna', +sessionDmg[n-1]);
    state.fuerza = Math.max(0, (state.fuerza||0) - 10);
    updateFuerzaBar();
    save();
  }
  updateGates();
  save();
}

function updateSessionProgUI() {
  const icons = ['🎙️','💪','🏃','😤','🛡️','🎵','🏆'];
  for(let i=1; i<=7; i++) {
    const el = document.getElementById('prog-s'+i);
    if(el) {
      if(state.sessions[i-1]) {
        el.style.borderColor = 'var(--green)';
        el.style.background = 'rgba(0,255,136,0.1)';
        el.innerHTML = `<div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--green)">S${i}</div><div style="font-size:18px">✅</div>`;
      } else {
        el.style.borderColor = 'var(--border)';
        el.style.background = 'var(--panel2)';
        el.innerHTML = `<div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--text-dim)">S${i}</div><div style="font-size:18px">${icons[i-1]}</div>`;
      }
    }
  }
}

// =================== CHAR UNLOCKS ===================
function updateCharUnlocks() {
  var s = state.sessions;
  var unlocks = [
    { key: 'once',   session: 1, label: 'DESBLOQUEADO S2' },
    { key: 'dustin', session: 2, label: 'DESBLOQUEADO S3' },
    { key: 'max',    session: 3, label: 'DESBLOQUEADO S4' },
    { key: 'lucas',  session: 4, label: 'DESBLOQUEADO S5' },
    { key: 'will',   session: 5, label: 'DESBLOQUEADO S6' }
  ];
  unlocks.forEach(function(u) {
    if (s[u.session]) unlockChar(u.key, u.label);
  });
  updateStats();
}

function unlockChar(name, label) {
  state.chars[name] = true;
  var card = document.getElementById('char-'+name);
  var tag = document.getElementById(name+'-tag');
  if (card) {
    // Remove locked class and set unlocked directly via style attribute
    card.className = 'char-card unlocked';
    card.style.filter = 'none';
    card.style.webkitFilter = 'none';
    card.style.opacity = '1';
    card.style.borderColor = 'rgba(0,212,255,0.3)';
    card.style.boxShadow = '0 0 20px rgba(0,212,255,0.1)';
  }
  if (tag) {
    tag.innerHTML = '✅ ' + label;
    tag.style.cssText = 'display:inline-block;padding:3px 10px;border-radius:20px;font-family:Orbitron,sans-serif;font-size:8px;font-weight:700;letter-spacing:1px;margin-top:8px;background:rgba(0,255,136,0.15);color:#00ff88;border:1px solid #00ff88';
  }
  var sessEl = card ? card.querySelector('.char-card-session') : null;
  if (sessEl) { sessEl.textContent = '✅ ' + label; sessEl.style.color = '#00ff88'; }
}

// =================== RETOS ===================
function onRetoCheck(el, xpAmount) {
  var dmg = xpAmount >= 50 ? 4 : xpAmount >= 35 ? 3 : 2;
  if(el.checked) {
    state.retosCompleted = (state.retosCompleted || 0) + 1;
    addXP(xpAmount);
    changeHP('vecna', -dmg);
    state.fuerza = Math.min(100, (state.fuerza||0) + Math.round(100/34));
    updateFuerzaBar();
    // Auto-detect which session this reto belongs to and mark it complete
    var retoId = el.id || '';
    var sessMatch = retoId.match(/^s(\d+)r/);
    if(sessMatch) {
      var sessNum = parseInt(sessMatch[1]);
      if(!state.sessions[sessNum-1]) {
        state.sessions[sessNum-1] = true;
        updateSessionProgUI();
        updateCharUnlocks();
        showToast('⚔️ +' + xpAmount + ' XP · S' + sessNum + ' completada!');
      } else {
        showToast('⚔️ +' + xpAmount + ' XP · VECNA -' + dmg + ' HP');
      }
    } else {
      showToast('⚔️ +' + xpAmount + ' XP · VECNA -' + dmg + ' HP');
    }
    save();
  } else {
    state.retosCompleted = Math.max(0, (state.retosCompleted || 0) - 1);
    changeHP('vecna', dmg);
    state.fuerza = Math.max(0, (state.fuerza||0) - Math.round(100/34));
    updateFuerzaBar();
    save();
  }
  updateStats();
  updateGates();
  save();
}

// =================== REFLEXIONES ===================
let currentRefSession = 'Sesión 1';

function selectRefSession(btn, sess) {
  document.querySelectorAll('.ref-sess-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  currentRefSession = sess;
}

function insertPrompt(el) {
  const ta = document.getElementById('ref-input');
  ta.value = (ta.value ? ta.value + '\n\n' : '') + el.textContent + '\n';
  ta.focus();
}

function saveReflection() {
  const text = document.getElementById('ref-input').value.trim();
  if(!text) { showToast('⚠️ Escribe algo primero...'); return; }
  const entry = {
    id: Date.now(),
    session: currentRefSession,
    text: text,
    date: new Date().toLocaleDateString('es-ES')
  };
  if(!state.reflections) state.reflections = [];
  state.reflections.unshift(entry);
  save();
  document.getElementById('ref-input').value = '';
  renderReflections();
  addXP(30);
  changeHP('vecna', -5);
  state.fuerza = Math.min(100, (state.fuerza||0) + 8);
  updateFuerzaBar();
  save();
  showToast('📓 ¡Reflexión guardada en el Diario Guardián!');
  updateGates();
}

function clearReflection() {
  document.getElementById('ref-input').value = '';
}

function deleteReflection(id) {
  state.reflections = state.reflections.filter(r => r.id !== id);
  save();
  renderReflections();
  updateGates();
}

function renderReflections() {
  const list = document.getElementById('reflections-list');
  if(!state.reflections || state.reflections.length === 0) {
    list.innerHTML = '<div style="font-size:12px; color:var(--text-dim); text-align:center; padding:20px">Aún no hay reflexiones guardadas. ¡Escribe la primera entrada de tu Diario Guardián!</div>';
    return;
  }
  list.innerHTML = state.reflections.map(r => `
    <div class="reflection-entry">
      <div class="ref-entry-header">
        <span class="ref-entry-session">📡 ${r.session}</span>
        <span class="ref-entry-date">${r.date}</span>
      </div>
      <div class="ref-entry-text">${r.text.replace(/\n/g,'<br>')}</div>
      <button class="ref-delete" onclick="deleteReflection(${r.id})">🗑️</button>
    </div>
  `).join('');
}

// =================== AUTOEVALUACIÓN ===================
const starLabels = ['','🔴 Necesito mejorar','🟡 En progreso','🔵 Lo tengo','🌟 Guardián Élite'];

function setStar(oa, val) {
  state.stars[oa] = val;
  const container = document.getElementById('stars-'+oa);
  const label = document.getElementById('label-'+oa);
  if(container) {
    container.querySelectorAll('.star-btn').forEach((b,i) => {
      b.classList.toggle('active', i < val);
    });
  }
  if(label) label.textContent = starLabels[val];
  updateDiana();
  save();
}

function restoreStars() {
  if(state.stars) {
    Object.entries(state.stars).forEach(([oa,val]) => setStar(oa, val));
  }
}

function saveAutoeval() {
  save();
  showToast('⭐ Autoevaluación guardada');
}

function updateDiana() {
  const vals = {
    oa11: state.stars.oa11 || 0,
    oa13: state.stars.oa13 || 0,
    oa21: state.stars.oa21 || 0,
    oa31: state.stars.oa31 || 0
  };
  // Map 0-4 to 0-140 radius max 140, center 160
  const r = (v) => (v/4) * 120;
  const cx = 160, cy = 160;
  // Top: oa11, Right: oa13, Bottom: oa21, Left: oa31
  const pts = [
    [cx, cy - r(vals.oa11)],      // top
    [cx + r(vals.oa13), cy],      // right
    [cx, cy + r(vals.oa21)],      // bottom
    [cx - r(vals.oa31), cy]       // left
  ];
  const poly = document.getElementById('diana-polygon');
  if(poly) poly.setAttribute('points', pts.map(p=>p.join(',')).join(' '));
}

// =================== KPSI ===================
function saveKPSI(key, val) {
  state.kpsi[key] = val;
  save();
  // check if initial fields filled for gate
  const initKeys = ['k1i','k2i','k3i','k4i','k5i','k6i','k7i','k8i','k9i'];
  const filled = initKeys.filter(k => state.kpsi[k] && state.kpsi[k] !== '').length;
  if(state.kpsi && filled >= 4) { state.kpsiDone = true; save(); }
}

function saveKPSIFull() {
  save();
  showToast('📊 KPSI guardado correctamente');
  const initKeys = ['k1i','k2i','k3i','k4i','k5i','k6i','k7i','k8i','k9i'];
  const filled = initKeys.filter(k => state.kpsi[k] && state.kpsi[k] !== '').length;
  const finalKeys = ['k1f','k2f','k3f','k4f','k5f','k6f','k7f','k8f','k9f'];
  const filledF = finalKeys.filter(k => state.kpsi[k] && state.kpsi[k] !== '').length;
  const res = document.getElementById('kpsi-result');
  if(res) {
    if(filledF > 0) {
      res.innerHTML = `✅ Inicio: ${filled}/9 · Final: ${filledF}/9 completados`;
      res.style.color = 'var(--green)';
    } else {
      res.innerHTML = `✅ Inicio: ${filled}/9 ítems completados`;
      res.style.color = 'var(--cyan)';
    }
  }
  if(filled >= 4) { state.kpsiDone = true; save(); updateGates(); }
}

function updateKPSIArrow() {}

function restoreKPSI() {
  if(!state.kpsi) return;
  // For new structured KPSI selects using onchange attributes
  document.querySelectorAll('[onchange*="saveKPSI"]').forEach(el => {
    const match = el.getAttribute('onchange').match(/saveKPSI\('([^']+)'/);
    if(match && state.kpsi[match[1]]) {
      el.value = state.kpsi[match[1]];
    }
  });
}

// =================== SESSION PANEL TOGGLE ===================
function togglePanel(id, event) {
  if(event && event.target.closest('input, select, label')) return;
  const panel = document.getElementById(id+'-panel');
  const arrow = document.getElementById(id+'-arrow');
  if(!panel) return;
  const isOpen = panel.style.display !== 'none';
  panel.style.display = isOpen ? 'none' : 'block';
  if(arrow) arrow.textContent = isOpen ? '▼ VER DETALLE' : '▲ OCULTAR';
}
function toggleS2Panel(event) { togglePanel('s2', event); }

// =================== GATES ===================
function updateGates() {
  const sessComp = state.sessions ? state.sessions.filter(Boolean).length : 0;
  const retosComp = state.retosCompleted || 0;
  const refCount = state.reflections ? state.reflections.length : 0;
  const kpsiDone = state.kpsiDone || (state.kpsi && Object.keys(state.kpsi).filter(k => k.endsWith('i') && state.kpsi[k]).length >= 4);
  const charCount = [state.chars.once,state.chars.dustin,state.chars.max,state.chars.lucas,state.chars.will].filter(Boolean).length + 1;
  const xp = state.xp || 0;

  const checks = [
    { id:'gate1', met: sessComp >= 4, text: `Al menos 4 sesiones completadas (${sessComp}/4)` },
    { id:'gate2', met: retosComp >= 3, text: `Al menos 3 retos superados (${retosComp}/3)` },
    { id:'gate3', met: refCount >= 2, text: `Al menos 2 reflexiones guardadas (${refCount}/2)` },
    { id:'gate4', met: kpsiDone, text: 'KPSI inicial completado' },
    { id:'gate5', met: charCount >= 4, text: `Al menos 4 Guardianes desbloqueados (${charCount}/6)` },
    { id:'gate6', met: xp >= 200, text: `Al menos 200 XP acumulados (${xp}/200)` },
  ];

  checks.forEach(c => {
    const el = document.getElementById(c.id);
    if(!el) return;
    el.className = 'gate-item' + (c.met ? ' met' : '');
    el.innerHTML = `<span class="gate-icon">${c.met ? '✅' : '🔲'}</span> ${c.text}`;
  });
}

// =================== RESET ===================
function resetAll() {
  // Custom confirm since confirm() is blocked in iframes
  const overlay = document.createElement('div');
  overlay.style.cssText = 'position:fixed;inset:0;background:rgba(0,0,0,0.8);z-index:99999;display:flex;align-items:center;justify-content:center';
  overlay.innerHTML = `
    <div style="background:#12121f;border:1px solid #c0392b;border-radius:12px;padding:28px 32px;max-width:340px;text-align:center;box-shadow:0 0 40px rgba(192,57,43,0.4)">
      <div style="font-size:32px;margin-bottom:12px">⚠️</div>
      <div style="font-family:'Orbitron',sans-serif;font-size:13px;font-weight:700;color:#e74c3c;margin-bottom:10px">¿REINICIAR TODO?</div>
      <div style="font-size:12px;color:#8888aa;margin-bottom:22px;line-height:1.5">Se perderán todas las sesiones, XP, reflexiones y progreso. Esta acción no se puede deshacer.</div>
      <div style="display:flex;gap:12px;justify-content:center">
        <button id="reset-cancel" style="padding:9px 20px;background:transparent;border:1px solid #2a2a4a;border-radius:6px;color:#8888aa;font-family:'Orbitron',sans-serif;font-size:10px;cursor:pointer">CANCELAR</button>
        <button id="reset-confirm" style="padding:9px 20px;background:linear-gradient(135deg,#7b241c,#c0392b);border:none;border-radius:6px;color:white;font-family:'Orbitron',sans-serif;font-size:10px;font-weight:700;cursor:pointer">SÍ, REINICIAR</button>
      </div>
    </div>`;
  document.body.appendChild(overlay);
  document.getElementById('reset-cancel').onclick = () => overlay.remove();
  document.getElementById('reset-confirm').onclick = () => {
    overlay.remove();
    doReset();
  };
}

function doReset() {
  state = {
    vecnaHP: 100,
    fuerza: 0,
    xp: 0,
    sessions: [false,false,false,false,false,false,false],
    retosCompleted: 0,
    reflections: [],
    chars: { once:false, dustin:false, max:false, lucas:false, will:false },
    stars: {},
    kpsi: {},
    avatarChar: 'hopper',
    avatarName: ''
  };
  save();
  document.querySelectorAll('input[type=checkbox]').forEach(el => el.checked = false);
  document.querySelectorAll('.kpsi-select').forEach(el => el.value = '');
  const ni = document.getElementById('avatar-name-input');
  if(ni) ni.value = '';
  updateVecnaBar();
  updateFuerzaBar();
  updateXPBar();
  updateStats();
  renderReflections();
  restoreStars();
  updateGates();
  updateSessionProgUI();
  restoreAvatar();
  ['once','dustin','max','lucas','will'].forEach(c => {
    const card = document.getElementById('char-'+c);
    const tag = document.getElementById(c+'-tag');
    if(card) { card.classList.add('locked-char'); card.classList.remove('unlocked'); card.style.borderColor=''; card.style.filter=''; card.style.opacity=''; }
    if(tag) { tag.textContent='🔒 BLOQUEADO'; tag.style.background='rgba(255,255,255,0.05)'; tag.style.color='var(--text-dim)'; tag.style.border='1px solid var(--border)'; }
  });
  showToast('🔄 ¡Todo reiniciado a cero!');
}


let toastTimeout;
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(toastTimeout);
  toastTimeout = setTimeout(() => t.classList.remove('show'), 2500);
}

// ===== MAPA =====
var _mc=['#e74c3c','#3498db','#f39c12','#8e44ad','#00ff88','#e67e22','#c0392b'];
var _mn=['S1 lista','S2 lista','S3 lista','S4 lista','S5 lista','S6 lista','S7 lista'];
function updateMapa(){
  for(var i=1;i<=7;i++){
    var z=document.getElementById('mz'+i),t=document.getElementById('mzt'+i);
    if(!z)continue;
    if(state.sessions[i-1]){
      var c=_mc[i-1];
      z.setAttribute('fill',c+'44');z.setAttribute('stroke',c);z.setAttribute('stroke-width','2.5');
      z.style.filter='drop-shadow(0 0 10px '+c+')';
      if(t){t.setAttribute('fill',c);t.textContent='S'+i+' OK';}
    }else{
      z.setAttribute('fill','rgba(20,0,40,0.7)');z.setAttribute('stroke','rgba(80,0,120,0.4)');z.setAttribute('stroke-width','1.5');
      z.style.filter='';
      if(t){t.setAttribute('fill','rgba(180,100,255,0.5)');t.textContent='S'+i;}
    }
  }
  var leg=document.getElementById('mapa-leyenda');
  if(!leg)return;
  var h='';
  for(var j=0;j<7;j++){
    var done=state.sessions[j],col=done?_mc[j]:'var(--border)';
    h+='<div style="background:rgba(255,255,255,0.02);border:1px solid '+col+';border-radius:6px;padding:7px 9px;font-size:9px;display:flex;align-items:center;gap:6px">';
    h+='<span style="font-size:12px">'+(done?'[OK]':'[ ]')+'</span>';
    h+='<div><div style="font-family:Orbitron,sans-serif;font-size:7px;color:'+(done?col:'var(--text-dim)')+';margin-bottom:1px">S'+(j+1)+'</div>';
    h+='<div style="color:var(--text-dim)">Sesion '+(j+1)+'</div></div></div>';
  }
  leg.innerHTML=h;
}

// ===== PODCAST =====
var _rMR=null,_rCh=[],_rTI=null,_rSec=0,_rAn=null,_rAF=null;
var _recs={1:[],2:[],3:[],4:[]},_rEp=1;
function selectEp(ep,el){
  _rEp=ep;
  for(var i=1;i<=4;i++){var b=document.getElementById('epbtn'+i);if(b){b.style.background='rgba(255,255,255,0.03)';b.style.border='2px solid var(--border)';}}
  el.style.background='rgba(192,57,43,0.15)';el.style.border='2px solid var(--red-glow)';
  var t=document.getElementById('rec-ep-title');if(t)t.textContent='EP. '+ep+' SELECCIONADO';
  _renderRecs();
}
function toggleRecord(){
  if(_rMR&&_rMR.state==='recording'){_rMR.stop();return;}
  if(!navigator.mediaDevices){showToast('Necesita HTTPS para grabar');return;}
  navigator.mediaDevices.getUserMedia({audio:true}).then(function(stream){
    try{var ac=new(window.AudioContext||window.webkitAudioContext)();var src=ac.createMediaStreamSource(stream);_rAn=ac.createAnalyser();_rAn.fftSize=256;src.connect(_rAn);_drawRW();}catch(e){}
    _rMR=new MediaRecorder(stream);_rCh=[];
    _rMR.ondataavailable=function(e){_rCh.push(e.data);};
    _rMR.onstop=function(){
      clearInterval(_rTI);if(_rAF)cancelAnimationFrame(_rAF);stream.getTracks().forEach(function(t){t.stop();});
      var blob=new Blob(_rCh,{type:'audio/webm'}),url=URL.createObjectURL(blob);
      _recs[_rEp].unshift({url:url,date:new Date().toLocaleTimeString('es-ES'),secs:_rSec});
      _renderRecs();
      var br=document.getElementById('btn-rec'),bs=document.getElementById('btn-stop');
      if(br){br.textContent='GRABAR';br.style.background='linear-gradient(135deg,var(--red-dark),var(--red-glow))';}
      if(bs){bs.disabled=true;bs.style.cursor='not-allowed';bs.style.color='var(--text-dim)';}
      _rSec=0;var rt=document.getElementById('rec-timer');if(rt)rt.textContent='00:00';
      _clearRW();addXP(15);showToast('Grabacion guardada Ep.'+_rEp);
    };
    _rMR.start();_rSec=0;
    _rTI=setInterval(function(){_rSec++;var m=String(Math.floor(_rSec/60)).padStart(2,'0'),s=String(_rSec%60).padStart(2,'0');var rt=document.getElementById('rec-timer');if(rt)rt.textContent=m+':'+s;},1000);
    var br=document.getElementById('btn-rec'),bs=document.getElementById('btn-stop');
    if(br){br.textContent='GRABANDO...';br.style.background='linear-gradient(135deg,#440000,#ff2200)';}
    if(bs){bs.disabled=false;bs.style.cursor='pointer';bs.style.color='var(--text)';}
  }).catch(function(){showToast('Permiso de microfono denegado');});
}
function stopRecord(){if(_rMR&&_rMR.state==='recording')_rMR.stop();}
function _drawRW(){
  var c=document.getElementById('rec-canvas');if(!c||!_rAn)return;
  var ctx=c.getContext('2d'),buf=new Uint8Array(_rAn.frequencyBinCount);
  function draw(){_rAF=requestAnimationFrame(draw);_rAn.getByteTimeDomainData(buf);ctx.clearRect(0,0,c.width,c.height);ctx.strokeStyle='#e74c3c';ctx.lineWidth=2;ctx.beginPath();var sw=c.width/buf.length,x=0;for(var i=0;i<buf.length;i++){var y=(buf[i]/128)*c.height/2;i===0?ctx.moveTo(x,y):ctx.lineTo(x,y);x+=sw;}ctx.stroke();}
  draw();
}
function _clearRW(){var c=document.getElementById('rec-canvas');if(!c)return;var ctx=c.getContext('2d');ctx.clearRect(0,0,c.width,c.height);ctx.strokeStyle='rgba(231,76,60,0.15)';ctx.lineWidth=1;ctx.beginPath();ctx.moveTo(0,26);ctx.lineTo(420,26);ctx.stroke();}
function _renderRecs(){
  var list=document.getElementById('rec-list');if(!list)return;
  var recs=_recs[_rEp];
  if(!recs||!recs.length){list.innerHTML='<div style="font-size:11px;color:var(--text-dim);text-align:center;padding:12px">No hay grabaciones para este episodio</div>';return;}
  var h='';
  for(var i=0;i<recs.length;i++){
    var r=recs[i],m=String(Math.floor(r.secs/60)).padStart(2,'0'),s=String(r.secs%60).padStart(2,'0');
    h+='<div style="background:rgba(255,255,255,0.03);border:1px solid var(--border);border-radius:7px;padding:9px;display:flex;align-items:center;gap:9px;margin-bottom:7px;flex-wrap:wrap">';
    h+='<div style="flex-shrink:0"><div style="font-family:Orbitron,sans-serif;font-size:8px;color:var(--cyan)">EP.'+_rEp+' TOMA '+(recs.length-i)+'</div>';
    h+='<div style="font-size:9px;color:var(--text-dim)">'+r.date+' '+m+':'+s+'</div></div>';
    h+='<audio controls src="'+r.url+'" style="flex:1;height:28px;min-width:0"></audio>';
    h+='<a href="'+r.url+'" download="ep'+_rEp+'_t'+(recs.length-i)+'.webm" style="color:var(--green);font-size:16px;text-decoration:none;flex-shrink:0">[DL]</a></div>';
  }
  list.innerHTML=h;
}

// ===== IA =====
var _iaDb=[
  {k:['pulso','corazon','frecuencia','bpm','cardiaca'],r:'🔬 El corazon es vuestro reactor, Guardianes. En reposo late 60-100 veces por minuto, pero al hacer ejercicio puede llegar a 180-200. Cuanto mas entrenais, mas eficiente se vuelve y mas bajo es vuestro pulso en reposo. Medidlo ahora mismo y comparadlo con el de hace unas semanas. Notais diferencia?'},
  {k:['flexibilidad','estirar','elasticidad'],r:'📡 Los musculos son como cables del Upside Down: si no los estiras, se endurecen y pueden romperse. Solo 10 minutos de estiramientos al dia durante unas semanas marcan una diferencia enorme. Quien del grupo crees que es el mas flexible y por que puede ser eso?'},
  {k:['fuerza','musculo','tonificar'],r:'💪 La fuerza muscular se construye poco a poco, como derrotar a VECNA: sesion a sesion. Los musculos crecen cuando los trabajais Y cuando descansais. Sin descanso no hay adaptacion. Que ejercicio de fuerza os resulta mas dificil y cual mas facil?'},
  {k:['resistencia','cansancio','aguante','cardio'],r:'🏃 La resistencia es la capacidad de aguantar el esfuerzo en el tiempo. Mejora con entrenamiento regular y variado. El truco del Laboratorio: cuando os canséis, no paréis del todo, bajad el ritmo. Cual fue el momento en que mas os costó aguantar en las sesiones?'},
  {k:['emocion','nervioso','miedo','enfado','tristeza','frustrado'],r:'🧠 Las emociones durante el ejercicio son señales de vuestro cuerpo, no problemas. Los nervios antes de un reto os preparan para dar lo mejor. La clave es reconocerlas sin que os bloqueen. Que emocion aparece mas a menudo cuando os equivocais en clase?'},
  {k:['error','equivocar','fallo','fracaso'],r:'🛡️ El error es el mejor maestro del Laboratorio Hawkins. Cada caida de Hopper le hizo mas fuerte. Cuando os equivocais en un ejercicio, preguntaos: que puedo ajustar? No que hice mal. Cual fue el error del que mas aprendisteis en estas sesiones?'},
  {k:['conflicto','pelea','discutir','equipo','grupo'],r:'🤝 En Hawkins los conflictos los resolvian hablando, no ignorandolos. La clave: escuchar antes de responder, y buscar soluciones juntos en vez de buscar culpables. Que estrategia usasteis la ultima vez que hubo tension en el grupo?'},
  {k:['mito','mentira','verdad','creer','real'],r:'🔍 El Laboratorio tiene datos claros: muchos mitos del ejercicio son tan falsos como el Demogorgon. El musculo NO se convierte en grasa, son tejidos completamente distintos. Que otros mitos sobre el deporte habeis escuchado y quereis comprobar?'},
  {k:['salud','beneficio','cuerpo','sano','activo'],r:'💡 El ejercicio regular reduce el estres, mejora el sueno, fortalece el corazon y hasta mejora la concentracion en clase. No es magia, es ciencia guardiana. Cual de estos beneficios notais mas en vosotros mismos tras estas semanas?'},
  {k:['calentamiento','calentar','lesion','prevenir'],r:'🔥 El calentamiento es el escudo que os protege de las lesiones. Al menos 5-10 minutos aumentando la temperatura muscular de forma progresiva. Sin escudo, el Upside Down gana terreno. Como calentais antes de empezar normalmente?'},
  {k:['descanso','dormir','recuperar','sueno'],r:'😴 El Laboratorio tiene datos claros: los ninos de vuestra edad necesitan 9-11 horas de sueno. Durante el sueno los musculos se reparan y el cerebro procesa lo aprendido. El descanso ES entrenamiento. Cuantas horas dormis de media y como os levantais?'},
  {k:['podcast','grabar','episodio','audio','microfono'],r:'🎙️ Para un episodio guardián de calidad: hablad despacio y claro, usad ejemplos de vuestra propia experiencia, y no leais un papel: contadlo como si le hablarais a un amigo. Que parte del podcast os parece mas dificil de preparar?'},
  {k:['habito','sedentarismo','movimiento','actividad'],r:'⚡ El sedentarismo es el aliado de VECNA. Nuestro cuerpo esta diseñado para moverse, no para estar sentado 8 horas. Incluso levantarse y caminar 5 minutos cada hora marca la diferencia. Cuantas horas al dia estais sentados sin moveros?'},
  {k:['alimentacion','comer','nutricion','dieta'],r:'🥗 El Laboratorio confirma: la alimentacion y el ejercicio van de la mano. Nuestro cuerpo necesita combustible de calidad para rendir. Sin buen combustible, hasta los Guardianes fallan. Que comeis normalmente antes de hacer ejercicio?'}
];
function _iaFallback(msg){
  var lm=msg.toLowerCase();
  for(var i=0;i<_iaDb.length;i++)for(var j=0;j<_iaDb[i].k.length;j++)if(lm.indexOf(_iaDb[i].k[j])!==-1)return _iaDb[i].r;
  return 'Senal recibida en el Laboratorio Hawkins. Tu cuerpo es la herramienta mas poderosa que teneis. Cuidadlo y escuchadlo. Podeis reformular la pregunta?';
}
function sendIA(){
  var input=document.getElementById('ia-input'),chat=document.getElementById('ia-chat');
  if(!input||!chat)return;
  var msg=input.value.trim();if(!msg)return;input.value='';
  var uDiv=document.createElement('div');
  uDiv.style.cssText='display:flex;gap:9px;align-items:flex-start;flex-direction:row-reverse;margin-bottom:10px';
  var uBub=document.createElement('div');
  uBub.style.cssText='background:rgba(192,57,43,0.12);border:1px solid rgba(192,57,43,0.3);border-radius:8px 0 8px 8px;padding:10px 13px;font-size:12px;color:var(--text);line-height:1.6;max-width:82%';
  uBub.textContent=msg;
  var uIco=document.createElement('div');uIco.style.cssText='font-size:18px;flex-shrink:0';uIco.textContent='🧑';
  uDiv.appendChild(uIco);uDiv.appendChild(uBub);chat.appendChild(uDiv);
  var tDiv=document.createElement('div');
  tDiv.style.cssText='display:flex;gap:9px;align-items:flex-start;margin-bottom:10px';
  var bub=document.createElement('div');
  bub.style.cssText='background:rgba(0,212,255,0.07);border:1px solid rgba(0,212,255,0.2);border-radius:0 8px 8px 8px;padding:10px 13px;font-size:12px;color:var(--text-dim);font-style:italic;line-height:1.6;max-width:82%';
  bub.textContent='El Laboratorio procesando...';
  var tIco=document.createElement('div');tIco.style.cssText='font-size:18px;flex-shrink:0';tIco.textContent='🔬';
  tDiv.appendChild(tIco);tDiv.appendChild(bub);chat.appendChild(tDiv);chat.scrollTop=chat.scrollHeight;
  var gn=state.avatarName||'Guardianes',ses=state.sessions.filter(Boolean).length;
  // Respuesta instantánea con IA offline inteligente
  setTimeout(function(){
    var reply=_iaFallback(msg);
    bub.textContent=reply;bub.style.fontStyle='normal';bub.style.color='var(--text)';chat.scrollTop=chat.scrollHeight;
  }, 600);
}

// ===== EXHIBICION =====
function abrirExhibicion(){var ov=document.getElementById('exh-overlay');if(ov){ov.style.display='block';document.body.style.overflow='hidden';refreshExhibicion();}}
function cerrarExhibicion(){var ov=document.getElementById('exh-overlay');if(ov)ov.style.display='none';document.body.style.overflow='';}
function refreshExhibicion(){
  var eg=document.getElementById('exh-grupo');if(eg)eg.textContent=(state.avatarName||'GRUPO GUARDIAN').toUpperCase();
  var vb=document.getElementById('exh-vbar'),vv=document.getElementById('exh-vval');if(vb)vb.style.width=state.vecnaHP+'%';if(vv)vv.textContent=state.vecnaHP+' / 100';
  var fb=document.getElementById('exh-fbar'),fv=document.getElementById('exh-fval');var f=Math.min(100,state.fuerza||0);if(fb)fb.style.width=f+'%';if(fv)fv.textContent=f+' / 100';
  var xp=document.getElementById('exh-xp');if(xp)xp.textContent=state.xp||0;
  var icons=['🎙️','💪','🏃','😤','🛡️','🎵','🏆'];
  var ses=document.getElementById('exh-ses');
  if(ses){var sh='';for(var i=0;i<7;i++){var done=state.sessions[i];sh+='<div style="background:'+(done?'rgba(0,255,136,0.15)':'rgba(255,255,255,0.03)')+';border:2px solid '+(done?'var(--green)':'var(--border)')+';border-radius:6px;padding:5px;text-align:center"><div style="font-size:13px">'+(done?'[+]':icons[i])+'</div><div style="font-family:Orbitron,sans-serif;font-size:7px;color:'+(done?'var(--green)':'var(--text-dim)')+'">S'+(i+1)+'</div></div>';}ses.innerHTML=sh;}
  var cl=[{e:'💀',c:'#e74c3c',n:'HOPPER',on:true},{e:'🌪️',c:'#3498db',n:'ONCE',on:state.chars.once},{e:'⚙️',c:'#f39c12',n:'DUSTIN',on:state.chars.dustin},{e:'🎶',c:'#8e44ad',n:'MAX',on:state.chars.max},{e:'🧭',c:'#00ff88',n:'LUCAS',on:state.chars.lucas},{e:'🔥',c:'#e74c3c',n:'WILL',on:state.chars.will}];
  var ch=document.getElementById('exh-chars');
  if(ch){var ch2='';for(var j=0;j<cl.length;j++){var cc=cl[j];ch2+='<div style="text-align:center;opacity:'+(cc.on?1:0.25)+'"><div style="font-size:26px;border:2px solid '+(cc.on?cc.c:'var(--border)')+';border-radius:50%;width:42px;height:42px;display:flex;align-items:center;justify-content:center;margin:0 auto 3px">'+cc.e+'</div><div style="font-family:Orbitron,sans-serif;font-size:7px;color:'+(cc.on?cc.c:'var(--text-dim)')+'">'+cc.n+'</div></div>';}ch.innerHTML=ch2;}
  var qv=document.getElementById('qr-url'),eq=document.getElementById('exh-qr');
  if(eq&&qv&&qv.value.trim())eq.innerHTML='<img src="https://api.qrserver.com/v1/create-qr-code/?size=110x110&data='+encodeURIComponent(qv.value.trim())+'" style="border-radius:4px;background:white;padding:6px">';
}
function generarQR(){
  var u=document.getElementById('qr-url'),o=document.getElementById('qr-output');
  if(!u||!o)return;var url=u.value.trim();if(!url){showToast('Escribe primero la URL');return;}
  o.innerHTML='<div style="display:inline-block;background:white;padding:10px;border-radius:8px"><img src="https://api.qrserver.com/v1/create-qr-code/?size=160x160&data='+encodeURIComponent(url)+'" style="display:block"><div style="font-family:monospace;font-size:9px;color:#333;text-align:center;margin-top:5px">Escanea para acceder</div></div>';
  showToast('QR generado correctamente');
}

// ===== HOOK mapa into session toggle =====
var _origTP=window.toggleSessionProg;
window.toggleSessionProg=function(n){if(_origTP)_origTP(n);updateMapa();if(document.getElementById('exh-overlay')&&document.getElementById('exh-overlay').style.display!=='none')refreshExhibicion();};

// ===== INIT =====
var _origOL=window.onload;
window.onload=function(){if(_origOL)_origOL();updateMapa();_clearRW();_renderRecs();};

// ===== KPSI MULTI-MEMBER =====
var currentKPSIMember = 1;
function selectKPSIMember(m, btn) {
  currentKPSIMember = m;
  // Update button styles
  document.querySelectorAll('.kpsi-member-btn').forEach(function(b) {
    b.style.background = 'rgba(255,255,255,0.03)';
    b.style.borderColor = 'var(--border)';
    b.style.color = 'var(--text-dim)';
  });
  btn.style.background = m === 'G' ? 'rgba(243,156,18,0.15)' : 'rgba(0,212,255,0.15)';
  btn.style.borderColor = m === 'G' ? 'var(--yellow)' : 'var(--cyan)';
  btn.style.color = m === 'G' ? 'var(--yellow)' : 'var(--cyan)';
  var lbl = document.getElementById('kpsi-member-label');
  if (lbl) lbl.textContent = 'Rellenando KPSI de: ' + (m === 'G' ? 'MODO GRUPAL' : 'MIEMBRO ' + m);
  // Restore selects for this member
  restoreKPSIForMember(m);
}

function getKPSIKey(key) {
  return 'M' + currentKPSIMember + '_' + key;
}

function saveKPSI(key, val) {
  var fullKey = getKPSIKey(key);
  if (!state.kpsi) state.kpsi = {};
  state.kpsi[fullKey] = val;
  save();
  var initKeys = ['k1i','k2i','k3i','k4i','k5i','k6i','k7i','k8i','k9i'];
  var filled = initKeys.filter(function(k) { return state.kpsi[getKPSIKey(k)] && state.kpsi[getKPSIKey(k)] !== ''; }).length;
  if (filled >= 4) { state.kpsiDone = true; save(); }
}

function restoreKPSIForMember(m) {
  var prev = currentKPSIMember;
  currentKPSIMember = m;
  document.querySelectorAll('[onchange*="saveKPSI"]').forEach(function(el) {
    var match = el.getAttribute('onchange').match(/saveKPSI\('([^']+)'/);
    if (match) {
      var fullKey = getKPSIKey(match[1]);
      el.value = (state.kpsi && state.kpsi[fullKey]) ? state.kpsi[fullKey] : '';
    }
  });
  currentKPSIMember = prev;
  currentKPSIMember = m;
}

</script>
<div id="exh-overlay" style="display:none;position:fixed;inset:0;z-index:9000;background:#050208;overflow:auto">
  <button onclick="cerrarExhibicion()" style="position:fixed;top:12px;right:16px;background:rgba(192,57,43,0.3);border:1px solid var(--red-glow);border-radius:6px;color:var(--red-glow);font-family:'Orbitron',sans-serif;font-size:10px;padding:7px 12px;cursor:pointer;z-index:9010">SALIR</button>
  <div style="max-width:860px;margin:0 auto;padding:24px 16px;text-align:center">
    <div style="font-family:'Creepster',cursive;font-size:clamp(26px,6vw,58px);color:var(--red-glow);text-shadow:0 0 40px rgba(231,76,60,0.8);margin-bottom:4px">GUARDIANES DE HAWKINS</div>
    <div id="exh-grupo" style="font-family:'Orbitron',sans-serif;font-size:clamp(11px,3vw,18px);color:var(--cyan);letter-spacing:4px;margin-bottom:22px">GRUPO GUARDIAN</div>
    <div style="background:rgba(12,4,4,0.9);border:1px solid rgba(192,57,43,0.4);border-radius:12px;padding:18px;margin-bottom:14px">
      <div style="font-family:'Orbitron',sans-serif;font-size:11px;color:var(--red-glow);letter-spacing:3px;margin-bottom:7px">VIDA DE VECNA</div>
      <div style="height:22px;background:rgba(255,255,255,0.05);border-radius:11px;overflow:hidden;border:1px solid rgba(192,57,43,0.3)"><div id="exh-vbar" style="height:100%;background:linear-gradient(90deg,var(--red-dark),var(--red-glow));border-radius:11px;transition:width 1s ease;width:100%"></div></div>
      <div id="exh-vval" style="font-family:'Share Tech Mono',monospace;font-size:18px;color:var(--red-glow);margin-top:5px">100 / 100</div>
    </div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:14px">
      <div style="background:rgba(2,10,4,0.9);border:1px solid rgba(0,255,136,0.3);border-radius:12px;padding:16px">
        <div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--green);letter-spacing:2px;margin-bottom:7px">FUERZA</div>
        <div style="height:12px;background:rgba(255,255,255,0.05);border-radius:6px;overflow:hidden"><div id="exh-fbar" style="height:100%;background:linear-gradient(90deg,#008830,var(--green));border-radius:6px;transition:width 1s ease;width:0%"></div></div>
        <div id="exh-fval" style="font-family:'Share Tech Mono',monospace;font-size:16px;color:var(--green);margin-top:5px">0 / 100</div>
      </div>
      <div style="background:rgba(10,8,2,0.9);border:1px solid rgba(243,156,18,0.3);border-radius:12px;padding:16px">
        <div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--yellow);letter-spacing:2px;margin-bottom:3px">XP TOTAL</div>
        <div id="exh-xp" style="font-family:'Orbitron',sans-serif;font-size:clamp(28px,5vw,50px);font-weight:900;color:var(--yellow)">0</div>
        <div style="font-size:9px;color:var(--text-dim)">/ 500 XP</div>
      </div>
    </div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:14px">
      <div style="background:var(--panel);border:1px solid var(--border);border-radius:12px;padding:16px">
        <div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--cyan);letter-spacing:2px;margin-bottom:10px">SESIONES</div>
        <div id="exh-ses" style="display:grid;grid-template-columns:repeat(7,1fr);gap:4px"></div>
      </div>
      <div style="background:var(--panel);border:1px solid var(--border);border-radius:12px;padding:16px">
        <div style="font-family:'Orbitron',sans-serif;font-size:9px;color:var(--cyan);letter-spacing:2px;margin-bottom:10px">GUARDIANES</div>
        <div id="exh-chars" style="display:flex;gap:8px;justify-content:center;flex-wrap:wrap"></div>
      </div>
    </div>
    <div id="exh-qr"></div>
  </div>
</div>
</body>
</html>
(9).html…]()
