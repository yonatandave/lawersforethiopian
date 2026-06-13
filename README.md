<div class="profile-photo" id="profilePhotoBtn" style="background-image: url('profile.jpg'); background-size: cover; background-position: center;">
    <!-- remove the <i> tag or hide it -->
</div><!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
git add .
git commit -m "Describe your changes"
git push    <title>የህግ ባለሞያ ለኢትዮጵያ | Lawyers for Ethiopia</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;git add index.html profile.jpg
git commit -m "Change profile picture"
git push
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0f172a;
            line-height: 1.5;
        }

        /* Header & Navigation */
        .header {
            background: linear-gradient(135deg, #0a2b3e 0%, #1e4a6e 100%);
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }

        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .profile-photo {
            width: 55px;
            height: 55px;
            background: #f59e0b;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: transform 0.2s;
            border: 2px solid #ffd966;
            overflow: hidden;
        }

        .profile-photo i {
            font-size: 2rem;
            color: #fff;
        }

        .profile-photo:hover {
            transform: scale(1.05);
        }

        .site-title h1 {
            font-size: 1.4rem;
            font-weight: 700;
        }

        .site-title p {
            font-size: 0.8rem;
            opacity: 0.9;
        }

        .lang-switch {
            display: flex;
            gap: 0.5rem;
            background: rgba(255,255,255,0.2);
            padding: 0.4rem 0.8rem;
            border-radius: 40px;
        }

        .lang-btn {
            background: none;
            border: none;
            color: white;
            font-weight: 600;
            cursor: pointer;
            padding: 0.3rem 0.8rem;
            border-radius: 30px;
            transition: all 0.2s;
        }

        .lang-btn.active {
            background: #f59e0b;
            color: #0f172a;
        }

        /* Main container */
        .container {
            max-width: 1400px;
            margin: 2rem auto;
            padding: 0 2rem;
        }

        /* admin panel (hidden by default) */
        .admin-panel {
            background: white;
            border-radius: 20px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 14px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            display: none;
        }

        .admin-panel.show {
            display: block;
        }

        .admin-credentials {
            background: #f1f5f9;
            padding: 1rem;
            border-radius: 16px;
            margin-bottom: 1rem;
        }

        /* Cards grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.8rem;
            margin-bottom: 2rem;
        }

        .card {
            background: white;
            border-radius: 24px;
            padding: 1.5rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            transition: 0.2s;
            border: 1px solid #e2e8f0;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }

        .card i {
            font-size: 2.2rem;
            color: #1e4a6e;
            margin-bottom: 1rem;
        }

        .card h3 {
            font-size: 1.4rem;
            margin-bottom: 0.75rem;
        }

        /* Training & rulings */
        .section {
            background: white;
            border-radius: 24px;
            padding: 1.8rem;
            margin-bottom: 2rem;
            border: 1px solid #e2e8f0;
        }

        .btn {
            background: #1e4a6e;
            color: white;
            border: none;
            padding: 0.7rem 1.3rem;
            border-radius: 40px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-warning {
            background: #f59e0b;
            color: #0f172a;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid #1e4a6e;
            color: #1e4a6e;
        }

        .payment-options {
            background: #fef9e3;
            padding: 1rem;
            border-radius: 16px;
            margin: 1rem 0;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1rem;
        }

        .social-link {
            background: #eef2ff;
            padding: 0.5rem 1rem;
            border-radius: 40px;
            text-decoration: none;
            color: #0f172a;
            font-weight: 500;
        }

        .ruling-search {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin: 1.2rem 0;
        }

        input, select, textarea {
            padding: 0.7rem;
            border-radius: 12px;
            border: 1px solid #cbd5e1;
            font-family: inherit;
        }

        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.7);
            justify-content: center;
            align-items: center;
            z-index: 2000;
        }

        .modal-content {
            background: white;
            padding: 2rem;
            border-radius: 28px;
            max-width: 500px;
            width: 90%;
        }

        footer {
            text-align: center;
            padding: 2rem;
            background: #0f172a;
            color: #94a3b8;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .container { padding: 0 1rem; }
            .header-container { flex-direction: column; }
        }
    </style>
</head>
<body>

<div class="header">
    <div class="header-container">
        <div class="logo-area">
            <div class="profile-photo" id="profilePhotoBtn">
                <i class="fas fa-user-graduate"></i>
            </div>
            <div class="site-title">
                <h1 id="siteTitle">የህግ ባለሞያ ለኢትዮጵያ</h1>
                <p id="siteSubtitle">Lawyers for Ethiopia | የህግ እውቀት ለሁሉም</p>
            </div>
        </div>
        <div class="lang-switch">
            <button class="lang-btn active" data-lang="am">አማርኛ</button>
            <button class="lang-btn" data-lang="en">English</button>
        </div>
    </div>
