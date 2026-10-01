<!DOCTYPE html>
<html dir="rtl" lang="ar">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>علي ثامر</title>

<link rel="shortcut icon" href="https://i.ibb.co/Cp1yXqYr/IMG-0991.png"/>
<meta name="referrer" content="no-referrer"/>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">

<!-- Feather Icons -->
<script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>

<!-- Shaka Player -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/shaka-player/4.7.13/shaka-player.compiled.js"></script>

<!-- mpegts.js -->
<script src="https://cdn.jsdelivr.net/npm/mpegts.js@1.8.0/dist/mpegts.min.js"></script>

<style>
:root{
    --primary-color:#00FC3C;
    --live-color:#e62e2e;
    --menu-bg:#282828;
}

*{
    box-sizing:border-box;
}

html,body{
    margin:0;
    padding:0;
    width:100%;
    height:100%;
    overflow:hidden;
    background:#000;
    font-family:'Tajawal',sans-serif!important;
    -webkit-tap-highlight-color:transparent;
    user-select:none;
}

#player-container{
    position:fixed;
    inset:0;
    width:100%;
    height:100%;
    background:#000;
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
}

#video-wrapper{
    position:absolute;
    inset:0;
    width:100%;
    height:100%;
    background:#000;
}

#video{
    width:100%;
    height:100%;
    object-fit:contain;
    background:#000;
}

#loading-spinner{
    width:50px;
    height:50px;
    border:4px solid rgba(255,255,255,.2);
    border-top-color:var(--primary-color);
    border-radius:50%;
    animation:spin 1s linear infinite;
    position:absolute;
    left:50%;
    top:50%;
    transform:translate(-50%,-50%);
    z-index:100;
    pointer-events:none;
}

@keyframes spin{
    to{transform:translate(-50%,-50%) rotate(360deg)}
}

#error-overlay{
    position:absolute;
    z-index:100;
    inset:0;
    background:rgba(0,0,0,.92);
    color:#fff;
    display:none;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:20px;
}

#error-overlay i,
#error-overlay svg{
    width:48px;
    height:48px;
    margin-bottom:15px;
    color:var(--live-color);
}

#error-overlay h3{
    margin:5px 0 10px;
}

#error-overlay p{
    max-width:450px;
    line-height:1.6;
    color:#ccc;
    font-size:0.95em;
}

/* عناصر التحكم */
.controls-overlay{
    position:absolute;
    z-index:10;
    transition:opacity .3s ease, visibility .3s ease;
    opacity:0;
    visibility:hidden;
    pointer-events:none;
}

.controls-overlay.visible{
    opacity:1;
    visibility:visible;
    pointer-events:auto;
}

#bottom-controls-container{
    bottom:0;
    left:0;
    right:0;
    padding:5px 15px 12px;
    background:linear-gradient(to top, rgba(0,0,0,.9), transparent);
}

#center-controls{
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
}

.center-controls-cluster{
    display:flex;
    align-items:center;
    gap:35px;
    background:rgba(0,0,0,.4);
    padding:10px 24px;
    border-radius:50px;
    backdrop-filter:blur(5px);
}

.control-button,
.center-control-button{
    background:none;
    border:none;
    color:#fff;
    cursor:pointer;
    padding:0;
    outline:none;
    display:flex;
    align-items:center;
    justify-content:center;
    -webkit-tap-highlight-color:transparent;
    transition:all .2s ease;
}

.control-button:hover,
.center-control-button:hover{
    color:var(--primary-color);
    transform:scale(1.1);
}

.control-button i,
.control-button svg{
    width:22px;
    height:22px;
}

.center-control-button i,
.center-control-button svg{
    width:42px;
    height:42px;
}

.center-seek-button i,
.center-seek-button svg{
    width:30px;
    height:30px;
}

.progress-bar-container{
    width:100%;
    padding:8px 0;
}

.progress-bar{
    width:100%;
    height:5px;
    cursor:pointer;
    accent-color:var(--primary-color);
    direction:ltr;
    display:block;
}

.bottom-controls{
    display:flex;
    justify-content:space-between;
    align-items:center;
    width:100%;
}

.controls-left,
.controls-right{
    display:flex;
    align-items:center;
    gap:14px;
}

#time-display-container{
    color:#fff;
    font-size:.85em;
    font-weight:500;
    direction:ltr;
    min-width:90px;
    text-align:center;
}

