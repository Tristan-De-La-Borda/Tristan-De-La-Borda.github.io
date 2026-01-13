# Tristan-De-La-Borda.github.io
My Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | Your Name</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --gray-color: #95a5a6;
        }

        body {
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary-color);
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            text-align: center;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
            min-height: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 2px dashed #ccc;
            border-radius: 10px;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--gray-color);
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .cta-button {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: 2px solid var(--secondary-color);
        }

        .cta-button:hover {
            background-color: transparent;
            color: var(--secondary-color);
        }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2:after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background-color: var(--secondary-color);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-text {
            flex: 1;
        }

        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Portfolio Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
        }

        .portfolio-img {
            height: 200px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray-color);
        }

        .portfolio-info {
            padding: 20px;
        }

        /* Skills Section */
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .skill {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            width: 150px;
            transition: transform 0.3s;
        }

        .skill:hover {
            transform: translateY(-5px);
        }

        .skill i {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        /* Contact Section */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 50px 0 20px;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
            margin-bottom: 30px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 50px;
            height: 2px;
            background-color: var(--secondary-color);
            bottom: 0;
            left: 0;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        .social-links a:hover {
            background-color: var(--secondary-color);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                flex-direction: column;
                background-color: white;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
                padding: 20px 0;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero h1 {
                font-size: 2.2rem;
                min-height: 100px;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 576px) {
            .hero {
                padding: 120px 0 80px;
            }
            
            .hero h1 {
                font-size: 1.8rem;
                min-height: 80px;
            }
            
            section {
                padding: 60px 0;
            }
            
            .contact-form {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Port<span>folio</span></a>
                
                <div class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </div>
                
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1 id="portfolioTitle">[Your Title Here]</h1>
            <p>Welcome to my portfolio website. I'm a passionate professional dedicated to creating amazing work. Explore my projects and skills below.</p>
            <a href="#portfolio" class="cta-button">View My Work</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Hi, I'm [Your Name]</h3>
                    <p>I'm a creative professional with expertise in various fields. I have a passion for delivering high-quality work and solving complex problems through innovative solutions.</p>
                    <p>With several years of experience, I've developed a strong skill set that allows me to adapt to different challenges and deliver exceptional results for my clients and employers.</p>
                    <p>When I'm not working, I enjoy learning new technologies, exploring creative outlets, and contributing to open-source projects.</p>
                </div>
                <div class="about-image">
                    <div class="portfolio-img" style="height: 100%;">
                        <i class="fas fa-user" style="font-size: 5rem; color: #bbb;"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" style="background-color: #f5f7fa;">
        <div class="container">
            <div class="section-title">
                <h2>My Portfolio</h2>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <div class="portfolio-img">
                        <i class="fas fa-laptop-code" style="font-size: 3rem;"></i>
                    </div>
                    <div class="portfolio-info">
                        <h3>Project One</h3>
                        <p>A brief description of your project goes here. Explain what the project is about and what technologies you used.</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <div class="portfolio-img">
                        <i class="fas fa-mobile-alt" style="font-size: 3rem;"></i>
                    </div>
                    <div class="portfolio-info">
                        <h3>Project Two</h3>
                        <p>A brief description of your project goes here. Explain what the project is about and what technologies you used.</p>
                    </div>
                </div>
                
                <div class="portfolio-item">
                    <div class="portfolio-img">
                        <i class="fas fa-palette" style="font-size: 3rem;"></i>
                    </div>
                    <div class="portfolio-info">
                        <h3>Project Three</h3>
                        <p>A brief description of your project goes here. Explain what the project is about and what technologies you used.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>My Skills</h2>
            </div>
            <div class="skills-container">
                <div class="skill">
                    <i class="fab fa-html5"></i>
                    <h4>Web Design</h4>
                </div>
                <div class="skill">
                    <i class="fas fa-code"></i>
                    <h4>Development</h4>
                </div>
                <div class="skill">
                    <i class="fas fa-paint-brush"></i>
                    <h4>UI/UX Design</h4>
                </div>
                <div class="skill">
                    <i class="fas fa-chart-line"></i>
                    <h4>Strategy</h4>
                </div>
                <div class="skill">
                    <i class="fas fa-bullhorn"></i>
                    <h4>Marketing</h4>
                </div>
                <div class="skill">
                    <i class="fas fa-camera"></i>
                    <h4>Photography</h4>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" style="background-color: #f5f7fa;">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" required></textarea>
                    </div>
                    <button type="submit" class="cta-button" style="border: none; cursor: pointer;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Portfolio</h3>
                    <p>A showcase of my work, skills, and professional journey. Feel free to explore and get in touch for collaboration opportunities.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul style="list-style: none;">
                        <li style="margin-bottom: 10px;"><a href="#home" style="color: #ddd; text-decoration: none;">Home</a></li>
                        <li style="margin-bottom: 10px;"><a href="#about" style="color: #ddd; text-decoration: none;">About</a></li>
                        <li style="margin-bottom: 10px;"><a href="#portfolio" style="color: #ddd; text-decoration: none;">Portfolio</a></li>
                        <li style="margin-bottom: 10px;"><a href="#contact" style="color: #ddd; text-decoration: none;">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Info</h3>
                    <p><i class="fas fa-envelope" style="margin-right: 10px;"></i> email@example.com</p>
                    <p><i class="fas fa-phone" style="margin-right: 10px;"></i> (123) 456-7890</p>
                    <p><i class="fas fa-map-marker-alt" style="margin-right: 10px;"></i> City, Country</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; <span id="currentYear"></span> Portfolio. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Set current year in footer
        document.getElementById('currentYear').textContent = new Date().getFullYear();
        
        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            this.reset();
        });
        
        // Simple title editor (you can replace this with your own logic)
        const portfolioTitle = document.getElementById('portfolioTitle');
        
        // Double-click to edit title (for demonstration)
        portfolioTitle.addEventListener('dblclick', function() {
            const newTitle = prompt('Enter your portfolio title:', portfolioTitle.textContent);
            if (newTitle && newTitle.trim() !== '') {
                portfolioTitle.textContent = newTitle;
            }
        });
    </script>
</body>
</html>
