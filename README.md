# athan
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<link rel="manifest" href="data:application/manifest+json;base64,eyJuYW1lIjogItij2LDYp9mGINmC2LHZitipINin2YTYqNmI2LfYudmF2KkiLCAic2hvcnRfbmFtZSI6ICLYo9iw2KfZhiDYp9mE2KjZiNi32LnZhdipIiwgImRlc2NyaXB0aW9uIjogItmF2YjYp9mC2YrYqiDYp9mE2LXZhNin2KkgLSDZgtix2YrYqSDYp9mE2KjZiNi32LnZhdipIiwgInN0YXJ0X3VybCI6ICIuIiwgImRpc3BsYXkiOiAic3RhbmRhbG9uZSIsICJiYWNrZ3JvdW5kX2NvbG9yIjogIiMwMDAwMDAiLCAidGhlbWVfY29sb3IiOiAiIzAwMDAwMCIsICJvcmllbnRhdGlvbiI6ICJwb3J0cmFpdCIsICJsYW5nIjogImFyIiwgImRpciI6ICJydGwiLCAiaWNvbnMiOiBbeyJzcmMiOiAiZGF0YTppbWFnZS9zdmcreG1sO2Jhc2U2NCxQSE4yWnlCNGJXeHVjejBpYUhSMGNEb3ZMM2QzZHk1M015NXZjbWN2TWpBd01DOXpkbWNpSUhacFpYZENiM2c5SWpBZ01DQXhPVElnTVRreUlqNDhjbVZqZENCM2FXUjBhRDBpTVRreUlpQm9aV2xuYUhROUlqRTVNaUlnWm1sc2JEMGlJekF3TUNJdlBqeDBaWGgwSUhnOUlqazJJaUI1UFNJeE16QWlJR1p2Ym5RdGMybDZaVDBpTVRFd0lpQjBaWGgwTFdGdVkyaHZjajBpYldsa1pHeGxJaUJtYVd4c1BTSWpZemxoT0RSaklqNG1JemszT0RrN1BDOTBaWGgwUGp3dmMzWm5QZz09IiwgInNpemVzIjogIjE5MngxOTIiLCAidHlwZSI6ICJpbWFnZS9zdmcreG1sIiwgInB1cnBvc2UiOiAiYW55IG1hc2thYmxlIn1dfQ==">
<link rel="apple-touch-icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxODAgMTgwIj48cmVjdCB3aWR0aD0iMTgwIiBoZWlnaHQ9IjE4MCIgcng9IjQwIiBmaWxsPSIjMDAwIi8+PHRleHQgeD0iOTAiIHk9IjEyNSIgZm9udC1zaXplPSIxMDAiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZpbGw9IiNjOWE4NGMiPiYjOTc4OTs8L3RleHQ+PC9zdmc+">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="أذان البوطعمة">
<meta name="mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#000000">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>أذان قرية البوطعمة</title>

<style>
:root {
  --gold: #c9a84c;
  --gold2: #e8d08a;
  --gold3: #a07830;
  --black: #000000;
  --black4: #1a1a1a;
  --text: #f0e8d0;
  --text-dim: #887755;
}

* { margin:0; padding:0; box-sizing:border-box; -webkit-tap-highlight-color:transparent; }

html, body {
  height: 100%;
  overflow: hidden;
  background: var(--black);
  font-family: 'Geeza Pro', 'SF Arabic', 'Noto Naskh Arabic', 'Droid Arabic Naskh', 'Arabic Typesetting', Arial, sans-serif;
  color: var(--text);
}

#app {
  width: 100vw;
  height: 100svh;
  overflow: hidden;
  background:
    radial-gradient(ellipse at 50% 0%, rgba(201,168,76,0.12) 0%, transparent 60%),
    linear-gradient(180deg, #0a0a0a 0%, #000 60%);
  display: flex;
  flex-direction: column;
  align-items: center;
}

#app::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image:
    repeating-linear-gradient(45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 40px),
    repeating-linear-gradient(-45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 40px);
  pointer-events: none;
  z-index: 0;
}

.inner {
  position: relative;
  z-index: 1;
  width: 100%;
  max-width: 430px;
  height: 100svh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* ── Header: ~12% of screen ── */
.header {
  width: 100%;
  flex: 0 0 auto;
  padding: 1svh 20px 0.8svh;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-bottom: 1px solid rgba(201,168,76,0.2);
  background: rgba(0,0,0,0.6);
  backdrop-filter: blur(10px);
}

.moon-icon {
  font-size: 3.5svh;
  margin-bottom: 0.3svh;
  filter: drop-shadow(0 0 8px rgba(201,168,76,0.6));
  animation: spin-slow 20s linear infinite;
}
@keyframes spin-slow {
  from { transform: rotate(0deg); }
  to   { transform: rotate(360deg); }
}

.village-name {
  font-family: 'Geeza Pro', 'SF Arabic', 'Noto Naskh Arabic', 'Arabic Typesetting', Georgia, serif;
  font-size: 3.2svh;
  color: var(--gold);
  text-shadow: 0 0 20px rgba(201,168,76,0.5);
  letter-spacing: 1px;
  line-height: 1.1;
}

.divider {
  width: 50px;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--gold3), transparent);
  margin: 0.5svh auto 0.4svh;
}

.sub-name {
  font-size: 1.5svh;
  color: var(--text-dim);
  letter-spacing: 2px;
}

/* ── Clock: ~11% of screen ── */
.clock-section {
  width: 100%;
  flex: 0 0 auto;
  padding: 0.8svh 20px 0.6svh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: linear-gradient(180deg, rgba(201,168,76,0.06) 0%, transparent 100%);
  border-bottom: 1px solid rgba(201,168,76,0.15);
}

.clock-display {
  font-size: 6.5svh;
  font-weight: 900;
  color: var(--gold);
  letter-spacing: 3px;
  line-height: 1;
  text-shadow: 0 0 30px rgba(201,168,76,0.6), 0 0 60px rgba(201,168,76,0.2);
  font-variant-numeric: tabular-nums;
}

.clock-seconds {
  font-size: 3.2svh;
  color: var(--gold3);
  vertical-align: super;
  letter-spacing: 2px;
}

.date-display {
  margin-top: 0.3svh;
  font-size: 1.7svh;
  color: var(--text-dim);
  font-weight: 600;
}

