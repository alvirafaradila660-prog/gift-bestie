<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Gift For My Bestie 💖</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>
body{
  font-family:'Poppins',sans-serif;
  margin:0;
  background:linear-gradient(180deg,#fff0f5,#ffe4ec);
}

.container{
  max-width:430px;
  margin:auto;
  background:white;
  min-height:100vh;
  padding:20px;
}

/* PAGE */
.page{display:none;}
.page.active{display:block;}

h1{text-align:center;color:#d81b60}

/* CARD */
.card{
  border:2px solid #d81b60;
  padding:20px;
  border-radius:20px;
  margin:10px 0;
  text-align:center;
  cursor:pointer;
}

/* VIDEO */
.video-box video{
  width:100%;
  border-radius:15px;
  border:3px solid #d81b60;
}
</style>
</head>

<body>

<div class="container">

<!-- HOME -->
<div class="page active" id="home">
  <h1>THIS IS FOR YOU 💖</h1>

  <div class="card" onclick="openPage('memories')">
    🎥 Memories
  </div>

  <div class="card" onclick="openPage('music')">
    🎵 Song
  </div>
</div>

<!-- MEMORIES -->
<div class="page" id="memories">
  <h1>Memories 🎥</h1>

  <div class="video-box">
    <video controls>
      <source src="./memories.mp4" type="video/mp4">
    </video>
  </div>

  <div class="card" onclick="goHome()">Back</div>
</div>

<!-- MUSIC -->
<div class="page" id="music">
  <h1>Song 🎵</h1>

  <div class="video-box">
    <video controls>
      <source src="./song.mp4" type="video/mp4">
    </video>
  </div>

  <div class="card" onclick="goHome()">Back</div>
</div>

</div>

<script>
function openPage(id){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

function goHome(){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById('home').classList.add('active');
}
</script>

</body>
</html>
