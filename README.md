# rutthoivang
<!DOCTYPE html><html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rút Thỏi Vàng - Play Together</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('https://i.imgur.com/fR8XwXk.jpg') no-repeat center center fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background: rgba(255, 255, 255, 0.95);
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
    }
    h1 {
      color: #e83c77;
      font-size: 28px;
    }
    input, select, button {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      font-size: 16px;
      border-radius: 8px;
      border: 1px solid #ccc;
    }
    button {
      background-color: #ff69b4;
      color: white;
      border: none;
      cursor: pointer;
    }
    .success {
      display: none;
      color: green;
      font-weight: bold;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="https://i.imgur.com/UhAYPhU.png" alt="Logo" width="120">
    <h1>Rút Thỏi Vàng Play Together</h1>
    <input type="text" id="playerId" placeholder="Nhập ID người chơi">
    <select id="goldAmount">
      <option value="100">100 Thỏi Vàng</option>
      <option value="300">300 Thỏi Vàng</option>
      <option value="500">500 Thỏi Vàng</option>
      <option value="1000">1000 Thỏi Vàng</option>
    </select>
    <button onclick="withdrawGold()">Rút Ngay</button>
    <div class="success" id="successMsg">Đã rút thành công! Vào game kiểm tra hộp thư.</div>
  </div>
  <script>
    function withdrawGold() {
      const id = document.getElementById('playerId').value;
      if (!id) return alert('Vui lòng nhập ID người chơi!');
      document.getElementById('successMsg').style.display = 'none';
      alert('Đang xử lý...');
      setTimeout(() => {
        document.getElementById('successMsg').style.display = 'block';
      }, 2000);
    }
  </script>
</body>
</html>