/* نافذة الإعدادات */
#settings-popup{
    position:absolute;
    bottom:70px;
    left:20px;
    width:230px;
    background:var(--menu-bg);
    border-radius:8px;
    z-index:25;
    display:none;
    box-shadow:0 8px 24px rgba(0,0,0,.6);
    border:1px solid rgba(255,255,255,.1);
    overflow:hidden;
}

#settings-list{
    list-style:none;
    padding:5px;
    margin:0;
    max-height:200px;
    overflow-y:auto;
}

.settings-header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:8px 12px;
    border-bottom:1px solid rgba(255,255,255,.1);
    background:rgba(0,0,0,.2);
}

.settings-title{
    color:#eee;
    font-weight:700;
    font-size:0.9em;
}

.settings-close-btn{
    cursor:pointer;
    color:#aaa;
    display:flex;
    align-items:center;
}

.settings-close-btn:hover{
    color:#fff;
}

.menu-item{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:8px 10px;
    border-radius:4px;
    cursor:pointer;
    font-weight:500;
    font-size:0.9em;
    color:#fff;
}

.menu-item:hover{
    background:rgba(255,255,255,.1);
}

.menu-item.active{
    color:var(--primary-color);
    font-weight:700;
}

.menu-item svg{
    width:16px;
    height:16px;
}

@media(max-width:600px){
    .center-controls-cluster{
        gap:22px;
        padding:8px 16px;
    }
    .center-control-button i,
    .center-control-button svg{
        width:34px;
        height:34px;
    }
    #settings-popup{
        left:10px;
        bottom:65px;
        width:200px;
    }
}
</style>
</head>

<body>

<div id="player-container">

    <div id="loading-spinner"></div>

    <div id="error-overlay">
        <i data-feather="alert-triangle"></i>
        <h3 id="error-title">تعذر تشغيل الفيديو</h3>
        <p id="error-message">قد يكون الرابط غير متاح حالياً أو أن الخادم يمنع التشغيل عبر المتصفح.</p>
    </div>

    <div id="video-wrapper">
        <video
            id="video"
            playsinline
            webkit-playsinline
            preload="auto"
            poster="https://i.ibb.co/VpPrbF94/image.png">
        </video>
    </div>

    <!-- نافذة الإعدادات -->
    <div id="settings-popup">
        <div class="settings-header">
            <span class="settings-title">سرعة التشغيل</span>
            <span class="settings-close-btn" id="settings-close-btn">
                <i data-feather="x" style="width:16px; height:16px;"></i>
            </span>
        </div>
        <ul id="settings-list"></ul>
    </div>

    <!-- أزرار المنتصف -->
    <div id="center-controls" class="controls-overlay">
        <div class="center-controls-cluster">
            <button class="control-button center-seek-button" id="seek-backward-btn" title="تأخير 10 ثوانٍ">
                <i data-feather="rotate-ccw"></i>
            </button>

            <button class="center-control-button" id="play-pause-center-btn" title="تشغيل / إيقاف">
                <i data-feather="play"></i>
            </button>

            <button class="control-button center-seek-button" id="seek-forward-btn" title="تقديم 10 ثوانٍ">
                <i data-feather="rotate-cw"></i>
            </button>
        </div>
    </div>

    <!-- الشريط السفلي -->
    <div id="bottom-controls-container" class="controls-overlay">
        <div class="progress-bar-container">
            <input
                type="range"
                id="seek-bar"
                min="0"
                max="100"
                value="0"
                step="0.1"
                class="progress-bar">
        </div>

        <div class="bottom-controls">
            <div class="controls-left">
                <button class="control-button" id="fullscreen-btn" title="ملء الشاشة">
                    <i data-feather="maximize"></i>
                </button>

                <button id="settings-btn" class="control-button" title="السرعة والإعدادات">
                    <i data-feather="settings"></i>
                </button>

                <button class="control-button" id="expand-btn" title="تغيير مقاس العرض"></button>
            </div>

            <div class="controls-right">
                <div id="time-display-container">
                    <span id="time-display">00:00 / 00:00</span>
                </div>

                <button class="control-button" id="mute-btn" title="كتم / تشغيل الصوت">
                    <i data-feather="volume-2"></i>
                </button>

                <button class="control-button" id="play-pause-btn" title="تشغيل / إيقاف">
                    <i data-feather="play"></i>
                </button>
            </div>
        </div>
    </div>

