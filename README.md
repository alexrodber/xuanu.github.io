#<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sidrería El Xuañu | Restaurante & Experiencia Gastronómica</title>
    <style>
        /* --- ESTILOS GENERALES Y VARIABLES --- */
        :root {
            --color-primario: #c5a880; /* Dorado / Champán elegante */
            --color-secundario: #e2c792; /* Dorado claro */
            --color-oscuro: #111827; /* Fondo oscuro premium */
            --color-gris-claro: #faf9f6; /* Blanco roto / Hueso */
            --color-texto: #374151;
            --color-blanco: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--color-gris-claro);
            color: var(--color-texto);
            line-height: 1.6;
        }

        .contenedor {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- MENÚ DE NAVEGACIÓN --- */
        header {
            background-color: rgba(17, 24, 39, 0.98);
            backdrop-filter: blur(5px);
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 18px 0;
        }

        .logo {
            color: var(--color-blanco);
            font-size: 24px;
            font-weight: bold;
            text-decoration: none;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--color-primario);
        }

        .nav-links {
            display: flex;
            list-style: none;
            align-items: center;
        }

        .nav-links li {
            margin-left: 25px;
        }

        .nav-links a {
            color: #9ca3af;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--color-blanco);
        }

        .telefono-nav {
            color: var(--color-primario) !important;
            font-weight: bold;
        }

        .btn-nav {
            background-color: var(--color-primario);
            color: var(--color-oscuro) !important;
            padding: 8px 18px;
            border-radius: 4px;
            font-weight: bold;
            transition: background 0.3s !important;
        }

        .btn-nav:hover {
            background-color: var(--color-secundario);
        }

        /* --- PORTADA / HERO --- */
        .hero {
            min-height: 95vh;
            background-image: linear-gradient(135deg, rgba(17, 24, 39, 0.95) 45%, rgba(0, 0, 0, 0.2)), url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&q=80&w=1600');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            color: var(--color-blanco);
            padding-top: 120px;
            padding-bottom: 60px;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 50px;
            align-items: center;
        }

        .hero-texto h1 {
            font-size: 48px;
            line-height: 1.2;
            margin-bottom: 20px;
            font-weight: 800;
            letter-spacing: -1px;
        }

        .hero-texto h1 span {
            color: var(--color-primario);
        }

        .hero-texto p {
            font-size: 18px;
            color: #d1d5db;
            margin-bottom: 25px;
        }

        /* Tarjeta de Reserva */
        .tarjeta-registro {
            background-color: var(--color-blanco);
            color: var(--color-oscuro);
            padding: 35px;
            border-radius: 8px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.3);
        }

        .tarjeta-registro h3 {
            font-size: 24px;
            margin-bottom: 8px;
            color: var(--color-oscuro);
            text-align: center;
        }

        .tarjeta-registro p {
            font-size: 14px;
            color: #6b7280;
            margin-bottom: 25px;
            text-align: center;
        }

        .form-group {
            margin-bottom: 18px;
        }

        .form-group label {
            display: block;
            font-size: 13px;
            font-weight: 600;
            margin-bottom: 6px;
            color: #4b5563;
        }

        .form-group input {
            width: 100%;
            padding: 12px;
            border: 1px solid #d1d5db;
            border-radius: 4px;
            font-size: 15px;
            outline: none;
            transition: border-color 0.3s;
        }

        .form-group input:focus {
            border-color: var(--color-primario);
        }

        .btn-registro {
            width: 100%;
            background-color: var(--color-primario);
            color: var(--color-oscuro);
            padding: 14px;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }

        .btn-registro:hover {
            background-color: var(--color-secundario);
        }

        .texto-consentimiento {
            font-size: 11px !important;
            color: #6b7280;
            line-height: 1.4;
            margin-top: 15px;
            text-align: justify;
            border-top: 1px solid #e5e7eb;
            padding-top: 12px;
        }

        /* --- SECCIONES GENERALES --- */
        .seccion {
            padding: 90px 0;
        }

        .seccion-alt {
            background-color: var(--color-blanco);
        }

        .titulo-seccion {
            text-align: center;
            font-size: 32px;
            color: var(--color-oscuro);
            margin-bottom: 15px;
            font-weight: 700;
            letter-spacing: 1px;
        }

        .subtitulo-seccion {
            text-align: center;
            color: #6b7280;
            max-width: 600px;
            margin: 0 auto 60px auto;
            font-size: 16px;
        }

        /* --- BENEFICIOS / VALORES --- */
        .beneficios-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .beneficio-card {
            background-color: var(--color-blanco);
            padding: 35px 30px;
            border-radius: 4px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            border: 1px solid #e5e7eb;
            text-align: center;
        }

        .beneficio-icono {
            font-size: 36px;
            margin-bottom: 15px;
            color: var(--color-primario);
        }

        .beneficio-card h3 {
            font-size: 20px;
            color: var(--color-oscuro);
            margin-bottom: 12px;
        }

        .beneficio-card p {
            font-size: 15px;
            color: #6b7280;
        }

        /* --- NUESTRA FILOSOFÍA --- */
        .detalles-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .detalles-imagen img {
            width: 100%;
            border-radius: 6px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        .pasos-lista {
            list-style: none;
        }

        .paso-item {
            display: flex;
            margin-bottom: 25px;
        }

        .paso-numero {
            background-color: rgba(197, 168, 128, 0.15);
            color: #b0936b;
            font-weight: bold;
            font-size: 18px;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 20px;
            flex-shrink: 0;
        }

        .paso-texto h4 {
            font-size: 18px;
            color: var(--color-oscuro);
            margin-bottom: 5px;
        }

        .paso-texto p {
            color: #6b7280;
            font-size: 15px;
        }

        /* --- FOOTER --- */
        footer {
            background-color: var(--color-oscuro);
            color: #9ca3af;
            text-align: center;
            padding: 40px 0;
            font-size: 14px;
            border-top: 1px solid rgba(255,255,255,0.05);
        }

        footer p {
            margin-bottom: 10px;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 992px) {
            .hero-grid { grid-template-columns: 1fr; gap: 40px; }
            .hero-texto { text-align: center; }
            .hero-texto h1 { font-size: 38px; }
            .detalles-grid { grid-template-columns: 1fr; gap: 30px; }
            .detalles-imagen { order: 2; }
        }
        @media (max-width: 768px) {
            .nav-links li:not(.ultimo):not(.contacto-li) { display: none; }
        }
    </style>
</head>
<body>

    <!-- MENÚ DE NAVEGACIÓN -->
    <header>
        <div class="contenedor">
            <nav>
                <a href="#" class="logo">Sidrería El <span>Xuañu</span></a>
                <ul class="nav-links">
                    <li><a href="#valores">Experiencia</a></li>
                    <li><a href="#filosofia">Nuestra Casa</a></li>
                    <li class="contacto-li"><a href="tel: 684 61 95 16" class="telefono-nav">📞 684-619-516</a></li>
                    <li class="ultimo"><a href="#reserva" class="btn-nav">Reservar Mesa</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- PORTADA CON FORMULARIO DE RESERVAS -->
    <section class="hero">
        <div class="contenedor hero-grid">
            
            <div class="hero-texto">
                <h1>Una experiencia culinaria que merece <span>ser compartida</span></h1>
                <p>Cocina de la tierra con ingredientes locales, frescos y de temporada. Diseñamos platos tradicionales con un enfoque vanguardista para deleitar tu paladar.</p>
                <p style="font-size: 16px; color: var(--color-primario); font-weight: bold;">⭐ Reserva con antelación para asegurar tu velada.</p>
            </div>

            <!-- TARJETA DE RESERVA CONEXIÓN GOOGLE SHEETS -->
            <div id="reserva" class="tarjeta-registro">
                <h3>Reserva tu Mesa</h3>
                <p>Completa los datos y registraremos tu solicitud intentando confirmarte a la mayor brevedad.</p><p> No obstante hasta no enviarte una confirmación la reserva no será firme.</p><p>En caso de ser necesario un pago previo te lo avisaremos.</p>
                
                <!-- REEMPLAZA EL TEXTO DE ABAJO POR TU URL DE GOOGLE APPS SCRIPT -->
                <form id="miFormulario" action="https://script.google.com/macros/s/AKfycbxFINlestIluOSCEZY27Yck9crT7ZaUPLL_pP1XUWg8xBsSCBCTS103fxbJJP4MiYXt/exec" method="POST">
                    
                    <div class="form-group">
                        <label for="nombre">Nombre del Titular</label>
                        <input type="text" id="nombre" name="nombre" required placeholder="Ej. Michel del Toboso">
                    </div>
                    
                    <div class="form-group">
                        <label for="telefono">Teléfono de Contacto</label>
                        <input type="tel" id="telefono" name="telefono" required placeholder="Ej. +34 600 123 456">
                    </div>
                    
                    <div class="form-group">
                        <label for="fecha">Fecha de la Reserva</label>
                        <input type="date" id="fecha" name="fecha" required>
                    </div>

                    <div class="form-group">
                        <label for="personas">Número de Personas</label>
                        <input type="number" id="personas" name="personas" min="1" max="40" required placeholder="Ej. 4">
                    </div>

                    <button type="submit" class="btn-registro">Confirmar Solicitud</button>
                    
                    <!-- TEXTO DE CONSENTIMIENTO SOLICITADO -->
                    <p class="texto-consentimiento">
                        * Al cumplimentar y enviar este formulario, usted nos autoriza expresamente a almacenar los datos proporcionados, en nuestro sistema de gestión y a ponernos en contacto con usted a través de su teléfono móvil con el único fin de confirmar, coordinar o gestionar los detalles de su reserva así como informarle de futuras ofertas.
                    </p>
                </form>
            </div>

        </div>
    </section>

    <!-- VALORES / EXPERIENCIA -->
    <section id="valores" class="seccion">
        <div class="contenedor">
            <h2 class="titulo-seccion">El Placer de la Buena Mesa</h2>
            <p class="subtitulo-seccion">Cuidamos cada detalle para ofrecerte un servicio de alta cocina en un ambiente cálido e informal.</p>
            
            <div class="beneficios-grid">
                <div class="beneficio-card">
                    <div class="beneficio-icono">🥑</div>
                    <h3>Alta Calidad</h3>
                    <p>Trabajamos con productores locales y agricultura ecológica de kilómetro cero, buscando siempre la calidad de nuestros elaborados.</p>
                </div>
                <div class="beneficio-card">
                    <div class="beneficio-icono">🍷</div>
                    <h3>Bodega Selecta</h3>
                    <p>Una cuidada carta de vinos y maridajes seleccionados por nuestro sumiller para potenciar cada sabor.</p>
                </div>
                <div class="beneficio-card">
                    <div class="beneficio-icono">✨</div>
                    <h3>Ambiente Entrañable</h3>
                    <p>Espacios perfectamente ambientados, ideales para cenas románticas o reuniones familiares o de amigos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FILOSOFÍA / CÓMO FUNCIONA -->
    <section id="filosofia" class="seccion seccion-alt">
        <div class="contenedor detalles-grid">
            
            <div class="detalles-imagen">
                <img src="https://images.unsplash.com/photo-1414235077428-338989a2e8c0?auto=format&fit=crop&q=80&w=600" alt="Plato gourmet preparado">
            </div>

            <div>
                <h2 class="titulo-seccion" style="text-align: left; margin-bottom: 25px;">Política de tu Reserva</h2>
                <ul class="pasos-lista">
                    <li class="paso-item">
                        <div class="paso-numero">1</div>
                        <div class="paso-texto">
                            <h4>Registro Digital</h4>
                            <p>Al rellenar el formulario, tu mesa queda pre-asignada en nuestro sistema interno de Google Drive al instante.</p>
                        </div>
                    </li>
                    <li class="paso-item">
                        <div class="paso-numero">2</div>
                        <div class="paso-texto">
                            <h4>Llamada de Confirmación</h4>
                            <p>Nuestro equipo de sala revisará el cupo y te confirmará la reserva en firme para coordinar el horario exacto y alergias alimentarias.</p>
                        </div>
                    </li>
                    <li class="paso-item">
                        <div class="paso-numero">3</div>
                        <div class="paso-texto">
                            <h4>Margen de Cortesía</h4>
                            <p>Las mesas se guardarán por un máximo de 15 minutos respecto a la hora acordada para garantizar un servicio fluido para todos.</p>
                        </div>
                    </li>
                </ul>
            </div>

        </div>
    </section>

    <!-- PIE DE PÁGINA -->
    <footer>
        <div class="contenedor">
            <p>&copy; 2026 Sidrería El Xuañu. Ctra.Carbonera 50, Contrueces, Gijón. Todos los derechos reservados.</p>
            <p>Contacto Directo: <a href="tel:684-619-516" style="color: var(--color-primario); text-decoration: none; font-weight: bold;">684-619-516</a></p>
            <p style="font-size: 12px; color: #4b5563; margin-top: 15px;">Sistema de reservas enlazado localmente.</p>
        </div>
    </footer>

    <!-- SCRIPT DE ENVÍO ASÍNCRONO DE RESERVAS -->
    <script>
        const formulario = document.getElementById('miFormulario');
        
        formulario.addEventListener('submit', function(e) {
            e.preventDefault(); 
            
            const btn = formulario.querySelector('.btn-registro');
            btn.textContent = 'Procesando tu Mesa...';
            btn.disabled = true;

            fetch(formulario.action, {
                method: 'POST',
                body: new FormData(formulario)
            })
            .then(response => {
                alert('¡Solicitud Enviada! Los datos de tu reserva se han registrado correctamente en nuestra lista de sala. Nos pondremos en contacto contigo por teléfono móvil para confirmar.');
                formulario.reset(); 
                btn.textContent = 'Confirmar Solicitud';
                btn.disabled = false;
            })
            .catch(error => {
                alert('Hubo un error al procesar tu reserva. Por favor, verifica la conexión e inténtalo de nuevo.');
                btn.textContent = 'Confirmar Solicitud';
                btn.disabled = false;
            });
        });
    </script>

</body>
</html>
