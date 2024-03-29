<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Nutricional</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            background-color: #4CAF50; /* Color verde deportivo */
            font-family: 'Arial', sans-serif; /* Cambia la fuente a Arial */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh; /* Hace que el cuerpo ocupe toda la altura de la ventana */
            margin: 0; /* Elimina el margen predeterminado */
            background-image: url('Almacenamiento interno/Download/istockphoto-1635731898-1024x1024-transformed.jpeg'); /* Agrega la imagen de fondo */
            background-size: cover; /* Cubre todo el fondo */
            background-repeat: no-repeat; /* No se repite la imagen */
            background-position: center; /* Centra la imagen */
            position: relative; /* Establece la posición relativa para que los elementos floten sobre el fondo */
        }

        header {
            margin-bottom: 20px; /* Añade espacio entre el encabezado y el contenido */
            text-align: center; /* Centra el texto en el encabezado */
            color: #fff; /* Color del texto */
            z-index: 1; /* Asegura que el encabezado esté sobre el fondo */
        }

        h1 {
            font-size: 36px; /* Tamaño del texto del nombre */
            margin-bottom: 10px; /* Añade espacio entre el nombre y las opciones de inicio de sesión */
        }

        #opcionesInicioSesion {
            text-align: center; /* Centra las opciones de inicio de sesión */
            z-index: 1; /* Asegura que las opciones estén sobre el fondo */
        }

        button {
            background-color: #fff; /* Color de fondo de los botones */
            color: #4CAF50; /* Color del texto de los botones */
            border: none; /* Sin borde */
            padding: 10px 20px; /* Espaciado interno */
            border-radius: 5px; /* Bordes redondeados */
            margin: 5px; /* Margen entre los botones */
            cursor: pointer; /* Cambia el cursor al pasar sobre los botones */
            font-size: 16px; /* Tamaño del texto */
            transition: background-color 0.3s ease; /* Transición suave del color de fondo */
        }

        button:hover {
            background-color: #e7e7e7; /* Color de fondo al pasar el cursor sobre los botones */
        }

        a {
            color: #fff; /* Color del texto de los enlaces */
            text-decoration: none; /* Sin subrayado */
            margin-top: 10px; /* Margen superior */
            display: block; /* Mostrar como bloque para ocupar todo el ancho */
            transition: color 0.3s ease; /* Transición suave del color del texto */
        }

        a:hover {
            color: #e7e7e7; /* Color del texto al pasar el cursor sobre los enlaces */
        }

        footer {
            margin-top: 20px; /* Margen superior */
            color: #fff; /* Color del texto del pie de página */
            font-size: 14px; /* Tamaño del texto del pie de página */
            z-index: 1; /* Asegura que el pie de página esté sobre el fondo */
        }
    </style>
</head>
<body>
    <header>
        <h1>CALCULADORA NUTRICIONAL</h1>
    </header>

    <main>
        <div class="container">
            <section id="opcionesInicioSesion">
                <button onclick="location.href='registro.html'">Crear cuenta</button>
                <button onclick="location.href='inicio_sesion.html'">Iniciar sesión</button>
                <a href="#" onclick="recuperarContrasena()">¿Olvidaste tu contraseña?</a>
            </section>
        </div>
    </main>

    <footer>
        <p>&copy; 2024 Calculadora Nutricional. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
