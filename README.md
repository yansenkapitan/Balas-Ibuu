<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Pesan Rahasia 💌</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;

    font-family: Arial, sans-serif;
    color: white;

    background:
        radial-gradient(circle at 15% 15%,
        rgba(255,255,255,.20) 0 2px,
        transparent 3px),

        radial-gradient(circle at 80% 30%,
        rgba(255,255,255,.15) 0 1px,
        transparent 2px),

        linear-gradient(135deg,
        #180d2b,
        #35124e,
        #701c4e);

    background-size:
        80px 80px,
        120px 120px,
        100% 100%;

    overflow: hidden;
}


/* KARTU UTAMA */

.card {
    width: min(440px, 100%);

    padding: 28px 24px 24px;

    border-radius: 30px;

    background: rgba(20, 12, 35, .75);

    backdrop-filter: blur(18px);

    border: 1px solid rgba(255,255,255,.18);

    box-shadow:
        0 25px 80px rgba(0,0,0,.4);

    position: relative;
    overflow: hidden;
}


/* GLOW */

.glow {
    position: absolute;

    width: 180px;
    height: 180px;

    border-radius: 50%;

    background: #ff5ca8;

    filter: blur(70px);

    opacity: .25;

    right: -70px;
    top: -70px;
}


/* HEADER */

.top {
    text-align: center;
    position: relative;
}

.badge {
    display: inline-block;

    padding: 7px 12px;

    border-radius: 999px;

    background: rgba(255,255,255,.1);

    font-size: 11px;

    letter-spacing: .5px;
}

.envelope {
    font-size: 55px;

    margin-top: 10px;

    animation:
        floating 3s ease-in-out infinite;
}

@keyframes floating {

    50% {
        transform:
            translateY(-8px)
            rotate(3deg);
    }

}

h1 {
    font-size: 29px;

    line-height: 1.1;

    margin:
        18px 0 8px;
}

.subtitle {
    color: #d8cedf;

    line-height: 1.5;

    font-size: 14px;

    max-width: 350px;

    margin: auto;
}


/* AREA PESAN */

.screen {

    margin:
        24px 0 18px;

    background: #0c0814;

    border-radius: 22px;

    padding: 18px;

    border:
        1px solid
        rgba(255,255,255,.08);
}

.fake-status {

    display: flex;

    justify-content: space-between;

    color: #aaa0b0;

    font-size: 11px;

    margin-bottom: 14px;
}

.dot {

    width: 7px;
    height: 7px;

    border-radius: 50%;

    background: #70e08a;

    display: inline-block;

    margin-right: 5px;
}


/* BUBBLE */

.message {

    background: #241a2e;

    border-radius: 16px;

    padding: 15px;
}

.message b {
    font-size: 13px;
}

.message p {

    font-size: 13px;

    color: #ddd4e2;

    line-height: 1.5;

    margin:
        8px 0 0;
}


/* GELOMBANG AUDIO */

.wave {

    height: 52px;

    display: flex;

    align-items: center;

    justify-content: center;

    gap: 3px;

    margin:
        17px 0;
}

.bar {

    width: 4px;

    border-radius: 5px;

    background: #ff70b1;

    animation:
        wave 1s ease-in-out infinite;
}

.bar:nth-child(1) {
    height: 15px;
}

.bar:nth-child(2) {
    height: 27px;
    animation-delay: .08s;
}

.bar:nth-child(3) {
    height: 40px;
    animation-delay: .16s;
}

.bar:nth-child(4) {
    height: 24px;
    animation-delay: .24s;
}

.bar:nth-child(5) {
    height: 34px;
    animation-delay: .32s;
}

.bar:nth-child(6) {
    height: 18px;
    animation-delay: .40s;
}

.bar:nth-child(7) {
    height: 42px;
    animation-delay: .48s;
}

.bar:nth-child(8) {
    height: 25px;
    animation-delay: .56s;
}

.bar:nth-child(9) {
    height: 35px;
    animation-delay: .64s;
}

.bar:nth-child(10) {
    height: 16px;
    animation-delay: .72s;
}

.bar:nth-child(11) {
    height: 29px;
    animation-delay: .80s;
}

.bar:nth-child(12) {
    height: 20px;
    animation-delay: .88s;
}

@keyframes wave {

    0%,100% {
        transform: scaleY(.7);
        opacity: .55;
    }

    50% {
        transform: scaleY(1.08);
        opacity: 1;
    }

}

.time {

    font-size: 11px;

    color: #8d8494;

    text-align: center;
}


/* BUTTON */

button {

    width: 100%;

    border: none;

    border-radius: 17px;

    padding: 16px 18px;

    cursor: pointer;

    color: white;

    font-size: 16px;

    font-weight: bold;

    background:
        linear-gradient(
            135deg,
            #ff4f9a,
            #a84dff
        );

    box-shadow:
        0 12px 30px
        rgba(255,79,154,.25);

    transition: .2s;
}

button:hover {

    transform:
        translateY(-2px);

    box-shadow:
        0 16px 34px
        rgba(255,79,154,.35);
}

button:active {

    transform:
        translateY(1px);
}

button.playing {

    background:
        linear-gradient(
            135deg,
            #6f5cff,
            #ff4f9a
        );
}


/* HINT */

.hint {

    text-align: center;

    color: #9e95a4;

    font-size: 11px;

    margin:
        12px 0 0;
}


