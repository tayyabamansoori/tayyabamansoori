<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tayyaba Rehan - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Mono:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #6e44ff;
            --secondary: #ff4d7c;
            --accent: #2ec4b6;
            --dark: #1a1a2e;
            --darker: #0d0d1a;
            --light: #f8f9fa;
            --gray: #6c757d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: var(--light);
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 60px 20px;
            position: relative;
            overflow: hidden;
            margin-bottom: 40px;
        }
        
        .header-content {
            position: relative;
            z-index: 2;
        }
        
        .animated-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(110, 68, 255, 0.3) 0%, transparent 20%),
                radial-gradient(circle at 90% 70%, rgba(255, 77, 124, 0.3) 0%, transparent 20%),
                radial-gradient(circle at 50% 30%, rgba(46, 196, 182, 0.2) 0%, transparent 30%);
            z-index: 1;
            animation: pulse 15s infinite alternate;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.7; }
            100% { transform: scale(1); opacity: 0.5; }
        }
        
        h1 {
            font-size: 4rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% auto;
            animation: gradientShift 5s infinite alternate;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }
        
        .tagline {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--light);
            font-weight: 300;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: var(--gray);
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        /* Card Styles */
        .card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            overflow: hidden;
            position: relative;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }
        
        .card:hover::before {
            transform: scaleX(1);
        }
        
        .card-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--light);
            display: flex;
            align-items: center;
        }
        
        .card-title i {
            margin-right: 15px;
            color: var(--primary);
        }
        
        /* Section Styles */
        .section {
            margin-bottom: 60px;
        }
        
        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 40px;
            color: var(--light);
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 2px;
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        @media (max-width: 768px) {
            .about-content {
                grid-template-columns: 1fr;
            }
        }
        
        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .tech-category {
            margin-bottom: 30px;
        }
        
        .tech-category h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--accent);
            display: flex;
            align-items: center;
        }
        
        .tech-category h3 i {
            margin-right: 10px;
        }
        
        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            cursor: default;
            border: 1px solid transparent;
        }
        
        .tech-item:hover {
            background: rgba(255, 255, 255, 0.15);
            border-color: var(--primary);
            transform: translateY(-2px);
        }
        
        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
        }
        
        .project-header {
            padding: 20px;
            background: rgba(0, 0, 0, 0.2);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-title {
            font-size: 1.4rem;
            margin-bottom: 10px;
            color: var(--light);
        }
        
        .project-tech {
            font-size: 0.9rem;
            color: var(--gray);
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
        }
        
        .project-tech span {
            background: rgba(110, 68, 255, 0.2);
            padding: 3px 8px;
            border-radius: 10px;
        }
        
        .project-body {
            padding: 20px;
            flex-grow: 1;
        }
        
        .project-description {
            margin-bottom: 20px;
        }
        
        /* Stats */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .stat-card {
            text-align: center;
            padding: 30px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
        }
        
        .stat-value {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-label {
            font-size: 1.2rem;
            color: var(--gray);
        }
        
        /* Contact */
        .contact-methods {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .contact-btn {
            display: flex;
            align-items: center;
            padding: 15px 25px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50px;
            text-decoration: none;
            color: var(--light);
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }
        
        .contact-btn:hover {
            background: rgba(255, 255, 255, 0.15);
            border-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .contact-btn i {
            margin-right: 10px;
            font-size: 1.2rem;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 5s ease-in-out infinite;
        }
        
        /* Particle effect */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .particle {
            position: absolute;
            border-radius: 50%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            opacity: 0.3;
            animation: float 8s ease-in-out infinite;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.4rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .card-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <header>
            <div class="animated-bg"></div>
            <div class="header-content">
                <h1>Tayyaba Rehan</h1>
                <p class="tagline">Software Developer & AI Enthusiast</p>
                <p class="subtitle">Crafting innovative solutions and exploring the intersection of technology and creativity</p>
            </div>
        </header>
        
        <section class="section">
            <h2 class="section-title">About Me</h2>
            <div class="card">
                <h3 class="card-title"><i class="fas fa-user"></i> Hello World!</h3>
                <div class="about-content">
                    <div>
                        <p>I'm a passionate software developer currently pursuing dual degrees in Computer Science and Software Engineering from Aptech, set to graduate in 2025.</p>
                        <p>With a solid foundation in Java, C++, .NET MVC, SQL, PHP, MySQL, and mobile app development using Flutter and Dart, I thrive on crafting innovative software solutions.</p>
                    </div>
                    <div>
                        <p>My journey is fueled by a deep interest in AI and emerging technologies, and I aspire to create impactful projects that solve real-world problems and drive meaningful progress.</p>
                        <p>When I'm not coding, you can find me exploring new technologies, contributing to open source, or sharing knowledge with the developer community.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">Tech Stack & Tools</h2>
            <div class="card">
                <div class="tech-grid">
                    <div class="tech-category">
                        <h3><i class="fas fa-code"></i> Languages</h3>
                        <div class="tech-items">
                            <span class="tech-item">Java</span>
                            <span class="tech-item">C++</span>
                            <span class="tech-item">PHP</span>
                            <span class="tech-item">SQL</span>
                            <span class="tech-item">Dart</span>
                            <span class="tech-item">Python</span>
                            <span class="tech-item">JavaScript</span>
                            <span class="tech-item">TypeScript</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3><i class="fas fa-cubes"></i> Frameworks & Databases</h3>
                        <div class="tech-items">
                            <span class="tech-item">.NET MVC</span>
                            <span class="tech-item">Flutter</span>
                            <span class="tech-item">React</span>
                            <span class="tech-item">Node.js</span>
                            <span class="tech-item">Express.js</span>
                            <span class="tech-item">MongoDB</span>
                            <span class="tech-item">MySQL</span>
                            <span class="tech-item">Firebase</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3><i class="fas fa-brain"></i> AI/ML & Data Science</h3>
                        <div class="tech-items">
                            <span class="tech-item">TensorFlow</span>
                            <span class="tech-item">Keras</span>
                            <span class="tech-item">scikit-learn</span>
                            <span class="tech-item">pandas</span>
                            <span class="tech-item">NumPy</span>
                            <span class="tech-item">spaCy</span>
                            <span class="tech-item">Hugging Face</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3><i class="fas fa-tools"></i> Tools & Platforms</h3>
                        <div class="tech-items">
                            <span class="tech-item">Azure</span>
                            <span class="tech-item">Git</span>
                            <span class="tech-item">VS Code</span>
                            <span class="tech-item">Jupyter</span>
                            <span class="tech-item">Postman</span>
                            <span class="tech-item">Docker</span>
                            <span class="tech-item">Figma</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">💻 Laptop Harbour App</h3>
                        <div class="project-tech">
                            <span>Flutter</span>
                            <span>Firebase</span>
                            <span>Dart</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Cross-platform app for renting and selling laptops with real-time listings and chat functionality.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">🏥 NGO Donation Website</h3>
                        <div class="project-tech">
                            <span>.NET Core</span>
                            <span>MVC</span>
                            <span>SQL Server</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Donation and volunteer management portal for NGOs with full admin control and reporting.</p>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">🌍 Trip Budgeter App</h3>
                        <div class="project-tech">
                            <span>Flutter</span>
                            <span>Firebase</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Travel budget calculator with destination tracking and group trip cost sharing features.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-value">42</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">128</div>
                    <div class="stat-label">Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">16</div>
                    <div class="stat-label">Technologies</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">2025</div>
                    <div class="stat-label">Graduation Year</div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">Get In Touch</h2>
            <div class="card">
                <h3 class="card-title"><i class="fas fa-paper-plane"></i> Let's Connect</h3>
                <p>I'm always open to discussing new projects, creative ideas, or opportunities to be part of your vision.</p>
                <div class="contact-methods">
                    <a href="mailto:tayyabarehanmansoori0099@gmail.com" class="contact-btn">
                        <i class="fas fa-envelope"></i> Email
                    </a>
                    <a href="https://linkedin.com/in/tayyabarehan" class="contact-btn">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                    <a href="https://github.com/tayyabamansoori" class="contact-btn">
                        <i class="fab fa-github"></i> GitHub
                    </a>
                </div>
            </div>
        </section>
    </div>
    
    <footer>
        <p>© 2023 Tayyaba Rehan. Crafted with passion and ☕</p>
    </footer>

    <script>
        // Create particle effect
        document.addEventListener('DOMContentLoaded', function() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random properties
                const size = Math.random() * 20 + 5;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 5;
                
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${posX}%`;
                particle.style.top = `${posY}%`;
                particle.style.animationDelay = `${delay}s`;
                particle.style.opacity = Math.random() * 0.3 + 0.1;
                
                particlesContainer.appendChild(particle);
            }
            
            // Add interactive cursor effect
            document.addEventListener('mousemove', function(e) {
                const cards = document.querySelectorAll('.card, .project-card, .stat-card');
                cards.forEach(card => {
                    const rect = card.getBoundingClientRect();
                    const x = e.clientX - rect.left;
                    const y = e.clientY - rect.top;
                    
                    card.style.setProperty('--mouse-x', `${x}px`);
                    card.style.setProperty('--mouse-y', `${y}px`);
                });
            });
        });
    </script>
</body>
</html>
