<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stargazers Astronomy Club</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #fff;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(0, 0, 0, 0.8);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffd700;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #ffd700;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><rect fill="%23000" width="1000" height="1000"/><g fill="%23fff"><circle cx="200" cy="200" r="1"/><circle cx="400" cy="150" r="0.5"/><circle cx="600" cy="300" r="1.5"/><circle cx="800" cy="100" r="0.8"/><circle cx="150" cy="400" r="0.6"/><circle cx="350" cy="500" r="1.2"/><circle cx="750" cy="450" r="0.9"/><circle cx="900" cy="350" r="0.7"/><circle cx="100" cy="700" r="1.1"/><circle cx="500" cy="750" r="0.8"/><circle cx="700" cy="650" r="1.3"/><circle cx="300" cy="800" r="0.5"/></g></svg>') center/cover;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            color: #000;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(255, 215, 0, 0.3);
        }

        .section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #ffd700;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .card {
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: #ffd700;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .events-list {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            margin-top: 2rem;
        }

        .event-item {
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1rem 0;
        }

        .event-item:last-child {
            border-bottom: none;
        }

        .event-date {
            color: #ffd700;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #ffd700;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.1);
            color: #fff;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        footer {
            background: rgba(0, 0, 0, 0.8);
            text-align: center;
            padding: 2rem 0;
            margin-top: 4rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .cards {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">🌟 Stargazers Club</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#events">Events</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Welcome to Stargazers</h1>
            <p>Join our community of astronomy enthusiasts and explore the wonders of the universe together. From beginner stargazing to advanced astrophotography, there's a place for everyone under our night sky.</p>
            <a href="#about" class="btn">Discover More</a>
        </div>
    </section>

    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About Our Club</h2>
            <div class="cards">
                <div class="card">
                    <h3>🔭 Stargazing Sessions</h3>
                    <p>Regular observing nights at dark-sky locations where we explore planets, galaxies, nebulae, and other celestial wonders through telescopes and binoculars.</p>
                </div>
                <div class="card">
                    <h3>📚 Educational Workshops</h3>
                    <p>Learn about astronomy basics, telescope operation, astrophotography techniques, and the latest discoveries in space science from experienced members and guest speakers.</p>
                </div>
                <div class="card">
                    <h3>👥 Community</h3>
                    <p>Connect with fellow astronomy enthusiasts of all skill levels. Share knowledge, equipment, and the excitement of astronomical discoveries in a welcoming environment.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="events" class="section">
        <div class="container">
            <h2 class="section-title">Upcoming Events</h2>
            <div class="events-list">
                <div class="event-item">
                    <div class="event-date">March 15, 2025</div>
                    <h4>New Member Welcome Night</h4>
                    <p>Introduction to the club, basic stargazing tips, and telescope demonstration. Perfect for beginners!</p>
                </div>
                <div class="event-item">
                    <div class="event-date">March 22, 2025</div>
                    <h4>Saturn Observation Session</h4>
                    <p>Special evening dedicated to observing Saturn and its magnificent rings. Weather permitting.</p>
                </div>
                <div class="event-item">
                    <div class="event-date">April 5, 2025</div>
                    <h4>Astrophotography Workshop</h4>
                    <p>Learn the basics of capturing the night sky with your camera or smartphone. Equipment provided for beginners.</p>
                </div>
                <div class="event-item">
                    <div class="event-date">April 18, 2025</div>
                    <h4>Meteor Shower Watch Party</h4>
                    <p>Join us for the Lyrid meteor shower peak. Bring blankets and enjoy the celestial fireworks!</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Join Our Club</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Name:</label>
                        <input type="text" id="name" name="name" required placeholder="Your full name">
                    </div>
                    <div class="form-group">
                        <label for="email">Email:</label>
                        <input type="email" id="email" name="email" required placeholder="your.email@example.com">
                    </div>
                    <div class="form-group">
                        <label for="experience">Experience Level:</label>
                        <select id="experience" name="experience" style="width: 100%; padding: 10px; border: 1px solid rgba(255, 255, 255, 0.3); border-radius: 5px; background: rgba(255, 255, 255, 0.1); color: #fff;">
                            <option value="beginner">Complete Beginner</option>
                            <option value="some">Some Experience</option>
                            <option value="intermediate">Intermediate</option>
                            <option value="advanced">Advanced</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Tell us about your interest in astronomy:</label>
                        <textarea id="message" name="message" rows="4" placeholder="What aspects of astronomy interest you most?"></textarea>
                    </div>
                    <button type="submit" class="btn">Join the Club</button>
                </form>
            </div>
            <div style="text-align: center; margin-top: 2rem; padding: 1rem; background: rgba(255, 255, 255, 0.05); border-radius: 10px;">
                <h3 style="color: #ffd700; margin-bottom: 1rem;">Meeting Details</h3>
                <p><strong>When:</strong> Every Friday at 7:00 PM</p>
                <p><strong>Where:</strong> Community Center, Room 201</p>
                <p><strong>Contact:</strong> stargazers@email.com | (555) 123-4567</p>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Stargazers Astronomy Club. Reach for the stars! ✨</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission handling
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(this);
            const name = formData.get('name');
            const email = formData.get('email');
            const experience = formData.get('experience');
            const message = formData.get('message');
            
            // Simple validation
            if (!name || !email) {
                alert('Please fill in all required fields.');
                return;
            }
            
            // Simulate form submission
            alert(`Thank you, ${name}! Your membership request has been received. We'll contact you at ${email} soon with more details about our next meeting.`);
            
            // Reset form
            this.reset();
        });

        // Add some interactive stars
        function createStars() {
            const starsContainer = document.createElement('div');
            starsContainer.style.position = 'fixed';
            starsContainer.style.top = '0';
            starsContainer.style.left = '0';
            starsContainer.style.width = '100%';
            starsContainer.style.height = '100%';
            starsContainer.style.pointerEvents = 'none';
            starsContainer.style.zIndex = '-1';
            
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.style.position = 'absolute';
                star.style.width = Math.random() * 3 + 'px';
                star.style.height = star.style.width;
                star.style.background = '#fff';
                star.style.borderRadius = '50%';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.opacity = Math.random();
                star.style.animation = `twinkle ${Math.random() * 3 + 2}s infinite alternate`;
                starsContainer.appendChild(star);
            }
            
            document.body.appendChild(starsContainer);
        }

        // CSS animation for twinkling stars
        const style = document.createElement('style');
        style.textContent = `
            @keyframes twinkle {
                0% { opacity: 0.3; }
                100% { opacity: 1; }
            }
        `;
        document.head.appendChild(style);

        // Initialize stars when page loads
        window.addEventListener('load', createStars);
    </script>
