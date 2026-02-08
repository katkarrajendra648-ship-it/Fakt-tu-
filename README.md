<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Anjali 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{
  margin:0;
  font-family:'Segoe UI',sans-serif;
  background:linear-gradient(120deg,#ff5fa2,#ff9a9e);
  color:white;
  overflow-x:hidden;
}

/* Container */
.container{
  max-width:800px;
  margin:auto;
  padding:20px;
  text-align:center;
}

.majkur{
  font-size:18px;
  line-height:1.7;
  min-height:200px;
}

/* Typing effect */
@keyframes blink { 0%,100% {border-color:transparent;} 50% {border-color:#fff;} }

.typing{
  border-right:3px solid #fff;
  white-space:pre-wrap;
  overflow:hidden;
}

/* Buttons */
.buttons{margin-top:30px;}
button{
  padding:15px 30px;
  font-size:18px;
  border:none;
  border-radius:30px;
  cursor:pointer;
  margin:10px;
  transition:0.3s;
}
#yesBtn{background:#fff;color:#ff2d75;}
#noBtn{background:#ff2d75;color:white;}

/* Popup full-screen */
.popup{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.95);
  backdrop-filter:blur(12px);
  display:none;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  z-index:9999;
  transition:0.5s;
}

.slide{
  display:none;
  text-align:center;
  animation:slideFade 1s ease;
}
@keyframes slideFade{
  from{opacity:0; transform:scale(0.95);}
  to{opacity:1; transform:scale(1);}
}

.slide img{
  max-width:80%;
  max-height:70vh;
  border-radius:20px;
  box-shadow:0 0 60px #ff5fa2;
}

.caption{
  margin-top:15px;
  font-size:22px;
  font-weight:bold;
  color:#fff;
  text-shadow:0 0 15px #ff99ac,0 0 30px #ff2d75;
  animation: glowText 2s ease-in-out infinite alternate;
}
@keyframes glowText{
  from{text-shadow:0 0 10px #ff99ac,0 0 20px #ff2d75;}
  to{text-shadow:0 0 25px #fff,0 0 50px #ff2d75;}
}

.close{
  position:absolute;
  top:20px;
  right:20px;
  font-size:30px;
  cursor:pointer;
}

/* Hearts */
.heart span{
  position:fixed;
  bottom:-20px;
  color:#ff5fa2;
  font-size:22px;
  animation: float 6s linear infinite;
}
@keyframes float{
  0%{transform:translateY(0);opacity:1;}
  100%{transform:translateY(-110vh);opacity:0;}
}

/* Confetti */
.confetti{
  position:absolute;
  width:10px; height:10px;
  top:0;
  animation:fall linear forwards;
  z-index:999;
}
@keyframes fall{
  0%{transform:translateY(0) rotate(0deg);opacity:1;}
  100%{transform:translateY(100vh) rotate(720deg);opacity:0;}
}

/* Fireworks */
.firework{
  position:absolute;
  width:6px; height:6px;
  border-radius:50%;
  background:hotpink;
  top:50%;
  left:50%;
  animation:explode 1s linear forwards;
  z-index:9999;
}
@keyframes explode{
  0%{transform:translate(0,0) scale(1);opacity:1;}
  100%{transform:translate(var(--x),var(--y)) scale(0);opacity:0;}
}
</style>
</head>
<body>

<div class="container">
<div class="majkur typing" id="majkurText"></div>

<div class="buttons">
<button id="yesBtn" onclick="openPopup()">YES 💖</button>
<button id="noBtn" onclick="growYes()">NO 🙈</button>
</div>
</div>

<!-- Popup -->
<div class="popup" id="popup">
<div class="close" onclick="closePopup()">✖</div>

<div class="slide">
<img src="mine1" alt="">
<div class="caption">ur mine 💖</div>
</div>

<div class="slide">
<img src="mine2" alt="">
<div class="caption">ur my angel 😇</div>
</div>

<div class="slide">
<img src="mine3" alt="">
<div class="caption">ur my princess 👑</div>
</div>

<div class="slide">
<img src="mine4" alt="">
<div class="caption">
ur my everything 💞<br>Anjali i love you so much<br>much more and ever 🌍💋🫂🧿
</div>
</div>

<audio id="music" src="love.mp3"></audio>
</div>

<script>
// Majkur typing effect
const text=`Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo. But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay. Tula mahity ka mi sagalyana sangitalay ki mi tujhyavar prem karato aani mla tuch havi tujhyavar sarkhi pn nako. Aani tu thambshil rahashil mla sodun jashil mla kahi ghen den nahi but I know ki tu pahije. I love you love you love you so much much more and ever 🌍💗😘 fakt tuch.khup prem zalay tujhyavar tuch aani tuch pahije majhya black and white zindagi madhi colourfull person tu 🧿\nMazhi special one mazhi kaju katli 💋 mazhi aaichyaa hatachi puranpoli 💕😘🌎 love you babydoll mazhi 💗🫂😘🌎\n\nAnjali i love you yar 🥺🤌💕🫂🌎🧿 say yes or no 🤌🤍`;
let i=0;
function typing(){ 
  if(i<text.length){document.getElementById("majkurText").innerHTML+=text.charAt(i); i++; setTimeout(typing,25);}
}
typing();

let yesSize=1;
let slideIndex=0;
let slides;

function growYes(){ yesSize+=0.2; document.getElementById("yesBtn").style.transform=`scale(${yesSize})`; }

function openPopup(){
  document.getElementById("popup").style.display="flex";
  slides=document.getElementsByClassName("slide");
  slideIndex=0;
  showSlide();
  document.getElementById("music").currentTime=0;
  document.getElementById("music").play();
}

function closePopup(){
  document.getElementById("popup").style.display="none";
  document.getElementById("music").pause();
}

function showSlide(){
  for(let i=0;i<slides.length;i++) slides[i].style.display="none";
  slides[slideIndex].style.display="block";
  if(slideIndex===slides.length-1){spawnConfetti();spawnFireworks();}
  slideIndex++;
  if(slideIndex>=slides.length) slideIndex=0;
  setTimeout(showSlide,3000);
}

// Floating hearts
setInterval(()=>{
  const h=document.createElement("span");
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"vw";
  h.style.animationDuration=(Math.random()*3+3)+"s";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),6000);
},400);

// Confetti
function spawnConfetti(){
  for(let i=0;i<50;i++){
    const c=document.createElement("div");
    c.className="confetti";
    c.style.left=Math.random()*100+"vw";
    c.style.background=['#ff2d75','#ff99ac','#ffd6e0','#fff'][Math.floor(Math.random()*4)];
    c.style.width=Math.random()*8+4+"px";
    c.style.height=Math.random()*8+4+"px";
    c.style.animationDuration=(Math.random()*2+3)+"s";
    document.body.appendChild(c);
    setTimeout(()=>c.remove(),4000);
  }
}

// Fireworks
function spawnFireworks(){
  for(let i=0;i<30;i++){
    const f=document.createElement("div");
    f.className="firework";
    f.style.setProperty('--x',(Math.random()*400-200)+'px');
    f.style.setProperty('--y',(Math.random()*400-200)+'px');
    document.body.appendChild(f);
    setTimeout(()=>f.remove(),1000);
  }
}
</script>

</body>
</html>
