<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <title>Visszaszámláló</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;

      /* 🔥 erős, de elegáns narancs háttér */
      background: linear-gradient(135deg, #ea580c, #fb923c);
    }

    .box {
      background: rgba(0, 0, 0, 0.25);
      padding: 40px 25px;
      border-radius: 20px;
      max-width: 520px;
      width: 100%;
      text-align: center;

      backdrop-filter: blur(8px);
      box-shadow: 0 20px 50px rgba(0,0,0,0.4);
    }

    h2 {
      font-weight: 500;
      font-size: 20px;
      line-height: 1.4;
      margin-bottom: 30px;
      opacity: 0.95;
    }

    .countdown {
      display: flex;
      justify-content: center;
      gap: 14px;
      flex-wrap: wrap;
    }

    .countdown div {
      background: rgba(0,0,0,0.35);
      padding: 18px 16px;
      border-radius: 14px;
      min-width: 75px;

      transition: transform 0.2s ease, background 0.3s;
    }

    .countdown span {
      font-size: 28px;
      font-weight: 600;
      display: block;
      letter-spacing: 1px;

      /* ✨ enyhe glow */
      text-shadow: 0 0 10px rgba(255,255,255,0.4);
    }

    .label {
      font-size: 11px;
      opacity: 0.8;
      margin-top: 4px;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* finom számváltás */
    .tick {
      transform: scale(1.12);
    }

    /* ⚠️ utolsó 24 óra */
    .urgent {
      background: rgba(153, 27, 27, 0.9) !important;
    }

    @media (max-width: 500px) {
      .box {
        padding: 30px 15px;
      }

      .countdown span {
        font-size: 22px;
      }

      h2 {
        font-size: 18px;
      }
    }
  </style>
</head>
<body>

<div class="box">
  <h2>Meddig kell várni, hogy újra a békepárti Fidesz legyen hatalmon:</h2>

  <div class="countdown" id="countdown">
    <div id="d"><span id="days">0</span><div class="label">nap</div></div>
    <div id="h"><span id="hours">0</span><div class="label">óra</div></div>
    <div id="m"><span id="minutes">0</span><div class="label">perc</div></div>
    <div id="s"><span id="seconds">0</span><div class="label">mp</div></div>
  </div>

  <div id="message"></div>
</div>

<script>
  const target = new Date("2030-04-14T23:59:00").getTime();

  let last = { d: null, h: null, m: null, s: null };

  function animate(id) {
    const el = document.getElementById(id);
    el.classList.add("tick");
    setTimeout(() => el.classList.remove("tick"), 200);
  }

  function update() {
    const now = new Date().getTime();
    const diff = target - now;

    const d = Math.floor(diff / (1000 * 60 * 60 * 24));
    const h = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const m = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    const s = Math.floor((diff % (1000 * 60)) / 1000);

    if (d !== last.d) animate("d");
    if (h !== last.h) animate("h");
    if (m !== last.m) animate("m");
    if (s !== last.s) animate("s");

    last = { d, h, m, s };

    document.getElementById("days").innerText = d;
    document.getElementById("hours").innerText = h;
    document.getElementById("minutes").innerText = m;
    document.getElementById("seconds").innerText = s;

    if (diff < 1000 * 60 * 60 * 24) {
      document.querySelectorAll(".countdown div").forEach(el => {
        el.classList.add("urgent");
      });
    }

    if (diff < 0) {
      document.getElementById("countdown").style.display = "none";
      document.getElementById("message").innerHTML = "<h2>🎉 ELINDULT! 🎉</h2>";
    }
  }

  setInterval(update, 1000);
  update();
</script>

</body>
</html>
