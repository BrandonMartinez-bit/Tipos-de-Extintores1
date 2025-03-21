# Tipos-de-Extintores
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tipos de Extintores</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        header {
            text-align: center;
            margin-bottom: 20px;
        }
        .tabs {
            display: flex;
            cursor: pointer;
            background-color: #f4f4f4;
            padding: 10px;
        }
        .tab {
            flex: 1;
            text-align: center;
            padding: 10px;
            border: 1px solid #ccc;
            border-bottom: none;
            background-color: #e0e0e0;
        }
        .tab.active {
            background-color: #fff;
            font-weight: bold;
        }
        .content {
            border: 1px solid #ccc;
            padding: 20px;
            display: none;
        }
        .content.active {
            display: block;
        }
        img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 10px auto;
        }
    </style>
    <script>
        function showContent(id) {
            const contents = document.querySelectorAll('.content');
            const tabs = document.querySelectorAll('.tab');
            contents.forEach(content => content.classList.remove('active'));
            tabs.forEach(tab => tab.classList.remove('active'));
            document.getElementById(id).classList.add('active');
            document.querySelector(`[data-tab="${id}"]`).classList.add('active');
        }
    </script>
</head>
<body>

    <!-- Portada -->
    <header>
        <img src="escudo.png" alt="" style="width: 150px;">
        <h1>Universidad Autónoma del Estado de México</h1>
        <h2>Licenciatura en Informática Administrativa</h2>
        <h3>Materia: Instalaciones y Seguridad Informática</h3>
        <h3>Nombre: Ángel Brandon Martínez Rodríguez</h3>
        <h3>Tema: Tipos de Extintores</h3>
    </header>

    <hr>

    <!-- Contenido con pestañas -->
    <h1>Tipos de Extintores</h1>
    <div class="tabs">
        <div class="tab active" data-tab="co2" onclick="showContent('co2')">Extintor de CO₂</div>
        <div class="tab" data-tab="polvo" onclick="showContent('polvo')">Extintor de Polvo Químico</div>
        <div class="tab" data-tab="agua" onclick="showContent('agua')">Extintor de Agua</div>
        <div class="tab" data-tab="espuma" onclick="showContent('espuma')">Extintor de Espuma</div>
        <div class="tab" data-tab="halon" onclick="showContent('halon')">Extintor de Halón</div>
    </div>

    <div id="co2" class="content active">
        <h2>Extintor de CO₂</h2>
        <p><strong>Apto para Material Eléctrico:</strong> Sí</p>
        <p><strong>Características:</strong> No deja residuos, es limpio y no conductor.</p>
        <p><strong>Componentes:</strong> Dióxido de carbono comprimido.</p>
        <img src="CO2.jpg" alt="">
    </div>

    <div id="polvo" class="content">
        <h2>Extintor de Polvo Químico Seco</h2>
        <p><strong>Apto para Material Eléctrico:</strong> A veces (si es clase C)</p>
        <p><strong>Características:</strong> Versátil, adecuado para fuegos clase A, B y C.</p>
        <p><strong>Componentes:</strong> Polvo químico (fosfato monoamónico).</p>
        <img src="Extintor de Polvo Químico Seco.jpg" alt="">
    </div>

    <div id="agua" class="content">
        <h2>Extintor de Agua</h2>
        <p><strong>Apto para Material Eléctrico:</strong> No</p>
        <p><strong>Características:</strong> Solo para fuegos de clase A (combustibles sólidos).</p>
        <p><strong>Componentes:</strong> Agua presurizada.</p>
        <img src="Extintor de Agua.jpg" alt="">
    </div>

    <div id="espuma" class="content">
        <h2>Extintor de Espuma</h2>
        <p><strong>Apto para Material Eléctrico:</strong> No</p>
        <p><strong>Características:</strong> Efectivo en líquidos inflamables (clase B).</p>
        <p><strong>Componentes:</strong> Agente espumante y agua.</p>
        <img src="Extintor de Espuma.jpg" alt="">
    </div>

    <div id="halon" class="content">
        <h2>Extintor de Halón</h2>
        <p><strong>Apto para Material Eléctrico:</strong> Sí</p>
        <p><strong>Características:</strong> Limpio y no conductor, sustituido por gases ecológicos.</p>
        <p><strong>Componentes:</strong> Halón o agente halogenado.</p>
        <img src="Extintor de Halón.jpg" alt="">
    </div>

</body>
</html>