</div>

<script>
document.addEventListener("DOMContentLoaded", function(){
    feather.replace();

    const STREAM_URL = "https://b2.shahidtv.net/files/Movies/hollywood/Spider-Man-Brand-New-Day-2026/Spider-Man-Brand-New-Day-2026-hdts-720p.mp4";

    const video = document.getElementById("video");
    const container = document.getElementById("player-container");
    const loading = document.getElementById("loading-spinner");
    const errorOverlay = document.getElementById("error-overlay");
    const errorTitle = document.getElementById("error-title");
    const errorMessage = document.getElementById("error-message");

    const centerControls = document.getElementById("center-controls");
    const bottomControls = document.getElementById("bottom-controls-container");
    const playBtn = document.getElementById("play-pause-btn");
    const centerPlayBtn = document.getElementById("play-pause-center-btn");
    const muteBtn = document.getElementById("mute-btn");
    const fullscreenBtn = document.getElementById("fullscreen-btn");
    const expandBtn = document.getElementById("expand-btn");
    const settingsBtn = document.getElementById("settings-btn");
    const settingsPopup = document.getElementById("settings-popup");
    const settingsList = document.getElementById("settings-list");
    const seekBar = document.getElementById("seek-bar");
    const timeDisplay = document.getElementById("time-display");

    let isSeeking = false;
    let mpegPlayer = null;
    let shakaPlayer = null;

    /* إعداد زر مقاس الفيديو */
    expandBtn.innerHTML = `
    <svg fill="currentColor" width="22" height="22" viewBox="0 0 100 100">
        <path d="M22 20h14c1 0 2-1 2-2s-1-2-2-2H19c-1 0-2 1-2 2v17c0 1 1 2 2 2s2-1 2-2V25l16 16c1 1 2 1 3 0s1-2 0-3L22 20z"/>
        <path d="M83 16H66c-1 0-2 1-2 2s1 2 2 2h13L62 37c-1 1-1 2 0 3s2 1 3 0l16-16v12c0 1 1 2 2 2s2-1 2-2V18c0-1-1-2-2-2z"/>
        <path d="M37 61L20 77V66c0-1-1-2-2-2s-2 1-2 2v17c0 1 1 2 2 2h17c1 0 2-1 2-2s-1-2-2-2H23l17-16c1-1 1-2 0-3s-2-1-3-1z"/>
        <path d="M83 64c-1 0-2 1-2 2v12L64 61c-1-1-2-1-3 0s-1 2 0 3l17 17H66c-1 0-2 1-2 2s1 2 2 2h17c1 0 2-1 2-2V66c0-1-1-2-2-2z"/>
    </svg>`;

    let expandIndex = 0;
    const expandModes = ["contain", "cover", "fill"];

    /* تشغيل / إيقاف */
    function updatePlayIcon(){
        const icon = video.paused ? "play" : "pause";
        playBtn.innerHTML = `<i data-feather="${icon}"></i>`;
        centerPlayBtn.innerHTML = `<i data-feather="${icon}"></i>`;
        feather.replace();
    }

    function togglePlay(){
        if(video.paused){
            video.play().catch(() => {});
        } else {
            video.pause();
        }
    }

    /* الصوت */
    function updateMuteIcon(){
        let icon = "volume-2";
        if(video.muted || video.volume === 0){
            icon = "volume-x";
        } else if(video.volume < 0.5){
            icon = "volume-1";
        }
        muteBtn.innerHTML = `<i data-feather="${icon}"></i>`;
        feather.replace();
    }

    /* الوقت */
    function formatTime(seconds){
        if(!isFinite(seconds) || isNaN(seconds)) return "00:00";
        seconds = Math.max(0, Math.floor(seconds));
        const hours = Math.floor(seconds / 3600);
        const minutes = Math.floor((seconds % 3600) / 60);
        const secs = seconds % 60;

        if(hours > 0){
            return `${String(hours).padStart(2,"0")}:${String(minutes).padStart(2,"0")}:${String(secs).padStart(2,"0")}`;
        }
        return `${String(minutes).padStart(2,"0")}:${String(secs).padStart(2,"0")}`;
    }

    function updateTimeDisplay(){
        timeDisplay.textContent = `${formatTime(video.currentTime)} / ${formatTime(video.duration)}`;
    }

    /* شريط التقدم */
    function updateDuration(){
        if(isFinite(video.duration) && video.duration > 0){
            seekBar.max = video.duration;
        }
        updateTimeDisplay();
    }

    video.addEventListener("loadedmetadata", updateDuration);
    video.addEventListener("durationchange", updateDuration);

    video.addEventListener("timeupdate", function(){
        if(isFinite(video.duration) && !isSeeking){
            seekBar.value = video.currentTime;
        }
        updateTimeDisplay();
    });

    seekBar.addEventListener("mousedown", () => { isSeeking = true; });
    seekBar.addEventListener("touchstart", () => { isSeeking = true; }, {passive:true});

    seekBar.addEventListener("input", function(){
        if(isFinite(video.duration)){
            timeDisplay.textContent = `${formatTime(Number(seekBar.value))} / ${formatTime(video.duration)}`;
        }
    });

    function applySeek(){
        if(isFinite(video.duration)){
            video.currentTime = Number(seekBar.value);
        }
        isSeeking = false;
    }

    seekBar.addEventListener("mouseup", applySeek);
    seekBar.addEventListener("touchend", applySeek);

    /* الشاشة الكاملة */
    async function toggleFullscreen(){
        try{
            if(!document.fullscreenElement){
                if(container.requestFullscreen){
                    await container.requestFullscreen();
                } else if(video.webkitEnterFullscreen){
                    video.webkitEnterFullscreen();
                }
            } else {
                if(document.exitFullscreen){
                    await document.exitFullscreen();
                }
            }
        }catch(e){
            console.error("Fullscreen error:", e);
        }
    }

    function updateFullscreenIcon(){
        fullscreenBtn.innerHTML = `<i data-feather="${document.fullscreenElement ? "minimize" : "maximize"}"></i>`;
        feather.replace();
    }

    document.addEventListener("fullscreenchange", updateFullscreenIcon);

    /* إظهار وإخفاء أدوات التحكم */
    let controlTimer = null;
    function showControls(){
        centerControls.classList.add("visible");
        bottomControls.classList.add("visible");
        clearTimeout(controlTimer);

        if(!video.paused){
            controlTimer = setTimeout(function(){
                if(settingsPopup.style.display !== "block"){
                    centerControls.classList.remove("visible");
                    bottomControls.classList.remove("visible");
                }
            }, 3500);
        }
    }

    function hideControls(){
        if(settingsPopup.style.display === "block") return;
        centerControls.classList.remove("visible");
        bottomControls.classList.remove("visible");
    }

    container.addEventListener("mousemove", showControls);
    container.addEventListener("click", function(e){
        if(e.target === container || e.target === video){
            if(centerControls.classList.contains("visible")){
                hideControls();
            } else {
                showControls();
            }
        }
    });

    /* قائمة السرعة الإعدادات */
    const playbackSpeeds = [0.5, 0.75, 1, 1.25, 1.5, 2];
    function renderSettings(){
        settingsList.innerHTML = "";
        playbackSpeeds.forEach(speed => {
            const li = document.createElement("li");
            li.className = `menu-item ${video.playbackRate === speed ? "active" : ""}`;
            li.innerHTML = `<span>${speed === 1 ? "عادي (1x)" : speed + "x"}</span>`;
            if(video.playbackRate === speed){
                li.innerHTML += `<i data-feather="check"></i>`;
            }
            li.onclick = () => {
                video.playbackRate = speed;
                renderSettings();
                settingsPopup.style.display = "none";
            };
            settingsList.appendChild(li);
        });
        feather.replace();
    }

    settingsBtn.onclick = function(e){
        e.stopPropagation();
        if(settingsPopup.style.display === "block"){
            settingsPopup.style.display = "none";
        } else {
            renderSettings();
            settingsPopup.style.display = "block";
        }
    };

    document.getElementById("settings-close-btn").onclick = function(){
        settingsPopup.style.display = "none";
    };

    /* مشغل MPEG-TS */
    function startTS(){
        if(typeof mpegts === "undefined" || !mpegts.isSupported()){
            showError("المتصفح لا يدعم بث TS", "يحتاج هذا البث إلى متصفح يدعم تقنية Media Source Extensions.");
            return;
        }

        try{
            mpegPlayer = mpegts.createPlayer({
                type: "mpegts",
                url: STREAM_URL,
                isLive: true,
                cors: true
            },{
                enableWorker: true,
                lazyLoad: false,
                liveBufferLatencyChasing: true
            });

            mpegPlayer.attachMediaElement(video);
            mpegPlayer.load();
            mpegPlayer.play().catch(() => { video.muted = true; });

            mpegPlayer.on(mpegts.Events.ERROR, function(type, detail, info){
                console.error("MPEGTS ERROR:", type, detail, info);
                showError("فشل تشغيل البث", "تعذر الاتصال بمصدر بث TS المباشر.");
            });
        }catch(err){
            showError("خطأ في تشغيل البث", err.message || "حدث خطأ غير معروف.");
        }
    }

    /* تشغيل الفيديو العام */
    async function startStream(){
        loading.style.display = "block";
        errorOverlay.style.display = "none";

        const url = STREAM_URL.toLowerCase();

        // 1. ملفات MP4
        if(url.includes(".mp4")){
            video.src = STREAM_URL;
            video.load();
            video.play().catch(() => {});
            return;
        }

        // 2. ملفات TS
        if(url.includes(".ts")){
            startTS();
            return;
        }

        // 3. ملفات HLS المباشرة لأجهزة iOS / Safari
        if(url.includes(".m3u8") && video.canPlayType("application/vnd.apple.mpegurl")){
            video.src = STREAM_URL;
            video.load();
            video.play().catch(() => {});
            return;
        }

        // 4. تشغيل Shaka Player (DASH / HLS على باقي المتصفحات)
        try{
            if(!window.shaka) throw new Error("مكتبة Shaka Player غير محملة");

            shaka.polyfill.installAll();
            if(!shaka.Player.isBrowserSupported()){
                throw new Error("المتصفح الحالي لا يدعم تقنيات البث الحديثة");
            }

            shakaPlayer = new shaka.Player(video);
            shakaPlayer.configure({
                streaming: { rebufferingGoal: 2, bufferingGoal: 10 }
            });

            await shakaPlayer.load(STREAM_URL);
            video.play().catch(() => {});
        }catch(error){
            console.error("Stream Error:", error);
            showError("تعذر تشغيل الفيديو", error.message || "يرجى التحقق من اتصال الإنترنت أو صلاحية الرابط.");
        }
    }

    /* رسائل الخطأ */
    function showError(title, message){
        loading.style.display = "none";
        errorTitle.textContent = title;
        errorMessage.textContent = message;
        errorOverlay.style.display = "flex";
        feather.replace();
    }

    /* الاستماع للأحداث */
    playBtn.onclick = (e) => { e.stopPropagation(); togglePlay(); };
    centerPlayBtn.onclick = (e) => { e.stopPropagation(); togglePlay(); };
    muteBtn.onclick = (e) => { e.stopPropagation(); video.muted = !video.muted; updateMuteIcon(); };
    fullscreenBtn.onclick = (e) => { e.stopPropagation(); toggleFullscreen(); };

    expandBtn.onclick = function(e){
        e.stopPropagation();
        expandIndex = (expandIndex + 1) % expandModes.length;
        video.style.objectFit = expandModes[expandIndex];
    };

    video.addEventListener("play", () => { updatePlayIcon(); showControls(); });
    video.addEventListener("pause", () => { updatePlayIcon(); showControls(); });
    video.addEventListener("volumechange", updateMuteIcon);

    video.addEventListener("waiting", () => { loading.style.display = "block"; });
    video.addEventListener("playing", () => { loading.style.display = "none"; });
    video.addEventListener("canplay", () => { loading.style.display = "none"; updatePlayIcon(); });

    video.addEventListener("error", function(){
        loading.style.display = "none";
        if(video.error){
            showError("خطأ في تشغيل الفيديو", "تعذر تحميل ملف الوسائط من الخادم.");
        }
    });

    /* تقديم وتأخير 10 ثوانٍ */
    document.getElementById("seek-backward-btn").onclick = function(e){
        e.stopPropagation();
        if(isFinite(video.currentTime)){
            video.currentTime = Math.max(0, video.currentTime - 10);
            showControls();
        }
    };

    document.getElementById("seek-forward-btn").onclick = function(e){
        e.stopPropagation();
        if(isFinite(video.currentTime)){
            video.currentTime = Math.min(video.duration || Infinity, video.currentTime + 10);
            showControls();
        }
    };

    // البدء
    updateMuteIcon();
    updatePlayIcon();
    startStream();
});
</script>

</body>
</html>
