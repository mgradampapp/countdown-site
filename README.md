<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <title>Visszaszámláló</title>
  <style>
    body {
      font-family: Arial;
      text-align: center;
      background: #0f172a;
      color: white;
      padding-top: 80px;
    }

    .box {
      display: inline-block;
      background: #1e293b;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    }

    .countdown {
      display: flex;
      gap: 15px;
      justify-content: center;
      margin-top: 20px;
    }

    .countdown div {
      background: #334155;
      padding: 15px;
      border-radius: 10px;
      min-width: 70px;
    }

    .countdown span {
      font-size: 28px;
      font-weight: bold;
      display: block;
    }

    .label {
      font-size: 12px;
      opacity: 0.8;
    }

    .urgent {
      background: #dc2626 !important;
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

    // utolsó 24 óra
    if (diff < 1000 * 60 * 60 * 24) {
      document.querySelectorAll(".countdown div").forEach(el => {
        el.classList.add("urgent");
      });
    }

    // lejárt
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
