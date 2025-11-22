:root {
    --primary-color: #FF6565;
    --dark-color: #071629;
    --light-color: #ffffff;
    --text-color: #333333;

    --font-main: "Source Sans Pro", sans-serif;
    --font-secondary: "Spin Cycle OT", sans-serif;

    --max-width: 1100px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: var(--font-main);
    color: var(--text-color);
    background: #fff;
    line-height: 1.6;
}

/* Utility classes */
.container {
    width: 100%;
    max-width: var(--max-width);
    margin: 0 auto;
    padding: 0 20px;
}

/* Buttons */
.btn-primary {
    background: var(--primary-color);
    color: var(--light-color);
    border: none;
    padding: 15px 30px;
    font-size: 1.1rem;
    border-radius: 25px;
    cursor: pointer;
    transition: opacity 0.3s ease;
}

.btn-primary:hover {
    opacity: 0.9;
}


.header {
    padding: 20px 0;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav ul {
    display: flex;
    gap: 30px;
    list-style: none;
}

.nav a {
    text-decoration: none;
    color: var(--light-color);
    font-weight: 600;
    transition: color 0.3s ease;
}

.nav a:hover {
    color: var(--primary-color);
}


.hero {
    height: 90vh;
    background: url("../images/hero.jpg") no-repeat center center/cover;
    position: relative;
    color: var(--light-color);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.hero .overlay {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.5);
}

.hero-content {
    position: relative;
    max-width: 700px;
}

.hero h1 {
    font-size: 4rem;
    margin-bottom: 10px;
}

.hero p {
    font-size: 1.4rem;
    margin-bottom: 30px;
}


.testimonials {
    padding: 80px 0;
}

.testimonials h2 {
    text-align: center;
    font-size: 2.4rem;
    margin-bottom: 40px;
}

.testimonial-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 25px;
}

.testimonial-card {
    text-align: center;
    padding: 20px;
}

.testimonial-card img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 15px;
}

.testimonial-card blockquote {
    font-style: italic;
    font-size: 0.95rem;
}

.testimonial-card footer {
    margin-top: 10px;
    font-weight: bold;
}


.services {
    padding: 80px 0;
    background: #f8f8f8;
}

.services h2 {
    text-align: center;
    margin-bottom: 50px;
    font-size: 2.4rem;
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
    text-align: center;
}

.services-grid img {
    width: 80px;
    height: 80px;
    margin-bottom: 20px;
}

.services-grid h3 {
    margin-bottom: 10px;
    font-size: 1.3rem;
}


.footer {
    background: var(--dark-color);
    color: var(--light-color);
    padding: 40px 0;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.footer-logo {
    width: 150px;
}



@media (max-width: 900px) {
    .testimonial-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .services-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile */
@media (max-width: 600px) {
    .hero h1 {
        font-size: 2.8rem;
    }

    .hero p {
        font-size: 1rem;
    }

    .testimonial-grid {
        grid-template-columns: 1fr;
    }

    .services-grid {
        grid-template-columns: 1fr;
    }

    .footer-content {
        flex-direction: column;
        text-align: center;
        gap: 20px;
    }
}