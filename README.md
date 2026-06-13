index.html<!DOCTYPE html>
<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>የህግ ባለሞያ ለኢትዮጵያ - ማዋቀሪያ ፓነል ያለው</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0f172a;
            line-height: 1.5;
        }
        /* header & main content (same as before) */
        .header { background: linear-gradient(135deg, #0a2b3e 0%, #1e4a6e 100%); color: white; padding: 1rem 2rem; position: sticky; top: 0; z-index: 1000; }
        .header-container { max-width: 1400px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem; }
        .logo-area { display: flex; align-items: center; gap: 1rem; }
        .profile-photo { width: 55px; height: 55px; background: #f59e0b; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; overflow: hidden; border: 2px solid #ffd966; }
        .profile-photo img { width: 100%; height: 100%; object-fit: cover; }
        .site-title h1 { font-size: 1.4rem; }
        .lang-switch { display: flex; gap: 0.5rem; background: rgba(255,255,255,0.2); padding: 0.4rem 0.8rem; border-radius: 40px; }
        .lang-btn { background: none; border: none; color: white; font-weight: 600; cursor: pointer; padding: 0.3rem 0.8rem; border-radius: 30px; }
        .lang-btn.active { background: #f59e0b; color: #0f172a; }
        .container { max-width: 1400px; margin: 2rem auto; padding: 0 2rem; }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.8rem; margin-bottom: 2rem; }
        .card { background: white; border-radius: 24px; padding: 1.5rem; box-shadow: 0 4px 12px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; transition: 0.2s; }
        .btn { background: #1e4a6e; color: white; border: none; padding: 0.7rem 1.3rem; border-radius: 40px; font-weight: 500; cursor: pointer; display: inline-flex; align-items: center; gap: 0.5rem; }
        .btn-warning { background: #f59e0b; color: #0f172a; }
        .payment-options { background: #fef9e3; padding: 1rem; border-radius: 16px; margin: 1rem 0; }
        .social-links { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 1rem; }
        .social-link { background: #eef2ff; padding: 0.5rem 1rem; border-radius: 40px; text-decoration: none; color: #0f172a; font-weight: 500; }
        .section { background: white; border-radius: 24px; padding: 1.8rem; margin-bottom: 2rem; border: 1px solid #e2e8f0; }
        .modal { display: none; position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.7); justify-content: center; align-items: center; z-index: 2000; }
        .modal-content { background: white; padding: 2rem; border-radius: 28px; max-width: 600px; width: 90%; max-height: 80vh; overflow-y: auto; }
        footer { text-align: center; padding: 2rem; background: #0f172a; color: #94a3b8; margin-top: 2rem; }
        
        /* Settings Panel (cog wheel) */
        .settings-cog {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #1e4a6e;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 1500;
            transition: 0.2s;
            color: white;
            font-size: 1.8rem;
        }
        .settings-cog:hover { transform: scale(1.05); background: #0f3b55; }
        .settings-panel {
            position: fixed;
            top: 0;
            right: -450px;
            width: 450px;
            height: 100%;
            background: white;
            box-shadow: -2px 0 20px rgba(0,0,0,0.2);
            z-index: 1600;
            transition: right 0.3s ease;
            display: flex;
            flex-direction: column;
            overflow-y: auto;
            font-family: monospace;
        }
        .settings-panel.open { right: 0; }
        .settings-header {
            background: #0a2b3e;
            color: white;
            padding: 1.2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
        }
        .settings-body { padding: 1.5rem; flex:1; }
        .setting-group { margin-bottom: 1.5rem; border-bottom: 1px solid #e2e8f0; padding-bottom: 1rem; }
        .setting-group label { display: block; font-weight: 600; margin-bottom: 0.5rem; }
        .setting-group input, .setting-group textarea, .setting-group select { width: 100%; padding: 0.5rem; border-radius: 8px; border: 1px solid #cbd5e1; }
        .setting-group textarea { height: 80px; }
        .array-item { background: #f1f5f9; padding: 0.5rem; margin-bottom: 0.5rem; border-radius: 8px; display: flex; gap: 0.5rem; align-items: center; }
        .array-item input { flex:1; }
        .btn-small { background: #e2e8f0; border: none; padding: 0.2rem 0.6rem; border-radius: 20px; cursor: pointer; }
        .btn-danger { background: #ef4444; color: white; }
        .btn-save { background: #10b981; color: white; width: 100%; margin-top: 1rem; }
        .overlay { position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.4); z-index: 1550; display: none; }
        .overlay.show { display: block; }
    </style>
</head>
<body>

<div class="header">
    <div class="header-container">
        <div class="logo-area">
            <div class="profile-photo" id="profilePhotoBtn">
                <img id="profileImg" src="" alt="Profile" style="display:none; width:100%; height:100%; object-fit:cover;">
                <i id="defaultIcon" class="fas fa-user-graduate"></i>
            </div>
            <div class="site-title">
                <h1 id="siteTitle"></h1>
                <p id="siteSubtitle"></p>
            </div>
        </div>
        <div class="lang-switch">
            <button class="lang-btn active" data-lang="am">አማርኛ</button>
            <button class="lang-btn" data-lang="en">English</button>
        </div>
    </div>
</div>

<div class="container">
    <div class="services-grid">
        <div class="card"><i class="fas fa-gavel"></i><h3 data-key="legalConsultTitle"></h3><p data-key="legalConsultDesc"></p><button class="btn consultBtn"><i class="fas fa-comments"></i> <span data-key="consultBtnText"></span></button></div>
        <div class="card"><i class="fas fa-video"></i><h3 data-key="mediaLawTitle"></h3><p data-key="mediaLawDesc"></p><button class="btn btn-outline" id="viewMediaBtn"><i class="fas fa-play-circle"></i> <span data-key="viewMedia"></span></button></div>
        <div class="card"><i class="fas fa-chalkboard-user"></i><h3 data-key="trainingTitle"></h3><p data-key="trainingDesc"></p><button class="btn" id="trainingsBtn"><i class="fas fa-certificate"></i> <span data-key="trainingsBtn"></span></button></div>
        <div class="card"><i class="fas fa-share-alt"></i><h3 data-key="socialShareTitle"></h3><p data-key="socialShareDesc"></p><div id="socialLinks" class="social-links"></div></div>
    </div>
    <div class="section" id="mediaLibrary"><h2><i class="fas fa-database"></i> <span data-key="libraryTitle"></span></h2><div id="mediaGrid" style="display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:1rem;"></div></div>
    <div class="section"><h2><i class="fas fa-balance-scale"></i> <span data-key="rulingTitle"></span></h2><p data-key="rulingDesc"></p><div class="payment-options" id="paymentOptions"></div><button class="btn btn-warning" id="purchaseRulingBtn"><i class="fas fa-key"></i> <span data-key="purchaseAccess"></span></button><div id="rulingSearchArea" style="display:none;"><select id="lawFilter"><option value="all">ሁሉም</option></select><input type="text" id="searchRuling" placeholder="ፈልግ..."><button id="searchRulingBtn">ፈልግ</button><div id="rulingResults"></div></div></div>
    <div class="section"><h2><i class="fas fa-user-plus"></i> <span data-key="joinTitle"></span></h2><p data-key="joinDesc"></p><div id="joinLinks" class="social-links"></div></div>
</div>
<footer><p>© 2025 የህግ ባለሞያ ለኢትዮጵያ</p></footer>

<!-- Settings Cog & Panel -->
<div class="settings-cog" id="settingsCog"><i class="fas fa-cog"></i></div>
<div class="overlay" id="settingsOverlay"></div>
<div class="settings-panel" id="settingsPanel">
    <div class="settings-header">
        <span><i class="fas fa-sliders-h"></i> የዌብሳይት ማዋቀሪያ (Settings)</span>
        <button id="closeSettingsBtn" style="background:none; border:none; color:white; font-size:1.5rem;">&times;</button>
    </div>
    <div class="settings-body">
        <div class="setting-group">
            <label>የገጽ ርዕስ (አማርኛ)</label>
            <input type="text" id="setTitleAm" placeholder="የህግ ባለሞያ ለኢትዮጵያ">
        </div>
        <div class="setting-group">
            <label>የገጽ ርዕስ (English)</label>
            <input type="text" id="setTitleEn" placeholder="Lawyers for Ethiopia">
        </div>
        <div class="setting-group">
            <label>የፕሮፋይል ፎቶ URL (ሙሉ አድራሻ ወይም ፋይል ስም)</label>
            <input type="text" id="setProfilePic" placeholder="e.g., profile.jpg or https://...">
        </div>
        <div class="setting-group">
            <label>የኢትዮጵያ ንግድ ባንክ ቁጥር</label>
            <input type="text" id="setBank" placeholder="1000417819437">
        </div>
        <div class="setting-group">
            <label>ሲቢኢ ብር / ቴሌ ብር ቁጥር</label>
            <input type="text" id="setMobileMoney" placeholder="0951727278">
        </div>
        <div class="setting-group">
            <label>ቲክቶክ አገናኝ</label>
            <input type="text" id="setTiktok" placeholder="https://www.tiktok.com/@...">
        </div>
        <div class="setting-group">
            <label>ፌስቡክ አገናኝ</label>
            <input type="text" id="setFacebook" placeholder="https://www.facebook.com/...">
        </div>
        <div class="setting-group">
            <label>ቴሌግራም አገናኝ</label>
            <input type="text" id="setTelegram" placeholder="https://t.me/...">
        </div>
        <div class="setting-group">
            <label>የሰበር ውሳኔዎች ዋጋ (ብር)</label>
            <input type="number" id="setRulingPrice" value="500">
        </div>
        <div class="setting-group">
            <label>የሚዲያ ዝርዝር (JSON ቅርጸት - አርትዕ ማድረግ ለሚችሉ ተጠቃሚዎች)</label>
            <textarea id="setMediaItems" rows="5" placeholder='[{"type":"document","title":"የወንጀል ህግ","url":"#","desc":"..."}]'></textarea>
        </div>
        <div class="setting-group">
            <label>የሰበር ውሳኔዎች (JSON)</label>
            <textarea id="setRulings" rows="5" placeholder='[{"category":"የወንጀል ህግ","caseNumber":"ሰበር 101/2012","summary":"..."}]'></textarea>
        </div>
        <button class="btn-save" id="saveSettingsBtn"><i class="fas fa-save"></i> ማዋቀሪያዎችን አስቀምጥ</button>
        <button class="btn" id="exportSettingsBtn" style="margin-top:0.5rem; background:#6c757d;"><i class="fas fa-download"></i> ማዋቀሪያ ኮድ አውጣ</button>
        <p style="font-size:0.8rem; margin-top:1rem;">ማስታወሻ: ለውጦች በአሁኑ ጊዜ በእርስዎ ብራውዘር ውስጥ ይቀመጣሉ። ወደ GitHub ለመላክ ከላይ "ኮድ አውጣ" በመጫን የተሻሻለውን CONFIG ማግኘት ይችላሉ።</p>
    </div>
</div>

<script>
    // ---------- DEFAULT CONFIG (same as before) ----------
    const defaultConfig = {
        siteTitle_am: "የህግ ባለሞያ ለኢትዮጵያ",
        siteTitle_en: "Lawyers for Ethiopia",
        siteSubtitle_am: "የህግ እውቀት ለሁሉም",
        siteSubtitle_en: "Legal Knowledge for Everyone",
        profileImageUrl: "",
        paymentBank: "1000417819437",
        paymentMobile: "0951727278",
        social: { tiktok: "https://www.tiktok.com/@lawyersforethiopia", facebook: "https://www.facebook.com/Lawyeryonatandawit", telegram: "https://t.me/LAWYERSFORETHIOPIA" },
        rulingPrice: 500,
        mediaItems: [
            { id:1, type:"document", title:"የወንጀል ህግ ቁ.1", url:"#", desc:"የኢትዮጵያ ወንጀል ህግ" },
            { id:2, type:"video", title:"የውል ህግ ትምህርት", url:"https://www.youtube.com/embed/dQw4w9WgXcQ", desc:"ቪዲዮ" }
        ],
        rulings: [
            { id:1, category:"የወንጀል ህግ", caseNumber:"ሰበር 101/2012", summary:"የህይወት እስራት", fileRef:"ሰ/ሰ/101" }
        ]
    };
    
    // Load from localStorage or default
    let config = JSON.parse(localStorage.getItem("lawyerSiteConfig")) || defaultConfig;
    
    // Helper to update UI based on config
    function applyConfigToUI() {
        document.getElementById("siteTitle").innerText = currentLang === "am" ? config.siteTitle_am : config.siteTitle_en;
        document.getElementById("siteSubtitle").innerText = currentLang === "am" ? config.siteSubtitle_am : config.siteSubtitle_en;
        // profile picture
        const profileImg = document.getElementById("profileImg");
        const defaultIcon = document.getElementById("defaultIcon");
        if(config.profileImageUrl && config.profileImageUrl.trim() !== "") {
            profileImg.src = config.profileImageUrl;
            profileImg.style.display = "block";
            defaultIcon.style.display = "none";
        } else {
            profileImg.style.display = "none";
            defaultIcon.style.display = "flex";
        }
        // payment options
        const paymentDiv = document.getElementById("paymentOptions");
        if(paymentDiv) {
            paymentDiv.innerHTML = `<i class="fas fa-money-bill-wave"></i> <strong>የክፍያ አማራጮች:</strong><br>
            🏦 የኢትዮጵያ ንግድ ባንክ: <strong>${config.paymentBank}</strong><br>
            📱 ሲቢኢ ብር/ቴሌ ብር: <strong>${config.paymentMobile}</strong>`;
        }
        // social links
        function buildSocial(containerId) {
            const container = document.getElementById(containerId);
            if(container) container.innerHTML = `
                <a href="${config.social.tiktok}" target="_blank" class="social-link"><i class="fab fa-tiktok"></i> TikTok</a>
                <a href="${config.social.facebook}" target="_blank" class="social-link"><i class="fab fa-facebook"></i> Facebook</a>
                <a href="${config.social.telegram}" target="_blank" class="social-link"><i class="fab fa-telegram"></i> Telegram</a>
            `;
        }
        buildSocial("socialLinks");
        buildSocial("joinLinks");
        // media library render
        renderMedia(config.mediaItems);
        // rulings price text
        document.querySelectorAll("[data-key='purchaseAccess']").forEach(el => el.innerText = (currentLang === "am" ? `የውሳኔ ፍለጋ መብት ግዙ (${config.rulingPrice} ብር)` : `Purchase Access (${config.rulingPrice} ETB)`));
        document.querySelectorAll("[data-key='rulingDesc']").forEach(el => el.innerText = currentLang === "am" ? `ከ${config.rulingPrice} ብር ክፍያ በኋላ ውሳኔዎችን ፈልግ` : `After ${config.rulingPrice} ETB payment, search rulings`);
        // store rulings for search
        window.currentRulings = config.rulings;
    }
    
    function renderMedia(mediaArray) {
        const grid = document.getElementById("mediaGrid");
        if(!grid) return;
        grid.innerHTML = "";
        mediaArray.forEach(item => {
            const card = document.createElement("div");
            card.style.background = "#fff";
            card.style.padding = "1rem";
            card.style.borderRadius = "16px";
            card.style.border = "1px solid #e2e8f0";
            let inner = "";
            if(item.type === "document") inner = `<i class="fas fa-file-pdf"></i><h4>${item.title}</h4><p>${item.desc}</p><a href="${item.url}" target="_blank">ክፈት</a>`;
            else if(item.type === "video") inner = `<i class="fas fa-video"></i><h4>${item.title}</h4><iframe width="100%" height="150" src="${item.url}" frameborder="0"></iframe>`;
            else if(item.type === "image") inner = `<img src="${item.url}" width="100%"><h4>${item.title}</h4>`;
            else if(item.type === "audio") inner = `<i class="fas fa-headphones"></i><h4>${item.title}</h4><audio controls src="${item.url}" style="width:100%"></audio>`;
            card.innerHTML = inner;
            grid.appendChild(card);
        });
    }
    
    // Language handling
    let currentLang = "am";
    const translations = {
        am: { legalConsultTitle:"የህግ ማማከር", legalConsultDesc:"ከባለሙያዎች የህግ ምክር ያግኙ", consultBtnText:"አማክሩኝ", mediaLawTitle:"የህግ ትምህርቶች", mediaLawDesc:"በቪዲዮ፣ ድምጽ፣ ምስል", viewMedia:"ይዘቶችን ይመልከቱ", trainingTitle:"ቋሚ ስልጠናዎች", trainingDesc:"የኢትዮጵያ ህጎች", trainingsBtn:"ስልጠናዎች", socialShareTitle:"ማህበራዊ ሚዲያ", socialShareDesc:"ይቀላቀሉ", libraryTitle:"የህግ ማውጫ", rulingTitle:"የሰበር ውሳኔዎች", joinTitle:"መቀላቀል", joinDesc:"ቅድመ ሁኔታዎችን ይመልከቱ" },
        en: { legalConsultTitle:"Legal Consultation", legalConsultDesc:"Get legal advice", consultBtnText:"Consult", mediaLawTitle:"Law Tutorials", mediaLawDesc:"Video/Audio/Image", viewMedia:"Browse Media", trainingTitle:"Trainings", trainingDesc:"Ethiopian laws", trainingsBtn:"Trainings", socialShareTitle:"Social Media", socialShareDesc:"Join us", libraryTitle:"Legal Library", rulingTitle:"Cassation Decisions", joinTitle:"Join Us", joinDesc:"Check prerequisites" }
    };
    function updateLang() {
        const t = translations[currentLang];
        for(let key in t) {
            let el = document.querySelector(`[data-key="${key}"]`);
            if(el) el.innerText = t[key];
        }
        applyConfigToUI(); // refresh dynamic texts
    }
    document.querySelectorAll(".lang-btn").forEach(btn => {
        btn.addEventListener("click", () => {
            currentLang = btn.getAttribute("data-lang");
            document.querySelectorAll(".lang-btn").forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            updateLang();
        });
    });
    
    // Settings panel functionality
    const cog = document.getElementById("settingsCog");
    const panel = document.getElementById("settingsPanel");
    const overlay = document.getElementById("settingsOverlay");
    const closeBtn = document.getElementById("closeSettingsBtn");
    function openSettings() {
        // populate fields from current config
        document.getElementById("setTitleAm").value = config.siteTitle_am;
        document.getElementById("setTitleEn").value = config.siteTitle_en;
        document.getElementById("setProfilePic").value = config.profileImageUrl || "";
        document.getElementById("setBank").value = config.paymentBank;
        document.getElementById("setMobileMoney").value = config.paymentMobile;
        document.getElementById("setTiktok").value = config.social.tiktok;
        document.getElementById("setFacebook").value = config.social.facebook;
        document.getElementById("setTelegram").value = config.social.telegram;
        document.getElementById("setRulingPrice").value = config.rulingPrice;
        document.getElementById("setMediaItems").value = JSON.stringify(config.mediaItems, null, 2);
        document.getElementById("setRulings").value = JSON.stringify(config.rulings, null, 2);
        panel.classList.add("open");
        overlay.classList.add("show");
    }
    function closeSettings() {
        panel.classList.remove("open");
        overlay.classList.remove("show");
    }
    cog.addEventListener("click", openSettings);
    closeBtn.addEventListener("click", closeSettings);
    overlay.addEventListener("click", closeSettings);
    
    document.getElementById("saveSettingsBtn").addEventListener("click", () => {
        // gather values
        config.siteTitle_am = document.getElementById("setTitleAm").value;
        config.siteTitle_en = document.getElementById("setTitleEn").value;
        config.profileImageUrl = document.getElementById("setProfilePic").value;
        config.paymentBank = document.getElementById("setBank").value;
        config.paymentMobile = document.getElementById("setMobileMoney").value;
        config.social.tiktok = document.getElementById("setTiktok").value;
        config.social.facebook = document.getElementById("setFacebook").value;
        config.social.telegram = document.getElementById("setTelegram").value;
        config.rulingPrice = parseInt(document.getElementById("setRulingPrice").value) || 500;
        try {
            config.mediaItems = JSON.parse(document.getElementById("setMediaItems").value);
            config.rulings = JSON.parse(document.getElementById("setRulings").value);
        } catch(e) { alert("JSON ቅርጸት ስህተት ነው"); return; }
        localStorage.setItem("lawyerSiteConfig", JSON.stringify(config));
        applyConfigToUI();
        updateLang();
        closeSettings();
        alert("ማዋቀሪያዎች ተቀምጠዋል! ገጹ ታድሷል።");
    });
    
    document.getElementById("exportSettingsBtn").addEventListener("click", () => {
        const exportCode = `// ይህንን CONFIG ወደ ዌብሳይትዎ ኮድ ይቅዱ
const CONFIG = ${JSON.stringify(config, null, 2)};`;
        const blob = new Blob([exportCode], {type: "text/javascript"});
        const url = URL.createObjectURL(blob);
        const a = document.createElement("a");
        a.href = url;
        a.download = "website_config.js";
        a.click();
        URL.revokeObjectURL(url);
        alert("ማዋቀሪያዎች በፋይል ተወርደዋል። ይህን ፋይል ወደ GitHub በማስገባት ማዘመን ይችላሉ።");
    });
    
    // Consultation modal (simple)
    const consultModal = document.createElement("div"); consultModal.className = "modal"; consultModal.id = "consultModal";
    consultModal.innerHTML = `<div class="modal-content"><h3>የህግ ማማከር</h3><textarea id="consultQ" rows="4" placeholder="ጥያቄዎን ይጻፉ" style="width:100%"></textarea><button id="sendConsult" class="btn">ላክ</button><button id="closeConsult" class="btn-outline">ዝጋ</button></div>`;
    document.body.appendChild(consultModal);
    document.querySelectorAll(".consultBtn").forEach(btn => btn.addEventListener("click", () => consultModal.style.display = "flex"));
    document.getElementById("closeConsult")?.addEventListener("click", () => consultModal.style.display = "none");
    document.getElementById("sendConsult")?.addEventListener("click", () => { alert("ጥያቄ ተልኳል። መልስ በቅርቡ ይላካል"); consultModal.style.display = "none"; });
    document.getElementById("trainingsBtn")?.addEventListener("click", () => alert("ስልጠናዎች በቅርቡ ይጀምራሉ።"));
    document.getElementById("viewMediaBtn")?.addEventListener("click", () => document.getElementById("mediaLibrary").scrollIntoView({behavior:"smooth"}));
    
    // Rulings search logic
    let rulingsAccess = false;
    document.getElementById("purchaseRulingBtn")?.addEventListener("click", () => {
        if(confirm(`እባክዎ ${config.rulingPrice} ብር ከላይ በተጠቀሰው ቁጥር ይክፈሉ። ከፍለው ከጨረሱ ፍለጋ ይከፈታል።`)) {
            rulingsAccess = true;
            document.getElementById("rulingSearchArea").style.display = "block";
            // populate category filter
            const filterSelect = document.getElementById("lawFilter");
            const cats = [...new Set(config.rulings.map(r => r.category))];
            filterSelect.innerHTML = '<option value="all">ሁሉም</option>' + cats.map(c => `<option value="${c}">${c}</option>`).join('');
        }
    });
    function searchRulingsFunc() {
        if(!rulingsAccess) { alert("መጀመሪያ ክፍያ ያስፈልጋል"); return; }
        const category = document.getElementById("lawFilter").value;
        const query = document.getElementById("searchRuling").value.toLowerCase();
        let filtered = config.rulings.filter(r => (category === "all" || r.category === category) && (r.caseNumber.toLowerCase().includes(query) || r.summary.toLowerCase().includes(query)));
        const resultsDiv = document.getElementById("rulingResults");
        if(filtered.length === 0) resultsDiv.innerHTML = "<p>ምንም አልተገኘም</p>";
        else resultsDiv.innerHTML = filtered.map(r => `<div><strong>${r.caseNumber}</strong> (${r.category})<br>${r.summary}<br><small>ፋይል: ${r.fileRef}</small></div>`).join("");
    }
    document.getElementById("searchRulingBtn")?.addEventListener("click", searchRulingsFunc);
    document.getElementById("profilePhotoBtn")?.addEventListener("click", () => alert("ዮናታን ዳዊት መንግስቱ - የህግ ባለሞያ"));
    
    // Initial apply
    applyConfigToUI();
    updateLang();
</script>
</body>
</html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>የህግ ባለሞያ ለኢትዮጵያ - ማዋቀሪያ ፓነል ያለው</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0f172a;
            line-height: 1.5;
        }
        /* header & main content (same as before) */
        .header { background: linear-gradient(135deg, #0a2b3e 0%, #1e4a6e 100%); color: white; padding: 1rem 2rem; position: sticky; top: 0; z-index: 1000; }
        .header-container { max-width: 1400px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem; }
        .logo-area { display: flex; align-items: center; gap: 1rem; }
        .profile-photo { width: 55px; height: 55px; background: #f59e0b; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; overflow: hidden; border: 2px solid #ffd966; }
        .profile-photo img { width: 100%; height: 100%; object-fit: cover; }
        .site-title h1 { font-size: 1.4rem; }
        .lang-switch { display: flex; gap: 0.5rem; background: rgba(255,255,255,0.2); padding: 0.4rem 0.8rem; border-radius: 40px; }
        .lang-btn { background: none; border: none; color: white; font-weight: 600; cursor: pointer; padding: 0.3rem 0.8rem; border-radius: 30px; }
        .lang-btn.active { background: #f59e0b; color: #0f172a; }
        .container { max-width: 1400px; margin: 2rem auto; padding: 0 2rem; }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.8rem; margin-bottom: 2rem; }
        .card { background: white; border-radius: 24px; padding: 1.5rem; box-shadow: 0 4px 12px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; transition: 0.2s; }
        .btn { background: #1e4a6e; color: white; border: none; padding: 0.7rem 1.3rem; border-radius: 40px; font-weight: 500; cursor: pointer; display: inline-flex; align-items: center; gap: 0.5rem; }
        .btn-warning { background: #f59e0b; color: #0f172a; }
        .payment-options { background: #fef9e3; padding: 1rem; border-radius: 16px; margin: 1rem 0; }
        .social-links { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 1rem; }
        .social-link { background: #eef2ff; padding: 0.5rem 1rem; border-radius: 40px; text-decoration: none; color: #0f172a; font-weight: 500; }
        .section { background: white; border-radius: 24px; padding: 1.8rem; margin-bottom: 2rem; border: 1px solid #e2e8f0; }
        .modal { display: none; position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.7); justify-content: center; align-items: center; z-index: 2000; }
        .modal-content { background: white; padding: 2rem; border-radius: 28px; max-width: 600px; width: 90%; max-height: 80vh; overflow-y: auto; }
        footer { text-align: center; padding: 2rem; background: #0f172a; color: #94a3b8; margin-top: 2rem; }
        
        /* Settings Panel (cog wheel) */
        .settings-cog {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #1e4a6e;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 1500;
            transition: 0.2s;
            color: white;
            font-size: 1.8rem;
        }
        .settings-cog:hover { transform: scale(1.05); background: #0f3b55; }
        .settings-panel {
            position: fixed;
            top: 0;
            right: -450px;
            width: 450px;
            height: 100%;
            background: white;
            box-shadow: -2px 0 20px rgba(0,0,0,0.2);
            z-index: 1600;
            transition: right 0.3s ease;
            display: flex;
            flex-direction: column;
            overflow-y: auto;
            font-family: monospace;
        }
        .settings-panel.open { right: 0; }
        .settings-header {
            background: #0a2b3e;
            color: white;
            padding: 1.2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
        }
        .settings-body { padding: 1.5rem; flex:1; }
        .setting-group { margin-bottom: 1.5rem; border-bottom: 1px solid #e2e8f0; padding-bottom: 1rem; }
        .setting-group label { display: block; font-weight: 600; margin-bottom: 0.5rem; }
        .setting-group input, .setting-group textarea, .setting-group select { width: 100%; padding: 0.5rem; border-radius: 8px; border: 1px solid #cbd5e1; }
        .setting-group textarea { height: 80px; }
        .array-item { background: #f1f5f9; padding: 0.5rem; margin-bottom: 0.5rem; border-radius: 8px; display: flex; gap: 0.5rem; align-items: center; }
        .array-item input { flex:1; }
        .btn-small { background: #e2e8f0; border: none; padding: 0.2rem 0.6rem; border-radius: 20px; cursor: pointer; }
        .btn-danger { background: #ef4444; color: white; }
        .btn-save { background: #10b981; color: white; width: 100%; margin-top: 1rem; }
        .overlay { position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.4); z-index: 1550; display: none; }
        .overlay.show { display: block; }
    </style>
</head>
<body>

<div class="header">
    <div class="header-container">
        <div class="logo-area">
            <div class="profile-photo" id="profilePhotoBtn">
                <img id="profileImg" src="" alt="Profile" style="display:none; width:100%; height:100%; object-fit:cover;">
                <i id="defaultIcon" class="fas fa-user-graduate"></i>
            </div>
            <div class="site-title">
                <h1 id="siteTitle"></h1>
                <p id="siteSubtitle"></p>
            </div>
        </div>
        <div class="lang-switch">
            <button class="lang-btn active" data-lang="am">አማርኛ</button>
            <button class="lang-btn" data-lang="en">English</button>
        </div>
    </div>
</div>

<div class="container">
    <div class="services-grid">
        <div class="card"><i class="fas fa-gavel"></i><h3 data-key="legalConsultTitle"></h3><p data-key="legalConsultDesc"></p><button class="btn consultBtn"><i class="fas fa-comments"></i> <span data-key="consultBtnText"></span></button></div>
        <div class="card"><i class="fas fa-video"></i><h3 data-key="mediaLawTitle"></h3><p data-key="mediaLawDesc"></p><button class="btn btn-outline" id="viewMediaBtn"><i class="fas fa-play-circle"></i> <span data-key="viewMedia"></span></button></div>
        <div class="card"><i class="fas fa-chalkboard-user"></i><h3 data-key="trainingTitle"></h3><p data-key="trainingDesc"></p><button class="btn" id="trainingsBtn"><i class="fas fa-certificate"></i> <span data-key="trainingsBtn"></span></button></div>
        <div class="card"><i class="fas fa-share-alt"></i><h3 data-key="socialShareTitle"></h3><p data-key="socialShareDesc"></p><div id="socialLinks" class="social-links"></div></div>
    </div>
    <div class="section" id="mediaLibrary"><h2><i class="fas fa-database"></i> <span data-key="libraryTitle"></span></h2><div id="mediaGrid" style="display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:1rem;"></div></div>
    <div class="section"><h2><i class="fas fa-balance-scale"></i> <span data-key="rulingTitle"></span></h2><p data-key="rulingDesc"></p><div class="payment-options" id="paymentOptions"></div><button class="btn btn-warning" id="purchaseRulingBtn"><i class="fas fa-key"></i> <span data-key="purchaseAccess"></span></button><div id="rulingSearchArea" style="display:none;"><select id="lawFilter"><option value="all">ሁሉም</option></select><input type="text" id="searchRuling" placeholder="ፈልግ..."><button id="searchRulingBtn">ፈልግ</button><div id="rulingResults"></div></div></div>
    <div class="section"><h2><i class="fas fa-user-plus"></i> <span data-key="joinTitle"></span></h2><p data-key="joinDesc"></p><div id="joinLinks" class="social-links"></div></div>
</div>
<footer><p>© 2025 የህግ ባለሞያ ለኢትዮጵያ</p></footer>

<!-- Settings Cog & Panel -->
<div class="settings-cog" id="settingsCog"><i class="fas fa-cog"></i></div>
<div class="overlay" id="settingsOverlay"></div>
<div class="settings-panel" id="settingsPanel">
    <div class="settings-header">
        <span><i class="fas fa-sliders-h"></i> የዌብሳይት ማዋቀሪያ (Settings)</span>
        <button id="closeSettingsBtn" style="background:none; border:none; color:white; font-size:1.5rem;">&times;</button>
    </div>
    <div class="settings-body">
        <div class="setting-group">
            <label>የገጽ ርዕስ (አማርኛ)</label>
            <input type="text" id="setTitleAm" placeholder="የህግ ባለሞያ ለኢትዮጵያ">
        </div>
        <div class="setting-group">
            <label>የገጽ ርዕስ (English)</label>
            <input type="text" id="setTitleEn" placeholder="Lawyers for Ethiopia">
        </div>
        <div class="setting-group">
            <label>የፕሮፋይል ፎቶ URL (ሙሉ አድራሻ ወይም ፋይል ስም)</label>
            <input type="text" id="setProfilePic" placeholder="e.g., profile.jpg or https://...">
        </div>
        <div class="setting-group">
            <label>የኢትዮጵያ ንግድ ባንክ ቁጥር</label>
            <input type="text" id="setBank" placeholder="1000417819437">
        </div>
        <div class="setting-group">
            <label>ሲቢኢ ብር / ቴሌ ብር ቁጥር</label>
            <input type="text" id="setMobileMoney" placeholder="0951727278">
        </div>
        <div class="setting-group">
            <label>ቲክቶክ አገናኝ</label>
            <input type="text" id="setTiktok" placeholder="https://www.tiktok.com/@...">
        </div>
        <div class="setting-group">
            <label>ፌስቡክ አገናኝ</label>
            <input type="text" id="setFacebook" placeholder="https://www.facebook.com/...">
        </div>
        <div class="setting-group">
            <label>ቴሌግራም አገናኝ</label>
            <input type="text" id="setTelegram" placeholder="https://t.me/...">
        </div>
        <div class="setting-group">
            <label>የሰበር ውሳኔዎች ዋጋ (ብር)</label>
            <input type="number" id="setRulingPrice" value="500">
        </div>
        <div class="setting-group">
            <label>የሚዲያ ዝርዝር (JSON ቅርጸት - አርትዕ ማድረግ ለሚችሉ ተጠቃሚዎች)</label>
            <textarea id="setMediaItems" rows="5" placeholder='[{"type":"document","title":"የወንጀል ህግ","url":"#","desc":"..."}]'></textarea>
        </div>
        <div class="setting-group">
            <label>የሰበር ውሳኔዎች (JSON)</label>
            <textarea id="setRulings" rows="5" placeholder='[{"category":"የወንጀል ህግ","caseNumber":"ሰበር 101/2012","summary":"..."}]'></textarea>
        </div>
        <button class="btn-save" id="saveSettingsBtn"><i class="fas fa-save"></i> ማዋቀሪያዎችን አስቀምጥ</button>
        <button class="btn" id="exportSettingsBtn" style="margin-top:0.5rem; background:#6c757d;"><i class="fas fa-download"></i> ማዋቀሪያ ኮድ አውጣ</button>
        <p style="font-size:0.8rem; margin-top:1rem;">ማስታወሻ: ለውጦች በአሁኑ ጊዜ በእርስዎ ብራውዘር ውስጥ ይቀመጣሉ። ወደ GitHub ለመላክ ከላይ "ኮድ አውጣ" በመጫን የተሻሻለውን CONFIG ማግኘት ይችላሉ።</p>
    </div>
</div>

<script>
    // ---------- DEFAULT CONFIG (same as before) ----------
    const defaultConfig = {
        siteTitle_am: "የህግ ባለሞያ ለኢትዮጵያ",
        siteTitle_en: "Lawyers for Ethiopia",
        siteSubtitle_am: "የህግ እውቀት ለሁሉም",
        siteSubtitle_en: "Legal Knowledge for Everyone",
        profileImageUrl: "",
        paymentBank: "1000417819437",
        paymentMobile: "0951727278",
        social: { tiktok: "https://www.tiktok.com/@lawyersforethiopia", facebook: "https://www.facebook.com/Lawyeryonatandawit", telegram: "https://t.me/LAWYERSFORETHIOPIA" },
        rulingPrice: 500,
        mediaItems: [
            { id:1, type:"document", title:"የወንጀል ህግ ቁ.1", url:"#", desc:"የኢትዮጵያ ወንጀል ህግ" },
            { id:2, type:"video", title:"የውል ህግ ትምህርት", url:"https://www.youtube.com/embed/dQw4w9WgXcQ", desc:"ቪዲዮ" }
        ],
        rulings: [
            { id:1, category:"የወንጀል ህግ", caseNumber:"ሰበር 101/2012", summary:"የህይወት እስራት", fileRef:"ሰ/ሰ/101" }
        ]
    };
    
    // Load from localStorage or default
    let config = JSON.parse(localStorage.getItem("lawyerSiteConfig")) || defaultConfig;
    
    // Helper to update UI based on config
    function applyConfigToUI() {
        document.getElementById("siteTitle").innerText = currentLang === "am" ? config.siteTitle_am : config.siteTitle_en;
        document.getElementById("siteSubtitle").innerText = currentLang === "am" ? config.siteSubtitle_am : config.siteSubtitle_en;
        // profile picture
        const profileImg = document.getElementById("profileImg");
        const defaultIcon = document.getElementById("defaultIcon");
        if(config.profileImageUrl && config.profileImageUrl.trim() !== "") {
            profileImg.src = config.profileImageUrl;
            profileImg.style.display = "block";
            defaultIcon.style.display = "none";
        } else {
            profileImg.style.display = "none";
            defaultIcon.style.display = "flex";
        }
        // payment options
        const paymentDiv = document.getElementById("paymentOptions");
        if(paymentDiv) {
            paymentDiv.innerHTML = `<i class="fas fa-money-bill-wave"></i> <strong>የክፍያ አማራጮች:</strong><br>
            🏦 የኢትዮጵያ ንግድ ባንክ: <strong>${config.paymentBank}</strong><br>
            📱 ሲቢኢ ብር/ቴሌ ብር: <strong>${config.paymentMobile}</strong>`;
        }
        // social links
        function buildSocial(containerId) {
            const container = document.getElementById(containerId);
            if(container) container.innerHTML = `
                <a href="${config.social.tiktok}" target="_blank" class="social-link"><i class="fab fa-tiktok"></i> TikTok</a>
                <a href="${config.social.facebook}" target="_blank" class="social-link"><i class="fab fa-facebook"></i> Facebook</a>
                <a href="${config.social.telegram}" target="_blank" class="social-link"><i class="fab fa-telegram"></i> Telegram</a>
            `;
        }
        buildSocial("socialLinks");
        buildSocial("joinLinks");
        // media library render
        renderMedia(config.mediaItems);
        // rulings price text
        document.querySelectorAll("[data-key='purchaseAccess']").forEach(el => el.innerText = (currentLang === "am" ? `የውሳኔ ፍለጋ መብት ግዙ (${config.rulingPrice} ብር)` : `Purchase Access (${config.rulingPrice} ETB)`));
        document.querySelectorAll("[data-key='rulingDesc']").forEach(el => el.innerText = currentLang === "am" ? `ከ${config.rulingPrice} ብር ክፍያ በኋላ ውሳኔዎችን ፈልግ` : `After ${config.rulingPrice} ETB payment, search rulings`);
        // store rulings for search
        window.currentRulings = config.rulings;
    }
    
    function renderMedia(mediaArray) {
        const grid = document.getElementById("mediaGrid");
        if(!grid) return;
        grid.innerHTML = "";
        mediaArray.forEach(item => {
            const card = document.createElement("div");
            card.style.background = "#fff";
            card.style.padding = "1rem";
            card.style.borderRadius = "16px";
            card.style.border = "1px solid #e2e8f0";
            let inner = "";
            if(item.type === "document") inner = `<i class="fas fa-file-pdf"></i><h4>${item.title}</h4><p>${item.desc}</p><a href="${item.url}" target="_blank">ክፈት</a>`;
            else if(item.type === "video") inner = `<i class="fas fa-video"></i><h4>${item.title}</h4><iframe width="100%" height="150" src="${item.url}" frameborder="0"></iframe>`;
            else if(item.type === "image") inner = `<img src="${item.url}" width="100%"><h4>${item.title}</h4>`;
            else if(item.type === "audio") inner = `<i class="fas fa-headphones"></i><h4>${item.title}</h4><audio controls src="${item.url}" style="width:100%"></audio>`;
            card.innerHTML = inner;
            grid.appendChild(card);
        });
    }
    
    // Language handling
    let currentLang = "am";
    const translations = {
        am: { legalConsultTitle:"የህግ ማማከር", legalConsultDesc:"ከባለሙያዎች የህግ ምክር ያግኙ", consultBtnText:"አማክሩኝ", mediaLawTitle:"የህግ ትምህርቶች", mediaLawDesc:"በቪዲዮ፣ ድምጽ፣ ምስል", viewMedia:"ይዘቶችን ይመልከቱ", trainingTitle:"ቋሚ ስልጠናዎች", trainingDesc:"የኢትዮጵያ ህጎች", trainingsBtn:"ስልጠናዎች", socialShareTitle:"ማህበራዊ ሚዲያ", socialShareDesc:"ይቀላቀሉ", libraryTitle:"የህግ ማውጫ", rulingTitle:"የሰበር ውሳኔዎች", joinTitle:"መቀላቀል", joinDesc:"ቅድመ ሁኔታዎችን ይመልከቱ" },
        en: { legalConsultTitle:"Legal Consultation", legalConsultDesc:"Get legal advice", consultBtnText:"Consult", mediaLawTitle:"Law Tutorials", mediaLawDesc:"Video/Audio/Image", viewMedia:"Browse Media", trainingTitle:"Trainings", trainingDesc:"Ethiopian laws", trainingsBtn:"Trainings", socialShareTitle:"Social Media", socialShareDesc:"Join us", libraryTitle:"Legal Library", rulingTitle:"Cassation Decisions", joinTitle:"Join Us", joinDesc:"Check prerequisites" }
    };
    function updateLang() {
        const t = translations[currentLang];
        for(let key in t) {
            let el = document.querySelector(`[data-key="${key}"]`);
            if(el) el.innerText = t[key];
        }
        applyConfigToUI(); // refresh dynamic texts
    }
    document.querySelectorAll(".lang-btn").forEach(btn => {
        btn.addEventListener("click", () => {
            currentLang = btn.getAttribute("data-lang");
            document.querySelectorAll(".lang-btn").forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            updateLang();
        });
    });
    
    // Settings panel functionality
    const cog = document.getElementById("settingsCog");
    const panel = document.getElementById("settingsPanel");
    const overlay = document.getElementById("settingsOverlay");
    const closeBtn = document.getElementById("closeSettingsBtn");
    function openSettings() {
        // populate fields from current config
        document.getElementById("setTitleAm").value = config.siteTitle_am;
        document.getElementById("setTitleEn").value = config.siteTitle_en;
        document.getElementById("setProfilePic").value = config.profileImageUrl || "";
        document.getElementById("setBank").value = config.paymentBank;
        document.getElementById("setMobileMoney").value = config.paymentMobile;
        document.getElementById("setTiktok").value = config.social.tiktok;
        document.getElementById("setFacebook").value = config.social.facebook;
        document.getElementById("setTelegram").value = config.social.telegram;
        document.getElementById("setRulingPrice").value = config.rulingPrice;
        document.getElementById("setMediaItems").value = JSON.stringify(config.mediaItems, null, 2);
        document.getElementById("setRulings").value = JSON.stringify(config.rulings, null, 2);
        panel.classList.add("open");
        overlay.classList.add("show");
    }
    function closeSettings() {
        panel.classList.remove("open");
        overlay.classList.remove("show");
    }
    cog.addEventListener("click", openSettings);
    closeBtn.addEventListener("click", closeSettings);
    overlay.addEventListener("click", closeSettings);
    
    document.getElementById("saveSettingsBtn").addEventListener("click", () => {
        // gather values
        config.siteTitle_am = document.getElementById("setTitleAm").value;
        config.siteTitle_en = document.getElementById("setTitleEn").value;
        config.profileImageUrl = document.getElementById("setProfilePic").value;
        config.paymentBank = document.getElementById("setBank").value;
        config.paymentMobile = document.getElementById("setMobileMoney").value;
        config.social.tiktok = document.getElementById("setTiktok").value;
        config.social.facebook = document.getElementById("setFacebook").value;
        config.social.telegram = document.getElementById("setTelegram").value;
        config.rulingPrice = parseInt(document.getElementById("setRulingPrice").value) || 500;
        try {
            config.mediaItems = JSON.parse(document.getElementById("setMediaItems").value);
            config.rulings = JSON.parse(document.getElementById("setRulings").value);
        } catch(e) { alert("JSON ቅርጸት ስህተት ነው"); return; }
        localStorage.setItem("lawyerSiteConfig", JSON.stringify(config));
        applyConfigToUI();
        updateLang();
        closeSettings();
        alert("ማዋቀሪያዎች ተቀምጠዋል! ገጹ ታድሷል።");
    });
    
    document.getElementById("exportSettingsBtn").addEventListener("click", () => {
        const exportCode = `// ይህንን CONFIG ወደ ዌብሳይትዎ ኮድ ይቅዱ
const CONFIG = ${JSON.stringify(config, null, 2)};`;
        const blob = new Blob([exportCode], {type: "text/javascript"});
        const url = URL.createObjectURL(blob);
        const a = document.createElement("a");
        a.href = url;
        a.download = "website_config.js";
        a.click();
        URL.revokeObjectURL(url);
        alert("ማዋቀሪያዎች በፋይል ተወርደዋል። ይህን ፋይል ወደ GitHub በማስገባት ማዘመን ይችላሉ።");
    });
    
    // Consultation modal (simple)
    const consultModal = document.createElement("div"); consultModal.className = "modal"; consultModal.id = "consultModal";
    consultModal.innerHTML = `<div class="modal-content"><h3>የህግ ማማከር</h3><textarea id="consultQ" rows="4" placeholder="ጥያቄዎን ይጻፉ" style="width:100%"></textarea><button id="sendConsult" class="btn">ላክ</button><button id="closeConsult" class="btn-outline">ዝጋ</button></div>`;
    document.body.appendChild(consultModal);
    document.querySelectorAll(".consultBtn").forEach(btn => btn.addEventListener("click", () => consultModal.style.display = "flex"));
    document.getElementById("closeConsult")?.addEventListener("click", () => consultModal.style.display = "none");
    document.getElementById("sendConsult")?.addEventListener("click", () => { alert("ጥያቄ ተልኳል። መልስ በቅርቡ ይላካል"); consultModal.style.display = "none"; });
    document.getElementById("trainingsBtn")?.addEventListener("click", () => alert("ስልጠናዎች በቅርቡ ይጀምራሉ።"));
    document.getElementById("viewMediaBtn")?.addEventListener("click", () => document.getElementById("mediaLibrary").scrollIntoView({behavior:"smooth"}));
    
    // Rulings search logic
    let rulingsAccess = false;
    document.getElementById("purchaseRulingBtn")?.addEventListener("click", () => {
        if(confirm(`እባክዎ ${config.rulingPrice} ብር ከላይ በተጠቀሰው ቁጥር ይክፈሉ። ከፍለው ከጨረሱ ፍለጋ ይከፈታል።`)) {
            rulingsAccess = true;
            document.getElementById("rulingSearchArea").style.display = "block";
            // populate category filter
            const filterSelect = document.getElementById("lawFilter");
            const cats = [...new Set(config.rulings.map(r => r.category))];
            filterSelect.innerHTML = '<option value="all">ሁሉም</option>' + cats.map(c => `<option value="${c}">${c}</option>`).join('');
        }
    });
    function searchRulingsFunc() {
        if(!rulingsAccess) { alert("መጀመሪያ ክፍያ ያስፈልጋል"); return; }
        const category = document.getElementById("lawFilter").value;
        const query = document.getElementById("searchRuling").value.toLowerCase();
        let filtered = config.rulings.filter(r => (category === "all" || r.category === category) && (r.caseNumber.toLowerCase().includes(query) || r.summary.toLowerCase().includes(query)));
        const resultsDiv = document.getElementById("rulingResults");
        if(filtered.length === 0) resultsDiv.innerHTML = "<p>ምንም አልተገኘም</p>";
        else resultsDiv.innerHTML = filtered.map(r => `<div><strong>${r.caseNumber}</strong> (${r.category})<br>${r.summary}<br><small>ፋይል: ${r.fileRef}</small></div>`).join("");
    }
    document.getElementById("searchRulingBtn")?.addEventListener("click", searchRulingsFunc);
    document.getElementById("profilePhotoBtn")?.addEventListener("click", () => alert("ዮናታን ዳዊት መንግስቱ - የህግ ባለሞያ"));
    
    // Initial apply
    applyConfigToUI();
    updateLang();
</script>
</body>
</html>
