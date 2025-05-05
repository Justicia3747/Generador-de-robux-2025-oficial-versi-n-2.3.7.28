<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Hola Spam</title>
</head>
<body>
  <h1>Haz clic para saludar 100,000 veces</h1>
  <button onclick="abrirVentanas()">¡Empezar!</button>

  <script>
    function abrirVentanas() {
      for (let i = 0; i < 100000; i++) {
        const win = window.open("", "_blank");
        if (win) {
          win.document.write("<h1>Hola " + (i + 1) + "</h1>");
          win.document.title = "Hola " + (i + 1);
        } else {
          alert("El navegador bloqueó las ventanas emergentes.");
          break;
        }
      }
    }
  </script>
</body>
</html>
