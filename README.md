
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no">
    <title>Duta Kesehatan Jawa Timur | Portal Kesehatan Modern</title>
    <!-- Google Fonts & Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- SweetAlert2 -->
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
    <!-- AOS Animation -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }
        body {
            background: #f8fafc;
            color: #0f172a;
            scroll-behavior: smooth;
        }
        /* Modern Navbar */
        .navbar {
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(8px);
            box-shadow: 0 4px 20px rgba(0,0,0,0.02);
            padding: 1rem 0;
            transition: all 0.3s;
        }
        .navbar-brand {
            font-weight: 800;
            font-size: 1.8rem;
            background: linear-gradient(135deg, #0b63e5, #2b9c5c);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
        }
        .navbar-brand i {
            background: none;
            color: #2b9c5c;
            margin-right: 6px;
        }
        .nav-link {
            font-weight: 500;
            color: #1e293b !important;
            margin: 0 0.5rem;
            transition: 0.2s;
        }
        .nav-link:hover {
            color: #2b9c5c !important;
        }
        .btn-outline-success-custom {
            border: 1px solid #2b9c5c;
            background: white;
            color: #2b9c5c;
            border-radius: 40px;
            padding: 8px 20px;
            font-weight: 500;
            transition: 0.3s;
        }
        .btn-outline-success-custom:hover {
            background: #2b9c5c;
            color: white;
        }
        .btn-outline-danger-custom {
            border: 1px solid #dc2626;
            background: white;
            color: #dc2626;
            border-radius: 40px;
            padding: 8px 20px;
            font-weight: 500;
            transition: 0.3s;
        }
        .btn-outline-danger-custom:hover {
            background: #dc2626;
            color: white;
        }
        /* Hero Section */
        .hero {
            background: linear-gradient(120deg, #eef2ff 0%, #e0f2fe 100%);
            padding: 120px 0 80px;
            border-radius: 0 0 40px 40px;
        }
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            line-height: 1.2;
        }
        .hero .highlight {
            background: linear-gradient(120deg, #0b63e5, #2b9c5c);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        /* Cards & Modern UI */
        .card-hover {
            transition: all 0.3s ease;
            border: none;
            border-radius: 28px;
            background: white;
            box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
        }
        .card-hover:hover {
            transform: translateY(-8px);
            box-shadow: 0 24px 40px -12px rgba(0, 0, 0, 0.15);
        }
        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            position: relative;
            display: inline-block;
        }
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -12px;
            left: 0;
            width: 60px;
            height: 4px;
            background: #2b9c5c;
            border-radius: 4px;
        }
        .badge-date {
            background: #eef2ff;
            color: #1e40af;
            border-radius: 100px;
            font-size: 0.8rem;
            padding: 5px 12px;
            display: inline-block;
        }
        .btn-modern {
            border-radius: 40px;
            padding: 10px 25px;
            font-weight: 600;
            transition: 0.2s;
        }
        .btn-primary-custom {
            background: #2b9c5c;
            border: none;
            color: white;
        }
        .btn-primary-custom:hover {
            background: #227a47;
            transform: scale(1.02);
        }
        .btn-outline-dark-custom {
            border: 1px solid #cbd5e1;
            background: white;
        }
        /* Modal form styling */
        .modal-content {
            border-radius: 32px;
            border: none;
            padding: 10px;
        }
        .form-control, .form-select {
            border-radius: 20px;
            padding: 12px 18px;
            border: 1px solid #e2e8f0;
        }
        footer {
            background: #0f172a;
            color: #cbd5e1;
            padding: 50px 0 30px;
            border-radius: 40px 40px 0 0;
            margin-top: 60px;
        }
        .action-icons i {
            font-size: 1.2rem;
            margin: 0 6px;
            cursor: pointer;
            transition: 0.2s;
            color: #64748b;
        }
        .action-icons i:hover {
            color: #2b9c5c;
        }
        .admin-badge {
            background: #2b9c5c;
            color: white;
            border-radius: 20px;
            padding: 4px 12px;
            font-size: 0.75rem;
            margin-left: 10px;
        }
        .event-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            border-radius: 20px;
        }
        .login-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.85);
            z-index: 10000;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .login-card {
            background: white;
            border-radius: 32px;
            padding: 40px;
            width: 400px;
            max-width: 90%;
        }
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
        }
    </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg fixed-top" id="mainNavbar">
    <div class="container">
        <a class="navbar-brand" href="#"><i class="fas fa-heartbeat"></i> DutaKes Jatim</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto align-items-center">
                <li class="nav-item"><a class="nav-link" href="#home">Beranda</a></li>
                <li class="nav-item"><a class="nav-link" href="#events">Event</a></li>
                <li class="nav-item"><a class="nav-link" href="#info-sehat">Info Sehat</a></li>
                <li class="nav-item"><a class="nav-link" href="#tentang">Tentang</a></li>
                <li class="nav-item ms-2" id="adminButtonContainer">
                    <button class="btn btn-outline-success-custom" id="loginAdminBtn">
                        <i class="fas fa-user-shield"></i> Admin Login
                    </button>
                </li>
            </ul>
        </div>
    </div>
