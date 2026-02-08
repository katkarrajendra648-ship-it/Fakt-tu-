<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Anjali ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
    margin:0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(120deg,#ff5fa2,#ff9a9e);
    color:white;
    overflow-x:hidden;
}

.container{
    max-width:800px;
    margin:auto;
    padding:20px;
    text-align:center;
}

.majkur{
    font-size:18px;
    line-height:1.7;
    animation: heartbeat 2s infinite;
}

@keyframes heartbeat{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.02);}
}

.buttons{
    margin-top:30px;
}

button{
    padding:15px 30px;
    font-size:18px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:10px;
}

#yesBtn{
    background:#fff;
    color:#ff2d75;
    transition:0.3s;
}

#noBtn{
    background:#ff2d75;
    color:white;
}

/* Popup */
.popup{
    position:fixed;
    top:0; left:0;
    width:100%; height:100%;
    background:rgba(0,0,0,0.9);
    display:none;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    z-index:999;
}

.slide{
    display:none;
    text-align:center;
}

.slide img{
    max-width:80%;
    max-height:70vh;
    border-radius:20px;
    box-shadow:0 0 20px #ff5fa2;
}

.caption{
    margin-top:15px;
    font-size:22px;
    color:#fff;
    animation: fadeIn 1.5s;
}

@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

.close{
    position:absolute;
    top:20px;
    right:20px;
    font-size:30px;
    cursor:pointer;
}

.hearts span{
    position:fixed;
    bottom:-20px;
    color:#ff5fa2;
    font-size:20px;
    animation: float 6s linear infinite;
}

@keyframes float{
    0%{transform:translateY(0); opacity:1;}
    100%{transform:translateY(-110vh); opacity:0;}
}
</style>
</head>

<body>

<div class="container">
<div class="majkur">
Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo.
But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast
aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay.
Tula mahity ka mi sagalyana sangitalay ki mi tujhyavar prem karato aani mla tuch havi
tujhya sarkhi pn nako. Aani tu thambshil rahashil mla sodun jashil mla kahi ghen den nahi
but I know ki tu pahije.

<br><br>
I love you love you love you so much much more and ever 🌍💗😘  
fakt tuch. khup prem zalay tujhyavar tuch aani tuch pahije  
majhya black and white zindagi madhi colourfull person tu 🧿

<br><br>
Mazhi special one mazhi kaju katli 💋  
mazhi aaichyaa hatachi puranpoli 💕😘🌎  
love you babydoll mazhi 💗🫂😘🌎

<br><br>
Anjali i love you yar 🥺🤌💕🫂🌎🧿  
say yes or no 🤌🤍
</div>

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
ur my everything 💖<br>
Anjali i love you so much<br>
much more and ever 🌍💋🫂🧿
</div>
</div>

<audio id="music" src="love.mp3"></audio>
</div>

<script>
let yesSize = 1;
let slideIndex = 0;
let slides;

function growYes(){
    yesSize += 0.2;
    document.getElementById("yesBtn").style.transform =
        `scale(${yesSize})`;
}

function openPopup(){
    document.getElementById("popup").style.display="flex";
    slides = document.getElementsByClassName("slide");
    slideIndex = 0;
    showSlide();
    document.getElementById("music").play();
}

function closePopup(){
    document.getElementById("popup").style.display="none";
    document.getElementById("music").pause();
}

function showSlide(){
    for(let i=0;i<slides.length;i++){
        slides[i].style.display="none";
    }
    slides[slideIndex].style.display="block";
    slideIndex++;
    if(slideIndex >= slides.length) slideIndex = 0;
    setTimeout(showSlide,3000);
}

/* hearts */
setInterval(()=>{
    const heart=document.createElement("span");
    heart.innerHTML="❤️";
    heart.style.left=Math.random()*100+"vw";
    heart.style.animationDuration=(Math.random()*3+3)+"s";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),6000);
},400);
</script>

</body>
</html>