/* ── Next prayer banner: ~9% ── */
.next-banner {
  width: calc(100% - 20px);
  margin: 0.8svh 10px 0;
  flex: 0 0 auto;
  background: linear-gradient(135deg, rgba(201,168,76,0.15), rgba(160,120,48,0.1));
  border: 1px solid rgba(201,168,76,0.35);
  border-radius: 10px;
  padding: 0.9svh 14px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.next-label {
  font-size: 1.5svh;
  color: var(--text-dim);
  margin-bottom: 0.2svh;
}

.next-name {
  font-size: 2.2svh;
  font-weight: 700;
  color: var(--gold);
}

.next-counter { text-align: left; }

.next-time-val {
  font-size: 2.8svh;
  font-weight: 900;
  color: var(--gold2);
  letter-spacing: 2px;
  font-variant-numeric: tabular-nums;
}

.iqama-label {
  font-size: 1.3svh !important;
  color: var(--text-dim);
  margin-top: 0.2svh !important;
}

.iqama-info {
  font-size: 1.4svh;
  color: var(--text-dim);
  text-align: left;
}

/* ── Prayer cards: fill remaining space ── */
.prayers-list {
  width: calc(100% - 20px);
  margin: 0 10px;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  padding: 0.5svh 0 0;
}

.prayer-card {
  width: 100%;
  background: var(--black4);
  border: 1px solid rgba(201,168,76,0.12);
  border-radius: 10px;
  padding: 1svh 12px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  transition: border-color 0.3s, background 0.3s, box-shadow 0.3s;
  position: relative;
  overflow: hidden;
}

.prayer-card::before {
  content: '';
  position: absolute;
  right: 0; top: 0; bottom: 0;
  width: 3px;
  background: transparent;
  transition: background 0.3s;
  border-radius: 0 10px 10px 0;
}

.prayer-card.active {
  background: rgba(201,168,76,0.1);
  border-color: rgba(201,168,76,0.5);
  animation: pulse-glow 3s ease-in-out infinite;
}

.prayer-card.active::before { background: var(--gold); }
.prayer-card.passed { opacity: 0.45; }

.prayer-left {
  display: flex;
  flex-direction: column;
  gap: 0;
}

.prayer-name-ar {
  font-family: 'Geeza Pro', 'SF Arabic', 'Noto Naskh Arabic', 'Arabic Typesetting', Georgia, serif;
  font-size: 2.6svh;
  color: var(--text);
  font-weight: 700;
  line-height: 1.1;
}

.prayer-card.active .prayer-name-ar { color: var(--gold2); }

.prayer-iqama-row {
  font-size: 1.3svh;
  color: var(--text-dim);
  margin-top: 0.2svh;
}

.prayer-iqama-row span { color: var(--gold3); font-weight: 700; }

.prayer-right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 0.3svh;
}

.prayer-time {
  font-size: 3svh;
  font-weight: 900;
  color: var(--gold);
  letter-spacing: 2px;
  font-variant-numeric: tabular-nums;
  line-height: 1;
}

.prayer-card.active .prayer-time {
  color: var(--gold2);
  text-shadow: 0 0 15px rgba(201,168,76,0.5);
}

.after-badge {
  font-size: 1.2svh;
  background: rgba(201,168,76,0.12);
  border: 1px solid rgba(201,168,76,0.25);
  color: var(--gold3);
  border-radius: 20px;
  padding: 0.2svh 7px;
  white-space: nowrap;
}

.prayer-card.sunrise {
  border-style: dashed;
  opacity: 0.65;
}

/* ── Footer credit ── */
.footer-credit {
  flex: 0 0 auto;
  padding: 0.5svh 0 0.8svh;
  font-size: 1.3svh;
  color: rgba(201,168,76,0.5);
  letter-spacing: 1px;
  text-align: center;
  font-family: 'Geeza Pro', 'SF Arabic', 'Noto Naskh Arabic', 'Droid Arabic Naskh', 'Arabic Typesetting', Arial, sans-serif;
}

@keyframes pulse-glow {
  0%,100% { box-shadow: 0 4px 20px rgba(201,168,76,0.15), inset 0 0 20px rgba(201,168,76,0.04); }
  50%      { box-shadow: 0 4px 30px rgba(201,168,76,0.28), inset 0 0 30px rgba(201,168,76,0.08); }
}
</style>
<script>
if ('serviceWorker' in navigator) {
  const sw = `
const CACHE = 'athan-v1';
self.addEventListener('install', e => {
  self.skipWaiting();
});
self.addEventListener('activate', e => {
  self.clients.claim();
});
self.addEventListener('fetch', e => {
  e.respondWith(
    caches.match(e.request).then(r => r || fetch(e.request).catch(() => new Response('', {status: 408})))
  );
});
`;
  const blob = new Blob([sw], {type: 'application/javascript'});
  const url = URL.createObjectURL(blob);
  navigator.serviceWorker.register(url).catch(() => {});
}