</div>

<div class="container">
    <!-- Admin Panel only visible after login (yonatan dawit) -->
    <div id="adminPanel" class="admin-panel">
        <div class="admin-credentials">
            <i class="fas fa-lock"></i> <strong id="adminWelcome">የአስተዳዳሪ ፓነል | በዮናታን ዳዊት መንግስቱ ብቻ</strong>
            <p id="adminInfo">ልዩ ተደራሽነት: ይዘት መጨመር፣ የሰበር ውሳኔዎችን ማስተዳደር፣ ስልጠናዎችን መፍጠር</p>
            <button class="btn btn-outline" id="logoutAdminBtn" style="margin-top:10px;"><i class="fas fa-sign-out-alt"></i> Logout</button>
        </div>
        <!-- quick upload demo -->
        <div>
            <h4><i class="fas fa-upload"></i> አዲስ የህግ ዶክመንት / ቪዲዮ አጋራ</h4>
            <input type="text" id="newDocTitle" placeholder="ርዕስ (Title)" style="width:70%">
            <select id="docTypeSelect">
                <option value="document">ዶክመንት</option>
                <option value="video">ቪዲዮ</option>
                <option value="image">ምስል</option>
                <option value="audio">ድምጽ</option>
            </select>
            <button class="btn" id="addContentBtn">አክል / Add</button>
            <p class="small" style="margin-top:8px;">* ማሳያ ዓላማ: ይዘቶች በ "የህግ ይዘቶች" ክፍል ይታያሉ</p>
        </div>
    </div>

    <!-- Services grid -->
    <div class="services-grid">
        <div class="card">
            <i class="fas fa-gavel"></i>
            <h3 data-key="legalConsultTitle">የህግ ማማከር</h3>
            <p data-key="legalConsultDesc">ከባለሙያዎች የህግ ምክር ያግኙ። ጥያቄዎን ይላኩልን።</p>
            <button class="btn" id="consultBtn"><i class="fas fa-comments"></i> <span data-key="consultBtnText">አማክሩኝ</span></button>
        </div>
        <div class="card">
            <i class="fas fa-video"></i>
            <h3 data-key="mediaLawTitle">የህግ ትምህርቶች (ቪዲዮ/ድምጽ/ምስል)</h3>
            <p data-key="mediaLawDesc">የወንጀል፣ ንግድ፣ ውል ህጎች በቪዲዮ፣ ድምጽ እና ሰነዶች ይገኛሉ።</p>
            <button class="btn btn-outline" id="viewMediaBtn"><i class="fas fa-play-circle"></i> <span data-key="viewMedia">ይዘቶችን ይመልከቱ</span></button>
        </div>
        <div class="card">
            <i class="fas fa-chalkboard-user"></i>
            <h3 data-key="trainingTitle">ቋሚ የህግ ስልጠናዎች</h3>
            <p data-key="trainingDesc">የኢትዮጵያ ህጎች ላይ ሰፊ ስልጠና በመስመር ላይ ይከታተሉ።</p>
            <button class="btn" id="trainingsBtn"><i class="fas fa-certificate"></i> <span data-key="trainingsBtn">ስልጠናዎች</span></button>
        </div>
        <div class="card">
            <i class="fas fa-share-alt"></i>
            <h3 data-key="socialShareTitle">ማህበራዊ ድረ-ገፅ ስራዎቼን አጋራ</h3>
            <p data-key="socialShareDesc">በቲክቶክ፣ ፌስቡክ፣ ቴሌግራም ይቀላቀሉና ያጋሩ።</p>
            <div class="social-links">
                <a href="https://www.tiktok.com/@lawyersforethiopia" target="_blank" class="social-link"><i class="fab fa-tiktok"></i> TikTok</a>
                <a href="https://www.facebook.com/Lawyeryonatandawit" target="_blank" class="social-link"><i class="fab fa-facebook"></i> Facebook</a>
                <a href="https://t.me/LAWYERSFORETHIOPIA" target="_blank" class="social-link"><i class="fab fa-telegram"></i> Telegram</a>
            </div>
        </div>
    </div>

    <!-- Law content area (documents, videos, images, audio) -->
    <div class="section" id="mediaLibrarySection">
        <h2><i class="fas fa-database"></i> <span data-key="libraryTitle">የህግ ማውጫ (ዶክመንት / ቪዲዮ / ምስል / ድምጽ)</span></h2>
        <div id="mediaGrid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(260px,1fr)); gap:1rem; margin-top:1rem;"></div>
    </div>

    <!-- Supreme Court rulings with payment simulation -->
    <div class="section">
        <h2><i class="fas fa-balance-scale"></i> <span data-key="rulingTitle">የኢፌድሪ ሰበር ሰሚ ችሎት ውሳኔዎች</span></h2>
        <p data-key="rulingDesc">ከ500 ብር ክፍያ በኋላ ውሳኔዎችን በህግ ዘርፍ ፈልገው ማግኘት ይችላሉ። ከዚህ በታች የክፍያ አማራጮች።</p>
        <div class="payment-options">
            <i class="fas fa-money-bill-wave"></i> <strong data-key="paymentHeader">የክፍያ አማራጮች:</strong><br>
            <span>🏦 የኢትዮጵያ ንግድ ባንክ: <strong>1000417819437</strong></span><br>
            <span>📱 ሲቢኢ ብር: <strong>0951727278</strong></span><br>
            <span>💳 ቴሌ ብር: <strong>0951727278</strong></span>
        </div>
        <button class="btn btn-warning" id="purchaseRulingAccessBtn"><i class="fas fa-key"></i> <span data-key="purchaseAccess">የውሳኔ ፍለጋ መብት ግዙ (500 ብር)</span></button>
        <div id="rulingSearchArea" style="display: none; margin-top: 1.5rem;">
            <div class="ruling-search">
                <select id="lawCategoryFilter">
                    <option value="all">ሁሉም ዘርፎች</option>
                    <option value="የወንጀል ህግ">የወንጀል ህግ</option>
                    <option value="የንግድ ህግ">የንግድ ህግ</option>
                    <option value="የውል ህግ">የውል ህግ</option>
                </select>
                <input type="text" id="searchRulingInput" placeholder="የውሳኔ ፍለጊያ... ለምሳሌ ቁጥር/ጉዳይ">
                <button class="btn" id="searchRulingBtn"><i class="fas fa-search"></i> ፈልግ</button>
            </div>
            <div id="rulingResults" style="background:#f1f5f9; border-radius:16px; padding:1rem;"></div>
        </div>
    </div>

    <!-- Join & Prerequisites -->
    <div class="section">
        <h2><i class="fas fa-user-plus"></i> <span data-key="joinTitle">ዌብሳይቱን መቀላቀል ለሚፈልጉ</span></h2>
        <p data-key="joinDesc">ከማህበራዊ ሚዲያ አካውንቶቻችን ጋር መቀላቀያ ቅድመ ሁኔታዎችን ያግኙ። ከዚህ በታች ያሉትን ይከተሉ።</p>
        <div class="social-links">
            <a href="https://www.tiktok.com/@lawyersforethiopia" class="social-link"><i class="fab fa-tiktok"></i> @lawyersforethiopia</a>
            <a href="https://www.facebook.com/Lawyeryonatandawit" class="social-link"><i class="fab fa-facebook"></i> Lawyer Yonatan Dawit</a>
            <a href="https://t.me/LAWYERSFORETHIOPIA" class="social-link"><i class="fab fa-telegram"></i> @LAWYERSFORETHIOPIA</a>
        </div>
    </div>
