<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Untuk Sayangku ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
    background:
    radial-gradient(circle at top left,#ff6b9d,transparent 40%),
    radial-gradient(circle at bottom right,#a855f7,transparent 40%),
    #0f172a;
}

/* Partikel */
.particles{
    position:fixed;
    inset:0;
    pointer-events:none;
}

/* Tombol amplop */
.envelope{
    width:240px;
    height:240px;
    border:none;
    border-radius:35px;
    background:rgba(255,255,255,0.12);
    backdrop-filter:blur(20px);
    color:white;
    cursor:pointer;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    gap:12px;
    font-size:80px;
    box-shadow:0 0 40px rgba(255,255,255,.15);
    transition:.4s;
    z-index:10;
}

.envelope:hover{
    transform:translateY(-10px) scale(1.05);
    box-shadow:0 0 60px rgba(255,182,193,.5);
}

.envelope span{
    font-size:18px;
    font-weight:600;
}

/* Surat */
.card{
    display:none;
    width:90%;
    max-width:850px;
    max-height:85vh;
    overflow-y:auto;
    padding:40px;
    background:rgba(255,255,255,0.08);
    backdrop-filter:blur(25px);
    border:1px solid rgba(255,255,255,0.15);
    border-radius:30px;
    color:white;
    box-shadow:0 20px 50px rgba(0,0,0,.3);
    animation:showCard 1s ease;
    z-index:10;
}

@keyframes showCard{
    from{
        opacity:0;
        transform:translateY(40px) scale(.9);
    }
    to{
        opacity:1;
        transform:translateY(0) scale(1);
    }
}

h1{
    text-align:center;
    margin-bottom:10px;
}

.date{
    text-align:center;
    opacity:.8;
    margin-bottom:20px;
}

.love{
    text-align:center;
    font-size:60px;
    margin-bottom:20px;
    animation:beat 1.2s infinite;
}

@keyframes beat{
    50%{
        transform:scale(1.2);
    }
}

p{
    line-height:1.9;
    margin-bottom:18px;
    font-size:17px;
}

.footer{
    text-align:center;
    margin-top:25px;
    font-size:20px;
    font-weight:600;
    color:#ffc0cb;
}

/* Scrollbar */
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

<div class="particles"></div>

<button id="openBtn" class="envelope">
    💌
    <span>Tekan Disini Ya Sayang ❤️</span>
</button>

<div class="card" id="card">

    <h1>🎓 Selamat Wisuda Sayangku Tercinta 🎓</h1>

    <div class="date">
        15 Juni 2026 ❤️
    </div>

    <div class="love">💖</div>

    <p>
        Hari ini adalah hari yang sangat istimewa.
        Setelah begitu banyak perjuangan, doa, air mata,
        dan senyum yang kamu lalui,
        akhirnya kamu berhasil sampai di titik yang indah ini.
    </p>

    <p>
        Aku bangga sekali padamu.
        Bukan hanya karena gelar yang kamu raih,
        tetapi karena kerja keras, ketekunan,
        dan semangatmu yang tidak pernah menyerah.
    </p>

    <p>
        Terima kasih karena selalu berjuang,
        bahkan ketika keadaan terasa berat.
        Terima kasih karena sudah menjadi pribadi yang kuat,
        hebat, dan menginspirasi.
    </p>

    <p>
        Semoga setelah wisuda ini,
        semua impian yang kamu simpan perlahan menjadi kenyataan.
        Semoga setiap langkahmu dipenuhi keberkahan,
        kebahagiaan, kesehatan, dan kesuksesan.
    </p>

    <p>
        Jangan pernah meragukan dirimu sendiri.
        Kamu jauh lebih hebat daripada yang kamu pikirkan.
        Aku akan selalu mendukungmu dan bangga padamu.
    </p>

    <p>
        Selamat wisuda sayangku ❤️
        Hari ini dunia melihat keberhasilanmu,
        dan aku melihat alasan lain untuk semakin bangga mencintaimu.
    </p>

    <div class="footer">
        Dengan penuh cinta ❤️<br>
        Untuk Sayangku Tercinta 💕
    </div>

</div>

<script>
// Buka surat
const btn = document.getElementById("openBtn");
const card = document.getElementById("card");

btn.addEventListener("click",()=>{
    btn.style.display="none";
    card.style.display="block";
});

// Partikel hati & bintang
setInterval(()=>{
    const p=document.createElement("div");

    const icons=[
        "❤️","💕","💖","💗","💓",
        "💞","✨","⭐"
    ];

    p.innerHTML=icons[Math.floor(Math.random()*icons.length)];

    p.style.position="fixed";
    p.style.left=Math.random()*100+"vw";
    p.style.top="-20px";
    p.style.fontSize=(Math.random()*18+12)+"px";
    p.style.pointerEvents="none";
    p.style.zIndex="1";

    document.body.appendChild(p);

    let pos=-20;

    const anim=setInterval(()=>{
        pos+=2;
        p.style.top=pos+"px";
        p.style.opacity=1-(pos/window.innerHeight);

        if(pos>window.innerHeight){
            clearInterval(anim);
            p.remove();
        }
    },20);

},150);
</script>

</body>
</html>
