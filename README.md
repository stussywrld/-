<!DOCTYPE html>
<html lang="kk">
<head>
  <meta charset="UTF-8">
  <title>Үйлену тойына RSVP</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f9f6ff;
      margin: 0;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: #6a0dad;
    }
    .btn {
      display: inline-block;
      margin: 10px;
      padding: 12px 18px;
      border: none;
      border-radius: 8px;
      background: #6a0dad;
      color: #fff;
      font-size: 16px;
      cursor: pointer;
      transition: .2s;
    }
    .btn:hover {
      opacity: 0.8;
    }
    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #333;
    }
    input {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
      width: 60%;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>Біздің үйлену тойына RSVP</h1>
  <p>Атыңды жазып, таңдауыңды белгіле:</p>

  <input type="text" id="name" placeholder="Атыңды енгіз">
  <br>

  <button class="btn" onclick="submitRSVP('Барамын')">Барамын</button>
  <button class="btn" onclick="submitRSVP('Бармаймын')">Бармаймын</button>
  <button class="btn" onclick="submitRSVP('Жалғыз барамын')">Жалғыз барамын</button>

  <div id="result"></div>

  <script>
    function submitRSVP(choice) {
      const name = document.getElementById('name').value.trim();
      if (!name) {
        alert("Алдымен атыңды жаз!");
        return;
      }
      document.getElementById('result').innerText = name + " таңдады: " + choice;
    }
  </script>
</body>
</html>
