<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Responsive Page</title>

    <style>
        /* General Styles */
        body.single #footer { text-align: center; }
        #intro header p { font-size: 0.8em; }
        #footer .icons, #footer .copyright { color: #aaaaaa; }
        #footer .copyright { font-family: "Raleway", Helvetica, sans-serif; font-size: 0.5em; font-weight: 400; letter-spacing: 0.25em; text-transform: uppercase; }

        /* Menu */
        #menu {
            transform: translateX(25em);
            transition: transform 0.5s ease, visibility 0.5s;
            -webkit-overflow-scrolling: touch;
            background: #fff;
            border-left: 1px solid rgba(160,160,160,0.3);
            box-shadow: none;
            height: 100%;
            width: 25em;
            position: fixed;
            top: 0;
            right: 0;
            visibility: hidden;
            z-index: 10002;
        }

        #menu > * { padding: 3em; border-top: 1px solid rgba(160,160,160,0.3); }
        #menu > * > :last-child { margin-bottom: 0; }
        #menu > :first-child { border-top: 0; }
        #menu .links { list-style: none; padding: 0; }
        #menu .links > li {
            margin-top: 1.5em;
            padding-top: 1.5em;
            border-top: 1px dotted rgba(160,160,160,0.3);
        }
        #menu .links > li a { display: block; }
        #menu .links > li a h3 { font-size: 0.7em; transition: color 0.2s ease; }
        #menu .links > li a p { font-family: "Raleway", Helvetica, sans-serif; font-size: 0.6em; letter-spacing: 0.25em; text-transform: uppercase; margin-bottom: 0; }
        #menu .links > li a:hover h3 { color: #2ebaae; }
        body.is-menu-visible #menu { transform: translateX(0); visibility: visible; }

        /* Responsive Design */
        @media (max-width: 1280px) {
            #intro { margin-bottom: 3em; text-align: center; }
            #intro header h2 { font-size: 2em; }
            #intro header p { font-size: 0.7em; }
        }
        
        @media (max-width: 736px) {
            #intro { margin-bottom: 1.5em; padding: 1.25em 0; }
            #intro > :last-child { margin-bottom: 0; }
            #intro .logo { margin-bottom: 0.5em; }
            #intro header h2 { font-size: 1.25em; }

            #menu > * { padding: 1.5em; }
        }
    </style>
</head>

<body>

    <!-- Intro Section -->
    <div id="intro">
        <header>
            <h2>Welcome to My Website</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </header>
        <div class="logo">
            <img src="logo.png" alt="Website Logo" />
        </div>
        <div class="content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur auctor dui sed libero vulputate, ac lacinia enim ullamcorper. Phasellus in nulla nec felis mollis consequat. Sed hendrerit, magna eu cursus auctor, enim ante varius sapien, et tristique ligula orci vel nunc.</p>
            <p>Donec fringilla est eu ligula malesuada, ac vulputate libero tincidunt. Suspendisse potenti. Mauris id sapien nec ante pretium faucibus. Phasellus tincidunt mollis magna, in tincidunt ligula scelerisque a.</p>
        </div>
    </div>

    <!-- Menu -->
    <nav id="menu">
        <ul class="links">
            <li><a href="#"><h3>Home</h3><p>Lorem ipsum dolor sit amet</p></a></li>
            <li><a href="#"><h3>About</h3><p>Learn more about us</p></a></li>
            <li><a href="#"><h3>Services</h3><p>Discover our services</p></a></li>
            <li><a href="#"><h3>Contact</h3><p>Get in touch</p></a></li>
        </ul>
    </nav>

    <!-- Footer -->
    <footer id="footer">
        <div class="icons">
            <p>Follow us on social media!</p>
        </div>
        <div class="copyright">
            <p>&copy; 2025 My Website. All rights reserved.</p>
        </div>
    </footer>

    <!-- Scripts (optional) -->
    <script>
        const menuButton = document.querySelector("#menuButton");
        const menu = document.querySelector("#menu");

        menuButton.addEventListener("click", () => {
            menu.classList.toggle("is-menu-visible");
        });
    </script>

</body>

</html>
