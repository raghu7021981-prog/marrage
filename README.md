<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prasanna ❤️ Mani Wedding</title>

<style>
body {
    margin:0;
    font-family:'Georgia',serif;
    overflow-x:hidden;
}

/* LOGIN PAGE */
#loginPage {
    height:100vh;
    background: linear-gradient(135deg, maroon, gold);
    display:flex;
    justify-content:center;
    align-items:center;
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
    width:200px;
}

button {
    padding:10px 20px;
    background:maroon;
    color:white;
    border:none;
    cursor:pointer;
}

/* MAIN SITE */
#mainSite {
    display:none;
}

/* HERO */
.hero {
    height:100vh;
    background: linear-gradient(rgba(0,0,0,0.6), rgba(90,15,46,0.8)),
    url('https://images.unsplash.com/photo-1504198453319-5ce911bafcde?w=1600');
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
}

.hero h2 {
    font-size:2rem;
}

/* COUPLE */
.couple img {
    width:350px;
    border-radius:20px;
    box-shadow:0 10px 40px rgba(0,0,0,0.5);
}

/* MESSAGE */
.message {
    max-width:800px;
    margin:auto;
    background:#fff;
    padding:40px;
    border-radius:20px;
    font-size:20px;
    line-height:1.8;
}

/* FLOATING */
.float {
    position:fixed;
    top:-20px;
    animation:fall linear infinite;
    font-size:25px;
}

@keyframes fall {
    to { transform: translateY(110vh); }
}

/* FOOTER */
footer {
    background:maroon;
    color:gold;
    text-align:center;
    padding:20px;
}
</style>
</head>

<body>

<!-- LOGIN -->
<div id="loginPage">
    <div class="login-box">
        <h2>💖 Welcome 💖</h2>
        <input type="text" id="user" placeholder="Username"><br>
        <input type="password" id="pass" placeholder="Password"><br>
        <button onclick="login()">Enter</button>
    </div>
</div>

<!-- MAIN SITE -->
<div id="mainSite">

<!-- MUSIC -->
<audio autoplay loop>
    <source src="https://pagalworld.com.se/files/download/id/64603" type="audio/mp3">
</audio>

<!-- HERO -->
<div class="hero">
    <h1>Prasanna ❤️ Mani</h1>
    <h2>Forever Begins on May 3, 2026</h2>
    <h3 id="countdown"></h3>
</div>

<!-- COUPLE -->
<section class="couple" style="text-align:center; padding:50px;">
    <h2>💑 A Perfect Pair</h2>
    <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?w=500">
</section>

<!-- MESSAGE -->
<section>
<div class="message">
<p>Dear Akka Prasanna & Bava Mani,</p>

<p>
Akka, you are not just my sister… you are my world, my strength, and my biggest inspiration.
Seeing you as a bride is the most beautiful moment of my life.
</p>

<p>
Bava, you are truly lucky… but more than that, we are lucky to have you in our family.
You complete my Akka in the most perfect way.
</p>

<p>
Your love story is not just beautiful… it is magical.
May your life be filled with endless happiness, success, laughter, and unforgettable memories.
</p>

<p>
I am so proud, so emotional, and so happy for both of you.
This is not just a wedding… it is the beginning of a beautiful forever.
</p>

<p><b>❤️ Love you forever ❤️</b><br>
— Anneda Raghu Vardhan Reddy</p>
</div>
</section>

<footer>
Made with ❤️ for Prasanna & Mani
</footer>

</div>

<script>

/* LOGIN FUNCTION */
function login(){
    let u=document.getElementById("user").value;
    let p=document.getElementById("pass").value;

    if(u==="Prasanna and mani" && p==="352026"){
        document.getElementById("loginPage").style.display="none";
        document.getElementById("mainSite").style.display="block";
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

/* FLOATING HEARTS & FLOWERS */
for(let i=0;i<25;i++){
    let el=document.createElement("div");
    el.className="float";
    el.innerHTML = Math.random()>0.5 ? "💖" : "🌸";
    el.style.left=Math.random()*100+"vw";
    el.style.animationDuration=(4+Math.random()*6)+"s";
    document.body.appendChild(el);
}
</script>

</body>
</html>
