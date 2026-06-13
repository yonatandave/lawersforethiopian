<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>የህግ ባለሞያ ለኢትዮጵያ | Legal Expert Ethiopia</title>
    <!-- Font Awesome & Google Fonts -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #fef9e8;
            color: #2c2418;
            line-height: 1.5;
        }

        /* Ethiopian traditional accent */
        :root {
            --primary: #9e2a2b;
            --primary-dark: #7f1e1f;
            --secondary: #d4a373;
            --light-bg: #fff7ed;
            --card-bg: #ffffff;
            --border: #e2d5c0;
            --shadow: 0 8px 20px rgba(0,0,0,0.05);
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* header */
        header {
            background: white;
            box-shadow: 0 2px 12px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .header-inner {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            padding: 16px 0;
            gap: 16px;
        }
        .logo h1 {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        .logo p {
            font-size: 0.75rem;
            color: #5e4b3a;
        }
        .lang-switch {
            display: flex;
            gap: 12px;
            background: #f0e7db;
            padding: 6px 12px;
            border-radius: 40px;
        }
        .lang-btn {
            background: none;
            border: none;
            font-weight: 600;
            cursor: pointer;
            padding: 6px 14px;
            border-radius: 30px;
            transition: 0.2s;
        }
        .lang-btn.active {
            background: var(--primary);
            color: white;
        }
        .profile-photo {
            cursor: pointer;
            width: 48px;
            height: 48px;
            border-radius: 50%;
            background: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            border: 2px solid var(--primary);
        }
        .profile-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        nav {
            background: white;
            border-top: 1px solid var(--border);
            border-bottom: 1px solid var(--border);
        }
        .nav-links {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            padding: 12px 0;
        }
        .nav-links button {
            background: none;
            border: none;
            padding: 8px 16px;
            font-weight: 500;
            cursor: pointer;
            border-radius: 30px;
            transition: 0.2s;
        }
        .nav-links button:hover, .nav-links button.active-tab {
            background: var(--primary);
            color: white;
        }
        .section {
            display: none;
            margin: 40px 0;
        }
        .section.active-section {
            display: block;
        }
        .card {
            background: var(--card-bg);
            border-radius: 24px;
            padding: 24px;
            box-shadow: var(--shadow);
            border: 1px solid var(--border);
            margin-bottom: 24px;
        }
        .grid-2, .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 24px;
        }
        .btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 8px 20px;
            border-radius: 40px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
        }
        .btn-outline {
            background: transparent;
            border: 1px solid var(--primary);
            color: var(--primary);
        }
        .admin-badge {
            background: #f5c6a0;
            padding: 4px 12px;
            border-radius: 30px;
            font-size: 0.75rem;
        }
        input, select, textarea {
            width: 100%;
            padding: 10px;
            border-radius: 16px;
            border: 1px solid var(--border);
            margin-top: 6px;
            margin-bottom: 14px;
        }
        .modal {
            display: none;
            position: fixed;
            top:0;left:0; width:100%;height:100%;
            background: rgba(0,0,0,0.6);
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }
        .modal-content {
            background: white;
            max-width: 500px;
            width: 90%;
            border-radius: 28px;
            padding: 28px;
        }
        .payment-options {
            display: flex;
            gap: 16px;
            margin: 20px 0;
        }
        .payment-options label {
            display: flex;
            align-items: center;
            gap: 6px;
        }
        footer {
            background: #2c2418;
            color: #d9c7a7;
            padding: 32px 0;
            margin-top: 40px;
            text-align: center;
        }
        @media (max-width: 700px) {
            .header-inner { flex-direction: column; text-align: center; }
            .nav-links { justify-content: center; }
        }
    </style>
</head>
<body>

<header>
    <div class="container">
        <div class="header-inner">
            <div class="logo">
                <h1 data-en="Legal Expert for Ethiopia" data-am="የህግ ባለሞያ ለኢትዮጵያ">የህግ ባለሞያ ለኢትዮጵያ</h1>
                <p data-en="Justice & Legal Resources" data-am="ፍትህ እና የህግ መረጃዎች">ፍትህ እና የህግ መረጃዎች</p>
            </div>
            <div class="lang-switch">
                <button class="lang-btn active" data-lang="am">አማርኛ</button>
                <button class="lang-btn" data-lang="en">English</button>
            </div>
            <div class="profile-photo" id="profilePhotoBtn">
                <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="profile">
            </div>
        </div>
    </div>
    <nav>
        <div class="container">
            <div class="nav-links">
                <button data-tab="home" class="active-tab"><span data-en="Home" data-am="መነሻ">መነሻ</span></button>
                <button data-tab="laws"><span data-en="Laws Library" data-am="የህግ ቤተ መጻህፍት">የህግ ቤተ መጻህፍት</span></button>
                <button data-tab="consult"><span data-en="Consultation" data-am="ህጋዊ ማማከር">ህጋዊ ማማከር</span></button>
                <button data-tab="training"><span data-en="Trainings" data-am="ስልጠናዎች">ስልጠናዎች</span></button>
                <button data-tab="decisions"><span data-en="Court Decisions" data-am="የሰበር ውሳኔዎች">የሰበር ውሳኔዎች</span></button>
                <button data-tab="membership"><span data-en="Membership" data-am="አባልነት">አባልነት</span></button>
                <button data-tab="admin"><span data-en="Admin" data-am="አስተዳዳሪ">አስተዳዳሪ</span></button>
            </div>
        </div>
    </nav>
</header>

<main class="container">
    <!-- HOME -->
    <div id="home" class="section active-section">
        <div class="card">
            <h2 data-en="Welcome to Legal Expert Ethiopia" data-am="እንኳን ወደ የህግ ባለሞያ ኢትዮጵያ በደህና መጡ">እንኳን ወደ የህግ ባለሞያ ኢትዮጵያ በደህና መጡ</h2>
            <p data-en="Your trusted platform for Ethiopian laws, training, and legal consultation. Access criminal, commercial, contract laws, and more." data-am="የኢትዮጵያ ህጎች፣ ስልጠናዎች እና ህጋዊ ማማከር አስተማማኝ መድረክ። የወንጀል፣ የንግድ፣ የውል ህጎችን እና ሌሎችን ይድረሱ።">
            የኢትዮጵያ ህጎች፣ ስልጠናዎች እና ህጋዊ ማማከር አስተማማኝ መድረክ። የወንጀል፣ የንግድ፣ የውል ህጎችን እና ሌሎችን ይድረሱ።
            </p>
            <div style="margin-top: 20px;">
                <i class="fas fa-gavel"></i> <span data-en="Criminal, Commercial, Contract Law & more" data-am="የወንጀል፣ የንግድ፣ የውል ህግ እና ሌሎች">የወንጀል፣ የንግድ፣ የውል ህግ እና ሌሎች</span>
            </div>
        </div>
        <div class="card">
            <h3 data-en="Social Media & Resources" data-am="ማህበራዊ ሚዲያ እና ሃብቶች">ማህበራዊ ሚዲያ እና ሃብቶች</h3>
            <div style="display: flex; gap: 20px; margin-top: 12px;">
                <a href="#" id="fbLink" target="_blank"><i class="fab fa-facebook fa-2x"></i> Facebook</a>
                <a href="#" id="telegramLink" target="_blank"><i class="fab fa-telegram fa-2x"></i> Telegram</a>
                <a href="#" id="youtubeLink" target="_blank"><i class="fab fa-youtube fa-2x"></i> YouTube</a>
                <a href="#" id="linkedinLink" target="_blank"><i class="fab fa-linkedin fa-2x"></i> LinkedIn</a>
            </div>
        </div>
    </div>

    <!-- LAWS LIBRARY (documents, videos, images, audio) -->
    <div id="laws" class="section">
        <div class="card">
            <h2 data-en="Ethiopian Laws - Multimedia Library" data-am="የኢትዮጵያ ህጎች - መልቲሚዲያ ቤተ መጻህፍት">የኢትዮጵያ ህጎች - መልቲሚዲያ ቤተ መጻህፍት</h2>
            <div style="display: flex; gap: 12px; margin-bottom: 24px;">
                <button class="btn filter-media" data-type="document">📄 Documents</button>
                <button class="btn filter-media" data-type="video">🎥 Videos</button>
                <button class="btn filter-media" data-type="image">🖼️ Images</button>
                <button class="btn filter-media" data-type="audio">🎧 Audio</button>
            </div>
            <div id="mediaGrid" class="grid-3"></div>
        </div>
    </div>

    <!-- CONSULTATION -->
    <div id="consult" class="section">
        <div class="card">
            <h2 data-en="Legal Consultation Service" data-am="የህግ ማማከር አገልግሎት">የህግ ማማከር አገልግሎት</h2>
            <p data-en="Submit your legal question, our team will respond within 48 hours." data-am="የህግ ጥያቄዎን ያስገቡ፣ ቡድናችን በ48 ሰአታት ውስጥ ይመልሳል።">የህግ ጥያቄዎን ያስገቡ፣ ቡድናችን በ48 ሰአታት ውስጥ ይመልሳል።</p>
            <input type="text" id="consultName" placeholder="Your Name / ስም" style="width:100%">
            <textarea id="consultMsg" rows="4" placeholder="Describe your legal issue..."></textarea>
            <button id="sendConsultBtn" class="btn">Send Request / ላክ</button>
            <div id="consultFeedback" style="margin-top:12px;"></div>
        </div>
    </div>

    <!-- TRAININGS -->
    <div id="training" class="section">
        <div class="card">
            <h2 data-en="Permanent Law Trainings" data-am="ቋሚ የህግ ስልጠናዎች">ቋሚ የህግ ስልጠናዎች</h2>
            <div id="trainingList" class="grid-2"></div>
            <button id="registerTrainingBtn" class="btn-outline btn" style="margin-top: 20px;"><span data-en="Register for Training" data-am="ለስልጠና ይመዝገቡ">ለስልጠና ይመዝገቡ</span></button>
        </div>
    </div>

    <!-- COURT DECISIONS (pay per view) -->
    <div id="decisions" class="section">
        <div class="card">
            <h2 data-en="Federal Supreme Court Cassation Decisions" data-am="የሰበር ሰሚ ችሎት ውሳኔዎች">የሰበር ሰሚ ችሎት ውሳኔዎች</h2>
            <div style="display: flex; gap: 16px; flex-wrap: wrap;">
                <select id="lawTypeFilter"><option value="all">All / ሁሉም</option><option value="criminal">Criminal</option><option value="commercial">Commercial</option><option value="civil">Civil</option></select>
                <select id="fieldFilter"><option value="all">All Fields</option><option value="contract">Contract</option><option value="property">Property</option><option value="family">Family</option></select>
                <button id="searchDecisionsBtn" class="btn">Search / ፈልግ</button>
            </div>
            <div id="decisionsList" style="margin-top: 28px;"></div>
        </div>
    </div>

    <!-- MEMBERSHIP (join conditions) -->
    <div id="membership" class="section">
        <div class="card">
            <h2 data-en="Join Our Legal Community" data-am="የህግ ማህበረሰባችንን ይቀላቀሉ">የህግ ማህበረሰባችንን ይቀላቀሉ</h2>
            <div><strong data-en="Prerequisites / ቅድመ ሁኔታዎች" data-am="ቅድመ ሁኔታዎች">ቅድመ ሁኔታዎች</strong>
                <ul><li data-en="Must be law student, legal professional, or justice seeker" data-am="የህግ ተማሪ፣ ህግ ባለሞያ ወይም ፍትህ ፈላጊ መሆን አለበት።">የህግ ተማሪ፣ ህግ ባለሞያ ወይም ፍትህ ፈላጊ መሆን አለበት።</li>
                <li data-en="Accept community guidelines" data-am="የማህበረሰብ መመሪያዎችን መቀበል">የማህበረሰብ መመሪያዎችን መቀበል</li>
                <li data-en="Register with full name and email" data-am="በሙሉ ስም እና ኢሜይል መመዝገብ">በሙሉ ስም እና ኢሜይል መመዝገብ</li></ul>
            </div>
            <input type="text" id="memberName" placeholder="Full Name"><input type="email" id="memberEmail" placeholder="Email"><button id="joinMemberBtn" class="btn">Join / ተቀላቀል</button>
            <div id="memberMsg"></div>
        </div>
    </div>

    <!-- ADMIN PANEL -->
    <div id="admin" class="section">
        <div class="card">
            <h3 data-en="Admin Access - Yonatan Dawit Mengistu" data-am="የአስተዳዳሪ መግቢያ - ዮናታን ዳዊት መንግስቱ">የአስተዳዳሪ መግቢያ - ዮናታን ዳዊት መንግስቱ</h3>
            <div id="adminLoginArea">
                <input type="password" id="adminPass" placeholder="Password / የይለፍ ቃል">
                <button id="adminLoginBtn" class="btn">Login</button>
            </div>
            <div id="adminPanel" style="display:none;">
                <h4>➕ Add Law (Doc/Video/Image/Audio)</h4>
                <input type="text" id="lawTitle" placeholder="Title"><select id="lawTypeMedia"><option value="document">Document</option><option value="video">Video</option><option value="image">Image</option><option value="audio">Audio</option></select>
                <input type="text" id="lawUrl" placeholder="Media URL (YouTube/PDF/Image/Audio link)"><button id="addLawBtn" class="btn">Add Law</button>
                <hr><h4>📚 Add Training</h4><input id="trainName" placeholder="Training name"><input id="trainDate" placeholder="Date / Duration"><button id="addTrainingBtn">Add Training</button>
                <hr><h4>⚖️ Add Cassation Decision</h4><input id="decCaseName" placeholder="Case Name"><input id="decFileNum" placeholder="File Number"><select id="decLawType"><option value="criminal">Criminal</option><option value="commercial">Commercial</option><option value="civil">Civil</option></select><select id="decField"><option value="contract">Contract</option><option value="property">Property</option><option value="family">Family</option></select><textarea id="decSummary" placeholder="Full summary (pay to view)"></textarea><button id="addDecisionBtn">Add Decision (Price 500 ETB)</button>
                <p class="admin-badge" style="margin-top:16px;">Admin: Yonatan Dawit Mengistu</p>
            </div>
        </div>
    </div>
</main>
<footer><div class="container">© 2025 የህግ ባለሞያ ለኢትዮጵያ | Empowering Justice</div></footer>

<!-- Profile Modal -->
<div id="profileModal" class="modal">
    <div class="modal-content">
        <span style="float:right;cursor:pointer;" id="closeModal">&times;</span>
        <h3>ዮናታን ዳዊት መንግስቱ</h3>
        <p data-en="Founder & Legal Expert | Supreme Court advocate" data-am="መስራች እና የህግ ባለሞያ | የሰበር ተሟጋች">መስራች እና የህግ ባለሞያ | የሰበር ተሟጋች</p>
        <p data-en="Admin of this platform, dedicated to accessible Ethiopian law." data-am="የዚህ መድረክ አስተዳዳሪ፣ ተደራሽ የኢትዮጵያ ህግ ለማቅረብ ቁርጠኛ">የዚህ መድረክ አስተዳዳሪ፣ ተደራሽ የኢትዮጵያ ህግ ለማቅረብ ቁርጠኛ</p>
    </div>
</div>

<script>
    // ---- DATA STORES (localStorage) ----
    let laws = JSON.parse(localStorage.getItem('ethioLaws')) || [
        { id:1, title:"የወንጀል ህግ ቁጥር 1", type:"document", url:"https://www.wipo.int/wipolex/am/text/221210", desc:"የኢፌድሪ ወንጀል ህግ ሰነድ"},
        { id:2, title:"የንግድ ህግ ማብራሪያ ቪዲዮ", type:"video", url:"https://www.youtube.com/embed/dQw4w9WgXcQ", desc:"Commercial law overview"},
        { id:3, title:"የውል ህግ መሰረታዊ ምስል", type:"image", url:"https://picsum.photos/id/104/300/200", desc:"Contract law infographic"},
        { id:4, title:"የህግ ንግግር ኦዲዮ", type:"audio", url:"https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3", desc:"Legal audio explanation"}
    ];
    let trainings = JSON.parse(localStorage.getItem('ethioTrainings')) || [
        { id:1, name:"የወንጀል ህግ ስልጠና", date:"March 20-25, 2025" },
        { id:2, name:"የንግድ ህግ ውድድር", date:"April 10-12" }
    ];
    let decisions = JSON.parse(localStorage.getItem('ethioDecisions')) || [
        { id:1, caseName:"የሰበር ውሳኔ 12/2012", fileNumber:"FSC/1234", lawType:"criminal", field:"contract", summary:"በወንጀል ጉዳይ የሰበር ችሎት ውሳኔ የቅጣት መጠን ቀንሷል", price:500 },
        { id:2, caseName:"የንግድ ውል ውሳኔ", fileNumber:"FSC/5678", lawType:"commercial", field:"contract", summary:"የንግድ ውል አለመፈጸም ላይ የሰበር ውሳኔ", price:500 }
    ];
    let purchasedDecisions = JSON.parse(localStorage.getItem('purchasedDecisions')) || [];

    function saveAll() {
        localStorage.setItem('ethioLaws', JSON.stringify(laws));
        localStorage.setItem('ethioTrainings', JSON.stringify(trainings));
        localStorage.setItem('ethioDecisions', JSON.stringify(decisions));
        localStorage.setItem('purchasedDecisions', JSON.stringify(purchasedDecisions));
    }

    // UI rendering
    function renderMedia(filterType="document") {
        const filtered = laws.filter(l => l.type === filterType);
        const grid = document.getElementById("mediaGrid");
        grid.innerHTML = filtered.map(l => `<div class="card" style="margin:0">
            <strong>${l.title}</strong><br>
            ${l.type==='document'? `<a href="${l.url}" target="_blank">📄 Open Document</a>`:''}
            ${l.type==='video'? `<iframe width="100%" height="180" src="${l.url}" frameborder="0"></iframe>`:''}
            ${l.type==='image'? `<img src="${l.url}" width="100%" style="border-radius:12px">`:''}
            ${l.type==='audio'? `<audio controls src="${l.url}" style="width:100%"></audio>`:''}
            <p>${l.desc || ''}</p>
        </div>`).join('');
    }

    function renderTrainings() {
        const container = document.getElementById("trainingList");
        container.innerHTML = trainings.map(t => `<div class="card"><h4>${t.name}</h4><p>${t.date}</p><button class="btn-outline btn trainingRegisterBtn" data-name="${t.name}">Register</button></div>`).join('');
    }

    function renderDecisions(filterLaw="all", filterField="all") {
        let filtered = decisions.filter(d => (filterLaw==="all" || d.lawType===filterLaw) && (filterField==="all" || d.field===filterField));
        const container = document.getElementById("decisionsList");
        if(filtered.length===0){ container.innerHTML="<p>No decisions found</p>"; return; }
        container.innerHTML = filtered.map(d => {
            const purchased = purchasedDecisions.includes(d.id);
            return `<div class="card"><strong>${d.caseName}</strong> (File: ${d.fileNumber}) <br> Law: ${d.lawType} | Field: ${d.field}<br>
            ${purchased ? `<p><strong>Summary:</strong> ${d.summary}</p>` : `<button class="btn payDecisionBtn" data-id="${d.id}" data-price="500">🔓 Pay 500 ETB to view summary</button>`}
            </div>`;
        }).join('');
        document.querySelectorAll('.payDecisionBtn').forEach(btn => btn.addEventListener('click', (e) => {
            let id = parseInt(btn.dataset.id);
            showPaymentModal(id);
        }));
    }

    let paymentCallback = null;
    function showPaymentModal(decisionId) {
        const modal = document.createElement('div'); modal.className='modal'; modal.style.display='flex';
        modal.innerHTML = `<div class="modal-content"><h3>Select Payment Method</h3><div class="payment-options">
        <label><input type="radio" name="payMethod" value="cbe"> ንግድ ባንክ (CBE)</label>
        <label><input type="radio" name="payMethod" value="cbebirr"> CBE ብር</label>
        <label><input type="radio" name="payMethod" value="telebirr"> ቴሌ ብር</label>
        </div><button id="confirmPayBtn" class="btn">Confirm Payment 500 ETB</button><button id="cancelPayModal">Cancel</button></div>`;
        document.body.appendChild(modal);
        document.getElementById('confirmPayBtn').onclick = () => {
            const selected = document.querySelector('input[name="payMethod"]:checked');
            if(selected) {
                if(!purchasedDecisions.includes(decisionId)) purchasedDecisions.push(decisionId);
                saveAll();
                alert(`✅ Payment successful via ${selected.value}. Summary unlocked!`);
                renderDecisions(document.getElementById("lawTypeFilter").value, document.getElementById("fieldFilter").value);
                modal.remove();
            } else alert("Please select payment option");
        };
        document.getElementById('cancelPayModal').onclick = () => modal.remove();
    }

    // Admin
    let adminLogged = false;
    document.getElementById("adminLoginBtn").onclick = () => {
        let pwd = document.getElementById("adminPass").value;
        if(pwd === "yonatan2025") { adminLogged=true; document.getElementById("adminPanel").style.display="block"; document.getElementById("adminLoginArea").style.display="none"; alert("Welcome Admin Yonatan"); }
        else alert("Invalid password");
    };
    document.getElementById("addLawBtn").onclick = () => {
        let newLaw = { id:Date.now(), title:document.getElementById("lawTitle").value, type:document.getElementById("lawTypeMedia").value, url:document.getElementById("lawUrl").value, desc:"Added by admin" };
        laws.push(newLaw); saveAll(); renderMedia("document"); alert("Law added");
    };
    document.getElementById("addTrainingBtn").onclick = () => {
        trainings.push({ id:Date.now(), name:document.getElementById("trainName").value, date:document.getElementById("trainDate").value });
        saveAll(); renderTrainings();
    };
    document.getElementById("addDecisionBtn").onclick = () => {
        let newDec = { id:Date.now(), caseName:document.getElementById("decCaseName").value, fileNumber:document.getElementById("decFileNum").value, lawType:document.getElementById("decLawType").value, field:document.getElementById("decField").value, summary:document.getElementById("decSummary").value, price:500 };
        decisions.push(newDec); saveAll(); renderDecisions("all","all");
    };

    // Language switch + dynamic text
    let currentLang = 'am';
    function translatePage() {
        document.querySelectorAll('[data-en][data-am]').forEach(el => {
            if(currentLang === 'am') el.innerText = el.getAttribute('data-am');
            else el.innerText = el.getAttribute('data-en');
        });
        document.querySelectorAll('[data-en]').forEach(el => { if(!el.hasAttribute('data-am')) el.innerText = currentLang==='am'?el.innerText:el.getAttribute('data-en'); });
    }
    document.querySelectorAll('.lang-btn').forEach(btn => btn.onclick = () => { currentLang = btn.dataset.lang; document.querySelectorAll('.lang-btn').forEach(b=>b.classList.remove('active')); btn.classList.add('active'); translatePage(); });
    
    // Tab switching
    document.querySelectorAll('[data-tab]').forEach(btn => {
        btn.onclick = () => {
            document.querySelectorAll('.section').forEach(s=>s.classList.remove('active-section'));
            document.getElementById(btn.dataset.tab).classList.add('active-section');
            document.querySelectorAll('[data-tab]').forEach(b=>b.classList.remove('active-tab'));
            btn.classList.add('active-tab');
            if(btn.dataset.tab === 'laws') renderMedia('document');
            if(btn.dataset.tab === 'training') renderTrainings();
            if(btn.dataset.tab === 'decisions') renderDecisions('all','all');
        };
    });
    document.querySelectorAll('.filter-media').forEach(btn => btn.onclick = (e) => renderMedia(btn.dataset.type));
    document.getElementById("searchDecisionsBtn").onclick = () => renderDecisions(document.getElementById("lawTypeFilter").value, document.getElementById("fieldFilter").value);
    document.getElementById("sendConsultBtn").onclick = () => { document.getElementById("consultFeedback").innerHTML = "<span style='color:green'>Request sent! We'll contact you.</span>"; };
    document.getElementById("joinMemberBtn").onclick = () => { localStorage.setItem('member_'+Date.now(), document.getElementById("memberName").value); alert("Membership request received! Welcome."); };
    document.getElementById("registerTrainingBtn").onclick = () => alert("Registration form will be sent to your email. Thanks!");
    document.getElementById("profilePhotoBtn").onclick = () => document.getElementById("profileModal").style.display = "flex";
    document.getElementById("closeModal").onclick = () => document.getElementById("profileModal").style.display = "none";
    window.onclick = (e) => { if(e.target===document.getElementById("profileModal")) document.getElementById("profileModal").style.display="none"; };
    // Social media placeholder links
    document.getElementById("fbLink").href="https://facebook.com"; document.getElementById("telegramLink").href="https://t.me"; document.getElementById("youtubeLink").href="https://youtube.com"; document.getElementById("linkedinLink").href="https://linkedin.com";
    // initial renders
    renderMedia('document'); renderTrainings(); renderDecisions('all','all'); translatePage();
    // also add training register dynamic
    setInterval(()=>{ document.querySelectorAll('.trainingRegisterBtn').forEach(btn=>btn.onclick = ()=> alert(`Registered for ${btn.dataset.name}`)); },500);
    saveAll();
</script>
</body>
</html>
