# KT4
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
        font-size: 28px;
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
        font-size: 16px;
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

    .tile-icon {
        font-size: 50px;
        margin-bottom: 20px;
    }

    .tile-title {
        font-size: 20px;
        font-weight: 600;
        margin-bottom: 10px;
    }

    .tile-desc {
        font-size: 14px;
        opacity: 0.7;
        line-height: 1.2;
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

    
    .tile-bottom {
        grid-column: 1 / -1;
        min-height: 700px;
        background: rgba(255, 255, 255, 0.15);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 28px;
        font-weight: 600;
        border-radius: 12px;
        text-align: center;
       
    }

    @media (max-width: 768px) {
        .tile-title { font-size: 30px; }
        .tile-desc { font-size: 12px; }
        .tile-icon { font-size: 40px; margin-bottom: 15px; }
    }

    @media (max-width: 576px) {
        .tile-title { font-size: 16px; }
        .tile-desc { font-size: 11px; }
        .tile-icon { font-size: 35px; margin-bottom: 10px; }
    }

    @media (max-width: 400px) {
        .tile-title { font-size: 14px; }
        .tile-desc { font-size: 10px; }
        .tile-icon { font-size: 30px; margin-bottom: 8px; }
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
        <div class="tile-title">Дашборд</div>
        <div class="tile-desc">Отчёты</div>
    </div>
    
    <div class="tile tile-2">
        <div class="tile-icon"></div>
        <div class="tile-title">Аналитика</div>
        <div class="tile-desc">Графики</div>
    </div>
    
    <div class="tile tile-3 tile-tall">
        <div class="tile-icon"></div>
        <div class="tile-title">Безопасность</div>
        <div class="tile-desc">Защита</div>
    </div>
    
    <div class="tile tile-4">
        <div class="tile-icon"></div>
        <div class="tile-title">Облако</div>
        <div class="tile-desc">Файлы</div>
    </div>
    
    <div class="tile tile-5">
        <div class="tile-icon"></div>
        <div class="tile-title">AI</div>
        <div class="tile-desc">Инструменты</div>
    </div>
    
    <div class="tile tile-6 tile-wide">
        <div class="tile-icon"></div>
        <div class="tile-title">Мобильные</div>
        <div class="tile-desc">Приложения</div>
    </div>
    
    <div class="tile tile-7 tile-large">
        <div class="tile-icon"></div>
        <div class="tile-title">Дизайн</div>
        <div class="tile-desc">Студия</div>
    </div>
    
    <div class="tile tile-8">
        <div class="tile-icon"></div>
        <div class="tile-title">Настройки</div>
        <div class="tile-desc">Система</div>
    </div>
    
    <div class="tile tile-9">
        <div class="tile-icon"></div>
        <div class="tile-title">Рост</div>
        <div class="tile-desc">Метрики</div>
    </div>
    
    <div class="tile tile-10">
        <div class="tile-icon"></div>
        <div class="tile-title">Уведомления</div>
        <div class="tile-desc">События</div>
    </div>

    <div class="tile-bottom">
        РАБОТАТЬ С НАМИ
    </div>
</div>

</body>
</html>
