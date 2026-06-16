# ethovore-by-lu
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ETHOVORE by Lu. | Smart Catering & Blockchain Dining</title>
    <style>
        /* Variables de Color e Identidad */
        :root {
            --verde-manzana: #70b000;
            --verde-profundo: #1b4332;
            --tierra-suave: #f4f1de;
            --crema-fondo: #faf9f6;
            --oscuro: #222222;
            --blanco: #ffffff;
        }

        /* Estilos Generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }

        body {
            background-color: var(--crema-fondo);
            color: var(--oscuro);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Navbar / Encabezado */
        header {
            background-color: var(--blanco);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            font-size: 20px;
            font-weight: bold;
            color: var(--verde-profundo);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .logo span {
            color: var(--verde-manzana);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--oscuro);
            font-weight: bold;
            font-size: 14px;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--verde-manzana);
        }

        /* Sección Hero (Principal) */
        .hero {
            background: linear-gradient(rgba(27, 67, 50, 0.85), rgba(27, 67, 50, 0.95)), 
                        url('https://images.unsplash.com/photo-1555244162-803834f70033?q=80&w=1200') no-repeat center center/cover;
            color: var(--blanco);
            padding: 120px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .hero p {
            font-size: 18px;
            max-width: 700px;
            margin: 0 auto 30px auto;
            font-weight: 300;
        }

        .btn {
            display: inline-block;
            background-color: var(--verde-manzana);
            color: var(--blanco);
            padding: 12px 30px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 4px;
            text-transform: uppercase;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: #609900;
        }

        /* Sección Sobre Nosotros */
        .about {
            padding: 80px 0;
            background-color: var(--blanco);
        }

        .grid-2 {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .section-title {
            font-size: 28px;
            color: var(--verde-profundo);
            margin-bottom: 20px;
            text-transform: uppercase;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background-color: var(--verde-manzana);
            margin-top: 8px;
        }

        .about p {
            margin-bottom: 15px;
            text-align: justify;
        }

        .about-img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        /* Sección Pilares del Modelo (Tarjetas) */
        .pilares {
            padding: 80px 0;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 40px;
        }

        .card {
            background-color: var(--blanco);
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.04);
            border-top: 4px solid var(--verde-manzana);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: var(--verde-profundo);
            margin-bottom: 15px;
            font-size: 18px;
            text-transform: uppercase;
        }

        /* Simulación Interactiva de Menú QR */
        .qr-demo {
            padding: 80px 0;
            background-color: var(--tierra-suave);
        }

        .qr-box {
            background-color: var(--blanco);
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.05);
            max-width: 650px;
            margin: 40px auto 0 auto;
            text-align: center;
        }

        .qr-placeholder {
            width: 120px;
            height: 120px;
            background-color: #eee;
            margin: 0 auto 20px auto;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed var(--verde-profundo);
            font-size: 12px;
            color: #666;
        }

        .menu-interactivo {
            background: #fdfdfd;
            border: 1px solid #e3e3e3;
            border-radius: 6px;
            padding: 20px;
            text-align: left;
            margin-top: 15px;
        }

        /* Pie de página */
        footer {
            background-color: var(--verde-profundo);
            color: var(--blanco);
            padding: 40px 0;
            text-align: center;
            font-size: 14px;
        }

        /* Responsivo */
        @media (max-width: 768px) {
            .grid-2, .grid-3 {
                grid-template-columns: 1fr;
            }
            .nav-container {
                flex-direction: column;
            }
            nav ul {
                margin-top: 15px;
            }
            .hero h1 {
                font-size: 30px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="container nav-container">
            <div class="logo">ETHOVORE <span>by Lu.</span></div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#nosotros">Nosotros</a></li>
                    <li><a href="#impacto">Impacto</a></li>
                    <li><a href="#experiencia">Experiencia QR</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="inicio" class="hero">
        <div class="container">
            <h1>Catering Responsable y Sostenible</h1>
            <p>Fusionamos alta gastronomía, tecnología y honestidad radical para transformar tus eventos corporativos masivos en motores de desarrollo social y ambiental.</p>
            <a href="#experiencia" class="btn">Prueba la Experiencia</a>
        </div>
    </section>

    <section id="nosotros" class="about">
        <div class="container grid-2">
            <div>
                <h2 class="section-title">Nuestra Esencia</h2>
                <p><strong>ETHOVORE by Lu.</strong> nace de la unión entre el griego <em>Ethos</em> (ética) y el latín <em>Vora</em> (comer). No somos una banquetera común; somos una plataforma de hospitalidad de impacto que utiliza innovación para asegurar la transparencia total en la industria del catering premium.</p>
                <p>Nuestra misión es profesionalizar el sector mediante esquemas de comercio directo, bienestar laboral y trazabilidad auditable, garantizando que cada plato servido respete activamente a las comunidades locales y los ecosistemas.</p>
            </div>
            <div>
                <img src="https://images.unsplash.com/photo-1511795409834-ef04bbd61622?q=80&w=600" alt="Banquete ETHOVORE" class="about-img">
            </div>
        </div>
    </section>

    <section id="impacto" class="pilares">
        <div class="container">
            <h2 class="section-title" style="text-align: center; margin-bottom: 10px;">Estrategia de Triple Impacto</h2>
            <p style="text-align: center; max-width: 600px; margin: 0 auto;">Diseñamos cada operación logística bajo esquemas circulares medibles.</p>
            
            <div class="grid-3">
                <div class="card">
                    <h3>Gastronomía Kilómetro Cero</h3>
                    <p>Prohibimos insumos que viajen más de 150 km. Si un ingrediente no es local, nuestro equipo creativo rediseña la receta con opciones frescas y de temporada de productores de la región.</p>
                </div>
                <div class="card">
                    <h3>Banquetes con Causa</h3>
                    <p>Cero mermas. Los excedentes limpios e inocuos que no se llegan a servir se procesan mediante estaciones móviles de envasado al vacío y se entregan a comedores comunitarios.</p>
                </div>
                <div class="card">
                    <h3>Comercio Directo y Justo</h3>
                    <p>Eliminamos intermediarios comerciales. Trabajamos de la mano con cooperativas locales y liquidamos el pago de sus insumos en un plazo máximo de 5 días hábiles.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="experiencia" class="qr-demo">
        <div class="container">
            <h2 class="section-title" style="text-align: center;">Smart Catering & Blockchain Dining</h2>
            <p style="text-align: center; max-width: 600px; margin: 10px auto 0 auto;">Imagina la experiencia de tus invitados al sentarse en la mesa de tu evento:</p>
            
            <div class="qr-box">
                <div class="qr-placeholder">
                    <svg width="60" height="60" viewBox="0 0 24 24" fill="none" stroke="#1b4332" stroke-width="2">
                        <path d="M3 3h6v6H3V3zm12 0h6v6h-6V3zM3 15h6v6H3v-6zm14 2h2v2h-2v-2z"/>
                        <path d="M14 14h2v2h-2v-2zm3 0h4v2h-4v-2zm-3 3h2v4h-2v-4zm5 2h2v2h-2v-2z"/>
                    </svg>
                </div>
                <h3>[ Menú Interactivo Auditado ]</h3>
                <p style="font-size: 14px; color: #666; margin-top: 5px;">Rastreo digital en tiempo real generado por el plato seleccionado.</p>
                
                <div class="menu-interactivo">
                    <p style="color: var(--verde-profundo); font-weight: bold; margin-bottom: 5px;">Ensalada de la Tierra Sostenible</p>
                    <p style="font-size: 13px; color: #555;"><strong>Origen:</strong> Jitomate saladette e higos cosechados hace 24 horas por la Cooperativa Agrícola Pérez en Atlixco, Puebla.</p>
                    <p style="font-size: 13px; color: #555; margin-top: 5px;"><strong>Impacto Local:</strong> Este plato inyectó $15 MXN de ganancia neta directa a la comunidad sin intermediación.</p>
                    <p style="font-size: 13px; color: #555; margin-top: 5px;"><strong>Huella Hídrica:</strong> Menú optimizado para un ahorro del 35% de agua en riego.</p>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>ETHOVORE by Lu. &copy; 2026 | Hospitalidad Consciente con Rigor Tecnológico</p>
            <p style="font-size: 11px; margin-top: 10px; color: rgba(255,255,255,0.6);">Atlixco, Puebla, México.</p>
        </div>
    </footer>

</body>
</html>
