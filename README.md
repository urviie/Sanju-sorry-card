# Sanju-sorry-card<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry Card for Sanju</title>
<style>
  body {
    font-family: 'Comic Sans MS', cursive, sans-serif;
    background: linear-gradient(135deg, #ffe0f0, #fff0e0);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  #card {
    background: #fff;
    border-radius: 25px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    padding: 30px;
    width: 350px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .round {
    display: none;
    animation: fadeIn 0.6s;
  }
  .round.active {
    display: block;
  }
  button {
    background: #ffb6c1;
    border: none;
    padding: 10px 20px;
    margin: 10px 5px;
    border-radius: 15px;
    font-size: 16px;
    cursor: pointer;
    transition: 0.3s;
  }
  button:hover {
    transform: scale(1.1);
    background: #ff69b4;
    color: #fff;
  }
  img {
    width: 100px;
    border-radius: 50%;
    margin-bottom: 15px;
    border: 3px solid #ffb6c1;
  }
  @keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
  }
</style>
</head>
<body>
<div id="card">
  <!-- Starting pic + intro -->
  <div class="round active" id="round0">
    <img src="your_pic_url_here.jpg" alt="Urvi GF Pic">
    <p>Dekho sweetu, aapki coder gf ne aapke liye kya banaya hai 😭💖</p>
    <button onclick="nextRound()">Next ➡️</button>
  </div>

  <!-- Round 1 -->
  <div class="round" id="round1">
    <p>Sanju Mondal... 😔<br>
    Kabhi kabhi na sweetu, mai jada bol deti hu…<br>
    par dil se toh kabhi bura nahi chahti 🥺💗<br>
    Sorry bolne ka ek mauka dega?</p>
    <button onclick="nextRound()">💖 Yes baby!</button>
    <button onclick="nextRound()">🙈 Soch rahi hu…</button>
  </div>

  <!-- Round 2 -->
  <div class="round" id="round2">
    <p>Pata hai jab tu chhup ho jaata h na…<br>
    toh dil literally dull ho jaata h 🥺💔<br>
    Mujhe realize hota h kitna pyaar karti hu tujhse 💞</p>
    <button onclick="nextRound()">🥺 Awww</button>
    <button onclick="nextRound()">🙂 Hmm okay</button>
  </div>

  <!-- Round 3 -->
  <div class="round" id="round3">
    <p>Promise sweetu!<br>
    Next time mai jada bolungi toh…<br>
    tu sirf ek tight hug de dena, gussa nahi 💋😚</p>
    <button onclick="nextRound()">💖 Deal</button>
    <button onclick="nextRound()">🙈 Mujhe sochne de</button>
  </div>

  <!-- Round 4 -->
  <div class="round" id="round4">
    <p>Waise ek baat puchu?<br>
    Tu abhi bhi mujhe utna hi cute maanta hai jitna pehle maanta tha? 😚💞</p>
    <button onclick="nextRound()">💘 Of course</button>
    <button onclick="nextRound()">😂 Kabhi kabhi</button>
  </div>

  <!-- Round 5 -->
  <div class="round" id="round5">
    <p>Ab bataa sweetu...<br>
    Abhi bhi mere pe voh pics dene ka option bacha hai kya? 😏📸💕</p>
    <button onclick="nextRound()">🙈 Yes (thoda soch ke 😜)</button>
    <button onclick="nextRound()">😤 No (par mann keh raha h Yes)</button>
  </div>

  <!-- Round 6 -->
  <div class="round" id="round6">
    <p>Tere bina na ek din bhi ajeeb lagta hai...<br>
    tera ‘hmm’ bhi sukoon deta h 💗<br>
    Bas tu rehna mere saath hamesha 🫶</p>
    <button onclick="nextRound()">💖 Always</button>
    <button onclick="nextRound()">🥺 Forever</button>
  </div>

  <!-- Round 7: Final Sorry -->
  <div class="round" id="round7">
    <p>Bas itna kehna tha…<br>
    I’m really sorry sweetu 🥺<br>
    Kabhi kabhi mai jada bol deti hu, par tu mera sab kuch hai 💞<br>
    Love you sweetu 💖</p>
    <button onclick="restart()">💖 Read again</button>
  </div>
</div>

<script>
let current = 0;
function nextRound() {
  document.getElementById("round"+current).classList.remove("active");
  current++;
  if(current > 7) current = 7;
  document.getElementById("round"+current).classList.add("active");
}
function restart() {
  document.getElementById("round"+current).classList.remove("active");
  current = 0;
  document.getElementById("round"+current).classList.add("active");
}
</script>
</body>
</html>
