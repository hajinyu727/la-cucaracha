<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>다국어 여행 서비스</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #fff3e0, #ffffff);
      margin: 0;
      padding: 0;
      position: relative;
    }
    .background-title {
      position: fixed;
      top: 10px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 36px;
      font-weight: bold;
      background: linear-gradient(to right, #f44336, #ff9800, #4caf50);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      z-index: 1000;
      pointer-events: none;
    }
    .container {
      max-width: 800px;
      margin: 0 auto;
      padding: 80px 30px 30px;
      text-align: center;
    }
    .page {
      display: none;
    }
    .active {
      display: block;
    }
    h2 {
      margin-bottom: 20px;
    }
    .button-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 15px;
      justify-content: center;
      margin-top: 20px;
    }
    button {
      padding: 12px 16px;
      font-size: 16px;
      border-radius: 10px;
      border: none;
      background-color: #f44336;
      color: white;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #d32f2f;
    }
    .button-grid button:nth-child(3n+2) {
      background-color: #ff9800;
    }
    .button-grid button:nth-child(3n+2):hover {
      background-color: #fb8c00;
    }
    .button-grid button:nth-child(3n+3) {
      background-color: #4caf50;
    }
    .button-grid button:nth-child(3n+3):hover {
      background-color: #388e3c;
    }
    .back {
      background-color: #6c757d;
      margin-top: 60px;
      display: block;
      margin-left: auto;
      margin-right: auto;
    }
  </style>
</head>
<body>
  <div class="background-title">LA CUCARACHA</div>
  <div class="container">
    <!-- 다국어 선택 페이지 -->
    <div id="languagePage" class="page active">
      <h2>언어를 선택하세요</h2>
      <div class="button-grid" id="languageButtons">
        <button onclick="goToMenuPage('English')">English</button>
        <button onclick="goToMenuPage('Chinese')">中文</button>
        <button onclick="goToMenuPage('Japanese')">日本語</button>
        <button onclick="goToMenuPage('Vietnamese')">Tiếng Việt</button>
        <button onclick="goToMenuPage('Thai')">ภาษาไทย</button>
        <button onclick="goToMenuPage('Uzbek')">Oʻzbek</button>
        <button onclick="goToMenuPage('Khmer')">ខ្មែរ</button>
        <button onclick="goToMenuPage('Tagalog')">Tagalog</button>
        <button onclick="goToMenuPage('Indonesian')">Bahasa Indonesia</button>
        <button onclick="goToMenuPage('Nepali')">नेपाली</button>
      </div>
    </div>

    <!-- 메뉴 선택 페이지 -->
    <div id="menuPage" class="page menu-page">
      <h2>원하시는 서비스를 선택하세요</h2>
      <div class="button-grid">
        <button onclick="goToPage('exchangePage')">수수료 없는 외화 환전</button>
        <button onclick="goToPage('transportPage')">빠른 교통수단 예약</button>
        <button onclick="goToPage('cardPage')">라차카드 서비스</button>
        <button onclick="goToPage('supportPage')">기타 고객지원</button>
      </div>
      <button class="back" onclick="goBack('languagePage')">← 뒤로가기</button>
    </div>

    <!-- 환전 페이지 -->
    <div id="exchangePage" class="page">
      <h2>✈ 한국 여행의 시작, 더 간편하게!</h2>
      <p>💸 수수료 0원 외화 환전</p>
      <p>🚆 버스·지하철·기차 바로 탑승</p>
      <p>💳 현금 없이 카드 하나로 한국 여행 끝!</p>
      <p>👉 QR코드를 스캔해서 바로 신청하세요!</p>
      <div class="button-grid">
        <button>💵 USD</button>
        <button>💴 JPY</button>
        <button>💶 CNY</button>
        <button>🇻🇳 VND</button>
        <button>🇹🇭 THB</button>
        <button>🇺🇿 UZS</button>
        <button>🇰🇭 KHR</button>
        <button>🇵🇭 PHP</button>
        <button>🇮🇩 IDR</button>
        <button>🇳🇵 NPR</button>
      </div>
      <button class="back" onclick="goBack('menuPage')">← 뒤로가기</button>
    </div>

    <!-- 교통수단 페이지 -->
    <div id="transportPage" class="page">
      <h2>교통수단을 선택하세요</h2>
      <div class="button-grid">
        <button onclick="alert('버스 예약 페이지')">🚌 버스</button>
        <button onclick="alert('비행기 예약 페이지')">✈ 비행기</button>
        <button onclick="alert('택시 예약 페이지')">🚖 택시</button>
        <button onclick="alert('KTX 예약 페이지')">🚄 KTX</button>
      </div>
      <button class="back" onclick="goBack('menuPage')">← 뒤로가기</button>
    </div>

    <!-- 라차카드 페이지 -->
    <div id="cardPage" class="page">
      <h2>라차카드 서비스</h2>
      <div class="button-grid">
        <button onclick="alert('가입 안내 페이지')">라차카드 가입</button>
        <button onclick="alert('포인트 조회 페이지')">포인트 안내</button>
        <button onclick="alert('분실 신고 안내 페이지')">카드 분실</button>
        <button onclick="alert('이용 방법 안내 페이지')">이용 방법</button>
      </div>
      <button class="back" onclick="goBack('menuPage')">← 뒤로가기</button>
    </div>

    <!-- 고객지원 페이지 -->
    <div id="supportPage" class="page">
      <h2>고객지원</h2>
      <p>상담원 연결 안내: 1234-5678로 연락해주세요.</p>
      <button class="back" onclick="goBack('menuPage')">← 뒤로가기</button>
    </div>
  </div>

  <script>
    function goToMenuPage(language) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById('menuPage').classList.add('active');
    }
    function goToPage(pageId) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
    }
    function goBack(pageId) {
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
    }
  </script>
</body>
</html>
