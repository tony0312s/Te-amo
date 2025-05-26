<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Te Amo Infinito</title>
  <style>
    body {
      margin: 0;
      background: black;
      color: #ff4dd2;
      font-family: 'Courier New', Courier, monospace;
      overflow: hidden;
    }

    .matrix {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      height: 100vh;
      width: 100vw;
    }

    .column {
      display: flex;
      flex-direction: column;
      animation: scroll 10s linear infinite;
      margin: 0 10px;
    }

    .text {
      font-size: 18px;
      line-height: 1.5;
      text-align: center;
    }

    @keyframes scroll {
      0% {
        transform: translateY(0%);
      }
      100% {
        transform: translateY(-100%);
      }
    }

    .message {
      position: absolute;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      text-align: center;
      font-size: 20px;
      padding: 10px 20px;
      background-color: rgba(0, 0, 0, 0.6);
      border-radius: 10px;
      z-index: 10;
    }
  </style>
</head>
<body>
  <div class="matrix" id="matrix"></div>

  <div class="message">
    No fue un error de seguridad...<br>
    fue un acceso intencional,<br>
    para que sepas que me importas.
  </div>

  <script>
    const matrix = document.getElementById('matrix');
    const columns = 50; // Número de columnas
    const rows = 30;    // Número de "TE AMO" por columna

    for (let i = 0; i < columns; i++) {
      const col = document.createElement('div');
      col.className = 'column';
      for (let j = 0; j < rows; j++) {
        const text = document.createElement('div');
        text.className = 'text';
        text.innerText = 'TE\nAMO';
        col.appendChild(text);
      }
      matrix.appendChild(col);
    }
  </script>
</body>
</html>