</nav>

<!-- Hero -->
<section class="hero" id="home">
    <div class="container">
        <div class="row align-items-center">
            <div class="col-lg-7" data-aos="fade-up">
                <h1>Jaga Kesehatan, <br> <span class="highlight">Bangun Jawa Timur</span> Sehat</h1>
                <p class="lead mt-4 text-secondary">Duta Kesehatan Jawa Timur hadir untuk memberikan informasi kesehatan terpercaya, event edukasi, dan layanan publik yang modern.</p>
                <div class="mt-4">
                    <a href="#events" class="btn btn-primary-custom btn-modern me-3"><i class="fas fa-calendar-alt me-2"></i>Lihat Event</a>
                    <a href="#info-sehat" class="btn btn-outline-dark-custom btn-modern"><i class="fas fa-newspaper me-2"></i>Artikel Kesehatan</a>
                </div>
            </div>
            <div class="col-lg-5 text-center d-none d-lg-block" data-aos="fade-left">
                <img src="https://placehold.co/500x400/eef2ff/2b9c5c?text=Ilustrasi+Kesehatan" class="img-fluid rounded-4 shadow-sm" alt="health illustration">
            </div>
        </div>
    </div>
</section>

<!-- Event Section -->
<div class="container mt-5 pt-4" id="events">
    <div class="d-flex flex-wrap justify-content-between align-items-center mb-4">
        <div><h2 class="section-title">📅 Event & Kegiatan</h2><p class="text-muted">Ikuti event kesehatan terbaru dari Duta Kesehatan Jatim</p></div>
        <button class="btn btn-primary-custom btn-modern" id="addEventBtn" style="display: none;"><i class="fas fa-plus-circle"></i> Tambah Event</button>
    </div>
    <div class="row" id="eventsContainer"></div>
</div>

<!-- Info Kesehatan Section -->
<div class="container mt-5 pt-3" id="info-sehat">
    <div class="d-flex flex-wrap justify-content-between align-items-center mb-4">
        <div><h2 class="section-title">📰 Informasi Kesehatan</h2><p class="text-muted">Artikel dan tips dari para ahli</p></div>
        <button class="btn btn-primary-custom btn-modern" id="addInfoBtn" style="display: none;"><i class="fas fa-plus-circle"></i> Tambah Info</button>
    </div>
    <div class="row" id="infoContainer"></div>
</div>

