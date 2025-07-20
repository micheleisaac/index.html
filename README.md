# index.html
Ufirstyoga
<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UFirst Yoga & Wellness</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    body {
        font-family: 'Arial', sans-serif;
        line-height: 1.6;
        color: #333;
        overflow-x: hidden;
    }

    /* Color Palette */
    :root {
        --primary-beige: #c4a888;
        --light-beige: #e6dccf;
        --white: #ffffff;
        --dark-gray: #2c2c2c;
        --soft-gray: #f8f6f3;
    }

    /* Navigation */
    nav {
        position: fixed;
        top: 0;
        width: 100%;
        background: rgba(196, 168, 136, 0.95);
        backdrop-filter: blur(10px);
        z-index: 1000;
        padding: 1rem 0;
        transition: all 0.3s ease;
    }

    nav.scrolled {
        background: rgba(196, 168, 136, 0.98);
        box-shadow: 0 2px 20px rgba(0,0,0,0.1);
    }

    .nav-container {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 2rem;
    }

    .logo {
        display: flex;
        align-items: center;
        gap: 15px;
        color: var(--white);
        text-decoration: none;
        font-size: 1.5rem;
        font-weight: bold;
        letter-spacing: 3px;
    }

    .lotus-icon {
        width: 40px;
        height: 40px;
        fill: var(--white);
    }

    .nav-links {
        display: flex;
        list-style: none;
        gap: 2rem;
    }

    .nav-links a {
        color: var(--white);
        text-decoration: none;
        font-weight: 500;
        transition: all 0.3s ease;
        padding: 0.5rem 1rem;
        border-radius: 25px;
    }

    .nav-links a:hover {
        background: rgba(255,255,255,0.2);
        transform: translateY(-2px);
    }

    /* Hero Section */
    .hero {
        height: 100vh;
        background: linear-gradient(135deg, var(--primary-beige) 0%, var(--light-beige) 100%);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        position: relative;
        overflow: hidden;
    }

    .hero::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="lotus" patternUnits="userSpaceOnUse" width="50" height="50"><circle cx="25" cy="25" r="1" fill="rgba(255,255,255,0.1)"/></pattern></defs><rect width="100" height="100" fill="url(%23lotus)"/></svg>');
        opacity: 0.3;
    }

    .hero-content {
        position: relative;
        z-index: 2;
        animation: fadeInUp 1s ease-out;
    }

    .hero-lotus {
        width: 120px;
        height: 120px;
        fill: var(--white);
        margin-bottom: 2rem;
        animation: float 6s ease-in-out infinite;
    }

    .hero h1 {
        font-size: 4rem;
        color: var(--white);
        margin-bottom: 1rem;
        letter-spacing: 8px;
        font-weight: 300;
    }

    .hero .tagline {
        font-size: 1.5rem;
        color: var(--white);
        margin-bottom: 3rem;
        letter-spacing: 3px;
        opacity: 0.9;
    }

    .cta-button {
        display: inline-block;
        padding: 1rem 2.5rem;
        background: var(--white);
        color: var(--primary-beige);
        text-decoration: none;
        border-radius: 50px;
        font-weight: bold;
        transition: all 0.3s ease;
        box-shadow: 0 8px 25px rgba(0,0,0,0.15);
    }

    .cta-button:hover {
        transform: translateY(-3px);
        box-shadow: 0 12px 35px rgba(0,0,0,0.2);
        background: var(--soft-gray);
    }

    /* Sections */
    .section {
        padding: 5rem 0;
        max-width: 1200px;
        margin: 0 auto;
        padding-left: 2rem;
        padding-right: 2rem;
    }

    .section h2 {
        text-align: center;
        font-size: 2.5rem;
        color: var(--primary-beige);
        margin-bottom: 3rem;
        position: relative;
    }

    .section h2::after {
        content: '';
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        width: 60px;
        height: 3px;
        background: var(--primary-beige);
        border-radius: 2px;
    }

    /* About Section */
    .about {
        background: var(--soft-gray);
    }

    .about-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .about-text {
        font-size: 1.1rem;
        line-height: 1.8;
        color: var(--dark-gray);
    }

    .about-image {
        width: 100%;
        height: 400px;
        background: var(--primary-beige);
        border-radius: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        overflow: hidden;
    }

    .about-image::before {
        content: 'Peaceful Practice Space';
        color: var(--white);
        font-size: 1.2rem;
        text-align: center;
    }

    /* Services Section */
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
    }

    .service-card {
        background: var(--white);
        padding: 2.5rem;
        border-radius: 20px;
        text-align: center;
        box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        transition: all 0.3s ease;
        border: 2px solid transparent;
    }

    .service-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        border-color: var(--primary-beige);
    }

    .service-icon {
        width: 60px;
        height: 60px;
        fill: var(--primary-beige);
        margin: 0 auto 1.5rem;
    }

    .service-card h3 {
        color: var(--dark-gray);
        margin-bottom: 1rem;
        font-size: 1.5rem;
    }

    .service-card p {
        color: #666;
        line-height: 1.6;
    }

    /* Contact Section */
    .contact {
        background: var(--primary-beige);
        color: var(--white);
        text-align: center;
    }

    .contact h2 {
        color: var(--white);
    }

    .contact-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 3rem;
        margin-top: 3rem;
    }

    .contact-item {
        padding: 2rem;
    }

    .contact-item h3 {
        margin-bottom: 1rem;
        font-size: 1.3rem;
    }

    /* Social Media */
    .social-links {
        display: flex;
        justify-content: center;
        gap: 2rem;
        margin-top: 3rem;
    }

    .social-link {
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        padding: 1rem 2rem;
        background: rgba(255, 255, 255, 0.1);
        color: var(--white);
        text-decoration: none;
        border-radius: 50px;
        border: 2px solid rgba(255, 255, 255, 0.3);
        transition: all 0.3s ease;
        font-weight: 500;
    }

    .social-link:hover {
        background: var(--white);
        color: var(--primary-beige);
        transform: translateY(-3px);
        box-shadow: 0 8px 25px rgba(0,0,0,0.2);
    }

    .social-icon {
        width: 24px;
        height: 24px;
        fill: currentColor;
    }

    /* Footer */
    .footer {
        background: var(--dark-gray);
        color: var(--white);
        text-align: center;
        padding: 2rem 0;
    }

    .footer-content {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    .footer-social {
        margin-bottom: 1.5rem;
    }

    .footer-social .social-link {
        background: transparent;
        border: 2px solid var(--primary-beige);
        color: var(--primary-beige);
        padding: 0.8rem 1.5rem;
    }

    .footer-social .social-link:hover {
        background: var(--primary-beige);
        color: var(--white);
    }

    /* Animations */
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(50px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-20px); }
    }

    /* Responsive Design */
    @media (max-width: 768px) {
        .nav-links {
            display: none;
        }

        .hero h1 {
            font-size: 2.5rem;
            letter-spacing: 4px;
        }

        .hero .tagline {
            font-size: 1.2rem;
            letter-spacing: 2px;
        }

        .about-content {
            grid-template-columns: 1fr;
            text-align: center;
        }

        .section {
            padding-left: 1rem;
            padding-right: 1rem;
        }
    }
