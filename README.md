<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Anjali ❤️</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    text-align: center;
    overflow-x: hidden;
}

.container {
    background: rgba(255,255,255,0.2);
    border-radius: 20px;
    padding: 20px;
    width: 90%;
    max-width: 500px;
    backdrop-filter: blur(10px);
    border: 3px solid #fff;
    animation: fadeIn 1.5s ease;
}

@keyframes fadeIn {
    from {opacity:0; transform: scale(0.9);}
    to {opacity:1; transform: scale(1);}
}

.text {
    color: #fff;
    font-size: 16px;
    line-height: 1.6;
    min-height: 250px;
}

#goBtn{
    margin-top:20px;
    padding:12px 30px;
    font-size:18px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    background:#fff;
    color:#ff2d75;
    box-shadow:0 0 20px #fff;
    animation:pulse 2s infinite;
}
@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.1);}
    100%{transform:scale(1);}
}

.buttons{
    margin-top:20px;
    display:none;
}

button{
    padding:12px 25px;
    font-size:18px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:10px;
    transition:0.3s;
}

#yesBtn{background:#ff4d6d; color:white;}
#noBtn{background:#555; color:white; position:relative;}

.confetti{
    position:fixed;
    top:-10px;
    width:10px;
    height:10px;
    background:red;
    animation:fall 3s linear infinite;
}
@keyframes fall{
    to{transform:translateY(110vh) rotate(360deg);}
}
</style>
</head>
<body>

<div class="container">
    <div class="text" id="majkurText">
        <h2>Babydoll I have something to say…</h2>
    </div>

    <button id="goBtn" onclick="startMajkur()">GO 💫</button>

    <div class="buttons" id="ynButtons">
        <button id="yesBtn">YES 💕</button>
        <button id="noBtn">NO 🙈</button>
    </div>
</div>

<audio id="music" src="love.mp3"></audio>

<script>
const majkurText = document.getElementById("majkurText");
const goBtn = document.getElementById("goBtn");
const ynButtons = document.getElementById("ynButtons");
const yesBtn = document.getElementById("yesBtn");
const noBtn = document.getElementById("noBtn");
const music = document.getElementById("music");

const text = `Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo.
But tula sangatoy mahiti nahi mla ki ks kay
but mla tujhyavar prem zalay te pn khup jast
aani mla mahitiy tujhya baddal sagal kahi tari pn
mla tujhyavarach prem zalay.
aani mla tuch havi tujhya sarkhi pn nako.

.

.

Ki karu sukhane sansar aapan.
Tu premachi pahili payari hoshil ka 💕
Lihil nanyane swatahala tujhya sobat.
Tu aayushyachi dairy hoshil ka 🧿
Aani jevha yeu yekatr aapan.
duniya karel kautuk aapl 🍂🌸
Mi hoto shabd tuzhe.
Tu mazhi shayari hoshil ka 🫂🤌🤍💋❤️

.

.
Say S or No 🤌🤍`;

let i = 0;
function startMajkur(){
    goBtn.style.display = "none";
    majkurText.innerHTML = "";
    typeMajkur();
}

function typeMajkur(){
    if(i < text.length){
        majkurText.innerHTML += text.charAt(i);
        i++;
        setTimeout(typeMajkur,25);
    } else {
        ynButtons.style.display = "block";
    }
}

// NO button hover
noBtn.addEventListener("mouseover", () => {
    yesBtn.style.transform = "scale(1.3)";
});
noBtn.addEventListener("mouseout", () => {
    yesBtn.style.transform = "scale(1)";
});

// YES click
yesBtn.addEventListener("click", () => {
    music.play();
    for(let i=0;i<80;i++){
        const confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random()*100+"vw";
        confetti.style.backgroundColor=`hsl(${Math.random()*360},100%,50%)`;
        confetti.style.animationDuration=(Math.random()*3+2)+"s";
        document.body.appendChild(confetti);
        setTimeout(()=>confetti.remove(),5000);
    }
    alert("Anjali ❤️ I love you so much much more and ever 🌍💋");
});
</script>

</body>
</html>
