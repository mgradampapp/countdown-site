<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <title>Visszaszámláló</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #f97316;
      color: white;
      margin: 0;
      padding: 40px 10px;
    }

    .box {
      display: inline-block;
      background: rgba(255,255,255,0.1);
      padding: 25px;
      border-radius: 20px;
      backdrop-filter: blur(10px);
      max-width: 500px;
      width: 100%;
    }

    .countdown {
      display: flex;
      justify-content: center;
      gap: 12px;
      margin-top: 20px;
      flex-wrap: wrap;
    }

    .countdown div {
      background: rgba(0,0,0,0.2);
      padding: 15px;
      border-radius: 12px;
      min-width: 70px;
      transition: transform 0.2s ease, background 0.3s;
    }

    .countdown span {
      font-size: 26px;
      font-weight: bold;
      display: block;
    }

    .label {
      font-size: 12px;
      opacity: 0.9;
    }

    /* ✨ finom “pop” effekt */
    .tick {
      transform: scale(1.15);
    }

    /* ⚠️ utolsó 24 óra */
    .urgent {
      background: #dc2626 !important;
    }

    @media (max-width: 500px) {
      .countdown span {
        font-size: 20px;
      }
    }
  </style>
</head>
<body>

<div class="box">
  <h2>Újra a Fidesz nyer</h2>

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
