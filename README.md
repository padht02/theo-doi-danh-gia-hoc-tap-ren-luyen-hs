<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f4f8;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    .banner {
      background-color: #ffeb3b;
      color: #333;
      font-weight: bold;
      padding: 15px 0;
      font-size: 24px;
      text-transform: uppercase;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    }

    .navbar {
      display: flex;
      justify-content: center;
      background-color: #1a73e8;
      padding: 15px;
      gap: 20px;
    }
    .navbar a {
      color: white;
      font-weight: bold;
      text-decoration: none;
      padding: 10px 20px;
      background-color: #1a73e8;
      border-radius: 5px;
      transition: background-color 0.3s;
    }
    .navbar a:hover {
      background-color: #1558b0;
    }

    .title {
      margin-top: 30px;
      color: #333;
      line-height: 1.5;
      font-size: 24px;
      font-weight: bold;
    }

    .content {
      display: none;
      margin-top: 20px;
    }
    .content.active {
      display: block;
    }

    .button-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      max-width: 80%;
      margin: 0 auto;
    }
    .button-container a {
      padding: 10px 15px;
      background-color: #ffeb3b;
      color: #333;
      text-decoration: none;
      font-weight: bold;
      border-radius: 5px;
      width: 100%;
      max-width: 400px;
      transition: background-color 0.3s, transform 0.3s;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
      display: none;
    }
    .button-container a:hover {
      background-color: #ffd600;
      transform: translateY(-3px);
    }

    .search-container {
      margin-top: 20px;
      margin-bottom: 20px;
      position: relative;
      display: flex;
      justify-content: center;
    }
    .search-input {
      padding: 10px;
      width: 300px;
      border-radius: 5px;
      border: 1px solid #ddd;
      font-size: 16px;
    }
    .suggestions {
      position: absolute;
      top: 100%;
      width: 300px;
      background-color: white;
      border: 1px solid #ddd;
      border-radius: 5px;
      max-height: 200px;
      overflow-y: auto;
      display: none;
    }
    .suggestion-item {
      padding: 10px;
      cursor: pointer;
    }
    .suggestion-item:hover {
      background-color: #f0f0f0;
    }
  </style>
