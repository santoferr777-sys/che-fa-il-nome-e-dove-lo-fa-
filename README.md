# chi?cosa fa?dove?quando?
/index.html
/style.css
/script.js
<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>chi?cosa fa?dove?quando?</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Chi?cosa fa?dove?quando?</h1>

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
// Stato del gioco
let currentTurn = 0;
const maxTurns = 4;
let sentenceParts = [];

// Elementi della UI
const input = document.getElementById("inputText");
const submitBtn = document.getElementById("submitBtn");
const instructions = document.getElementById("instructions");
const gameDiv = document.getElementById("game");
const resultDiv = document.getElementById("result");
const finalPhrase = document.getElementById("finalPhrase");

// Istruzioni per ogni turno
const turnInstructions = [
  "Chi? (es. 'Mario')",
  "Cosa fa? (es. 'mangia')",
  "Dove? (es. 'nel parco')",
  "Quando? (es. 'di notte')"
];

// Mostra prima istruzione
instructions.textContent = turnInstructions[currentTurn];

// Quando si clicca "Invia"
submitBtn.addEventListener("click", () => {
  const text = input.value.trim();
  if (text === "") return;

  // Salva la parte scritta
  sentenceParts.push(text);
  input.value = "";
  currentTurn++;

  // Passa al turno successivo o mostra la frase
  if (currentTurn < maxTurns) {
    instructions.textContent = turnInstructions[currentTurn];
  } else {
    // Costruisci e mostra la frase finale
    const [chi, cosa Fa, dove, quando] = sentenceParts;
    const fraseFinale = ${chi} ${cosaFa} ${dove} ${quando}.;

    gameDiv.style.display = "none";
    resultDiv.style.display = "block";
    finalPhrase.textContent = fraseFinale;
  }
});
