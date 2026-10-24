HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Landing Page — Header & Hero</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- 1. Header Section -->
    <header class="navbar-container">
        <!-- Logo -->
        <div class="logo">
            <a href="#">SaaSify</a>
        </div>

        <!-- Navigation Links -->
        <nav>
            <ul class="nav-links">
                <li><a href="#">Features</a></li>
                <li><a href="#">Solutions</a></li>
                <li><a href="#">Pricing</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>

        <!-- CTA Button -->
        <div class="nav-btn">
            <a href="#" class="btn btn-secondary">Sign In</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero-section">
        <!-- 4 & 5. Flex Container for Side-by-Side Content -->
        <div class="hero-container">
            
            <!-- 2. Hero Text Content (Heading, Paragraph, Buttons) -->
            <div class="hero-text">
                <span class="badge">Version 2.0 Released</span>
                <h1>Build Better Products Faster</h1>
                <p>Empower your team with next-generation analytics and workflow automation. Scale effortlessly from startup to enterprise without missing a beat.</p>
                <div class="hero-actions">
                    <a href="#" class="btn btn-primary">Get Started Free</a>
                    <a href="#" class="btn btn-outline">Watch Demo</a>
                </div>
            </div>

            <!-- 3. Hero Illustration / Image -->
            <div class="hero-image">
                <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=800&q=80" alt="Dashboard Analytics Illustration">
            </div>

        </div>
    </section>

    <!-- 6. Footer Section -->
    <footer class="footer-section">
        <p>&copy; 2026 SaaSify Inc. All rights reserved. Built using CSS Flexbox.</p>
    </footer>

</body>
</html>

CSS
/* Universal Resets */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f8fafc;
    color: #1e293b;
    line-height: 1.6;
}

/* ==========================================================
   1. Header Styling (Sticky Navigation Bar)
   ========================================================== */
.navbar-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #ffffff;
    padding: 1.25rem 5%;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo a {
    font-size: 1.5rem;
    font-weight: 700;
    color: #0f172a;
    text-decoration: none;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-links a {
    text-decoration: none;
    color: #64748b;
    font-weight: 500;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: #2563eb;
}

/* ==========================================================
   2, 4 & 5. Hero Section & Flex Layout Alignment
   ========================================================== */
.hero-section {
    padding: 6rem 5%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero-container {
    display: flex;             /* 4. Side-by-side layout via Flexbox */
    flex-direction: row;
    align-items: center;       /* 5. Vertically center content */
    justify-content: space-between;
    gap: 4rem;
    max-width: 1200px;
    width: 100%;
}

.hero-text {
    flex: 1;                   /* Takes up equal responsive width */
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.badge {
    background-color: #dbeafe;
    color: #1d4ed8;
    font-size: 0.8rem;
    font-weight: 600;
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    margin-bottom: 1.25rem;
    text-transform: uppercase;
    letter-spacing: 0.05em;
}

.hero-text h1 {
    font-size: 3rem;
    font-weight: 800;
    color: #0f172a;
    line-height: 1.2;
    margin-bottom: 1.25rem;
}

.hero-text p {
    font-size: 1.125rem;
    color: #475569;
    margin-bottom: 2rem;
}

.hero-actions {
    display: flex;
    gap: 1rem;
}

/* 3. Hero Image Styling */
.hero-image {
    flex: 1;                   /* Takes up equal responsive width */
    display: flex;
    justify-content: center;
}

.hero-image img {
    width: 100%;
    max-width: 550px;
    border-radius: 12px;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}

/* Button Variants */
.btn {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s ease;
    text-align: center;
}

.btn-primary {
    background-color: #2563eb;
    color: #ffffff;
}

.btn-primary:hover {
    background-color: #1d4ed8;
}

.btn-secondary {
    color: #2563eb;
    background-color: transparent;
    padding: 0.5rem 1rem;
}

.btn-secondary:hover {
    background-color: #f1f5f9;
}

.btn-outline {
    background-color: transparent;
    color: #475569;
    border: 1px solid #cbd5e1;
}

.btn-outline:hover {
    background-color: #f1f5f9;
    color: #0f172a;
}

/* ==========================================================
   6. Footer Styling
   ========================================================== */
.footer-section {
    background-color: #ffffff;
    border-top: 1px solid #e2e8f0;
    padding: 2rem 5%;
    text-align: center;
    color: #64748b;
    font-size: 0.9rem;
}

/* ==========================================================
   7. Responsive Layout Check (Mobile Viewports)
   ========================================================== */
@media (max-width: 900px) {
    .navbar-container {
        flex-direction: column;
        gap: 1rem;
        padding: 1rem;
    }

    .nav-links {
        gap: 1rem;
    }

    .hero-container {
        flex-direction: column; /* Stacks text and image vertically on smaller screens */
        text-align: center;
        gap: 2.5rem;
    }

    .hero-text {
        align-items: center;    /* Centers text items on mobile */
    }

    .hero-text h1 {
        font-size: 2.25rem;
    }

    .hero-actions {
        justify-content: center;
        flex-wrap: wrap;
    }
}