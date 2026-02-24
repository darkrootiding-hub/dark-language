<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DarkRoot // OVERLORD v5 - AI System Admin</title>

<!-- LIBRARIES -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/styles/atom-one-dark.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.7.0/highlight.min.js"></script>

<style>
/* ================= VARIABLES & THEME ================= */
:root {
  --bg-color: #030303;
  --panel-bg: rgba(10, 12, 16, 0.96);
  --border-color: #1f1f1f;
  --primary: #00ff41;
  --secondary: #a855f7;
  --danger: #ff003c;
  --warning: #facc15;
  --info: #3b82f6;
  --text-main: #e0e0e0;
  --text-dim: #555;
  --glass: blur(12px);
  --success: #10b981;
  --deepseek-green: #00d8a7;
  --cyber-blue: #00d4ff;
  --hacker-green: #00ff88;
}

* { box-sizing: border-box; scrollbar-width: thin; scrollbar-color: var(--primary) #000; }
::-webkit-scrollbar { width: 5px; }
::-webkit-scrollbar-thumb { background: var(--primary); }

body {
  margin: 0; font-family: 'Courier New', Courier, monospace;
  background-color: var(--bg-color); color: var(--text-main);
  height: 100vh; width: 100vw; overflow: hidden;
  display: flex; justify-content: center; align-items: center;
}

/* MATRIX BG */
#matrix-canvas { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: 0; opacity: 0.05; pointer-events: none; }

/* LOGIN */
#login-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: #000; z-index: 9999; display: flex; justify-content: center; align-items: center; }
.login-box { width: 350px; padding: 40px; border: 1px solid var(--primary); background: #050505; box-shadow: 0 0 50px rgba(0, 255, 65, 0.1); text-align: center; }

/* LAYOUT */
.main-wrapper { position: relative; z-index: 10; width: 100%; height: 100%; display: flex; flex-direction: column; padding: 5px; }

.dashboard-grid {
  display: none; width: 100%; height: 100%;
  grid-template-columns: 260px 1fr 300px; 
  grid-template-rows: 60px 1fr 160px; 
  gap: 8px;
}

/* PANELS */
.panel {
  background: var(--panel-bg); border: 1px solid var(--border-color);
  padding: 15px; display: flex; flex-direction: column;
  box-shadow: 0 10px 30px rgba(0,0,0,0.9); border-radius: 2px;
  overflow: hidden;
}

.header-panel { grid-column: 1 / -1; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid var(--primary); }
.sidebar { grid-row: 2 / -1; border-right: 1px solid var(--border-color); overflow-y: auto; }
.main-content { grid-column: 2 / 3; grid-row: 2 / 3; overflow: hidden; position: relative; }
.stats-panel { grid-column: 3 / 4; grid-row: 2 / 3; border-left: 1px solid var(--border-color); overflow-y: auto; }
.console-panel { grid-column: 2 / 4; grid-row: 3 / 4; background: #000; font-family: 'Fira Code', monospace; overflow-y: auto; font-size: 0.75rem; border-top: 1px solid var(--border-color); color:#aaa; }

/* UI ELEMENTS */
h1 { color: var(--primary); margin: 0; font-size: 1.2rem; letter-spacing: 2px; font-weight: bold; text-shadow: 0 0 10px rgba(0,255,65,0.4); }
h2 { font-size: 1rem; color: var(--primary); margin: 15px 0 10px; border-bottom: 1px solid #333; padding-bottom: 5px; }
h3 { font-size: 0.7rem; color: var(--text-dim); margin: 0 0 10px 0; border-bottom: 1px solid #222; padding-bottom: 5px; text-transform: uppercase; letter-spacing: 1px; }

input, textarea, select {
  width: 100%; padding: 8px; margin: 4px 0;
  background: #080808; border: 1px solid #333; color: var(--primary);
  font-family: monospace; outline: none; font-size: 0.8rem;
}
input:focus, textarea:focus { border-color: var(--primary); background: #0a1a0a; }

button {
  background: rgba(0, 255, 65, 0.05); border: 1px solid var(--primary); color: var(--primary);
  padding: 6px 10px; cursor: pointer; font-weight: bold; font-family: monospace; transition: 0.2s;
  font-size: 0.7rem; text-transform: uppercase; margin-bottom: 4px;
}
button:hover { background: var(--primary); color: #000; box-shadow: 0 0 15px var(--primary); }

button.primary { border-color: var(--info); color: var(--info); }
button.primary:hover { background: var(--info); color: white; }

button.danger { border-color: var(--danger); color: var(--danger); background: rgba(255, 0, 60, 0.05); }
button.danger:hover { background: var(--danger); color: white; box-shadow: 0 0 15px var(--danger); }

button.warning { border-color: var(--warning); color: var(--warning); }
button.warning:hover { background: var(--warning); color: black; }

button.success { border-color: var(--success); color: var(--success); }
button.success:hover { background: var(--success); color: black; }

button.deepseek { border-color: var(--deepseek-green); color: var(--deepseek-green); }
button.deepseek:hover { background: var(--deepseek-green); color: black; }

/* TABS */
.nav-tabs { display: flex; gap: 2px; margin-bottom: 10px; border-bottom: 1px solid #333; flex-wrap: wrap; }
.nav-tab {
  padding: 8px 15px; cursor: pointer; color: #555; font-weight: bold; font-size: 0.75rem;
  border-top: 2px solid transparent; background: #050505; flex:1; text-align: center; min-width: 80px;
}
.nav-tab:hover { color: #fff; background: #111; }
.nav-tab.active { color: var(--primary); border-top: 2px solid var(--primary); background: #111; }

.view-section { display: none; height: 100%; flex-direction: column; overflow-y: auto; padding-right: 5px; }
.view-section.active { display: flex; }

/* TABLES */
.table-wrapper { flex: 1; overflow-y: auto; border: 1px solid #222; max-height: 100%; }
table { width: 100%; border-collapse: collapse; font-size: 0.75rem; }
th { position: sticky; top: 0; background: #111; text-align: left; padding: 10px; color: #888; border-bottom: 1px solid #333; }
td { padding: 8px; border-bottom: 1px solid #1a1a1a; color: #ccc; vertical-align: middle; }
tr:hover { background: rgba(255,255,255,0.02); }

/* SPY CHAT */
.spy-layout { display: flex; gap: 10px; height: 100%; overflow: hidden; }
.spy-list { width: 200px; border-right: 1px solid #222; overflow-y: auto; flex-shrink: 0; }
.spy-viewer { flex: 1; display: flex; flex-direction: column; min-width: 0; } 
.chat-container { flex: 1; overflow-y: auto; padding: 15px; background: #050505; border: 1px solid #222; margin-top: 5px; display: flex; flex-direction: column; gap: 8px; }
.msg-bubble { padding: 8px 12px; margin-bottom: 6px; border-radius: 4px; max-width: 90%; font-size: 0.8rem; white-space: pre-wrap; word-wrap: break-word; }
.msg-user { background: #111; border: 1px solid #333; align-self: flex-end; color: #ccc; margin-left: auto; }
.msg-ai { background: rgba(0,255,65,0.05); border: 1px solid rgba(0,255,65,0.2); color: var(--primary); align-self: flex-start; }

/* CODE BLOCKS */
.code-block-wrapper {
  margin-top: 8px; border-radius: 4px; overflow: hidden;
  border: 1px solid #30363d; background: #0d1117; width: 100%;
}
.code-header {
  display: flex; justify-content: space-between; align-items: center;
  padding: 6px 10px; background: #161b22; border-bottom: 1px solid #30363d;
  font-size: 0.7rem; color: #94a3b8;
}
.code-actions button {
  background: transparent; border: 1px solid #30363d; color: #94a3b8;
  border-radius: 4px; padding: 2px 6px; font-size: 0.65rem; cursor: pointer; margin-left: 5px;
}
pre { margin: 0; padding: 0; overflow-x: auto; }
code.hljs { padding: 10px; font-family: 'Fira Code', monospace; font-size: 0.8rem; }

/* SCRATCHPAD */
#admin-scratchpad { width: 100%; height: 200px; background: #080808; color: #ddd; border: 1px solid #333; padding: 10px; font-family: monospace; resize: none; font-size: 0.8rem; }

/* UTILS */
.badge { padding: 2px 5px; border-radius: 3px; font-size: 0.6rem; font-weight: bold; background: #222; color: #fff; }
.badge-banned { background: var(--danger); color: #fff; }
.badge-active { background: var(--primary); color: #000; }
.badge-admin { background: var(--secondary); color: #fff; }
.blink { animation: blinker 1s linear infinite; }
@keyframes blinker { 50% { opacity: 0; } }

.metric-card {
  background: #080808; border: 1px solid #222; padding: 10px; margin-bottom: 10px;
  display: flex; flex-direction: column; gap: 5px;
}
.metric-label { color: #888; font-size: 0.7rem; }
.metric-value { color: var(--primary); font-size: 1.2rem; font-weight: bold; }

/* DYNAMIC BUTTON PREVIEW */
.button-preview {
  background: #080808; border: 1px solid #333; padding: 15px; margin: 10px 0;
  display: flex; flex-direction: column; gap: 10px;
}
.preview-btn {
  padding: 12px; border-radius: 8px; color: white; cursor: pointer;
  display: flex; align-items: center; gap: 10px; font-size: 0.9rem;
}

/* RESPONSIVE */
@media (max-width: 1024px) {
  .dashboard-grid { display: flex; flex-direction: column; overflow-y: auto; }
  .panel { min-height: fit-content; margin-bottom: 5px; }
  .main-content { min-height: 500px; }
}
</style>
</head>
<body>

<canvas id="matrix-canvas"></canvas>

<!-- LOGIN -->
<div id="login-overlay">
  <div class="login-box">
    <h1 style="margin-bottom:30px;">OVERLORD ACCESS</h1>
    <input type="email" id="admin-email" placeholder="COMMANDER ID">
    <input type="password" id="admin-password" placeholder="PASSPHRASE">
    <button onclick="adminLogin()" id="login-btn" style="width:100%; margin-top:20px;">ESTABLISH LINK</button>
    <div id="login-msg" style="color:var(--danger); margin-top:15px; font-size:0.7rem;"></div>
  </div>
</div>

<!-- DASHBOARD -->
<div class="main-wrapper">
  <div class="dashboard-grid" id="dashboard">
    
    <!-- HEADER -->
    <div class="panel header-panel">
      <div style="display:flex; align-items:center; gap:15px;">
        <i class="fas fa-biohazard" style="color:var(--primary); font-size:1.8rem;"></i>
        <div>
          <h1>DARKROOT <span style="color:#fff;">OVERLORD v5</span></h1>
          <div style="font-size:0.6rem; color:#666; letter-spacing:1px;">AI SYSTEM ADMINISTRATOR</div>
        </div>
      </div>
      <div style="display:flex; gap:10px; align-items:center;">
        <div id="maint-indicator" style="display:none; color:var(--warning); font-size:0.7rem; font-weight:bold;" class="blink">⚠ MAINTENANCE MODE</div>
        <button onclick="logout()" class="danger" style="width:auto;">TERMINATE</button>
      </div>
    </div>

    <!-- SIDEBAR -->
    <div class="panel sidebar">
      <h3>CRITICAL CONTROLS</h3>
      
      <div style="margin-bottom: 15px;">
        <label style="font-size:0.6rem; color:var(--warning);">SYSTEM ALERT (BROADCAST)</label>
        <div style="display:flex; gap:2px;">
          <input type="text" id="broadcast-msg" placeholder="Message all users..." style="margin:0;">
          <button onclick="sendBroadcast()" class="warning" style="width:auto; margin:0;"><i class="fas fa-bullhorn"></i></button>
        </div>
      </div>

      <div style="margin-bottom: 15px;">
        <button onclick="toggleMaintenance()" id="btn-maint" class="warning" style="width:100%;">ENABLE MAINTENANCE MODE</button>
      </div>

      <div style="margin-bottom: 15px;">
        <button onclick="downloadFullBackup()" class="primary" style="width:100%;"><i class="fas fa-download"></i> FULL SYSTEM BACKUP</button>
      </div>

      <div style="margin-bottom: 15px;">
        <button onclick="syncAllData()" class="success" style="width:100%;"><i class="fas fa-sync"></i> SYNC ALL DATA</button>
      </div>

      <h3>QUICK STATS</h3>
      <div class="metric-card">
        <span class="metric-label">TOTAL USERS</span>
        <span class="metric-value" id="stat-total">0</span>
      </div>
      <div class="metric-card">
        <span class="metric-label">ACTIVE SESSIONS</span>
        <span class="metric-value" id="stat-sessions">0</span>
      </div>
      <div class="metric-card">
        <span class="metric-label">BRAIN RULES</span>
        <span class="metric-value" id="stat-rules">0</span>
      </div>
      <div class="metric-card">
        <span class="metric-label">DYNAMIC BUTTONS</span>
        <span class="metric-value" id="stat-buttons">0</span>
      </div>

      <h3>NOTES (LOCAL)</h3>
      <textarea id="admin-scratchpad" placeholder="Admin notes..." oninput="saveNotes()"></textarea>
    </div>

    <!-- MAIN CONTENT -->
    <div class="panel main-content">
      <div class="nav-tabs">
        <div class="nav-tab active" onclick="switchTab('users')">USERS</div>
        <div class="nav-tab" onclick="switchTab('brain')">BRAIN</div>
        <div class="nav-tab" onclick="switchTab('buttons')">BUTTONS</div>
        <div class="nav-tab" onclick="switchTab('training')">TRAINING</div>
        <div class="nav-tab" onclick="switchTab('spy')">SPY</div>
        <div class="nav-tab" onclick="switchTab('config')">CONFIG</div>
        <div class="nav-tab" onclick="switchTab('prompts')">PROMPTS</div>
      </div>

      <!-- VIEW 1: USERS -->
      <div id="view-users" class="view-section active">
        <div style="display:flex; gap:10px; margin-bottom:10px;">
          <input type="text" id="user-search" placeholder="Search by Name, Email, or UID..." onkeyup="filterUsers()" style="margin:0; flex:1;">
          <button onclick="loadUsers()" style="width:auto; margin:0;"><i class="fas fa-sync"></i></button>
        </div>
        <div class="table-wrapper">
          <table>
            <thead><tr><th>STATUS</th><th>ALIAS</th><th>EMAIL / ID</th><th>SESSIONS</th><th>ACTIONS</th></tr></thead>
            <tbody id="user-table-body"></tbody>
          </table>
        </div>
      </div>

      <!-- VIEW 2: BRAIN RULES -->
      <div id="view-brain" class="view-section">
        <div style="margin-bottom:15px; border-bottom:1px solid #333; padding-bottom:15px;">
          <h3 style="color:var(--primary);">ADD NEW RULE</h3>
          <input type="text" id="rule-trigger" placeholder="Trigger Phrase (e.g. who are you)">
          <textarea id="rule-answer" placeholder="System Response" rows="3"></textarea>
          <div style="display:flex; gap:10px;">
            <select id="rule-mode" style="flex:1;">
              <option value="exact">Exact Match</option>
              <option value="contains">Contains</option>
              <option value="regex">Regex</option>
            </select>
            <button onclick="addRule()" id="btn-save-rule" class="success">ADD RULE</button>
          </div>
        </div>
        <div class="table-wrapper">
          <table>
            <thead><tr><th>TRIGGER</th><th>RESPONSE</th><th>MODE</th><th>ACTIONS</th></tr></thead>
            <tbody id="rules-table-body"></tbody>
          </table>
        </div>
      </div>

      <!-- VIEW 3: DYNAMIC BUTTONS -->
      <div id="view-buttons" class="view-section">
        <div style="margin-bottom:15px; border-bottom:1px solid #333; padding-bottom:15px;">
          <h3 style="color:var(--primary);">CREATE BUTTON</h3>
          <input type="text" id="btn-title" placeholder="Button Title">
          <input type="text" id="btn-prompt" placeholder="Prompt Text">
          <div style="display:flex; gap:10px;">
            <input type="text" id="btn-icon" placeholder="Icon (e.g. fa-code)" value="fa-star">
            <input type="color" id="btn-color" value="#8b5cf6">
          </div>
          <div style="display:flex; gap:10px; margin-top:5px;">
            <input type="checkbox" id="btn-new" checked> <label style="color:#888;">Mark as NEW</label>
          </div>
          <button onclick="addDynamicButton()" class="success" style="margin-top:10px;">CREATE BUTTON</button>
        </div>
        
        <h3>ACTIVE BUTTONS</h3>
        <div id="buttons-list" style="max-height:300px; overflow-y:auto;"></div>
      </div>

      <!-- VIEW 4: AI TRAINING -->
      <div id="view-training" class="view-section">
        <h3 style="color:var(--primary);">AI TRAINING PROMPT</h3>
        <textarea id="ai-training-text" rows="15" style="font-family:monospace; font-size:0.8rem;"></textarea>
        <div style="display:flex; gap:10px; margin-top:10px;">
          <button onclick="saveTrainingPrompt()" class="success">SAVE TRAINING</button>
          <button onclick="resetTrainingPrompt()" class="warning">RESET TO DEFAULT</button>
        </div>
      </div>

      <!-- VIEW 5: SPY -->
      <div id="view-spy" class="view-section">
        <div class="spy-layout">
          <div class="spy-list" id="spy-user-list"></div>
          <div class="spy-viewer">
            <div style="display:flex; gap:10px; margin-bottom:5px;">
              <select id="spy-session-select" onchange="loadSelectedSession()" style="margin:0; flex:1;">
                <option value="">Select Session...</option>
              </select>
              <button onclick="copyTranscript()" style="width:auto; margin:0;">COPY</button>
              <button onclick="wipeUserHistory()" class="danger" style="width:auto; margin:0;">WIPE</button>
            </div>
            <div id="spy-chat-window" class="chat-container"></div>
            <div style="display:flex; justify-content:space-between; font-size:0.7rem; color:#555; margin-top:5px;">
              <span>Messages: <span id="msg-count">0</span></span>
              <span>Est. Tokens: <span id="token-count">0</span></span>
            </div>
          </div>
        </div>
      </div>

      <!-- VIEW 6: CONFIG -->
      <div id="view-config" class="view-section">
        <h3>API CONFIGURATION</h3>
        <label style="font-size:0.7rem; color:#888;">OPENROUTER API KEY</label>
        <div style="display:flex; gap:5px;">
          <input type="password" id="api-key-input" placeholder="sk-or-v1-...">
          <button onclick="updateApiKey()" class="primary" style="width:auto; margin:0;">SAVE</button>
        </div>

        <h3 style="margin-top:20px;">DEFAULT AI MODEL</h3>
        <select id="default-model">
          <option value="deepseek/deepseek-chat">DarkRoot AI (DeepSeek)</option>
          <option value="google/gemini-2.0-flash-001">Gemini 2.0 Flash</option>
          <option value="meta-llama/llama-3-70b-instruct">Llama 3 70B</option>
          <option value="mistralai/mistral-7b-instruct">Mistral 7B</option>
        </select>
        <button onclick="saveDefaultModel()" class="success" style="margin-top:5px;">SET DEFAULT</button>

        <h3 style="margin-top:20px;">MAX TOKENS</h3>
        <select id="max-tokens">
          <option value="2048">2048 (Normal)</option>
          <option value="4096">4096 (Long)</option>
          <option value="8192">8192 (Very Long)</option>
        </select>
        <button onclick="saveMaxTokens()" class="success" style="margin-top:5px;">SAVE</button>

        <h3 style="margin-top:20px;">SYSTEM LOGS</h3>
        <button onclick="document.getElementById('sys-console').innerHTML='';" class="warning">CLEAR CONSOLE</button>
      </div>

      <!-- VIEW 7: CUSTOM PROMPTS -->
      <div id="view-prompts" class="view-section">
        <div style="margin-bottom:15px;">
          <h3 style="color:var(--primary);">ADD CUSTOM PROMPT</h3>
          <input type="text" id="prompt-title" placeholder="Prompt Title">
          <textarea id="prompt-content" placeholder="Prompt Content" rows="4"></textarea>
          <div style="display:flex; gap:10px;">
            <input type="checkbox" id="prompt-public"> <label style="color:#888;">Make Public</label>
          </div>
          <button onclick="addCustomPrompt()" class="success" style="margin-top:10px;">ADD PROMPT</button>
        </div>
        
        <h3>SAVED PROMPTS</h3>
        <div id="prompts-list" style="max-height:300px; overflow-y:auto;"></div>
      </div>
    </div>

    <!-- STATS -->
    <div class="panel stats-panel">
      <h3>SYSTEM METRICS</h3>
      <canvas id="userChart" style="max-height:120px; margin-bottom:15px;"></canvas>
      
      <h3>RECENT ACTIVITY</h3>
      <div id="recent-activity" style="font-size:0.7rem; color:#888; overflow-y:auto; max-height:200px;">
        <div>• System ready</div>
      </div>

      <h3>SERVER TIME</h3>
      <div id="server-time" style="color:var(--primary); font-size:0.8rem; text-align:center;">--:--:--</div>
    </div>

    <!-- CONSOLE -->
    <div class="panel console-panel" id="sys-console">
      <div class="log-entry log-info">> WAITING FOR COMMAND...</div>
    </div>

  </div>
</div>

<!-- LOGIC -->
<script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-app.js";
  import { getAuth, signInWithEmailAndPassword, signOut, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-auth.js";
  import { getDatabase, ref as rRef, get as rGet, set as rSet, onValue, update, remove } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-database.js";
  import { getFirestore, collection, getDocs, doc, getDoc, updateDoc, deleteDoc, setDoc, query, where, addDoc } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-firestore.js";

  // CONFIGURATION
  const firebaseConfig = {
    apiKey: "AIzaSyBw9l9Zc0sUosH2Vtx1BgY9sqQOFtoQmmI",
    authDomain: "darkroot-ai.firebaseapp.com",
    databaseURL: "https://darkroot-ai-default-rtdb.europe-west1.firebasedatabase.app",
    projectId: "darkroot-ai",
    storageBucket: "darkroot-ai.firebasestorage.app",
    messagingSenderId: "996214418394",
    appId: "1:996214418394:web:24d0fc6457b491eb43aee3"
  };

  const app = initializeApp(firebaseConfig);
  const auth = getAuth(app);
  const db = getDatabase(app);
  const firestore = getFirestore(app);
  const ALLOWED_ADMIN = "davidstha900@gmail.com"; 

  // --- STATE ---
  let allUsers = [];
  let currentSpyUser = null;
  let maintenanceMode = false;
  let currentRules = {};
  let dynamicButtons = [];
  let customPrompts = [];
  let myChart = null;
  let activeTab = 'users';

  // --- UI SWITCHING ---
  window.switchTab = (tabId) => {
    activeTab = tabId;
    document.querySelectorAll('.view-section').forEach(el => el.classList.remove('active'));
    document.getElementById('view-'+tabId).classList.add('active');
    document.querySelectorAll('.nav-tab').forEach(el => el.classList.remove('active'));
    event.currentTarget.classList.add('active');
  };

  function sysLog(msg, type="info") {
    const term = document.getElementById('sys-console');
    const d = document.createElement('div');
    d.className = `log-entry log-${type}`;
    const prefix = type === 'error' ? '✗' : type === 'success' ? '✓' : '>';
    d.innerText = `${prefix} ${msg}`;
    term.appendChild(d); 
    term.scrollTop = term.scrollHeight;
    
    // Add to recent activity
    const activity = document.getElementById('recent-activity');
    const act = document.createElement('div');
    act.innerHTML = `• ${new Date().toLocaleTimeString()} - ${msg}`;
    act.style.color = type === 'error' ? 'var(--danger)' : type === 'success' ? 'var(--success)' : '#888';
    activity.insertBefore(act, activity.firstChild);
    if(activity.children.length > 10) activity.removeChild(activity.lastChild);
  }

  // --- AUTHENTICATION ---
  window.adminLogin = async () => {
    const e = document.getElementById('admin-email').value;
    const p = document.getElementById('admin-password').value;
    try { 
      await signInWithEmailAndPassword(auth, e, p); 
    } 
    catch(err) { 
      document.getElementById('login-msg').innerText = "INVALID CREDENTIALS"; 
      sysLog("LOGIN FAILED", "error"); 
    }
  };
  
  window.logout = () => signOut(auth);

  onAuthStateChanged(auth, (user) => {
    if (user) {
      if(user.email.toLowerCase() !== ALLOWED_ADMIN.toLowerCase()) { 
        signOut(auth); 
        return; 
      }
      document.getElementById('login-overlay').style.display = 'none';
      document.getElementById('dashboard').style.display = 'grid';
      if(window.innerWidth <= 1024) document.getElementById('dashboard').style.display = 'flex';
      sysLog(`OVERLORD CONNECTED: ${user.email}`, "success");
      initData();
      startClock();
    } else {
      document.getElementById('login-overlay').style.display = 'flex';
      document.getElementById('dashboard').style.display = 'none';
    }
  });

  // --- CLOCK ---
  function startClock() {
    setInterval(() => {
      document.getElementById('server-time').innerText = new Date().toLocaleTimeString();
    }, 1000);
  }

  // --- DATA INIT ---
  async function initData() {
    await Promise.all([
      loadApiKey(),
      loadRules(),
      loadUsers(),
      checkMaintenanceStatus(),
      loadNotes(),
      loadDynamicButtons(),
      loadTrainingPrompt(),
      loadCustomPrompts(),
      loadDefaultModel(),
      loadMaxTokens()
    ]);
  }

  // --- 1. SYSTEM CONTROLS ---
  window.sendBroadcast = async () => {
    const msg = document.getElementById('broadcast-msg').value;
    if(!msg) return;
    await rSet(rRef(db, 'system/broadcast'), { 
      message: msg, 
      timestamp: Date.now(),
      sender: auth.currentUser?.email || 'admin'
    });
    sysLog(`BROADCAST SENT: ${msg}`, "warn");
    document.getElementById('broadcast-msg').value = "";
  }

  function checkMaintenanceStatus() {
    onValue(rRef(db, 'config/maintenance'), (snap) => {
      maintenanceMode = snap.val() || false;
      const btn = document.getElementById('btn-maint');
      const ind = document.getElementById('maint-indicator');
      if(maintenanceMode) {
        btn.innerText = "DISABLE MAINTENANCE";
        btn.classList.add('danger');
        btn.classList.remove('warning');
        ind.style.display = "block";
      } else {
        btn.innerText = "ENABLE MAINTENANCE MODE";
        btn.classList.remove('danger');
        btn.classList.add('warning');
        ind.style.display = "none";
      }
    });
  }
  
  window.toggleMaintenance = async () => {
    const newState = !maintenanceMode;
    if(!confirm(newState ? "LOCK SYSTEM? Users will be disconnected." : "UNLOCK SYSTEM?")) return;
    await rSet(rRef(db, 'config/maintenance'), newState);
    sysLog(`MAINTENANCE MODE ${newState ? 'ENABLED' : 'DISABLED'}`, "warn");
  }

  async function loadApiKey() {
    const s = await rGet(rRef(db, 'config/api_key'));
    if(s.exists()) document.getElementById('api-key-input').value = s.val();
  }
  
  window.updateApiKey = async () => {
    await rSet(rRef(db, 'config/api_key'), document.getElementById('api-key-input').value);
    sysLog("API KEY UPDATED", "success");
  }

  async function loadDefaultModel() {
    const s = await rGet(rRef(db, 'config/default_model'));
    if(s.exists()) document.getElementById('default-model').value = s.val();
  }
  
  window.saveDefaultModel = async () => {
    const model = document.getElementById('default-model').value;
    await rSet(rRef(db, 'config/default_model'), model);
    sysLog(`DEFAULT MODEL SET: ${model}`, "success");
  }

  async function loadMaxTokens() {
    const s = await rGet(rRef(db, 'config/max_tokens'));
    if(s.exists()) document.getElementById('max-tokens').value = s.val();
  }
  
  window.saveMaxTokens = async () => {
    const tokens = document.getElementById('max-tokens').value;
    await rSet(rRef(db, 'config/max_tokens'), tokens);
    sysLog(`MAX TOKENS SET: ${tokens}`, "success");
  }

  window.downloadFullBackup = async () => {
    sysLog("GENERATING FULL BACKUP...", "info");
    const data = {
      users: allUsers,
      rules: currentRules,
      buttons: dynamicButtons,
      prompts: customPrompts,
      timestamp: Date.now()
    };
    const blob = new Blob([JSON.stringify(data, null, 2)], {type: 'application/json'});
    const a = document.createElement('a'); 
    a.href = URL.createObjectURL(blob);
    a.download = `darkroot_full_backup_${Date.now()}.json`; 
    a.click();
    sysLog("BACKUP DOWNLOADED", "success");
  }

  window.syncAllData = async () => {
    sysLog("SYNCING ALL DATA...", "info");
    await Promise.all([
      loadUsers(),
      loadRules(),
      loadDynamicButtons(),
      loadCustomPrompts()
    ]);
    sysLog("SYNC COMPLETE", "success");
  }

  function loadNotes() {
    const n = localStorage.getItem('admin_notes');
    if(n) document.getElementById('admin-scratchpad').value = n;
  }
  
  window.saveNotes = () => {
    localStorage.setItem('admin_notes', document.getElementById('admin-scratchpad').value);
  }

  // --- 2. BRAIN RULES ---
  function loadRules() {
    onValue(rRef(db, 'darkroot_admin_rules'), (snap) => {
      const tbody = document.getElementById('rules-table-body');
      tbody.innerHTML = '';
      let data = snap.exists() ? (typeof snap.val() === 'string' ? JSON.parse(snap.val()) : snap.val()) : {};
      currentRules = data;
      let count = 0;
      for (const [trigger, rule] of Object.entries(data)) {
        if(typeof rule === 'object') {
          count++;
          tbody.innerHTML += `<tr>
            <td style="color:#fff;">${trigger}</td>
            <td style="color:#888;">${rule.response.substring(0,40)}...</td>
            <td>${rule.mode || 'exact'}</td>
            <td>
              <button class="danger" style="margin:0;padding:2px 5px;" onclick="deleteRule('${trigger}')">X</button>
            </td>
          </tr>`;
        }
      }
      document.getElementById('stat-rules').innerText = count;
    });
  }

  window.addRule = async () => {
    const trigger = document.getElementById('rule-trigger').value.toLowerCase().trim();
    const response = document.getElementById('rule-answer').value.trim();
    const mode = document.getElementById('rule-mode').value;
    
    if(!trigger || !response) return;
    
    currentRules[trigger] = { response, mode, created: Date.now() };
    await rSet(rRef(db, 'darkroot_admin_rules'), currentRules);
    sysLog(`RULE ADDED: ${trigger}`, "success");
    document.getElementById('rule-trigger').value = "";
    document.getElementById('rule-answer').value = "";
  };

  window.deleteRule = async (trigger) => {
    if(!confirm("Delete this rule?")) return;
    delete currentRules[trigger];
    await rSet(rRef(db, 'darkroot_admin_rules'), currentRules);
    sysLog(`RULE DELETED: ${trigger}`, "warn");
  }

  // --- 3. DYNAMIC BUTTONS ---
  async function loadDynamicButtons() {
    try {
      const docRef = doc(firestore, "system", "buttons_config");
      const docSnap = await getDoc(docRef);
      
      if (docSnap.exists()) {
        const data = docSnap.data();
        dynamicButtons = data.buttons || [];
      } else {
        dynamicButtons = [];
      }
      
      renderButtonsList();
      document.getElementById('stat-buttons').innerText = dynamicButtons.length;
    } catch(e) {
      console.error("Error loading buttons:", e);
      dynamicButtons = [];
    }
  }

  window.addDynamicButton = async () => {
    const title = document.getElementById('btn-title').value.trim();
    const prompt = document.getElementById('btn-prompt').value.trim();
    const icon = document.getElementById('btn-icon').value.trim() || 'fa-star';
    const color = document.getElementById('btn-color').value;
    const isNew = document.getElementById('btn-new').checked;

    if(!title || !prompt) {
      alert("Title and prompt required");
      return;
    }

    const newButton = {
      id: 'btn_' + Date.now(),
      title: title,
      prompt: prompt,
      icon: icon,
      color: color,
      bgColor: `linear-gradient(135deg, ${color}, ${color}dd)`,
      createdAt: Date.now(),
      isNew: isNew
    };

    dynamicButtons.unshift(newButton);
    
    await setDoc(doc(firestore, "system", "buttons_config"), {
      buttons: dynamicButtons,
      lastUpdated: Date.now()
    });

    renderButtonsList();
    document.getElementById('stat-buttons').innerText = dynamicButtons.length;
    
    // Clear inputs
    document.getElementById('btn-title').value = '';
    document.getElementById('btn-prompt').value = '';
    document.getElementById('btn-icon').value = 'fa-star';
    document.getElementById('btn-new').checked = true;
    
    sysLog(`BUTTON ADDED: ${title}`, "success");
  }

  window.deleteButton = async (id) => {
    if(!confirm("Delete this button?")) return;
    
    dynamicButtons = dynamicButtons.filter(b => b.id !== id);
    
    await setDoc(doc(firestore, "system", "buttons_config"), {
      buttons: dynamicButtons,
      lastUpdated: Date.now()
    });

    renderButtonsList();
    document.getElementById('stat-buttons').innerText = dynamicButtons.length;
    sysLog("BUTTON DELETED", "warn");
  }

  function renderButtonsList() {
    const list = document.getElementById('buttons-list');
    list.innerHTML = '';
    
    if(dynamicButtons.length === 0) {
      list.innerHTML = '<div style="color:#666; text-align:center; padding:20px;">No buttons configured</div>';
      return;
    }

    dynamicButtons.forEach(btn => {
      const div = document.createElement('div');
      div.style.marginBottom = '15px';
      div.style.padding = '10px';
      div.style.background = '#080808';
      div.style.border = '1px solid #333';
      div.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:10px;">
          <div style="display:flex; align-items:center; gap:10px;">
            <i class="fas ${btn.icon}" style="color:${btn.color};"></i>
            <strong style="color:#fff;">${btn.title}</strong>
            ${btn.isNew ? '<span class="badge" style="background:var(--primary); color:#000;">NEW</span>' : ''}
          </div>
          <button class="danger" style="padding:2px 5px;" onclick="deleteButton('${btn.id}')">X</button>
        </div>
        <div style="color:#888; font-size:0.7rem;">${btn.prompt}</div>
      `;
      list.appendChild(div);
    });
  }

  // --- 4. AI TRAINING ---
  async function loadTrainingPrompt() {
    try {
      const docRef = doc(firestore, "system", "ai_config");
      const docSnap = await getDoc(docRef);
      
      if (docSnap.exists()) {
        const data = docSnap.data();
        document.getElementById('ai-training-text').value = data.training_prompt || getDefaultTrainingText();
      } else {
        document.getElementById('ai-training-text').value = getDefaultTrainingText();
      }
    } catch(e) {
      console.error("Error loading training:", e);
      document.getElementById('ai-training-text').value = getDefaultTrainingText();
    }
  }

  window.saveTrainingPrompt = async () => {
    const text = document.getElementById('ai-training-text').value;
    
    await setDoc(doc(firestore, "system", "ai_config"), {
      training_prompt: text,
      lastUpdated: Date.now()
    }, { merge: true });

    sysLog("AI TRAINING PROMPT UPDATED", "success");
  }

  window.resetTrainingPrompt = () => {
    if(confirm("Reset to default training prompt?")) {
      document.getElementById('ai-training-text').value = getDefaultTrainingText();
    }
  }

  function getDefaultTrainingText() {
    return `You are DarkRoot AI, an advanced artificial intelligence assistant specialized in:
Cybersecurity
Ethical Hacking
Programming & Software Development
Technical Problem-Solving

Core Behavior
- Provide clear, structured, and in-depth responses
- Use proper Markdown formatting
- Apply syntax highlighting for all code blocks
- Be direct, precise, and technically accurate

Cybersecurity Rules (Strict)
- Discuss only legal and ethical cybersecurity practices
- Clearly warn against illegal actions
- Focus on defensive security, education, and best practices

Coding Rules
- Provide complete, runnable code examples
- Explain logic step-by-step when complexity is high
- Use clean, modern, and readable code
- Follow industry standards and best practices

Ethics Emphasis
- Always reinforce legal responsibility
- Promote learning, security awareness, and ethical development
- Never encourage harm, exploitation, or illegal access`;
  }

  // --- 5. CUSTOM PROMPTS ---
  async function loadCustomPrompts() {
    try {
      const promptsRef = query(collection(firestore, "custom_prompts"));
      const snapshot = await getDocs(promptsRef);
      customPrompts = [];
      snapshot.forEach(doc => {
        customPrompts.push({ id: doc.id, ...doc.data() });
      });
      renderPromptsList();
    } catch(e) {
      console.error("Error loading prompts:", e);
      customPrompts = [];
    }
  }

  window.addCustomPrompt = async () => {
    const title = document.getElementById('prompt-title').value.trim();
    const content = document.getElementById('prompt-content').value.trim();
    const isPublic = document.getElementById('prompt-public').checked;

    if(!title || !content) {
      alert("Title and content required");
      return;
    }

    await addDoc(collection(firestore, "custom_prompts"), {
      title: title,
      content: content,
      isPublic: isPublic,
      createdBy: auth.currentUser?.uid || "admin",
      createdAt: new Date().toISOString()
    });

    document.getElementById('prompt-title').value = '';
    document.getElementById('prompt-content').value = '';
    document.getElementById('prompt-public').checked = false;

    await loadCustomPrompts();
    sysLog(`PROMPT ADDED: ${title}`, "success");
  }

  window.deletePrompt = async (id) => {
    if(!confirm("Delete this prompt?")) return;
    await deleteDoc(doc(firestore, "custom_prompts", id));
    await loadCustomPrompts();
    sysLog("PROMPT DELETED", "warn");
  }

  function renderPromptsList() {
    const list = document.getElementById('prompts-list');
    list.innerHTML = '';

    if(customPrompts.length === 0) {
      list.innerHTML = '<div style="color:#666; text-align:center; padding:20px;">No custom prompts</div>';
      return;
    }

    customPrompts.forEach(prompt => {
      const div = document.createElement('div');
      div.style.marginBottom = '15px';
      div.style.padding = '10px';
      div.style.background = '#080808';
      div.style.border = '1px solid #333';
      div.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:5px;">
          <strong style="color:var(--primary);">${prompt.title}</strong>
          ${prompt.isPublic ? '<span class="badge" style="background:var(--info);">PUBLIC</span>' : ''}
        </div>
        <div style="color:#888; font-size:0.7rem; margin-bottom:10px;">${prompt.content.substring(0,100)}${prompt.content.length > 100 ? '...' : ''}</div>
        <button class="danger" style="padding:2px 5px;" onclick="deletePrompt('${prompt.id}')">DELETE</button>
      `;
      list.appendChild(div);
    });
  }

  // --- 6. USER MANAGEMENT ---
  window.loadUsers = async () => {
    sysLog("FETCHING USERS...", "info");
    const snap = await getDocs(collection(firestore, "users"));
    allUsers = [];
    let totalSessions = 0;
    
    snap.forEach(d => { 
      const user = {uid: d.id, ...d.data()};
      allUsers.push(user);
      if(user.sessions) totalSessions += user.sessions.length;
    });
    
    renderUserTable(allUsers);
    document.getElementById('stat-total').innerText = allUsers.length;
    document.getElementById('stat-sessions').innerText = totalSessions;
    
    // Chart Update
    const banned = allUsers.filter(u => u.banned).length;
    updateChart(allUsers.length, banned);
    
    sysLog("USER LIST REFRESHED", "success");
  }

  function renderUserTable(users) {
    const tbody = document.getElementById('user-table-body');
    const spyList = document.getElementById('spy-user-list');
    tbody.innerHTML = ''; 
    spyList.innerHTML = '';

    users.sort((a,b) => (b.lastActive || 0) - (a.lastActive || 0)).forEach(u => {
      const alias = u.adminLabel || u.displayName || "User";
      const banned = u.banned ? '<span class="badge badge-banned">BANNED</span>' : '<span class="badge badge-active">ACTIVE</span>';
      const sessionCount = u.sessions?.length || 0;
      
      // Table Row
      tbody.innerHTML += `
        <tr>
          <td>${banned}</td>
          <td style="color:${u.adminLabel?'var(--primary)':'#888'}">${alias}</td>
          <td style="font-family:monospace; color:#666;">${u.email || u.uid.substring(0,8)}...</td>
          <td>${sessionCount}</td>
          <td>
            <button style="width:auto; margin:0;" onclick="editAlias('${u.uid}', '${u.adminLabel||''}')"><i class="fas fa-pen"></i></button>
            <button style="width:auto; margin:0;" onclick="inspectUser('${u.uid}')"><i class="fas fa-eye"></i></button>
            <button class="${u.banned?'success':'danger'}" style="width:auto; margin:0;" onclick="toggleBan('${u.uid}', ${u.banned})">
              <i class="fas ${u.banned?'fa-unlock':'fa-ban'}"></i>
            </button>
          </td>
        </tr>`;

      // Spy List Item
      const item = document.createElement('div');
      item.style.padding = "8px"; 
      item.style.borderBottom = "1px solid #111"; 
      item.style.cursor = "pointer";
      item.style.display = "flex";
      item.style.flexDirection = "column";
      item.innerHTML = `
        <div style="font-weight:bold; color:${u.adminLabel?'#fff':'#888'}">${alias}</div>
        <div style="font-size:0.6rem; color:#444;">${u.uid.substring(0,10)}...</div>
        <div style="font-size:0.6rem; color:#666;">${sessionCount} sessions</div>
      `;
      item.onclick = () => inspectUser(u.uid);
      spyList.appendChild(item);
    });
  }

  window.toggleBan = async (uid, currentStatus) => {
    if(!confirm(currentStatus ? "Unban user?" : "BAN USER? They will lose access.")) return;
    await updateDoc(doc(firestore, "users", uid), { banned: !currentStatus });
    sysLog(`USER ${uid.substring(0,8)}... ${currentStatus ? 'UNBANNED' : 'BANNED'}`, "warn");
    loadUsers();
  }

  window.editAlias = async (uid, old) => {
    const n = prompt("Set Admin Alias:", old);
    if(n !== null) {
      await updateDoc(doc(firestore, "users", uid), { adminLabel: n });
      sysLog(`ALIAS UPDATED: ${n}`, "success");
      loadUsers();
    }
  }

  window.filterUsers = () => {
    const q = document.getElementById('user-search').value.toLowerCase();
    renderUserTable(allUsers.filter(u => 
      (u.email && u.email.toLowerCase().includes(q)) || 
      u.uid.toLowerCase().includes(q) ||
      (u.adminLabel && u.adminLabel.toLowerCase().includes(q)) ||
      (u.displayName && u.displayName.toLowerCase().includes(q))
    ));
  }

  // --- 7. SPY MODE ---
  window.inspectUser = async (uid) => {
    switchTab('spy');
    currentSpyUser = uid;
    sysLog(`SPYING ON: ${uid.substring(0,8)}...`, "warn");
    
    const sel = document.getElementById('spy-session-select');
    sel.innerHTML = '<option>Loading History...</option>';
    document.getElementById('spy-chat-window').innerHTML = '';
    document.getElementById('msg-count').innerText = '0';
    document.getElementById('token-count').innerText = '0';

    try {
      const d = await getDoc(doc(firestore, "users", uid));
      if(d.exists() && d.data().sessions) {
        sel.innerHTML = '<option value="">Select Session...</option>';
        window.spySessions = d.data().sessions;
        window.spySessions.sort((a,b) => b.timestamp - a.timestamp).forEach((s, i) => {
          const date = new Date(s.timestamp).toLocaleString();
          sel.innerHTML += `<option value="${i}">${date} | ${(s.title || 'Chat').substring(0,30)}</option>`;
        });
      } else { 
        sel.innerHTML = '<option>No History</option>'; 
      }
    } catch(e) { 
      sysLog("FETCH ERROR", "error"); 
    }
  }

  window.loadSelectedSession = () => {
    const index = document.getElementById('spy-session-select').value;
    const container = document.getElementById('spy-chat-window');
    container.innerHTML = '';
    let tokens = 0;
    let msgCount = 0;
    
    if(index !== "" && window.spySessions && window.spySessions[index]) {
      const session = window.spySessions[index];
      if(session.messages) {
        session.messages.forEach(m => {
          if(m.role !== 'system') {
            msgCount++;
            tokens += Math.ceil(m.content.length / 4);
            
            const div = document.createElement('div');
            div.className = `msg-bubble ${m.role === 'user' ? 'msg-user' : 'msg-ai'}`;
            
            // Format content
            if(m.role === 'ai' && m.content.includes('```')) {
              div.innerHTML = marked.parse(m.content);
              setTimeout(() => {
                div.querySelectorAll('pre code').forEach(block => hljs.highlightElement(block));
              }, 50);
            } else {
              div.textContent = m.content;
            }
            
            container.appendChild(div);
          }
        });
      }
    }
    
    document.getElementById('msg-count').innerText = msgCount;
    document.getElementById('token-count').innerText = Math.floor(tokens);
    container.scrollTop = container.scrollHeight;
  }

  window.wipeUserHistory = async () => {
    if(!currentSpyUser || !confirm("PERMANENTLY DELETE ALL HISTORY FOR THIS USER?")) return;
    await updateDoc(doc(firestore, "users", currentSpyUser), { sessions: [] });
    document.getElementById('spy-chat-window').innerHTML = "<div style='text-align:center; color:red; padding:20px;'>HISTORY WIPED</div>";
    document.getElementById('spy-session-select').innerHTML = '<option>No History</option>';
    sysLog(`WIPED HISTORY FOR ${currentSpyUser.substring(0,8)}...`, "error");
  }

  window.copyTranscript = () => {
    const text = document.getElementById('spy-chat-window').innerText;
    navigator.clipboard.writeText(text);
    sysLog("TRANSCRIPT COPIED", "info");
  }

  // --- 8. CHART ---
  function updateChart(total, banned) {
    const ctx = document.getElementById('userChart').getContext('2d');
    if(myChart) myChart.destroy();
    myChart = new Chart(ctx, {
      type: 'doughnut',
      data: { 
        labels: ['Active', 'Banned'], 
        datasets: [{ 
          data: [total-banned, banned], 
          backgroundColor: ['#00ff41', '#ff3333'], 
          borderWidth: 0 
        }] 
      },
      options: { 
        responsive: true, 
        maintainAspectRatio: false,
        plugins: {
          legend: { 
            position: 'right', 
            labels: { color: '#888', font: { size: 8 } } 
          }
        }, 
        cutout: '70%' 
      }
    });
  }

  // MATRIX ANIMATION
  const cvs = document.getElementById('matrix-canvas'), ctx = cvs.getContext('2d');
  cvs.width = window.innerWidth; 
  cvs.height = window.innerHeight;
  const cols = Math.floor(cvs.width/20), ypos = Array(cols).fill(0);
  
  setInterval(() => {
    ctx.fillStyle = '#0001'; 
    ctx.fillRect(0,0,cvs.width,cvs.height);
    ctx.fillStyle = '#0f0'; 
    ctx.font = '15pt monospace';
    ypos.forEach((y,i) => {
      const t = String.fromCharCode(Math.random()*128);
      ctx.fillText(t, i*20, y);
      ypos[i] = y > 100+Math.random()*10000 ? 0 : y+20;
    });
  }, 50);

  // EXPORT GLOBALS
  window.addRule = addRule;
  window.deleteRule = deleteRule;
  window.loadUsers = loadUsers;
  window.editAlias = editAlias;
  window.toggleBan = toggleBan;
  window.inspectUser = inspectUser;
  window.loadSelectedSession = loadSelectedSession;
  window.wipeUserHistory = wipeUserHistory;
  window.copyTranscript = copyTranscript;
  window.filterUsers = filterUsers;
  window.addDynamicButton = addDynamicButton;
  window.deleteButton = deleteButton;
  window.saveTrainingPrompt = saveTrainingPrompt;
  window.resetTrainingPrompt = resetTrainingPrompt;
  window.addCustomPrompt = addCustomPrompt;
  window.deletePrompt = deletePrompt;
</script>
</body>
</html>