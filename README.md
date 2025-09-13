
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Undangan Gathering Sahabat IRMA</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet" />

<style>
  /* --- Bagian CSS yang sebelumnya sudah ada --- */
  /* ... (potongan kode CSS sebelumnya tetap sama) ... */

  /* Tombol RSVP */
  .rsvp-btn {
    display: inline-block;
    margin: 2rem auto 0;
    padding: 0.9rem 2rem;
    font-size: 1.1rem;
    font-weight: 600;
    color: #fff;
    background: linear-gradient(135deg, #25D366, #128C7E);
    border-radius: 50px;
    text-decoration: none;
    text-align: center;
    transition: all 0.3s ease;
    box-shadow: 0 0 12px rgba(37, 211, 102, 0.6);
    animation: pulseWA 2s infinite;
  }
  .rsvp-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 0 20px rgba(37, 211, 102, 0.9);
  }

  @keyframes pulseWA {
    0%, 100% { box-shadow: 0 0 12px rgba(37, 211, 102, 0.6); }
    50% { box-shadow: 0 0 22px rgba(37, 211, 102, 0.9); }
  }
</style>
</head>
<body>

<!-- Overlay Intro -->
<div id="convety-overlay">
  <h1>Selamat Datang!</h1>
  <p>Undangan Gathering Sahabat IRMA</p>
</div>

<div class="container">
  <h1>Gathering & Outbound</h1>
  <h2>Sahabat IRMA</h2>

  <!-- Countdown -->
  <div class="countdown" id="countdown">
    <div class="time-box"><span id="days">0</span><small>Hari</small></div>
    <div class="time-box"><span id="hours">0</span><small>Jam</small></div>
    <div class="time-box"><span id="minutes">0</span><small>Menit</small></div>
    <div class="time-box"><span id="seconds">0</span><small>Detik</small></div>
  </div>

  <p>Assalamu’alaikum Warahmatullahi Wabarakatuh,</p>

  <p>Dengan penuh semangat dan kebersamaan, Panitia Gathering Masjid Darul Iman mengundang Sahabat IRMA untuk hadir dalam acara <strong>Gathering & Outbound</strong> yang akan menjadi momen berharga untuk mempererat tali silaturahmi dan menikmati suasana alam yang menyegarkan.</p>

  <p><span class="highlight">Dresscode:</span> Atasan hitam kaos, bawahan hitam celana panjang. Jangan lupa membawa baju dan celana cadangan agar tetap nyaman selama kegiatan berlangsung.</p>

  <p><span class="highlight">Waktu & Tanggal:</span> Pukul 08:00 - 15:00, <time datetime="2025-09-14T08:00:00">14 September 2025</time></p>

  <p><span class="highlight">Lokasi:</span> 
    <a href="https://maps.app.goo.gl/t7p2FZ4JPdKgNfyLA?g_st=aw" target="_blank" rel="noopener" class="location-link">
      Binalatung Beach, Tarakan Timur, Tarakan City
    </a>
  </p>

  <p>Kami sangat menantikan kehadiran Sahabat IRMA untuk bersama-sama menciptakan kenangan indah dan memperkuat ukhuwah.</p>

  <p>Wassalamu’alaikum Warahmatullahi Wabarakatuh,<br/>Panitia Gathering Masjid Darul Iman</p>

  <div class="footer">"Bersama kita kuat, bersama kita bahagia."</div>

  <!-- Tombol RSVP -->
  <div style="text-align:center;">
    <a href="https://wa.me/6281234567890?text=Assalamu%27alaikum%2C%20saya%20ingin%20konfirmasi%20kehadiran%20Gathering%20Sahabat%20IRMA." 
       target="_blank" class="rsvp-btn" aria-label="Konfirmasi Kehadiran via WhatsApp">
       ✅ Konfirmasi Kehadiran via WhatsApp
    </a>
  </div>
</div>

<!-- Musik Background -->
<audio id="bg-music" autoplay loop preload="auto">
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_1a1a7a7a7a.mp3?filename=chill-out-ambient-11043.mp3" type="audio/mpeg">
</audio>

<script>
  // Musik
  window.addEventListener('load', () => {
    const audio = document.getElementById('bg-music');
    if(audio) {
      audio.volume = 0.15;
      audio.play().catch(() => console.log("Autoplay dicegah browser"));
    }
  });

  // Countdown
  const eventDate = new Date("2025-09-14T08:00:00").getTime();
  const countdown = document.getElementById("countdown");

  function updateCountdown() {
    const now = new Date().getTime();
    const diff = eventDate - now;

    if (diff <= 0) {
      countdown.innerHTML = "<p style='text-align:center; font-size:1.3rem; color:#ffd700; font-weight:600;'>Acara Sedang Berlangsung 🎉</p>";
      clearInterval(timer);
      return;
    }

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((diff % (1000 * 60)) / 1000);

    document.getElementById("days").textContent = days;
    document.getElementById("hours").textContent = hours;
    document.getElementById("minutes").textContent = minutes;
    document.getElementById("seconds").textContent = seconds;
  }

  const timer = setInterval(updateCountdown, 1000);
  updateCountdown();
</script>
</body>
</html>