</div>

<footer>
    <p>© 2025 የህግ ባለሞያ ለኢትዮጵያ | Lawyers for Ethiopia | ሁሉም መብቶች ተጠብቀዋል</p>
</footer>

<!-- Modal for consultation -->
<div id="consultModal" class="modal">
    <div class="modal-content">
        <h3 id="modalTitle">የህግ ማማከር አገልግሎት</h3>
        <textarea id="consultQuestion" rows="4" placeholder="የህግ ጥያቄዎን ይጻፉ..." style="width:100%; margin: 1rem 0;"></textarea>
        <button class="btn" id="sendConsultBtn">ላክ / Send</button>
        <button class="btn btn-outline" id="closeModalBtn">ዝጋ</button>
    </div>
</div>

<script>
    // ---------- LANGUAGE SUPPORT ----------
    const translations = {
        am: {
            siteTitle: "የህግ ባለሞያ ለኢትዮጵያ",
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
            rulingDesc: "ከ500 ብር ክፍያ በኋላ ውሳኔዎችን ፈልገው ያግኙ",
            paymentHeader: "የክፍያ አማራጮች",
            purchaseAccess: "የውሳኔ ፍለጋ መብት ግዙ (500 ብር)",
            joinTitle: "ዌብሳይቱን መቀላቀል ለሚፈልጉ",
            joinDesc: "ቅድመ ሁኔታዎችን ከማህበራዊ ሚዲያ ይመልከቱ"
        },
        en: {
            siteTitle: "Lawyers for Ethiopia",
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
            rulingDesc: "After 500 ETB payment, search decisions by law field",
            paymentHeader: "Payment Options",
            purchaseAccess: "Purchase Ruling Access (500 ETB)",
            joinTitle: "For Those Who Wish to Join",
            joinDesc: "Check prerequisites on our social accounts"
        }
    };
    let currentLang = "am";
    function updateLanguage() {
        for(let key in translations[currentLang]) {
            let el = document.querySelector(`[data-key="${key}"]`);
            if(el) el.innerText = translations[currentLang][key];
            else {
                let idEl = document.getElementById(key);
                if(idEl) idEl.innerText = translations[currentLang][key];
            }
        }
        document.getElementById("siteTitle").innerText = translations[currentLang].siteTitle;
        const adminWelcome = document.getElementById("adminWelcome");
        if(adminWelcome) adminWelcome.innerHTML = currentLang === "am" ? "የአስተዳዳሪ ፓነል | በዮናታን ዳዊት መንግስቱ ብቻ" : "Admin Panel | Only Yonatan Dawit Mengistu";
    }
    document.querySelectorAll(".lang-btn").forEach(btn => {
        btn.addEventListener("click", () => {
            currentLang = btn.getAttribute("data-lang");
            document.querySelectorAll(".lang-btn").forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            updateLanguage();
        });
    });
    
    // ---------- PROFILE PHOTO MODAL (simple) ----------
    document.getElementById("profilePhotoBtn").addEventListener("click", () => {
        alert("👨‍⚖️ ዮናታን ዳዊት መንግስቱ | Yonatan Dawit Mengistu\n⚖️ የህግ ባለሞያ / Legal Expert");
    });
    
    // ---------- ADMIN LOGIN (yonatan dawit password) ----------
    let isAdmin = false;
    function checkAdmin() {
        let pwd = prompt("የአስተዳዳሪ ይለፍ ቃል ያስገቡ (Admin password):");
        if(pwd === "yonatan2025") {
            isAdmin = true;
            document.getElementById("adminPanel").classList.add("show");
        } else if(pwd !== null) alert("የይለፍ ቃል ተሳስቷል / Incorrect password");
    }
    setTimeout(() => { checkAdmin(); }, 500);
    document.getElementById("logoutAdminBtn")?.addEventListener("click", () => {
        isAdmin = false;
        document.getElementById("adminPanel").classList.remove("show");
    });
    
    // ---------- MEDIA LIBRARY (documents/videos/images/audio) - dynamic ----------
    let mediaItems = [
        { id:1, type:"document", title:"የወንጀል ህግ ቁ.1", url:"#", desc:"የኢትዮጵያ ወንጀል ህግ ሰነድ" },
        { id:2, type:"video", title:"የውል ህግ ትምህርት", url:"https://www.youtube.com/embed/dQw4w9WgXcQ", desc:"ቪዲዮ ማብራሪያ" },
        { id:3, type:"image", title:"የንግድ ህግ ማጠቃለያ", url:"https://picsum.photos/id/1/200/150", desc:"ምስላዊ ማብራሪያ" },
        { id:4, type:"audio", title:"የወንጀል ህግ ንባብ", url:"https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3", desc:"ድምጽ ቅጂ" }
    ];
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
            let contentHtml = "";
            if(item.type === "document") contentHtml = `<i class="fas fa-file-pdf" style="font-size:2rem;"></i><h4>${item.title}</h4><p>${item.desc}</p><a href="${item.url}" target="_blank">ክፈት ሰነድ</a>`;
            else if(item.type === "video") contentHtml = `<i class="fas fa-video"></i><h4>${item.title}</h4><iframe width="100%" height="150" src="${item.url}" frameborder="0"></iframe>`;
            else if(item.type === "image") contentHtml = `<img src="${item.url}" width="100%" style="border-radius:12px;"><h4>${item.title}</h4>`;
            else if(item.type === "audio") contentHtml = `<i class="fas fa-headphones"></i><h4>${item.title}</h4><audio controls src="${item.url}" style="width:100%"></audio>`;
            card.innerHTML = contentHtml;
            grid.appendChild(card);
        });
    }
    document.getElementById("addContentBtn")?.addEventListener("click", () => {
        if(!isAdmin) { alert("አስተዳዳሪ ብቻ መጨመር ይችላሉ!"); return; }
        const title = document.getElementById("newDocTitle").value;
        const type = document.getElementById("docTypeSelect").value;
        if(!title) { alert("ርዕስ ያስፈልጋል"); return; }
        let demoUrl = "#";
        if(type === "video") demoUrl = "https://www.youtube.com/embed/dQw4w9WgXcQ";
        if(type === "image") demoUrl = "https://picsum.photos/id/20/200/150";
        if(type === "audio") demoUrl = "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3";
        mediaItems.push({ id: Date.now(), type: type, title: title, url: demoUrl, desc: "አዲስ ይዘት" });
        renderMedia();
        document.getElementById("newDocTitle").value = "";
    });
    
    // ---------- CONSULTATION MODAL ----------
    const consultModal = document.getElementById("consultModal");
    document.getElementById("consultBtn")?.addEventListener("click", () => consultModal.style.display = "flex");
    document.getElementById("closeModalBtn")?.addEventListener("click", () => consultModal.style.display = "none");
    document.getElementById("sendConsultBtn")?.addEventListener("click", () => {
        const msg = document.getElementById("consultQuestion").value;
        if(msg) alert(`ማማከር ጥያቄ ተልኳል። በቅርቡ እንመልሳለን።\nQuestion: ${msg}`);
        else alert("እባክዎ ጥያቄ ይጻፉ");
        consultModal.style.display = "none";
    });
    
    // ---------- TRAINING BUTTON ----------
    document.getElementById("trainingsBtn")?.addEventListener("click", () => {
        alert(currentLang === "am" ? "ቋሚ ስልጠናዎች፡ በወንጀል፣ ንግድ፣ ውል ህግ ላይ ዝርዝር ስልጠና በቅርቡ ይጀምራል። ለበለጠ መረጃ በቴሌግራም ይመዝገቡ።" : "Permanent trainings on Criminal, Commercial, Contract law will start soon. Join Telegram for updates.");
    });
    
    // ---------- SUPREME COURT RULINGS (payment simulation + search) ----------
    let rulingsAccess = false;
    const sampleRulings = [
        { id:1, category:"የወንጀል ህግ", caseNumber:"ሰበር 101/2012", summary:"የህይወት እስራት ውሳኔ", fileRef:"ፋይል ቁጥር ሰ/ሰ/101" },
        { id:2, category:"የንግድ ህግ", caseNumber:"ሰበር 45/2018", summary:"የንግድ ውል አለመፈጸም", fileRef:"ፋይል ቁጥር ን/45/2018" },
        { id:3, category:"የውል ህግ", caseNumber:"ሰበር 22/2020", summary:"የኪራይ ውል አለመከበር", fileRef:"ውል 22/2020" }
    ];
    document.getElementById("purchaseRulingAccessBtn")?.addEventListener("click", () => {
        if(confirm(currentLang === "am" ? "500 ብር ለውሳኔዎች መዳረሻ ይክፈላሉ። ከተከፈለ በኋላ ፍለጋ ይከፈታል። ክፍያ ከተጠቀሱት አማራጮች መክፈል ይችላሉ። መፈለግ ይፈልጋሉ?" : "Pay 500 ETB to access rulings. You can pay via listed options. Proceed?")) {
            rulingsAccess = true;
            document.getElementById("rulingSearchArea").style.display = "block";
            alert("አመሰግናለሁ! አሁን የሰበር ውሳኔዎችን መፈለግ ይችላሉ።");
        }
    });
    function searchRulings() {
        if(!rulingsAccess) { alert("እባክዎ በመጀመሪያ 500 ብር ከፍለው መዳረሻ ይግዙ"); return; }
        const category = document.getElementById("lawCategoryFilter").value;
        const query = document.getElementById("searchRulingInput").value.toLowerCase();
        let filtered = sampleRulings.filter(r => (category === "all" || r.category === category) && (r.caseNumber.toLowerCase().includes(query) || r.summary.toLowerCase().includes(query)));
        const resultsDiv = document.getElementById("rulingResults");
        if(filtered.length === 0) { resultsDiv.innerHTML = "<p>ምንም ውጤት አልተገኘም / No results</p>"; return; }
        resultsDiv.innerHTML = filtered.map(r => `<div style="border-bottom:1px solid #cbd5e1; padding:0.5rem;"><strong>${r.caseNumber}</strong> (${r.category})<br>${r.summary}<br><small>ፋይል ቁጥር: ${r.fileRef}</small></div>`).join("");
    }
    document.getElementById("searchRulingBtn")?.addEventListener("click", searchRulings);
    document.getElementById("viewMediaBtn")?.addEventListener("click", () => {
        document.getElementById("mediaLibrarySection").scrollIntoView({ behavior: "smooth" });
    });
    
    renderMedia();
    updateLanguage();
</script>
</body>
</html>
