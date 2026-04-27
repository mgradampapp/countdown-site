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

    h2 {
      margin: 10px 0;
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
      animation: pulse 2s infinite;
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

    /* 💓 pulzáló animáció */
    @keyframes pulse {
      0% {
        transform: scale(1);
        box-shadow: 0 0 0 rgba(0,0,0,0.2);
      }
      50% {
        transform: scale(1.08);
        box-shadow: 0 0 20px rgba(0,0,0,0.4);
      }
      100% {
        transform: scale(1);
        box-shadow: 0 0 0 rgba(0,0,0,0.2);
      }
    }

    /* ⚠️ utolsó 24 óra */
    .urgent {
      background: #dc2626 !important;
      animation: pulseFast 1s infinite;
    }

    @keyframes pulseFast {
      0% { transform: scale(1); }
      50% { transform: scale(1.12); }
      100% { transform: scale(1); }
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
    <div><span id="days">0</span><div class="label">nap</div></div>
    <div><span id="hours">0</span><div class="label">óra</div></div>
    <div><span id="minutes">0</span><div class="label">perc</div></div>
    <div><span id="seconds">0</span><div class="label">mp</div></div>
  </div>

  <div id="message"></div>
</div>

<script>
  const target = new Date("2030-04-14T23:59:00").getTime();

  function update() {
    const now = new Date().getTime();
    const diff = target - now;

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((diff % (1000 * 60)) / 1000);

    document.getElementById("days").innerText = days;
    document.getElementById("hours").innerText = hours;
    document.getElementById("minutes").innerText = minutes;
    document.getElementById("seconds").innerText = seconds;

    // ⚠️ utolsó 24 óra
    if (diff < 1000 * 60 * 60 * 24) {
      document.querySelectorAll(".countdown div").forEach(el => {
        el.classList.add("urgent");
      });
    }

    // 🎉 lejárt
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