</style>
```

</head>
<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="nav-container">
            <a href="#" class="logo">
                <svg class="lotus-icon" viewBox="0 0 100 100">
                    <!-- Outer petals -->
                    <path d="M50 20 C35 20, 20 35, 20 50 C20 35, 35 20, 50 20 C65 20, 80 35, 80 50 C80 35, 65 20, 50 20 Z" fill="white" opacity="0.9"/>
                    <!-- Middle petals -->
                    <path d="M50 25 C38 25, 28 38, 28 50 C28 38, 38 25, 50 25 C62 25, 72 38, 72 50 C72 38, 62 25, 50 25 Z" fill="white" opacity="0.95"/>
                    <!-- Inner petals -->
                    <path d="M50 30 C42 30, 35 42, 35 50 C35 42, 42 30, 50 30 C58 30, 65 42, 65 50 C65 42, 58 30, 50 30 Z" fill="white"/>
                    <!-- Side petals -->
                    <path d="M30 50 C30 35, 42 25, 50 25 C42 25, 30 35, 30 50 C30 65, 42 75, 50 75 C42 75, 30 65, 30 50 Z" fill="white" opacity="0.9"/>
                    <path d="M70 50 C70 35, 58 25, 50 25 C58 25, 70 35, 70 50 C70 65, 58 75, 50 75 C58 75, 70 65, 70 50 Z" fill="white" opacity="0.9"/>
                    <!-- Center circle -->
                    <circle cx="50" cy="50" r="8" fill="white"/>
                </svg>
                UFIRST
            </a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

```
<!-- Hero Section -->
<section id="home" class="hero">
    <div class="hero-content">
        <svg class="hero-lotus" viewBox="0 0 100 100">
            <!-- Outer petals -->
            <path d="M50 20 C35 20, 20 35, 20 50 C20 35, 35 20, 50 20 C65 20, 80 35, 80 50 C80 35, 65 20, 50 20 Z" fill="white" opacity="0.9"/>
            <!-- Middle petals -->
            <path d="M50 25 C38 25, 28 38, 28 50 C28 38, 38 25, 50 25 C62 25, 72 38, 72 50 C72 38, 62 25, 50 25 Z" fill="white" opacity="0.95"/>
            <!-- Inner petals -->
            <path d="M50 30 C42 30, 35 42, 35 50 C35 42, 42 30, 50 30 C58 30, 65 42, 65 50 C65 42, 58 30, 50 30 Z" fill="white"/>
            <!-- Side petals -->
            <path d="M30 50 C30 35, 42 25, 50 25 C42 25, 30 35, 30 50 C30 65, 42 75, 50 75 C42 75, 30 65, 30 50 Z" fill="white" opacity="0.9"/>
            <path d="M70 50 C70 35, 58 25, 50 25 C58 25, 70 35, 70 50 C70 65, 58 75, 50 75 C58 75, 70 65, 70 50 Z" fill="white" opacity="0.9"/>
            <!-- Center circle -->
            <circle cx="50" cy="50" r="8" fill="white"/>
            <!-- Additional detail petals for hero -->
            <path d="M40 40 C45 35, 55 35, 60 40 C55 35, 45 35, 40 40 Z" fill="rgba(255,255,255,0.7)"/>
            <path d="M40 60 C45 65, 55 65, 60 60 C55 65, 45 65, 40 60 Z" fill="rgba(255,255,255,0.7)"/>
        </svg>
        <h1>UFIRST</h1>
        <p class="tagline">YOGA & WELLNESS</p>
        <a href="#services" class="cta-button">Begin Your Journey</a>
    </div>
