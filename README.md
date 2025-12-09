<!DOCTYPE html>
<html lang="kk">
<head>
<meta charset="UTF-8">
<title>Сирия Қақтығысының Интерактивті Картасы</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #ffffff; /* Ақ фон */
        color: #222; 
        margin: 0;
        padding: 20px;
    }
    h1, h2 {
        text-align: center;
        color: #c27c00; /* алтындау түс */
    }
    .actor-box {
        background: #f1f1f1;
        border-radius: 10px;
        padding: 15px;
        margin: 10px 0;
        transition: 0.3s;
        cursor: pointer;
        border-left: 5px solid #c27c00;
    }
    .actor-box:hover {
        background: #e2e2e2;
        transform: scale(1.02);
    }
    .content {
        display: none;
        padding-left: 20px;
        margin-top: 10px;
        border-left: 2px solid #bbb;
        animation: fadeIn 0.4s;
        color: #333;
        background: #fafafa;
        border-radius: 8px;
        padding: 10px;
    }
    @keyframes fadeIn {
        from {opacity: 0;}
        to {opacity: 1;}
    }

    table {
        width: 100%;
        border-collapse: collapse;
        margin-top: 25px;
        background: #f8f8f8;
        border-radius: 10px;
        overflow: hidden;
        border: 1px solid #ddd;
    }
    th {
        background: #ffdd77;
        color: #4a3d00;
        padding: 12px;
        font-size: 16px;
    }
    td {
        border-bottom: 1px solid #e0e0e0;
        padding: 10px;
        font-size: 14px;
    }
    tr:hover {
        background: #f0f0f0;
    }

    .tag {
        display:inline-block;
        padding: 4px 8px;
        border-radius: 6px;
        margin-right: 5px;
        font-size: 12px;
        font-weight: bold;
        color: white;
    }
    .gov { background:#d9534f; }
    .opp { background:#5bc0de; }
    .kurds { background:#5cb85c; }
    .ext { background:#f0ad4e; }
</style>
</head>
<body>

<h1>Сирия Қақтығысының Интерактивті Картасы</h1>
<h2>Тарихи деректерге сүйенген талдау</h2>

<!-- ==== ACTOR SECTION ==== -->
<div class="actor-box" onclick="toggleContent('gov')">
    <strong>🟥 Сирия үкіметі (Башар Асад режимі)</strong>
</div>
<div class="content" id="gov">
    <p><b>Мүдделері:</b> орталық билікті сақтау, территориялық тұтастық, халықаралық легитимділік.</p>
    <p><b>Мақсаттары:</b> негізгі қалаларды бақылауда ұстау, оппозицияны әскери түрде әлсірету.</p>
    <p><b>Тарихи дерек:</b> 1970 жылдан бергі Асадтар билігі авторитарлық модельге негізделген.</p>
</div>

<div class="actor-box" onclick="toggleContent('opp')">
    <strong>🟦 Қарулы оппозиция (FSA және басқа топтар)</strong>
</div>
<div class="content" id="opp">
    <p><b>Мүдделері:</b> Асад режимін құлату, демократиялық реформа.</p>
    <p><b>Мақсаттары:</b> халықаралық қолдау, территориялық бақылау орнату.</p>
    <p><b>Тарихи дерек:</b> 2011 жылы бейбіт шерулерден басталған қозғалыс қарулы фракцияларға бөлінді.</p>
</div>

<div class="actor-box" onclick="toggleContent('kurds')">
    <strong>🟩 Күрд күштері (YPG/SDF)</strong>
</div>
<div class="content" id="kurds">
    <p><b>Мүдделері:</b> күрд аймақтарының автономиясы.</p>
    <p><b>Мақсаттары:</b> Рожаваның өзін-өзі басқару моделін сақтау.</p>
    <p><b>Тарихи дерек:</b> 2012 ж. күрдтер өз аймақтарын бақылауға алып, автономиялық кеңестер құрды.</p>
</div>

<div class="actor-box" onclick="toggleContent('radical')">
    <strong>⬛ Радикалды топтар (ISIS, ан-Нусра)</strong>
</div>
<div class="content" id="radical">
    <p><b>Мүдделері:</b> теократиялық халифат құру.</p>
    <p><b>Мақсаттары:</b> мұнай, логистикалық аймақтарды бақылау.</p>
    <p><b>Тарихи дерек:</b> 2014 ж. ISIS Сирия мен Ирактың үлкен бөлігін жаулап алды.</p>
</div>

<div class="actor-box" onclick="toggleContent('ext')">
    <strong>🌍 Сыртқы державалар (Ресей, Иран, Түркия, АҚШ)</strong>
</div>
<div class="content" id="ext">
    <p><b>Ресей:</b> Асадты қолдау → 2015 жылдан бастап әскери операциялар.</p>
    <p><b>Иран:</b> аймақтық шиит осінің мүдделері.</p>
    <p><b>Түркия:</b> күрд автономиясына жол бермеу.</p>
    <p><b>АҚШ:</b> ISIS-ке қарсы коалиция.</p>
</div>

<!-- ==== TABLE ==== -->
<h2>📊 Мүдделер мен мақсаттардың салыстырмалы кестесі</h2>
<table>
    <tr>
        <th>Тарап</th>
        <th>Қысқа мерзімді мүдделер</th>
        <th>Ұзақ мерзімді мүдделер</th>
        <th>Стратегиялық мақсат</th>
    </tr>

    <tr>
        <td><span class="tag gov">Үкімет</span></td>
        <td>Территорияны бақылауға алу</td>
        <td>Билікті сақтау</td>
        <td>Халықаралық легитимділік</td>
    </tr>

    <tr>
        <td><span class="tag opp">Оппозиция</span></td>
        <td>Әскери баланс</td>
        <td>Саяси реформа</td>
        <td>Жаңа басқару жүйесі</td>
    </tr>

    <tr>
        <td><span class="tag kurds">Күрд күштері</span></td>
        <td>Қауіпсіздік</td>
        <td>Автономия</td>
        <td>Рожаваның нығаюы</td>
    </tr>

    <tr>
        <td><span class="tag ext">Сыртқы державалар</span></td>
        <td>Өз ықпалын күшейту</td>
        <td>Аймақтық үстемдік</td>
        <td>Геосаяси позицияны бекіту</td>
    </tr>
</table>

<script>
function toggleContent(id) {
    var x = document.getElementById(id);
    if (x.style.display === "block") x.style.display = "none";
    else x.style.display = "block";
}
</script>

</body>
</html>
