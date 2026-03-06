<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anniversaire Amira ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&family=Dancing+Script:wght@600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}
body{
background:url('https://images3.alphacoders.com/856/thumb-1920-856363.jpg') center/cover no-repeat fixed;
color:white;
text-align:center;
overflow-x:hidden;
}
body::before{
content:"";
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.4);
z-index:-1;
}
header{padding:20px;}
.heart{
font-size:90px;
animation:beat 1s infinite;
margin-top:20px;
}
@keyframes beat{
0%{transform:scale(1)}
50%{transform:scale(1.3)}
100%{transform:scale(1)}
}
.card{
background:rgba(255,255,255,0.15);
padding:20px;
border-radius:20px;
backdrop-filter:blur(10px);
margin:20px auto;
max-width:500px;
position:relative;
}
input{
padding:10px;
border-radius:20px;
border:none;
width:80%;
text-align:center;
}
button{
margin-top:10px;
padding:10px 20px;
border:none;
border-radius:20px;
background:white;
color:#ff1744;
font-weight:bold;
cursor:pointer;
}
#error{
margin-top:10px;
color:yellow;
min-height:20px;
}
.shake{animation:shake 0.4s;}
@keyframes shake{
0%{transform:translateX(0)}
25%{transform:translateX(-8px)}
50%{transform:translateX(8px)}
75%{transform:translateX(-8px)}
100%{transform:translateX(0)}
}
.falling{
position:fixed;
top:-10px;
font-size:22px;
animation:fall linear infinite;
}
@keyframes fall{
to{transform:translateY(100vh)}
}
#letter,#birthday-surprise,#proposal{display:none}
#cake{
position:relative;
width:200px;
height:150px;
margin:90px auto;
}
.cake-layer{
position:absolute;
width:100%;
height:50%;
background:#ff4d6d;
border-radius:20px;
}
.cake-top{top:0;background:#ff85a2;}
.cake-bottom{bottom:0;}
.candle{
position:absolute;
top:-30px;
width:30px;
height:50px;
background:white;
border-radius:5px;
line-height:50px;
color:#ff1744;
font-weight:bold;
opacity:0.5;
}
.candle.on{opacity:1}
.flame{
position:absolute;
top:-18px;
left:50%;
transform:translateX(-50%);
width:12px;
height:18px;
background:orange;
border-radius:50%;
opacity:0;
animation:flicker .3s infinite alternate;
}
.flame.on{opacity:1}
@keyframes flicker{
from{transform:translateX(-50%) scaleY(.8)}
to{transform:translateX(-50%) scaleY(1.2)}
}
#gift-photo{
max-width:90%;
border-radius:20px;
margin-top:20px;
display:none;
opacity:0;
transition:opacity 1s;
}
@keyframes vibrate{
0%{transform:translateX(0)}
25%{transform:translateX(-5px)}
50%{transform:translateX(5px)}
75%{transform:translateX(-5px)}
100%{transform:translateX(0)}
}
.vibrate{
animation:vibrate 0.1s infinite;
}
footer{
margin-top:40px;
padding:20px;
background:rgba(0,0,0,0.5);
backdrop-filter:blur(5px);
}
footer h3{
font-family:'Dancing Script',cursive;
font-size:28px;
margin-bottom:10px;
}

/* bague animation */
#ring{
font-size:60px;
margin-top:20px;
opacity:0;
transition:opacity 1s, transform 0.5s;
}
#ring.show{
opacity:1;
transform:scale(1.3);
}
</style>
</head>

<body>

<header>
<div class="heart">❤️</div>
<h1>Joyeux anniversaire Amira ❤️</h1>
<p>Mon amour, chaque instant avec toi est magique</p>
</header>

<div class="card">
<h3>🔒 Espace privé</h3>
<input type="password" id="password" placeholder="password">
<br>
<button onclick="checkPassword()">Entrer 💕</button>
<p id="error"></p>
</div>

<div class="card" id="letter">
<h3>💌 Lettre pour toi</h3>
<p>
Mon amour Amira ❤️  
Depuis notre rencontre le 31 août 2025,  
mon cœur ne bat que pour toi.  
Chaque jour avec toi est un cadeau.  
Je t'aime plus que tout al3mer wlh
hacha kmi ivghigh hacha itmennigh 
a3zouzou ynu. 

<div id="relation-time"></div>
<div id="countdown"></div>
</div>

<!-- proposition -->
<div class="card" id="proposal">
<h2>💍 Question importante</h2>
<p>Amira ❤️ veux-tu être ma femme ?</p>
<button id="yesBtn">OUI</button>
<button id="noBtn">NON</button>
<p id="answer"></p>
<div id="ring">💍</div>
</div>

<div class="card" id="birthday-surprise">
<h2>🎉 Surprise 🎉</h2>
<div id="cake">
<div class="cake-layer cake-top"></div>
<div class="cake-layer cake-bottom"></div>
<div class="candle" id="candle1" style="left:50px">1<div class="flame" id="flame1"></div></div>
<div class="candle" id="candle2" style="left:120px">7<div class="flame" id="flame2"></div></div>
</div>
<button onclick="lightCandles()">Allumer les bougies 🕯️</button>
<br>
<button onclick="showGift()">Claim your gift 🎁</button>
<br>
<img id="gift-photo" src="gift.png.jpg">
<p id="gift-message"></p>
</div>

