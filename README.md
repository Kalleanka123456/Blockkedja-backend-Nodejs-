

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary: #2563eb;
    --primary-dark: #1d4ed8;

    --background: #f4f6f9;
    --surface: #ffffff;

    --text: #172033;
    --text-light: #64748b;

    --border: #e2e8f0;

    --success: #16a34a;
    --warning: #d97706;
    --danger: #dc2626;

    --sidebar-width: 250px;

    font-family:
        Inter,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        sans-serif;
}

body {
    background: var(--background);
    color: var(--text);
    min-height: 100vh;
}


/* =========================
   GENERAL
========================= */

.hidden {
    display: none !important;
}

.page {
    min-height: 100vh;
}

button,
input,
textarea,
select {
    font: inherit;
}


/* =========================
   LOGIN
========================= */

#login-page {
    display: flex;
    align-items: center;
    justify-content: center;

    background:
        linear-gradient(
            135deg,
            #eef4ff,
            #f8fafc
        );
}

.login-container {
    width: 100%;
    max-width: 420px;

    background: var(--surface);

    padding: 40px;

    border-radius: 16px;

    box-shadow:
        0 20px 50px rgba(15, 23, 42, 0.08);
}

.logo {
    display: flex;
    align-items: center;
    gap: 12px;

    margin-bottom: 8px;
}

.logo span {
    display: flex;
    align-items: center;
    justify-content: center;

    width: 42px;
    height: 42px;

    background: var(--primary);
    color: white;

    border-radius: 10px;

    font-size: 28px;
    font-weight: 700;
}

.logo h1 {
    font-size: 24px;
}

.subtitle {
    color: var(--text-light);
    margin-bottom: 32px;
}


/* =========================
   FORMS
========================= */

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;

    margin-bottom: 8px;

    font-size: 14px;
    font-weight: 600;
}

input,
textarea,
select {
    width: 100%;

    padding: 12px 14px;

    border: 1px solid var(--border);
    border-radius: 8px;

    background: white;
    color: var(--text);

    outline: none;

    transition: 0.2s;
}

input:focus,
textarea:focus,
select:focus {
    border-color: var(--primary);

    box-shadow:
        0 0 0 3px rgba(37, 99, 235, 0.1);
}


/* =========================
   BUTTONS
========================= */

.btn {
    border: none;
    border-radius: 8px;

    padding: 11px 18px;

    cursor: pointer;

    font-weight: 600;

    transition: 0.2s;
}

.btn-primary {
    background: var(--primary);
    color: white;
}

.btn-primary:hover {
    background: var(--primary-dark);
}

.btn-secondary {
    background: #e2e8f0;
    color: var(--text);
}

.btn-secondary:hover {
    background: #cbd5e1;
}

.login-container .btn {
    width: 100%;
}

.error-message {
    color: var(--danger);
    margin-top: 15px;
    font-size: 14px;
}


/* =========================
   APP LAYOUT
========================= */

.app {
    min-height: 100vh;

    display: flex;
}


/* =========================
   SIDEBAR
========================= */

.sidebar {
    width: var(--sidebar-width);

    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;

    background: #111827;
    color: white;

    display: flex;
    flex-direction: column;
}

.sidebar-logo {
    height: 80px;

    display: flex;
    align-items: center;

    gap: 12px;

    padding: 0 24px;

    font-weight: 700;
}

.logo-icon {
    width: 34px;
    height: 34px;

    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 8px;

    background: var(--primary);

    font-size: 22px;
}

.navigation {
    padding: 20px 12px;
}

.nav-item {
    display: flex;
    align-items: center;

    gap: 12px;

    padding: 12px;

    margin-bottom: 5px;

    color: #cbd5e1;
    text-decoration: none;

    border-radius: 8px;

    transition: 0.2s;
}

.nav-item:hover,
.nav-item.active {
    background: #1e293b;
    color: white;
}

.sidebar-bottom {
    margin-top: auto;
    padding: 20px;
}

.server-status {
    display: flex;
    align-items: center;
    gap: 10px;

    padding: 12px;

    background: #1e293b;
    border-radius: 8px;

    margin-bottom: 15px;
}

.server-status small {
    display: block;
    color: #94a3b8;
}

.server-status strong {
    font-size: 13px;
}

.status-dot {
    width: 9px;
    height: 9px;

    border-radius: 50%;

    background: var(--success);
}

.logout-button {
    width: 100%;

    padding: 10px;

    border: none;
    border-radius: 8px;

    background: #334155;
    color: white;

    cursor: pointer;
}


/* =========================
   MAIN
========================= */

.main-content {
    margin-left: var(--sidebar-width);

    width: calc(100% - var(--sidebar-width));

    min-height: 100vh;
}


/* =========================
   TOPBAR
========================= */

.topbar {
    min-height: 80px;

    padding: 20px 32px;

    background: white;

    border-bottom: 1px solid var(--border);

    display: flex;
    justify-content: space-between;
    align-items: center;
}

.topbar h2 {
    font-size: 22px;
}

.topbar p {
    color: var(--text-light);
    font-size: 14px;
    margin-top: 3px;
}

.user-info {
    display: flex;
    align-items: center;

    gap: 10px;
}

.user-info small {
    display: block;
    color: var(--text-light);
}

.user-avatar {
    width: 40px;
    height: 40px;

    border-radius: 50%;

    display: flex;
    align-items: center;
    justify-content: center;

    background: #dbeafe;
    color: var(--primary);

    font-weight: 700;
}


