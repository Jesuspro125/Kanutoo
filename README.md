<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comprobante de Pago</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0px 4px 8px rgba(0,0,0,0.2);
            width: 300px;
            height: 700px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .logo {
            width: 140px;
            height: auto;
            margin: 5px auto;
        }
        h1 {
            color: #2d9cdb;
            font-size: 24px;
            margin-top: 0px;
            margin-bottom: 12px;
        }
        .details {
            text-align: left;
            font-size: 16px;
        }
        .details p {
            margin: 10px 0;
            display: flex;
            flex-direction: column;
        }
        .details input {
            border: none;
            font-size: 16px;
            text-align: left;
            background: transparent;
            width: 100%;
        }
        .buttons {
            margin-top: 15px;
        }
        .buttons button {
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            width: 100%;
            margin-bottom: 8px;
        }
        .edit {
            background-color: #f2994a;
            color: white;
        }
        .save {
            background-color: #2d9cdb;
            color: white;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3PsVKQKTaFupmLKL4ZvJi2KL_gX2WQWjEww&usqp=CAU" alt="Logo" class="logo">
        <h1>¡Pago exitoso!</h1>
        <div class="details">
            <p><strong>Cliente:</strong><input type="text" value="Josué y su amiga traídores del grupo"></p>
            <p><strong>Operación:</strong><input type="text" value="Pago de servicios"></p>
            <p><strong>Cantidad:</strong><input type="text" value="$50.000"></p>
            <p><strong>Número de cuenta:</strong><input type="text" value="3001234567"></p>
            <p><strong>Fecha:</strong><input type="text" value="4/5/2025"></p>
            <p><strong>No. de referencia:</strong><input type="text" value="532449231"></p>
            <p><strong>Folio:</strong><input type="text" value="56288196524678"></p>
        </div>
        <div class="buttons">
            <button class="edit" onclick="toggleEdit()">Editar comprobante</button>
            <button class="save">Guardar comprobante</button>
        </div>
    </div>

    <script>
        function toggleEdit() {
            const inputs = document.querySelectorAll(".details input");
            inputs.forEach(input => {
                input.toggleAttribute("readonly"); // Alterna el estado de edición
            });
        }
    </script>
</body>
</html>
