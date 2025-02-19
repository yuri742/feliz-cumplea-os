
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Es tu cumpleaños</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin-top: 50px;
        }
        h1 {
            color: #ff4500;
        }
        #mensaje {
            font-size: 18px;
            font-weight: bold;
            color: red;
            display: none;
        }
        #pregunta2 {
            display: none;
        }
        #botonNo {
            font-size: 16px;
            transition: all 0.3s ease;
            }
    </style>
</head>
<body>
    <!-- Primera Pregunta -->
    <div id="pregunta1">
        <h1>¿Es tu cumpleaños?</h1>
        <button onclick="cambiarPantalla()">Sí</button>
        <button onclick="mostrarMensaje()">No</button>
        <p id="mensaje">Eres pendejo, si es tu cumpleaños dale "Sí".</p>
    </div>

    <!-- Segunda Pregunta -->
    <div id="pregunta2">
        <h1>¿Quieres un regalo?</h1>
        <button onclick="agrandarNo()">Sí</button>
        <button id="botonNo" onclick="despedida()">No</button>
    </div>

    <script>
        function cambiarPantalla() {
            document.getElementById("pregunta1").style.display = "none";
            document.getElementById("pregunta2").style.display = "block";
        }

        function mostrarMensaje() {
            document.getElementById("mensaje").style.display = "block";
        }

  function agrandarNo() {
            let botonNo = document.getElementById("botonNo");
            let tamaño = parseFloat(window.getComputedStyle(botonNo).fontSize);
            botonNo.style.fontSize = (tamaño + 10) + "px"; // Aumenta el tamaño del botón "No"
        }

        function despedida() {
            document.getElementById("pregunta2").innerHTML = "<h1>Gracias por tu humildad, adiós.</h1>";
        }
    </script>
</body>
</html>

