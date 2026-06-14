<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Untuk Bochillkuu Tersayang ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins',sans-serif;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
    background:
    radial-gradient(circle at top left,#ff6b9d55,transparent 35%),
    radial-gradient(circle at bottom right,#a855f755,transparent 35%),
    #0f172a;
}

/* Partikel */
#particles{
    position:fixed;
    inset:0;
    overflow:hidden;
    z-index:0;
}

.particle{
    position:absolute;
    opacity:0.18;
    pointer-events:none;
    animation:fall linear forwards;
}

@keyframes fall{
    from{
        transform:translateY(-50px);
    }
    to{
        transform:translateY(110vh);
    }
}

/* Amplop */
.envelope{
    z-index:10;
    width:260px;
    height:260px;
    border:none;
    cursor:pointer;
    border-radius:35px;
    color:white;
    background:rgba(255,255,255,0.08);
    backdrop-filter:blur(20px);
    box-shadow:0 0 50px rgba(255,105,180,.25);
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    transition:.4s;
}

.envelope:hover{
    transform:scale(1.05);
}

.envelope .icon{
    font-size:85px;
}

.envelope .text{
    margin-top:10px;
    font-size:18px;
    font-weight:600;
}

/* Surat */
.card{
    display:none;
    position:relative;
    z-index:10;
    width:92%;
    max-width:850px;
    max-height:85vh;
    overflow-y:auto;
    padding:40px;
    border-radius:30px;
    background:rgba(255,255,255,0.08);
    backdrop-filter:blur(20px);
    border:1px solid rgba(255,255,255,0.15);
    color:white;
    box-shadow:0 20px 60px rgba(0,0,0,.35);
    animation:showCard 1s ease;
}

@keyframes showCard{
    from{
        opacity:0;
        transform:translateY(30px) scale(.95);
    }
    to{
        opacity:1;
        transform:translateY(0) scale(1);
    }
}

h1{
    text-align:center;
    font-family:'Playfair Display',serif;
    margin-bottom:10px;
    font-size:38px;
}

.date{
    text-align:center;
    opacity:.8;
    margin-bottom:25px;
}

.love{
    text-align:center;
    font-size:55px;
    margin-bottom:20px;
    animation:beat 1.3s infinite;
}

@keyframes beat{
    50%{
        transform:scale(1.15);
    }
}

p{
    line-height:2;
    margin-bottom:18px;
    font-size:17px;
    color:#f8fafc;
}

.footer{
    margin-top:30px;
    text-align:center;
    color:#ffc0cb;
    font-size:20px;
    font-weight:600;
}

.signature{
    margin-top:15px;
    text-align:center;
    font-size:28px;
}

::-webkit-scrollbar{
    width:6px;
}
::-webkit-scrollbar-thumb{
    background:#ff8fb1;
    border-radius:20px;
}
</style>
</head>

<body>

<div id="particles"></div>

<button class="envelope" id="openBtn">
    <div class="icon">💌</div>
    <div class="text">Tekan Disini Ya Sayang ❤️</div>
</button>

<div class="card" id="card">

<h1>🎓 Selamat Wisuda Sayangku 🎓</h1>

<div class="date">
15 Juni 2026 ❤️
</div>

<div class="love">💖</div>

<p>
Hari ini adalah hari yang sangat spesial. Setelah semua perjuangan, tugas, ujian, rasa lelah, doa, dan air mata yang pernah kamu lewati, akhirnya kamu berhasil sampai di titik ini.
</p>

<p>
Aku ingin kamu tahu bahwa aku bangga sekali padamu. Bukan hanya karena kamu berhasil wisuda, tetapi karena aku tahu betapa kerasnya perjuangan yang kamu lakukan untuk sampai di sini.
</p>

<p>
Terima kasih karena selalu kuat ketika keadaan tidak mudah. Terima kasih karena tidak menyerah meskipun banyak hal yang mungkin membuatmu lelah.
</p>

<p>
Semoga setelah hari ini, semua mimpi yang kamu simpan perlahan menjadi kenyataan. Semoga setiap langkahmu dipenuhi kebahagiaan, keberuntungan, kesehatan, dan keberkahan yang tidak ada habisnya.
</p>

<p>
Jangan pernah meragukan dirimu sendiri ya sayang. Kamu jauh lebih hebat daripada yang kamu bayangkan. Aku percaya kamu bisa mencapai hal-hal besar di masa depan.
</p>

<p>
Selamat wisuda bochillkuu tersayanggg ❤️. Hari ini dunia melihat keberhasilanmu, dan aku melihat alasan lain untuk semakin bangga mencintaimu.
</p>

<div class="footer">
💌 DARI AUFI UNTUK BOCHILLKUUUU TERSAYANGG 💌
</div>

<div class="signature">
💕 Aku Bangga Padamu Selalu 💕
</div>

</div>

<script>
// Buka surat
const openBtn = document.getElementById("openBtn");
const card = document.getElementById("card");

openBtn.onclick = () => {
    openBtn.style.display = "none";
    card.style.display = "block";
};

// Partikel estetik (jarang agar tidak menutupi tulisan)
const particles = document.getElementById("particles");

setInterval(() => {

    const p = document.createElement("div");

    const icons = ["❤️","💕","💖","✨"];

    p.className = "particle";
    p.innerHTML = icons[Math.floor(Math.random()*icons.length)];

    p.style.left = Math.random()*100 + "vw";
    p.style.fontSize = (12 + Math.random()*10) + "px";
    p.style.animationDuration = (8 + Math.random()*6) + "s";

    particles.appendChild(p);

    setTimeout(() => {
        p.remove();
    }, 15000);

}, 700);
</script>

</body>
</html>
