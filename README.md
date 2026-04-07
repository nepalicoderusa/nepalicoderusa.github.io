<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Privacy Policy – Holy Bible KJV</title>
  <link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Cinzel:wght@400;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --parchment: #f5ede0;
      --parchment-dark: #e8d9c4;
      --ink: #2b1d0e;
      --ink-soft: #4a3520;
      --gold: #b8860b;
      --gold-light: #d4a843;
      --red: #8b1a1a;
      --border: #c9a96e;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background-color: var(--parchment);
      color: var(--ink);
      font-family: 'EB Garamond', Georgia, serif;
      font-size: 18px;
      line-height: 1.85;
      background-image:
        url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3CfeColorMatrix type='saturate' values='0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23noise)' opacity='0.06'/%3E%3C/svg%3E");
    }

    .page-wrap {
      max-width: 780px;
      margin: 0 auto;
      padding: 60px 40px 80px;
    }

    /* --- Header --- */
    .header {
      text-align: center;
      padding-bottom: 40px;
      border-bottom: 2px solid var(--border);
      margin-bottom: 50px;
      position: relative;
    }

    .cross-ornament {
      font-size: 2.2rem;
      color: var(--gold);
      letter-spacing: 0.15em;
      margin-bottom: 16px;
      display: block;
      animation: fadeIn 1s ease both;
    }

    h1 {
      font-family: 'Cinzel', serif;
      font-size: 2.1rem;
      font-weight: 600;
      color: var(--red);
      letter-spacing: 0.04em;
      line-height: 1.25;
      animation: fadeIn 1s ease 0.2s both;
    }

    .subtitle {
      font-family: 'EB Garamond', serif;
      font-style: italic;
      font-size: 1.05rem;
      color: var(--ink-soft);
      margin-top: 8px;
      animation: fadeIn 1s ease 0.4s both;
    }

    .effective-date {
      display: inline-block;
      margin-top: 18px;
      font-family: 'Cinzel', serif;
      font-size: 0.78rem;
      letter-spacing: 0.12em;
      color: var(--gold);
      text-transform: uppercase;
      border: 1px solid var(--border);
      padding: 5px 16px;
      border-radius: 2px;
      animation: fadeIn 1s ease 0.6s both;
    }

    /* --- Decorative divider --- */
    .divider {
      text-align: center;
      color: var(--gold-light);
      font-size: 1.2rem;
      letter-spacing: 0.5em;
      margin: 36px 0;
      opacity: 0.7;
    }

    /* --- Sections --- */
    .section {
      margin-bottom: 42px;
      animation: slideUp 0.6s ease both;
    }

    .section:nth-child(1) { animation-delay: 0.1s; }
    .section:nth-child(2) { animation-delay: 0.2s; }
    .section:nth-child(3) { animation-delay: 0.3s; }
    .section:nth-child(4) { animation-delay: 0.4s; }
    .section:nth-child(5) { animation-delay: 0.5s; }
    .section:nth-child(6) { animation-delay: 0.6s; }
    .section:nth-child(7) { animation-delay: 0.7s; }

    h2 {
      font-family: 'Cinzel', serif;
      font-size: 1.05rem;
      font-weight: 600;
      color: var(--red);
      letter-spacing: 0.08em;
      text-transform: uppercase;
      margin-bottom: 14px;
      padding-bottom: 8px;
      border-bottom: 1px solid var(--parchment-dark);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    h2::before {
      content: '✦';
      font-size: 0.6rem;
      color: var(--gold);
      flex-shrink: 0;
    }

    p {
      color: var(--ink-soft);
      margin-bottom: 12px;
    }

    ul {
      list-style: none;
      padding-left: 0;
      margin-bottom: 12px;
    }

    ul li {
      color: var(--ink-soft);
      padding: 5px 0 5px 24px;
      position: relative;
    }

    ul li::before {
      content: '·';
      position: absolute;
      left: 8px;
      color: var(--gold);
      font-size: 1.4rem;
      line-height: 1;
      top: 6px;
    }

    a {
      color: var(--red);
      text-decoration: none;
      border-bottom: 1px dotted var(--border);
      transition: color 0.2s, border-color 0.2s;
    }

    a:hover {
      color: var(--gold);
      border-bottom-color: var(--gold);
    }

    /* --- Highlight box --- */
    .note-box {
      background: linear-gradient(135deg, #fdf6eb, #f0e4cc);
      border-left: 3px solid var(--gold);
      padding: 16px 20px;
      margin: 18px 0;
      font-style: italic;
      color: var(--ink);
      border-radius: 0 4px 4px 0;
    }

    /* --- Contact block --- */
    .contact-block {
      background: var(--parchment-dark);
      border: 1px solid var(--border);
      padding: 24px 28px;
      border-radius: 4px;
      text-align: center;
    }

    .contact-block p {
      margin-bottom: 6px;
    }

    .contact-block .email {
      font-family: 'Cinzel', serif;
      font-size: 0.95rem;
      color: var(--red);
      letter-spacing: 0.04em;
    }

    /* --- Footer --- */
    footer {
      text-align: center;
      margin-top: 60px;
      padding-top: 30px;
      border-top: 1px solid var(--border);
      font-style: italic;
      color: var(--gold);
      font-size: 0.9rem;
    }

    footer .app-name {
      font-family: 'Cinzel', serif;
      font-style: normal;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      display: block;
      margin-top: 6px;
      color: var(--ink-soft);
    }

    /* --- Animations --- */
    @keyframes fadeIn {
      from { opacity: 0; }
      to   { opacity: 1; }
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(16px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* --- Responsive --- */
    @media (max-width: 600px) {
      .page-wrap { padding: 36px 22px 60px; }
      h1 { font-size: 1.55rem; }
      h2 { font-size: 0.92rem; }
      body { font-size: 16px; }
    }
  </style>
</head>
<body>
<div class="page-wrap">

  <header class="header">
    <span class="cross-ornament">✝ &nbsp; ✦ &nbsp; ✝</span>
    <h1>Privacy Policy</h1>
    <p class="subtitle">Holy Bible KJV &mdash; King James Version</p>
    <span class="effective-date">Effective Date: April 6, 2025</span>
  </header>

  <div class="note-box">
    Your privacy is important to us. This policy describes what data the Holy Bible KJV app collects, how it is used, and the choices you have.
  </div>

  <div class="divider">· · · ✦ · · ·</div>

  <div class="section">
    <h2>1. Information We Collect</h2>
    <p>The Holy Bible KJV app is designed with your privacy in mind. We collect minimal data necessary for the app to function and improve your experience:</p>
    <ul>
      <li><strong>Usage Data:</strong> Anonymous, aggregated statistics such as app crashes and performance metrics, collected through Google Firebase Crashlytics (if enabled). This data does not identify you personally.</li>
      <li><strong>Advertising Data:</strong> The app uses Google AdMob to serve ads. AdMob may collect device identifiers, IP address, and ad interaction data to serve relevant advertisements. Please refer to <a href="https://policies.google.com/privacy" target="_blank">Google's Privacy Policy</a> for details.</li>
      <li><strong>Local Storage:</strong> Bookmarks, highlights, reading progress, and preferences are stored <em>locally on your device only</em> and are never transmitted to our servers.</li>
    </ul>
  </div>

  <div class="section">
    <h2>2. How We Use Your Information</h2>
    <p>We use the information collected solely for the following purposes:</p>
    <ul>
      <li>To display advertisements via Google AdMob and support the free availability of the app.</li>
      <li>To diagnose crashes, fix bugs, and improve app stability.</li>
      <li>To personalize your in-app reading experience (locally, on your device).</li>
    </ul>
    <p>We do <strong>not</strong> sell, rent, or share your personal data with third parties for marketing purposes.</p>
  </div>

  <div class="section">
    <h2>3. Third-Party Services</h2>
    <p>The app integrates the following third-party services, each governed by their own privacy policies:</p>
    <ul>
      <li><strong>Google AdMob</strong> — Advertising platform. <a href="https://policies.google.com/privacy" target="_blank">Privacy Policy</a></li>
      <li><strong>Google Firebase</strong> — Crash reporting and analytics. <a href="https://firebase.google.com/support/privacy" target="_blank">Privacy Policy</a></li>
    </ul>
    <p>We encourage you to review the privacy policies of these services to understand how they handle your data.</p>
  </div>

  <div class="section">
    <h2>4. Data Retention &amp; Storage</h2>
    <p>All personal reading data — including bookmarks, highlights, notes, and preferences — is stored exclusively on your local device. We do not operate servers that store your personal reading data. Uninstalling the app will remove all locally stored data.</p>
  </div>

  <div class="section">
    <h2>5. Children's Privacy</h2>
    <p>The Holy Bible KJV app is intended for general audiences. We do not knowingly collect personal information from children under the age of 13. If you believe a child has provided personal information through the app, please contact us so we can take appropriate action.</p>
  </div>

  <div class="section">
    <h2>6. Your Choices</h2>
    <ul>
      <li><strong>Ad Personalization:</strong> You can opt out of personalized ads in your device's Google settings under <em>Ads &gt; Opt out of Ads Personalization</em>.</li>
      <li><strong>Permissions:</strong> The app may request permissions (e.g., notifications for Daily Verse). You can revoke these at any time via your device settings.</li>
      <li><strong>Data Deletion:</strong> Since personal data is stored only on your device, you can delete it by clearing the app's data or uninstalling the app.</li>
    </ul>
  </div>

  <div class="section">
    <h2>7. Security</h2>
    <p>We take reasonable technical measures to protect the integrity of the app and any data processed through it. However, no method of electronic transmission or storage is 100% secure, and we cannot guarantee absolute security.</p>
  </div>

  <div class="section">
    <h2>8. Changes to This Policy</h2>
    <p>We may update this Privacy Policy periodically. Any changes will be reflected by an updated effective date at the top of this page. Continued use of the app after changes constitutes acceptance of the revised policy.</p>
  </div>

  <div class="section">
    <h2>9. Contact Us</h2>
    <div class="contact-block">
      <p>If you have any questions or concerns about this Privacy Policy, please reach out:</p>
      <p class="email">nepalicoder@gmail.com</p>
      <p style="margin-top:10px; font-size:0.92rem;">Developer: Jasbin Karki &nbsp;·&nbsp; <em>com.nepalicoder</em></p>
    </div>
  </div>

  <div class="divider">· · · ✦ · · ·</div>

  <footer>
    &ldquo;Thy word is a lamp unto my feet, and a light unto my path.&rdquo; &mdash; Psalm 119:105
    <span class="app-name">Holy Bible KJV &nbsp;·&nbsp; com.nepalicoder &nbsp;·&nbsp; All Rights Reserved</span>
  </footer>

</div>
</body>
</html>
