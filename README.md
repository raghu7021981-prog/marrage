
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Prasanna ❤️ Mani Wedding</title>

<style>
body {
    margin:0;
    font-family:'Georgia',serif;
    background:linear-gradient(to bottom,#fff5e6,#ffe6e6);
}

/* LOGIN */
#loginPage {
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg, maroon, gold);
}

.login-box {
    background:white;
    padding:30px;
    border-radius:15px;
    text-align:center;
}

input {
    padding:10px;
    margin:10px;
}

button {
    padding:10px 20px;
    background:maroon;
    color:white;
}

/* MAIN */
#mainSite { display:none; }

/* HERO */
.hero {
    height:100vh;
    background:linear-gradient(rgba(0,0,0,0.6),rgba(90,15,46,0.8)),
    url('https://images.unsplash.com/photo-1511285560929-80b456fea0bc?w=1600');
    background-size:cover;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    color:gold;
    text-align:center;
}

.hero h1 {
    font-size:4rem;
    text-shadow:0 0 20px gold;
}

/* SECTION */
section {
    padding:80px 20px;
    text-align:center;
}

/* COUPLE */
.couple img {
    border-radius:20px;
    box-shadow:0 0 30px gold;
}

/* MESSAGE */
.message {
    max-width:800px;
    margin:auto;
    background:white;
    padding:40px;
    border-radius:20px;
    line-height:1.8;
}

/* GALLERY */
.gallery img {
    width:250px;
    margin:10px;
    border-radius:15px;
}

/* FLOATING */
.float {
    position:fixed;
    top:-20px;
    animation:fall linear infinite;
}

@keyframes fall {
    to { transform:translateY(110vh); }
}

/* FOOTER */
footer {
    background:maroon;
    color:gold;
    padding:20px;
}
</style>
</head>

<body>

<!-- LOGIN -->
<div id="loginPage">
    <div class="login-box">
        <h2>💖 Welcome Prasanna & Mani 💖</h2>
        <input type="text" id="user" placeholder="Username"><br>
        <input type="password" id="pass" placeholder="Password"><br>
        <button onclick="login()">Enter</button>
    </div>
</div>

<!-- MAIN -->
<div id="mainSite">

<!-- MUSIC -->
<audio id="bgMusic" loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_115b9b1a9d.mp3" type="audio/mp3">
</audio>

<!-- HERO -->
<div class="hero">
    <h1>Prasanna ❤️ Mani</h1>
    <h2>Forever Begins on May 3, 2026</h2>
    <h3 id="countdown"></h3>
</div>

<!-- COUPLE -->
<section class="couple">
    <h2>💑 Made For Each Other</h2>
    <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?w=500">
</section>

<!-- STORY -->
<section>
    <h2>✨ A Beautiful Journey</h2>
    <p style="max-width:700px;margin:auto;font-size:18px;">
    Two hearts, two souls, one beautiful journey.  
    This is not just a wedding, but the start of a forever filled with love and happiness.
    </p>
</section>

<!-- MESSAGE -->
<section>
<div class="message">
<p>Dear Akka Prasanna & Bava Mani,</p>

<p>
Akka, you are my strength, my guide, and my everything.
Seeing you as a bride is the most emotional and happiest moment of my life.
</p>

<p>
Bava, you are not just lucky… we are lucky to have you.
You complete my Akka perfectly.
</p>

<p>
May your life be filled with endless love, happiness, and success.
May every day bring new joy and beautiful memories.
</p>

<p><b>❤️ Forever with love ❤️</b><br>
— Anneda Raghu Vardhan Reddy</p>
</div>
</section>

<!-- GALLERY -->
<!-- GALLERY -->
<section>
<h2>📸 Memories</h2>

<div class="gallery" style="display:flex; justify-content:center; flex-wrap:wrap;">

<img src="https://images.unsplash.com/photo-1519741497674-611481863552?w=500">

<!-- YOUR IMAGE (center highlight) -->
<img src="your-image.png" style="width:300px; border:4px solid gold;">

</div>

</section>
<footer>
Made with ❤️ for Prasanna & Mani
</footer>

</div>

<script>

/* LOGIN + MUSIC FIX */
function login(){
    let u=document.getElementById("user").value.toLowerCase();
    let p=document.getElementById("pass").value;

    if(u==="prasanna and mani" && p==="352026"){
        document.getElementById("loginPage").style.display="none";
        document.getElementById("mainSite").style.display="block";

        // PLAY MUSIC AFTER CLICK ✅
        document.getElementById("bgMusic").play();
    } else {
        alert("Wrong Username or Password");
    }
}

/* COUNTDOWN */
const date=new Date("May 3, 2026 18:00:00").getTime();
setInterval(()=>{
    let now=new Date().getTime();
    let gap=date-now;

    let d=Math.floor(gap/(1000*60*60*24));
    let h=Math.floor((gap%(1000*60*60*24))/(1000*60*60));
    let m=Math.floor((gap%(1000*60*60))/(1000*60));
    let s=Math.floor((gap%(1000*60))/1000);

    document.getElementById("countdown").innerHTML=
    d+" Days "+h+" Hours "+m+" Minutes "+s+" Seconds";
},1000);

/* FLOATING */
for(let i=0;i<30;i++){
    let el=document.createElement("div");
    el.className="float";
    el.innerHTML=Math.random()>0.5?"💖":"🌸";
    el.style.left=Math.random()*100+"vw";
    el.style.animationDuration=(4+Math.random()*6)+"s";
    document.body.appendChild(el);
}
</script>

</body>
</html>>
