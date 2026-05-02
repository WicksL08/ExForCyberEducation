---
layout: none
---
<!DOCTYPE html>
<html lang="en">
<head> 
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Student Tools | CTFforCyberLearning</title>
  <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
  <style>
    *,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
    :root{--bg:#050f0d;--bg2:#0a1f1a;--bg3:#0d2b24;--green:#00e5a0;--green3:#004d35;--amber:#f5a623;--blue:#5ab0ff;--text:#d4f0e8;--muted:#6fa898;--border:rgba(0,229,160,0.15);--mono:'Share Tech Mono',monospace;--sans:'Outfit',sans-serif;}
    html{scroll-behavior:smooth;}
    body{font-family:var(--sans);background:var(--bg);color:var(--text);line-height:1.6;overflow-x:hidden;}
    body::before{content:'';position:fixed;inset:0;z-index:0;background-image:linear-gradient(rgba(0,229,160,0.03) 1px,transparent 1px),linear-gradient(90deg,rgba(0,229,160,0.03) 1px,transparent 1px);background-size:40px 40px;pointer-events:none;}
    nav{position:sticky;top:0;z-index:200;display:flex;align-items:center;justify-content:space-between;padding:1rem 2.5rem;background:rgba(5,15,13,0.95);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);}
    .nav-brand{font-family:var(--mono);font-size:1.1rem;color:var(--green);letter-spacing:1px;text-decoration:none;}
    .nav-brand span{color:var(--text);}
    .nav-links{display:flex;gap:0.5rem;flex-wrap:wrap;}
    .nav-links a{font-size:0.8rem;font-family:var(--mono);padding:0.3rem 0.85rem;border-radius:4px;color:var(--muted);text-decoration:none;border:1px solid transparent;transition:all 0.2s;}
    .nav-links a:hover,.nav-links a.active{color:var(--green);border-color:var(--green3);background:rgba(0,229,160,0.06);}
    .page-hero{padding:4rem 2.5rem 3rem;border-bottom:1px solid var(--border);position:relative;z-index:1;overflow:hidden;}
    .page-hero::after{content:'';position:absolute;top:-60px;right:-80px;width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,rgba(0,229,160,0.07) 0%,transparent 65%);pointer-events:none;}
    .breadcrumb{font-family:var(--mono);font-size:0.7rem;color:var(--muted);margin-bottom:1rem;letter-spacing:1px;}
    .breadcrumb a{color:var(--green);text-decoration:none;}
    .breadcrumb span{margin:0 0.5rem;opacity:0.4;}
    .page-tag{display:inline-flex;align-items:center;gap:0.5rem;font-family:var(--mono);font-size:0.7rem;letter-spacing:2px;color:var(--green);text-transform:uppercase;background:rgba(0,229,160,0.08);border:1px solid rgba(0,229,160,0.25);padding:0.3rem 0.8rem;border-radius:3px;margin-bottom:1.25rem;width:fit-content;}
    .page-tag::before{content:'//';opacity:0.6;}
    .page-hero h1{font-family:var(--mono);font-size:clamp(1.8rem,4vw,2.6rem);font-weight:700;color:#fff;line-height:1.15;margin-bottom:0.85rem;}
    .page-hero h1 span{color:var(--green);}
    .page-hero p{font-size:0.95rem;color:var(--muted);max-width:620px;line-height:1.75;}
    .ethics-bar{background:rgba(245,166,35,0.06);border-top:1px solid rgba(245,166,35,0.2);border-bottom:1px solid rgba(245,166,35,0.2);padding:0.85rem 2.5rem;display:flex;align-items:center;gap:0.75rem;position:relative;z-index:1;}
    .ethics-bar p{font-size:0.85rem;color:var(--muted);}
    .ethics-bar strong{color:var(--amber);}
    .ethics-bar a{color:var(--green);text-decoration:underline;}
    .section{padding:3rem 2.5rem;position:relative;z-index:1;}
    .section+.section{border-top:1px solid var(--border);}
    .section-tag{font-family:var(--mono);font-size:0.68rem;color:var(--green);letter-spacing:2px;text-transform:uppercase;margin-bottom:0.5rem;display:block;}
    .section h2{font-size:1.4rem;font-weight:700;color:#fff;margin-bottom:0.5rem;}
    .section-desc{font-size:0.88rem;color:var(--muted);margin-bottom:1.5rem;max-width:640px;line-height:1.7;}

    /* QUICK ACCESS BUTTONS */
    .quick-grid{display:flex;flex-wrap:wrap;gap:0.6rem;margin-bottom:0.5rem;}
    .quick-btn{font-family:var(--mono);font-size:0.75rem;padding:0.4rem 0.9rem;border-radius:5px;text-decoration:none;border:1px solid var(--border);color:var(--muted);background:var(--bg2);transition:all 0.2s;display:inline-flex;align-items:center;gap:0.4rem;}
    .quick-btn:hover{color:var(--green);border-color:rgba(0,229,160,0.4);background:rgba(0,229,160,0.06);}
    .qb-g{border-color:rgba(0,229,160,0.2);color:var(--green);}
    .qb-a{border-color:rgba(245,166,35,0.2);color:var(--amber);}
    .qb-b{border-color:rgba(90,176,255,0.2);color:var(--blue);}

    /* TOOL CARDS */
    .tools-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:1rem;margin-top:1.25rem;}
    .tool-card{background:var(--bg2);border:1px solid var(--border);border-radius:8px;padding:1.25rem;transition:border-color 0.2s,transform 0.2s;text-decoration:none;display:block;}
    .tool-card:hover{border-color:rgba(0,229,160,0.4);transform:translateY(-2px);}
    .tool-name{font-size:0.92rem;font-weight:600;color:#fff;margin-bottom:0.3rem;display:flex;align-items:center;gap:0.5rem;}
    .tool-url{font-family:var(--mono);font-size:0.68rem;color:var(--green);margin-bottom:0.5rem;display:block;opacity:0.8;}
    .tool-card p{font-size:0.82rem;color:var(--muted);line-height:1.6;}

    /* WARNING BOX */
    .warning{background:rgba(245,166,35,0.06);border:1px solid rgba(245,166,35,0.2);border-left:3px solid var(--amber);border-radius:6px;padding:0.85rem 1.1rem;margin-top:1.25rem;font-size:0.84rem;color:var(--muted);}
    .warning strong{color:var(--amber);}

    /* SAFETY BOX */
    .safety-box{background:var(--bg2);border:1px solid var(--border);border-radius:10px;padding:1.75rem;margin-top:1rem;}
    .safety-box h3{font-size:1rem;font-weight:600;color:#fff;margin-bottom:1rem;}
    .safety-list{list-style:none;display:flex;flex-direction:column;gap:0.6rem;}
    .safety-list li{display:flex;align-items:flex-start;gap:0.65rem;font-size:0.88rem;color:var(--text);}
    .safety-list li::before{content:'▸';color:var(--amber);font-family:var(--mono);flex-shrink:0;margin-top:2px;}

    footer{background:var(--bg2);border-top:1px solid var(--border);padding:2.5rem 2.5rem 1.5rem;position:relative;z-index:1;}
    .footer-top{display:flex;justify-content:space-between;flex-wrap:wrap;gap:2rem;margin-bottom:2rem;}
    .footer-brand{font-family:var(--mono);color:var(--green);font-size:1rem;margin-bottom:0.5rem;}
    .footer-desc{font-size:0.82rem;color:var(--muted);max-width:260px;line-height:1.6;}
    .footer-links h4{font-size:0.78rem;font-family:var(--mono);color:var(--green);letter-spacing:1px;margin-bottom:0.75rem;text-transform:uppercase;}
    .footer-links a{display:block;font-size:0.82rem;color:var(--muted);text-decoration:none;margin-bottom:0.4rem;transition:color 0.2s;}
    .footer-links a:hover{color:var(--text);}
    .footer-bottom{border-top:1px solid var(--border);padding-top:1.25rem;display:flex;justify-content:space-between;flex-wrap:wrap;gap:0.5rem;}
    .footer-copy{font-size:0.78rem;color:var(--muted);font-family:var(--mono);}
    .footer-ua{font-size:0.78rem;color:var(--muted);}
    @media(max-width:600px){nav,.page-hero,.section,.ethics-bar,footer{padding-left:1.25rem;padding-right:1.25rem;}}
  </style>
</head>
<body>
<nav>
  <a href="/CTFforCyberLearning/" class="nav-brand">CTFfor<span>CyberLearning</span></a>
  <div class="nav-links">
    <a href="/CTFforCyberLearning/about/">About</a>
    <a href="/CTFforCyberLearning/learning/" class="active">Learning Lab</a>
    <a href="/CTFforCyberLearning/challenges/">Challenges</a>
    <a href="/CTFforCyberLearning/teachers/">Teacher Toolkit</a>
  </div>
</nav>

<div class="page-hero">
  <div class="breadcrumb"><a href="/CTFforCyberLearning/">Home</a><span>/</span><a href="/CTFforCyberLearning/learning/">Learning Lab</a><span>/</span>Student Tools</div>
  <div class="page-tag">Student Tools</div>
  <h1>Your CTF<br><span>Toolkit.</span></h1>
  <p>All the tools you need to solve the CTF challenges — free, browser-based, and organized by module. Use them only for class activities and follow the Code of Conduct.</p>
</div>

<div class="ethics-bar">
  <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>
  <p><strong>Ethics reminder:</strong> Use these tools only for school-approved CTF challenges. Never use them on real people, devices, or accounts. Review the <a href="/CTFforCyberLearning/about/student-agreement/">Code of Conduct</a> before starting.</p>
</div>

<!-- QUICK ACCESS -->
<div class="section">
  <span class="section-tag">// quick access</span>
  <h2>Jump to a Tool</h2>
  <p class="section-desc">Click any tool below to open it directly in a new tab.</p>

  <span class="section-tag">OSINT Tools</span>
  <div class="quick-grid">
    <a href="https://web.archive.org" target="_blank" class="quick-btn qb-g">Wayback Machine</a>
    <a href="https://images.google.com" target="_blank" class="quick-btn qb-g">Google Images</a>
    <a href="https://tineye.com" target="_blank" class="quick-btn qb-g">TinEye</a>
    <a href="https://www.metadata2go.com/" target="_blank" class="quick-btn qb-g">Metadata2Go</a>
    <a href="https://www.urlvoid.com/" target="_blank" class="quick-btn qb-g">URLVoid</a>
    <a href="https://who.is" target="_blank" class="quick-btn qb-g">WHOIS</a>
    <a href="https://www.iplocation.net/ip-lookup" target="_blank" class="quick-btn qb-g">IP Lookup</a>
    <a href="https://www.shodan.io" target="_blank" class="quick-btn qb-g">Shodan</a>
  </div>

  <br/>
  <span class="section-tag">Cryptography Tools</span>
  <div class="quick-grid">
    <a href="https://gchq.github.io/CyberChef/" target="_blank" class="quick-btn qb-a">CyberChef</a>
    <a href="https://cryptii.com/" target="_blank" class="quick-btn qb-a">Cryptii</a>
    <a href="https://www.dcode.fr/tools-list" target="_blank" class="quick-btn qb-a">dCode</a>
    <a href="https://www.base64decode.org/" target="_blank" class="quick-btn qb-a">Base64</a>
    <a href="https://www.asciitable.com/" target="_blank" class="quick-btn qb-a">ASCII Table</a>
    <a href="https://md5hashing.net/hash" target="_blank" class="quick-btn qb-a">Hash Generator</a>
    <a href="https://www.boxentriq.com/code-breaking/caesar-cipher" target="_blank" class="quick-btn qb-a">Caesar Cipher</a>
    <a href="https://www.boxentriq.com/code-breaking/vigenere-cipher" target="_blank" class="quick-btn qb-a">Vigenère Cipher</a>
  </div>

  <br/>
  <span class="section-tag">Password Tools</span>
  <div class="quick-grid">
    <a href="https://lowe.github.io/tryzxcvbn/" target="_blank" class="quick-btn qb-b">Password Strength</a>
    <a href="https://gchq.github.io/CyberChef/" target="_blank" class="quick-btn qb-b">CyberChef</a>
  </div>
</div>

<!-- OSINT TOOLS -->
<div class="section">
  <span class="section-tag">// module 01 — osint</span>
  <h2>OSINT Tools</h2>
  <p class="section-desc">These tools help you find and verify information from publicly available online sources — ethically and responsibly.</p>
  <div class="tools-grid">
    <a href="https://web.archive.org" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>Wayback Machine</div>
      <span class="tool-url">web.archive.org</span>
      <p>Shows old or deleted versions of websites — essential for tracking down vanished content.</p>
    </a>
    <a href="https://images.google.com" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>Google Image Search</div>
      <span class="tool-url">images.google.com</span>
      <p>Helps find where an image comes from or where it appears online using reverse image search.</p>
    </a>
    <a href="https://tineye.com" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>TinEye</div>
      <span class="tool-url">tineye.com</span>
      <p>Reverse image search to find the original source of a photo across the web.</p>
    </a>
    <a href="https://www.metadata2go.com/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>Metadata2Go</div>
      <span class="tool-url">metadata2go.com</span>
      <p>Reveals hidden details inside files and images — date, time, device, location data.</p>
    </a>
    <a href="https://www.urlvoid.com/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>URLVoid</div>
      <span class="tool-url">urlvoid.com</span>
      <p>Checks if a website is safe or suspicious — scans against multiple security databases.</p>
    </a>
    <a href="https://who.is" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M9.09 9a3 3 0 0 1 5.83 1c0 2-3 3-3 3"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>WHOIS Lookup</div>
      <span class="tool-url">who.is</span>
      <p>Shows who owns a website, when it was created, and basic domain registration info.</p>
    </a>
    <a href="https://www.iplocation.net/ip-lookup" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>IP Lookup</div>
      <span class="tool-url">iplocation.net</span>
      <p>Shows basic geographic and network information about an IP address.</p>
    </a>
    <a href="https://www.shodan.io" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#00e5a0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="3" width="20" height="14" rx="2" ry="2"/><line x1="8" y1="21" x2="16" y2="21"/><line x1="12" y1="17" x2="12" y2="21"/></svg>Shodan</div>
      <span class="tool-url">shodan.io</span>
      <p>A search engine showing what devices are publicly visible online. Use only to understand security exposure — never interact with devices.</p>
    </a>
  </div>
  <div class="warning"><strong>Ethics reminder:</strong> Use OSINT tools only for class clues — never for investigating real people or unauthorized accounts.</div>
</div>

<!-- CRYPTO TOOLS -->
<div class="section">
  <span class="section-tag">// module 02 — cryptography</span>
  <h2>Cryptography &amp; Encoding Tools</h2>
  <p class="section-desc">These tools help you decode, encode, and analyze secret messages and ciphers used in the CTF challenges.</p>
  <div class="tools-grid">
    <a href="https://gchq.github.io/CyberChef/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>CyberChef</div>
      <span class="tool-url" style="color:var(--amber);">gchq.github.io/CyberChef</span>
      <p>A powerful all-in-one tool for decoding, encoding, hashing, and encryption operations.</p>
    </a>
    <a href="https://cryptii.com/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>Cryptii</div>
      <span class="tool-url" style="color:var(--amber);">cryptii.com</span>
      <p>Great for testing simple ciphers — Caesar, Bacon, Morse code, and more.</p>
    </a>
    <a href="https://www.dcode.fr/tools-list" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>dCode</div>
      <span class="tool-url" style="color:var(--amber);">dcode.fr</span>
      <p>A huge library of online cipher solvers for puzzles and encoded messages.</p>
    </a>
    <a href="https://www.base64decode.org/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>Base64 Decode</div>
      <span class="tool-url" style="color:var(--amber);">base64decode.org</span>
      <p>Turns Base64 encoded text into readable words and back again.</p>
    </a>
    <a href="https://www.asciitable.com/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>ASCII Table</div>
      <span class="tool-url" style="color:var(--amber);">asciitable.com</span>
      <p>Shows how letters and symbols are stored as numbers in computers.</p>
    </a>
    <a href="https://www.boxentriq.com/code-breaking/caesar-cipher" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>Caesar Cipher Tool</div>
      <span class="tool-url" style="color:var(--amber);">boxentriq.com</span>
      <p>Shifts letters to decode or encode Caesar cipher messages instantly.</p>
    </a>
    <a href="https://www.boxentriq.com/code-breaking/vigenere-cipher" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>Vigenère Cipher Tool</div>
      <span class="tool-url" style="color:var(--amber);">boxentriq.com</span>
      <p>Decodes messages that use repeating key patterns — the Vigenère cipher.</p>
    </a>
    <a href="https://md5hashing.net/hash" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#f5a623" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>Hash Generator</div>
      <span class="tool-url" style="color:var(--amber);">md5hashing.net</span>
      <p>Creates MD5 and SHA hash values — shows how passwords are stored in databases.</p>
    </a>
  </div>
</div>

<!-- PASSWORD TOOLS -->
<div class="section">
  <span class="section-tag">// module 03 — password security</span>
  <h2>Password Security Tools</h2>
  <p class="section-desc">These tools help you understand how passwords work, how they get cracked, and how to make them stronger. Never enter real passwords — use made-up sample passwords only.</p>
  <div class="tools-grid">
    <a href="https://lowe.github.io/tryzxcvbn/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#5ab0ff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>Password Strength Checker</div>
      <span class="tool-url" style="color:var(--blue);">lowe.github.io/tryzxcvbn</span>
      <p>Shows how strong a password is and estimates how long it would take to crack it.</p>
    </a>
    <a href="https://gchq.github.io/CyberChef/" target="_blank" class="tool-card">
      <div class="tool-name"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="#5ab0ff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>CyberChef</div>
      <span class="tool-url" style="color:var(--blue);">gchq.github.io/CyberChef</span>
      <p>Also useful for exploring hashing and encryption concepts related to password security.</p>
    </a>
  </div>
  <div class="warning"><strong>Important:</strong> Never enter real passwords into any online tool. Always use fake sample passwords when testing.</div>
</div>

<!-- SAFETY -->
<div class="section">
  <span class="section-tag">// safety reminders</span>
  <h2>Before You Start</h2>
  <div class="safety-box">
    <h3>Use These Tools Responsibly</h3>
    <ul class="safety-list">
      <li>Use these tools only for school-approved CTF challenges — nothing else</li>
      <li>Never scan, probe, or investigate real people's devices, accounts, or networks</li>
      <li>Never enter real passwords, personal info, or sensitive data into any tool</li>
      <li>Ask the researcher if you're unsure whether something is allowed</li>
      <li>Review the <a href="/CTFforCyberLearning/about/student-agreement/" style="color:var(--green);">Student Code of Conduct</a> before beginning any challenge</li>
    </ul>
  </div>
</div>

<footer>
  <div class="footer-top">
    <div><div class="footer-brand">CTFforCyberLearning</div><p class="footer-desc">Experiential Cyber Security education through CTF challenges, mapped to Alabama K–12 standards.</p></div>
    <div class="footer-links"><h4>Study</h4><a href="/CTFforCyberLearning/about/">About the Study</a><a href="/CTFforCyberLearning/about/team/">Research Team</a><a href="/CTFforCyberLearning/about/ethics/">Ethics & IRB</a><a href="/CTFforCyberLearning/about/consent/">Consent Forms</a></div>
    <div class="footer-links"><h4>Learn</h4><a href="/CTFforCyberLearning/learning/">Learning Lab</a><a href="/CTFforCyberLearning/learning/tools.html">Student Tools</a><a href="/CTFforCyberLearning/challenges/">Challenges</a></div>
    <div class="footer-links"><h4>Teachers</h4><a href="/CTFforCyberLearning/teachers/">Teacher Toolkit</a><a href="/CTFforCyberLearning/teachers/syllabus.html">Syllabus</a><a href="/CTFforCyberLearning/teachers/mapping.html">Standards Mapping</a></div>
  </div>
  <div class="footer-bottom">
    <span class="footer-copy">© 2025 Lacey Wicks · CTFforCyberLearning · All rights reserved.</span>
    <span class="footer-ua">Doctoral Research · Department of Computer Science · The University of Alabama</span>
  </div>
</footer>
</body>
</html>
