
 Sorry-manasa
Sorry
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>I'm Sorry Manasa 💔</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Nunito:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: linear-gradient(135deg, #fff0f6 0%, #fce4ff 50%, #ffecd2 100%);
    font-family: 'Nunito', sans-serif;
    overflow-x: hidden;
    min-height: 100vh;
  }

  /* ── Floating emojis ── */
  .floaters {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
  }
  .floater {
    position: absolute;
    animation: floatUp linear infinite;
    opacity: 0;
    font-size: 1.8rem;
  }
  @keyframes floatUp {
    0%   { transform: translateY(105vh) rotate(0deg); opacity: 0; }
    10%  { opacity: 0.8; }
    90%  { opacity: 0.8; }
    100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
  }

  .page {
    position: relative;
    z-index: 1;
    text-align: center;
    padding: 36px 16px 80px;
  }

  /* ── Bear ── */
  .bear-wrap {
    display: inline-block;
    animation: bearBounce 0.7s ease-in-out infinite alternate;
    font-size: 5.5rem;
    filter: drop-shadow(0 8px 18px rgba(255,107,157,0.4));
    position: relative;
  }
  @keyframes bearBounce {
    from { transform: translateY(0) rotate(-6deg) scale(1); }
    to   { transform: translateY(-16px) rotate(6deg) scale(1.05); }
  }

  .tear {
    position: absolute;
    font-size: 1.1rem;
    animation: tearDrop 1s ease-in infinite;
    opacity: 0;
  }
  .tear:nth-child(2) { left: 28%; top: 60%; animation-delay: 0s; }
  .tear:nth-child(3) { left: 55%; top: 60%; animation-delay: 0.5s; }
  @keyframes tearDrop {
    0%   { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(30px); opacity: 0; }
  }

  /* ── Title ── */
  .title {
    font-family: 'Pacifico', cursive;
    font-size: 2.6rem;
    background: linear-gradient(90deg, #ff6b9d, #c77dff, #ff9a3c, #ff6b9d);
    background-size: 300% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shimmer 2.5s linear infinite;
    margin: 20px 0 6px;
    line-height: 1.2;
  }
  @keyframes shimmer {
    to { background-position: 300% center; }
  }

  .name-highlight {
    font-family: 'Pacifico', cursive;
    font-size: 3rem;
    background: linear-gradient(90deg, #c77dff, #ff6b9d);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    display: block;
    animation: namePop 2s ease-in-out infinite alternate;
  }
  @keyframes namePop {
    from { transform: scale(1); }
    to   { transform: scale(1.06); }
  }

  /* ── Photo card ── */
  .photo-card {
    width: 160px;
    height: 160px;
    border-radius: 50%;
    margin: 24px auto 0;
    border: 5px solid #ff6b9d;
    box-shadow: 0 0 0 8px #ffd6e7, 0 10px 30px rgba(255,107,157,0.3);
    overflow: hidden;
    animation: pulseRing 2s ease-in-out infinite;
    background: linear-gradient(135deg, #ffd6e7, #fce4ff);
    display: flex; align-items: center; justify-content: center;
    font-size: 5rem;
    cursor: pointer;
    transition: transform 0.3s;
  }
  .photo-card:hover { transform: scale(1.08) rotate(3deg); }
  @keyframes pulseRing {
    0%,100% { box-shadow: 0 0 0 8px #ffd6e7, 0 10px 30px rgba(255,107,157,0.3); }
    50%      { box-shadow: 0 0 0 16px #ffd6e7, 0 10px 36px rgba(255,107,157,0.5); }
  }
  .photo-card img { width: 100%; height: 100%; object-fit: cover; }

  .upload-hint {
    font-size: 0.75rem;
    color: #c77dff;
    font-weight: 700;
    margin-top: 8px;
    opacity: 0.8;
  }

  /* ── Sorry letter ── */
  .sorry-box {
    background: white;
    border-radius: 28px;
    padding: 30px 22px 24px;
    margin: 32px auto;
    max-width: 400px;
    box-shadow: 0 8px 32px rgba(255,107,157,0.18);
    border: 2px solid #ffd6e7;
    position: relative;
  }
  .sorry-box::before {
    content: '💌';
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 2.4rem;
    animation: letterBounce 1.5s ease-in-out infinite alternate;
  }
  @keyframes letterBounce {
    from { transform: translateX(-50%) translateY(0) rotate(-5deg); }
    to   { transform: translateX(-50%) translateY(-6px) rotate(5deg); }
  }
  .sorry-box h2 {
    font-family: 'Pacifico', cursive;
    color: #ff6b9d;
    font-size: 1.5rem;
    margin-bottom: 16px;
  }
  .sorry-box p {
    color: #666;
    font-size: 0.96rem;
    line-height: 1.75;
    margin-bottom: 10px;
  }
  .sorry-box p .pink { color: #ff6b9d; font-weight: 900; }
  .sorry-box p .purple { color: #c77dff; font-weight: 900; }

  /* ── Main sorry button ── */
  .btn-sorry {
    display: inline-block;
    background: linear-gradient(135deg, #ff6b9d, #c77dff);
    color: white;
    font-family: 'Nunito', sans-serif;
    font-size: 1.1rem;
    font-weight: 900;
    padding: 14px 38px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    box-shadow: 0 6px 20px rgba(255,107,157,0.45);
    animation: wiggle 1.8s ease-in-out infinite;
    margin-top: 12px;
    letter-spacing: 0.5px;
  }
  @keyframes wiggle {
    0%,100% { transform: rotate(-3deg) scale(1); }
    50%      { transform: rotate(3deg) scale(1.08); }
  }

  /* ── She loves section ── */
  .loves-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.5rem;
    color: #c77dff;
    margin: 40px 0 20px;
  }

  .loves-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    max-width: 360px;
    margin: 0 auto;
  }

  .love-card {
    background: white;
    border-radius: 18px;
    padding: 16px 6px 12px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.07);
    transition: transform 0.2s, box-shadow 0.2s;
    border: 2px solid transparent;
  }
  .love-card:hover {
    transform: scale(1.12) rotate(-3deg);
    box-shadow: 0 8px 24px rgba(255,107,157,0.25);
    border-color: #ff6b9d;
  }
  .love-card .lc-emoji {
    font-size: 2.5rem;
    display: block;
    margin-bottom: 6px;
    animation: popBounce 2.5s ease-in-out infinite;
  }
  .love-card:nth-child(1) .lc-emoji { animation-delay: 0s; }
  .love-card:nth-child(2) .lc-emoji { animation-delay: 0.4s; }
  .love-card:nth-child(3) .lc-emoji { animation-delay: 0.8s; }
  .love-card:nth-child(4) .lc-emoji { animation-delay: 1.2s; }
  .love-card:nth-child(5) .lc-emoji { animation-delay: 1.6s; }
  .love-card:nth-child(6) .lc-emoji { animation-delay: 2s; }
  @keyframes popBounce {
    0%,70%,100% { transform: scale(1); }
    75% { transform: scale(1.35) rotate(-8deg); }
    85% { transform: scale(1.35) rotate(8deg); }
    95% { transform: scale(1.1); }
  }
  .love-card .lc-label {
    font-size: 0.72rem;
    color: #999;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  /* ── Excuse generator ── */
  .funny-section {
    margin: 40px auto;
    max-width: 400px;
    padding: 0 4px;
  }
  .funny-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.3rem;
    color: #ff6b9d;
    margin-bottom: 16px;
  }
  .excuse-box {
    background: linear-gradient(135deg, #fff8f0, #ffd6e7);
    border-radius: 20px;
    padding: 22px 18px;
    box-shadow: 0 4px 16px rgba(255,107,157,0.12);
    font-size: 1rem;
    color: #555;
    font-weight: 700;
    min-height: 80px;
    display: flex; align-items: center; justify-content: center;
    border: 2px dashed #ff6b9d;
    line-height: 1.5;
    transition: all 0.4s;
    margin-bottom: 14px;
    cursor: default;
  }
  .excuse-box.pop {
    animation: boxPop 0.4s ease;
  }
  @keyframes boxPop {
    0%  { transform: scale(0.95); }
    60% { transform: scale(1.04); }
    100%{ transform: scale(1); }
  }

  .btn-excuse {
    background: linear-gradient(135deg, #ff6b9d, #ffb347);
    color: white;
    border: none;
    padding: 13px 30px;
    border-radius: 50px;
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 1rem;
    cursor: pointer;
    box-shadow: 0 5px 18px rgba(255,107,157,0.35);
    transition: transform 0.15s;
  }
  .btn-excuse:active { transform: scale(0.95); }

  /* ── Hearts explosion ── */
  .hearts-section {
    margin: 40px auto 0;
    max-width: 400px;
  }
  .hearts-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.3rem;
    color: #c77dff;
    margin-bottom: 16px;
  }
  .heart-row {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
  }
  .heart {
    font-size: 2rem;
    cursor: pointer;
    transition: transform 0.2s;
    animation: heartbeat 1.4s ease-in-out infinite;
    display: inline-block;
  }
  .heart:nth-child(1) { animation-delay: 0s; }
  .heart:nth-child(2) { animation-delay: 0.2s; }
  .heart:nth-child(3) { animation-delay: 0.4s; }
  .heart:nth-child(4) { animation-delay: 0.6s; }
  .heart:nth-child(5) { animation-delay: 0.8s; }
  .heart:nth-child(6) { animation-delay: 1.0s; }
  .heart:nth-child(7) { animation-delay: 1.2s; }
  @keyframes heartbeat {
    0%,100% { transform: scale(1); }
    14%     { transform: scale(1.3); }
    28%     { transform: scale(1); }
    42%     { transform: scale(1.2); }
    70%     { transform: scale(1); }
  }
  .heart:hover { transform: scale(1.5) rotate(10deg) !important; }

  /* ── Footer ── */
  .footer {
    margin-top: 50px;
    font-family: 'Pacifico', cursive;
    font-size: 1.1rem;
    color: #ff6b9d;
    opacity: 0.7;
    animation: fadePulse 2s ease-in-out infinite alternate;
  }
  @keyframes fadePulse {
    from { opacity: 0.5; }
    to   { opacity: 1; }
  }

  /* ── Confetti burst ── */
  .confetti-container {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 999;
  }
  .conf {
    position: absolute;
    width: 10px; height: 10px;
    border-radius: 2px;
    animation: confettiFall 1.8s ease-in forwards;
    opacity: 0;
  }
  @keyframes confettiFall {
    0%  { transform: translateY(-20px) rotate(0deg); opacity: 1; }
    100%{ transform: translateY(100vh) rotate(720deg); opacity: 0; }
  }

  /* ── Yes/No buttons ── */
  .yesno-section {
    margin: 32px auto;
    max-width: 400px;
  }
  .yesno-title {
    font-family: 'Pacifico', cursive;
    font-size: 1.2rem;
    color: #7b3f00;
    margin-bottom: 18px;
  }
  .yesno-btns {
    display: flex;
    gap: 14px;
    justify-content: center;
    align-items: center;
  }
  #btn-yes {
    background: linear-gradient(135deg, #ff6b9d, #c77dff);
    color: white;
    border: none;
    padding: 14px 34px;
    border-radius: 50px;
    font-family: 'Nunito', sans-serif;
    font-weight: 900;
    font-size: 1.1rem;
    cursor: pointer;
    box-shadow: 0 5px 18px rgba(255,107,157,0.35);
    transition: transform 0.15s;
  }
  #btn-yes:hover { transform: scale(1.08); }
  #btn-no {
    background: #f0f0f0;
    color: #999;
    border: none;
    padding: 10px 22px;
    border-radius: 50px;
    font-family: 'Nunito', sans-serif;
    font-weight: 700;
    font-size: 0.9rem;
    cursor: pointer;
    transition: all 0.2s;
  }
  .response-msg {
    margin-top: 18px;
    font-family: 'Pacifico', cursive;
    font-size: 1.4rem;
    color: #ff6b9d;
    min-height: 40px;
    animation: popIn 0.4s ease;
  }
  @keyframes popIn {
    from { transform: scale(0.7); opacity: 0; }
    to   { transform: scale(1); opacity: 1; }
  }
</style>
</head>
<body>

<!-- Floating background emojis -->
<div class="floaters" id="floaters"></div>
<div class="confetti-container" id="confetti"></div>

<div class="page">

  <!-- Bear + tears -->
  <div class="bear-wrap">
    🐻
    <span class="tear">💧</span>
    <span class="tear">💧</span>
  </div>

  <!-- Title -->
  <h1 class="title">
    I'm So Sorry my little
   cute manasa<br>
    <span class="name-highlight">Manasa 💕</span>
  </h1>

  <!-- Photo -->
  <div class="photo-card" id="photoCard" onclick="document.getElementById('photoInput').click()">
    👧
  </div>
  <input type="file" id="photoInput" accept="image/*" style="display:none" onchange="loadPhoto(event)">
  <p class="upload-hint">📸 Tap to add Manasa's photo</p>

  <!-- Sorry letter -->
  <div class="sorry-box">
    <h2>Dear Manasa,</h2>
    <p>I know I messed up and I'm <span class="pink">truly, deeply sorry</span>. 😔</p>
    <p>You are the most <span class="purple">amazing, kind, and beautiful</span> person I know — and you deserve so much better than my mistake.plz don't leave me <span class="blue">I promise you that I will be for you until my last breath</span> <span class="pink">[18-02-2025]</span> </p>
    <p>Please forgive me? I promise to make it up to you with <span class="pink">chocolates 🍫, ice cream 🍦</span> and all the cute pets you want 🐾.</p>
    <p>You mean the <span class="purple">whole world</span> to me, Manasa. 🌍💕</p>
    <button class="btn-sorry" onclick="launchConfetti()">💖 Please Forgive Me!</button>
  </div>

  <!-- Things she loves -->
  <div class="loves-title">✨ Things Manasa Loves ✨</div>
  <div class="loves-grid">
    <div class="love-card">
      <span class="lc-emoji">🐾</span>
      <span class="lc-label">Pets</span>
    </div>
    <div class="love-card">
      <span class="lc-emoji">🍫</span>
      <span class="lc-label">Chocolates</span>
    </div>
    <div class="love-card">
      <span class="lc-emoji">🍦</span>
      <span class="lc-label">Ice Cream</span>
    </div>
    <div class="love-card">
      <span class="lc-emoji">🐶</span>
      <span class="lc-label">Cute Dogs</span>
    </div>
    <div class="love-card">
      <span class="lc-emoji">🌸</span>
      <span class="lc-label">Flowers</span>
    </div>
    <div class="love-card">
      <span class="lc-emoji">💕</span>
      <span class="lc-label">Love</span>
    </div>
  </div>

  <!-- Funny excuse generator -->
  <div class="funny-section">
    <div class="funny-title">😂 My Excuse Generator</div>
    <div class="excuse-box" id="excuseBox">
      Press the button to hear my amazing excuse... 👇
    </div>
    <button class="btn-excuse" onclick="newExcuse()">🎲 Give Me An Excuse!</button>
  </div>

  <!-- Yes/No question -->
  <div class="yesno-section">
    <div class="yesno-title">So... are we okay? 🥺</div>
    <div class="yesno-btns">
      <button id="btn-yes" onclick="sayYes()">💖 Yes!</button>
      <button id="btn-no" onmouseover="runAway()" onclick="runAway()">No</button>
    </div>
    <div class="response-msg" id="responseMsg"></div>
  </div>

  <!-- Heartbeat row -->
  <div class="hearts-section">
    <div class="hearts-title">Tap a heart for Manasa 💜</div>
    <div class="heart-row">
      <span class="heart" onclick="popHeart(this)">❤️</span>
      <span class="heart" onclick="popHeart(this)">💜</span>
      <span class="heart" onclick="popHeart(this)">💛</span>
      <span class="heart" onclick="popHeart(this)">💙</span>
      <span class="heart" onclick="popHeart(this)">🧡</span>
      <span class="heart" onclick="popHeart(this)">💚</span>
      <span class="heart" onclick="popHeart(this)">🩷</span>
    </div>
  </div>

  <div class="footer">Made with 💗 just for Manasa</div>
</div>

<script>
  // ── Floating emojis ──
  const emojis = ['🍫','🍦','🐾','💕','🌸','🐶','🍭','🧸','🌺','💝','🍬','🐱','💐'];
  const floaters = document.getElementById('floaters');
  function spawnFloater() {
    const el = document.createElement('div');
    el.className = 'floater';
    el.textContent = emojis[Math.floor(Math.random() * emojis.length)];
    el.style.left = Math.random() * 100 + 'vw';
    const dur = 6 + Math.random() * 8;
    el.style.animationDuration = dur + 's';
    el.style.animationDelay = Math.random() * 3 + 's';
    el.style.fontSize = (1.2 + Math.random() * 1.4) + 'rem';
    floaters.appendChild(el);
    setTimeout(() => el.remove(), (dur + 3) * 1000);
  }
  setInterval(spawnFloater, 600);

  // ── Photo upload ──
  function loadPhoto(e) {
    const file = e.target.files[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = function(ev) {
      const card = document.getElementById('photoCard');
      card.innerHTML = '<img src="' + ev.target.result + '" alt="Manasa">';
    };
    reader.readAsDataURL(file);
  }

  // ── Excuse generator ──
  const excuses = [
    "I was abducted by aliens 👽 and they didn't let me apologize until now!",
    "A chocolate 🍫 told me to do it. I can't say no to chocolate. You understand.",
    "My brain went on vacation 🧳 without telling me. It's back now. Mostly.",
    "I was training to be a better boyfriend and… the training was going badly. 😅",
    "A cute dog 🐶 distracted me! You know I can't resist cute things — like you!",
    "My heart was sending the right signals but my mouth went rogue. Sorry! 😬",
    "I was testing how forgiving you are. You're passing with flying colors! 🌈",
    "Mercury was in retrograde and I fully blame the planets. 🪐",
    "I sneezed and accidentally caused the whole problem. True story. 🤧",
    "A cat 🐱 stole my good judgment. I've filed a complaint. Please forgive me."
    "really i don't wanna lose you bcoz i truely loved with my heart manasa.💖💝💘."
  ];
  let lastIdx = -1;
  function newExcuse() {
    let idx;
    do { idx = Math.floor(Math.random() * excuses.length); } while (idx === lastIdx);
    lastIdx = idx;
    const box = document.getElementById('excuseBox');
    box.textContent = excuses[idx];
    box.classList.remove('pop');
    void box.offsetWidth;
    box.classList.add('pop');
  }

  // ── Yes / No ──
  let noClicks = 0;
  function sayYes() {
    document.getElementById('responseMsg').textContent = '🎉 Yaaay!! I love you Manasa! 💖';
    launchConfetti();
    launchConfetti();
  }
  function runAway() {
    noClicks++;
    const btn = document.getElementById('btn-no');
    const msgs = ['😢','😭','🥺','Please...','Nooo!!','I really need you!','Pleaseee 🙏'];
    const msg = msgs[Math.min(noClicks - 1, msgs.length - 1)];
    document.getElementById('responseMsg').textContent = msg;
    const maxX = window.innerWidth - 100;
    const maxY = document.body.scrollHeight - 100;
    btn.style.position = 'fixed';
    btn.style.left = Math.random() * (maxX - 60) + 'px';
    btn.style.top  = Math.random() * (window.innerHeight - 60) + 'px';
    btn.style.zIndex = 999;
  }

  // ── Heart pop ──
  function popHeart(el) {
    el.style.transform = 'scale(2) rotate(15deg)';
    setTimeout(() => el.style.transform = '', 300);
    launchConfetti(8);
  }

  // ── Confetti ──
  const confColors = ['#ff6b9d','#c77dff','#ffb347','#80ffdb','#ffd6e7','#ff9a3c'];
  function launchConfetti(count = 40) {
    const container = document.getElementById('confetti');
    for (let i = 0; i < count; i++) {
      const c = document.createElement('div');
      c.className = 'conf';
      c.style.left = (20 + Math.random() * 60) + 'vw';
      c.style.top = '-10px';
      c.style.background = confColors[Math.floor(Math.random() * confColors.length)];
      c.style.borderRadius = Math.random() > 0.5 ? '50%' : '2px';
      c.style.width  = (6 + Math.random() * 8) + 'px';
      c.style.height = (6 + Math.random() * 8) + 'px';
      c.style.animationDuration = (1 + Math.random() * 1.2) + 's';
      c.style.animationDelay = (Math.random() * 0.5) + 's';
      container.appendChild(c);
      setTimeout(() => c.remove(), 2500);
    }
  }
</script>
</body>
</html