<audio id="birthday-music" src="birthday.mp3"></audio>
<audio id="final-music" src="happy-birthday.mp3"></audio>

<footer>
<h3>💞 Notre histoire</h3>
<p>
Tout a commencé le <b>31 août 2025</b>.  
Depuis ce jour, chaque moment avec toi est devenu précieux.  
Chaque rire, chaque message, chaque appel a construit notre histoire.  
Et aujourd'hui je veux simplement te dire que je suis heureux de t’avoir dans ma vie.
</p>
<p style="margin-top:10px;">
Avec tout mon amour pour toi Amira ❤️
</p>
</footer>

<script>
let attempts=0
const funnyMessages=["ta3gount 😂","nighamiid ta3gount 😜","ammii stp udtfghara ar yemmak 🤣","tamongolt 😏"]
const correctPassword="070309"

function checkPassword(){
  let pass=document.getElementById("password").value
  let error=document.getElementById("error")
  let card=document.querySelector(".card")
  if(pass===correctPassword){
    document.getElementById("letter").style.display="block"
    document.getElementById("birthday-surprise").style.display="block"
    document.getElementById("proposal").style.display="block"
    startFalling()
    updateTimes()
    error.innerText=""
  } else {
    attempts++
    card.classList.add("shake")
    setTimeout(()=>card.classList.remove("shake"),400)
    let msg=new SpeechSynthesisUtterance("Be patient")
    speechSynthesis.speak(msg)
    if(attempts<=4){
      error.innerText=funnyMessages[attempts-1]
    } else {
      error.innerText="C’est le jour où le monde a souri jj mm aa 😏"
    }
  }
}

function startFalling(){
  setInterval(()=>{
    let heart=document.createElement("div")
    heart.classList.add("falling")
    heart.innerHTML="🌹"
    heart.style.left=Math.random()*100+"vw"
    heart.style.animationDuration=(Math.random()*3+2)+"s"
    document.body.appendChild(heart)
    setTimeout(()=>heart.remove(),5000)
  },400)
}

function updateTimes(){
  let relationStart=new Date("2025-08-31")
  let nextBirthday=new Date("2026-03-07")
  let countdownEl=document.getElementById("countdown")
  function update(){
    let now=new Date()
    let diff=now-relationStart
    let days=Math.floor(diff/1000/60/60/24)
    let hours=Math.floor(diff/1000/60/60)%24
    let minutes=Math.floor(diff/1000/60)%60
    let seconds=Math.floor(diff/1000)%60
    document.getElementById("relation-time").innerText=`Notre relation dure : ${days}j ${hours}h ${minutes}m ${seconds}s ❤️`
    let diffB=nextBirthday-now
    if(diffB>0){
      let d=Math.floor(diffB/1000/60/60/24)
      let h=Math.floor(diffB/1000/60/60)%24
      let m=Math.floor(diffB/1000/60)%60
      let s=Math.floor(diffB/1000)%60
      countdownEl.innerText=`Anniversaire dans : ${d}j ${h}h ${m}m ${s}s 🎂`
    } else {
      countdownEl.innerText="🎂 Joyeux Anniversaire ! 🎂"
      countdownEl.classList.add("vibrate")
      setTimeout(()=>countdownEl.classList.remove("vibrate"),5000)
      document.getElementById("final-music").play()
    }
  }
  update()
  setInterval(update,1000)
}

function lightCandles(){
  document.getElementById("flame1").classList.add("on")
  document.getElementById("flame2").classList.add("on")
  document.getElementById("candle1").classList.add("on")
  document.getElementById("candle2").classList.add("on")
  document.getElementById("gift-message").innerText="Amira ton cadeau est tout mon amour ❤️"
  document.getElementById("birthday-music").play()
}

function showGift(){
  const gift=document.getElementById("gift-photo")
  gift.style.display="block"
  setTimeout(()=>{gift.style.opacity=1},50)
}

// Proposition de mariage
const yesBtn = document.getElementById('yesBtn')
const noBtn = document.getElementById('noBtn')
const answer = document.getElementById('answer')
const ring = document.getElementById('ring')

// OUI
yesBtn.addEventListener('click', ()=>{
  answer.innerHTML="Merci ! Je suis le plus heureux 💖💍"
  ring.classList.add('show')
})

// NON qui bouge
noBtn.addEventListener('mouseenter', ()=>{
  const card = document.getElementById('proposal')
  const maxX = card.offsetWidth - noBtn.offsetWidth
  const maxY = card.offsetHeight - noBtn.offsetHeight
  const randomX = Math.floor(Math.random() * maxX)
  const randomY = Math.floor(Math.random() * maxY)
  noBtn.style.position='absolute'
  noBtn.style.left=randomX+'px'
  noBtn.style.top=randomY+'px'
})
</script>

</body>
</html>
