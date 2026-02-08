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
    animation: textGlow 2s infinite alternate;
}

@keyframes textGlow {
    from {text-shadow: 0 0 5px #fff;}
    to {text-shadow: 0 0 15px #ff4d6d;}
}

.buttons {
    margin-top: 20px;
}

button {
    padding: 12px 25px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    margin: 10px;
    transition: all 0.3s ease;
}

#yesBtn {
    background: #ff4d6d;
    color: white;
}

#noBtn {
    background: #555;
    color: white;
    position: relative;
}

.confetti {
    position: fixed;
    top: -10px;
    width: 10px;
    height: 10px;
    background: red;
    animation: fall 3s linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(110vh) rotate(360deg);
    }
}
</style>
</head>

<body>

<div class="container">
    <div class="text">
        <p><b>Hlo mazhi kaju katli 💋</b><br>
        mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo.<br>
        But tula sangatoy mahiti nahi mla ki ks kay<br>
        but mla tujhyavar prem zalay te pn khup jast<br>
        aani mla mahitiy tujhya baddal sagal kahi tari pn<br>
        mla tujhyavarach prem zalay.<br>
        aani mla <b>tuch havi</b> tujhya sarkhi pn nako.</p>

        <p>.<br>.</p>

        <p>
        Ki karu sukhane sansar aapan.<br>
        <b>Tu premachi pahili payari hoshil ka 💕</b>
        </p>

        <p>
        Lihil nanyane swatahala tujhya sobat.<br>
        <b>Tu aayushyachi dairy hoshil ka 🧿</b>
        </p>

        <p>
        Aani jevha yeu yekatr aapan,<br>
        duniya karel kautuk aapl 🍂🌸
        </p>

        <p>
        Mi hoto shabd tuzhe.<br>
        <b>Tu mazhi shayari hoshil ka 🫂🤌🤍💋❤️</b>
        </p>

        <p>.<br>.</p>

        <p><b>Say S or No 🤌🤍</b></p>
    </div>

    <div class="buttons">
        <button id="yesBtn">YES 💕</button>
        <button id="noBtn">NO 🙈</button>
    </div>
</div>

<audio id="music" src="love.mp3"></audio>

<script>
const yesBtn = document.getElementById("yesBtn");
const noBtn = document.getElementById("noBtn");
const music = document.getElementById("music");

noBtn.addEventListener("mouseover", () => {
    yesBtn.style.transform = "scale(1.3)";
});

noBtn.addEventListener("mouseout", () => {
    yesBtn.style.transform = "scale(1)";
});

yesBtn.addEventListener("click", () => {
    music.play();
    for (let i = 0; i < 80; i++) {
        const confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random() * 100 + "vw";
        confetti.style.backgroundColor =
            `hsl(${Math.random() * 360},100%,50%)`;
        confetti.style.animationDuration =
            Math.random() * 3 + 2 + "s";
        document.body.appendChild(confetti);

        setTimeout(() => confetti.remove(), 5000);
    }
    alert("Anjali ❤️ I love you so much much more and ever 🌍💋");
});
</script>

</body>
</html>
