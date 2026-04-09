<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NepaliCoder Apps</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #F7F4EE;
      --surface: #FFFFFF;
      --surface2: #F0EDE6;
      --text: #1A1714;
      --text-muted: #7A7570;
      --text-light: #B0ABA5;
      --accent: #1D4E2A;
      --accent-light: #E8F4EB;
      --accent-mid: #3A8C4F;
      --border: rgba(26,23,20,0.1);
      --border-strong: rgba(26,23,20,0.2);
      --radius: 16px;
      --radius-sm: 10px;
      --shadow: 0 2px 16px rgba(0,0,0,0.07), 0 1px 3px rgba(0,0,0,0.04);
    }

    @media (prefers-color-scheme: dark) {
      :root {
        --bg: #141210;
        --surface: #1E1C1A;
        --surface2: #272420;
        --text: #F0ECE6;
        --text-muted: #8A8480;
        --text-light: #5A5550;
        --accent: #5CB878;
        --accent-light: #1A2E1D;
        --accent-mid: #4CA065;
        --border: rgba(240,236,230,0.08);
        --border-strong: rgba(240,236,230,0.15);
        --shadow: 0 2px 16px rgba(0,0,0,0.3);
      }
    }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
    }

    header {
      padding: 2.5rem 1.5rem 1.5rem;
      max-width: 900px;
      margin: 0 auto;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--accent-mid);
    }

    .brand-name {
      font-family: 'DM Serif Display', serif;
      font-size: 1.1rem;
      color: var(--text-muted);
      letter-spacing: 0.02em;
    }

    .hero {
      padding: 2rem 1.5rem 1rem;
      max-width: 900px;
      margin: 0 auto;
    }

    .hero h1 {
      font-family: 'DM Serif Display', serif;
      font-size: clamp(2rem, 6vw, 3.2rem);
      line-height: 1.15;
      letter-spacing: -0.01em;
      margin-bottom: 0.75rem;
    }

    .hero h1 em {
      font-style: italic;
      color: var(--accent-mid);
    }

    .hero p {
      font-size: 1rem;
      color: var(--text-muted);
      line-height: 1.65;
      max-width: 480px;
    }

    main {
      padding: 2rem 1.5rem 4rem;
      max-width: 900px;
      margin: 0 auto;
    }

    .section-label {
      font-size: 0.72rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-light);
      margin-bottom: 1rem;
    }

    /* ── App Grid ── */
    .apps-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(min(100%, 360px), 1fr));
      gap: 1.25rem;
    }

    .app-card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 1.75rem;
      box-shadow: var(--shadow);
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      transition: border-color 0.2s, transform 0.2s;
    }

    .app-card:hover {
      border-color: var(--border-strong);
      transform: translateY(-2px);
    }

    /* App header row */
    .app-header {
      display: flex;
      align-items: flex-start;
      gap: 1rem;
    }

    .app-icon {
      width: 60px;
      height: 60px;
      border-radius: 14px;
      background: var(--accent-light);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      border: 1px solid var(--border);
    }

    .app-icon svg {
      width: 30px;
      height: 30px;
    }

    .app-meta {
      flex: 1;
      min-width: 0;
    }

    .app-name {
      font-family: 'DM Serif Display', serif;
      font-size: 1.3rem;
      line-height: 1.2;
      margin-bottom: 0.3rem;
    }

    .app-tagline {
      font-size: 0.85rem;
      color: var(--text-muted);
      line-height: 1.5;
    }

    .app-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 0.5rem;
    }

    .badge {
      font-size: 0.7rem;
      font-weight: 500;
      padding: 3px 8px;
      border-radius: 20px;
      background: var(--accent-light);
      color: var(--accent-mid);
      border: 1px solid rgba(58,140,79,0.2);
    }

    /* Body content inside card */
    .app-body {
      display: grid;
      grid-template-columns: auto 1fr;
      gap: 1.5rem;
      align-items: start;
    }

    @media (max-width: 440px) {
      .app-body {
        grid-template-columns: 1fr;
      }
      .qr-col { display: flex; justify-content: center; }
    }

    .qr-col {}

    .qr-wrapper {
      background: #FFFFFF;
      border: 1px solid var(--border);
      border-radius: var(--radius-sm);
      padding: 10px;
      display: inline-flex;
      flex-direction: column;
      align-items: center;
      gap: 6px;
    }

    .qr-wrapper canvas,
    .qr-wrapper img {
      display: block;
      border-radius: 4px;
    }

    .qr-label {
      font-size: 0.65rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      color: var(--text-light);
    }

    .info-col {
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }

    .info-row {
      display: flex;
      flex-direction: column;
      gap: 3px;
    }

    .info-key {
      font-size: 0.7rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--text-light);
    }

    .info-val {
      font-size: 0.88rem;
      color: var(--text-muted);
      word-break: break-all;
    }

    /* CTA buttons */
    .app-actions {
      display: flex;
      gap: 0.75rem;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 0.65rem 1.1rem;
      border-radius: var(--radius-sm);
      font-family: 'DM Sans', sans-serif;
      font-size: 0.88rem;
      font-weight: 500;
      text-decoration: none;
      transition: all 0.18s;
      cursor: pointer;
      border: none;
      flex: 1;
      justify-content: center;
      min-width: 130px;
    }

    .btn-primary {
      background: var(--accent);
      color: #FFFFFF;
    }

    .btn-primary:hover {
      background: var(--accent-mid);
      transform: translateY(-1px);
    }

    .btn-secondary {
      background: var(--surface2);
      color: var(--text);
      border: 1px solid var(--border-strong);
    }

    .btn-secondary:hover {
      background: var(--accent-light);
      border-color: var(--accent-mid);
      color: var(--accent-mid);
      transform: translateY(-1px);
    }

    .btn svg {
      width: 16px;
      height: 16px;
      flex-shrink: 0;
    }

    /* footer */
    footer {
      text-align: center;
      padding: 2rem 1.5rem;
      font-size: 0.8rem;
      color: var(--text-light);
      border-top: 1px solid var(--border);
    }

    footer a {
      color: var(--accent-mid);
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div class="hero">
    <h1>Apps built with<br /><em>purpose &amp; care</em></h1>
    <p>Independent apps for Android — simple, focused, and offline-first. Scan the QR code or tap to get started.</p>
  </div>

  <main>
    <p class="section-label">Available Apps</p>

    <!-- ══ APPS GRID — add more .app-card items here as you build more apps ══ -->
    <div class="apps-grid" id="appsGrid">

      <!-- ── App 1: Holy Bible KJV ── -->
      <div class="app-card">
        <div class="app-header">
          <div class="app-icon">
            <!-- Book / Bible icon -->
            <svg viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect x="4" y="4" width="16" height="22" rx="2" fill="none" stroke="#3A8C4F" stroke-width="1.6"/>
              <rect x="8" y="4" width="12" height="22" rx="2" fill="#E8F4EB" stroke="#3A8C4F" stroke-width="1.4"/>
              <line x1="12" y1="9" x2="17" y2="9" stroke="#3A8C4F" stroke-width="1.2" stroke-linecap="round"/>
              <line x1="14.5" y1="6.5" x2="14.5" y2="11.5" stroke="#3A8C4F" stroke-width="1.2" stroke-linecap="round"/>
              <line x1="11" y1="14" x2="18" y2="14" stroke="#3A8C4F" stroke-width="1" stroke-linecap="round" stroke-dasharray="1.5 1.5"/>
              <line x1="11" y1="17" x2="18" y2="17" stroke="#3A8C4F" stroke-width="1" stroke-linecap="round" stroke-dasharray="1.5 1.5"/>
              <line x1="11" y1="20" x2="15" y2="20" stroke="#3A8C4F" stroke-width="1" stroke-linecap="round" stroke-dasharray="1.5 1.5"/>
            </svg>
          </div>
          <div class="app-meta">
            <div class="app-name">Holy Bible KJV</div>
            <div class="app-tagline">Complete King James Version — read, search, bookmark &amp; highlight scripture offline.</div>
            <div class="app-badges">
              <span class="badge">Free</span>
              <span class="badge">Offline</span>
              <span class="badge">Android</span>
            </div>
          </div>
        </div>

        <div class="app-body">
          <div class="qr-col">
            <div class="qr-wrapper">
              <div id="qr-bible"></div>
              <span class="qr-label">Scan to open</span>
            </div>
          </div>
          <div class="info-col">
            <div class="info-row">
              <span class="info-key">Package</span>
              <span class="info-val">com.nepalicoder</span>
            </div>
            <div class="info-row">
              <span class="info-key">Platform</span>
              <span class="info-val">Android (Google Play)</span>
            </div>
            <div class="info-row">
              <span class="info-key">Features</span>
              <span class="info-val">Daily verse, TTS, bookmarks, highlights, dark mode</span>
            </div>
          </div>
        </div>

        <div class="app-actions">
          <a class="btn btn-primary"
             href="https://play.google.com/store/apps/details?id=com.nepalicoder"
             target="_blank" rel="noopener">
            <!-- Play icon -->
            <svg viewBox="0 0 16 16" fill="currentColor"><path d="M3 2.5l10 5.5-10 5.5V2.5z"/></svg>
            Open on Play Store
          </a>
          <a class="btn btn-secondary"
             href="https://play.google.com/store/apps/details?id=com.nepalicoder"
             target="_blank" rel="noopener">
            <!-- Download icon -->
            <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round">
              <path d="M8 2v8M5 7l3 3 3-3"/><path d="M2 12h12"/>
            </svg>
            Download APK
          </a>
        </div>
      </div>

      <!-- ══ TEMPLATE: Copy the block below to add a new app ══
      <div class="app-card">
        <div class="app-header">
          <div class="app-icon">
            (your SVG icon here)
          </div>
          <div class="app-meta">
            <div class="app-name">App Name</div>
            <div class="app-tagline">Short description of the app.</div>
            <div class="app-badges">
              <span class="badge">Free</span>
            </div>
          </div>
        </div>
        <div class="app-body">
          <div class="qr-col">
            <div class="qr-wrapper">
              <div id="qr-APPID"></div>
              <span class="qr-label">Scan to open</span>
            </div>
          </div>
          <div class="info-col">
            <div class="info-row"><span class="info-key">Package</span><span class="info-val">com.nepalicoder.appname</span></div>
            <div class="info-row"><span class="info-key">Platform</span><span class="info-val">Android (Google Play)</span></div>
          </div>
        </div>
        <div class="app-actions">
          <a class="btn btn-primary" href="YOUR_PLAY_STORE_LINK" target="_blank" rel="noopener">
            <svg viewBox="0 0 16 16" fill="currentColor"><path d="M3 2.5l10 5.5-10 5.5V2.5z"/></svg>
            Open on Play Store
          </a>
          <a class="btn btn-secondary" href="YOUR_PLAY_STORE_LINK" target="_blank" rel="noopener">
            <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M8 2v8M5 7l3 3 3-3"/><path d="M2 12h12"/></svg>
            Download APK
          </a>
        </div>
      </div>
      ══ END TEMPLATE ══ -->

    </div>
  </main>

  <footer>
    Built by <a href="https://play.google.com/store/apps/dev?id=com.nepalicoder" target="_blank" rel="noopener">NepaliCoder</a> &mdash; independent Android developer
  </footer>

  <script>
    new QRCode(document.getElementById("qr-bible"), {
      text: "https://play.google.com/store/apps/details?id=com.nepalicoder",
      width: 120,
      height: 120,
      colorDark: "#1A1714",
      colorLight: "#FFFFFF",
      correctLevel: QRCode.CorrectLevel.M
    });
  </script>
</body>
</html>
