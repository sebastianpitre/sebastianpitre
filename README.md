<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Presentación GitHub</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Source+Code+Pro&display=swap');
        
        :root {
            --primary: #2b3137;
            --secondary: #28a745;
            --accent: #0366d6;
            --light: #f6f8fa;
            --dark: #24292e;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
            background-color: var(--primary);
            color: var(--light);
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        header {
            text-align: center;
            padding: 4rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .github-corner:hover .octo-arm {
            animation: octocat-wave 560ms ease-in-out;
        }
        
        @keyframes octocat-wave {
            0%, 100% { transform: rotate(0); }
            20%, 60% { transform: rotate(-25deg); }
            40%, 80% { transform: rotate(10deg); }
        }
        
        h1 {
            font-size: 4rem;
            margin: 0;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: fadeIn 2s;
        }
        
        h2 {
            color: var(--secondary);
            border-bottom: 2px solid var(--accent);
            padding-bottom: 0.5rem;
            margin-top: 3rem;
        }
        
        .tagline {
            font-size: 1.5rem;
            margin: 1rem 0 2rem;
            opacity: 0.9;
        }
        
        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 5px solid var(--accent);
            object-fit: cover;
            margin: 2rem auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
        }
        
        .profile-img:hover {
            transform: scale(1.05) rotate(5deg);
        }
        
        .stats {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 1.5rem;
            min-width: 150px;
            text-align: center;
            backdrop-filter: blur(5px);
            transition: transform 0.3s, box-shadow 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--secondary);
            margin: 0.5rem 0;
        }
        
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-image {
            height: 180px;
            background: var(--dark);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--light);
            font-size: 3rem;
        }
        
        .project-info {
            padding: 1.5rem;
        }
        
        .project-title {
            margin: 0;
            color: var(--secondary);
        }
        
        .project-description {
            margin: 1rem 0;
            opacity: 0.8;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }
        
        .tech-item {
            background: rgba(3, 102, 214, 0.2);
            color: var(--accent);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-family: 'Source Code Pro', monospace;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            margin: 1rem 0.5rem;
            transition: background 0.3s, transform 0.3s;
        }
        
        .btn:hover {
            background: #0356b6;
            transform: translateY(-3px);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--accent);
            color: var(--accent);
        }
        
        .btn-outline:hover {
            background: rgba(3, 102, 214, 0.1);
        }
        
        footer {
            text-align: center;
            padding: 3rem 0;
            margin-top: 3rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .social-icon {
            color: var(--light);
            font-size: 2rem;
            transition: color 0.3s, transform 0.3s;
        }
        
        .social-icon:hover {
            color: var(--secondary);
            transform: scale(1.2);
        }
        
        .typewriter {
            overflow: hidden;
            border-right: 3px solid var(--secondary);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 0.15em;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--secondary); }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        /* Efectos especiales para la sección de código */
        .code-showcase {
            background: var(--dark);
            border-radius: 10px;
            padding: 1rem;
            margin: 2rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .code-header {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .code-dots {
            display: flex;
            gap: 0.5rem;
            margin-right: 1rem;
        }
        
        .code-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .dot-red { background: #ff5f56; }
        .dot-yellow { background: #ffbd2e; }
        .dot-green { background: #27c93f; }
        
        .code-title {
            font-family: 'Source Code Pro', monospace;
            color: var(--light);
            opacity: 0.8;
        }
        
        pre {
            margin: 0;
            font-family: 'Source Code Pro', monospace;
            font-size: 0.9rem;
            line-height: 1.5;
        }
        
        .language-javascript {
            color: #f8f8f2;
        }
        
        .token.comment {
            color: #6272a4;
        }
        
        .token.keyword {
            color: #ff79c6;
        }
        
        .token.function {
            color: #50fa7b;
        }
        
        .token.string {
            color: #f1fa8c;
        }
        
        .token.number {
            color: #bd93f9;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .stat-card {
                width: 80%;
            }
        }
    </style>
</head>
<body>
    <!-- Efecto de partículas -->
    <div id="particles-js" class="particles"></div>
    
    <div class="container">
        <header>
            <h1>Hola, soy <span id="typed"></span></h1>
            <p class="tagline typewriter">Desarrollador apasionado | Especialista en GitHub | Creador de soluciones</p>
            
            <img src="https://avatars.githubusercontent.com/u/tu-id" alt="Tu foto de perfil" class="profile-img" id="profile-img">
            
            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number" id="repos">10+</div>
                    <p>Repositorios</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="stars">50+</div>
                    <p>Estrellas</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="contributions">100+</div>
                    <p>Contribuciones</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="years">3+</div>
                    <p>Años de experiencia</p>
                </div>
            </div>
            
            <div>
                <a href="https://github.com/tu-usuario" class="btn" target="_blank">Ver mi GitHub</a>
                <a href="#contact" class="btn btn-outline">Contacto</a>
            </div>
        </header>
        
        <section>
            <h2>Mis Proyectos Destacados</h2>
            <div class="projects">
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(135deg, #6e48aa 0%, #9d50bb 100%);">
                        🚀
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Proyecto Innovador</h3>
                        <p class="project-description">Un proyecto revolucionario que cambia la forma en que interactuamos con la tecnología.</p>
                        <div class="tech-stack">
                            <span class="tech-item">JavaScript</span>
                            <span class="tech-item">React</span>
                            <span class="tech-item">Node.js</span>
                        </div>
                        <a href="#" class="btn btn-outline" style="margin-top: 1rem; display: inline-block;">Ver Proyecto</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(135deg, #4776E6 0%, #8E54E9 100%);">
                        💡
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Solución Inteligente</h3>
                        <p class="project-description">Una solución elegante para un problema complejo, con un diseño limpio y eficiente.</p>
                        <div class="tech-stack">
                            <span class="tech-item">Python</span>
                            <span class="tech-item">Django</span>
                            <span class="tech-item">PostgreSQL</span>
                        </div>
                        <a href="#" class="btn btn-outline" style="margin-top: 1rem; display: inline-block;">Ver Proyecto</a>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-image" style="background: linear-gradient(135deg, #1A2980 0%, #26D0CE 100%);">
                        🔧
                    </div>
                    <div class="project-info">
                        <h3 class="project-title">Herramienta de Desarrollo</h3>
                        <p class="project-description">Una herramienta esencial para desarrolladores que mejora el flujo de trabajo diario.</p>
                        <div class="tech-stack">
                            <span class="tech-item">TypeScript</span>
                            <span class="tech-item">Vue.js</span>
                            <span class="tech-item">GraphQL</span>
                        </div>
                        <a href="#" class="btn btn-outline" style="margin-top: 1rem; display: inline-block;">Ver Proyecto</a>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
            <h2>Mi Flujo de Trabajo en GitHub</h2>
            <p>Utilizo las mejores prácticas de GitHub para mantener un flujo de trabajo limpio y colaborativo:</p>
            
            <div class="code-showcase">
                <div class="code-header">
                    <div class="code-dots">
                        <div class="code-dot dot-red"></div>
                        <div class="code-dot dot-yellow"></div>
                        <div class="code-dot dot-green"></div>
                    </div>
                    <div class="code-title">workflow.js</div>
                </div>
                <pre><code class="language-javascript">
<span class="token comment">// 1. Crear una nueva rama para cada característica</span>
<span class="token keyword">git</span> checkout -b feature/<span class="token string">nueva-funcionalidad</span>

<span class="token comment">// 2. Hacer commits atómicos con mensajes claros</span>
<span class="token keyword">git</span> commit -m <span class="token string">"Agrega autenticación de usuario"</span>
<span class="token keyword">git</span> commit -m <span class="token string">"Corrige error en validación de formulario"</span>

<span class="token comment">// 3. Sincronizar con el repositorio remoto</span>
<span class="token keyword">git</span> push origin feature/<span class="token string">nueva-funcionalidad</span>

<span class="token comment">// 4. Crear un Pull Request para revisión</span>
<span class="token comment">// 5. Revisar y resolver comentarios</span>
<span class="token comment">// 6. Hacer merge después de aprobación</span>
<span class="token keyword">git</span> checkout main
<span class="token keyword">git</span> merge feature/<span class="token string">nueva-funcionalidad</span>
<span class="token keyword">git</span> push origin main

<span class="token comment">// 7. Eliminar la rama ya fusionada</span>
<span class="token keyword">git</span> branch -d feature/<span class="token string">nueva-funcionalidad</span>
                </code></pre>
            </div>
        </section>
        
        <section id="contact">
            <h2>Contacto</h2>
            <p>¿Quieres colaborar o saber más sobre mi trabajo? ¡Contáctame!</p>
            
            <div class="social-links">
                <a href="https://github.com/tu-usuario" target="_blank" class="social-icon">👨‍💻</a>
                <a href="https://linkedin.com/in/tu-usuario" target="_blank" class="social-icon">🔗</a>
                <a href="mailto:tu@email.com" class="social-icon">✉️</a>
                <a href="https://twitter.com/tu-usuario" target="_blank" class="social-icon">🐦</a>
            </div>
        </section>
        
        <footer>
            <p>© <span id="year"></span> Tu Nombre. Todos los derechos reservados.</p>
            <p>Hecho con ❤️ y GitHub</p>
        </footer>
    </div>
    
    <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
    <script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
    <script>
        // Efecto de escritura para el título
        new Typed('#typed', {
            strings: ['Tu Nombre', 'Desarrollador', 'GitHub Expert'],
            typeSpeed: 50,
            backSpeed: 30,
            loop: true
        });
        
        // Configuración de partículas
        particlesJS("particles-js", {
            "particles": {
                "number": {
                    "value": 80,
                    "density": {
                        "enable": true,
                        "value_area": 800
                    }
                },
                "color": {
                    "value": "#28a745"
                },
                "shape": {
                    "type": "circle",
                    "stroke": {
                        "width": 0,
                        "color": "#000000"
                    },
                    "polygon": {
                        "nb_sides": 5
                    }
                },
                "opacity": {
                    "value": 0.5,
                    "random": false,
                    "anim": {
                        "enable": false,
                        "speed": 1,
                        "opacity_min": 0.1,
                        "sync": false
                    }
                },
                "size": {
                    "value": 3,
                    "random": true,
                    "anim": {
                        "enable": false,
                        "speed": 40,
                        "size_min": 0.1,
                        "sync": false
                    }
                },
                "line_linked": {
                    "enable": true,
                    "distance": 150,
                    "color": "#28a745",
                    "opacity": 0.4,
                    "width": 1
                },
                "move": {
                    "enable": true,
                    "speed": 2,
                    "direction": "none",
                    "random": false,
                    "straight": false,
                    "out_mode": "out",
                    "bounce": false,
                    "attract": {
                        "enable": false,
                        "rotateX": 600,
                        "rotateY": 1200
                    }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                    "onhover": {
                        "enable": true,
                        "mode": "grab"
                    },
                    "onclick": {
                        "enable": true,
                        "mode": "push"
                    },
                    "resize": true
                },
                "modes": {
                    "grab": {
                        "distance": 140,
                        "line_linked": {
                            "opacity": 1
                        }
                    },
                    "bubble": {
                        "distance": 400,
                        "size": 40,
                        "duration": 2,
                        "opacity": 8,
                        "speed": 3
                    },
                    "repulse": {
                        "distance": 200,
                        "duration": 0.4
                    },
                    "push": {
                        "particles_nb": 4
                    },
                    "remove": {
                        "particles_nb": 2
                    }
                }
            },
            "retina_detect": true
        });
        
        // Animación de estadísticas
        function animateValue(id, start, end, duration) {
            let obj = document.getElementById(id);
            let startTimestamp = null;
            const step = (timestamp) => {
                if (!startTimestamp) startTimestamp = timestamp;
                const progress = Math.min((timestamp - startTimestamp) / duration, 1);
                obj.innerHTML = Math.floor(progress * (end - start) + start) + "+";
                if (progress < 1) {
                    window.requestAnimationFrame(step);
                }
            };
            window.requestAnimationFrame(step);
        }
        
        // Iniciar animaciones cuando se desplaza a la sección
        window.addEventListener('scroll', function() {
            const statsSection = document.querySelector('.stats');
            const statsPosition = statsSection.getBoundingClientRect().top;
            const screenPosition = window.innerHeight / 1.3;
            
            if (statsPosition < screenPosition) {
                animateValue("repos", 0, 10, 1000);
                animateValue("stars", 0, 50, 1000);
                animateValue("contributions", 0, 100, 1000);
                animateValue("years", 0, 3, 1000);
                // Eliminar el event listener después de ejecutarlo una vez
                window.removeEventListener('scroll', this);
            }
        });
        
        // Año actual en el footer
        document.getElementById('year').textContent = new Date().getFullYear();
        
        // Efecto de hover en la imagen de perfil
        const profileImg = document.getElementById('profile-img');
        profileImg.addEventListener('mouseenter', () => {
            profileImg.style.transform = 'scale(1.05) rotate(5deg)';
        });
        profileImg.addEventListener('mouseleave', () => {
            profileImg.style.transform = 'scale(1) rotate(0deg)';
        });
    </script>
</body>
</html>
