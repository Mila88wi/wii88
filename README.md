<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teclado</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .keyboard-row {
            display: flex;
            justify-content: center;
            margin-bottom: 10px;
        }
        .button {
            padding: 10px 20px;
            margin: 5px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Teclado</h1>
    <div class="keyboard">
        <div class="keyboard-row">
            <div class="button" onclick="handleButtonClick('Q')">Q</div>
            <div class="button" onclick="handleButtonClick('W')">W</div>
            <div class="button" onclick="handleButtonClick('E')">E</div>
            <div class="button" onclick="handleButtonClick('R')">R</div>
            <div class="button" onclick="handleButtonClick('T')">T</div>
            <div class="button" onclick="handleButtonClick('Y')">Y</div>
            <div class="button" onclick="handleButtonClick('U')">U</div>
            <div class="button" onclick="handleButtonClick('I')">I</div>
            <div class="button" onclick="handleButtonClick('O')">O</div>
            <div class="button" onclick="handleButtonClick('P')">P</div>
        </div>
        <div class="keyboard-row">
            <div class="button" onclick="handleButtonClick('A')">A</div>
            <div class="button" onclick="handleButtonClick('S')">S</div>
            <div class="button" onclick="handleButtonClick('D')">D</div>
            <div class="button" onclick="handleButtonClick('F')">F</div>
            <div class="button" onclick="handleButtonClick('G')">G</div>
            <div class="button" onclick="handleButtonClick('H')">H</div>
            <div class="button" onclick="handleButtonClick('J')">J</div>
            <div class="button" onclick="handleButtonClick('K')">K</div>
            <div class="button" onclick="handleButtonClick('L')">L</div>
        </div>
        <div class="keyboard-row">
            <div class="button" onclick="handleButtonClick('Z')">Z</div>
            <div class="button" onclick="handleButtonClick('X')">X</div>
            <div class="button" onclick="handleButtonClick('C')">C</div>
            <div class="button" onclick="handleButtonClick('V')">V</div>
            <div class="button" onclick="handleButtonClick('B')">B</div>
            <div class="button" onclick="handleButtonClick('N')">N</div>
            <div class="button" onclick="handleButtonClick('M')">M</div>
        </div>
        <div class="keyboard-row">
            <div class="button" onclick="handleButtonClick(' ')">Espacio</div>
            <div class="button" onclick="handleBackspace()">Borrar</div>
        </div>
    </div>
    <input type="text" id="result" placeholder="Resultado" readonly>

    <script>
        function handleButtonClick(char) {
            document.getElementById('result').value += char;
        }

        function handleBackspace() {
            const currentValue = document.getElementById('result').value;
            document.getElementById('result').value = currentValue.slice(0, -1);
        }
    </script>
</body>
</html>
