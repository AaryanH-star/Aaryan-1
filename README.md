<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aaryan - Musician</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            overflow-x: hidden;
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgb(121, 21, 198);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #fff;
            text-decoration: none;
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
            color: #ff6b35;
        }
        .hero{
position:relative;
height:100vh;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
color:#fff;
overflow:hidden;
}

/* VIDEO FIX */
.bg-video{
position:absolute;
top:0;
left:0;
width:100%;
height:100%;
object-fit:cover;
z-index:-1;
}
/* TEXT ABOVE VIDEO */
.hero-content{
position:relative;
z-index:1;
}

.hero-content h1{
font-size:4rem;
margin-bottom:1rem;
}

.hero-content p{
font-size:1.5rem;
margin-bottom:2rem;
}

.cta-button{
padding:15px 40px;
background:#ff6b35;
color:#fff;
text-decoration:none;
border-radius:50px;
}

.cta-button:hover{
background:#e55a2b;
}


        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: #fff;
            margin: 3px 0;
            transition: 0.3s;
        }
        /* Sections */
        section {
            padding: 100px 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        h2 {
            font-size: 3rem;
            text-align: center;
            margin-bottom: 4rem;
            color: #333;
        }

        /* About */
        .about {
            background: #ffffff;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text p {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            text-align: justify;
        }

        .about-image {
            text-align: center;
        }

        .about-image img {
            width: 100%;
            max-width: 400px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        /* Music */
        .music-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .music-card {
            background: #fff;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }

        .music-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .music-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 1rem;
        }
        .grid{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:30px;
    }
    .card{
    width:220px;
    text-align:center;
    background:#fff;
    padding:15px;
    border-radius:15px;
    box-shadow:0 10px 25px rgba(0,0,0,0.1);
    transition:0.3s;
    }
    .card:hover{
    transform:translateY(-10px);
    }
    .card img{
    width:100%;
    height:220px;
    object-fit:cover;
    border-radius:10px;
    }



        .play-btn {
            background: #ff6b35;
            color: #fff;
            border: none;
            padding: 12px 30px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
            margin-top: 1rem;
        }

        .play-btn:hover {
            background: #e55a2b;
            transform: scale(1.05);
        }

        /* Tours */
        .tour-item {
            background: #fff;
            margin-bottom: 2rem;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(197, 32, 32, 0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .tour-date {
            font-size: 1.2rem;
            font-weight: bold;
            color: #ff6b35;
        }

        .tour-soldout {
            background: #ff4757;
            color: #fff;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: bold;
        }

        /* Contact */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            color: #ff6b35;
            margin-bottom: 1rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: #ff6b35;
            margin-right: 1rem;
            width: 30px;
        }

        .contact-form {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #e9ecef;
            border-radius: 10px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ff6b35;
        }

        /* Footer */
        footer {
            background: #222;
            color: #fff;
            text-align: center;
            padding: 3rem 5%;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
        }

        .social-links a {
            color: #fff;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: #ff6b35;
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

        /* Responsive */
        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background-color: #000;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                padding: 2rem 0;
            }

            .nav-links.active {
                left: 0;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-content p {
                font-size: 1.2rem;
            }

            .about-content,
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <a href="#" class="logo"></a>The Weeknd
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#music">Music</a></li>
                <li><a href="#tour">Tour</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <video autoplay muted loop playsinline class="bg-video">
<source src="https://www.w3schools.com/howto/rain.mp4" type="video/mp4">
</video>
        <div class="hero-content">
            <h1>The Weeknd</h1>
            <p>Indie Folk Artist | Touring Worldwide</p>
            <a href="https://open.spotify.com/artist/1Xyo4u8uXC1ZmMpatF05PJ?si=266d3ac20aaf48dc" 
   class="cta-button" 
   target="_blank">
   Listen Now
</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Weeknd</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Aaryan Band is a rising indie folk artist whose soulful melodies and heartfelt lyrics have captivated audiences worldwide. With a guitar as his companion and stories as his muse, Alex crafts music that resonates with the human experience.</p>
                <p>From intimate coffeehouse performances to sold-out festival stages, Aaryan's journey has taken him across continents, sharing his music with fans who become family.</p>
            </div>
            <div class="about-image">
                <img src="https://tse3.mm.bing.net/th/id/OIP.mgyO3a0KRHS4fKvVZqJDBAHaEK?pid=Api&h=220&P=0" alt="Aaryan Band">
            </div>
        </div>
    </section>

    <!-- Music Section -->
    <section id="music">
        <h2>Latest Music</h2>
        <div class="music-grid">
            <div class="music-card">
                <img src="https://i.pinimg.com/736x/3e/d0/9a/3ed09af655d811862ac3fd9eeb7dca9b.jpg" alt="Single Cover">
                <h3>Sao Paulo</h3>
                <p>Latest Single - Out Now</p>
                <a href="https://open.spotify.com/track/7DY756WOLyOz2Xnhw4EFiC?si=585dd79c1a464df9" target="_blank">
        <button class="play-btn">Play on Spotify</button>
    </a>
            </div>
            <div class="music-card">
                <img src="https://assets.audiomack.com/Chillmusic01/f9b40c98e1dbd93eb72b85b87e2fff0d6c7b637e5419a468355cd32681efe521.jpeg?width=1000&height=1000&max=true" alt="Album Cover">
                <h3>Timeless</h3>
                <p>Debut Album</p>
                 <a href="https://open.spotify.com/track/0FIDCNYYjNvPVimz5icugS?si=3ff79aa15f1c4fa8" target="_blank">
        <button class="play-btn">Play on Spotify</button>
    </a>
            </div>
            <div class="music-card">
                <img src="https://i.pinimg.com/originals/ee/a3/25/eea325212a0fd17118d526da6b7df931.jpg" alt="EP Cover">
                <h3>Blinding lights</h3>
                <p>Acoustic EP</p>
                 <a href="https://open.spotify.com/track/0VjIjW4GlUZAMYd2vXMi3b?si=df7794352f104419" target="_blank">
        <button class="play-btn">Play on Spotify</button>
    </a>
            </div>
        </div>
    </section>
<section class="section" id="merch">
<h2>Merch Store</h2>
<div class="grid">
<div class="card">
    <img src="https://th.bing.com/th/id/OIP.uEEJrzEcF-ypT8e2V7t59QHaHa?w=208&h=208&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3">
    <h3>T-Shirt</h3>
    <p>$20</p>
</div>
<div class="card">
    <img src="https://th.bing.com/th/id/OIP.WQqr2NXCmopJNyWBI3jATwHaHa?w=166&h=180&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3">
    <h3>Cap</h3>
    <p>$10</p>
</div>
<div class="card">
    <img src="data:image/webp;base64,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">
    <h3>Poster</h3>
    <p>$5</p>
</div>
</div>
</section>
    <!-- Tour Section -->
    <section id="tour" style="background: #d49696;">
        <h2>Upcoming Tour</h2>
        <div class="tour-item">
            <div>
                <div class="tour-date">Mar 15 - New York, NY</div>
                <div>Webster Hall</div>
            </div>
            <div class="tour-soldout">Sold Out</div>
        </div>
        <div class="tour-item">
            <div>
                <div class="tour-date">Apr 2 - Los Angeles, CA</div>
                <div>The Troubadour</div>
            </div>
            <span style="color: #ff6b35; font-weight: bold;">Tickets</span>
        </div>
        <div class="tour-item">
            <div>
                <div class="tour-date">Apr 20 - London, UK</div>
                <div>Roundhouse</div>
            </div>
            <span style="color: #ff6b35; font-weight: bold;">Tickets</span>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get In Touch</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <h3>Let's Connect</h3>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <div>
                        <div>hello@theweeknd.com</div>
                    </div>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <div>9175222889</div>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <div>Los Angeles, CA</div>
                </div>
            </div>
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <input type="text" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <textarea rows="5" placeholder="Your Message" required></textarea>
                    </div>
                    <button type="submit" class="cta-button" style="width: 100%;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="social-links">
            <a href="#"><i class="fab fa-spotify"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-tiktok"></i></a>
        </div>
        <p>&copy; 2026 The . All rWeekndights reserved. | Made with ❤️ for music</p>
    </footer>

    <script>
        // Mobile menu toggle
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
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

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(0, 0, 0, 0.98)';
            } else {
                header.style.background = 'rgba(0, 0, 0, 0.95)';
            }
        });

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I\'ll get back to you soon.');
            this.reset();
        });

        // Play button functionality (demo)
        document.querySelectorAll('.play-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                alert('Opening Spotify... (Demo)');
            });
        });
    </script>
</body>
</html>
