# BASIC-Project-task-2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rahul's Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        /* General Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f4f4f4;
        }

        /* Header Section */
        header {
            background-color: #002147;
            color: #fff;
            padding: 20px 0;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            margin: 0 auto;
        }

        nav a {
            color: #fff;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }

        nav a:hover {
            text-decoration: underline;
        }

        /* Hero Section */
        .hero {
            background-color: #005792;
            color: #fff;
            text-align: center;
            padding: 100px 20px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 10px;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        .hero a {
            background-color: #e0e1dd;
            color: #005792;
            padding: 10px 20px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
        }

        .hero a:hover {
            background-color: #fff;
            color: #002147;
        }

        /* About Section */
        .about {
            padding: 50px 20px;
            text-align: center;
            background-color: #fff;
        }

        .about h2 {
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .about p {
            max-width: 600px;
            margin: 0 auto;
            font-size: 1.1rem;
            color: #555;
        }

        /* Projects Section */
        .projects {
            background-color: #f0f0f0;
            padding: 50px 20px;
        }

        .projects h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #002147;
        }

        .project-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }

        .project-item {
            background-color: #fff;
            border: 1px solid #ddd;
            border-radius: 8px;
            margin: 15px;
            padding: 20px;
            width: calc(33.333% - 40px);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .project-item h3 {
            margin-bottom: 10px;
            color: #005792;
        }

        .project-item p {
            font-size: 0.9rem;
            color: #555;
        }

        .project-item a {
            display: inline-block;
            margin-top: 10px;
            color: #005792;
            text-decoration: none;
            font-weight: bold;
        }

        .project-item a:hover {
            text-decoration: underline;
        }

        /* Experience Section */
        .experience {
            padding: 50px 20px;
            text-align: center;
            background-color: #fff;
        }

        .experience h2 {
            margin-bottom: 20px;
            color: #002147;
        }

        .experience-item {
            background-color: #f8f8f8;
            border: 1px solid #ddd;
            border-radius: 8px;
            margin: 15px auto;
            padding: 20px;
            width: 80%;
            max-width: 500px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .experience-item h3 {
            margin-bottom: 10px;
            color: #005792;
        }

        .experience-item p {
            font-size: 0.9rem;
            color: #555;
        }

        /* Social Media Section */
        .social-media {
            padding: 20px;
            text-align: center;
            background-color: #e0e1dd;
        }

        .social-media h2 {
            margin-bottom: 20px;
            color: #002147;
        }

        .social-media a {
            margin: 0 10px;
            color: #005792;
            font-size: 24px;
            text-decoration: none;
        }

        .social-media a:hover {
            color: #002147;
        }

        /* Contact Section */
        .contact {
            padding: 50px 20px;
            text-align: center;
            background-color: #fff;
        }

        .contact h2 {
            margin-bottom: 20px;
            color: #002147;
        }

        .contact form {
            display: inline-block;
            max-width: 500px;
            width: 100%;
            text-align: left;
        }

        .contact input, .contact textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact input[type="submit"] {
            background-color: #005792;
            color: #fff;
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .contact input[type="submit"]:hover {
            background-color: #002147;
        }

        .thank-you-message {
            display: none;
            color: green;
            margin-top: 20px;
            font-weight: bold;
        }

        /* Footer */
        footer {
            background-color: #002147;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .project-item {
                width: calc(50% - 40px);
            }

            .experience-item {
                width: 100%;
            }
        }

        @media (max-width: 480px) {
            .project-item {
                width: 100%;
            }
        }
    </style>
    <script>
        // JavaScript to show thank you message on form submission
        document.addEventListener('DOMContentLoaded', function() {
            const form = document.querySelector('form');
            form.addEventListener('submit', function(event) {
                event.preventDefault(); // Prevent default form submission
                form.style.display = 'none'; // Hide the form
                document.querySelector('.thank-you-message').style.display = 'block'; // Show thank you message
            });
        });
    </script>
</head>
<body>
    <!-- Header -->
    <header>
        <h1>Rahul's Portfolio</h1>
        <nav>
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#experience">Experience</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Welcome to My Portfolio</h1>
        <p>Discover my work and experience.</p>
        <a href="#contact">Get in Touch</a>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Me</h2>
        <p>Hello! I am Rahul, a passionate web developer with experience in creating dynamic and user-friendly websites. My goal is to build responsive, accessible, and efficient applications that provide a seamless user experience.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <h2>Projects</h2>
        <div class="project-list">
            <div class="project-item">
                <h3>Project 1: Portfolio Website</h3>
                <p>A responsive personal portfolio website showcasing my skills, projects, and experience. Built with HTML, CSS, and JavaScript.</p>
                <a href="#" target="_blank">View Project</a>
            </div>
            <div class="project-item">
                <h3>Project 2: E-Commerce Store</h3>
                <p>An online store with a user-friendly interface, shopping cart, and payment integration. Built using React and Node.js.</p>
                <a href="#" target="_blank">View Project</a>
            </div>
            <div class="project-item">
                <h3>Project 3: Blog Platform</h3>
                <p>A content management system (CMS) for creating and managing blogs. Features include a rich text editor, user authentication, and comments.</p>
                <a href="#" target="_blank">View Project</a>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <h2>Experience</h2>
        <div class="experience-item">
            <h3>Front-End Developer</h3>
            <p>Tech Solutions Inc., 2021 - Present</p>
            <p>Developed and maintained the front end of multiple websites and web applications, ensuring responsiveness and accessibility.</p>
        </div>
        <div class="experience-item">
            <h3>Web Developer Intern</h3>
            <p>Web Innovations LLC, 2020 - 2021</p>
            <p>Assisted in the development of web applications, collaborated with the design team, and performed QA testing to ensure functionality.</p>
        </div>
    </section>

    <!-- Social Media Section -->
    <section class="social-media">
        <h2>Follow Me</h2>
        <a href="https://www.linkedin.com/in/your-linkedin-profile" target="_blank">🔗 LinkedIn</a>
        <a href="https://github.com/your-github-username" target="_blank">🔗 GitHub</a>
        <a href="https://twitter.com/your-twitter-handle" target="_blank">🔗 Twitter</a>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Contact Me</h2>
        <form action="https://getform.io/f/bdrylkpb" method="POST">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
            <input type="submit" value="Send">
        </form>
        <div class="thank-you-message">Thank you for reaching out! I will get back to you soon.</div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Rahul's Portfolio. All rights reserved.</p>
    </footer>
</body>
</html>
