# chi?cosa fa?dove?quando?
/index.html
/style.css
/script.js
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>che fa chi e dove e quando lo fa?</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Chi fa chi e dove e quando lo fa?</h1>

  <div id="game">
    <p id="instructions">Scrivi la tua parte della frase:</p>
    <textarea id="inputText" placeholder="Scrivi qui..." rows="3"></textarea>
    <br>
    <button id="submitBtn">Invia</button>
  </div>

  <div id="result" style="display:none;">
    <h2>Frase completata:</h2>
    <p id="finalPhrase"></p>
    <button onclick="location.reload()">Gioca ancora</button>
  </div>

  <script src="script.js"></script>
</body>
</html>
