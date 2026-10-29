<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Love Note 💗</title>

<style>
:root {
  --pink: #f47d9b;
  --dark-pink: #d94f76;
  --blush: #fff0f4;
  --pale: #fff8fa;
  --ink: #633b4a;
  --muted: #936b7a;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 86px;
}

body {
  margin: 0;
  color: var(--ink);
  background: radial-gradient(circle at 10% 10%, #ffe1ea, transparent 28%),
              radial-gradient(circle at 90% 25%, #ffeaf0, transparent 24%),
              var(--pale);
  font-family: "Trebuchet MS", Arial, sans-serif;
  line-height: 1.6;
}

button, input {
  font: inherit;
}

button, .button {
  border: 0;
  border-radius: 999px;
  padding: 12px 20px;
  background: var(--pink);
  color: white;
  cursor: pointer;
  box-shadow: 0 7px 16px #d94f7630;
  transition: transform .2s, background .2s;
  text-decoration: none;
  display: inline-block;
}

button:hover, .button:hover {
  transform: translateY(-2px);
  background: var(--dark-pink);
}

.topbar {
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 14px;
  padding: 14px 5%;
  background: #fff8faed;
  backdrop-filter: blur(12px);
  border-bottom: 1px solid #f8d7e1;
}

.brand {
  font-weight: bold;
  color: var(--dark-pink);
  white-space: nowrap;
  text-decoration: none;
}

nav {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

nav a {
  color: var(--muted);
  font-size: .9rem;
  text-decoration: none;
}

nav a:hover {
  color: var(--dark-pink);
}

main {
  overflow: hidden;
}

section {
  padding: 76px 6%;
}

.hero {
  min-height: 78vh;
  display: grid;
  place-items: center;
  text-align: center;
  position: relative;
}

.hero-inner {
  max-width: 760px;
  position: relative;
  z-index: 1;
}

.eyebrow {
  color: var(--dark-pink);
  letter-spacing: .12em;
  text-transform: uppercase;
  font-size: .78rem;
  font-weight: bold;
}

h1, h2, h3, p {
  margin-top: 0;
}

h1 {
  font-family: Georgia, serif;
  font-size: clamp(2.7rem, 7vw, 5.5rem);
  line-height: 1.05;
  margin: 16px 0;
}

h1 em {
  color: var(--dark-pink);
  font-weight: normal;
}

.hero p {
  max-width: 560px;
  margin: 0 auto 25px;
  color: var(--muted);
  font-size: 1.1rem;
}

.tiny-note {
  color: var(--muted);
  font-size: .88rem;
  margin-top: 18px;
}

.float-heart {
  position: absolute;
  color: #f3a0b6;
  animation: float 5s ease-in-out infinite;
  pointer-events: none;
}

.heart1 {
  top: 18%;
  left: 12%;
  font-size: 2rem;
}

.heart2 {
  top: 30%;
  right: 13%;
  font-size: 1.4rem;
  animation-delay: -2s;
}

.heart3 {
  bottom: 17%;
  left: 20%;
  font-size: 1.1rem;
  animation-delay: -3s;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0) rotate(-8deg);
  }
  50% {
    transform: translateY(-18px) rotate(8deg);
  }
}

.section-head {
  text-align: center;
  max-width: 650px;
  margin: 0 auto 34px;
}

.section-head h2 {
  font: 2.3rem Georgia, serif;
  margin-bottom: 8px;
}

.section-head p {
  color: var(--muted);
}

.letter-wrap {
  max-width: 800px;
  margin: auto;
  background: white;
  padding: clamp(24px, 5vw, 52px);
  border: 1px solid #f7d5df;
  border-radius: 18px;
  box-shadow: 0 12px 32px #b1506f1f;
  position: relative;
}

.letter-wrap:before {
  content: "♡";
  position: absolute;
  right: 24px;
  top: 8px;
  font-size: 2.5rem;
  color: #f5b4c6;
}

.letter-wrap h3 {
  font: 1.65rem Georgia, serif;
  color: var(--dark-pink);
}

.letter-wrap p {
  white-space: pre-line;
}

.signature {
  font-family: Georgia, serif;
  font-style: italic;
  color: var(--dark-pink);
  font-size: 1.2rem;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 20px;
  max-width: 1050px;
  margin: auto;
}

.photo-card {
  background: white;
  padding: 12px 12px 18px;
  border-radius: 9px;
  box-shadow: 0 12px 32px #b1506f1f;
  transform: rotate(var(--tilt));
  transition: transform .25s;
}

.photo-card:hover {
  transform: rotate(0) translateY(-5px);
}

.photo-card img {
  display: block;
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 5px;
  background: #ffdce6;
}

.photo-card p {
  text-align: center;
  margin: 12px 0 0;
  color: var(--muted);
  font-family: Georgia, serif;
}

.upload-row {
  text-align: center;
  margin-top: 25px;
  color: var(--muted);
  font-size: .9rem;
}

input[type=file] {
  max-width: 100%;
  margin: 8px;
  color: var(--muted);
}

.reasons {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
  max-width: 1000px;
  margin: auto;
}

.reason {
  background: linear-gradient(145deg, white, #ffe9ef);
  border: 1px solid #f8d7e1;
  border-radius: 18px;
  padding: 24px 18px;
  text-align: center;
  box-shadow: 0 8px 20px #b1506f12;
}

.reason .icon {
  font-size: 1.7rem;
  display: block;
  margin-bottom: 8px;
}

.reason p {
  margin: 0;
}

.music-card {
  max-width: 680px;
  margin: auto;
  text-align: center;
  padding: 32px;
  border-radius: 22px;
  background: linear-gradient(135deg, #ffe1e9, #fff8fa);
  border: 1px solid #f5cad7;
}

.music-disc {
  width: 100px;
  height: 100px;
  margin: 0 auto 18px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  font-size: 2.2rem;
  background: repeating-radial-gradient(circle, #f5a5ba 0 7px, #ffe5ec 8px 15px);
  box-shadow: 0 12px 32px #b1506f1f;
}

.music-disc.playing {
  animation: spin 4s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.music-hint {
  color: var(--muted);
  font-size: .9rem;
}

audio {
  width: 100%;
  max-width: 450px;
  margin-top: 14px;
}

.surprise-box {
  text-align: center;
  max-width: 720px;
  margin: auto;
}

.gift {
  font-size: 5rem;
  display: block;
  margin-bottom: 12px;
  animation: float 3s ease-in-out infinite;
}

.surprise-message {
  display: none;
  margin: 24px auto 0;
  background: white;
  border: 1px dashed #ef9ab1;
  border-radius: 18px;
  padding: 28px;
  max-width: 620px;
  box-shadow: 0 12px 32px #b1506f1f;
}

.surprise-message.show {
  display: block;
  animation: pop .45s ease-out;
}

@keyframes pop {
  from {
    opacity: 0;
    transform: scale(.92);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

footer {
  text-align: center;
  padding: 28px 18px;
  background: #ffeaf0;
  color: var(--muted);
  font-size: .9rem;
}

footer strong {
  color: var(--dark-pink);
}

.confetti-heart {
  position: fixed;
  z-index: 30;
  top: -30px;
  pointer-events: none;
  animation: fall 3.5s linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(600deg);
    opacity: 0;
  }
}

@media (max-width: 760px) {
  .topbar {
    align-items: flex-start;
    flex-direction: column;
    padding: 12px 18px;
  }

  nav {
    justify-content: flex-start;
    gap: 10px 14px;
  }

  nav a {
    font-size: .82rem;
  }

  section {
    padding-top: 58px;
    padding-bottom: 58px;
  }

  .gallery {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }

  .reasons {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 12px;
  }
}

@media (max-width: 440px) {
  .gallery, .reasons {
    grid-template-columns: 1fr;
  }

  .photo-card {
    max-width: 340px;
    width: 100%;
    margin: auto;
  }

  .music-card {
    padding: 24px 16px;
  }

  h1 {
    font-size: 2.8rem;
  }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    animation-duration: .01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: .01ms !important;
  }
}
</style>
</head>

<body>

<header class="topbar">
  <a class="brand" href="#home"><span>♡</span> A Little Love Note</a>

  <nav aria-label="Main navigation">
    <a href="#home">Home</a>
    <a href="#letter">Letter</a>
    <a href="#photos">Photos</a>
    <a href="#reasons">Reasons</a>
    <a href="#music">Music</a>
    <a href="#surprise">Surprise</a>
  </nav>
</header>

<main>

  <!-- HOME -->
  <section class="hero" id="home">
    <span class="float-heart heart1">♡</span>
    <span class="float-heart heart2">♥</span>
    <span class="float-heart heart3">♡</span>

    <div class="hero-inner">
      <div class="eyebrow">A tiny corner of the internet, just for you</div>

      <h1>Hey, <em>my cutu baby.</em> 💗</h1>

      <p>
        I made this little website to remind you how loved you are.
        Every page has a tiny piece of my heart in it.
      </p>

      <a class="button" href="#letter">Open your little love letter ♡</a>

      <div class="tiny-note">
        Made with love, just for <span data-his-name>my baby</span>.
      </div>
    </div>
  </section>

  <!-- LOVE LETTER -->
  <section id="letter">
    <div class="section-head">
      <div class="eyebrow">From my heart to yours</div>
      <h2>A little love letter 💌</h2>
      <p>Some things deserve to be said more than once.</p>
    </div>

    <article class="letter-wrap">
      <h3>Dear <span data-his-name>Baby</span>,</h3>

      <p>I just wanted to remind you how much you mean to me. You make ordinary days feel special, and even the smallest moments with you become memories I want to keep.

Thank you for being someone I can laugh with, talk to, and care about so much. I hope you always remember that you matter, that you are appreciated, and that you make my world a little brighter just by being in it.

I LOVE YOU SO MUCH BUDDHU BABY. 💗</p>

      <p class="signature">
        Always sending you love,<br>
        <span data-my-name>Karan baby ♡</span>
      </p>
    </article>
  </section>

  <!-- PHOTO GALLERY -->
  
<section class="gallery" id="gallery">
  <h2>Our Little Memories 💕</h2>
  <p>Little moments, endless love.</p>

  <div class="photo-grid">
    <img src="images/photo1.jpg" alt="Our first garba together ♡">
    <img src="images/photo2.jpg" alt="The smile of yours ♡">
    <img src="images/photo3.jpg" alt="Happiest with you ♡">
    <img src="images/photo4.jpg" alt="My baby ♡"
  </div>
</section>

<style>
.gallery {
  text-align: center;
  padding: 50px 20px;
}

.gallery h2 {
  color: #c94f82;
}

.photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 18px;
  max-width: 850px;
  margin: 25px auto;
}

.photo-grid img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  border-radius: 18px;
  box-shadow: 0 5px 15px #e8a4c455;
  transition: transform 0.3s ease;
}

.photo-grid img:hover {
  transform: translateY(-5px);
}
</style>

  <!-- REASONS -->
  <section id="reasons">
    <div class="section-head">
      <div class="eyebrow">And I could list a thousand more</div>
      <h2>Reasons I love you 💗</h2>
      <p>Little things that mean more than you know.</p>
    </div>

    <div class="reasons">
      <div class="reason"><span class="icon">🌷</span><p>Hamesha mujhe rage bait karna phir pyari pyari baate karke mujhe manana.</p></div>
      <div class="reason"><span class="icon">☁️</span><p>Aapne se jada mere baare mai sochna hamesha mujhe aage rakhte ho buddhu.</p></div>
      <div class="reason"><span class="icon">🫶</span><p>Meri weird weird baate sunke hasna.</p></div>
      <div class="reason"><span class="icon">✨</span><p>Mistey ke aalawa jaise koi word tumhe aata hi na ho.</p></div>
      <div class="reason"><span class="icon">💌</span><p>Ek sath future imagine karke shaadi ke baare mai sochna.</p></div>
      <div class="reason"><span class="icon">🌙</span><p>Itna pyar karte ho mujhse itna special feel karate ho Thank you bhi kam hai uske liye.</p></div>
    </div>
  </section>

  <!-- MUSIC -->
  
<section class="music-section">
  <h2>🎶 Our Song Baby ♡</h2>
  <p>A little music, a little love, and lots of us. 💗</p>

  <div class="music-card">
    <div class="music-icon">♫</div>
    <h3>Our Song</h3>
    <p>Made sweeter because of you 💕</p>

    <audio controls loop>
      <source src="audio/love-song.mp3" type="audio/mpeg">
      Your browser does not support audio.
    </audio>
  </div>
</section>

<style>
.music-section {
  text-align: center;
  padding: 45px 20px;
}

.music-section h2 {
  color: #c94f82;
}

.music-card {
  max-width: 380px;
  margin: 25px auto;
  padding: 28px;
  border-radius: 24px;
  background: #fff0f6;
  box-shadow: 0 8px 25px #e8a4c433;
}

.music-icon {
  font-size: 48px;
  color: #d85b91;
}

.music-card audio {
  width: 100%;
  margin-top: 15px;
}
</style>


  <!-- SECRET SURPRISE -->
  <section id="surprise">
    <div class="section-head">
      <div class="eyebrow">Psst… there's one more thing</div>
      <h2>A tiny surprise 🎁</h2>
      <p>There's a message waiting just for you.</p>
    </div>

    <div class="surprise-box">
      <span class="gift" aria-hidden="true">🎀</span>

      <button id="surpriseBtn" type="button">
        Unlock your surprise ♡
      </button>

      <div class="surprise-message" id="surpriseMessage" aria-live="polite">
        <h3>Surprise! 💗</h3>

        <p>
          If I could give you one thing, it would be the chance to see
          yourself through my eyes — so you could understand how special
          you are to me.
        </p>

        <p>
          Mujhe nahi lagta mujhe koi itna pyar kar payega jitna tum mujhe karte ho baby.

        </p>

        <strong>Sending you the biggest bundle of hearts! ♡</strong>
      </div>
    </div>
  </section>

</main>

<footer>
  Made with <strong>Love ♡</strong>You deserve.<br>
  <span data-my-name>your person ♡</span> made this just for
  <span data-his-name>my baby</span>.
</footer>

<script>
  // CHANGE THESE NAMES
  const boyfriendName = "Karan baby";
  const yourName = "Mistey";

  document.querySelectorAll("[data-his-name]").forEach(el => {
    el.textContent = boyfriendName.trim() || "my favourite person";
  });

  document.querySelectorAll("[data-my-name]").forEach(el => {
    el.textContent = yourName.trim() || "your person ♡";
  });

  // PHOTO PREVIEW
  const photoUpload = document.getElementById("photoUpload");
  const photoCards = document.querySelectorAll(".photo-card");
  let photoUrls = [];

  photoUpload.addEventListener("change", () => {
    photoUrls.forEach(URL.revokeObjectURL);
    photoUrls = [];

    const files = Array.from(photoUpload.files || [])
      .filter(file => file.type.startsWith("image/"))
      .slice(0, 3);

    files.forEach((file, index) => {
      const url = URL.createObjectURL(file);
      photoUrls.push(url);

      photoCards[index].querySelector("img").src = url;

      photoCards[index].querySelector("p").textContent =
        file.name.replace(/\.[^.]+$/, "").replace(/[-_]/g, " ")
        || "A favourite memory ♡";
    });
  });

  // MUSIC PLAYER
  const musicUpload = document.getElementById("musicUpload");
  const audioPlayer = document.getElementById("audioPlayer");
  const musicDisc = document.getElementById("musicDisc");
  const musicStatus = document.getElementById("musicStatus");
  let musicUrl = null;

  musicUpload.addEventListener("change", () => {
    const file = musicUpload.files && musicUpload.files[0];
    if (!file) return;

    if (musicUrl) URL.revokeObjectURL(musicUrl);

    musicUrl = URL.createObjectURL(file);
    audioPlayer.src = musicUrl;
    audioPlayer.hidden = false;
    musicStatus.textContent = "Selected: " + file.name;
  });

  audioPlayer.addEventListener("play", () => {
    musicDisc.classList.add("playing");
  });

  audioPlayer.addEventListener("pause", () => {
    musicDisc.classList.remove("playing");
  });

  audioPlayer.addEventListener("ended", () => {
    musicDisc.classList.remove("playing");
  });

  // SECRET SURPRISE + FLOATING HEARTS
  document.getElementById("surpriseBtn").addEventListener("click", () => {
    const message = document.getElementById("surpriseMessage");
    message.classList.add("show");

    message.scrollIntoView({
      behavior: "smooth",
      block: "center"
    });

    for (let i = 0; i < 22; i++) {
      const heart = document.createElement("span");

      heart.className = "confetti-heart";
      heart.textContent = ["💗", "💕", "♡", "💖"][
        Math.floor(Math.random() * 4)
      ];

      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (16 + Math.random() * 20) + "px";
      heart.style.animationDelay = Math.random() * .8 + "s";

      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 4500);
    }
  });
</script>

</body>
</html>