<!-- Tentang Section -->
<section id="tentang" class="container mt-5 pt-5">
    <div class="row bg-white rounded-4 p-5 shadow-sm align-items-center" data-aos="zoom-in">
        <div class="col-md-6">
            <h2 class="section-title">Tentang Duta Kesehatan Jatim</h2>
            <p class="mt-4">Duta Kesehatan Jawa Timur merupakan program unggulan yang bertujuan meningkatkan kesadaran masyarakat akan pola hidup sehat, pencegahan penyakit, serta akses layanan kesehatan yang merata. Kami bekerja sama dengan tenaga kesehatan profesional, pemuda, dan pemerintah daerah.</p>
            <p><i class="fas fa-check-circle text-success me-2"></i>Edukasi Masyarakat</p>
            <p><i class="fas fa-check-circle text-success me-2"></i>Gerakan Hidup Sehat</p>
            <p><i class="fas fa-check-circle text-success me-2"></i>Layanan Konsultasi Kesehatan</p>
        </div>
        <div class="col-md-6 text-center">
            <img src="https://placehold.co/500x350/d1fae5/2b9c5c?text=Duta+Kes+Jatim" class="img-fluid rounded-3 shadow" alt="about">
        </div>
    </div>
</section>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="row">
            <div class="col-md-4 mb-3">
                <h4 class="text-white"><i class="fas fa-heartbeat me-2"></i>DutaKes Jatim</h4>
                <p>Gerakan kesehatan modern & inklusif untuk seluruh masyarakat Jawa Timur.</p>
            </div>
            <div class="col-md-4 mb-3">
                <h5>Kontak</h5>
                <p><i class="fas fa-map-marker-alt me-2"></i> Surabaya, Jawa Timur</p>
                <p><i class="fas fa-envelope me-2"></i> Dukes.jatim@gmail.com</p>
            </div>
            <div class="col-md-4 mb-3">
                <h5>Ikuti Kami</h5>
                <div>
                    <i class="fab fa-instagram me-3"></i> dutakesehatan.jatim</p>
                </div>
            </div>
        </div>
        <hr class="opacity-25">
        <div class="text-center small">© 2026 Duta Kesehatan Jawa Timur</div>
    </div>
</footer>

<!-- MODAL LOGIN ADMIN -->
<div id="loginOverlay" class="login-overlay" style="display: none;">
    <div class="login-card">
        <h3 class="text-center mb-4"><i class="fas fa-user-shield"></i> Login Admin</h3>
        <form id="adminLoginForm">
            <div class="mb-3">
                <label>Username</label>
                <input type="text" class="form-control" id="loginUsername" required placeholder="admin">
            </div>
            <div class="mb-3">
                <label>Password</label>
                <input type="password" class="form-control" id="loginPassword" required placeholder="******">
            </div>
            <button type="submit" class="btn btn-primary-custom w-100">Login</button>
            <p class="text-muted text-center mt-3 small">Demo: admin / admin123</p>
        </form>
    </div>
</div>

<!-- MODAL: Event Form -->
<div class="modal fade" id="eventModal" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header border-0">
                <h5 class="modal-title fw-bold" id="eventModalLabel">Tambah Event Baru</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <input type="hidden" id="eventId">
                <div class="mb-3"><label class="form-label">Nama Event</label><input type="text" class="form-control" id="eventName" placeholder="Contoh: Senam Sehat Bersama"></div>
                <div class="mb-3"><label class="form-label">Tanggal</label><input type="date" class="form-control" id="eventDate"></div>
                <div class="mb-3"><label class="form-label">Lokasi</label><input type="text" class="form-control" id="eventLocation" placeholder="Surabaya, Malang, dll"></div>
                <div class="mb-3"><label class="form-label">Deskripsi</label><textarea class="form-control" id="eventDesc" rows="2" placeholder="Deskripsi singkat"></textarea></div>
                <div class="mb-3"><label class="form-label">URL Gambar (opsional)</label><input type="text" class="form-control" id="eventImage" placeholder="https://..."></div>
            </div>
            <div class="modal-footer border-0">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Batal</button>
                <button type="button" class="btn btn-primary-custom" id="saveEventBtn">Simpan Event</button>
            </div>
        </div>
    </div>
</div>

