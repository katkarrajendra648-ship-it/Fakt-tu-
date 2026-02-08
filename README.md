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
  text-align:center;
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
/* floating hearts */
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
</style>
</head>
<body>

<div class="container">
<div id="intro">
  <h1>Babydoll 💖<br>I have something to tell you…</h1>
  <button id="goBtn" onclick="startStory()">GO 💫</button>
</div>

<div class="majkur typing" id="majkurText"></div>

<div class="buttons" id="ynButtons">
  <button id="yesBtn" onclick="openPopup()">YES 💖</button>
  <button id="noBtn" onclick="growYes()">NO 🙈</button>
</div>
</div>

<!-- Popup -->
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
Anjali I love you too so much<br>
much more and ever 🌍💋🫂🧿
</div>
</div>

<audio id="music" src="love.mp3"></audio>
</div>

<script>
const text=`Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo. But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay. Tula mahity ka mi sagalyana sangitalay ki mi tujhyavar prem karato aani mla tuch havi tujhyavar sarkhi pn nako. Aani tu thambshil rahashil mla sodun jashil mla kahi ghen den nahi but I know ki tu pahije. I love you love you love you so much much more and ever 🌍💗😘 fakt tuch.khup prem zalay tujhyavar tuch aani tuch pahije majhya black and white zindagi madhi colourfull person tu 🧿
Mazhi special one mazhi kaju katli 💋 mazhi aaichyaa hatachi puranpoli 💕😘🌎 love you babydoll mazhi 💗🫂😘🌎
Say s or no 🥺🤞`;

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
  slides=document.getElementsByClassName("slide");
  slideIndex=0;
  showSlide();
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

/* hearts */
setInterval(()=>{
  const h=document.createElement("span");
  h.innerHTML="❤️";
  h.style.left=Math.random()*100+"vw";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),6000);
},400);
</script>

</body>
</html>