</head>
<body>

  <div class="banner">
    PATHWAY ACADEMY - CƠ SỞ ĐÔNG HƯNG THUẬN 02
  </div>

  <div class="navbar">
    <a href="#" onclick="showContent('trang-chu')">Trang chủ</a>
    <a href="#" onclick="showContent('mon-hoc')">Môn học</a>
    <a href="#" onclick="showContent('lop')">Lớp</a>
    <a href="#" onclick="showContent('ban-giam-hieu')">Ban Giám Hiệu</a>
  </div>

  <h1 class="title">
    THEO DÕI VÀ ĐÁNH GIÁ<br>
    QUÁ TRÌNH HỌC TẬP - RÈN LUYỆN HỌC SINH<br>
    CẤP TRUNG HỌC CƠ SỞ
  </h1>

  <div id="trang-chu" class="content active">
    <p>Chào mừng bạn đến với trang theo dõi và đánh giá học sinh cơ sở ĐHT02</p>
    <img src="https://via.placeholder.com/600x400.png?text=Truong+Hoc" alt="Hình ảnh trường học" class="home-image">
  </div>

  <!-- Nội dung Môn học với các Shape -->
  <div id="mon-hoc" class="content">
    <h2>Môn học</h2>
    <div class="search-container">
      <input type="text" class="search-input" placeholder="Tìm kiếm tài liệu..." oninput="showSuggestions(this.value, 'mon-hoc')">
      <div class="suggestions" id="suggestions-mon-hoc"></div>
    </div>
    <div class="button-container" id="mon-hoc-buttons">
      <!-- Các nút shape với đường link, tất cả ban đầu đều ẩn -->
      <a href="https://docs.google.com/spreadsheets/d/15clADZFMDHkV1DZfZk-P8sEfVXDlvtYJ6tCWkrEuuOU/edit?usp=sharing" target="_blank">01 TOÁN - NGUYỄN THỊ NGỌC HÂN</a>
      <a href="https://docs.google.com/spreadsheets/d/1Ea_5Zxv5p5uqZa-hHAfM4dRfpddWWQDNlQUEzFc9vLg/edit?usp=sharing" target="_blank">02 TIN HỌC - NGUYỄN THỊ HỒNG NHUNG</a>
      <a href="https://docs.google.com/spreadsheets/d/1eBU92TdWakn0WZTcFeglHnF_mJhata2tIx_eys7d0qQ/edit?usp=sharing" target="_blank">03 GDTC - HOÀNG PHÚC TÝ</a>
      <a href="https://docs.google.com/spreadsheets/d/1bz0Hy9Zi6-h_ny9yhfSQooJYoSRaez9gDMt7kbxJNZU/edit?usp=sharing" target="_blank">04 TOÁN - ĐẶNG CAO VỸ</a>
      <a href="https://docs.google.com/spreadsheets/d/1DFwOfDAiozfeIu9HL2EmSg4cHmCJFW3ESc7qOr72tJY/edit?usp=sharing" target="_blank">05 NGỮ VĂN - PHAN THỊ PHƯƠNG THẢO</a>
      <a href="https://docs.google.com/spreadsheets/d/1GutwgT9_MoCAZJ0JmdCYAPziE5IeKGrAYEkLt0NWqNw/edit?usp=sharing" target="_blank">06 HĐTN - NGUYỄN HỮU TRÍ</a>
      <a href="https://docs.google.com/spreadsheets/d/1AbpregVh-fJsp5OOiKzX0VZrDMDl_Jo9ihen7CBRtVM/edit?usp=sharing" target="_blank">07 PPHT/HN - NGUYỄN HỮU TRÍ</a>
      <a href="https://docs.google.com/spreadsheets/d/1q2uyW8ZCSc5jZztasSDQJpdggPnXd7Vz9rf4-bxB-Po/edit?usp=sharing" target="_blank">08 KHOA HỌC TỰ NHIÊN - BÙI THỊ TƯỜNG VI</a>
      <a href="https://docs.google.com/spreadsheets/d/1xVR57tMNhMDeDfBB0Tm4Rm2KnbeiDCOEDww191lUVTA/edit?usp=sharing" target="_blank">09 NGỮ VĂN - TRẦN THỊ HIỀN</a>
      <a href="https://docs.google.com/spreadsheets/d/1uGIiiMtYdu4QkLAWku59t3DvMRCyW4aCxiLqzG7yiwQ/edit?usp=sharing" target="_blank">10 MAKERSPACE/CÔNG NGHỆ - BÙI THỊ TƯỜNG VI</a>
      <a href="https://docs.google.com/spreadsheets/d/1JOYzH35AyVWzrkDKqI5_ZlmwkBp9pZ2bmlB3ZQRXhzY/edit?usp=sharing" target="_blank">11 NGOẠI NGỮ 1 - HỒ THỊ TIN</a>
      <a href="https://docs.google.com/spreadsheets/d/1LeZv784PuLditTN3_CiKr0xd15Od-QWs1wYSHrsJrRg/edit?usp=sharing" target="_blank">12 KHOA HỌC TỰ NHIÊN - PHẠM THỊ THÙY NHIÊN</a>
      <a href="https://docs.google.com/spreadsheets/d/1JEH2KZsONxtJ6h9Bmiyp8Nt1QEmDjKzSxJ6DPUuUJnU/edit?usp=sharing" target="_blank">13 MAKERSPACE/CÔNG NGHỆ - PHẠM THỊ THÙY NHIÊN</a>
      <a href="https://docs.google.com/spreadsheets/d/12V_-K7JwuDYftgaYlMSrjrW-kZpUob4tU3V4Z5_yVXM/edit?usp=sharing" target="_blank">14 ÂM NHẠC - BÙI TRẦN QUANG</a>
      <a href="https://docs.google.com/spreadsheets/d/1DH_JoIEUBQOla9bwBG9IqZprL5EnfA6GDIhiA37S4hM/edit?usp=sharing" target="_blank">15 VÕ THUẬT - DƯƠNG VĂN VUI</a>
      <a href="https://docs.google.com/spreadsheets/d/1O5DF0SkmkVfbytxGgnAKcBFlug6y6qgUHXCvLvtNtfc/edit?usp=sharing" target="_blank">16 VÕ THUẬT - NGUYỄN NGỌC NINH</a>
      <a href="https://docs.google.com/spreadsheets/d/1oWSXma0yad5iZPzWlP2-0tpI8Q_dPeWq8_h28hdJywQ/edit?usp=sharing" target="_blank">17 GDCD - VÕ THỊ CẨM LOAN</a>
      <a href="https://docs.google.com/spreadsheets/d/1QseLUhr1_Mh-aFU3tj0I-M4O13PkEfn1MhptwtNG0pM/edit?usp=sharing" target="_blank">18 LỊCH SỬ VÀ ĐỊA LÝ - THẬP THỊ DIỆU THU</a>
      <a href="https://docs.google.com/spreadsheets/d/1aXQAmeOuVF9cVF0Gp8lLOPo5JeK3fdzOThQCidc8QOo/edit?usp=sharing" target="_blank">19 NGOẠI NGỮ 1 - NGUYỄN THỊ QUỲNH HOA</a>
      <a href="https://docs.google.com/spreadsheets/d/1jga2U518o-RQ9tfXWre7Y9IXzKQN0z97b6MajmgbgaQ/edit?usp=sharing" target="_blank">20 NGOẠI NGỮ 1 - NGUYỄN CÔNG TÀI</a>
      <a href="https://docs.google.com/spreadsheets/d/1wBhZkm5s_SSOsDzOZ9TsJKTP9yoEDY1SX3ZOs-NnM30/edit?usp=sharing" target="_blank">21 NGOẠI NGỮ 1 - HỒ THỊ HỒNG NHI</a>
      <a href="https://docs.google.com/spreadsheets/d/13TnXaFe36t_JibznWmvCZsWZ9rTKU6j9DRIhN3wUAK8/edit?usp=sharing" target="_blank">22 MỸ THUẬT - CAO XUÂN THI THIÊN</a>
      <a href="https://docs.google.com/spreadsheets/d/10wPUBtX96aNoMEaHAceY5OgaiGS74MhL2j0T8ljpNso/edit?usp=sharing" target="_blank">23 HỌC ĐƯỜNG - NGUYỄN VIẾT THUẬN</a>
      <a href="https://docs.google.com/spreadsheets/d/13Ofnr7TB41FBjV0sKTNBHlkEDEdMc5fNHGPuO4ax6x0/edit?usp=sharing" target="_blank">24 CHỦ NHIỆM - HỒ THỊ HỒNG NHI</a>
      <a href="https://docs.google.com/spreadsheets/d/1ZQHkROhB2orTpSwUPNK06CmwXYElCLMTNi8CgRxnJ4E/edit?usp=sharing" target="_blank">25 CHỦ NHIỆM - PHẠM THỊ THÙY NHIÊN</a>
      <a href="https://docs.google.com/spreadsheets/d/1lcQ4m7xx2mW_r0-Q8TjGlRjhs8fkPWMt6OJyNnN1Jiw/edit?usp=sharing" target="_blank">26 CHỦ NHIỆM - BÙI THỊ TƯỜNG VI</a>
      <a href="https://docs.google.com/spreadsheets/d/1Kq5VpDfDlziXkbXKVxEyvwfgB7ceOHsW3pxY-RjpwIE/edit?usp=sharing" target="_blank">27 CHỦ NHIỆM - NGUYỄN THỊ QUỲNH HOA</a>
      <a href="https://docs.google.com/spreadsheets/d/1PyCtYFPTZDFJlvLlDAmjL9JzpdysY1U04wxbIEPceDc/edit?usp=sharing" target="_blank">28 CHỦ NHIỆM - NGUYỄN CÔNG TÀI</a>
      <a href="https://docs.google.com/spreadsheets/d/1jZZhDZeK74ay6iILk_yBgRjvGKwW8_Tnj9gKbrYNZ8o/edit?usp=sharing" target="_blank">29 CHỦ NHIỆM - TRẦN THỊ HIỀN</a>
      <a href="https://docs.google.com/spreadsheets/d/1nGpzURdhTzkslwyL4y3ZsdnEr528HnBO3IVcn4iJi8E/edit?usp=sharing" target="_blank">30 GDCD - ĐOÀN KIM THỦY</a>
    </div>
  </div>

  <!-- Nội dung Lớp với các Shape -->
  <div id="lop" class="content">
    <h2>Lớp</h2>
    <div class="search-container">
      <input type="text" class="search-input" placeholder="Tìm kiếm lớp..." oninput="showSuggestions(this.value, 'lop')">
      <div class="suggestions" id="suggestions-lop"></div>
    </div>
    <div class="button-container" id="lop-buttons">
      <a href="https://docs.google.com/spreadsheets/d/1Ua3FpXSqq5_4LQFR7pb7hQUUK7lcdaBU0e2NkTkghwg/edit?usp=drive_link" target="_blank">6PA1</a>
      <a href="https://docs.google.com/spreadsheets/d/14aVSCQWXl3VGVC-rwWfUmdsy2NL71M3oQYtJlamSwmg/edit?usp=drive_link" target="_blank">6PA2</a>
      <a href="https://docs.google.com/spreadsheets/d/14KBCII5nxJ9uYtdrQQuNL-BEzG35pPyZxT945iFCGZA/edit?usp=drive_link" target="_blank">7PA1</a>
      <a href="https://docs.google.com/spreadsheets/d/1y43UeHmHKodRwAm2c2FuwaiHzFV75MCIOIU8cGAbln8/edit?usp=drive_link" target="_blank">7PA2</a>
      <a href="https://docs.google.com/spreadsheets/d/1gp254o4SDBC5-P0NhxQTEJCZA4uGCYBJ8fDFwHBDHXg/edit?usp=drive_link" target="_blank">8PA1</a>
      <a href="https://docs.google.com/spreadsheets/d/1zpDgivZznDy4c2qhBLXMOHzamHZRt1R4FeI0wGOFQV8/edit?usp=drive_link" target="_blank">9PA1</a>
    </div>
  </div>

  <script>
    const data = {
      "mon-hoc": [
        "01 TOÁN - NGUYỄN THỊ NGỌC HÂN",
        "02 TIN HỌC - NGUYỄN THỊ HỒNG NHUNG",
        "03 GDTC - HOÀNG PHÚC TÝ",
        "04 TOÁN - ĐẶNG CAO VỸ",
        "05 NGỮ VĂN - PHAN THỊ PHƯƠNG THẢO",
        "06 HĐTN - NGUYỄN HỮU TRÍ",
        "07 PPHT/HN - NGUYỄN HỮU TRÍ",
        "08 KHOA HỌC TỰ NHIÊN - BÙI THỊ TƯỜNG VI",
        "09 NGỮ VĂN - TRẦN THỊ HIỀN",
        "10 MAKERSPACE/CÔNG NGHỆ - BÙI THỊ TƯỜNG VI",
        "11 NGOẠI NGỮ 1 - HỒ THỊ TIN",
        "12 KHOA HỌC TỰ NHIÊN - PHẠM THỊ THÙY NHIÊN",
        "13 MAKERSPACE/CÔNG NGHỆ - PHẠM THỊ THÙY NHIÊN",
        "14 ÂM NHẠC - BÙI TRẦN QUANG",
        "15 VÕ THUẬT - DƯƠNG VĂN VUI",
        "16 VÕ THUẬT - NGUYỄN NGỌC NINH",
        "17 GDCD - VÕ THỊ CẨM LOAN",
        "18 LỊCH SỬ VÀ ĐỊA LÝ - THẬP THỊ DIỆU THU",
        "19 NGOẠI NGỮ 1 - NGUYỄN THỊ QUỲNH HOA",
        "20 NGOẠI NGỮ 1 - NGUYỄN CÔNG TÀI",
        "21 NGOẠI NGỮ 1 - HỒ THỊ HỒNG NHI",
        "22 MỸ THUẬT - CAO XUÂN THI THIÊN",
        "23 HỌC ĐƯỜNG - NGUYỄN VIẾT THUẬN",
        "24 CHỦ NHIỆM - HỒ THỊ HỒNG NHI",
        "25 CHỦ NHIỆM - PHẠM THỊ THÙY NHIÊN",
        "26 CHỦ NHIỆM - BÙI THỊ TƯỜNG VI",
        "27 CHỦ NHIỆM - NGUYỄN THỊ QUỲNH HOA",
        "28 CHỦ NHIỆM - NGUYỄN CÔNG TÀI",
        "29 CHỦ NHIỆM - TRẦN THỊ HIỀN",
        "30 GDCD - ĐOÀN KIM THỦY"
      ],
      "lop": [
        "6PA1",
        "6PA2",
        "7PA1",
        "7PA2",
        "8PA1",
        "9PA1"
      ]
    };

    function showContent(contentId) {
      const contents = document.querySelectorAll('.content');
      contents.forEach(content => content.classList.remove('active'));
      const selectedContent = document.getElementById(contentId);
      if (selectedContent) {
        selectedContent.classList.add('active');
      }
    }

    function showSuggestions(query, tabId) {
      const suggestions = document.getElementById(`suggestions-${tabId}`);
      suggestions.innerHTML = "";
      if (query.length === 0) {
        suggestions.style.display = "none";
        return;
      }

      const matchedItems = data[tabId].filter(item => item.toLowerCase().includes(query.toLowerCase()));
      matchedItems.forEach(item => {
        const div = document.createElement("div");
        div.classList.add("suggestion-item");
        div.textContent = item;
        div.onclick = () => selectSuggestion(item, tabId);
        suggestions.appendChild(div);
      });

      suggestions.style.display = matchedItems.length > 0 ? "block" : "none";
    }

    function selectSuggestion(item, tabId) {
      const suggestions = document.getElementById(`suggestions-${tabId}`);
      suggestions.style.display = "none";
      const buttons = document.getElementById(`${tabId}-buttons`).querySelectorAll("a");
      buttons.forEach(button => {
        button.style.display = button.textContent === item ? "inline-block" : "none";
      });
    }

    document.addEventListener('DOMContentLoaded', () => showContent('trang-chu'));
  </script>

</body>
</html>