</section>

<!-- About Section -->
<section id="about" class="about">
    <div class="section">
        <h2>About UFirst</h2>
        <div class="about-content">
            <div class="about-text">
                <p>At UFirst Yoga & Wellness, we believe that wellness begins with putting yourself first. Our sanctuary offers a holistic approach to health and mindfulness, creating a space where you can reconnect with your inner peace and discover your true potential.</p>
                <br>
                <p>Founded on the principles of authentic yoga practice and mindful living, we provide a nurturing environment where beginners and experienced practitioners alike can explore the transformative power of yoga, meditation, and wellness practices.</p>
                <br>
                <p>Our mission is to guide you on a journey of self-discovery, helping you cultivate balance, strength, and serenity in every aspect of your life.</p>
            </div>
            <div class="about-image"></div>
        </div>
    </div>
</section>

<!-- Services Section -->
<section id="services" class="services">
    <div class="section">
        <h2>Our Services</h2>
        <div class="services-grid">
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <path d="M50 10 L60 30 L80 30 L66 44 L72 64 L50 52 L28 64 L34 44 L20 30 L40 30 Z"/>
                </svg>
                <h3>Hatha Yoga</h3>
                <p>Gentle, slow-paced practice focusing on basic postures and breathing techniques. Perfect for beginners and those seeking relaxation.</p>
            </div>
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <circle cx="50" cy="50" r="40" stroke-width="8" fill="none"/>
                    <circle cx="50" cy="30" r="8"/>
                    <path d="M50 40 L50 70 M40 55 L60 55"/>
                </svg>
                <h3>Vinyasa Flow</h3>
                <p>Dynamic sequences that link movement with breath, building strength, flexibility, and mindful awareness through flowing transitions.</p>
            </div>
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <circle cx="30" cy="30" r="15" fill="none" stroke-width="4"/>
                    <circle cx="70" cy="70" r="15" fill="none" stroke-width="4"/>
                    <path d="M45 30 Q50 50 55 70" stroke-width="4" fill="none"/>
                </svg>
                <h3>Meditation Classes</h3>
                <p>Guided mindfulness sessions to help you develop inner peace, reduce stress, and cultivate a deeper connection with yourself.</p>
            </div>
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <rect x="20" y="40" width="60" height="20" rx="10"/>
                    <circle cx="35" cy="50" r="8"/>
                    <circle cx="65" cy="50" r="8"/>
                </svg>
                <h3>Wellness Coaching</h3>
                <p>Personalized guidance to help you create sustainable lifestyle changes and achieve your wellness goals through holistic practices.</p>
            </div>
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <path d="M30 50 Q50 30 70 50 Q50 70 30 50"/>
                    <circle cx="50" cy="50" r="5"/>
                </svg>
                <h3>Restorative Yoga</h3>
                <p>Deeply relaxing practice using props to support the body in gentle poses, promoting healing and stress relief.</p>
            </div>
            <div class="service-card">
                <svg class="service-icon" viewBox="0 0 100 100">
                    <rect x="25" y="45" width="50" height="10" rx="5"/>
                    <circle cx="35" cy="35" r="6"/>
                    <circle cx="65" cy="35" r="6"/>
                    <circle cx="50" cy="25" r="6"/>
                </svg>
                <h3>Private Sessions</h3>
                <p>One-on-one instruction tailored to your specific needs, goals, and experience level for accelerated growth and healing.</p>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section id="contact" class="contact">
    <div class="section">
        <h2>Connect With Us</h2>
        <div class="contact-content">
            <div class="contact-item">
                <h3>Visit Our Studio</h3>
                <p>St. Albert, Alberta</p>
            </div>
            <div class="contact-item">
                <h3>Get In Touch</h3>
                <p>Email: ufirstyoga@gmail.com</p>
            </div>
            <div class="contact-item">
                <h3>Studio Hours</h3>
                <p>Monday - Friday: 6am - 9pm<br>Weekend: 7am - 7pm</p>
            </div>
        </div>
        
        <div class="social-links">
            <a href="https://www.instagram.com/ufirst_yoga?igsh=MXcyaTVzdmFremJtdQ==" target="_blank" rel="noopener noreferrer" class="social-link">
                <svg class="social-icon" viewBox="0 0 24 24">
                    <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
                Follow @ufirst_yoga
            </a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="footer">
    <div class="footer-content">
        <div class="footer-social">
            <a href="https://www.instagram.com/ufirst_yoga?igsh=MXcyaTVzdmFremJtdQ==" target="_blank" rel="noopener noreferrer" class="social-link">
                <svg class="social-icon" viewBox="0 0 24 24">
                    <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
                Instagram
            </a>
        </div>
        <p>&copy; 2025 UFirst Yoga & Wellness. All rights reserved.</p>
        <p>Nurturing your journey to wellness and inner peace.</p>
    </div>
</footer>

<script>
    // Navbar scroll effect
    window.addEventListener('scroll', function() {
        const navbar = document.getElementById('navbar');
        if (window.scrollY > 50) {
            navbar.classList.add('scrolled');
        } else {
            navbar.classList.remove('scrolled');
        }
    });

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

    // Service cards hover effect
    const serviceCards = document.querySelectorAll('.service-card');
    serviceCards.forEach(card => {
        card.addEventListener('mouseenter', function() {
            this.style.transform = 'translateY(-10px) scale(1.02)';
        });
        
        card.addEventListener('mouseleave', function() {
            this.style.transform = 'translateY(0) scale(1)';
        });
    });
</script>
```

</body>
</html>
