<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfolio of a Data Analyst and Business Enthusiast">
    <title>Portfolio - Data Analyst & Business Enthusiast</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-bg: #ecf0f1;
            --text-dark: #2c3e50;
            --text-light: #7f8c8d;
            --white: #ffffff;
            --shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--white);
        }

        /* Navigation Bar */
        nav {
            position: sticky;
            top: 0;
            background-color: var(--primary-color);
            padding: 1rem 2rem;
            box-shadow: var(--shadow);
            z-index: 1000;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        nav a:hover {
            color: var(--secondary-color);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary-color);
            transition: var(--transition);
        }

        nav a:hover::after {
            width: 100%;
        }

        /* General Section Styling */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        h1, h2, h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
            padding-bottom: 1rem;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background-color: var(--secondary-color);
            border-radius: 2px;
        }

        /* Hero Section */
        #hero {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: var(--white);
            text-align: center;
            padding: 8rem 2rem;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        #hero h1 {
            font-size: 4rem;
            color: var(--white);
            margin-bottom: 1rem;
            animation: fadeInDown 1s ease-out;
        }

        #hero .subtitle {
            font-size: 1.5rem;
            color: var(--light-bg);
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out 0.2s backwards;
        }

        .cta-button {
            display: inline-block;
            padding: 0.75rem 2rem;
            background-color: var(--accent-color);
            color: var(--white);
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: var(--transition);
            cursor: pointer;
            border: none;
            font-size: 1rem;
            animation: fadeInUp 1s ease-out 0.4s backwards;
        }

        .cta-button:hover {
            background-color: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* About Section */
        #about {
            background-color: var(--light-bg);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        .education {
            background-color: var(--white);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: var(--shadow);
        }

        .education h3 {
            margin-bottom: 1rem;
        }

        .education-item {
            margin-bottom: 1.5rem;
        }

        .education-item h4 {
            color: var(--secondary-color);
            margin-bottom: 0.3rem;
        }

        .education-item p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* Skills Section */
        #skills {
            background-color: var(--white);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background-color: var(--light-bg);
            padding: 2rem;
            border-radius: 8px;
            text-align: center;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(52, 152, 219, 0.2);
            background: linear-gradient(135deg, var(--light-bg) 0%, var(--white) 100%);
        }

        .skill-card h3 {
            color: var(--secondary-color);
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .skill-card p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* Projects Section */
        #projects {
            background-color: var(--light-bg);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }

        .project-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--secondary-color) 0%, var(--primary-color) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 3rem;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-content h3 {
            margin-bottom: 0.5rem;
        }

        .project-content p {
            color: var(--text-light);
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .tech-tag {
            display: inline-block;
            background-color: var(--secondary-color);
            color: var(--white);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .project-link {
            display: inline-block;
            color: var(--secondary-color);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border-bottom: 2px solid transparent;
        }

        .project-link:hover {
            color: var(--accent-color);
            border-bottom-color: var(--accent-color);
        }

        /* Contact Section */
        #contact {
            background-color: var(--white);
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info {
            background-color: var(--light-bg);
            padding: 3rem;
            border-radius: 8px;
            margin-bottom: 2rem;
        }

        .contact-item {
            margin-bottom: 2rem;
        }

        .contact-item h3 {
            color: var(--secondary-color);
            margin-bottom: 0.5rem;
        }

        .contact-item a {
            color: var(--text-light);
            text-decoration: none;
            transition: var(--transition);
            font-size: 1.1rem;
        }

        .contact-item a:hover {
            color: var(--secondary-color);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: var(--secondary-color);
            color: var(--white);
            border-radius: 50%;
            text-decoration: none;
            font-weight: bold;
            transition: var(--transition);
            font-size: 1.5rem;
        }

        .social-links a:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: var(--white);
            text-align: center;
            padding: 2rem;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            nav ul {
                gap: 1rem;
            }

            #hero h1 {
                font-size: 2.5rem;
            }

            #hero .subtitle {
                font-size: 1.1rem;
            }

            h2 {
                font-size: 2rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            section {
                padding: 3rem 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <ul>
            <li><a href="#hero">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="hero">
        <h1>Welcome to My Portfolio</h1>
        <p class="subtitle">Data Analyst & Business Enthusiast | Turning Data into Insights</p>
        <a href="#projects" class="cta-button">View My Work</a>
    </section>

    <!-- About Me Section -->
    <section id="about">
        <h2>About Me</h2>
        <div class="about-content">
            <article class="about-text">
                <p>
                    I'm a passionate Data Analyst and Business Enthusiast dedicated to transforming raw data into actionable insights. With a strong foundation in data analysis, business administration, and problem-solving, I help organizations make informed decisions.
                </p>
                <p>
                    My journey involves combining technical expertise with business acumen to drive meaningful results. I believe in the power of data to tell stories and inspire change.
                </p>
            </article>
            <aside class="education">
                <h3>Education & Background</h3>
                <div class="education-item">
                    <h4>Bachelor of Business Administration</h4>
                    <p>University Name | Graduation Year</p>
                </div>
                <div class="education-item">
                    <h4>Data Analysis Certification</h4>
                    <p>Certification Program | Year Completed</p>
                </div>
                <div class="education-item">
                    <h4>Additional Training</h4>
                    <p>Relevant courses and certifications</p>
                </div>
            </aside>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2>Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <h3>📊 Data Analysis</h3>
                <p>Proficient in analyzing datasets and extracting meaningful insights using statistical methods.</p>
            </div>
            <div class="skill-card">
                <h3>🐍 Python</h3>
                <p>Advanced Python programming for data analysis, automation, and application development.</p>
            </div>
            <div class="skill-card">
                <h3>🗄️ SQL</h3>
                <p>Expert in database querying, data manipulation, and optimization using SQL.</p>
            </div>
            <div class="skill-card">
                <h3>📈 Business Administration</h3>
                <p>Strong understanding of business processes, strategy, and organizational management.</p>
            </div>
            <div class="skill-card">
                <h3>📊 Tableau & Visualization</h3>
                <p>Creating compelling visual dashboards and reports for data-driven decision making.</p>
            </div>
            <div class="skill-card">
                <h3>💡 Problem Solving</h3>
                <p>Strategic thinking and analytical approach to solving complex business challenges.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>Projects</h2>
        <div class="projects-grid">
            <!-- Project Card 1 -->
            <article class="project-card">
                <div class="project-image">📊</div>
                <div class="project-content">
                    <h3>Sales Performance Analytics</h3>
                    <p>A comprehensive analysis of quarterly sales data revealing key trends and performance metrics across different regions and product categories.</p>
                    <div class="tech-tags">
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Pandas</span>
                        <span class="tech-tag">SQL</span>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener noreferrer" class="project-link">View on GitHub →</a>
                </div>
            </article>

            <!-- Project Card 2 -->
            <article class="project-card">
                <div class="project-image">💼</div>
                <div class="project-content">
                    <h3>Customer Segmentation Model</h3>
                    <p>Machine learning project to segment customers based on purchasing behavior and demographics for targeted marketing strategies.</p>
                    <div class="tech-tags">
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Scikit-learn</span>
                        <span class="tech-tag">ML</span>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener noreferrer" class="project-link">View on GitHub →</a>
                </div>
            </article>

            <!-- Project Card 3 -->
            <article class="project-card">
                <div class="project-image">📈</div>
                <div class="project-content">
                    <h3>Financial Dashboard</h3>
                    <p>Interactive dashboard displaying real-time financial metrics, budget analysis, and expense tracking with visual representations.</p>
                    <div class="tech-tags">
                        <span class="tech-tag">Tableau</span>
                        <span class="tech-tag">SQL</span>
                        <span class="tech-tag">Excel</span>
                    </div>
                    <a href="https://github.com" target="_blank" rel="noopener noreferrer" class="project-link">View on GitHub →</a>
                </div>
            </article>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get In Touch</h2>
        <div class="contact-content">
            <div class="contact-info">
                <div class="contact-item">
                    <h3>Email</h3>
                    <a href="mailto:your.email@example.com">your.email@example.com</a>
                </div>
                <div class="contact-item">
                    <h3>Location</h3>
                    <p>Your City, Your Country</p>
                </div>
                <div class="social-links">
                    <a href="https://linkedin.com/in/yourprofile" target="_blank" rel="noopener noreferrer" title="LinkedIn">in</a>
                    <a href="https://github.com/yourprofile" target="_blank" rel="noopener noreferrer" title="GitHub">⚙️</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 My Portfolio. All rights reserved.</p>
    </footer>
</body>
</html>