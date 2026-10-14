---
theme: default
title: Rayperclip Demo
info: |
  Demo van wat REA is en wat je ermee kan
transition: slide-left
mdc: true
class: text-center
---

# REA + Opus => Rayperclip 🖇️

Een demo van wat REA is en wat je er mee kan

---

# Wat is REA? 🔍

**REA = Reverse Engineer Anything**

Een toolkit die reverse-engineering-mogelijkheden toevoegt aan AI-coding agents 🤖

- Claude Code
- Cursor
- Copilot
- OpenCode
- Vergelijkbare CLI-assistenten

---

# Wat kun je ermee? 🛠️

1. 🧩 **Native binaries inspecteren**
   Exe's en libraries (.dll, .dylib, .so) decompileren en analyseren: strings, assembly, functies, call-chains
2. 📦 **JavaScript & Electron-apps doorgronden**
   ASAR-archieven, gebundelde frontend-scripts, interne IPC-communicatie en routes in kaart brengen
3. 🌐 **Runtime- en browsergedrag analyseren**
   Via debugging-interfaces (zoals CDP) netwerk- en procesactiviteit monitoren en vergelijken
4. 🧬 **Logica reproduceren of klonen**
   Business rules of game-mechanieken achterhalen en nabouwen in schone code

---

# Logica reproduceren 🎮

Voorbeelden van wat REA kan achterhalen:

- 🧮 De exacte berekeningsregels in de **Windows Calculator**
- 🦖 De versnellingslogica in de **Chrome Dino-game**

…en direct laten nabouwen in schone code ✨

---
layout: center
class: text-center
---

# Ondersteuning ✅

<img src="/rea_support.jpeg" class="mx-auto" />

---
layout: center
class: text-center
---

# Demo tijd! 🚀

Van gesloten app naar eigen "Clean room" app

---

# Wat heb ik gebruikt? 🧰

- 📋 **Copyclip 2**: macOS-app die klembordgeschiedenis toevoegt
  (zoals Windows-toets + V)
- 🍎 Blijkt geschreven in **Swift**
- 🔍 **REA** als reverse-engineering toolkit
- 🤖 **OpenCode** als AI-agent
- 🐉 **Ghidra**: software reverse engineering framework

---

# Voorbereiding ⚙️

1. ⬇️ REA installeren via `npx`
2. 🔧 REA configureren in OpenCode
3. 🐉 Ghidra installeren en configureren

---

# Prompt 1: snap de originele app 🕵️

> Analyseer `/Applications/Copyclip 2.app/Contents/MacOS/<App>` met Ghidra

Doel: begrijpen wat de OG-app doet

---

# Prompt 2: bouw het na 🦀

> Maak een nieuwe app in **Rust** die alles kan wat Copyclip 2 kan

Vragen die de agent stelde:

- 🖼️ UI
- 💾 Opslag en scope
- ⌨️ Hotkeys
- 🎨 Thema's
- 📌 Autopaste
- ⚙️ Opties en instellingen

---

# ☕️ Pauze

15 minuten (misschien iets langer, plus een paar extra prompts)

---
layout: center
class: text-center
---

<div class="finale">
  <div class="ring"></div>
  <div class="ring ring2"></div>
  <span class="spark" style="--n:0"></span><span class="spark" style="--n:1"></span><span class="spark" style="--n:2"></span><span class="spark" style="--n:3"></span><span class="spark" style="--n:4"></span><span class="spark" style="--n:5"></span><span class="spark" style="--n:6"></span><span class="spark" style="--n:7"></span><span class="spark" style="--n:8"></span><span class="spark" style="--n:9"></span><span class="spark" style="--n:10"></span><span class="spark" style="--n:11"></span>
  <div class="clip">🖇️</div>
  <div class="small">Uitkomst</div>
  <h1 class="title"><span class="letter" style="--i:0">R</span><span class="letter" style="--i:1">a</span><span class="letter" style="--i:2">y</span><span class="letter" style="--i:3">p</span><span class="letter" style="--i:4">e</span><span class="letter" style="--i:5">r</span><span class="letter" style="--i:6">c</span><span class="letter" style="--i:7">l</span><span class="letter" style="--i:8">i</span><span class="letter" style="--i:9">p</span></h1>
</div>

<style>
.finale { position: relative; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 100%; overflow: visible; perspective: 800px; }
.clip { font-size: 7rem; animation: clip-in 1.4s cubic-bezier(.2,1.4,.4,1) both, float 3s ease-in-out 1.4s infinite; filter: drop-shadow(0 0 25px #a855f7); }
.small { font-size: 1.5rem; letter-spacing: .6em; text-transform: uppercase; opacity: 0; animation: fade-up .8s ease-out 1.2s forwards; }
.title { display: flex; font-size: 6rem !important; line-height: 1.4 !important; margin: 0; overflow: visible; }
.letter { display: inline-block; padding: .2em .02em; line-height: 1.4; opacity: 0; background: linear-gradient(90deg, #f472b6, #a855f7, #38bdf8, #34d399, #f472b6); background-size: 300% 100%; -webkit-background-clip: text; background-clip: text; color: transparent; animation: letter-in .9s cubic-bezier(.2,1.5,.4,1) calc(1.5s + var(--i) * .09s) forwards, shine 4s linear 3s infinite, wave 2s ease-in-out calc(3s + var(--i) * .1s) infinite; }
.ring { position: absolute; width: 10px; height: 10px; border: 3px solid #a855f7; border-radius: 50%; opacity: 0; animation: ring 2s ease-out 1.2s infinite; }
.ring2 { border-color: #38bdf8; animation-delay: 1.8s; }
.spark { position: absolute; top: 50%; left: 50%; width: 10px; height: 10px; border-radius: 50%; background: hsl(calc(var(--n) * 30) 90% 60%); opacity: 0; animation: burst 1.6s ease-out 1.1s forwards; --a: calc(var(--n) * 30deg); }
@keyframes clip-in { 0% { transform: translateY(-600px) rotate(-720deg) scale(.1); opacity: 0; } 70% { opacity: 1; } 100% { transform: none; opacity: 1; } }
@keyframes float { 50% { transform: translateY(-14px) rotate(8deg); } }
@keyframes fade-up { from { opacity: 0; transform: translateY(20px); } to { opacity: .8; transform: none; } }
@keyframes letter-in { 0% { opacity: 0; transform: translateY(-120px) rotateX(540deg) scale(3); filter: blur(12px); } 100% { opacity: 1; transform: none; filter: none; } }
@keyframes shine { to { background-position: 300% 0; } }
@keyframes wave { 50% { transform: translateY(-8px); } }
@keyframes ring { 0% { opacity: .9; transform: scale(1); } 100% { opacity: 0; transform: scale(90); } }
@keyframes burst { 0% { opacity: 1; transform: rotate(var(--a)) translateX(0); } 100% { opacity: 0; transform: rotate(var(--a)) translateX(380px) scale(.3); } }
</style>

---
layout: center
class: text-center
---

# Bedankt! 🎉

Vragen?