// Show install prompt on Android Chrome
let deferredPrompt;
window.addEventListener('beforeinstallprompt', e => {
  e.preventDefault();
  deferredPrompt = e;
  document.getElementById('installBtn').style.display = 'flex';
});
window.addEventListener('appinstalled', () => {
  document.getElementById('installBtn').style.display = 'none';
  deferredPrompt = null;
});
function triggerInstall() {
  if (deferredPrompt) {
    deferredPrompt.prompt();
    deferredPrompt.userChoice.then(() => { deferredPrompt = null; });
  } else {
    document.getElementById('installGuide').style.display = 'flex';
  }
}
</script>
</head>
<body>
<div id="app">
<div class="inner">
  <!-- Install Button -->
  <div id="installBtn" onclick="triggerInstall()" style="display:none;position:fixed;bottom:18px;left:50%;transform:translateX(-50%);z-index:100;background:linear-gradient(135deg,#c9a84c,#a07830);color:#000;font-weight:700;font-size:0.9rem;padding:10px 24px;border-radius:24px;box-shadow:0 4px 20px rgba(201,168,76,0.5);cursor:pointer;align-items:center;gap:8px;white-space:nowrap;">
    <span style="font-size:1.1rem;">⊕</span> أضف للشاشة الرئيسية
  </div>

  <!-- Header -->
  <div class="header">
    <div class="moon-icon">☽</div>
    <div class="village-name">قرية البوطعمة</div>
    <div class="divider"></div>
    <div class="sub-name">ناحية الحجاج &nbsp;•&nbsp; مواقيت الصلاة</div>
  </div>

  <!-- Clock -->
  <div class="clock-section">
    <div class="clock-display">
      <span id="clockH">00</span>:<span id="clockM">00</span><span class="clock-seconds">:<span id="clockS">00</span></span>
    </div>
    <div class="date-display" id="dateDisplay">—</div>
  </div>

  <!-- Next prayer -->
  <div class="next-banner">
    <div>
      <div class="next-label">الصلاة القادمة</div>
      <div class="next-name" id="nextName">—</div>
    </div>
    <div class="next-counter">
      <div class="next-time-val" id="nextCountdown">00:00:00</div>
      <div class="iqama-label" style="font-size:0.7rem;color:var(--text-dim);margin-top:2px">بعد الأذان للإقامة</div>
      <div class="iqama-info" id="nextIqama">— دقيقة</div>
    </div>
  </div>

  <!-- Prayer cards -->
  <div class="prayers-list" id="prayersList"></div>


  <!-- Offline install guide -->
  <div id="installGuide" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,0.92);z-index:999;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:24px;text-align:center;" onclick="this.style.display='none'">
    <div style="color:#c9a84c;font-size:1.5rem;margin-bottom:12px;">☽</div>
    <div style="color:#e8d08a;font-size:1.1rem;font-weight:700;margin-bottom:16px;">أضف للشاشة الرئيسية</div>
    <div style="background:#1a1a1a;border:1px solid rgba(201,168,76,0.3);border-radius:12px;padding:16px;margin-bottom:12px;width:100%;max-width:300px;">
      <div style="color:#c9a84c;font-weight:700;margin-bottom:8px;">📱 الأيفون (Safari)</div>
      <div style="color:#f0e8d0;font-size:0.85rem;line-height:1.7;">
        ١. افتح الملف في Safari<br>
        ٢. اضغط زر المشاركة <span style="font-size:1rem;">⬆️</span><br>
        ٣. اختر <strong style="color:#c9a84c;">"Add to Home Screen"</strong><br>
        ٤. اضغط "Add" ✓
      </div>
    </div>
    <div style="background:#1a1a1a;border:1px solid rgba(201,168,76,0.3);border-radius:12px;padding:16px;width:100%;max-width:300px;">
      <div style="color:#c9a84c;font-weight:700;margin-bottom:8px;">📱 الأندرويد (Chrome)</div>
      <div style="color:#f0e8d0;font-size:0.85rem;line-height:1.7;">
        ١. افتح الملف في Chrome<br>
        ٢. اضغط القائمة <span style="font-size:1rem;">⋮</span><br>
        ٣. اختر <strong style="color:#c9a84c;">"Add to Home Screen"</strong><br>
        ٤. اضغط "Add" ✓
      </div>
    </div>
    <div style="color:#887755;font-size:0.75rem;margin-top:16px;">اضغط أي مكان للإغلاق</div>
  </div>
  <div class="footer-credit" onclick="document.getElementById('installGuide').style.display='flex'" style="cursor:pointer;" title="اضغط لإضافة للشاشة الرئيسية">علي جاسم خلف • قرية البوطعمة &nbsp;⊕</div>

</div>
</div>

<script>
// ════════════════════════════════════════════
//  PRAYER DATA  (month 1-12, day 1-31)
//  Format per day: [fajr2, shoroq, dhuhr, asr, maghrib, isha]
//  (fajr1 not shown on main screen, iqama computed separately)
// ════════════════════════════════════════════

