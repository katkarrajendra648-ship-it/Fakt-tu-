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
  display:flex;
  justify-content:center;
  align-items:center;
  overflow:hidden;
  font-family:'Segoe UI',sans-serif;
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
@keyframes heartbeat{
  50%{transform:scale(1.15)}
}

p{
  font-size:18px;
  line-height:1.9;
}

.buttons{margin-top:25px}
button{
  border:none;
  padding:12px 25px;
  font-size:20px;
  border-radius:30px;
  cursor:pointer;
}
#yes{
  background:#ff2f6e;
  color:#fff;
}
#no{
  background:#fff;
  color:#ff2f6e;
  margin-left:15px;
}

/* POPUP */
.modal{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.75);
  display:none;
  justify-content:center;
  align-items:center;
  z-index:999;
}
.modal-content{
  background:linear-gradient(135deg,#ff6a88,#ff99ac);
  padding:30px;
  border-radius:25px;
  text-align:center;
  color:#fff;
  width:300px;
  box-shadow:0 0 40px hotpink;
  animation:pop .8s ease;
}
@keyframes pop{
  from{transform:scale(.6);opacity:0}
  to{transform:scale(1);opacity:1}
}
.modal-content img{
  width:100%;
  border-radius:20px;
  box-shadow:0 0 20px #fff;
}
.caption{
  margin-top:15px;
  font-size:20px;
  font-weight:bold;
  line-height:1.5;
  animation:glow 2s infinite alternate;
}
@keyframes glow{
  from{text-shadow:0 0 10px pink}
  to{text-shadow:0 0 25px hotpink}
}
.close{
  margin-top:15px;
  font-size:22px;
  cursor:pointer;
}

/* HEARTS */
.heart{
  position:absolute;
  bottom:-20px;
  font-size:22px;
  animation:floatUp linear forwards;
}
@keyframes floatUp{
  to{transform:translateY(-120vh);opacity:0}
}
</style>
</head>

<body>

<div class="card">
<h1>Anjali 💖</h1>

<p>
Hlo mazhi kaju katli 💋  
mla nahi mahiti kasa prem zala pan  
mla tujhyavar khup khup jast prem zalay 💞  

majhya black & white life madhe  
colour tu aahe 🧿🌈  

<b>Anjali, I love you yaar 🥺🤌💕🫂🌍</b>
</p>

<div class="buttons">
<button id="yes">YES 💖</button>
<button id="no">NO 🙈</button>
</div>
</div>

<!-- POPUP SLIDESHOW -->
<div class="modal" id="popup">
  <div class="modal-content">
    <img id="slideImg" src="mine1.jpg">
    <div class="caption" id="caption"></div>
    <div class="close" id="close">✖ Close</div>
  </div>
</div>

<audio id="music" src="love.mp3"></audio>

<script>
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

no.onclick=()=>{
  yes.style.transform="scale(1.3)";
};

yes.onclick=()=>{
  popup.style.display="flex";
  music.play();
  showSlide();
  timer=setInterval(showSlide,3000);
};

function showSlide(){
  slideImg.src=slides[index].img;
  caption.innerHTML=slides[index].text;
  index=(index+1)%slides.length;
}

document.getElementById("close").onclick=()=>{
  popup.style.display="none";
  music.pause();
  clearInterval(timer);
};

// floating hearts
setInterval(()=>{
  const h=document.createElement("div");
  h.className="heart";
  h.innerHTML="💖";
  h.style.left=Math.random()*100+"vw";
  h.style.animationDuration=(Math.random()*3+4)+"s";
  document.body.appendChild(h);
  setTimeout(()=>h.remove(),7000);
},300);
</script>

</body>
</html>
