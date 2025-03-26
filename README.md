<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Acceso Protegido</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        input { padding: 10px; margin: 10px; }
        button { padding: 10px 20px; cursor: pointer; }
    </style>
    <script>
        // Bloquear copiar/pegar
        document.addEventListener("copy", (event) => event.preventDefault());
        document.addEventListener("paste", (event) => event.preventDefault());

        function verificar() {
            var password = document.getElementById("password").value;

            // Contraseña correcta
            if (password === "1234") {  
                sessionStorage.setItem("accesoPermitido", "true"); // Guarda acceso en la sesión
                window.location.href = "https://djdm1995.github.io/PROVEEDOR2.github.io/"; // Redirige a la página protegida
            } else {
                alert("❌ Contraseña incorrecta. Intenta de nuevo.");
            }
        }
    </script>
</head>
<body>
    <h2>🔒 Página Protegida</h2>
    <p>Ingrese la contraseña para acceder al contenido:</p>
    <input type="password" id="password" placeholder="Escriba la contraseña">
    <button onclick="verificar()">🔑 Acceder</button>
</body>
</html>
