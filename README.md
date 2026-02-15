<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Vrushali ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
body {
    margin:0;
    padding:0;
    font-family:'Poppins',sans-serif;
    background:linear-gradient(135deg,#ff9a9e,#fad0c4);
    text-align:center;
    color:white;
    overflow-x:hidden;
}

/* PASSWORD SCREEN */
#lockScreen {
    position:fixed;
    width:100%;
    height:100%;
    background:#ff758c;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    z-index:1000;
}
#lockScreen input {
    padding:10px;
    border:none;
    border-radius:5px;
}
#lockScreen button {
    margin-top:10px;
    padding:8px 15px;
    border:none;
    background:white;
    color:#ff4e7a;
    font-weight:bold;
    border-radius:5px;
    cursor:pointer;
}

/* GOLD NAME */
.name {
    font-family:'Great Vibes',cursive;
    font-size:60px;
    background:linear-gradient(45deg,gold,#fff,gold);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
    animation:shine 3s infinite linear;
}
@keyframes shine {
    0%{background-position:0%;}
    100%{background-position:200%;}
}

/* TYPING */
.typing {
    font-size:26px;
    border-right:3px solid white;
    white-space:nowrap;
    overflow:hidden;
    width:0;
    margin:auto;
    animation:typing 4s steps(40,end) forwards;
}
@keyframes typing {
    from{width:0}
    to{width:100%}
}

.note {
    margin-top:40px;
    font-size:20px;
    line-height:1.8;
    white-space:pre-line;
}

/* POPUP */
#lovePopup {
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:white;
    color:#ff4e7a;
    padding:30px;
    border-radius:15px;
    display:none;
    font-size:28px;
    z-index:2000;
}

/* COUNTDOWN */
#countdown {
    margin-top:30px;
    font-size:20px;
}

/* PROPOSAL BUTTON */
.proposeBtn {
    margin-top:40px;
    padding:12px 25px;
    background:white;
    color:#ff4e7a;
    border:none;
    border-radius:30px;
    font-size:18px;
    cursor:pointer;
    transition:0.3s;
}
.proposeBtn:hover {
    transform:scale(1.1);
}

/* MEMORIES */
.memories{margin-top:80px;}
.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
    gap:20px;
    margin-top:30px;
}
.polaroid{
    background:white;
    padding:10px;
    border-radius:10px;
    transform:scale(0);
    animation:pop 0.8s forwards;
}
.polaroid img{width:100%;border-radius:8px;}
.polaroid:nth-child(1){animation-delay:0.5s;}
.polaroid:nth-child(2){animation-delay:1s;}
.polaroid:nth-child(3){animation-delay:1.5s;}
.polaroid:nth-child(4){animation-delay:2s;}
@keyframes pop{to{transform:scale(1);}}

/* FLOATING HEARTS */
.heart{
    position:fixed;
    bottom:-50px;
    animation:float 8s linear infinite;
}
@keyframes float{
    0%{transform:translateY(0);opacity:1;}
    100%{transform:translateY(-100vh);opacity:0;}
}
.sparkle{
    position:fixed;
    animation:sparkle 5s infinite;
}
@keyframes sparkle{
    0%,100%{opacity:0;transform:scale(0.5);}
    50%{opacity:1;transform:scale(1);}
}
</style>
</head>

<body>

<!-- PASSWORD LOCK -->
<div id="lockScreen">
<h2>Enter Our Secret Password ❤️</h2>
<input type="password" id="passwordInput">
<button onclick="checkPassword()">Unlock</button>
</div>

<!-- POPUP -->
<div id="lovePopup">I Love You Vrushali ❤️</div>

<audio autoplay loop>
<source src="romantic.mp3" type="audio/mp3">
</audio>

<div class="container">

<div class="name">Vrushali ❤️</div>
<div class="typing">My Love...</div>

<div class="note">
My day begins with you  
and ends with you in my heart.

You are my peace, my happiness,  
my safest place, and my forever.

Every single day I fall for you more.  
Your smile melts my heart effortlessly.

Without you, life feels incomplete.  
With you, love feels eternal.
</div>

<div id="countdown"></div>

<button class="proposeBtn" onclick="showLove()">Will You Stay With Me Forever? 💍</button>

<div style="margin-top:40px;font-size:22px;">
Forever Yours,<br>
Kush ❤️
</div>

<div class="memories">
<h2>✨ Our Memories ✨</h2>
<div class="grid">
<div class="polaroid"><img src="photo1.jpg"></div>
<div class="polaroid"><img src="photo2.jpg"></div>
<div class="polaroid"><img src="photo3.jpg"></div>
<div class="polaroid"><img src="photo4.jpg"></div>
</div>
</div>

</div>

<script>
function checkPassword(){
    if(document.getElementById("passwordInput").value==="onlyus"){
        document.getElementById("lockScreen").style.display="none";
    } else {
        alert("Wrong Password 😘");
    }
}

function showLove(){
    document.getElementById("lovePopup").style.display="block";
}

/* Countdown since first date */
const startDate = new Date("2024-01-01"); // CHANGE THIS
setInterval(()=>{
    const now = new Date();
    const diff = now - startDate;
    const days = Math.floor(diff/(1000*60*60*24));
    document.getElementById("countdown").innerHTML =
    "We have been in love for ❤️ " + days + " days ❤️";
},1000);

/* Hearts */
function createHeart(){
    const heart=document.createElement('div');
    heart.classList.add('heart');
    heart.innerHTML=Math.random()>0.5?"🎈❤️":"😘💋";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(20+Math.random()*20)+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),8000);
}
setInterval(createHeart,800);

function createSparkle(){
    const sparkle=document.createElement('div');
    sparkle.classList.add('sparkle');
    sparkle.innerHTML="✨";
    sparkle.style.left=Math.random()*100+"vw";
    sparkle.style.top=Math.random()*100+"vh";
    document.body.appendChild(sparkle);
    setTimeout(()=>sparkle.remove(),5000);
}
setInterval(createSparkle,1000);
</script>

</body>
</html>