const DATA = {
  1:[  // January  كانون الثاني
    null,
    ["05:07","07:13","12:16","02:55","05:54","06:32"],
    ["05:08","07:14","12:16","02:55","05:54","06:32"],
    ["05:09","07:14","12:17","02:56","05:54","06:32"],
    ["05:09","07:14","12:17","02:57","05:55","06:32"],
    ["05:10","07:14","12:18","02:58","05:55","06:33"],
    ["05:11","07:14","12:18","02:58","05:55","06:33"],
    ["05:12","07:14","12:19","02:59","05:55","06:33"],
    ["05:13","07:14","12:19","03:00","05:55","06:33"],
    ["05:14","07:14","12:19","03:01","05:55","06:33"],
    ["05:15","07:14","12:20","03:01","05:55","06:34"],
    ["05:15","07:14","12:20","03:02","05:55","06:35"],
    ["05:16","07:14","12:20","03:03","05:55","06:36"],
    ["05:17","07:14","12:21","03:04","05:55","06:37"],
    ["05:18","07:13","12:21","03:05","05:55","06:38"],
    ["05:19","07:13","12:22","03:05","05:55","06:39"],
    ["05:20","07:13","12:22","03:06","05:55","06:40"],
    ["05:21","07:13","12:22","03:07","05:55","06:41"],
    ["05:22","07:12","12:23","03:08","05:55","06:42"],
    ["05:23","07:12","12:23","03:09","05:55","06:43"],
    ["05:24","07:12","12:23","03:10","05:54","06:44"],
    ["05:25","07:11","12:23","03:10","05:54","06:45"],
    ["05:26","07:11","12:24","03:11","05:54","06:46"],
    ["05:27","07:10","12:24","03:12","05:53","06:47"],
    ["05:28","07:10","12:24","03:13","05:53","06:48"],
    ["05:29","07:09","12:24","03:14","05:53","06:49"],
    ["05:30","07:09","12:25","03:15","05:52","06:50"],
    ["05:31","07:08","12:25","03:15","05:52","06:51"],
    ["05:32","07:08","12:25","03:16","05:51","06:52"],
    ["05:33","07:07","12:25","03:17","05:51","06:53"],
    ["05:34","07:06","12:25","03:18","05:50","06:54"],
    ["05:35","07:06","12:26","03:19","05:50","06:55"],
  ],
  2:[  // February  شباط
    null,
    ["05:37","07:05","12:26","03:19","05:49","06:57"],
    ["05:38","07:04","12:26","03:20","05:48","06:58"],
    ["05:39","07:03","12:26","03:21","05:47","06:59"],
    ["05:40","07:03","12:26","03:22","05:47","07:00"],
    ["05:41","07:02","12:26","03:23","05:46","07:01"],
    ["05:42","07:01","12:26","03:23","05:45","07:02"],
    ["05:43","07:00","12:26","03:24","05:44","07:03"],
    ["05:44","06:59","12:27","03:25","05:43","07:04"],
    ["05:45","06:58","12:27","03:26","05:42","07:05"],
    ["05:46","06:57","12:27","03:26","05:41","07:06"],
    ["05:47","06:56","12:27","03:27","05:40","07:07"],
    ["05:48","06:55","12:27","03:28","05:39","07:08"],
    ["05:49","06:54","12:27","03:29","05:38","07:09"],
    ["05:49","06:53","12:27","03:29","05:37","07:09"],
    ["05:50","06:52","12:27","03:30","05:36","07:10"],
    ["05:51","06:51","12:27","03:31","05:35","07:11"],
    ["05:52","06:50","12:27","03:31","05:34","07:12"],
    ["05:53","06:49","12:26","03:32","05:33","07:13"],
    ["05:54","06:48","12:26","03:32","05:32","07:14"],
    ["05:55","06:47","12:26","03:33","05:31","07:15"],
    ["05:56","06:46","12:26","03:34","05:30","07:16"],
    ["05:57","06:45","12:26","03:34","05:29","07:17"],
    ["05:57","06:43","12:26","03:35","05:28","07:17"],
    ["05:58","06:42","12:26","03:35","05:27","07:18"],
    ["05:59","06:41","12:26","03:36","05:26","07:19"],
    ["06:00","06:40","12:26","03:36","05:25","07:20"],
    ["06:01","06:39","12:26","03:37","05:24","07:21"],
    ["06:02","06:37","12:25","03:37","05:22","07:22"],
    ["06:02","06:36","12:25","03:38","05:21","07:22"],
  ],
  3:[  // March  آذار
    null,
    ["06:04","06:35","12:25","03:40","05:20","07:24"],
    ["06:05","06:34","12:25","03:40","05:19","07:25"],
    ["06:06","06:32","12:25","03:41","05:17","07:26"],
    ["06:07","06:31","12:25","03:41","05:16","07:27"],
    ["06:07","06:30","12:24","03:42","05:15","07:27"],
    ["06:08","06:28","12:24","03:42","05:13","07:28"],
    ["06:09","06:27","12:24","03:43","05:12","07:29"],
    ["06:10","06:26","12:24","03:43","05:11","07:30"],
    ["06:11","06:24","12:23","03:43","05:09","07:31"],
    ["06:12","06:23","12:23","03:44","05:08","07:32"],
    ["06:12","06:22","12:23","03:44","05:07","07:32"],
    ["06:13","06:20","12:23","03:44","05:05","07:33"],
    ["06:14","06:19","12:22","03:45","05:04","07:34"],
    ["06:15","06:17","12:22","03:45","05:02","07:35"],
    ["06:16","06:16","12:22","03:45","05:01","07:36"],
    ["06:17","06:15","12:22","03:46","05:00","07:37"],
    ["06:18","06:13","12:21","03:46","04:58","07:38"],
    ["06:18","06:12","12:21","03:46","04:57","07:38"],
    ["06:19","06:10","12:21","03:46","04:55","07:39"],
    ["06:20","06:09","12:20","03:47","04:54","07:40"],
    ["06:21","06:08","12:20","03:47","04:53","07:41"],
    ["06:21","06:06","12:20","03:47","04:51","07:41"],
    ["06:22","06:05","12:19","03:47","04:50","07:42"],
    ["06:23","06:03","12:19","03:47","04:48","07:43"],
    ["06:24","06:02","12:19","03:47","04:47","07:44"],
    ["06:25","06:01","12:18","03:48","04:46","07:45"],
    ["06:25","05:59","12:18","03:48","04:44","07:45"],
    ["06:26","05:58","12:18","03:48","04:43","07:46"],
    ["06:27","05:56","12:17","03:48","04:41","07:47"],
    ["06:28","05:55","12:17","03:48","04:40","07:48"],
    ["06:29","05:54","12:17","03:48","04:39","07:49"],
  ],
  4:[  // April  نيسان
    null,
    ["04:37","05:52","12:17","03:48","06:29","07:49"],
    ["04:36","05:51","12:16","03:49","06:30","07:50"],
    ["04:35","05:50","12:16","03:49","06:31","07:51"],
    ["04:33","05:48","12:16","03:49","06:32","07:52"],
    ["04:32","05:47","12:15","03:49","06:32","07:52"],
    ["04:30","05:45","12:15","03:49","06:33","07:53"],
    ["04:29","05:44","12:15","03:49","06:34","07:54"],
    ["04:28","05:43","12:14","03:49","06:35","07:55"],
    ["04:26","05:41","12:14","03:49","06:35","07:55"],
    ["04:24","05:40","12:14","03:49","06:36","07:56"],
    ["04:23","05:39","12:13","03:49","06:37","07:57"],
    ["04:21","05:37","12:13","03:49","06:38","07:58"],
    ["04:20","05:36","12:13","03:49","06:38","07:58"],
    ["04:19","05:35","12:13","03:49","06:39","07:59"],
    ["04:17","05:34","12:12","03:49","06:40","08:00"],
    ["04:15","05:32","12:12","03:49","06:41","08:01"],
    ["04:14","05:31","12:12","03:49","06:41","08:01"],
    ["04:13","05:30","12:12","03:49","06:42","08:02"],
    ["04:12","05:29","12:11","03:49","06:43","08:03"],
    ["04:10","05:27","12:11","03:49","06:44","08:04"],
    ["04:08","05:26","12:11","03:49","06:44","08:04"],
    ["04:07","05:25","12:11","03:49","06:45","08:05"],
    ["04:06","05:24","12:11","03:50","06:46","08:06"],
    ["04:04","05:23","12:10","03:50","06:47","08:07"],
    ["04:02","05:21","12:10","03:50","06:47","08:07"],
    ["04:01","05:20","12:10","03:50","06:49","08:09"],
    ["04:00","05:19","12:10","03:51","06:50","08:10"],
    ["03:59","05:18","12:10","03:51","06:51","08:11"],
    ["03:58","05:17","12:10","03:52","06:52","08:12"],
    ["03:57","05:16","12:09","03:52","06:53","08:13"],
  ],
  5:[  // May  أيار
    null,
    ["03:55","05:15","12:09","03:53","06:54","08:14"],
    ["03:54","05:14","12:09","03:53","06:55","08:15"],
    ["03:53","05:13","12:09","03:53","06:56","08:16"],
    ["03:51","05:12","12:09","03:53","06:56","08:16"],
    ["03:50","05:11","12:09","03:53","06:57","08:17"],
    ["03:49","05:10","12:09","03:53","06:58","08:18"],
    ["03:48","05:09","12:09","03:53","06:59","08:19"],
    ["03:46","05:08","12:09","03:53","06:59","08:20"],
    ["03:45","05:07","12:09","03:53","07:00","08:21"],
    ["03:44","05:06","12:09","03:53","07:01","08:22"],
    ["03:43","05:05","12:09","03:53","07:02","08:23"],
    ["03:42","05:04","12:09","03:53","07:02","08:23"],
    ["03:41","05:04","12:09","03:53","07:03","08:24"],
    ["03:40","05:03","12:09","03:53","07:04","08:25"],
    ["03:38","05:02","12:09","03:54","07:05","08:26"],
    ["03:37","05:01","12:09","03:54","07:05","08:26"],
    ["03:36","05:01","12:09","03:54","07:06","08:27"],
    ["03:35","05:00","12:09","03:54","07:07","08:28"],
    ["03:34","04:59","12:09","03:54","07:08","08:29"],
    ["03:34","04:59","12:09","03:54","07:08","08:29"],
    ["03:33","04:58","12:09","03:54","07:09","08:30"],
    ["03:33","04:58","12:09","03:54","07:10","08:31"],
    ["03:32","04:57","12:09","03:54","07:10","08:31"],
    ["03:31","04:56","12:09","03:55","07:11","08:32"],
    ["03:31","04:56","12:09","03:55","07:12","08:33"],
    ["03:30","04:55","12:10","03:55","07:12","08:33"],
    ["03:30","04:55","12:10","03:55","07:13","08:34"],
    ["03:29","04:55","12:10","03:55","07:14","08:35"],
    ["03:28","04:54","12:10","03:55","07:14","08:35"],
    ["03:28","04:54","12:10","03:55","07:15","08:36"],
    ["03:27","04:53","12:10","03:56","07:16","08:37"],
  ],
  6:[  // June  حزيران
    null,
    ["03:27","04:53","12:10","03:56","07:16","08:38"],
    ["03:27","04:53","12:11","03:56","07:17","08:39"],
    ["03:26","04:53","12:11","03:56","07:17","08:39"],
    ["03:26","04:52","12:11","03:56","07:18","08:40"],
    ["03:26","04:52","12:11","03:56","07:19","08:41"],
    ["03:25","04:52","12:11","03:57","07:19","08:42"],
    ["03:25","04:52","12:11","03:57","07:20","08:42"],
    ["03:25","04:52","12:12","03:57","07:20","08:43"],
    ["03:25","04:52","12:12","03:57","07:21","08:43"],
    ["03:24","04:51","12:12","03:57","07:21","08:44"],
    ["03:24","04:51","12:12","03:58","07:21","08:44"],
    ["03:24","04:51","12:12","03:58","07:22","08:45"],
    ["03:24","04:51","12:13","03:58","07:22","08:45"],
    ["03:24","04:51","12:13","03:58","07:23","08:46"],
    ["03:25","04:52","12:13","03:59","07:23","08:46"],
    ["03:25","04:52","12:13","03:59","07:23","08:46"],
    ["03:25","04:52","12:13","03:59","07:24","08:47"],
    ["03:25","04:52","12:14","03:59","07:24","08:47"],
    ["03:25","04:52","12:14","03:59","07:24","08:47"],
    ["03:25","04:52","12:14","03:59","07:25","08:47"],
    ["03:25","04:52","12:14","04:00","07:25","08:47"],
    ["03:26","04:53","12:14","04:00","07:25","08:48"],
    ["03:26","04:53","12:15","04:00","07:25","08:48"],
    ["03:26","04:53","12:15","04:00","07:25","08:48"],
    ["03:26","04:53","12:15","04:00","07:26","08:48"],
    ["03:27","04:54","12:15","04:01","07:26","08:48"],
    ["03:27","04:54","12:15","04:01","07:26","08:49"],
    ["03:28","04:55","12:16","04:01","07:26","08:49"],
    ["03:28","04:55","12:16","04:01","07:26","08:49"],
    ["03:28","04:55","12:16","04:01","07:26","08:49"],
  ],
  7:[  // July  تموز
    null,
    ["03:29","04:56","12:16","04:02","07:25","08:50"],
    ["03:29","04:56","12:16","04:02","07:25","08:50"],
    ["03:30","04:57","12:16","04:02","07:25","08:50"],
    ["03:30","04:57","12:16","04:02","07:25","08:49"],
    ["03:31","04:58","12:17","04:02","07:25","08:49"],
    ["03:31","04:58","12:17","04:02","07:25","08:49"],
    ["03:31","04:59","12:17","04:02","07:25","08:49"],
    ["03:32","04:59","12:17","04:03","07:24","08:48"],
    ["03:32","05:00","12:17","04:03","07:24","08:48"],
    ["03:33","05:00","12:18","04:03","07:24","08:48"],
    ["03:33","05:01","12:18","04:03","07:24","08:48"],
    ["03:34","05:02","12:18","04:03","07:23","08:47"],
    ["03:34","05:02","12:18","04:03","07:23","08:47"],
    ["03:35","05:03","12:18","04:03","07:22","08:46"],
    ["03:35","05:03","12:18","04:03","07:22","08:46"],
    ["03:36","05:04","12:18","04:03","07:22","08:45"],
    ["03:37","05:05","12:18","04:04","07:21","08:45"],
    ["03:38","05:05","12:18","04:04","07:21","08:44"],
    ["03:39","05:06","12:18","04:04","07:20","08:44"],
    ["03:40","05:07","12:18","04:04","07:19","08:43"],
    ["03:40","05:07","12:18","04:04","07:19","08:43"],
    ["03:41","05:08","12:19","04:04","07:18","08:43"],
    ["03:42","05:09","12:19","04:04","07:18","08:42"],
    ["03:43","05:10","12:19","04:04","07:17","08:41"],
    ["03:44","05:10","12:19","04:04","07:16","08:40"],
    ["03:45","05:11","12:19","04:04","07:16","08:39"],
    ["03:46","05:12","12:19","04:04","07:15","08:38"],
    ["03:47","05:13","12:19","04:04","07:14","08:38"],
    ["03:48","05:13","12:19","04:03","07:13","08:37"],
    ["03:49","05:14","12:19","04:03","07:12","08:36"],
    ["03:50","05:15","12:19","04:03","07:12","08:35"],
  ],
  8:[  // August  آب
    null,
    ["03:50","05:15","12:18","04:03","07:11","08:34"],
    ["03:51","05:16","12:18","04:03","07:10","08:33"],
    ["03:52","05:17","12:18","04:03","07:09","08:32"],
    ["03:54","05:18","12:18","04:03","07:08","08:31"],
    ["03:55","05:18","12:18","04:02","07:07","08:31"],
    ["03:55","05:19","12:18","04:02","07:06","08:30"],
    ["03:56","05:20","12:18","04:02","07:05","08:29"],
    ["03:57","05:21","12:18","04:02","07:04","08:28"],
    ["03:59","05:22","12:18","04:02","07:03","08:26"],
    ["04:00","05:22","12:18","04:01","07:02","08:25"],
    ["04:01","05:23","12:18","04:01","07:01","08:24"],
    ["04:02","05:24","12:17","04:01","07:00","08:23"],
    ["04:03","05:25","12:17","04:00","06:59","08:22"],
    ["04:04","05:25","12:17","04:00","06:58","08:21"],
    ["04:05","05:26","12:17","04:00","06:57","08:20"],
    ["04:06","05:27","12:17","03:59","06:55","08:19"],
    ["04:07","05:28","12:17","03:59","06:54","08:18"],
    ["04:08","05:28","12:16","03:59","06:53","08:17"],
    ["04:09","05:29","12:16","03:58","06:52","08:16"],
    ["04:10","05:30","12:16","03:58","06:51","08:15"],
    ["04:11","05:31","12:16","03:57","06:49","08:14"],
    ["04:12","05:31","12:16","03:57","06:48","08:12"],
    ["04:13","05:32","12:15","03:56","06:47","08:10"],
    ["04:14","05:33","12:15","03:56","06:46","08:08"],
    ["04:15","05:34","12:15","03:55","06:44","08:07"],
    ["04:16","05:34","12:15","03:55","06:43","08:05"],
    ["04:16","05:35","12:14","03:54","06:42","08:03"],
    ["04:17","05:36","12:14","03:54","06:40","08:01"],
    ["04:18","05:36","12:14","03:53","06:39","07:59"],
    ["04:19","05:37","12:13","03:53","06:38","07:58"],
    ["04:20","05:38","12:13","03:52","06:36","07:56"],
  ],
  9:[  // September  أيلول
    null,
    ["04:21","05:39","12:13","03:50","06:35","07:55"],
    ["04:21","05:39","12:13","03:49","06:34","07:54"],
    ["04:22","05:40","12:12","03:48","06:32","07:52"],
    ["04:23","05:41","12:12","03:47","06:31","07:51"],
    ["04:24","05:42","12:12","03:47","06:30","07:50"],
    ["04:25","05:42","12:11","03:46","06:28","07:48"],
    ["04:26","05:43","12:11","03:45","06:27","07:47"],
    ["04:27","05:44","12:11","03:45","06:25","07:45"],
    ["04:28","05:44","12:10","03:44","06:24","07:44"],
    ["04:29","05:45","12:10","03:43","06:23","07:43"],
    ["04:30","05:46","12:10","03:42","06:21","07:41"],
    ["04:31","05:47","12:09","03:41","06:20","07:40"],
    ["04:32","05:47","12:09","03:41","06:18","07:38"],
    ["04:33","05:48","12:08","03:40","06:17","07:37"],
    ["04:34","05:49","12:08","03:39","06:15","07:35"],
    ["04:34","05:49","12:08","03:38","06:14","07:34"],
    ["04:35","05:50","12:07","03:37","06:13","07:33"],
    ["04:36","05:51","12:07","03:37","06:11","07:31"],
    ["04:37","05:52","12:07","03:36","06:10","07:30"],
    ["04:37","05:52","12:06","03:35","06:08","07:28"],
    ["04:38","05:53","12:06","03:34","06:07","07:27"],
    ["04:39","05:54","12:06","03:33","06:05","07:25"],
    ["04:40","05:55","12:05","03:32","06:04","07:24"],
    ["04:40","05:55","12:05","03:31","06:03","07:23"],
    ["04:41","05:56","12:04","03:30","06:01","07:21"],
    ["04:42","05:57","12:04","03:30","06:00","07:20"],
    ["04:43","05:58","12:04","03:29","05:58","07:18"],
    ["04:43","05:58","12:03","03:28","05:57","07:17"],
    ["04:44","05:59","12:03","03:27","05:55","07:15"],
    ["04:45","06:00","12:03","03:26","05:54","07:14"],
  ],
  10:[ // October  تشرين الأول
    null,
    ["05:53","06:01","12:02","03:25","04:46","07:13"],
    ["05:51","06:01","12:02","03:24","04:46","07:11"],
    ["05:50","06:02","12:02","03:23","04:47","07:10"],
    ["05:48","06:03","12:01","03:22","04:48","07:08"],
    ["05:47","06:04","12:01","03:21","04:49","07:07"],
    ["05:46","06:04","12:01","03:20","04:49","07:06"],
    ["05:44","06:05","12:00","03:19","04:50","07:04"],
    ["05:43","06:06","12:00","03:18","04:51","07:03"],
    ["05:42","06:07","12:00","03:17","04:52","07:02"],
    ["05:40","06:08","11:59","03:16","04:53","07:00"],
    ["05:39","06:08","11:59","03:16","04:53","06:59"],
    ["05:38","06:09","11:59","03:15","04:54","06:58"],
    ["05:36","06:10","11:59","03:14","04:55","06:56"],
    ["05:35","06:11","11:58","03:13","04:56","06:55"],
    ["05:34","06:12","11:58","03:12","04:57","06:54"],
    ["05:33","06:13","11:58","03:11","04:58","06:53"],
    ["05:31","06:13","11:58","03:10","04:58","06:52"],
    ["05:30","06:14","11:57","03:09","04:59","06:51"],
    ["05:29","06:15","11:57","03:08","05:00","06:50"],
    ["05:28","06:16","11:57","03:07","05:01","06:49"],
    ["05:26","06:17","11:57","03:07","05:02","06:48"],
    ["05:25","06:18","11:57","03:06","05:03","06:47"],
    ["05:24","06:19","11:57","03:05","05:04","06:46"],
    ["05:23","06:20","11:56","03:04","05:05","06:45"],
    ["05:22","06:20","11:56","03:03","05:05","06:44"],
    ["05:21","06:21","11:56","03:02","05:06","06:43"],
    ["05:20","06:22","11:56","03:02","05:07","06:42"],
    ["05:18","06:23","11:56","03:01","05:08","06:41"],
    ["05:17","06:24","11:56","03:00","05:09","06:40"],
    ["05:16","06:25","11:56","02:59","05:10","06:39"],
    ["05:15","06:26","11:56","02:58","05:11","06:38"],
  ],
  11:[ // November  تشرين الثاني
    null,
    ["05:14","06:27","11:56","02:57","05:12","06:36"],
    ["05:13","06:28","11:56","02:56","05:13","06:35"],
    ["05:12","06:29","11:56","02:55","05:14","06:34"],
    ["05:12","06:30","11:56","02:54","05:15","06:33"],
    ["05:11","06:31","11:56","02:53","05:15","06:32"],
    ["05:10","06:32","11:56","02:52","05:16","06:32"],
    ["05:09","06:33","11:56","02:51","05:17","06:31"],
    ["05:08","06:33","11:56","02:51","05:18","06:30"],
    ["05:07","06:34","11:56","02:50","05:19","06:29"],
    ["05:06","06:35","11:56","02:49","05:20","06:29"],
    ["05:06","06:36","11:56","02:49","05:20","06:28"],
    ["05:05","06:37","11:56","02:48","05:21","06:27"],
    ["05:04","06:38","11:57","02:48","05:22","06:27"],
    ["05:04","06:39","11:57","02:47","05:23","06:26"],
    ["05:03","06:40","11:57","02:47","05:24","06:26"],
    ["05:02","06:41","11:57","02:47","05:25","06:25"],
    ["05:02","06:42","11:57","02:46","05:25","06:25"],
    ["05:01","06:43","11:57","02:46","05:26","06:24"],
    ["05:01","06:44","11:58","02:46","05:27","06:24"],
    ["05:00","06:45","11:58","02:45","05:28","06:23"],
    ["05:00","06:46","11:58","02:45","05:29","06:23"],
    ["04:59","06:47","11:58","02:44","05:30","06:22"],
    ["04:59","06:48","11:59","02:44","05:30","06:22"],
    ["04:58","06:49","11:59","02:44","05:31","06:22"],
    ["04:58","06:50","11:59","02:44","05:32","06:22"],
    ["04:58","06:51","12:00","02:44","05:33","06:22"],
    ["04:58","06:52","12:00","02:44","05:34","06:22"],
    ["04:57","06:53","12:01","02:44","05:34","06:22"],
    ["04:57","06:54","12:01","02:44","05:35","06:22"],
    ["04:57","06:54","12:01","02:44","05:36","06:22"],
  ],
  12:[ // December  كانون الأول
    null,
    ["04:57","06:55","12:02","02:44","05:37","06:22"],
    ["04:57","06:56","12:02","02:44","05:37","06:22"],
    ["04:56","06:57","12:02","02:44","05:38","06:22"],
    ["04:56","06:58","12:03","02:44","05:39","06:22"],
    ["04:56","06:59","12:03","02:44","05:40","06:22"],
    ["04:56","07:00","12:04","02:44","05:40","06:22"],
    ["04:56","07:00","12:04","02:44","05:41","06:22"],
    ["04:57","07:01","12:05","02:44","05:42","06:22"],
    ["04:57","07:02","12:05","02:44","05:43","06:22"],
    ["04:57","07:03","12:05","02:44","05:43","06:22"],
    ["04:57","07:03","12:06","02:45","05:44","06:22"],
    ["04:57","07:04","12:06","02:45","05:45","06:22"],
    ["04:57","07:05","12:07","02:45","05:45","06:23"],
    ["04:58","07:06","12:07","02:45","05:46","06:23"],
    ["04:58","07:06","12:08","02:45","05:47","06:23"],
    ["04:58","07:07","12:08","02:46","05:47","06:24"],
    ["04:59","07:07","12:09","02:46","05:48","06:24"],
    ["04:59","07:08","12:09","02:47","05:48","06:24"],
    ["04:59","07:09","12:10","02:47","05:49","06:25"],
    ["05:00","07:09","12:10","02:47","05:49","06:25"],
    ["05:00","07:10","12:11","02:48","05:50","06:26"],
    ["05:01","07:10","12:11","02:48","05:50","06:26"],
    ["05:01","07:11","12:12","02:49","05:51","06:27"],
    ["05:02","07:11","12:12","02:49","05:51","06:27"],
    ["05:02","07:12","12:13","02:50","05:52","06:28"],
    ["05:03","07:12","12:13","02:50","05:52","06:29"],
    ["05:04","07:12","12:13","02:51","05:53","06:30"],
    ["05:04","07:13","12:14","02:51","05:53","06:31"],
    ["05:05","07:13","12:14","02:52","05:53","06:31"],
    ["05:06","07:13","12:15","02:53","05:54","06:32"],
    ["05:06","07:13","12:15","02:54","05:54","06:32"],
  ],
};

