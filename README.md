<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Portafolio | GitHub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2d2d2d;
            --secondary: #58a6ff;
            --accent: #f9826c;
            --light: #f5f5f5;
            --dark: #0d1117;
            --gray: #8b949e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--primary);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary);
        }
        
        .logo span {
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        /* Hero Section */
        .hero {
            padding: 100px 0;
            text-align: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: var(--gray);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #3d8eff;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--secondary);
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background-color: var(--secondary);
        }
        
        /* About Section */
        .section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.5rem;
            color: var(--light);
        }
        
        .section-title span {
            color: var(--secondary);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .about-text p {
            margin-bottom: 20px;
            color: var(--gray);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        .skill {
            background-color: rgba(88, 166, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(88, 166, 255, 0.3);
        }
        
        .about-image {
            flex: 1;
            text-align: center;
        }
        
        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary);
            box-shadow: 0 0 30px rgba(88, 166, 255, 0.3);
        }
        
        /* Projects Section */
        .projects {
            background-color: var(--primary);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background-color: var(--dark);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }
        
        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .project-info p {
            color: var(--gray);
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .tech {
            background-color: rgba(249, 130, 108, 0.1);
            color: var(--accent);
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
        }
        
        .project-links a {
            color: var(--light);
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s;
        }
        
        .project-links a:hover {
            color: var(--secondary);
        }
        
        /* Contact Section */
        .contact-content {
            display: flex;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: rgba(88, 166, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            color: var(--secondary);
            font-size: 1.2rem;
        }
        
        .contact-text h4 {
            margin-bottom: 5px;
            color: var(--light);
        }
        
        .contact-text p {
            color: var(--gray);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(88, 166, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--light);
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .social-link:hover {
            background-color: var(--secondary);
            transform: translateY(-5px);
        }
        
        .contact-form {
            flex: 1;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--light);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            background-color: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            color: var(--light);
            font-size: 1rem;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--secondary);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary);
            padding: 30px 0;
            text-align: center;
            color: var(--gray);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 20px 0;
        }
        
        .footer-links li {
            margin: 0 15px;
        }
        
        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
        }
        
        .copyright {
            margin-top: 20px;
            font-size: 0.9rem;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .about-content, .contact-content {
                flex-direction: column;
            }
            
            .about-image {
                order: -1;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Dev<span>Portfolio</span></div>
                <ul class="nav-links">
                    <li><a href="#home">Inicio</a></li>
                    <li><a href="#about">Sobre Mí</a></li>
                    <li><a href="#projects">Proyectos</a></li>
                    <li><a href="#contact">Contacto</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Hola, soy [Tu Nombre]</h1>
            <p>Desarrollador Full Stack apasionado por crear soluciones innovadoras y experiencias de usuario excepcionales. Bienvenido a mi portafolio de GitHub.</p>
            <a href="#projects" class="btn">Ver Proyectos</a>
            <a href="#contact" class="btn btn-outline">Contactar</a>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <h2 class="section-title">Sobre <span>Mí</span></h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Desarrollador & Diseñador</h3>
                    <p>Soy un desarrollador full stack con experiencia en la creación de aplicaciones web modernas y responsivas. Me encanta resolver problemas complejos y aprender nuevas tecnologías.</p>
                    <p>Mi enfoque se centra en escribir código limpio, eficiente y mantenible, siempre buscando las mejores prácticas y estándares de la industria.</p>
                    <div class="skills">
                        <span class="skill">JavaScript</span>
                        <span class="skill">React</span>
                        <span class="skill">Node.js</span>
                        <span class="skill">Python</span>
                        <span class="skill">HTML/CSS</span>
                        <span class="skill">Git</span>
                        <span class="skill">MongoDB</span>
                        <span class="skill">Express</span>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://via.placeholder.com/300" alt="Profile Image" class="profile-img">
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="section projects" id="projects">
        <div class="container">
            <h2 class="section-title">Mis <span>Proyectos</span></h2>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/350x200" alt="Project 1" class="project-img">
                    <div class="project-info">
                        <h3>E-commerce App</h3>
                        <p>Una aplicación de comercio electrónico completa con carrito de compras, procesamiento de pagos y panel de administración.</p>
                        <div class="project-tech">
                            <span class="tech">React</span>
                            <span class="tech">Node.js</span>
                            <span class="tech">MongoDB</span>
                            <span class="tech">Stripe</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Código</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/350x200" alt="Project 2" class="project-img">
                    <div class="project-info">
                        <h3>Task Manager</h3>
                        <p>Sistema de gestión de tareas con funciones de colaboración en tiempo real, notificaciones y análisis de productividad.</p>
                        <div class="project-tech">
                            <span class="tech">Vue.js</span>
                            <span class="tech">Firebase</span>
                            <span class="tech">CSS3</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Código</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/350x200" alt="Project 3" class="project-img">
                    <div class="project-info">
                        <h3>Weather Dashboard</h3>
                        <p>Dashboard meteorológico que muestra pronósticos en tiempo real con visualizaciones interactivas y alertas personalizadas.</p>
                        <div class="project-tech">
                            <span class="tech">JavaScript</span>
                            <span class="tech">API</span>
                            <span class="tech">Chart.js</span>
                        </div>
                        <div class="project-links">
                            <a href="#"><i class="fab fa-github"></i> Código</a>
                            <a href="#"><i class="fas fa-external-link-alt"></i> Demo</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">Contácta<span>me</span></h2>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Ubicación</h4>
                            <p>Ciudad, País</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Email</h4>
                            <p>tu.email@ejemplo.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Teléfono</h4>
                            <p>+1 234 567 890</p>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nombre</label>
                            <input type="text" id="name" class="form-control" placeholder="Tu nombre">
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" placeholder="tu.email@ejemplo.com">
                        </div>
                        <div class="form-group">
                            <label for="subject">Asunto</label>
                            <input type="text" id="subject" class="form-control" placeholder="Asunto del mensaje">
                        </div>
                        <div class="form-group">
                            <label for="message">Mensaje</label>
                            <textarea id="message" class="form-control" placeholder="Escribe tu mensaje aquí..."></textarea>
                        </div>
                        <button type="submit" class="btn">Enviar Mensaje</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="logo">Dev<span>Portfolio</span></div>
            <ul class="footer-links">
                <li><a href="#home">Inicio</a></li>
                <li><a href="#about">Sobre Mí</a></li>
                <li><a href="#projects">Proyectos</a></li>
                <li><a href="#contact">Contacto</a></li>
            </ul>
            <div class="copyright">
                &copy; 2023 [Tu Nombre]. Todos los derechos reservados.
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Form submission
        const contactForm = document.querySelector('form');
        if(contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('¡Gracias por tu mensaje! Te responderé pronto.');
                this.reset();
            });
        }
    </script>
</body>
</html>