</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stargazers Astronomy Club</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #fff;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(0, 0, 0, 0.8);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ffd700;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #ffd700;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><rect fill="%23000" width="1000" height="1000"/><g fill="%23fff"><circle cx="200" cy="200" r="1"/><circle cx="400" cy="150" r="0.5"/><circle cx="600" cy="300" r="1.5"/><circle cx="800" cy="100" r="0.8"/><circle cx="150" cy="400" r="0.6"/><circle cx="350" cy="500" r="1.2"/><circle cx="750" cy="450" r="0.9"/><circle cx="900" cy="350" r="0.7"/><circle cx="100" cy="700" r="1.1"/><circle cx="500" cy="750" r="0.8"/><circle cx="700" cy="650" r="1.3"/><circle cx="300" cy="800" r="0.5"/></g></svg>') center/cover;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            color: #000;
            text-decoration: none;
            border-radius: 25px;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(255, 215, 0, 0.3);
        }

        .section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #ffd700;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .card {
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: #ffd700;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .events-list {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            margin-top: 2rem;
        }

        .event-item {
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1rem 0;
        }

        .event-item:last-child {
            border-bottom: none;
        }

        .event-date {
            color: #ffd700;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #ffd700;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 5px;
            background: rgba(255, 255, 255, 0.1);
            color: #fff;
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        footer {
            background: rgba(0, 0, 0, 0.8);
            text-align: center;
            padding: 2rem 0;
            margin-top: 4rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .cards {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">🌟 Stargazers Club</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#events">Events</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Welcome to Stargazers</h1>
            <p>Join our community of astronomy enthusiasts and explore the wonders of the universe together. From beginner stargazing to advanced astrophotography, there's a place for everyone under our night sky.</p>
            <a href="#about" class="btn">Discover More</a>
        </div>
    </section>

    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About Our Club</h2>
            <div class="cards">
                <div class="card">
                    <h3>🔭 Stargazing Sessions</h3>
                    <p>Regular observing nights at dark-sky locations where we explore planets, galaxies, nebulae, and other celestial wonders through telescopes and binoculars.</p>
                </div>
                <div class="card">
                    <h3>📚 Educational Workshops</h3>
                    <p>Learn about astronomy basics, telescope operation, astrophotography techniques, and the latest discoveries in space science from experienced members and guest speakers.</p>
                </div>
                <div class="card">
                    <h3>👥 Community</h3>
                    <p>Connect with fellow astronomy enthusiasts of all skill levels. Share knowledge, equipment, and the excitement of astronomical discoveries in a welcoming environment.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="events" class="section">
        <div class="container">
            <h2 class="section-title">Upcoming Events</h2>
            <div class="events-list">
                <div class="event-item">
                    <div class="event-date">March 15, 2025</div>
                    <h4>New Member Welcome Night</h4>
                    <p>Introduction to the club, basic stargazing tips, and telescope demonstration. Perfect for beginners!</p>
                </div>
                <div class="event-item">
                    <div class="event-date">March 22, 2025</div>
                    <h4>Saturn Observation Session</h4>
                    <p>Special evening dedicated to observing Saturn and its magnificent rings. Weather permitting.</p>
                </div>
                <div class="event-item">
                    <div class="event-date">April 5, 2025</div>
                    <h4>Astrophotography Workshop</h4>
                    <p>Learn the basics of capturing the night sky with your camera or smartphone. Equipment provided for beginners.</p>
                </div>
                <div class="event-item">
                    <div class="event-date">April 18, 2025</div>
                    <h4>Meteor Shower Watch Party</h4>
                    <p>Join us for the Lyrid meteor shower peak. Bring blankets and enjoy the celestial fireworks!</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Join Our Club</h2>
            <div class="contact-form">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Name:</label>
                        <input type="text" id="name" name="name" required placeholder="Your full name">
                    </div>
                    <div class="form-group">
                        <label for="email">Email:</label>
                        <input type="email" id="email" name="email" required placeholder="your.email@example.com">
                    </div>
                    <div class="form-group">
                        <label for="experience">Experience Level:</label>
                        <select id="experience" name="experience" style="width: 100%; padding: 10px; border: 1px solid rgba(255, 255, 255, 0.3); border-radius: 5px; background: rgba(255, 255, 255, 0.1); color: #fff;">
                            <option value="beginner">Complete Beginner</option>
                            <option value="some">Some Experience</option>
                            <option value="intermediate">Intermediate</option>
                            <option value="advanced">Advanced</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Tell us about your interest in astronomy:</label>
                        <textarea id="message" name="message" rows="4" placeholder="What aspects of astronomy interest you most?"></textarea>
                    </div>
                    <button type="submit" class="btn">Join the Club</button>
                </form>
            </div>
            <div style="text-align: center; margin-top: 2rem; padding: 1rem; background: rgba(255, 255, 255, 0.05); border-radius: 10px;">
                <h3 style="color: #ffd700; margin-bottom: 1rem;">Meeting Details</h3>
                <p><strong>When:</strong> Every Friday at 7:00 PM</p>
                <p><strong>Where:</strong> Community Center, Room 201</p>
                <p><strong>Contact:</strong> stargazers@email.com | (555) 123-4567</p>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Stargazers Astronomy Club. Reach for the stars! ✨</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission handling
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(this);
            const name = formData.get('name');
            const email = formData.get('email');
            const experience = formData.get('experience');
            const message = formData.get('message');
            
            // Simple validation
            if (!name || !email) {
                alert('Please fill in all required fields.');
                return;
            }
            
            // Simulate form submission
            alert(`Thank you, ${name}! Your membership request has been received. We'll contact you at ${email} soon with more details about our next meeting.`);
            
            // Reset form
            this.reset();
        });

        // Add some interactive stars
        function createStars() {
            const starsContainer = document.createElement('div');
            starsContainer.style.position = 'fixed';
            starsContainer.style.top = '0';
            starsContainer.style.left = '0';
            starsContainer.style.width = '100%';
            starsContainer.style.height = '100%';
            starsContainer.style.pointerEvents = 'none';
            starsContainer.style.zIndex = '-1';
            
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.style.position = 'absolute';
                star.style.width = Math.random() * 3 + 'px';
                star.style.height = star.style.width;
                star.style.background = '#fff';
                star.style.borderRadius = '50%';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.opacity = Math.random();
                star.style.animation = `twinkle ${Math.random() * 3 + 2}s infinite alternate`;
                starsContainer.appendChild(star);
            }
            
            document.body.appendChild(starsContainer);
        }

        // CSS animation for twinkling stars
        const style = document.createElement('style');
        style.textContent = `
            @keyframes twinkle {
                0% { opacity: 0.3; }
                100% { opacity: 1; }
            }
        `;
        document.head.appendChild(style);

        // Initialize stars when page loads
        window.addEventListener('load', createStars);
    </script>
</body>
</html>
