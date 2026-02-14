# alpinebeat.gifthub.io
<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AlpineBeat - Lyžování budoucnosti</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family: Arial, Helvetica, sans-serif;
}

body{
background:#fff;
color:#111;
overflow-x:hidden;
}

header{
position:fixed;
width:100%;
padding:20px 10%;
display:flex;
justify-content:space-between;
align-items:center;
background:rgba(0,0,0,0.8);
backdrop-filter: blur(10px);
color:white;
z-index:1000;
}

header h1{
letter-spacing:2px;
}

nav a{
color:white;
text-decoration:none;
margin-left:20px;
font-weight:bold;
transition:0.3s;
}

nav a:hover{
opacity:0.6;
}

.hero{
height:100vh;
background:linear-gradient(to right,#000000cc,#00000099),
url('https://images.unsplash.com/photo-1519681393784-d120267933ba');
background-size:cover;
background-position:center;
display:flex;
flex-direction:column;
justify-content:center;
padding:0 10%;
color:white;
}

.hero h2{
font-size:65px;
animation: slideDown 1.2s ease forwards;
}

.hero p{
font-size:22px;
margin:20px 0;
animation: fadeIn 2s ease forwards;
}

.hero button{
padding:15px 35px;
border:none;
background:white;
color:black;
font-weight:bold;
cursor:pointer;
transition:0.4s;
animation: fadeIn 2.5s ease forwards;
}

.hero button:hover{
background:black;
color:white;
transform:scale(1.05);
}

section{
padding:120px 10%;
}

.features{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:40px;
}

.feature-box{
padding:40px;
border:1px solid #eee;
text-align:center;
opacity:0;
transform:translateY(40px);
transition:all 0.8s ease;
}

.feature-box:hover{
transform:translateY(-10px);
box-shadow:0 15px 40px rgba(0,0,0,0.15);
}

.feature-box.show{
opacity:1;
transform:translateY(0);
}

footer{
background:black;
color:white;
text-align:center;
padding:40px;
}

/* ANIMACE */
@keyframes slideDown{
from{
opacity:0;
transform:translateY(-40px);
}
to{
opacity:1;
transform:translateY(0);
}
}

@keyframes fadeIn{
from{opacity:0;}
to{opacity:1;}
}

</style>
</head>

<body>

<header>
<h1>AlpineBeat</h1>
<nav>
<a href="#">Domů</a>
<a href="#produkt">Produkt</a>
<a href="#onas">O nás</a>
</nav>
</header>

<section class="hero">
<h2>Lyžování budoucnosti</h2>
<p>Zažij revoluci na svahu s chytrou helmou AlpineBeat.</p>
<button onclick="scrollToSection()">Objev produkt</button>
</section>

<section id="produkt">
<h2>Náš produkt</h2>
<p style="margin:20px 0 60px 0;">
Chytrá helma AlpineBeat spojuje bezpečnost, komunikaci a moderní technologie do jednoho zařízení.
</p>

<div class="features">
<div class="feature-box">🎧<h3>Zabudovaná sluchátka</h3><p>Hudba přímo během jízdy.</p></div>
<div class="feature-box">🗣<h3>Hlasový asistent</h3><p>Ovládání hlasem bez použití rukou.</p></div>
<div class="feature-box">📍<h3>GPS Lokátor</h3><p>Najdi své přátele na svahu.</p></div>
<div class="feature-box">📞<h3>Volání</h3><p>Telefonuj přímo přes helmu.</p></div>
<div class="feature-box">⚠<h3>Varování před nebezpečím</h3><p>Zvýšená bezpečnost při jízdě.</p></div>
</div>
</section>

<section id="onas">
<h2>O nás</h2>
<p style="margin-top:20px;">
Jsme tým mladých inovátorů, kteří chtějí změnit budoucnost zimních sportů.
</p>
</section>

<footer>
<h3>AlpineBeat</h3>
<p>© 2026 AlpineBeat | Lyžování budoucnosti</p>
</footer>

<script>
function scrollToSection(){
document.getElementById("produkt").scrollIntoView({behavior:"smooth"});
}

/* Animace při scrollování */
const boxes = document.querySelectorAll(".feature-box");

window.addEventListener("scroll", () => {
boxes.forEach(box => {
const boxTop = box.getBoundingClientRect().top;
const trigger = window.innerHeight - 100;
if(boxTop < trigger){
box.classList.add("show");
}
});
});
</script>

</body>
</html>
