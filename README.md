<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hardik Rathwa | Portfolio</title>
    <style>
        /* RESET & BASE STYLES */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
        }
        
        /* GERMAN-INSPIRED DESIGN - Clean, structured, professional */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* HEADER SECTION */
        header {
            background: linear-gradient(135deg, #2c3e50, #3498db);
            color: white;
            padding: 60px 0;
            text-align: center;
        }
        
        header h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }
        
        header p {
            font-size: 1.3rem;
            opacity: 0.9;
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* NAVIGATION - Clean and clear */
        nav {
            background-color: #34495e;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 30px;
            flex-wrap: wrap;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 5px 10px;
            transition: all 0.3s;
            border-bottom: 2px solid transparent;
        }
        
        nav a:hover {
            border-bottom-color: #3498db;
        }
        
        /* SECTION STYLES */
        section {
            padding: 60px 0;
            border-bottom: 1px solid #e0e0e0;
        }
        
        section:last-child {
            border-bottom: none;
        }
        
        h2 {
            font-size: 2.2rem;
            margin-bottom: 30px;
            color: #2c3e50;
            position: relative;
            padding-bottom: 10px;
        }
        
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: #3498db;
        }
        
        /* ABOUT SECTION */
        .about-content {
            display: flex;
            gap: 40px;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .about-text {
            flex: 2;
            min-width: 300px;
        }
        
        .about-text p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }
        
        .about-image {
            flex: 1;
            min-width: 200px;
            text-align: center;
        }
        
        .about-image img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #3498db;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        /* SKILLS SECTION */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
        }
        
        .skill-category h3 {
            color: #3498db;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }
        
        .skill-category ul {
            list-style: none;
        }
        
        .skill-category li {
            margin-bottom: 10px;
            padding-left: 20px;
            position: relative;
        }
        
        .skill-category li::before {
            content: '✓';
            color: #27ae60;
            position: absolute;
            left: 0;
            font-weight: bold;
        }
        
        /* PROJECTS SECTION */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-content {
            padding: 25px;
        }
        
        .project-content h3 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        .project-tags {
            margin: 15px 0;
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        .tag {
            background: #ecf0f1;
            color: #7f8c8d;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }
        
        .project-links {
            margin-top: 15px;
        }
        
        .project-links a {
            display: inline-block;
            margin-right: 15px;
            color: #3498db;
            text-decoration: none;
            font-weight: 500;
        }
        
        .project-links a:hover {
            text-decoration: underline;
        }
        
        /* EXPERIENCE & EDUCATION */
        .timeline-item {
            background: white;
            padding: 25px;
            border-radius: 8px;
            margin-bottom: 20px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            border-left: 4px solid #3498db;
        }
        
        .timeline-item h3 {
            color: #2c3e50;
            margin-bottom: 5px;
            font-size: 1.2rem;
        }
        
        .timeline-item .date {
            color: #7f8c8d;
            font-size: 0.9rem;
            margin-bottom: 10px;
        }
        
        /* CONTACT SECTION */
        .contact-info {
            background: white;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            text-align: center;
        }
        
        .contact-details {
            display: flex;
            justify-content: center;
            gap: 40px;
            flex-wrap: wrap;
            margin: 30px 0;
        }
        
        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }
        
        .contact-item .icon {
            font-size: 2rem;
        }
        
        .contact-item a {
            color: #3498db;
            text-decoration: none;
        }
        
        .contact-item a:hover {
            text-decoration: underline;
        }
        
        .cv-button {
            display: inline-block;
            background: #3498db;
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 500;
            margin-top: 20px;
            transition: background 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .cv-button:hover {
            background: #2980b9;
        }
        
        /* FOOTER */
        footer {
            background: #2c3e50;
            color: white;
            text-align: center;
            padding: 30px 0;
        }
        
        /* RESPONSIVE DESIGN */
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
            h2 { font-size: 1.8rem; }
            nav ul { gap: 15px; }
            .about-content { flex-direction: column-reverse; text-align: center; }
            h2::after { left: 50%; transform: translateX(-50%); }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Hardik Rathwa</h1>
            <p>Student | Aspiring Professional | Based in Germany</p>
        </div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <!-- ABOUT SECTION -->
        <section id="about">
            <div class="container">
                <h2>About Me</h2>
                <div class="about-content">
                    <div class="about-text">
                        <p>Welcome to my portfolio! I'm Hardik, a motivated student looking for internship and working student opportunities in Germany.</p>
                        <p>I'm passionate about technology and eager to apply my skills in a professional environment. German employers value punctuality, organization, and quality - these are exactly the values I bring to every project.</p>
                        <p>Currently seeking opportunities in [your field] where I can contribute and grow.</p>
                    </div>
                    <div class="about-image">
                        <!-- OPTIONAL: Add a professional photo here -->
                        <img src="https://via.placeholder.com/200x200/3498db/ffffff?text=Hardik" alt="Hardik Rathwa">
                    </div>
                </div>
            </div>
        </section>
        
        <!-- SKILLS SECTION -->
        <section id="skills">
            <div class="container">
                <h2>Skills</h2>
                <div class="skills-container">
                    <div class="skill-category">
                        <h3>Technical Skills</h3>
                        <ul>
                            <li>HTML5 & CSS3</li>
                            <li>JavaScript (Basic)</li>
                            <li>Python</li>
                            <li>Git & GitHub</li>
                            <li>MS Office</li>
                        </ul>
                    </div>
                    <div class="skill-category">
                        <h3>Languages</h3>
                        <ul>
                            <li>English (Fluent)</li>
                            <li>German (Learning - A2/B1)</li>
                            <li>Hindi (Native)</li>
                        </ul>
                    </div>
                    <div class="skill-category">
                        <h3>Soft Skills</h3>
                        <ul>
                            <li>Team Collaboration</li>
                            <li>Problem Solving</li>
                            <li>Time Management</li>
                            <li>Adaptability</li>
                            <li>Attention to Detail</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- PROJECTS SECTION -->
        <section id="projects">
            <div class="container">
                <h2>Projects</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-content">
                            <h3>Personal Portfolio Website</h3>
                            <p>A responsive portfolio website built with HTML and CSS to showcase my skills and projects. Hosted on GitHub Pages.</p>
                            <div class="project-tags">
                                <span class="tag">HTML</span>
                                <span class="tag">CSS</span>
                                <span class="tag">GitHub Pages</span>
                            </div>
                            <div class="project-links">
                                <a href="#" target="_blank">Live Demo</a>
                                <a href="#" target="_blank">GitHub</a>
                            </div>
                        </div>
                    </div>
                    
                    <div class="project-card">
                        <div class="project-content">
                            <h3>Sample Project 2</h3>
                            <p>Description of your next project. What did you build? What technologies did you use? What problem does it solve?</p>
                            <div class="project-tags">
                                <span class="tag">Python</span>
                                <span class="tag">API</span>
                            </div>
                            <div class="project-links">
                                <a href="#" target="_blank">GitHub</a>
                            </div>
                        </div>
                    </div>
                    
                    <div class="project-card">
                        <div class="project-content">
                            <h3>University Project</h3>
                            <p>Describe a project you worked on during your studies. Include details about your role and what you learned.</p>
                            <div class="project-tags">
                                <span class="tag">Team Work</span>
                                <span class="tag">Research</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- EXPERIENCE SECTION -->
        <section id="experience">
            <div class="container">
                <h2>Experience</h2>
                <div class="timeline-item">
                    <h3>Internship / Working Student Position</h3>
                    <div class="date">Expected 2026 | Germany</div>
                    <p>Currently seeking internship opportunities in [your field]. This section will be updated with your actual experience.</p>
                </div>
                
                <div class="timeline-item">
                    <h3>Previous Experience (if any)</h3>
                    <div class="date">Add your experience here</div>
                    <p>Describe your responsibilities and achievements. German employers appreciate detailed, honest descriptions.</p>
                </div>
            </div>
        </section>
        
        <!-- EDUCATION SECTION -->
        <section id="education">
            <div class="container">
                <h2>Education</h2>
                <div class="timeline-item">
                    <h3>Your Degree Program</h3>
                    <div class="date">202X - Present | University Name, Germany</div>
                    <p>Brief description of your studies, focus areas, and any academic achievements.</p>
                </div>
                
                <div class="timeline-item">
                    <h3>Previous Education</h3>
                    <div class="date">202X - 202X | Institution Name</div>
                    <p>Details about your background.</p>
                </div>
            </div>
        </section>
        
        <!-- CONTACT SECTION -->
        <section id="contact">
            <div class="container">
                <h2>Contact Me</h2>
                <div class="contact-info">
                    <p>I'm actively looking for internship and working student opportunities in Germany. Let's connect!</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <span class="icon">📧</span>
                            <a href="mailto:your.email@example.com">your.email@example.com</a>
                        </div>
                        <div class="contact-item">
                            <span class="icon">📱</span>
                            <span>+49 XXX XXXXXXX</span>
                        </div>
                        <div class="contact-item">
                            <span class="icon">💼</span>
                            <a href="#">LinkedIn</a>
                        </div>
                        <div class="contact-item">
                            <span class="icon">🐙</span>
                            <a href="https://github.com/Hardik-Rathwa">GitHub</a>
                        </div>
                    </div>
                    
                    <!-- IMPORTANT: CV Download Button -->
                    <a href="#" class="cv-button" download>📄 Download My CV (PDF)</a>
                    <p style="margin-top: 15px; color: #7f8c8d; font-size: 0.9rem;">*German-style CV available for download</p>
                </div>
            </div>
        </section>
    </main>
    
    <footer>
        <div class="container">
            <p>&copy; 2026 Hardik Rathwa. All rights reserved.</p>
            <p style="margin-top: 10px; opacity: 0.7;">Designed for German internship applications</p>
        </div>
    </footer>
</body>
</html>
