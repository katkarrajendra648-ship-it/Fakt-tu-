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
  background: linear-gradient(120deg,#ff5fa2,#ff9a9e);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
  color:white;
  overflow-x:hidden;
  text-align:center;
}
@keyframes gradientBG{
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
}
.container{
  max-width:800px;
  margin:auto;
  padding:20px;
}
#intro{
  margin-top:80px;
  animation:fadeIn 2s ease;
}
@keyframes fadeIn{
  from{opacity:0; transform:translateY(20px);}
  to{opacity:1; transform:translateY(0);}
}
#intro h1{
  font-size:30px;
  text-shadow:0 0 20px #fff;
}
#goBtn{
  margin-top:30px;
  padding:15px 40px;
  font-size:20px;
  border:none;
  border-radius:40px;
  background:white;
  color:#ff2d75;
  cursor:pointer;
  box-shadow:0 0 30px #fff;
  animation:pulse 2s infinite;
}
@keyframes pulse{
  0%{transform:scale(1);}
  50%{transform:scale(1.1);}
  100%{transform:scale(1);}
}
.majkur{
  font-size:18px;
  line-height:1.7;
  min-height:200px;
  display:none;
  border:3px solid #fff;
  padding:15px;
  border-radius:20px;
  box-shadow:0 0 30px #ff9a9e;
}
.typing{
  border-right:3px solid #fff;
  white-space:pre-wrap;
  overflow:hidden;
}
.buttons{
  margin-top:30px;
  display:none;
}
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
.popup{
  position:fixed;
  inset:0;
  background: radial-gradient(circle at top,#ff5fa2,#8e44ad 90%);
  backdrop-filter:blur(12px);
  display:none;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  z-index:9999;
  overflow:hidden;
}
.star{
  position:absolute;
  width:2px;
  height:2px;
  background:white;
  border-radius:50%;
  opacity:0.8;
  animation:twinkle linear infinite;
}
@keyframes twinkle{
  0%,100%{opacity:0.2;}
  50%{opacity:1;}
}
.slide{display:none;}
.slide img{
  max-width:80%;
  max-height:70vh;
  border-radius:20px;
  box-shadow:0 0 80px #ff5fa2;
}
.caption{
  margin-top:15px;
  font-size:22px;
  font-weight:bold;
  text-shadow:0 0 20px #ff2d75;
}
.close{
  position:absolute;
  top:20px;
  right:20px;
  font-size:30px;
  cursor:pointer;
}
.heart span{
  position:fixed;
  bottom:-20px;
  font-size:22px;
  animation:float 6s linear infinite;
}
@keyframes float{
  from{transform:translateY(0);opacity:1;}
  to{transform:translateY(-110vh);opacity:0;}
}
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
<div id="intro">
  <h1>Babydoll I have something to say…</h1>
  <button id="goBtn" onclick="startStory()">GO 💫</button>
</div>

<div class="majkur typing" id="majkurText"></div>

<div class="buttons" id="ynButtons">
  <button id="yesBtn" onclick="openPopup()">YES 💖</button>
  <button id="noBtn" onclick="growYes()">NO 🙈</button>
</div>
</div>

<!-- POPUP -->
<div class="popup" id="popup">
<div class="close" onclick="closePopup()">✖</div>

<div class="slide">
<img src="mine1">
<div class="caption">ur mine 💖</div>
</div>
<div class="slide">
<img src="mine2">
<div class="caption">ur my angel 😇</div>
</div>
<div class="slide">
<img src="mine3">
<div class="caption">ur my princess 👑</div>
</div>
<div class="slide">
<img src="mine4">
<div class="caption">
ur my everything 💞<br>
Anjali I love you so much<br>
much more and ever 🌍💋🫂🧿
</div>
</div>

<audio id="music" src="love.mp3"></audio>
</div>

<script>
const text=`Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo. But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay. Aani mla tuch havi tujhyavar sarkhi pn nako. Tyavar hot ki
.
.
Ki karu sukhane sansar aapan. Tu premachi pahili payari hoshil ka 💕
Lihil nanyane swatahala tujhya sobat.tu aayushyachi dairy hoshil ka 🧿
Aani jevha yeu yekatr aapan.duniya karel kautuk aapl jevha yeu yekatr aapan duniya karel kautuk aapl.🍂🌸
Mi hoto shabd tuzhe. Tu mazhi shayari hoshil ka 🫂🤌🤍💋❤️
.
. say s or no 🤌🤍`;

let i=0;
function startStory(){
  document.getElementById("intro").style.display="none";
  document.getElementById("majkurText").style.display="block";
  type();
}

function type(){
  if(i<text.length){
    document.getElementById("majkurText").innerHTML+=text.charAt(i);
    i++;
    setTimeout(type,25);
  }else{
    document.getElementById("ynButtons").style.display="block";
  }
}

let yesSize=1;
function growYes(){
  yesSize+=0.2;
  document.getElementById("yesBtn").style.transform=`scale(${yesSize})`;
}

let slideIndex=0,slides;
function openPopup(){
  document.getElementById("popup").style.display="flex";
  createStars(80);
  slides=document.getElementsByClassName("slide");
  slideIndex=0;
  showSlide();
  spawnConfetti();
  spawnFireworks();
  document.getElementById("music").play();
}
function closePopup(){
  document.getElementById("popup").style.display="none";
  document.getElementById("music").pause();
}

function showSlide(){
  for(let i=0;i<slides.length;i++) slides[i].style.display="none";
  slides[slideIndex].style.display="block";
  slideIndex=(slideIndex+1)%slides.length;
  setTimeout(showSlide,3000);
}

// Hearts
setInterval(()=>{
  const h=document.createElement("span");
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"vw";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),6000);
},400);

// Stars
function createStars(num){
  const popup=document.getElementById("popup");
  for(let i=0;i<num;i++){
    const s=document.createElement("div");
    s.className="star";
    s.style.top=Math.random()*100+"%";
    s.style.left=Math.random()*100+"%";
    s.style.width=(Math.random()*2+1)+"px";
    s.style.height=s.style.width;
    s.style.animationDuration=(Math.random()*3+2)+"s";
    popup.appendChild(s);
  }
}

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
