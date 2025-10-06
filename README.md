# Vikram-portfolio-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vikram | Full-Stack Developer Portfolio</title>
    <meta name="description" content="Vikram - BCA student passionate about full-stack web development, cloud computing, and AI. Explore my projects and skills.">
    <meta name="keywords" content="Vikram, full-stack developer, Python, Django, SQL, web development, cloud computing, portfolio">
    <meta name="author" content="Vikram">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Vikram | Full-Stack Developer Portfolio">
    <meta property="og:description" content="BCA student passionate about full-stack web development, cloud computing, and AI.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://vikram-portfolio.com">
    <meta property="og:image" content="https://vikram-portfolio.com/images/og-image.jpg">
    
    <!-- JSON-LD Schema -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "Person",
      "name": "Vikram",
      "url": "https://vikram-portfolio.com",
      "description": "BCA student passionate about full-stack web development, cloud computing, and AI.",
      "knowsAbout": ["Python", "Django", "SQL", "Full-Stack Development", "Cloud Computing", "AI"],
      "alumniOf": {
        "@type": "EducationalOrganization",
        "name": "University Name"
      }
    }
    </script>
    
    <!-- Preload Resources -->
    <link rel="preload" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Orbitron:wght@400;500;700&display=swap" as="style">
    <link rel="preload" href="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js" as="script">
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Orbitron:wght@400;500;700&display=swap" rel="stylesheet">
    
    <!-- AOS Library -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --primary: #0a0a12;
            --secondary: #1a1a2e;
            --accent-cyan: #00f5ff;
            --accent-purple: #8a2be2;
            --accent-green: #00ff9d;
            --text-primary: #ffffff;
            --text-secondary: #b0b0b0;
            --glass-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --shadow-glow: 0 0 20px rgba(0, 245, 255, 0.3);
            --shadow-glow-purple: 0 0 20px rgba(138, 43, 226, 0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--primary);
            color: var(--text-primary);
            overflow-x: hidden;
            line-height: 1.6;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Orbitron', sans-serif;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        h1 {
            font-size: 3.5rem;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1.5rem;
        }

        h2 {
            font-size: 2.5rem;
            color: var(--accent-cyan);
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--accent-cyan);
        }

        p {
            margin-bottom: 1.5rem;
            color: var(--text-secondary);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 1.5rem 0;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            background: rgba(10, 10, 18, 0.8);
            border-bottom: 1px solid var(--glass-border);
        }

        nav.scrolled {
            padding: 1rem 0;
            background: rgba(10, 10, 18, 0.95);
            box-shadow: var(--shadow-glow);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent-cyan);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 2rem;
        }

        .nav-links a {
            color: var(--text-primary);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--accent-cyan);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-cyan);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--text-primary);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        #three-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .hero-content {
            text-align: center;
            z-index: 1;
            max-width: 800px;
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 0 0 10px rgba(0, 245, 255, 0.5);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--text-secondary);
        }

        .cta-button {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(45deg, var(--accent-cyan), var(--accent-purple));
            color: var(--text-primary);
            text-decoration: none;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: var(--shadow-glow);
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 245, 255, 0.4);
        }

        /* Sections */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text {
            padding-right: 20px;
        }

        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow-glow);
        }

        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--accent-cyan), var(--accent-purple));
            opacity: 0.3;
            z-index: 1;
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 10px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-glow);
            border-color: var(--accent-cyan);
        }

        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--accent-cyan);
        }

        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-glow);
            border-color: var(--accent-cyan);
        }

        .project-image {
            height: 200px;
            overflow: hidden;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.1);
        }

        .project-content {
            padding: 20px;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--accent-cyan);
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        .tech-tag {
            background: rgba(0, 245, 255, 0.1);
            color: var(--accent-cyan);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        /* Controls Section */
        .controls-section {
            background: var(--secondary);
            border-radius: 15px;
            padding: 40px;
            margin-top: 50px;
            box-shadow: var(--shadow-glow-purple);
        }

        .control-group {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }

        .control-item {
            flex: 1;
            min-width: 250px;
        }

        .control-label {
            display: block;
            margin-bottom: 10px;
            color: var(--accent-cyan);
            font-weight: 600;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .slider {
            flex: 1;
            -webkit-appearance: none;
            height: 8px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--accent-cyan);
            cursor: pointer;
            box-shadow: var(--shadow-glow);
        }

        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: 600;
            color: var(--accent-cyan);
        }

        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--accent-cyan);
        }

        .contact-form {
            background: var(--glass-bg);
            backdrop-filter: blur(10px);
            border: 1px solid var(--glass-border);
            border-radius: 10px;
            padding: 30px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            margin-bottom: 8px;
            color: var(--text-primary);
            font-weight: 500;
        }

        .form-input, .form-textarea {
            width: 100%;
            padding: 12px 15px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid var(--glass-border);
            border-radius: 5px;
            color: var(--text-primary);
            font-family: 'Inter', sans-serif;
            transition: all 0.3s ease;
        }

        .form-input:focus, .form-textarea:focus {
            outline: none;
            border-color: var(--accent-cyan);
            box-shadow: 0 0 0 2px rgba(0, 245, 255, 0.2);
        }

        .form-textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* Ad Placeholders */
        .ad-container {
            background: var(--glass-bg);
            border: 1px dashed var(--glass-border);
            border-radius: 5px;
            padding: 20px;
            text-align: center;
            margin: 30px 0;
            color: var(--text-secondary);
        }

        .ad-sidebar {
            position: fixed;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            width: 160px;
            background: var(--glass-bg);
            border: 1px dashed var(--glass-border);
            border-radius: 5px;
            padding: 15px;
            text-align: center;
            color: var(--text-secondary);
            z-index: 100;
        }

        /* Footer */
        footer {
            background: var(--secondary);
            padding: 60px 0 30px;
            text-align: center;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            color: var(--accent-cyan);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--accent-cyan);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: var(--glass-bg);
            border-radius: 50%;
            color: var(--text-primary);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: var(--accent-cyan);
            transform: translateY(-3px);
            box-shadow: var(--shadow-glow);
        }

        .copyright {
            padding-top: 30px;
            border-top: 1px solid var(--glass-border);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            h1 {
                font-size: 3rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .about-content, .contact-container {
                grid-template-columns: 1fr;
            }
            
            .ad-sidebar {
                display: none;
            }
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: var(--primary);
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: left 0.3s ease;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .projects-container {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            section {
                padding: 60px 0;
            }
            
            .controls-section {
                padding: 20px;
            }
            
            .control-group {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="container nav-container">
            <a href="#" class="logo">Vikram</a>
            <button class="mobile-menu-btn" id="mobileMenuBtn">☰</button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <canvas id="three-canvas"></canvas>
        <div class="hero-content">
            <h1 data-aos="fade-up">Vikram</h1>
            <p data-aos="fade-up" data-aos-delay="200">Full-Stack Developer & Cloud Enthusiast</p>
            <a href="#projects" class="cta-button" data-aos="fade-up" data-aos-delay="400">View My Work</a>
        </div>
    </section>

    <!-- Ad Placeholder - Between Sections -->
    <div class="container">
        <div class="ad-container" data-aos="fade-up">
            <!-- AdSense Ad Unit - Replace with your Ad Unit ID -->
            <!-- <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=YOUR_AD_UNIT_ID" crossorigin="anonymous"></script> -->
            <p>Advertisement Space</p>
        </div>
    </div>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title" data-aos="fade-up">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text" data-aos="fade-right">
                    <p>I'm Vikram, a second-year BCA student with a strong interest in full-stack web development and cloud computing.</p>
                    <p>I work with Python, Django, and SQL, and I enjoy building responsive web apps that solve real problems.</p>
                    <p>I'm curious about AI and love experimenting with new technologies. My goal is to join a company where I can grow as a developer and contribute to meaningful projects.</p>
                    <p>When I'm not coding, you'll find me exploring strategy games or reading about new tech trends.</p>
                    <a href="#contact" class="cta-button">Get In Touch</a>
                </div>
                <div class="about-image" data-aos="fade-left" data-aos-delay="200">
                    <img src="https://images.unsplash.com/photo-1542831371-29b0f74f9713?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Vikram - Full Stack Developer">
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title" data-aos="fade-up">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="skill-icon">💻</div>
                    <h3>Frontend Development</h3>
                    <p>HTML5, CSS3, JavaScript, React, Responsive Design</p>
                </div>
                <div class="skill-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="skill-icon">⚙️</div>
                    <h3>Backend Development</h3>
                    <p>Python, Django, SQL, REST APIs, Authentication</p>
                </div>
                <div class="skill-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="skill-icon">☁️</div>
                    <h3>Cloud Computing</h3>
                    <p>AWS, Azure, Docker, Serverless Architecture</p>
                </div>
                <div class="skill-card" data-aos="fade-up" data-aos-delay="400">
                    <div class="skill-icon">🤖</div>
                    <h3>AI & Machine Learning</h3>
                    <p>TensorFlow, Scikit-learn, Data Analysis, NLP</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Ad Placeholder - Between Sections -->
    <div class="container">
        <div class="ad-container" data-aos="fade-up">
            <!-- AdSense Ad Unit - Replace with your Ad Unit ID -->
            <!-- <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=YOUR_AD_UNIT_ID" crossorigin="anonymous"></script> -->
            <p>Advertisement Space</p>
        </div>
    </div>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-title" data-aos="fade-up">
                <h2>My Projects</h2>
            </div>
            <div class="projects-container">
                <div class="project-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="E-commerce Platform">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">E-commerce Platform</h3>
                        <div class="project-tech">
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">SQL</span>
                            <span class="tech-tag">JavaScript</span>
                        </div>
                        <p>A full-featured e-commerce platform with user authentication, product catalog, shopping cart, and payment integration.</p>
                    </div>
                </div>
                <div class="project-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Task Management App">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Task Management App</h3>
                        <div class="project-tech">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Express</span>
                        </div>
                        <p>A collaborative task management application with real-time updates, team collaboration, and progress tracking.</p>
                    </div>
                </div>
                <div class="project-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="project-image">
                        <img src="https://images.unsplash.com/photo-1555949963-aa79dcee981c?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Weather Dashboard">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Weather Dashboard</h3>
                        <div class="project-tech">
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">API Integration</span>
                            <span class="tech-tag">Chart.js</span>
                            <span class="tech-tag">CSS3</span>
                        </div>
                        <p>An interactive weather dashboard that displays current conditions, forecasts, and historical data with beautiful visualizations.</p>
                    </div>
                </div>
            </div>

            <!-- Controls Section -->
            <div class="controls-section" data-aos="fade-up">
                <h3>Interactive Controls</h3>
                <p>Adjust the settings below to see real-time changes in the 3D elements and media compression:</p>
                
                <div class="control-group">
                    <div class="control-item">
                        <label class="control-label">Image Compression Quality</label>
                        <div class="slider-container">
                            <input type="range" min="0" max="100" value="80" class="slider" id="compressionSlider">
                            <span class="slider-value" id="compressionValue">80%</span>
                        </div>
                    </div>
                    <div class="control-item">
                        <label class="control-label">Lighting Intensity</label>
                        <div class="slider-container">
                            <input type="range" min="0" max="100" value="60" class="slider" id="lightingSlider">
                            <span class="slider-value" id="lightingValue">60%</span>
                        </div>
                    </div>
                </div>
                
                <div class="control-group">
                    <div class="control-item">
                        <label class="control-label">3D Animation Speed</label>
                        <div class="slider-container">
                            <input type="range" min="0" max="100" value="50" class="slider" id="animationSlider">
                            <span class="slider-value" id="animationValue">50%</span>
                        </div>
                    </div>
                    <div class="control-item">
                        <label class="control-label">Particle Density</label>
                        <div class="slider-container">
                            <input type="range" min="0" max="100" value="75" class="slider" id="particleSlider">
                            <span class="slider-value" id="particleValue">75%</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title" data-aos="fade-up">
                <h2>Get In Touch</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info" data-aos="fade-right">
                    <h3>Let's Connect</h3>
                    <p>I'm always open to discussing new opportunities, collaborations, or just having a chat about technology.</p>
                    
                    <div class="contact-item">
                        <div class="contact-icon">📧</div>
                        <div>
                            <h4>Email</h4>
                            <p>vikram873704@gmail.com</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">📍</div>
                        <div>
                            <h4>Location</h4>
                            <p>India</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">💼</div>
                        <div>
                            <h4>LinkedIn</h4>
                            <p>https://www.linkedin.com/in/vikram-thapa-54485930a</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form" data-aos="fade-left" data-aos-delay="200">
                    <form id="contactForm">
                        <div class="form-group">
                            <label class="form-label" for="name">Your Name</label>
                            <input type="text" id="name" class="form-input" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="email">Your Email</label>
                            <input type="email" id="email" class="form-input" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="subject">Subject</label>
                            <input type="text" id="subject" class="form-input" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label" for="message">Your Message</label>
                            <textarea id="message" class="form-textarea" required></textarea>
                        </div>
                        
                        <button type="submit" class="cta-button">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Vikram</h3>
                    <p>Full-Stack Developer & Cloud Enthusiast</p>
                    <div class="social-links">
                        <a href="#" class="social-link">in</a>
                        <a href="#" class="social-link">gh</a>
                        <a href="#" class="social-link">tw</a>
                        <a href="#" class="social-link">ig</a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#skills">Skills</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Web Development</a></li>
                        <li><a href="#">Cloud Solutions</a></li>
                        <li><a href="#">API Development</a></li>
                        <li><a href="#">Consulting</a></li>
                    </ul>
                </div>
            </div>
            
            <!-- Ad Placeholder - Footer -->
            <div class="ad-container">
                <!-- AdSense Ad Unit - Replace with your Ad Unit ID -->
                <!-- <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=YOUR_AD_UNIT_ID" crossorigin="anonymous"></script> -->
                <p>Advertisement Space</p>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 Vikram. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <!-- Ad Sidebar (Desktop Only) -->
    <div class="ad-sidebar">
        <!-- AdSense Ad Unit - Replace with your Ad Unit ID -->
        <!-- <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=YOUR_AD_UNIT_ID" crossorigin="anonymous"></script> -->
        <p>Advertisement</p>
    </div>

    <!-- Scripts -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    
    <script>
        // Initialize AOS (Animate On Scroll)
        document.addEventListener('DOMContentLoaded', function() {
            AOS.init({
                duration: 1000,
                once: true,
                offset: 100
            });
            
            // Mobile menu toggle
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const navLinks = document.getElementById('navLinks');
            
            mobileMenuBtn.addEventListener('click', function() {
                navLinks.classList.toggle('active');
            });
            
            // Navbar scroll effect
            window.addEventListener('scroll', function() {
                const navbar = document.getElementById('navbar');
                if (window.scrollY > 50) {
                    navbar.classList.add('scrolled');
                } else {
                    navbar.classList.remove('scrolled');
                }
            });
            
            // Slider controls
            const compressionSlider = document.getElementById('compressionSlider');
            const compressionValue = document.getElementById('compressionValue');
            
            const lightingSlider = document.getElementById('lightingSlider');
            const lightingValue = document.getElementById('lightingValue');
            
            const animationSlider = document.getElementById('animationSlider');
            const animationValue = document.getElementById('animationValue');
            
            const particleSlider = document.getElementById('particleSlider');
            const particleValue = document.getElementById('particleValue');
            
            compressionSlider.addEventListener('input', function() {
                compressionValue.textContent = this.value + '%';
                // In a real implementation, this would adjust image compression
                updateVisuals();
            });
            
            lightingSlider.addEventListener('input', function() {
                lightingValue.textContent = this.value + '%';
                // In a real implementation, this would adjust lighting
                updateVisuals();
            });
            
            animationSlider.addEventListener('input', function() {
                animationValue.textContent = this.value + '%';
                // In a real implementation, this would adjust animation speed
                updateVisuals();
            });
            
            particleSlider.addEventListener('input', function() {
                particleValue.textContent = this.value + '%';
                // In a real implementation, this would adjust particle density
                updateVisuals();
            });
            
            function updateVisuals() {
                // This function would update the 3D scene based on slider values
                // For demonstration, we'll just log the values
                console.log('Compression:', compressionSlider.value);
                console.log('Lighting:', lightingSlider.value);
                console.log('Animation:', animationSlider.value);
                console.log('Particles:', particleSlider.value);
            }
            
            // Three.js Scene
            initThreeJS();
        });
        
        function initThreeJS() {
            const canvas = document.getElementById('three-canvas');
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer({ canvas, alpha: true });
            
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
            
            // Create particles
            const particlesGeometry = new THREE.BufferGeometry();
            const particlesCount = 1000;
            
            const posArray = new Float32Array(particlesCount * 3);
            
            for (let i = 0; i < particlesCount * 3; i++) {
                posArray[i] = (Math.random() - 0.5) * 10;
            }
            
            particlesGeometry.setAttribute('position', new THREE.BufferAttribute(posArray, 3));
            
            // Particle material
            const particlesMaterial = new THREE.PointsMaterial({
                size: 0.02,
                color: 0x00f5ff,
                transparent: true,
                opacity: 0.8
            });
            
            const particlesMesh = new THREE.Points(particlesGeometry, particlesMaterial);
            scene.add(particlesMesh);
            
            // Add some geometric shapes
            const geometry = new THREE.TorusGeometry(1, 0.4, 16, 100);
            const material = new THREE.MeshBasicMaterial({ 
                color: 0x8a2be2, 
                wireframe: true,
                transparent: true,
                opacity: 0.6
            });
            const torus = new THREE.Mesh(geometry, material);
            scene.add(torus);
            
            camera.position.z = 5;
            
            // Animation
            function animate() {
                requestAnimationFrame(animate);
                
                particlesMesh.rotation.y += 0.001;
                torus.rotation.x += 0.01;
                torus.rotation.y += 0.005;
                
                renderer.render(scene, camera);
            }
            
            animate();
            
            // Handle window resize
            window.addEventListener('resize', function() {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            });
        }
    </script>
</body>
</html>