// Prayer definitions
const PRAYERS = [
  { key:'fajr',    nameAr:'الفجر',   idx:0, iqamaMins:20 },
  { key:'shoroq',  nameAr:'الشروق',  idx:1, iqamaMins:null },  // no iqama
  { key:'dhuhr',   nameAr:'الظهر',   idx:2, iqamaMins:15 },
  { key:'asr',     nameAr:'العصر',   idx:3, iqamaMins:15 },
  { key:'maghrib', nameAr:'المغرب',  idx:4, iqamaMins:7  },
  { key:'isha',    nameAr:'العشاء',  idx:5, iqamaMins:15 },
];

const MONTH_NAMES = ['','يناير','فبراير','مارس','أبريل','مايو','يونيو','يوليو','أغسطس','سبتمبر','أكتوبر','نوفمبر','ديسمبر'];
const DAY_NAMES   = ['الأحد','الاثنين','الثلاثاء','الأربعاء','الخميس','الجمعة','السبت'];

function pad(n){ return String(n).padStart(2,'0'); }

// Parse "HH:MM" → total minutes
function toMins(str){
  const [h,m] = str.split(':').map(Number);
  return h*60+m;
}

// Total minutes → "HH:MM"
function fromMins(m){
  m = ((m % 1440)+1440)%1440;
  return pad(Math.floor(m/60))+':'+pad(m%60);
}

