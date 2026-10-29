# portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arav Raju Kale | Portfolio</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-primary: #f8fafc;
            --text-secondary: #94a3b8;
            --accent: #38bdf8;
            --accent-hover: #0ea5e9;
            --border-color: #334155;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-primary);
            line-height: 1.6;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 5%;
            z-index: 1000;
        }

        .logo {
            font-weight: 700;
            font-size: 1.2rem;
            color: var(--accent);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--text-secondary);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--accent);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 2rem;
            background: radial-gradient(circle at center, #1e293b 0%, var(--bg-color) 70%);
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero p {
            font-size: clamp(1rem, 2vw, 1.25rem);
            color: var(--text-secondary);
            max-width: 600px;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: #0f172a;
            padding: 0.8rem 2rem;
            border-radius: 6px;
            font-weight: 600;
            text-decoration: none;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .btn:hover {
            background-color: var(--accent-hover);
            transform: translateY(-2px);
        }

        /* General Section Styling */
        section {
            padding: 6rem 10% 4rem;
            border-bottom: 1px solid var(--border-color);
        }

        section h2 {
            font-size: 2rem;
            margin-bottom: 2.5rem;
            text-align: center;
            position: relative;
        }

        section h2::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: var(--accent);
            margin: 0.5rem auto 0;
            border-radius: 2px;
        }

        /* About Section */
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content p {
            color: var(--text-secondary);
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
        }

        .skills-container {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .skill-badge {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 0.5rem 1.2rem;
            border-radius: 20px;
            font-weight: 500;
            color: var(--accent);
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s ease, border-color 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
        }

        .project-card h3 {
            margin-bottom: 0.8rem;
            font-size: 1.3rem;
        }

        .project-card p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
        }

        /* Blogs Section */
        .blogs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .blog-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
        }

        .blog-card span {
            font-size: 0.85rem;
            color: var(--accent);
            text-transform: uppercase;
            font-weight: 600;
        }

        .blog-card h3 {
            margin: 0.5rem 0;
            font-size: 1.2rem;
        }

        .blog-card p {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        /* Links / Accounts Section */
        .links-container {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 1rem 1.5rem;
            border-radius: 8px;
            color: var(--text-primary);
            text-decoration: none;
            font-weight: 500;
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .social-link:hover {
            background-color: var(--border-color);
            border-color: var(--accent);
        }

        .social-link i {
            font-size: 1.3rem;
            color: var(--accent);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2.5rem;
            color: var(--text-secondary);
            font-size: 0.9rem;
            border-top: 1px solid var(--border-color);
        }

        /* Responsive Navbar Toggle for Mobile */
        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--text-primary);
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--card-bg);
                border-bottom: 1px solid var(--border-color);
                padding: 1.5rem;
                text-align: center;
                gap: 1.2rem;
            }
            nav ul.active {
                display: flex;
            }
            .menu-toggle {
                display: block;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <a href="#" class="logo">Arav Raju Kale</a>
        <div class="menu-toggle" id="mobile-menu">
            <i class="fas fa-bars"></i>
        </div>
        <nav>
            <ul id="nav-list">
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#blogs">Blogs</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Hi, I'm <span>Arav Raju Kale</span></h1>
        <p>2nd Year B.Tech CSE Student at JSPM University Pune. Passionate about software development, coding, and building practical tech solutions.</p>
        <a href="#projects" class="btn">Explore My Work</a>
    </section>

    <!-- About Me Section -->
    <section id="about">
        <h2>About Me</h2>
        <div class="about-content">
            <p>I am currently pursuing my Bachelor of Technology in Computer Science and Engineering (B.Tech CSE) at JSPM University Pune (2nd Year). I enjoy sharpening my logic through coding and expanding my skill set with certifications—including my Python Programming Internship Certificate from SkillTech.</p>
            <div class="skills-container">
                <span class="skill-badge">Python</span>
                <span class="skill-badge">Java</span>
                <span class="skill-badge">C</span>
                <span class="skill-badge">Problem Solving</span>
            </div>
        </div>
    </section>

    <!-- Technical Projects Section -->
    <section id="projects">
        <h2>Technical Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Number Guessing Game</h3>
                <p>A fun interactive terminal/GUI game built in Python where users guess a randomly generated number within a specified range with score tracking.</p>
            </div>
            <div class="project-card">
                <h3>Quiz Application</h3>
                <p>An application designed to present multiple-choice questions, tally scores instantly, and provide a user-friendly quiz experience.</p>
            </div>
            <div class="project-card">
                <h3>Student Record Management System</h3>
                <p>A backend-focused system to streamline adding, viewing, updating, and deleting student details efficiently.</p>
            </div>
        </div>
    </section>

    <!-- Blogs Section -->
    <section id="blogs">
        <h2>Blogs & Insights</h2>
        <div class="blogs-grid">
            <div class="blog-card">
                <span>[Placeholder] Date • 3 min read</span>
                <h3>My Journey into 2nd Year CSE at JSPM University</h3>
                <p>Reflecting on key learnings, core programming concepts, and adjusting to advanced coursework in computer science.</p>
            </div>
            <div class="blog-card">
                <span>[Placeholder] Date • 4 min read</span>
                <h3>Key Takeaways from my Python Programming Internship</h3>
                <p>Insights on practical application building, debugging techniques, and completing the SkillTech certification program.</p>
            </div>
        </div>
    </section>

    <!-- Links / Accounts Section -->
    <section id="contact">
        <h2>Connect With Me</h2>
        <div class="links-container">
            <a href="https://github.com/aravkale4" target="_blank" class="social-link">
                <i class="fab fa-github"></i> GitHub
            </a>
            <a href="https://www.linkedin.com/in/arav-kale-63320622a?utm_source=share_via&utm_content=profile&utm_medium=member_ios" target="_blank" class="social-link">
                <i class="fab fa-linkedin"></i> LinkedIn
            </a>
            <a href="mailto:arav.kale07@gmail.com" class="social-link">
                <i class="fas fa-envelope"></i> Email Me
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Arav Raju Kale. All rights reserved.</p>
    </footer>

    <!-- JavaScript for Mobile Menu Toggle -->
    <script>
        const mobileMenu = document.getElementById('mobile-menu');
        const navList = document.getElementById('nav-list');

        mobileMenu.addEventListener('click', () => {
            navList.classList.toggle('active');
        });

        // Close menu when clicking a link on mobile
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                navList.classList.remove('active');
            });
        });
    </script>
</body>
</html>
