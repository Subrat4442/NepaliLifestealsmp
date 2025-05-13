Nepali smp
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nepali Lifesteal SMP</title>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@500&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Kanit', sans-serif;
      color: white;
      background: linear-gradient(to bottom, rgba(0,0,0,0.7), rgba(0,0,0,0.9)), 
                  url('https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Mt._Machhapuchhre.jpg/1920px-Mt._Machhapuchhre.jpg') no-repeat center center fixed;
      background-size: cover;
      overflow-x: hidden;
    }

    body::after {
      content: "";
      background: url('https://wallpapercave.com/wp/wp2757874.png') no-repeat center bottom;
      background-size: cover;
      opacity: 0.08;
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      z-index: 0;
      pointer-events: none;
    }

    header, main, footer {
      position: relative;
      z-index: 1;
    }

    header {
      text-align: center;
      padding: 2rem 1rem;
      background: rgba(0, 0, 0, 0.6);
      backdrop-filter: blur(6px);
      border-bottom: 2px solid #ff4d4d;
      box-shadow: 0 4px 20px rgba(255, 77, 77, 0.3);
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
      text-shadow: 2px 2px 8px #000;
      animation: fadeInDown 1s ease-out;
    }

    p {
      animation: fadeIn 1.5s ease-out;
    }

    main {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      padding: 3rem 2rem;
    }

    .card {
      background: linear-gradient(135deg, rgba(0,0,0,0.7), rgba(30,30,30,0.6));
      border: 2px solid rgba(255, 77, 77, 0.5);
      border-radius: 15px;
      padding: 1.5rem;
      width: 300px;
      max-width: 90%;
      box-shadow: 0 0 20px rgba(255, 77, 77, 0.2);
      transition: all 0.4s ease;
      animation: fadeUp 1s ease forwards;
      opacity: 0;
    }

    .card:nth-child(1) { animation-delay: 0.2s; }
    .card:nth-child(2) { animation-delay: 0.4s; }
    .card:nth-child(3) { animation-delay: 0.6s; }
    .card:nth-child(4) { animation-delay: 0.8s; }

    .card:hover {
      transform: scale(1.04);
      box-shadow: 0 0 40px rgba(255, 77, 77, 0.6);
    }

    .card h2 {
      color: #ff4d4d;
      margin-top: 0;
      font-size: 1.8rem;
      text-shadow: 1px 1px 5px #000;
    }

    .features, .rules {
      text-align: left;
      padding-left: 1rem;
    }

    .ip-container {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 1rem 0;
    }

    .ip-box {
      font-size: 1.2rem;
      padding: 0.8rem 1.2rem;
      background-color: rgba(0, 0, 0, 0.6);
      border-radius: 10px;
      border: 1px solid #ff4d4d;
      box-shadow: inset 0 0 10px rgba(255, 77, 77, 0.2);
      flex-grow: 1;
    }

    .copy-btn {
      padding: 0.6rem 1rem;
      background: linear-gradient(45deg, #ff4d4d, #ff7373);
      color: white;
      border: none;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(255, 77, 77, 0.5);
      transition: 0.3s ease;
    }

    .copy-btn:hover {
      background: linear-gradient(45deg, #ff7373, #ff4d4d);
      box-shadow: 0 0 20px rgba(255, 77, 77, 0.8);
      transform: scale(1.05);
    }

    .toast {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(0, 0, 0, 0.85);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      font-weight: bold;
      z-index: 1000;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
    }

    .toast.show {
      opacity: 1;
      pointer-events: auto;
    }

    .socials a {
      display: inline-block;
      margin: 0.3rem 0.5rem;
      padding: 0.5rem 1rem;
      text-decoration: none;
      color: white;
      font-weight: bold;
      background: linear-gradient(45deg, #ff4d4d, #ff7373);
      border-radius: 8px;
      transition: 0.3s ease;
      box-shadow: 0 0 12px rgba(255, 77, 77, 0.5);
    }

    .socials a:hover {
      background: linear-gradient(45deg, #ff7373, #ff4d4d);
      box-shadow: 0 0 25px rgba(255, 77, 77, 0.8);
      transform: scale(1.05);
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      margin-top: 2rem;
    }

    .gallery img {
      width: 300px;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.5);
      transition: transform 0.3s ease;
      animation: fadeIn 2s ease forwards;
      opacity: 0;
    }

    .gallery img:hover {
      transform: scale(1.05);
    }

    footer {
      text-align: center;
      margin-top: 4rem;
      padding: 2rem;
      font-size: 0.9rem;
      color: #ccc;
      background: rgba(0, 0, 0, 0.4);
      border-top: 1px solid #ff4d4d;
    }

    hr {
      border: none;
      height: 1px;
      background: #fff;
      opacity: 0.1;
      margin: 0.8rem 0;
    }

    @keyframes fadeInDown {
      0% {
        transform: translateY(-40px);
        opacity: 0;
      }
      100% {
        transform: translateY(0);
        opacity: 1;
      }
    }

    @keyframes fadeUp {
      to {
        transform: translateY(0);
        opacity: 1;
      }
      from {
        transform: translateY(40px);
        opacity: 0;
      }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>

  <header>
    <h1>💔 Nepali Lifesteal SMP 🇳🇵</h1>
    <p>Where PvP means power — steal hearts, dominate, and survive</p>
  </header>

  <main>
    <div class="card">
      <h2>🔪 What is Lifesteal SMP?</h2>
      <ul class="features">
        <li>❤️ Kill players to steal their hearts</li>
        <li>⚰️ Lose all hearts? You're banned (for a time)</li>
        <li>🛡️ Hardcore survival meets PvP strategy</li>
        <li>🏰 Build, raid, and defend your base</li>
        <li>🌐 24/7 Online | Low Lag | Hosted in Asia</li>
      </ul>
    </div>

    <div class="card">
      <h2>📜 Rules</h2>
      <ul class="rules">
        <li>❌ No hacking or unfair mods (instant ban)</li>
        <li>🤝 Respect allies & enemies alike</li>
        <li>🔥 Griefing/raiding allowed — it’s Lifesteal!</li>
        <li>📢 No spam or advertising</li>
        <li>🎮 Play fair, fight smart, and have fun</li>
      </ul>
    </div>

    <div class="card">
      <h2>🌐 Join Now</h2>
      <p>Server IP:</p>
      <div class="ip-container">
        <div class="ip-box" id="server-ip">NepaliSMP.aternos.me:53729</div>
        <button class="copy-btn" onclick="copyIP()">📋 Copy</button>
      </div>
      <p>Supported Versions: 1.20 and above</p>
      <h3>📲 Connect With Us</h3>
      <div class="socials">
        <a href="https://discord.gg/gfKGADwz">Discord</a>
        <a href="https://www.youtube.com/@Sushant.Yt.94z">YouTube</a>
        <a href="https://m.me/j/Abat1aHVrKh4Ni4T/">Facebook</a>
      </div>
    </div>

    <div class="card">
      <h2>🛒 Shop & Ranks</h2>
      <ul class="features">
        <li><strong>🥉 Bronze Rank</strong><br/>➤ Starter Kit, /home, Colored Name<br/><em>Free</em></li>
        <hr>
        <li><strong>🥈 Silver Rank</strong><br/>➤ Daily Crates, Extra SetHome, /craft<br/><em>Invite 3 friends</em></li>
        <hr>
        <li><strong>🥇 Gold Rank</strong><br/>➤ /fly, Custom Prefix, Special Crate Keys<br/><em>Contact Admin</em></li>
        <hr>
        <li><strong>🎖️ VIP Rank</strong><br/>➤ Access to VIP area, /nick, Custom Skins<br/><em>Giveaway/Donation</em></li>
        <hr>
        <li><strong>📹 YouTuber Rank</strong><br/>➤ YT Tag, /broadcast, Media Kit<br/><em>Minimum 100+ subs</em></li>
        <hr>
        <li><strong>🛠️ Helper Rank</strong><br/>➤ Mute/Kick, Staff Chat, /helpop access<br/><em>Apply on Discord</em></li>
        <hr>
        <li><strong>🛡️ Admin Rank</strong><br/>➤ Full Permissions, Server Management Tools<br/><em>Staff Only</em></li>
        <hr>
        <li><strong>👑 Leader Rank</strong><br/>➤ Owner Tag, All Permissions, Special Effects<br/><em>Server Founder</em></li>
      </ul>
      <p>🎁 Most ranks are cosmetic or staff-only and do not break fair gameplay.</p>
      <div class="socials">
        <a href="https://discord.gg/gfKGADwz">Apply or Donate via Discord</a>
      </div>
    </div>
  </main>

  <section class="gallery">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6e/Mount_Everest_as_seen_from_Drukair2_PLW_edit.jpg" alt="Mount Everest Nepal">
    <img src="https://static.planetminecraft.com/files/resource_media/screenshot/1813/mcbuild_2500401.jpg" alt="Minecraft Castle Build">
    <img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Patan_Durbar_Square%2C_Nepal.jpg" alt="Patan Durbar Square Nepal">
    <img src="https://wallpapercave.com/wp/wp6906403.jpg" alt="Minecraft Village Night">
  </section>

  <footer>
    © 2025 Nepali Lifesteal SMP | Made with ❤️ for Nepali Warriors
  </footer>

  <!-- Toast Notification -->
  <div id="toast" class="toast">IP Copied!</div>

  <script>
    function copyIP() {
      const ip = document.getElementById("server-ip").innerText;
      navigator.clipboard.writeText(ip).then(() => {
        const toast = document.getElementById("toast");
        toast.classList.add("show");
        setTimeout(() => {
          toast.classList.remove("show");
        }, 2000);
      }).catch(err => {
        console.error("Copy failed:", err);
      });
    }
  </script>

</body>
</html>