function getTodayTimes(){
  const now = new Date();
  const m = now.getMonth()+1;
  const d = now.getDate();
  const monthData = DATA[m];
  if(!monthData) return null;
  // clamp to available days
  const day = Math.min(d, monthData.length-1);
  return monthData[day] || monthData[monthData.length-1];
}

function buildCards(times){
  const list = document.getElementById('prayersList');
  list.innerHTML = '';
  PRAYERS.forEach(p=>{
    const t = times[p.idx];
    const card = document.createElement('div');
    card.className = 'prayer-card' + (p.key==='shoroq' ? ' sunrise' : '');
    card.id = 'card-'+p.key;

    let iqamaHtml = '';
    if(p.iqamaMins !== null){
      const iqamaTime = fromMins(toMins(t) + p.iqamaMins);
      iqamaHtml = `<div class="prayer-iqama-row">الإقامة بعد <span>${p.iqamaMins} دقيقة</span> &nbsp;•&nbsp; <span>${iqamaTime}</span></div>`;
    } else {
      iqamaHtml = `<div class="prayer-iqama-row" style="color:var(--text-dim);font-style:italic">لا تقام صلاة الجماعة</div>`;
    }

    // After countdown placeholder (updated by tick)
    const afterId = 'after-'+p.key;

    card.innerHTML = `
      <div class="prayer-left">
        <div class="prayer-name-ar">${p.nameAr}</div>
        ${iqamaHtml}
      </div>
      <div class="prayer-right">
        <div class="prayer-time">${t}</div>
        <div class="after-badge" id="${afterId}">—</div>
      </div>
    `;
    list.appendChild(card);
  });
}

