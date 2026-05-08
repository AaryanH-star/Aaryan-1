<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Weeknd - Musician</title>

    <!-- CSS LINK -->
    <link rel="stylesheet" href="style.css">

    <!-- FONT AWESOME -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
</head>

<body>

<!-- HEADER -->
<header>
    <nav>
        <a href="#" class="logo">The Weeknd</a>

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

<!-- HERO -->
<section id="home" class="hero">

    <video autoplay muted loop playsinline class="bg-video">
        <source src="https://www.w3schools.com/howto/rain.mp4" type="video/mp4">
    </video>

    <div class="hero-content">
        <h1>The Weeknd</h1>
        <p>Indie Folk Artist | Touring Worldwide</p>

        <a href="https://open.spotify.com/" class="cta-button" target="_blank">
            Listen Now
        </a>
    </div>

</section>

<!-- ABOUT -->
<section id="about" class="about">

    <h2>About Weeknd</h2>

    <div class="about-content">

        <div class="about-text">
            <p>
                The Weeknd is a famous singer known for soulful music and amazing performances.
            </p>

            <p>
                His music is loved by millions around the world.
            </p>
        </div>

        <div class="about-image">
            <img src="https://tse3.mm.bing.net/th/id/OIP.mgyO3a0KRHS4fKvVZqJDBAHaEK?pid=Api&h=220&P=0" alt="">
        </div>

    </div>

</section>

<!-- MUSIC -->
<section id="music">

    <h2>Latest Music</h2>

    <div class="music-grid">

        <div class="music-card">
            <img src="https://i.pinimg.com/736x/3e/d0/9a/3ed09af655d811862ac3fd9eeb7dca9b.jpg">

            <h3>Sao Paulo</h3>

            <p>Latest Single</p>

            <button class="play-btn">Play</button>
        </div>

        <div class="music-card">
            <img src="https://assets.audiomack.com/Chillmusic01/f9b40c98e1dbd93eb72b85b87e2fff0d6c7b637e5419a468355cd32681efe521.jpeg?width=1000&height=1000&max=true">

            <h3>Timeless</h3>

            <p>Debut Album</p>

            <button class="play-btn">Play</button>
        </div>

    </div>

</section>

<!-- CONTACT -->
<section id="contact">

    <h2>Contact</h2>

    <div class="contact-grid">

        <div class="contact-info">

            <div class="contact-item">
                <i class="fas fa-envelope"></i>
                <p>weeknd@gmail.com</p>
            </div>

            <div class="contact-item">
                <i class="fas fa-phone"></i>
                <p>+91 9876543210</p>
            </div>

        </div>

    </div>

</section>

<!-- FOOTER -->
<footer>

    <p>© 2026 The Weeknd</p>

</footer>

<!-- JS LINK -->
<script src="script.js"></script>

</body>
</html>
