 <img width="1024" height="1024" alt="file_0000000012d461f4a951b905b84871c2" src="https://github.com/user-attachments/assets/49aae59c-e11a-448f-8dc5-3750e86c840f" />
📱 KC CRUIZER MD
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>WhatsApp Bot — README</title>
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--muted:#98a0b3;--accent:#7c3aed;--glass:rgba(255,255,255,0.04)}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,'Segoe UI',Roboto,'Helvetica Neue',Arial}
    body{background:linear-gradient(180deg,#071021 0%, #07172a 100%);color:#e6eef8;display:flex;align-items:center;justify-content:center;padding:36px}
    .wrap{width:100%;max-width:980px}

    header{display:flex;gap:18px;align-items:center;margin-bottom:22px}
    .logo{width:76px;height:76px;border-radius:14px;background:linear-gradient(135deg,var(--accent),#0ea5a6);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:22px;box-shadow:0 8px 30px rgba(0,0,0,0.6)}
    h1{margin:0;font-size:22px}
    p.lead{margin:6px 0 0;color:var(--muted)}

    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border-radius:12px;padding:20px;box-shadow:0 6px 24px rgba(2,6,23,0.7);border:1px solid rgba(255,255,255,0.03)}

    .grid{display:grid;grid-template-columns:2fr 1fr;gap:16px;margin-top:18px}
    pre.cmd{background:var(--card);padding:14px;border-radius:8px;color:#d6e6ff;margin:0;overflow:auto;font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, 'Roboto Mono', monospace}

    .buttons{display:flex;flex-wrap:wrap;gap:10px;margin-top:12px}
    .btn{display:inline-flex;align-items:center;gap:10px;padding:10px 14px;border-radius:10px;background:var(--glass);border:1px solid rgba(255,255,255,0.04);cursor:pointer;text-decoration:none;color:inherit;font-weight:600}
    .btn.primary{background:linear-gradient(90deg,var(--accent),#5eead4);color:#07122a}
    .btn.ghost{background:transparent;border:1px dashed rgba(255,255,255,0.06)}

    section h2{margin:0 0 10px;font-size:16px}
    .muted{color:var(--muted);font-size:13px}

    .list{display:flex;flex-direction:column;gap:8px}
    .kbd{background:#051225;padding:6px 8px;border-radius:6px;font-family:ui-monospace,monospace;margin-left:8px}

    footer{margin-top:18px;color:var(--muted);font-size:13px}

    @media (max-width:880px){.grid{grid-template-columns:1fr}.logo{width:64px;height:64px}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">WA</div>
      <div>
        <h1>WhatsApp Bot — Modular (Node.js + Baileys)</h1>
        <p class="lead">AI chat, stickers, anti-link, tagall, scheduler, games — production-ready template.</p>
      </div>
    </header>

    <div class="card">
      <div style="display:flex;justify-content:space-between;gap:16px;align-items:flex-start;flex-wrap:wrap">
        <div style="min-width:0;flex:1">
          <section>
            <h2>Quick actions</h2>
            <div class="buttons">
              <a class="btn primary" id="deploy-render" href="#" target="_blank">🚀 Deploy on Render</a>
              <a class="btn primary" id="deploy-railway" href="#" target="_blank">🚂 Deploy on Railway</a>
              <a class="btn ghost" id="fork" href="#" target="_blank">🍴 Fork on GitHub</a>
              <a class="btn" id="contact" href="mailto:you@example.com">✉️ Contact</a>
            </div>
            <p class="muted" style="margin-top:10px">Replace the buttons' links with your repo/deploy URLs before publishing.</p>
          </section>

          <section style="margin-top:14px">
            <h2>Local quick setup</h2>
            <div class="list">
              <div class="muted">Clone & install:</div>
              <pre class="cmd" id="cmd-clone">git clone https://github.com/OWNER/REPO.git
cd REPO
npm install
cp .env.example .env
# edit .env and add keys
npm run start</pre>
              <div class="muted">Use this to keep the bot running (optional): <span class="kbd">pm2 start src/index.js --name whatsapp-bot</span></div>
            </div>
          </section>

          <section style="margin-top:14px">
            <h2>Deploy to Render</h2>
            <ol class="muted">
              <li>Push repo to GitHub.</li>
              <li>On Render: New &rarr; Web Service &rarr; Connect GitHub repo.</li>
              <li>Build command: <code>npm install</code>. Start command: <code>npm run start</code>.</li>
              <li>Set environment variables in Render dashboard (OWNER_NUMBER, GEMINI_KEY, etc.).</li>
              <li>Deploy — view logs to scan QR or get pairing code.</li>
            </ol>
          </section>

          <section style="margin-top:14px">
            <h2>Deploy to Railway</h2>
            <ol class="muted">
              <li>Create project &rarr; Deploy from GitHub.</li>
              <li>Ensure start command is <code>npm run start</code>.</li>
              <li>Add environment variables in Railway "Variables".</li>
              <li>Deploy and check logs for QR / pairing code.</li>
            </ol>
          </section>

        </div>

        <aside style="width:320px;max-width:40%;min-width:220px">
          <section>
            <h2>Status & Tips</h2>
            <p class="muted">Keep <code>auth/</code> persisted on the host. If you lose it you must re-scan QR. Always store secrets in platform env settings.</p>
          </section>

          <section style="margin-top:12px">
            <h2>Commands cheat-sheet</h2>
            <pre class="cmd">!help
!sticker (reply to media)
!ai &lt;prompt&gt;
!tagall
!hidetag &lt;text&gt;
!antilink on|off
!anticall on|off
!antidelete on|off</pre>
          </section>

        </aside>
      </div>

      <footer>
        Created for <strong>KÇ</strong>. Feel free to edit links & contact info. Want a GitHub Actions auto-deploy script? Click contact.
      </footer>
    </div>
  </div>

  <script>
    // Replace these with your actual repo & deploy URLs
    const REPO = 'https://github.com/OWNER/REPO';
    const RENDER_DEPLOY = `https://dashboard.render.com/deploy?repo=${encodeURIComponent(REPO)}`;
    const RAILWAY_DEPLOY = `https://railway.app/new?template=${encodeURIComponent(REPO)}`;

    document.getElementById('deploy-render').href = RENDER_DEPLOY;
    document.getElementById('deploy-railway').href = RAILWAY_DEPLOY;
    document.getElementById('fork').href = REPO + '/fork';

    // Copy command helper when clicking the clone block
    document.getElementById('cmd-clone').addEventListener('click', async () => {
      try { await navigator.clipboard.writeText(document.getElementById('cmd-clone').innerText); alert('Copied to clipboard'); }
      catch(e){ console.log(e); }
    });
  </script>
</body>
</html>


