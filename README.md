<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>To My Favourite Person</title>
  <style>
    /* Basic reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    /* Background and layout */
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #4facfe, #00f2fe);
      overflow: hidden;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
    }
    .container {
      max-width: 600px;
      padding: 20px;
      background: rgba(0, 0, 0, 0.4);
      border-radius: 10px;
    }
    h1 {
      margin-bottom: 20px;
      font-size: 2em;
    }
    p {
      margin-bottom: 20px;
      font-size: 1.2em;
    }
    img {
      max-width: 100%;
      border-radius: 10px;
      animation: float 3s ease-in-out infinite;
    }
    /* Floating animation */
    @keyframes float {
      0% { transform: translatey(0px); }
      50% { transform: translatey(-20px); }
      100% { transform: translatey(0px); }
    }
    .link-button {
      margin-top: 20px;
      padding: 10px 20px;
      background: #ff4757;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1em;
    }
    .hidden-gift {
      display: none;
      margin-top: 20px;
      background: rgba(255, 255, 255, 0.2);
      padding: 15px;
      border-radius: 5px;
    }
    .hidden-gift img {
      margin-top: 15px;
      max-width: 150px;
      border-radius: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>To My Favourite Person</h1>
    <!-- Soheli's image -->
    <img src="soheli_image.jpg" alt="Soheli's Picture">
    <p>Happy Birthday, Soheli!</p>
    <!-- Button to reveal hidden gift -->
    <button class="link-button" onclick="revealGift()">Open Your Gift</button>
    <!-- Hidden gift content -->
    <div id="gift" class="hidden-gift">
      <p>
        Happy Birthday, Soheli! H<br>
        On this special day, I just want to remind you how amazing you are. Your kindness, laughter, and love make every moment brighter. I'm so lucky to have you in my life. May this year bring you endless joy, success, and all the happiness your heart desires. Love you always!
      </p>
      <img src="red_rose.jpg" alt="Red Rose">
    </div>
  </div>

  <!-- Audio Elements -->
  <audio id="audio1" src="pal_pal_dil_ke_pass.mp3"></audio>
  <audio id="audio2" src="happy_birthday_soheli.mp3"></audio>

  <script>
    // Reveal the hidden gift when the button is clicked.
    function revealGift() {
      document.getElementById('gift').style.display = 'block';
    }

    window.onload = function() {
      var audio1 = document.getElementById("audio1");
      var audio2 = document.getElementById("audio2");

      // Play the first audio clip (Pal Pal Dil Ke Pass main theme) for 10 seconds.
      audio1.play();
      setTimeout(function(){
        // Stop the first audio and reset its time.
        audio1.pause();
        audio1.currentTime = 0;
        // Play the second audio clip ("Happy Birthday Soheli") for 3 seconds.
        audio2.play();
        setTimeout(function(){
          audio2.pause();
        }, 3000);
      }, 10000);
    }
  </script>
</body>
</html>
