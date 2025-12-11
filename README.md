# KT4
[KT-4 — копия.html](https://github.com/user-attachments/files/24109939/KT-4.html)
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Modern Metro Tiles</title>
<style>
    * {
        box-sizing: border-box;
    }
    
    body {
        margin: 0;
        font-family: "Segoe UI", "Helvetica Neue", Arial, sans-serif;
        background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
        color: white;
        min-height: 100vh;
    }

    .top-bar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 20px 40px;
        background: rgba(0, 0, 0, 0.2);
        backdrop-filter: blur(10px);
        border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    }

    .logo {
        font-size: 24px;
        font-weight: 300;
        letter-spacing: 1px;
    }

    .logo span {
        font-weight: 600;
        color: #00b4ff;
    }

    .user-info {
        display: flex;
        align-items: center;
        gap: 15px;
    }

    .user-avatar {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background: linear-gradient(135deg, #00b4ff, #0088cc);
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: bold;
    }

    .tile-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
        gap: 15px;
        padding: 40px;
        max-width: 1400px;
        margin: 0 auto;
    }

    .tile {
        background: rgba(255, 255, 255, 0.1);
        border-radius: 8px;
        padding: 20px;
        display: flex;
        flex-direction: column;
        cursor: pointer;
        position: relative;
        overflow: hidden;
        min-height: 150px;
        border: 1px solid rgba(255, 255, 255, 0.05);
        transition: none; 
    }

    .tile::before {
        display: none; 
    }

    .tile-icon {
        font-size: 40px;
        margin-bottom: 15px;
        transform: none; 
    }

    .tile-badge {
        opacity: 1;
        transform: none;
    }

    .tile-wide { grid-column: span 2; }
    .tile-tall { grid-row: span 2; }
    .tile-large { grid-column: span 2; grid-row: span 2; }

    .tile-1 { color: #00b4ff; }
    .tile-2 { color: #00d68f; }
    .tile-3 { color: #ff4757; }
    .tile-4 { color: #ffa502; }
    .tile-5 { color: #9c88ff; }
    .tile-6 { color: #00d2d3; }
    .tile-7 { color: #ff6b81; }
    .tile-8 { color: #70a1ff; }
    .tile-9 { color: #ff9ff3; }
    .tile-10 { color: #54a0ff; }

    @media (max-width: 1200px) {
        .tile-container { max-width: 1000px; grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
    }
    @media (max-width: 992px) {
        .tile-container { grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); gap: 12px; padding: 30px; }
        .tile { min-height: 130px; padding: 15px; }
        .tile-icon { font-size: 35px; }
        .top-bar { padding: 15px 30px; }
    }
    @media (max-width: 768px) {
        .tile-container { grid-template-columns: repeat(auto-fill, minmax(120px, 1fr)); gap: 10px; padding: 20px; }
        .tile { min-height: 120px; padding: 12px; }
        .tile-icon { font-size: 30px; margin-bottom: 10px; }
        .tile-title { font-size: 14px; }
        .tile-desc { font-size: 11px; }
        .top-bar { padding: 12px 20px; }
        .logo { font-size: 20px; }
        .user-avatar { width: 35px; height: 35px; }
        .tile-wide, .tile-tall, .tile-large { grid-column: span 1; grid-row: span 1; }
    }
    @media (max-width: 576px) {
        .tile-container { grid-template-columns: repeat(3, 1fr); gap: 8px; padding: 15px; }
        .tile { min-height: 110px; padding: 10px; }
        .tile-icon { font-size: 28px; margin-bottom: 8px; }
        .tile-title { font-size: 13px; }
        .user-info { gap: 10px; }
    }
    @media (max-width: 400px) {
        .tile-container { grid-template-columns: repeat(2, 1fr); }
        .tile { min-height: 100px; }
        .tile-icon { font-size: 26px; }
        .top-bar { flex-direction: column; gap: 10px; align-items: flex-start; }
        .user-info { align-self: flex-end; margin-top: -40px; }
    }
</style>
</head>
<body>

<div class="top-bar">
    <div class="logo">Modern<span>UI</span></div>
    <div class="user-info">
        <div class="user-avatar">JD</div>
        <div>John Doe</div>
    </div>
</div>

<div class="tile-container">
    <div class="tile tile-1 tile-wide">
        <div class="tile-icon"></div>
        <div class="tile-title">Dashboard</div>
        <div class="tile-desc">Analytics & Reports</div>
        <div class="tile-badge">New</div>
    </div>
    
    <div class="tile tile-2">
        <div class="tile-icon"></div>
        <div class="tile-title">Analytics</div>
        <div class="tile-desc">Data visualization</div>
    </div>
    
    <div class="tile tile-3 tile-tall">
        <div class="tile-icon"></div>
        <div class="tile-title">Security</div>
        <div class="tile-desc">System protection</div>
        <div class="tile-badge">3</div>
    </div>
    
    <div class="tile tile-4">
        <div class="tile-icon"></div>
        <div class="tile-title">Cloud</div>
        <div class="tile-desc">Storage services</div>
    </div>
    
    <div class="tile tile-5">
        <div class="tile-icon"></div>
        <div class="tile-title">AI Tools</div>
        <div class="tile-desc">Machine learning</div>
    </div>
    
    <div class="tile tile-6 tile-wide">
        <div class="tile-icon"></div>
        <div class="tile-title">Mobile</div>
        <div class="tile-desc">App development</div>
    </div>
    
    <div class="tile tile-7 tile-large">
        <div class="tile-icon"></div>
        <div class="tile-title">Design Studio</div>
        <div class="tile-desc">Creative workspace with tools</div>
        <div class="tile-badge">Pro</div>
    </div>
    
    <div class="tile tile-8">
        <div class="tile-icon"></div>
        <div class="tile-title">Settings</div>
        <div class="tile-desc">System configuration</div>
    </div>
    
    <div class="tile tile-9">
        <div class="tile-icon"></div>
        <div class="tile-title">Growth</div>
        <div class="tile-desc">Performance metrics</div>
    </div>
    
    <div class="tile tile-10">
        <div class="tile-icon"></div>
        <div class="tile-title">Notifications</div>
        <div class="tile-desc">Alerts & updates</div>
        <div class="tile-badge">12</div>
    </div>
</div>

</body>
</html>
