<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>የህግ ባለሞያ ለኢትዮጵያ | Lawyers for Ethiopia</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
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
        /* same styles as before but compact */
        .header { background: linear-gradient(135deg, #0a2b3e 0%, #1e4a6e 100%); color: white; padding: 1rem 2rem; position: sticky; top: 0; z-index: 1000; box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
        .header-container { max-width: 1400px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem; }
        .logo-area { display: flex; align-items: center; gap: 1rem; }
        .profile-photo { width: 55px; height: 55px; background: #f59e0b; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; transition: transform 0.2s; border: 2px solid #ffd966; overflow: hidden; }
        .profile-photo img { width: 100%; height: 100%; object-fit: cover; }
        .site-title h1 { font-size: 1.4rem; font-weight: 700; }
        .lang-switch { display: flex; gap: 0.5rem; background: rgba(255,255,255,0.2); padding: 0.4rem 0.8rem; border-radius: 40px; }
        .lang-btn { background: none; border: none; color: white; font-weight: 600; cursor: pointer; padding: 0.3rem 0.8rem; border-radius: 30px; transition: all 0.2s; }
        .lang-btn.active { background: #f59e0b; color: #0f172a; }
        .container { max-width: 1400px; margin: 2rem auto; padding: 0 2rem; }
        .admin-panel { background: white; border-radius: 20px; padding: 1.5rem; margin-bottom: 2rem; box-shadow: 0 4px 14px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; display: none; }
        .admin-panel.show { display: block; }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 1.8rem; margin-bottom: 2rem; }
        .card { background: white; border-radius: 24px; padding: 1.5rem; box-shadow: 0 4px 12px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; transition: 0.2s; }
        .card:hover { transform: translateY(-4px); }
        .card i { font-size: 2.2rem; color: #1e4a6e; margin-bottom: 1rem; }
        .btn { background: #1e4a6e; color: white; border: none; padding: 0.7rem 1.3rem; border-radius: 40px; font-weight: 500; cursor: pointer; display: inline-flex; align-items: center; gap: 0.5rem; }
        .btn-warning { background: #f59e0b; color: #0f172a; }
        .btn-outline { background: transparent; border: 1px solid #1e4a6e; color: #1e4a6e; }
        .payment-options { background: #fef9e3; padding: 1rem; border-radius: 16px; margin: 1rem 0; }
        .social-links { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 1rem; }
        .social-link { background: #eef2ff; padding: 0.5rem 1rem; border-radius: 40px; text-decoration: none; color: #0f172a; font-weight: 500; }
        .section { background: white; border-radius: 24px; padding: 1.8rem; margin-bottom: 2rem; border: 1px solid #e2e8f0; }
        .modal { display: none; position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.7); justify-content: center; align-items: center; z-index: 2000; }
        .modal-content { background: white; padding: 2rem; border-radius: 28px; max-width: 500px; width: 90%; }
        footer { text-align: center; padding: 2rem; background: #0f172a; color: #94a3b8; margin-top: 2rem; }
        @media (max-width:768px){ .container { padding: 0 1rem; } .header-container { flex-direction: column; } }
    </style>
</head>
<body>

<!-- ======================== -->
<!-- ALL SETTINGS IN ONE PLACE -->
<!-- ======================== -->
<script>
// 🔧 CONFIGURATION – ONLY EDIT THIS BLOCK 🔧
const CONFIG = {
    // Site Identity
    siteTitle_am: "የህግ ባለሞያ ለኢትዮጵያ",
    siteTitle_en: "Lawyers for Ethiopia",
    siteSubtitle_am: "የህግ እውቀት ለሁሉም",
    siteSubtitle_en: "Legal Knowledge for Everyone",
    
    // Profile Photo (use full URL or relative path like "profile.jpg")
    profileImageUrl: "",  // empty = shows default icon. Put your image path e.g., "myphoto.jpg"
    
    // Admin password (only Yonatan Dawit)
    adminPassword: "yonatan2025",
    
    // Payment Details
    paymentBank: "1000417819437",
    paymentCBE: "0951727278",
    paymentTelebirr: "0951727278",
    
    // Social Media Links
    social: {
        tiktok: "https://www.tiktok.com/@lawyersforethiopia",
        facebook: "https://www.facebook.com/Lawyeryonatandawit",
        telegram: "https://t.me/LAWYERSFORETHIOPIA"
    },
    
    // Ruling Access Price (in ETB)
    rulingPrice: 500,
    
    // Sample Rulings (add/remove/edit as you like)
    rulings: [
        { id:1, category:"የወንጀል ህግ", caseNumber:"ሰበር 101/2012", summary:"የህይወት እስራት ውሳኔ", fileRef:"ፋይል ቁጥር ሰ/ሰ/101" },
        { id:2, category:"የንግድ ህግ", caseNumber:"ሰበር 45/2018", summary:"የንግድ ውል አለመፈጸም", fileRef:"ፋይል ቁጥር ን/45/2018" },
        { id:3, category:"የውል ህግ", caseNumber:"ሰበር 22/2020", summary:"የኪራይ ውል አለመከበር", fileRef:"ውል 22/2020" }
    ],
    
    // Media Library items (documents, videos, images, audio)
    mediaItems: [
        { id:1, type:"document", title:"የወንጀል ህግ ቁ.1", url:"#", desc:"የኢትዮጵያ ወንጀል ህግ ሰነድ" },
        { id:2, type:"video", title:"የውል ህግ ትምህርት", url:"https://www.youtube.com/embed/dQw4w9WgXcQ", desc:"ቪዲዮ ማብራሪያ" },
        { id:3, type:"image", title:"የንግድ ህግ ማጠቃለያ", url:"https://picsum.photos/id/1/200/150", desc:"ምስላዊ ማብራሪያ" },
        { id:4, type:"audio", title:"የወንጀል ህግ ንባብ", url:"https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3", desc:"ድምጽ ቅጂ" }
    ],
    
    // Consultation email (where messages go) – demo only, replace with your email
    consultationEmail: "yonatan@example.com",
    
    // Language strings (you can add more keys)
    translations: {
        am: {
            legalConsultTitle: "የህግ ማማከር",
            legalConsultDesc: "ከባለሙያዎች የህግ ምክር ያግኙ።",
            consultBtnText: "አማክሩኝ",
            mediaLawTitle: "የህግ ትምህርቶች (ቪዲዮ/ድምጽ/ምስል)",
            mediaLawDesc: "የወንጀል፣ ንግድ፣ ውል ህጎች በተለያየ ቅርጸት",
            viewMedia: "ይዘቶችን ይመልከቱ",
            trainingTitle: "ቋሚ የህግ ስልጠናዎች",
            trainingDesc: "የኢትዮጵያ ህጎች ላይ ሰፊ ስልጠና",
            trainingsBtn: "ስልጠናዎች",
            socialShareTitle: "ማህበራዊ ድረ-ገፅ ስራዎቼን አጋራ",
            socialShareDesc: "በቲክቶክ፣ ፌስቡክ፣ ቴሌግራም ይቀላቀሉ",
            libraryTitle: "የህግ ማውጫ (ዶክመንት / ቪዲዮ / ምስል / ድምጽ)",
            rulingTitle: "የኢፌድሪ ሰበር ሰሚ ችሎት ውሳኔዎች",
            rulingDesc: `ከ${CONFIG.rulingPrice} ብር ክፍያ በኋላ ውሳኔዎችን ፈልገው ያግኙ`,
            paymentHeader: "የክፍያ አማራጮች",
            purchaseAccess: `የውሳኔ ፍለጋ መብት ግዙ (${CONFIG.rulingPrice} ብር)`,
            joinTitle: "ዌብሳይቱን መቀላቀል ለሚፈልጉ",
            joinDesc: "ቅድመ ሁኔታዎችን ከማህበራዊ ሚዲያ ይመልከቱ"
        },
        en: {
            legalConsultTitle: "Legal Consultation",
            legalConsultDesc: "Get legal advice from professionals.",
            consultBtnText: "Consult Now",
            mediaLawTitle: "Law Tutorials (Video/Audio/Image)",
            mediaLawDesc: "Criminal, Commercial, Contract law in various formats",
            viewMedia: "Browse Media",
            trainingTitle: "Permanent Legal Trainings",
            trainingDesc: "Comprehensive Ethiopian law courses",
            trainingsBtn: "Trainings",
            socialShareTitle: "Share My Social Media Works",
            socialShareDesc: "Join me on TikTok, Facebook, Telegram",
            libraryTitle: "Legal Library (Document/Video/Image/Audio)",
            rulingTitle: "Federal Supreme Court Cassation Decisions",
            rulingDesc: `After ${CONFIG.rulingPrice} ETB payment, search decisions by law field`,
            paymentHeader: "Payment Options",
            purchaseAccess: `Purchase Ruling Access (${CONFIG.rulingPrice} ETB)`,
            joinTitle: "For Those Who Wish to Join",
            joinDesc: "Check prerequisites on our social accounts"
        }
    }
};

// Apply site titles from config
document.addEventListener("DOMContentLoaded", () => {
    if(CONFIG.siteTitle_am) document.getElementById("siteTitle").innerText = CONFIG.siteTitle_am;
    if(CONFIG.siteSubtitle_am) document.getElementById("siteSubtitle").innerText = CONFIG.siteSubtitle_am;
});
</script>

<div class="header">
    <div class="header-container">
        <div class="logo-area">
            <div class="profile-photo" id="profilePhotoBtn">
                <!-- profile image from CONFIG -->
                <img id="profileImg" src="" alt="Profile" style="width:100%; height:100%; object-fit:cover; border-radius:50%; display:none;">
                <i id="defaultProfileIcon" class="fas fa-user-graduate"></i>
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
    <!-- Admin Panel (only visible after correct password) -->
    <div id="adminPanel" class="admin-panel">
        <div class="admin-credentials">
            <i class="fas fa-lock"></i> <strong id="adminWelcome">የአስተዳዳሪ ፓነል</strong>
            <p>ልዩ ተደራሽነት: ይዘት መጨመር፣ ማስወገድ፣ ማዘመን</p>
            <button class="btn btn-outline" id="logoutAdminBtn"><i class="fas fa-sign-out-alt"></i> Logout</button>
        </div>
        <div>
            <h4><i class="fas fa-upload"></i> አዲስ የህግ ይዘት አጋራ</h4>
            <input type="text" id="newDocTitle" placeholder="ርዕስ" style="width:70%">
            <select id="docTypeSelect">
                <option value="document">ዶክመንት</option><option value="video">ቪዲዮ</option><option value="image">ምስል</option><option value="audio">ድምጽ</option>
            </select>
            <button class="btn" id="addContentBtn">አክል</button>
        </div>
        <div style="margin-top:1rem;">
            <h4>ማህደር አስተዳደር</h4>
            <button class="btn btn-outline" id="deleteLastMediaBtn">የመጨረሻውን ይዘት ሰርዝ</button>
        </div>
    </div>

    <!-- Services Grid -->
    <div class="services-grid">
        <div class="card"><i class="fas fa-gavel"></i><h3 data-key="legalConsultTitle"></h3><p data-key="legalConsultDesc"></p><button class="btn" id="consultBtn"><i class="fas fa-comments"></i> <span data-key="consultBtnText"></span></button></div>
        <div class="card"><i class="fas fa-video"></i><h3 data-key="mediaLawTitle"></h3><p data-key="mediaLawDesc"></p><button class="btn btn-outline" id="viewMediaBtn"><i class="fas fa-play-circle"></i> <span data-key="viewMedia"></span></button></div>
        <div class="card"><i class="fas fa-chalkboard-user"></i><h3 data-key="trainingTitle"></h3><p data-key="trainingDesc"></p><button class="btn" id="trainingsBtn"><i class="fas fa-certificate"></i> <span data-key="trainingsBtn"></span></button></div>
        <div class="card"><i class="fas fa-share-alt"></i><h3 data-key="socialShareTitle"></h3><p data-key="socialShareDesc"></p><div class="social-links" id="socialLinks"></div></div>
    </div>

    <!-- Media Library -->
    <div class="section" id="mediaLibrarySection"><h2><i class="fas fa-database"></i> <span data-key="libraryTitle"></span></h2><div id="mediaGrid" style="display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:1rem; margin-top:1rem;"></div></div>

    <!-- Supreme Court Rulings -->
    <div class="section"><h2><i class="fas fa-balance-scale"></i> <span data-key="rulingTitle"></span></h2><p data-key="rulingDesc"></p><div class="payment-options" id="paymentOptions"></div><button class="btn btn-warning" id="purchaseRulingAccessBtn"><i class="fas fa-key"></i> <span data-key="purchaseAccess"></span></button><div id="rulingSearchArea" style="display:none; margin-top:1.5rem;"><div class="ruling-search"><select id="lawCategoryFilter"><option value="all">ሁሉም ዘርፎች</option><option value="የወንጀል ህግ">የወንጀል ህግ</option><option value="የንግድ ህግ">የንግድ ህግ</option><option value="የውል ህግ">የውል ህግ</option></select><input type="text" id="searchRulingInput" placeholder="የውሳኔ ፍለጊያ..."><button class="btn" id="searchRulingBtn"><i class="fas fa-search"></i> ፈልግ</button></div><div id="rulingResults" style="background:#f1f5f9; border-radius:16px; padding:1rem;"></div></div></div>

    <!-- Join Section -->
    <div class="section"><h2><i class="fas fa-user-plus"></i> <span data-key="joinTitle"></span></h2><p data-key="joinDesc"></p><div class="social-links" id="joinSocialLinks"></div></div>
</div>
<footer><p>© 2025 የህግ ባለሞያ ለኢትዮጵያ | Lawyers for Ethiopia</p></footer>

<!-- Consultation Modal -->
<div id="consultModal" class="modal"><div class="modal-content"><h3 id="modalTitle">የህግ ማማከር አገልግሎት</h3><textarea id="consultQuestion" rows="4" placeholder="የህግ ጥያቄዎን ይጻፉ..." style="width:100%; margin:1rem 0;"></textarea><button class="btn" id="sendConsultBtn">ላክ</button><button class="btn btn-outline" id="closeModalBtn">ዝጋ</button></div></div>

<script>
// ------------------- Apply CONFIG to UI -------------------
// Profile image
const profileImg = document.getElementById("profileImg");
const defaultIcon = document.getElementById("defaultProfileIcon");
if(CONFIG.profileImageUrl && CONFIG.profileImageUrl.trim() !== "") {
    profileImg.src = CONFIG.profileImageUrl;
    profileImg.style.display = "block";
    defaultIcon.style.display = "none";
} else {
    profileImg.style.display = "none";
    defaultIcon.style.display = "flex";
}
// Payment options display
const paymentDiv = document.getElementById("paymentOptions");
if(paymentDiv) {
    paymentDiv.innerHTML = `<i class="fas fa-money-bill-wave"></i> <strong data-key="paymentHeader"></strong><br>
    <span>🏦 የኢትዮጵያ ንግድ ባንክ: <strong>${CONFIG.paymentBank}</strong></span><br>
    <span>📱 ሲቢኢ ብር: <strong>${CONFIG.paymentCBE}</strong></span><br>
    <span>💳 ቴሌ ብር: <strong>${CONFIG.paymentTelebirr}</strong></span>`;
}
// Social links from config
function buildSocialLinks(containerId) {
    const container = document.getElementById(containerId);
    if(container) {
        container.innerHTML = `
            <a href="${CONFIG.social.tiktok}" target="_blank" class="social-link"><i class="fab fa-tiktok"></i> TikTok</a>
            <a href="${CONFIG.social.facebook}" target="_blank" class="social-link"><i class="fab fa-facebook"></i> Facebook</a>
            <a href="${CONFIG.social.telegram}" target="_blank" class="social-link"><i class="fab fa-telegram"></i> Telegram</a>
        `;
    }
}
buildSocialLinks("socialLinks");
buildSocialLinks("joinSocialLinks");

// Media library state (copy from CONFIG)
let mediaItems = [...CONFIG.mediaItems];
let rulingsData = [...CONFIG.rulings];

// Language & translations
let currentLang = "am";
const translations = CONFIG.translations;
function updateLanguage() {
    const t = translations[currentLang];
    for(let key in t) {
        let elem = document.querySelector(`[data-key="${key}"]`);
        if(elem) elem.innerText = t[key];
    }
    document.getElementById("siteTitle").innerText = currentLang === "am" ? CONFIG.siteTitle_am : CONFIG.siteTitle_en;
    document.getElementById("siteSubtitle").innerText = currentLang === "am" ? CONFIG.siteSubtitle_am : CONFIG.siteSubtitle_en;
    document.querySelectorAll("[data-key='paymentHeader']").forEach(el => el.innerText = currentLang === "am" ? "የክፍያ አማራጮች" : "Payment Options");
    document.querySelectorAll("[data-key='purchaseAccess']").forEach(el => el.innerText = (currentLang === "am" ? `የውሳኔ ፍለጋ መብት ግዙ (${CONFIG.rulingPrice} ብር)` : `Purchase Ruling Access (${CONFIG.rulingPrice} ETB)`));
    document.querySelectorAll("[data-key='rulingDesc']").forEach(el => el.innerText = currentLang === "am" ? `ከ${CONFIG.rulingPrice} ብር ክፍያ በኋላ ውሳኔዎችን ፈልገው ያግኙ` : `After ${CONFIG.rulingPrice} ETB payment, search decisions by law field`);
}
document.querySelectorAll(".lang-btn").forEach(btn => {
    btn.addEventListener("click", () => {
        currentLang = btn.getAttribute("data-lang");
        document.querySelectorAll(".lang-btn").forEach(b => b.classList.remove("active"));
        btn.classList.add("active");
        updateLanguage();
    });
});

// Render media grid
function renderMedia() {
    const grid = document.getElementById("mediaGrid");
    if(!grid) return;
    grid.innerHTML = "";
    mediaItems.forEach(item => {
        const card = document.createElement("div");
        card.style.background = "#fff";
        card.style.padding = "1rem";
        card.style.borderRadius = "16px";
        card.style.border = "1px solid #e2e8f0";
        let inner = "";
        if(item.type === "document") inner = `<i class="fas fa-file-pdf" style="font-size:2rem;"></i><h4>${item.title}</h4><p>${item.desc}</p><a href="${item.url}" target="_blank">ክፈት</a>`;
        else if(item.type === "video") inner = `<i class="fas fa-video"></i><h4>${item.title}</h4><iframe width="100%" height="150" src="${item.url}" frameborder="0"></iframe>`;
        else if(item.type === "image") inner = `<img src="${item.url}" width="100%" style="border-radius:12px;"><h4>${item.title}</h4>`;
        else if(item.type === "audio") inner = `<i class="fas fa-headphones"></i><h4>${item.title}</h4><audio controls src="${item.url}" style="width:100%"></audio>`;
        card.innerHTML = inner;
        grid.appendChild(card);
    });
}

// Admin logic
let isAdmin = false;
function checkAdmin() {
    let pwd = prompt("የአስተዳዳሪ ይለፍ ቃል ያስገቡ:");
    if(pwd === CONFIG.adminPassword) {
        isAdmin = true;
        document.getElementById("adminPanel").classList.add("show");
    } else if(pwd !== null) alert("የይለፍ ቃል ተሳስቷል");
}
setTimeout(checkAdmin, 500);
document.getElementById("logoutAdminBtn")?.addEventListener("click", () => { isAdmin = false; document.getElementById("adminPanel").classList.remove("show"); });
document.getElementById("addContentBtn")?.addEventListener("click", () => {
    if(!isAdmin) { alert("አስተዳዳሪ ብቻ!"); return; }
    const title = document.getElementById("newDocTitle").value;
    const type = document.getElementById("docTypeSelect").value;
    if(!title) { alert("ርዕስ ያስፈልጋል"); return; }
    let demoUrl = "#";
    if(type === "video") demoUrl = "https://www.youtube.com/embed/dQw4w9WgXcQ";
    if(type === "image") demoUrl = "https://picsum.photos/id/20/200/150";
    if(type === "audio") demoUrl = "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3";
    mediaItems.push({ id: Date.now(), type, title, url: demoUrl, desc: "አዲስ ይዘት" });
    renderMedia();
    document.getElementById("newDocTitle").value = "";
});
document.getElementById("deleteLastMediaBtn")?.addEventListener("click", () => {
    if(!isAdmin) { alert("አስተዳዳሪ ብቻ!"); return; }
    if(mediaItems.length > 0) { mediaItems.pop(); renderMedia(); }
    else alert("ምንም ይዘት የለም");
});

// Consultation modal
const modal = document.getElementById("consultModal");
document.getElementById("consultBtn")?.addEventListener("click", () => modal.style.display = "flex");
document.getElementById("closeModalBtn")?.addEventListener("click", () => modal.style.display = "none");
document.getElementById("sendConsultBtn")?.addEventListener("click", () => {
    const msg = document.getElementById("consultQuestion").value;
    if(msg) alert(`ማማከር ጥያቄ ተልኳል። በቅርቡ እንመልሳለን።\nQuestion: ${msg}\n(እውነተኛ ላኪ: ${CONFIG.consultationEmail})`);
    else alert("እባክዎ ጥያቄ ይጻፉ");
    modal.style.display = "none";
});

// Trainings
document.getElementById("trainingsBtn")?.addEventListener("click", () => {
    alert(currentLang === "am" ? "ቋሚ ስልጠናዎች በቅርቡ ይጀምራሉ። ለዝርዝር በቴሌግራም ይመዝገቡ።" : "Trainings coming soon. Join Telegram for updates.");
});

// Rulings purchase & search
let rulingsAccess = false;
document.getElementById("purchaseRulingAccessBtn")?.addEventListener("click", () => {
    if(confirm(currentLang === "am" ? `${CONFIG.rulingPrice} ብር ይክፈላሉ። ከከፈሉ በኋላ ፍለጋ ይከፈታል።` : `Pay ${CONFIG.rulingPrice} ETB to access rulings.`)) {
        rulingsAccess = true;
        document.getElementById("rulingSearchArea").style.display = "block";
        alert("አመሰግናለሁ! አሁን የሰበር ውሳኔዎችን መፈለግ ይችላሉ።");
    }
});
function searchRulings() {
    if(!rulingsAccess) { alert("እባክዎ በመጀመሪያ ክፍያ ያድርጉ"); return; }
    const category = document.getElementById("lawCategoryFilter").value;
    const query = document.getElementById("searchRulingInput").value.toLowerCase();
    let filtered = rulingsData.filter(r => (category === "all" || r.category === category) && (r.caseNumber.toLowerCase().includes(query) || r.summary.toLowerCase().includes(query)));
    const resultsDiv = document.getElementById("rulingResults");
    if(filtered.length === 0) { resultsDiv.innerHTML = "<p>ምንም ውጤት አልተገኘም</p>"; return; }
    resultsDiv.innerHTML = filtered.map(r => `<div style="border-bottom:1px solid #cbd5e1; padding:0.5rem;"><strong>${r.caseNumber}</strong> (${r.category})<br>${r.summary}<br><small>ፋይል ቁጥር: ${r.fileRef}</small></div>`).join("");
}
document.getElementById("searchRulingBtn")?.addEventListener("click", searchRulings);
document.getElementById("viewMediaBtn")?.addEventListener("click", () => document.getElementById("mediaLibrarySection").scrollIntoView({ behavior: "smooth" }));
document.getElementById("profilePhotoBtn")?.addEventListener("click", () => alert("👨‍⚖️ ዮናታን ዳዊት መንግስቱ | Yonatan Dawit Mengistu\n⚖️ የህግ ባለሞያ"));

// Initial render
renderMedia();
updateLanguage();
</script>
</body>
</html>
