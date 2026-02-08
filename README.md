<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Anjali 💖</title>
<style>
body{
  margin:0;
  min-height:100vh;
  background:linear-gradient(270deg,#ff6a88,#ff99ac,#fad0c4);
  background-size:600% 600%;
  animation:bgMove 14s ease infinite;
  font-family:'Segoe UI',sans-serif;
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;
}
@keyframes bgMove{
  0%{background-position:0% 50%}
  50%{background-position:100% 50%}
  100%{background-position:0% 50%}
}

.card{
  max-width:900px;
  background:rgba(255,255,255,.22);
  backdrop-filter:blur(16px);
  padding:30px;
  border-radius:30px;
  color:#fff;
  text-align:center;
  box-shadow:0 0 50px rgba(255,0,120,.6);
}

h1{
  font-size:36px;
  animation:heartbeat 1.4s infinite;
}
@keyframes heartbeat{50%{transform:scale(1.15)}}
p{
  font-size:18px;
  line-height:1.9;
  white-space:pre-line;
}

.buttons{margin-top:25px}
button{
  border:none;
  padding:12px 25px;
  font-size:20px;
  border-radius:30px;
  cursor:pointer;
  transition:.3s;
}
#yes{background:#ff2f6e;color:#fff;}
#no{background:#fff;color:#ff2f6e;margin-left:15px;}

/* POPUP FULL SCREEN */
.modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,0.9);
  display:none;
  justify-content:center;
  align-items:center;
  z-index:9999;
  flex-direction:column;
}
.modal-content{
  max-width:600px;
  width:90%;
  text-align:center;
  color:#fff;
  animation:pop .8s ease;
}
@keyframes pop{from{opacity:0;transform:scale(.6)}to{opacity:1;transform:scale(1)}}
.modal-content img{
  width:100%;
  border-radius:20px;
  box-shadow:0 0 40px hotpink;
}
.caption{
  margin-top:15px;
  font-size:22px;
  font-weight:bold;
  line-height:1.5;
  animation:glow 2s infinite alternate;
}
@keyframes glow{from{text-shadow:0 0 10px pink}to{text-shadow:0 0 25px hotpink}}
.close{
  margin-top:20px;
  font-size:24px;
  cursor:pointer;
}

/* HEARTS */
.heart{
  position:absolute;
  bottom:-20px;
  font-size:24px;
  animation:floatUp linear forwards;
}
@keyframes floatUp{to{transform:translateY(-120vh);opacity:0}}

/* CONFETTI */
.confetti-piece{
  position:absolute;
  width:10px; height:10px;
  background:hotpink;
  top:0;
  animation:fall linear forwards;
}
@keyframes fall{
  0%{transform:translateY(0) rotate(0deg);opacity:1;}
  100%{transform:translateY(100vh) rotate(720deg);opacity:0;}
}
</style>
</head>
<body>

<div class="card">
<h1>Anjali 💖</h1>
<p>
Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo. But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay. Tula mahity ka mi sagalyana sangitalay ki mi tujhyavar prem karato aani mla tuch havi tujhya sarkhi pn nako. Aani tu thambshil rahashil mla sodun jashil mla kahi ghen den nahi but I know ki tu pahije. I love you love you love you so much much more and ever 🌍💗😘 fakt tuch.khup prem zalay tujhyavar tuch aani tuch pahije majhya black and white zindagi madhi colourfull person tu 🧿
Mazhi special one mazhi kaju katli 💋 mazhi aaichyaa hatachi puranpoli 💕😘🌎 love you babydoll mazhi 💗🫂😘🌎.

.

.

Anjali i love you yar 🥺🤌💕🫂🌎🧿 say yes or no 🤌🤍
</p>

<div class="buttons">
<button id="yes">YES 💖</button>
<button id="no">NO 🙈</button>
</div>
</div>

<!-- FULL SCREEN POPUP -->
<div class="modal" id="popup">
  <div class="modal-content">
    <img id="slideImg" src="mine1.jpg">
    <div class="caption" id="caption"></div>
    <div class="close" id="close">✖ Close</div>
  </div>
</div>

<audio id="music" src="love.mp3"></audio>

<script>
// SLIDES
const slides=[
  {img:"mine1", text:"ur mine 💖"},
  {img:"mine2", text:"ur my angel 😇"},
  {img:"mine3", text:"ur my princess 👑"},
  {img:"mine4", text:"ur my everything 💞<br>Anjali i love you so much<br>much more and ever 🌍💋🫂🧿"}
];
let index=0, timer;

const yes=document.getElementById("yes");
const no=document.getElementById("no");
const popup=document.getElementById("popup");
const slideImg=document.getElementById("slideImg");
const caption=document.getElementById("caption");
const music=document.getElementById("music");

no.onclick=()=>{yes.style.transform="scale(1.4)";};

yes.onclick=()=>{
  popup.style.display="flex";
  music.currentTime=0; music.play();
  showSlide();
  timer=setInterval(showSlide,3000);
};

function showSlide(){
  slideImg.src=slides[index].img;
  caption.innerHTML=slides[index].text;
  if(index===slides.length-1){createConfetti();}
  index=(index+1)%slides.length;
}

document.getElementById("close").onclick=()=>{
  popup.style.display="none";
  music.pause();
  clearInterval(timer);
};

// FLOATING HEARTS
setInterval(()=>{
  const h=document.createElement("div");
  h.className="heart"; h.innerHTML="💖";
  h.style.left=Math.random()*100+"vw";
  h.style.animationDuration=(Math.random()*3+5)+"s";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),7000);
},300);

// CONFETTI FUNCTION
function createConfetti(){
  for(let i=0;i<50;i++){
    const c=document.createElement("div");
    c.className="confetti-piece";
    c.style.left=Math.random()*100+"vw";
    c.style.background=['#ff2f6e','#ff99ac','#ffd6e0','#fff'][Math.floor(Math.random()*4)];
    c.style.animationDuration=(Math.random()*2+3)+"s";
    document.body.appendChild(c);
    setTimeout(()=>c.remove(),4000);
  }
}
</script>

</body>
</html>
