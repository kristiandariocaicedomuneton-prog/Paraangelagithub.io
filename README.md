# Para-Angela
Debes seleccionar una opcion. 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>💖</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #ffe6f0;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
    }
    .box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    h1 {
      margin-bottom: 20px;
    }
    button {
      padding: 10px 20px;
      margin: 10px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    .yes {
      background: #ff4d88;
      color: white;
    }
    .no {
      background: #ccc;
    }
    img {
      margin-top: 20px;
      max-width: 250px;
      border-radius: 15px;
    }
  </style>
</head>
<body>
  <div class="box" id="content">
    <h1 id="question">¿Me quieres?</h1>
    <button class="yes" onclick="sayYes()">Sí</button>
    <button class="no" onclick="sayNo()">No</button>
  </div>

  <script>
    let noCount = 0;
    const questions = [
      "¿Segura?",
      "¿Segurísima?",
      "¿De verdad no me quieres?",
      "Piénsalo bien 🥺",
      "Última oportunidad 😢"
    ];

    function sayNo() {
      const q = document.getElementById("question");
      q.textContent = questions[Math.min(noCount, questions.length - 1)];
      noCount++;
    }

    function sayYes() {
      const content = document.getElementById("content");
      content.innerHTML = `
        <h1>Yo también a ti ❤️</h1>
        <img src="https://images.unsplash.com/photo-1601758123927-1961a4f4a5b3" alt="Perrito feliz">
      `;
    }
  </script>
</body>
</html>