function updateUI(){
  const now = new Date();
  // Clock
  document.getElementById('clockH').textContent = pad(now.getHours());
  document.getElementById('clockM').textContent = pad(now.getMinutes());
  document.getElementById('clockS').textContent = pad(now.getSeconds());

  // Date
  const dayName = DAY_NAMES[now.getDay()];
  const day     = now.getDate();
  const month   = MONTH_NAMES[now.getMonth()+1];
  const year    = now.getFullYear();
  document.getElementById('dateDisplay').textContent = `${dayName}  ${day} ${month} ${year}`;

  // Get today's times
  const times = getTodayTimes();
  if(!times) return;

  const nowMins = now.getHours()*60 + now.getMinutes() + now.getSeconds()/60;

  // Find active / next prayer
  let activeIdx = -1;
  let nextIdx = -1;

  // Build minute values for each prayer
  const pMins = PRAYERS.map(p=>toMins(times[p.idx]));

  for(let i=0;i<PRAYERS.length;i++){
    const start = pMins[i];
    const end   = i<PRAYERS.length-1 ? pMins[i+1] : 1440; // midnight
    if(nowMins >= start && nowMins < end){
      activeIdx = i;
      nextIdx   = i+1 < PRAYERS.length ? i+1 : 0;
      break;
    }
  }
  if(activeIdx===-1){
    // Before fajr
    nextIdx = 0;
  }

  // Update card states & after-badge
  PRAYERS.forEach((p,i)=>{
    const card = document.getElementById('card-'+p.key);
    const badge = document.getElementById('after-'+p.key);
    card.classList.remove('active','passed');

    const diffSecs = Math.round((pMins[i] - nowMins)*60);

    if(i===activeIdx){
      card.classList.add('active');
      badge.textContent = 'الآن ✦';
      badge.style.color = 'var(--gold)';
      badge.style.borderColor = 'rgba(201,168,76,0.5)';
    } else if(diffSecs > 0){
      // upcoming
      const h = Math.floor(diffSecs/3600);
      const m = Math.floor((diffSecs%3600)/60);
      const s = diffSecs%60;
      let txt = h>0 ? `بعد ${h}س ${pad(m)}د` : `بعد ${m}:${pad(s)}`;
      badge.textContent = txt;
      badge.style.color = '';
      badge.style.borderColor = '';
    } else {
      card.classList.add('passed');
      badge.textContent = 'انتهى';
      badge.style.color = 'var(--text-dim)';
    }
  });

  // Next prayer banner
  const np = PRAYERS[nextIdx];
  const npMins = pMins[nextIdx];
  let diffToNext = (npMins - nowMins)*60; // seconds
  if(diffToNext < 0) diffToNext += 86400;
  diffToNext = Math.round(diffToNext);

  const hh = Math.floor(diffToNext/3600);
  const mm = Math.floor((diffToNext%3600)/60);
  const ss = diffToNext%60;
  document.getElementById('nextName').textContent = np.nameAr;
  document.getElementById('nextCountdown').textContent = `${pad(hh)}:${pad(mm)}:${pad(ss)}`;

  if(np.iqamaMins!==null){
    document.getElementById('nextIqama').textContent = `${np.iqamaMins} دقيقة`;
  } else {
    document.getElementById('nextIqama').textContent = 'لا إقامة';
  }
}

// Check if date changed → rebuild cards
let lastBuiltDate = -1;
function maybeRebuild(){
  const now = new Date();
  const d   = now.getDate();
  if(d !== lastBuiltDate){
    lastBuiltDate = d;
    const times = getTodayTimes();
    if(times) buildCards(times);
  }
}

// Init
maybeRebuild();
updateUI();
setInterval(()=>{ maybeRebuild(); updateUI(); }, 1000);
</script>
</body>
</html>
