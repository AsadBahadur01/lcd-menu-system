<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>LUXE LCD | Premium Menu Display System</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            user-select: none;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #000;
            overflow: hidden;
        }

        /* ========== LCD MAIN DISPLAY (CUSTOMER SIDE) ========== */
        .lcd-stage {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, #0a0a0a 0%, #000000 100%);
            z-index: 1;
        }

        .media-wrapper {
            width: 100%;
            height: 100%;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Image with Ken Burns effect */
        .menu-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
            opacity: 0;
            transition: opacity 1.2s cubic-bezier(0.4, 0, 0.2, 1);
            filter: brightness(1.02) contrast(1.02);
        }

        .menu-image.active {
            opacity: 1;
            z-index: 2;
        }

        /* Video element */
        .menu-video {
            width: 100%;
            height: 100%;
            object-fit: cover;
            position: absolute;
            top: 0;
            left: 0;
            opacity: 0;
            transition: opacity 0.8s ease;
        }

        .menu-video.active {
            opacity: 1;
            z-index: 2;
        }

        /* Animated overlay gradient (cinematic) */
        .cinematic-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            height: 30%;
            background: linear-gradient(to top, rgba(0,0,0,0.6) 0%, transparent 100%);
            z-index: 5;
            pointer-events: none;
        }

        /* Optional time/date (very subtle) */
        .time-overlay {
            position: absolute;
            bottom: 20px;
            right: 30px;
            color: rgba(255,255,255,0.5);
            font-size: 13px;
            font-weight: 400;
            letter-spacing: 1px;
            z-index: 6;
            font-family: monospace;
            backdrop-filter: blur(4px);
            padding: 6px 14px;
            border-radius: 40px;
            background: rgba(0,0,0,0.3);
            pointer-events: none;
        }

        /* Loading placeholder */
        .loading-placeholder {
            position: absolute;
            color: rgba(255,255,255,0.3);
            font-size: 14px;
            letter-spacing: 2px;
            z-index: 1;
        }

        /* NO BUTTONS — completely hidden */
        .hidden-controls {
            display: none;
        }

        /* ========== ADMIN LOGIN (Double Right Click) ========== */
        .admin-login-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.96);
            backdrop-filter: blur(24px);
            z-index: 2000;
            display: none;
            align-items: center;
            justify-content: center;
            animation: fadeIn 0.2s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .login-container {
            background: rgba(20,20,35,0.9);
            border: 1px solid rgba(255,255,255,0.15);
            border-radius: 32px;
            padding: 40px;
            width: 420px;
            text-align: center;
            backdrop-filter: blur(20px);
            box-shadow: 0 30px 50px rgba(0,0,0,0.5);
        }

        .login-container h2 {
            color: #fff;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .login-container p {
            color: #aaa;
            font-size: 14px;
            margin-bottom: 25px;
        }

        .login-container input {
            width: 100%;
            padding: 14px 16px;
            background: rgba(255,255,255,0.08);
            border: 1px solid rgba(255,255,255,0.2);
            border-radius: 60px;
            color: white;
            font-size: 15px;
            margin-bottom: 20px;
            outline: none;
            transition: 0.2s;
        }

        .login-container input:focus {
            border-color: #a855f7;
            background: rgba(255,255,255,0.12);
        }

        .login-container button {
            width: 100%;
            background: linear-gradient(135deg, #8b5cf6, #7c3aed);
            border: none;
            padding: 14px;
            border-radius: 60px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            font-size: 15px;
            transition: 0.2s;
        }

        .login-container button:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 20px rgba(139,92,246,0.4);
        }

        .close-login {
            position: absolute;
            top: 24px;
            right: 24px;
            background: rgba(255,255,255,0.1);
            border: none;
            color: white;
            width: 42px;
            height: 42px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 18px;
        }

        /* ========== PROFESSIONAL ADMIN PANEL (SLICK) ========== */
        .admin-panel-pro {
            position: fixed;
            top: 0;
            right: -650px;
            width: 650px;
            height: 100vh;
            background: #0b0b15;
            z-index: 3000;
            transition: right 0.35s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            box-shadow: -8px 0 32px rgba(0,0,0,0.6);
            overflow-y: auto;
            border-left: 1px solid rgba(255,255,255,0.08);
        }

        .admin-panel-pro.open {
            right: 0;
        }

        /* Admin Header */
        .admin-header-pro {
            background: linear-gradient(135deg, #0f0f1a, #1a1a2e);
            padding: 32px 28px;
            border-bottom: 1px solid rgba(255,255,255,0.08);
        }

        .admin-header-pro h1 {
            color: white;
            font-size: 26px;
            font-weight: 600;
            letter-spacing: -0.3px;
        }

        .admin-header-pro p {
            color: #8b8b9e;
            font-size: 13px;
            margin-top: 6px;
        }

        .close-admin-pro {
            position: absolute;
            top: 24px;
            right: 24px;
            background: rgba(255,255,255,0.08);
            border: none;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
        }

        /* Stats Cards */
        .stats-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
            padding: 24px 24px 0 24px;
        }

        .stat-card-pro {
            background: rgba(255,255,255,0.04);
            border-radius: 24px;
            padding: 18px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.05);
        }

        .stat-card-pro i {
            font-size: 32px;
            color: #a855f7;
            margin-bottom: 8px;
        }

        .stat-number {
            font-size: 32px;
            font-weight: 700;
            color: white;
        }

        .stat-label {
            font-size: 12px;
            color: #8b8b9e;
        }

        /* LCD Info Card */
        .info-card-pro {
            background: rgba(255,255,255,0.04);
            margin: 20px 24px;
            border-radius: 24px;
            padding: 20px;
            border: 1px solid rgba(255,255,255,0.05);
        }

        .info-row-pro {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid rgba(255,255,255,0.06);
        }

        .info-label-pro {
            color: #8b8b9e;
            font-size: 13px;
        }

        .info-value-pro {
            color: white;
            font-weight: 500;
            font-size: 13px;
        }

        .edit-icon {
            background: rgba(255,255,255,0.06);
            border: none;
            color: #a855f7;
            padding: 6px 12px;
            border-radius: 40px;
            cursor: pointer;
            font-size: 12px;
        }

        /* Upload Area (Drag & Drop) */
        .upload-zone {
            background: rgba(255,255,255,0.04);
            margin: 20px 24px;
            border-radius: 24px;
            padding: 24px;
            border: 1px dashed rgba(255,255,255,0.2);
            text-align: center;
            cursor: pointer;
            transition: 0.2s;
        }

        .upload-zone:hover {
            border-color: #a855f7;
            background: rgba(168,85,247,0.08);
        }

        .upload-zone i {
            font-size: 48px;
            color: #a855f7;
            margin-bottom: 12px;
        }

        .upload-hint {
            font-size: 12px;
            color: #6b6b80;
            margin-top: 8px;
        }

        /* Gallery Grid (Professional Masonry Style) */
        .gallery-grid-pro {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 14px;
            padding: 0 24px 24px 24px;
            max-height: 420px;
            overflow-y: auto;
        }

        .gallery-card-pro {
            background: rgba(255,255,255,0.04);
            border-radius: 20px;
            overflow: hidden;
            transition: 0.2s;
            border: 1px solid rgba(255,255,255,0.06);
        }

        .gallery-card-pro:hover {
            transform: translateY(-3px);
            border-color: rgba(168,85,247,0.4);
        }

        .gallery-preview-pro {
            width: 100%;
            height: 110px;
            object-fit: cover;
        }

        .gallery-meta {
            padding: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .badge-type {
            background: rgba(168,85,247,0.2);
            padding: 4px 10px;
            border-radius: 40px;
            font-size: 10px;
            color: #c084fc;
        }

        .action-group {
            display: flex;
            gap: 8px;
        }

        .action-icon {
            background: rgba(255,255,255,0.08);
            border: none;
            width: 30px;
            height: 30px;
            border-radius: 12px;
            cursor: pointer;
            color: white;
        }

        .action-icon.delete:hover {
            background: #ef4444;
        }

        /* Scrollbar */
        .gallery-grid-pro::-webkit-scrollbar {
            width: 5px;
        }
        .gallery-grid-pro::-webkit-scrollbar-track {
            background: #1e1e2e;
        }
        .gallery-grid-pro::-webkit-scrollbar-thumb {
            background: #a855f7;
            border-radius: 10px;
        }

        /* Toast */
        .toast-pro {
            position: fixed;
            bottom: 28px;
            left: 28px;
            background: #1e1e2e;
            backdrop-filter: blur(16px);
            padding: 12px 24px;
            border-radius: 60px;
            color: white;
            z-index: 4000;
            transform: translateX(-120%);
            transition: 0.3s;
            border-left: 3px solid #a855f7;
            font-size: 13px;
        }

        .toast-pro.show {
            transform: translateX(0);
        }
    </style>
</head>
<body>

<!-- LCD FULL SCREEN DISPLAY (NO BUTTONS, NO UI) -->
<div class="lcd-stage" id="lcdStage">
    <div class="media-wrapper">
        <img id="activeImage" class="menu-image" alt="Menu">
        <video id="activeVideo" class="menu-video" loop muted playsinline></video>
        <div class="cinematic-overlay"></div>
        <div class="time-overlay" id="liveTime"></div>
        <div class="loading-placeholder" id="loadingMsg">LUXE MENU • LOADING</div>
    </div>
</div>

<!-- ADMIN LOGIN MODAL -->
<div class="admin-login-modal" id="loginModal">
    <button class="close-login" onclick="closeLoginModal()"><i class="fas fa-times"></i></button>
    <div class="login-container">
        <i class="fas fa-shield-alt" style="font-size: 48px; color: #a855f7; margin-bottom: 16px;"></i>
        <h2>Administrator Access</h2>
        <p>Double right-click detected • Secure login required</p>
        <input type="password" id="adminPasswordInput" placeholder="Enter secure key" autocomplete="off">
        <button onclick="validateAdminLogin()">Unlock Panel <i class="fas fa-arrow-right"></i></button>
        <div style="margin-top: 18px; font-size: 12px; color: #5a5a70;">Default: <span style="color:#a855f7;">admin123</span></div>
    </div>
</div>

<!-- PROFESSIONAL ADMIN PANEL -->
<div class="admin-panel-pro" id="adminPanelPro">
    <div class="admin-header-pro">
        <h1><i class="fas fa-tv-retro"></i> LCD Command Center</h1>
        <p>Menu engineering • Bulk media • Real-time sync</p>
        <button class="close-admin-pro" onclick="closeAdminPanelPro()"><i class="fas fa-times"></i></button>
    </div>

    <!-- Stats -->
    <div class="stats-row">
        <div class="stat-card-pro">
            <i class="fas fa-layer-group"></i>
            <div class="stat-number" id="statTotal">0</div>
            <div class="stat-label">Total Assets</div>
        </div>
        <div class="stat-card-pro">
            <i class="fas fa-clock"></i>
            <div class="stat-number">8s</div>
            <div class="stat-label">Auto Transition</div>
        </div>
    </div>

    <!-- LCD Info -->
    <div class="info-card-pro">
        <div style="display: flex; justify-content: space-between; margin-bottom: 12px;">
            <span style="color:white; font-weight:500;"><i class="fas fa-display"></i> Display Identity</span>
        </div>
        <div class="info-row-pro">
            <span class="info-label-pro">LCD Name</span>
            <span class="info-value-pro" id="displayLcdName">Grand Counter LCD</span>
            <button class="edit-icon" onclick="editLcdNamePro()">Edit</button>
        </div>
        <div class="info-row-pro">
            <span class="info-label-pro">IP / Host</span>
            <span class="info-value-pro" id="displayLcdHost">192.168.1.240</span>
            <button class="edit-icon" onclick="editLcdHostPro()">Edit</button>
        </div>
        <div class="info-row-pro">
            <span class="info-label-pro">Server Endpoint</span>
            <span class="info-value-pro" id="displayServerUrl">localhost:8080</span>
            <button class="edit-icon" onclick="editServerUrlPro()">Edit</button>
        </div>
    </div>

    <!-- Drag & Drop Multi Upload -->
    <div class="upload-zone" id="dragZone">
        <i class="fas fa-cloud-upload-alt"></i>
        <p>Drop images / videos anywhere</p>
        <p class="upload-hint">Supports: JPG, PNG, GIF, MP4, WebM • Bulk upload</p>
        <input type="file" id="bulkFileInput" multiple accept="image/*,video/mp4,video/webm" style="display:none">
        <div style="margin-top: 12px;">
            <button class="edit-icon" onclick="document.getElementById('bulkFileInput').click()" style="background:#a855f7; color:white; border:none; padding:8px 20px;">Select Files</button>
        </div>
    </div>

    <!-- Gallery Section -->
    <div class="info-card-pro" style="margin-top:0;">
        <div style="display: flex; justify-content: space-between;">
            <span style="color:white;"><i class="fas fa-photo-film"></i> Media Library</span>
            <span style="color:#a855f7; font-size:12px;">Manual control only</span>
        </div>
    </div>
    <div class="gallery-grid-pro" id="galleryGridPro">
        <!-- Dynamic gallery -->
    </div>
</div>

<div class="toast-pro" id="toastPro">
    <i class="fas fa-circle-check" style="color:#a855f7; margin-right:8px;"></i>
    <span id="toastProMsg">System online</span>
</div>

<script>
    // ---------- DATA LAYER ----------
    let mediaMaster = [];      // {type, src}
    let currentIndex = 0;
    let slideInterval = null;
    let autoPlayActive = true;
    let activeType = 'image';
    let adminSession = false;
    let sessionTimer = null;

    // LCD Identity
    let lcdIdentity = {
        name: 'Grand Counter LCD',
        host: '192.168.1.240',
        serverUrl: window.location.hostname + ':' + (window.location.port || '80')
    };

    // Load from storage
    function loadMasterData() {
        const storedMedia = localStorage.getItem('luxe_lcd_media');
        if (storedMedia && JSON.parse(storedMedia).length > 0) {
            mediaMaster = JSON.parse(storedMedia);
        } else {
            // Premium default content
            mediaMaster = [
                {type: 'image', src: 'https://images.unsplash.com/photo-1504674900247-0877df9cc836?w=1920&h=1080&fit=crop'},
                {type: 'image', src: 'https://images.unsplash.com/photo-1546069901-ba9599a7e63c?w=1920&h=1080&fit=crop'},
                {type: 'image', src: 'https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=1920&h=1080&fit=crop'}
            ];
            persistMedia();
        }
        
        const storedIdentity = localStorage.getItem('luxe_lcd_identity');
        if (storedIdentity) lcdIdentity = JSON.parse(storedIdentity);
        updateIdentityUI();
        renderProGallery();
        updateTotalStat();
        
        if (mediaMaster.length) renderCurrentMedia(0);
        startAutoTransition();
    }

    function persistMedia() {
        localStorage.setItem('luxe_lcd_media', JSON.stringify(mediaMaster));
        updateTotalStat();
        renderProGallery();
    }

    function updateTotalStat() {
        document.getElementById('statTotal').innerText = mediaMaster.length;
    }

    // Professional media display with crossfade
    function renderCurrentMedia(index) {
        if (!mediaMaster.length) {
            document.getElementById('activeImage').style.display = 'none';
            document.getElementById('activeVideo').style.display = 'none';
            return;
        }
        const item = mediaMaster[index];
        const imgEl = document.getElementById('activeImage');
        const vidEl = document.getElementById('activeVideo');

        if (item.type === 'image') {
            if (vidEl.src) { vidEl.pause(); vidEl.src = ''; }
            vidEl.classList.remove('active');
            imgEl.classList.remove('active');
            setTimeout(() => {
                imgEl.src = item.src;
                imgEl.classList.add('active');
                vidEl.style.display = 'none';
                imgEl.style.display = 'block';
            }, 50);
            activeType = 'image';
        } else {
            imgEl.classList.remove('active');
            vidEl.classList.remove('active');
            setTimeout(() => {
                vidEl.src = item.src;
                vidEl.load();
                vidEl.play().catch(e=>console.log);
                vidEl.classList.add('active');
                imgEl.style.display = 'none';
                vidEl.style.display = 'block';
            }, 50);
            activeType = 'video';
        }
        document.getElementById('loadingMsg').style.opacity = '0';
    }

    function nextSlide() {
        if (!mediaMaster.length) return;
        currentIndex = (currentIndex + 1) % mediaMaster.length;
        renderCurrentMedia(currentIndex);
    }

    function startAutoTransition() {
        if (slideInterval) clearInterval(slideInterval);
        slideInterval = setInterval(() => {
            if (autoPlayActive && mediaMaster.length) nextSlide();
        }, 8000);
    }

    // ---------- BULK UPLOAD (MULTIPLE FILES) ----------
    function processMultipleFiles(files) {
        if (!files.length) return;
        let pending = files.length;
        let added = 0;
        for (let f of files) {
            if (!f.type.startsWith('image/') && !f.type.startsWith('video/')) {
                pending--; continue;
            }
            const reader = new FileReader();
            reader.onload = (e) => {
                const type = f.type.startsWith('image/') ? 'image' : 'video';
                mediaMaster.push({type, src: e.target.result});
                added++;
                if (added === pending) {
                    persistMedia();
                    if (mediaMaster.length === files.length && mediaMaster.length > 0) renderCurrentMedia(0);
                    showProToast(`✅ ${added} media items added`, '#22c55e');
                }
            };
            reader.readAsDataURL(f);
        }
        if (pending === 0) showProToast('No valid files', '#ef4444');
        document.getElementById('bulkFileInput').value = '';
    }

    // Remove media
    function removeMediaPro(idx) {
        if (confirm('Permanently delete this menu asset?')) {
            mediaMaster.splice(idx, 1);
            persistMedia();
            if (!mediaMaster.length) {
                document.getElementById('activeImage').style.display = 'none';
                document.getElementById('activeVideo').style.display = 'none';
            } else {
                if (currentIndex >= mediaMaster.length) currentIndex = mediaMaster.length-1;
                renderCurrentMedia(currentIndex);
            }
            showProToast('Removed from playlist', '#f97316');
        }
    }

    // Edit media (replace)
    function editMediaPro(idx) {
        const input = document.createElement('input');
        input.type = 'file';
        input.accept = mediaMaster[idx].type === 'image' ? 'image/*' : 'video/*';
        input.onchange = (e) => {
            const file = e.target.files[0];
            if (!file) return;
            const reader = new FileReader();
            reader.onload = (ev) => {
                mediaMaster[idx].src = ev.target.result;
                persistMedia();
                if (currentIndex === idx) renderCurrentMedia(currentIndex);
                showProToast('Asset updated', '#3b82f6');
            };
            reader.readAsDataURL(file);
        };
        input.click();
    }

    // Gallery render
    function renderProGallery() {
        const container = document.getElementById('galleryGridPro');
        if (!mediaMaster.length) {
            container.innerHTML = `<div style="grid-column:1/-1; text-align:center; padding:48px; color:#6b6b80;"><i class="fas fa-folder-open" style="font-size:48px; margin-bottom:12px;"></i><p>No menu items</p><p style="font-size:12px;">Upload images/videos</p></div>`;
            return;
        }
        container.innerHTML = mediaMaster.map((item, idx) => `
            <div class="gallery-card-pro">
                ${item.type === 'image' ? 
                    `<img src="${item.src}" class="gallery-preview-pro">` : 
                    `<video src="${item.src}" class="gallery-preview-pro" muted></video>`
                }
                <div class="gallery-meta">
                    <span class="badge-type">${item.type === 'image' ? '📷 PHOTO' : '🎬 VIDEO'}</span>
                    <div class="action-group">
                        <button class="action-icon" onclick="editMediaPro(${idx})"><i class="fas fa-pen"></i></button>
                        <button class="action-icon delete" onclick="removeMediaPro(${idx})"><i class="fas fa-trash"></i></button>
                    </div>
                </div>
            </div>
        `).join('');
    }

    // Identity UI
    function updateIdentityUI() {
        document.getElementById('displayLcdName').innerText = lcdIdentity.name;
        document.getElementById('displayLcdHost').innerText = lcdIdentity.host;
        document.getElementById('displayServerUrl').innerText = lcdIdentity.serverUrl;
    }
    function editLcdNamePro() { let val = prompt('LCD Display Name', lcdIdentity.name); if(val){ lcdIdentity.name=val; localStorage.setItem('luxe_lcd_identity', JSON.stringify(lcdIdentity)); updateIdentityUI(); showProToast('LCD name updated','#22c55e');} }
    function editLcdHostPro() { let val = prompt('IP / Hostname', lcdIdentity.host); if(val){ lcdIdentity.host=val; localStorage.setItem('luxe_lcd_identity', JSON.stringify(lcdIdentity)); updateIdentityUI(); showProToast('IP updated','#22c55e');} }
    function editServerUrlPro() { let val = prompt('Server URL', lcdIdentity.serverUrl); if(val){ lcdIdentity.serverUrl=val; localStorage.setItem('luxe_lcd_identity', JSON.stringify(lcdIdentity)); updateIdentityUI(); showProToast('Server URL set','#22c55e');} }

    // Admin panel + session
    function validateAdminLogin() {
        const pwd = document.getElementById('adminPasswordInput').value;
        if (pwd === 'admin123') {
            adminSession = true;
            closeLoginModal();
            document.getElementById('adminPanelPro').classList.add('open');
            showProToast('Admin access granted', '#a855f7');
            if (sessionTimer) clearTimeout(sessionTimer);
            sessionTimer = setTimeout(() => { if(adminSession){ closeAdminPanelPro(); showProToast('Session expired', '#f97316'); } }, 15*60*1000);
        } else {
            showProToast('Invalid security key', '#ef4444');
        }
        document.getElementById('adminPasswordInput').value = '';
    }
    function closeAdminPanelPro() { document.getElementById('adminPanelPro').classList.remove('open'); adminSession=false; }
    function closeLoginModal() { document.getElementById('loginModal').style.display = 'none'; }

    // Double right-click detection
    let dblClickFlag = null;
    document.getElementById('lcdStage').addEventListener('contextmenu', (e) => {
        e.preventDefault();
        if (dblClickFlag) {
            clearTimeout(dblClickFlag);
            dblClickFlag = null;
            document.getElementById('loginModal').style.display = 'flex';
        } else {
            dblClickFlag = setTimeout(() => { dblClickFlag = null; }, 280);
        }
    });

    // Fullscreen via keyboard (only for admin)
    document.addEventListener('keydown', (e) => {
        if (e.key === 'F11') { e.preventDefault(); if (!document.fullscreenElement) document.documentElement.requestFullscreen(); else document.exitFullscreen(); }
        if (e.key === 'ArrowRight' && adminSession) { nextSlide(); showProToast('Next slide', '#3b82f6'); }
        if (e.key === 'ArrowLeft' && adminSession) { currentIndex = (currentIndex-1+mediaMaster.length)%mediaMaster.length; renderCurrentMedia(currentIndex); showProToast('Previous slide', '#3b82f6'); }
    });

    // Drag & drop upload
    const dragZone = document.getElementById('dragZone');
    dragZone.addEventListener('dragover', (e) => { e.preventDefault(); dragZone.style.borderColor = '#a855f7'; });
    dragZone.addEventListener('dragleave', () => { dragZone.style.borderColor = 'rgba(255,255,255,0.2)'; });
    dragZone.addEventListener('drop', (e) => {
        e.preventDefault();
        dragZone.style.borderColor = 'rgba(255,255,255,0.2)';
        const files = Array.from(e.dataTransfer.files);
        processMultipleFiles(files);
    });
    document.getElementById('bulkFileInput').addEventListener('change', (e) => processMultipleFiles(Array.from(e.target.files)));

    function showProToast(msg, colorHint) { const toast = document.getElementById('toastPro'); document.getElementById('toastProMsg').innerHTML = msg; toast.classList.add('show'); setTimeout(()=>toast.classList.remove('show'), 2800); }

    // Live time
    function updateClock() { const now = new Date(); document.getElementById('liveTime').innerHTML = now.toLocaleTimeString('en-US', {hour:'2-digit', minute:'2-digit'}); }
    setInterval(updateClock, 1000);
    updateClock();

    loadMasterData();
    showProToast('✨ LUXE LCD SYSTEM • READY', '#a855f7');
    setTimeout(()=>{ showProToast('Double right‑click for admin', '#5a5a70'); }, 2000);
</script>
</body>
</html>