/* FOOTER */

.footer {

    text-align: center;

    margin-top: 18px;

    color: #8f8695;

    font-size: 10px;
}


/* CONFETTI */

.confetti {

    position: fixed;

    top: -20px;

    font-size: 18px;

    pointer-events: none;

    animation:
        fall 2.8s linear forwards;
}

@keyframes fall {

    to {

        transform:
            translateY(110vh)
            rotate(540deg);

        opacity: 0;
    }

}
</style>
</head>


<body>


<div class="card">

    <div class="glow"></div>


    <div class="top">

        <div class="badge">
            🔐 PESAN RAHASIA • LEVEL: AGAK NEKAT
        </div>


        <div class="envelope">
            💌
        </div>


        <h1>
            Hei, ada satu pesan<br>
            yang harus kamu dengar.
        </h1>


        <p class="subtitle">

            Tenang, ini bukan tagihan.
            Bukan juga surat tilang.

            Cuma seseorang yang sedang
            mencoba cara kreatif supaya
            pesannya tidak tenggelam
            di antara chat-chat lain. 😂

        </p>

    </div>



    <div class="screen">


        <div class="fake-status">

            <span>
                <span class="dot"></span>
                pesan ditemukan
            </span>

            <span>
                🎧 audio
            </span>

        </div>



        <div class="message">


            <b>
                📨 Pesan suara masuk
            </b>


            <p>

                “Klik tombolnya.
                Kalau setelah ini kamu masih
                belum balas, berarti sistem
                perlu di-upgrade.” 😭😂

            </p>



            <div
                class="wave"
                id="wave">
            </div>


            <div
                class="time"
                id="time">

                00:00 / 00:00

            </div>


        </div>


    </div>



    <button id="playBtn">

        ▶️ DENGARKAN PESANNYA

    </button>


    <p class="hint">

        Volume jangan terlalu kecil ya.
        Ini pesan resmi dari divisi
        orang yang menunggu balasan. 😌

    </p>


    <div class="footer">

        Dibuat dengan niat baik,
        sedikit keberanian,
        dan terlalu banyak ide. 😂

    </div>


</div>



<!--
=================================================
AUDIO
=================================================

Pastikan file audio bernama:

voice-note.mp3

dan berada satu folder dengan index.html.

-->

<audio
    id="audio"
    preload="metadata">

    <source
        src="voice-note.mp3"
        type="audio/mpeg">

</audio>



<script>


/* ===============================
   MEMBUAT GELOMBANG AUDIO
================================ */

const wave =
    document.getElementById("wave");


for (let i = 0; i < 12; i++) {

    const bar =
        document.createElement("span");

    bar.className = "bar";

    wave.appendChild(bar);

}



/* ===============================
   AUDIO
================================ */

const audio =
    document.getElementById("audio");

const button =
    document.getElementById("playBtn");

const time =
    document.getElementById("time");



/* FORMAT WAKTU */

function formatTime(seconds) {

    if (!isFinite(seconds))
        return "00:00";

    seconds =
        Math.floor(seconds);

    const minutes =
        Math.floor(seconds / 60);

    const secs =
        seconds % 60;

    return (

        String(minutes)
        .padStart(2,"0")

        +

        ":" +

        String(secs)
        .padStart(2,"0")

    );

}



/* SAAT AUDIO SIAP */

audio.addEventListener(
    "loadedmetadata",
    function() {

        time.textContent =
            "00:00 / " +
            formatTime(audio.duration);

    }
);



/* UPDATE WAKTU */

audio.addEventListener(
    "timeupdate",
    function() {

        time.textContent =

            formatTime(audio.currentTime)

            +

            " / "

            +

            formatTime(audio.duration);

    }
);



/* PLAY */

audio.addEventListener(
    "play",
    function() {

        button.classList.add(
            "playing"
        );

        button.textContent =
            "⏸️ JEDA SEBENTAR";

    }
);



/* PAUSE */

audio.addEventListener(
    "pause",
    function() {

        button.classList.remove(
            "playing"
        );

        button.textContent =
            "▶️ LANJUTKAN PESANNYA";

    }
);



/* SELESAI */

audio.addEventListener(
    "ended",
    function() {

        button.classList.remove(
            "playing"
        );

        button.textContent =
            "🔁 DENGARKAN LAGI";

        confetti();

    }
);



/* BUTTON */

button.addEventListener(
    "click",
    async function() {

        if (audio.paused) {

            try {

                await audio.play();

            }

            catch (error) {

                alert(
                    "Browser belum mengizinkan audio. " +
                    "Coba tekan tombol sekali lagi ya 😭"
                );

            }

        }

        else {

            audio.pause();

        }

    }
);



/* ===============================
   CONFETTI
================================ */

function confetti() {

    const emojis = [
        "💗",
        "😂",
        "✨",
        "💌",
        "🎉",
        "😭"
    ];


    for (
        let i = 0;
        i < 28;
        i++
    ) {

        const item =
            document.createElement("div");


        item.className =
            "confetti";


        item.textContent =
            emojis[
                Math.floor(
                    Math.random()
                    * emojis.length
                )
            ];


        item.style.left =
            Math.random() * 100 + "vw";


        item.style.animationDelay =
            Math.random() * .7 + "s";


        document.body.appendChild(item);


        setTimeout(
            function() {
                item.remove();
            },
            3600
        );

    }

}

</script>


</body>
</html>