/* =========================
   CONTENT
========================= */

.content {
    padding: 30px;
    max-width: 1600px;
    margin: auto;
}


/* =========================
   CARDS
========================= */

.card {
    background: var(--surface);

    border: 1px solid var(--border);

    border-radius: 12px;

    padding: 24px;

    margin-bottom: 24px;
}

.section-heading {
    display: flex;
    align-items: center;
    justify-content: space-between;

    margin-bottom: 20px;
}

.section-heading h3 {
    font-size: 18px;
}

.section-heading p {
    color: var(--text-light);

    font-size: 14px;

    margin-top: 4px;
}


/* =========================
   SEARCH
========================= */

.search-container {
    display: flex;
    gap: 10px;
}

.search-container input {
    flex: 1;
}


/* =========================
   PATIENT
========================= */

.patient-header {
    display: flex;
    align-items: center;

    gap: 16px;

    padding-bottom: 20px;

    border-bottom: 1px solid var(--border);
}

.patient-avatar {
    width: 60px;
    height: 60px;

    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 50%;

    background: #dbeafe;
    color: var(--primary);

    font-weight: 700;
    font-size: 18px;
}

.patient-header p {
    color: var(--text-light);

    margin-top: 4px;
}

.role-badge {
    margin-left: auto;

    padding: 6px 12px;

    border-radius: 20px;

    background: #e0f2fe;
    color: #0369a1;

    font-size: 12px;
    font-weight: 600;
}

.patient-details {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;

    margin-top: 20px;
}

.detail span {
    display: block;

    color: var(--text-light);

    font-size: 13px;

    margin-bottom: 5px;
}


/* =========================
   DASHBOARD GRID
========================= */

.dashboard-grid {
    display: grid;

    grid-template-columns:
        minmax(0, 1.5fr)
        minmax(320px, 1fr);

    gap: 24px;
}


/* =========================
   NOTES
========================= */

.note {
    border: 1px solid var(--border);

    border-radius: 10px;

    padding: 18px;

    margin-bottom: 14px;
}

.note-header {
    display: flex;
    justify-content: space-between;

    margin-bottom: 12px;
}

.note-header strong {
    display: inline-block;
}

.note-role {
    margin-left: 8px;

    color: var(--text-light);

    font-size: 12px;
}

.note-header time {
    color: var(--text-light);

    font-size: 12px;
}

.note-content {
    color: #475569;

    line-height: 1.6;
}

.note-footer {
    margin-top: 15px;
}

.visibility {
    display: inline-block;

    padding: 5px 9px;

    border-radius: 20px;

    font-size: 11px;
    font-weight: 600;
}

.visibility.public {
    background: #dcfce7;
    color: #166534;
}

.visibility.medical {
    background: #dbeafe;
    color: #1e40af;
}

.visibility.private {
    background: #fef3c7;
    color: #92400e;
}


/* =========================
   ACCESS LOG
========================= */

.blockchain-status {
    padding: 6px 10px;

    border-radius: 20px;

    background: #dcfce7;

    color: #166534;

    font-size: 11px;

    font-weight: 600;
}

.access-log {
    display: flex;
    align-items: flex-start;

    gap: 12px;

    padding: 14px 0;

    border-bottom: 1px solid var(--border);
}

.access-log:last-child {
    border-bottom: none;
}

.log-icon {
    width: 36px;
    height: 36px;

    display: flex;
    align-items: center;
    justify-content: center;

    background: #f1f5f9;

    border-radius: 8px;
}

.log-content {
    flex: 1;
}

.log-content strong {
    display: block;
}

.log-content span,
.log-content small {
    display: block;

    color: var(--text-light);

    font-size: 12px;

    margin-top: 3px;
}

.verified {
    font-size: 11px;

    color: var(--success);

    font-weight: 600;
}


/* =========================
   NEW NOTE
========================= */

.new-note-card {
    margin-top: 0;
}

.form-actions {
    display: flex;

    justify-content: flex-end;

    gap: 10px;
}


/* =========================
   ACCESS DENIED
========================= */

.access-denied {
    text-align: center;

    padding: 80px 20px;
}

.access-denied-icon {
    width: 60px;
    height: 60px;

    display: flex;
    align-items: center;
    justify-content: center;

    margin: 0 auto 20px;

    border-radius: 50%;

    background: #fee2e2;
    color: var(--danger);

    font-size: 28px;
    font-weight: 700;
}

.access-denied p {
    color: var(--text-light);

    margin: 10px 0 25px;
}


/* =========================
   RESPONSIVE
========================= */

@media (max-width: 1100px) {

    .dashboard-grid {
        grid-template-columns: 1fr;
    }

}

@media (max-width: 768px) {

    .sidebar {
        width: 70px;
    }

    .sidebar-logo span,
    .nav-item:not(.active)::after,
    .nav-item {
        font-size: 0;
    }

    .nav-item span {
        font-size: 18px;
    }

    .main-content {
        margin-left: 70px;
        width: calc(100% - 70px);
    }

    .content {
        padding: 20px;
    }

    .patient-details {
        grid-template-columns: 1fr;
    }

    .topbar {
        padding: 15px 20px;
    }

}

@media (max-width: 550px) {

    .login-container {
        margin: 20px;
        padding: 25px;
    }

    .search-container {
        flex-direction: column;
    }

    .patient-header {
        align-items: flex-start;
        flex-wrap: wrap;
    }

    .role-badge {
        margin-left: 0;
    }

}