<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Around-NFT | Market</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body>

    <nav class="navbar">
        <div class="logo">Around-NFT</div>
        <div class="nav-buttons">
            <button onclick="showPage('market')">Магазин</button>
            <button onclick="showPage('inventory')">Інвентар</button>
            <button onclick="checkAdmin()" class="admin-btn">🔧</button>
        </div>
    </nav>

    <div class="container">
        <section id="market-page">
            <h1 class="page-title">Доступні NFT</h1>
            <div class="nft-grid" id="market-grid">
                </div>
        </section>

        <section id="inventory-page" style="display:none;">
            <h1 class="page-title">Мій Інвентар</h1>
            <div class="nft-grid" id="inventory-grid">
                </div>
        </section>

        <section id="admin-page" style="display:none;">
            <h1 class="page-title">Адмін-панель (Контроль транзакцій)</h1>
            <div class="admin-table-container">
                <table id="admin-logs">
                    <thead>
                        <tr>
                            <th>Користувач</th>
                            <th>Дія</th>
                            <th>Предмет</th>
                            <th>Баланс TON</th>
                        </tr>
                    </thead>
                    <tbody id="logs-body">
                        </tbody>
                </table>
            </div>
        </section>
    </div>

    <script src="app.js"></script>
</body>
</html>

<div class="admin-create-form">
    
    <h3>➕ Створити нове NFT</h3>
    <div class="form-group">
        <input type="text" id="nft-name" placeholder="Назва NFT">
        <input type="text" id="nft-model" placeholder="Модель (напр. 3D, Classic)">
        <input type="number" id="nft-number" placeholder="Номер (напр. #001)">
        <input type="text" id="nft-image" placeholder="Посилання на картинку (URL)">
        <input type="number" id="nft-price" placeholder="Ціна в TON">
        <button onclick="createNewNFT()" class="create-btn">Створити та Виставити</button>
    </div>
</div>

<hr style="border: 1px solid #333; margin: 20px 0;">
