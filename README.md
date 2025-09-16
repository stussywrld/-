# -<!doctype html>
<html lang="kk">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Үйлену тойына RSVP</title>
  <style>
    body{font-family:Arial, sans-serif;background:#f9f6ff;margin:0;padding:20px;text-align:center}
    h1{color:#6a0dad}
    .btn{display:inline-block;margin:10px;padding:12px 18px;border:none;border-radius:8px;
         background:#6a0dad;color:#fff;font-size:16px;cursor:pointer;transition:.2s}
    .btn:hover{opacity:0.8}
    #result{margin-top:20px;font-weight:bold;color:#333}
    input{padding:10px;border:1px solid #ccc;border-radius:6px;width:60%;margin-top:10px}
  </style>
</head>
<body>
  <h1>Біздің үйлену тойына RSVP</h1>
  <p>Атыңды жазып, таңдауыңды белгіле:</p>
  <input id="name" type="text" placeholder="Атыңды енгіз" />
  <div>
    <button class="btn" onclick="submitRSVP('Барамын')">Барамын</button>
    <button class="btn" onclick="submitRSVP('Бармаймын')">Бармаймын</button>
    <button class="btn" onclick="submitRSVP('Жалғыз барамын')">Жалғыз барамын</button>
  </div>
  <div id="result"></div>

  <script>
    function submitRSVP(choice){
      const name = document.getElementById('name').value.trim();
      if(!name){
        alert("Алдымен атыңды жаз!");
        return;
      }
      // Жауапты шығару
      document.getElementById('result').innerText = 
        name + " таңдады: " + choice;
      
      // Егер кейін серверге/Google Sheets-ке сақтағың келсе — осы жерге код қосылады
    }
  </script>
</body>
</html>
