<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Tanishka 📖💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body{
    margin:0;
    font-family:'Poppins',sans-serif;
    background:linear-gradient(120deg,#fbc2eb,#a6c1ee);
    overflow-x:hidden;
}

.book{
    width:95%;
    max-width:420px;
    margin:40px auto;
    perspective:2500px;
    position:relative;
}

.page{
    width:100%;
    height:560px;
    position:absolute;
    background-size:cover;
    background-position:center;
    border-radius:20px 40px 40px 20px;
    box-shadow:0 25px 45px rgba(0,0,0,.25);
    transform-origin:left;
    transform-style:preserve-3d;
    transition:transform 1.3s ease;
    overflow:hidden;
}

.front,.back{
    position:absolute;
    width:100%;
    height:100%;
    padding:25px;
    box-sizing:border-box;
    backface-visibility:hidden;
}

.front{
    background:rgba(255,255,255,.78);
    border-radius:inherit;
}

.back{
    transform:rotateY(180deg);
}

.page.flipped{
    transform:rotateY(-180deg);
}
.page.flipped .front{
    display:none;
}

.page h1,.page h2{
    text-align:center;
    color:#ff5fa2;
    font-family:'Patrick Hand',cursive;
    font-weight: 800;
}
.page p{
    text-align:center;
    font-size:17px;
    color:#444;
    line-height:1.6;
}
.open-btn{
    position: absolute;
    bottom: 40px;        /* move up/down here */
    left: 50%;
    transform: translateX(-50%);
}

button{
    
    display:block;
    margin:50px auto;
    padding:10px 34px;
    font-size:16px;
    border:none;
    background:#f20101;
    color:#fff;
    border-radius:30px;
    cursor:pointer;
}

.photo{
    width:180px;
    height:180px;
    border-radius:50%;
    background-size:cover;
    background-position:center;
    margin:20px auto;
    border:6px solid #ff5fa2;
}

.photo-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:15px;
    margin-top:20px;
}
.photo-grid div{
    height:160px;
    border-radius:18px;
    background-size:cover;
    background-position:center;
}

.friendship{
    background:rgba(255,255,255,.9);
    border-radius:18px;
    padding:18px;
    margin-top:20px;
    font-family:'Patrick Hand',cursive;
}

#page1{z-index:5;}
#page2{z-index:4;}
#page3{z-index:3;}
#page4{z-index:2;}
#page5{z-index:1;}

@media(max-width:480px){
    .page{height:520px;}
    .photo{width:150px;height:150px;}
}
</style>
</head>

<body>

<audio id="bgMusic" loop>
    <source src="soft-music.mp3" type="audio/mpeg">
</audio>

<div class="book">

<!-- PAGE 1 (COVER – image ONLY before flip) -->
<div class="page" id="page1">
    <div class="front" style="background:url('cover.jpg') center/cover no-repeat;">
        <h1 style="text-align:center;
    color:#ffffff;
    font-family:'Patrick Hand',cursive;
    font-weight: 800;">Happy Birthday 🎉</h1>
        <h2 style="text-align:center;
    color:#ffffff;
    font-family:'Patrick Hand',cursive;
    font-weight: 800;">Tanishka 💖</h2>
        <p style="text-align:center;
    color:#ffffff;
    font-family:'Patrick Hand',cursive;
    font-weight: 800;">23rd December ✨<br>A beautiful soul deserves a beautiful day 🌸</p>
      <button class="open-btn" onclick="flipPage(1)">Open Notebook ➜</button>

    </div>
    <div class="back"></div>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2" style="background-image:url('photo1.jpg')">
    <div class="front">
        <h1>For You 🤍</h1>
        <div class="photo" style="background-image:url('photo1.jpg')"></div>
        <p>May your life be filled with smiles 😊<br>dreams 🌈 and happiness ✨</p>
        <button onclick="flipPage(2)">Next ➜</button>
    </div>
    <div class="back"></div>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3" style="background-image:url('collage.jpg')">
    <div class="front">
        <h1>Your Moments 📸</h1>
        <div class="photo-grid">
            <div style="background-image:url('photo1.jpg')"></div>
            <div style="background-image:url('photo2.jpg')"></div>
            <div style="background-image:url('photo3.jpg')"></div>
            <div style="background-image:url('photo4.jpg')"></div>
        </div>
        <button onclick="flipPage(3)">Next ➜</button>
    </div>
    <div class="back"></div>
</div>

<!-- PAGE 4 -->
<div class="page" id="page4" style="background-image:url('note-bg.jpg')">
    <div class="front">
        <h1>Friendship 💕</h1>
        <div class="friendship">
            You are not just my friend,<br>
            you are my safe place 🤍<br><br>
            Thank you for laughs 😂<br>
            talks 🌙 and memories ✨
        </div>
        <button onclick="flipPage(4)">Next ➜</button>
    </div>
    <div class="back"></div>
</div>

<!-- PAGE 5 -->
<div class="page" id="page5" style="background-image:url('end.jpg')">
    <div class="front">
        <h1>Thank You 🌸</h1>
        <p>For being YOU 💖<br>Happy Birthday 🎂✨</p>
        <p>📖💖🌸✨🧸</p>
    </div>
    <div class="back"></div>
</div>

</div>

<script>
const music=document.getElementById('bgMusic');
document.addEventListener('click',()=>{if(music.paused)music.play();});
function flipPage(n){document.getElementById('page'+n).classList.add('flipped');}
</script>

</body>
</html>