<!-- MODAL: Informasi Kesehatan Form -->
<div class="modal fade" id="infoModal" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header border-0">
                <h5 class="modal-title fw-bold" id="infoModalLabel">Tambah Informasi Kesehatan</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <input type="hidden" id="infoId">
                <div class="mb-3"><label class="form-label">Judul Artikel</label><input type="text" class="form-control" id="infoTitle" placeholder="Tips Jaga Imunitas"></div>
                <div class="mb-3"><label class="form-label">Kategori</label><input type="text" class="form-control" id="infoCategory" placeholder="Gizi, Olahraga, Umum"></div>
                <div class="mb-3"><label class="form-label">Konten / Ringkasan</label><textarea class="form-control" id="infoContent" rows="3" placeholder="Informasi kesehatan penting..."></textarea></div>
                <div class="mb-3"><label class="form-label">Gambar (URL)</label><input type="text" class="form-control" id="infoImgUrl" placeholder="URL gambar"></div>
            </div>
            <div class="modal-footer border-0">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Batal</button>
                <button type="button" class="btn btn-primary-custom" id="saveInfoBtn">Simpan Info</button>
            </div>
        </div>
    </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>
    AOS.init({ duration: 800, once: true });

    // Status Admin
    let isAdminLoggedIn = false;

    // Data
    let events = [];
    let infos = [];

    // Cek session admin dari localStorage
    function checkAdminSession() {
        const savedSession = localStorage.getItem('kadestim_admin_logged_in');
        if (savedSession === 'true') {
            isAdminLoggedIn = true;
            showAdminUI();
        } else {
            isAdminLoggedIn = false;
            showPublicUI();
        }
    }

    // Tampilkan UI untuk Admin
    function showAdminUI() {
        // Tampilkan tombol tambah
        document.getElementById('addEventBtn').style.display = 'inline-block';
        document.getElementById('addInfoBtn').style.display = 'inline-block';
        
        // Ubah tombol admin jadi Logout
        const adminContainer = document.getElementById('adminButtonContainer');
        adminContainer.innerHTML = `
            <div class="d-flex gap-2">
                <span class="admin-badge"><i class="fas fa-user-check"></i> Admin</span>
                <button class="btn btn-outline-danger-custom" id="logoutAdminBtn">
                    <i class="fas fa-sign-out-alt"></i> Logout
                </button>
            </div>
        `;
        
        // Attach logout event
        document.getElementById('logoutAdminBtn')?.addEventListener('click', logoutAdmin);
        
        // Render ulang dengan action icons (edit/hapus)
        renderEvents();
        renderInfos();
    }

    // Tampilkan UI untuk Publik (tanpa akses edit/hapus)
    function showPublicUI() {
        // Sembunyikan tombol tambah
        document.getElementById('addEventBtn').style.display = 'none';
        document.getElementById('addInfoBtn').style.display = 'none';
        
        // Kembalikan tombol login
        const adminContainer = document.getElementById('adminButtonContainer');
        adminContainer.innerHTML = `
            <button class="btn btn-outline-success-custom" id="loginAdminBtn">
                <i class="fas fa-user-shield"></i> Admin Login
            </button>
        `;
        
        // Attach login event
        document.getElementById('loginAdminBtn')?.addEventListener('click', showLoginModal);
        
        // Render ulang tanpa action icons
        renderEvents();
        renderInfos();
    }

    // Show login modal
    function showLoginModal() {
        document.getElementById('loginOverlay').style.display = 'flex';
    }

    // Login admin
    function loginAdmin(username, password) {
        if (username === 'Kadestim' && password === '17102004F') {
            isAdminLoggedIn = true;
            localStorage.setItem('kadestim_admin_logged_in', 'true');
            document.getElementById('loginOverlay').style.display = 'none';
            Swal.fire({
                icon: 'success',
                title: 'Login Berhasil!',
                text: 'Selamat datang Admin Duta Kesehatan Jatim',
                timer: 2000,
                showConfirmButton: false
            });
            showAdminUI();
        } else {
            Swal.fire({
                icon: 'error',
                title: 'Login Gagal!',
                text: 'Username atau password salah',
            });
        }
    }

    // Logout admin
    function logoutAdmin() {
        Swal.fire({
            title: 'Yakin logout?',
            icon: 'question',
            showCancelButton: true,
            confirmButtonColor: '#dc2626',
            confirmButtonText: 'Ya, Logout',
            cancelButtonText: 'Batal'
        }).then((result) => {
            if (result.isConfirmed) {
                isAdminLoggedIn = false;
                localStorage.removeItem('kadestim_admin_logged_in');
                Swal.fire('Logout', 'Anda telah logout dari mode admin', 'info');
                showPublicUI();
            }
        });
    }

    // Load initial data
    function loadInitialData() {
        const storedEvents = localStorage.getItem('dutakes_events');
        const storedInfos = localStorage.getItem('dutakes_infos');
        
        if (storedEvents) {
            events = JSON.parse(storedEvents);
        } else {
            events = [
                { id: 1, name: "Jalan Sehat Bersama Duta Kesehatan", date: "2026-05-10", location: "Surabaya - Taman Bungkul", desc: "Ajak keluarga untuk berolahraga pagi dan cek kesehatan gratis.", image: "https://placehold.co/600x400/ccf0e2/2b9c5c?text=Jalan+Sehat" },
                { id: 2, name: "Webinar: Pola Makan Sehat untuk Remaja", date: "2026-05-20", location: "Online (Zoom)", desc: "Diskusi interaktif bersama ahli gizi.", image: "https://placehold.co/600x400/d9f0ff/0b63e5?text=Webinar" }
            ];
            saveEvents();
        }
        
        if (storedInfos) {
            infos = JSON.parse(storedInfos);
        } else {
            infos = [
                { id: 1, title: "7 Langkah Cuci Tangan Pakai Sabun", category: "Kebersihan", content: "Cuci tangan adalah cara efektif cegah penyakit. Lakukan dengan sabun mengalir selama 20 detik.", imgUrl: "https://placehold.co/600x400/f1f5f9/2b9c5c?text=Cuci+Tangan" },
                { id: 2, title: "Manfaat Buah Lokal Jawa Timur", category: "Gizi", content: "Jeruk, apel, pisang mengandung vitamin tinggi yang baik untuk imunitas tubuh.", imgUrl: "https://placehold.co/600x400/e6f7ec/2b9c5c?text=Buah+Segar" }
            ];
            saveInfos();
        }
        
        renderEvents();
        renderInfos();
    }

    function saveEvents() { localStorage.setItem('dutakes_events', JSON.stringify(events)); }
    function saveInfos() { localStorage.setItem('dutakes_infos', JSON.stringify(infos)); }

    // Render Events (dengan atau tanpa action icons tergantung admin)
    function renderEvents() {
        const container = document.getElementById('eventsContainer');
        if (!container) return;
        
        if (events.length === 0) {
            container.innerHTML = `<div class="col-12 text-center py-5"><i class="fas fa-calendar-times fa-3x text-muted"></i><p class="mt-2">Belum ada event.</p></div>`;
            return;
        }
        
        let html = '';
        events.forEach(event => {
            html += `
                <div class="col-md-6 col-lg-4 mb-4" data-event-id="${event.id}">
                    <div class="card card-hover h-100">
                        <img src="${event.image || 'https://placehold.co/600x400/e2e8f0/2b9c5c?text=Event+Kesehatan'}" class="event-img" alt="${event.name}">
                        <div class="card-body">
                            <div class="d-flex justify-content-between align-items-start">
                                <h5 class="card-title fw-bold">${escapeHtml(event.name)}</h5>
                                ${isAdminLoggedIn ? `
                                    <div class="action-icons">
                                        <i class="fas fa-edit edit-event" data-id="${event.id}" data-bs-toggle="modal" data-bs-target="#eventModal"></i>
                                        <i class="fas fa-trash-alt delete-event" data-id="${event.id}"></i>
                                    </div>
                                ` : ''}
                            </div>
                            <p class="badge-date mt-2"><i class="far fa-calendar-alt"></i> ${event.date}  |  <i class="fas fa-map-marker-alt"></i> ${escapeHtml(event.location)}</p>
                            <p class="card-text text-muted">${escapeHtml(event.desc)}</p>
                        </div>
                    </div>
                </div>
            `;
        });
        container.innerHTML = html;
        
        if (isAdminLoggedIn) {
            attachEventActionListeners();
        }
    }

    // Render Info Kesehatan
    function renderInfos() {
        const container = document.getElementById('infoContainer');
        if (!container) return;
        
        if (infos.length === 0) {
            container.innerHTML = `<div class="col-12 text-center py-5"><i class="fas fa-info-circle fa-3x text-muted"></i><p>Belum ada informasi kesehatan.</p></div>`;
            return;
        }
        
        let html = '';
        infos.forEach(info => {
            html += `
                <div class="col-md-6 col-lg-4 mb-4" data-info-id="${info.id}">
                    <div class="card card-hover h-100">
                        <img src="${info.imgUrl || 'https://placehold.co/600x400/f8fafc/2b9c5c?text=Info+Sehat'}" class="event-img" style="height:160px" alt="${info.title}">
                        <div class="card-body">
                            <div class="d-flex justify-content-between">
                                <h5 class="card-title fw-bold">${escapeHtml(info.title)}</h5>
                                ${isAdminLoggedIn ? `
                                    <div class="action-icons">
                                        <i class="fas fa-edit edit-info" data-id="${info.id}" data-bs-toggle="modal" data-bs-target="#infoModal"></i>
                                        <i class="fas fa-trash-alt delete-info" data-id="${info.id}"></i>
                                    </div>
                                ` : ''}
                            </div>
                            <span class="badge bg-light text-dark mb-2">${escapeHtml(info.category)}</span>
                            <p class="card-text text-secondary small">${escapeHtml(info.content.substring(0, 80))}${info.content.length > 80 ? '...' : ''}</p>
                        </div>
                    </div>
                </div>
            `;
        });
        container.innerHTML = html;
        
        if (isAdminLoggedIn) {
            attachInfoActionListeners();
        }
    }

    // Event Listeners untuk Admin
    function attachEventActionListeners() {
        document.querySelectorAll('.delete-event').forEach(btn => {
            btn.removeEventListener('click', handleDeleteEvent);
            btn.addEventListener('click', handleDeleteEvent);
        });
        document.querySelectorAll('.edit-event').forEach(btn => {
            btn.removeEventListener('click', handleEditEvent);
            btn.addEventListener('click', handleEditEvent);
        });
    }
    
    function attachInfoActionListeners() {
        document.querySelectorAll('.delete-info').forEach(btn => {
            btn.removeEventListener('click', handleDeleteInfo);
            btn.addEventListener('click', handleDeleteInfo);
        });
        document.querySelectorAll('.edit-info').forEach(btn => {
            btn.removeEventListener('click', handleEditInfo);
            btn.addEventListener('click', handleEditInfo);
        });
    }
    
    function handleDeleteEvent(e) {
        const id = parseInt(e.currentTarget.getAttribute('data-id'));
        Swal.fire({
            title: 'Yakin hapus event?',
            icon: 'warning',
            showCancelButton: true,
            confirmButtonColor: '#dc2626',
            confirmButtonText: 'Ya, Hapus!',
            cancelButtonText: 'Batal'
        }).then((result) => {
            if (result.isConfirmed) {
                events = events.filter(ev => ev.id !== id);
                saveEvents();
                renderEvents();
                Swal.fire('Terhapus!', 'Event berhasil dihapus', 'success');
            }
        });
    }
    
    function handleEditEvent(e) {
        const id = parseInt(e.currentTarget.getAttribute('data-id'));
        const event = events.find(ev => ev.id === id);
        if (event) {
            document.getElementById('eventId').value = event.id;
            document.getElementById('eventName').value = event.name;
            document.getElementById('eventDate').value = event.date;
            document.getElementById('eventLocation').value = event.location;
            document.getElementById('eventDesc').value = event.desc;
            document.getElementById('eventImage').value = event.image || '';
            document.getElementById('eventModalLabel').innerText = 'Edit Event';
        }
    }
    
    function handleDeleteInfo(e) {
        const id = parseInt(e.currentTarget.getAttribute('data-id'));
        Swal.fire({
            title: 'Yakin hapus info kesehatan?',
            icon: 'warning',
            showCancelButton: true,
            confirmButtonColor: '#dc2626',
            confirmButtonText: 'Ya, Hapus!',
            cancelButtonText: 'Batal'
        }).then((result) => {
            if (result.isConfirmed) {
                infos = infos.filter(info => info.id !== id);
                saveInfos();
                renderInfos();
                Swal.fire('Terhapus!', 'Info kesehatan berhasil dihapus', 'success');
            }
        });
    }
    
    function handleEditInfo(e) {
        const id = parseInt(e.currentTarget.getAttribute('data-id'));
        const info = infos.find(i => i.id === id);
        if (info) {
            document.getElementById('infoId').value = info.id;
            document.getElementById('infoTitle').value = info.title;
            document.getElementById('infoCategory').value = info.category;
            document.getElementById('infoContent').value = info.content;
            document.getElementById('infoImgUrl').value = info.imgUrl || '';
            document.getElementById('infoModalLabel').innerText = 'Edit Informasi Kesehatan';
        }
    }

    // Save Event
    document.getElementById('saveEventBtn')?.addEventListener('click', () => {
        if (!isAdminLoggedIn) {
            Swal.fire('Akses Ditolak', 'Anda harus login sebagai admin', 'error');
            return;
        }
        
        const id = document.getElementById('eventId').value;
        const name = document.getElementById('eventName').value.trim();
        const date = document.getElementById('eventDate').value;
        const location = document.getElementById('eventLocation').value.trim();
        const desc = document.getElementById('eventDesc').value.trim();
        const image = document.getElementById('eventImage').value.trim();
        
        if (!name || !date || !location) {
            Swal.fire('Error', 'Harap isi Nama Event, Tanggal dan Lokasi!', 'error');
            return;
        }
        
        if (id) {
            const idx = events.findIndex(ev => ev.id == id);
            if (idx !== -1) {
                events[idx] = { ...events[idx], name, date, location, desc, image };
                saveEvents();
            }
        } else {
            const newId = events.length > 0 ? Math.max(...events.map(ev => ev.id)) + 1 : 3;
            events.push({ id: newId, name, date, location, desc, image });
            saveEvents();
        }
        
        resetEventModal();
        renderEvents();
        bootstrap.Modal.getInstance(document.getElementById('eventModal')).hide();
        Swal.fire('Berhasil', 'Event tersimpan', 'success');
    });

    // Save Info
    document.getElementById('saveInfoBtn')?.addEventListener('click', () => {
        if (!isAdminLoggedIn) {
            Swal.fire('Akses Ditolak', 'Anda harus login sebagai admin', 'error');
            return;
        }
        
        const id = document.getElementById('infoId').value;
        const title = document.getElementById('infoTitle').value.trim();
        const category = document.getElementById('infoCategory').value.trim();
        const content = document.getElementById('infoContent').value.trim();
        const imgUrl = document.getElementById('infoImgUrl').value.trim();
        
        if (!title || !category || !content) {
            Swal.fire('Error', 'Judul, Kategori dan Konten harus diisi!', 'error');
            return;
        }
        
        if (id) {
            const idx = infos.findIndex(i => i.id == id);
            if (idx !== -1) {
                infos[idx] = { ...infos[idx], title, category, content, imgUrl };
                saveInfos();
            }
        } else {
            const newId = infos.length > 0 ? Math.max(...infos.map(i => i.id)) + 1 : 3;
            infos.push({ id: newId, title, category, content, imgUrl });
            saveInfos();
        }
        
        resetInfoModal();
        renderInfos();
        bootstrap.Modal.getInstance(document.getElementById('infoModal')).hide();
        Swal.fire('Berhasil', 'Info kesehatan tersimpan', '
