<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Chemiscalc</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f7ff;
      text-align: center;
      padding: 30px;
    }

    .box {
      max-width: 450px;
      margin: auto;
      background: white;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 4px 15px #aaa;
    }

    h1 {
      color: #1769aa;
    }

    input {
      width: 90%;
      padding: 12px;
      margin: 10px;
      border-radius: 10px;
      border: 1px solid #aaa;
      font-size: 16px;
    }

    button {
      padding: 12px 25px;
      background: #1769aa;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
    }

    #result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>🧪 Chemiscalc</h1>
    <p>Modda miqdorini hisoblash</p>

    <input type="number" id="mass" placeholder="Massani kiriting (g)">
    <input type="number" id="molar" placeholder="Molyar massani kiriting (g/mol)">

    <br>

    <button onclick="calculate()">Hisoblash</button>

    <div id="result"></div>
  </div>

  <script>
    function calculate() {
      let mass = Number(document.getElementById("mass").value);
      let molar = Number(document.getElementById("molar").value);

      if (mass > 0 && molar > 0) {
        let n = mass / molar;
        document.getElementById("result").innerHTML =
          "Modda miqdori: " + n.toFixed(3) + " mol";
      } else {
        document.getElementById("result").innerHTML =
          "Iltimos, qiymatlarni kiriting!";
      }
    }
  </script>

</body>
</html># Chemiscalculator
A simple application for learning chemistry
