# SPACEYYY

SATURDAY HACKNIGHT PROJECT -1

## Overview

SPACEYYY Explorer is an immersive, interactive web experience that takes users on a journey through the cosmos. This single-page application features stunning space visuals, animated elements, and an engaging user interface that brings the wonders of the universe to life.

## Features

### Visual Elements
- **Dynamic Star Field**: Randomly generated stars with twinkling animation
- **3D Planets**: Interactive planet elements with rotation and parallax effects
- **Animated Spaceship**: Moving spacecraft that traverses the screen
- **Galaxy Background**: SVG-based galaxy with spiral arms and rotating animation
- **Cosmic Dust Particles**: Floating particles that add depth to the space environment
- **Mouse Trail Effect**: Interactive cursor trail that follows user movements

### Interactive Elements
- **Parallax Scrolling**: Elements move at different rates based on scroll position
- **Cursor Effects**: Stars react to cursor proximity
- **Planet Hover Effects**: 3D rotation effects on hover
- **CTA Button Animation**: Elastic animation on hover
- **Ambient Sound**: Optional space ambient sound with toggle functionality

### Animations
- **Loading Sequence**: Staggered reveal animations for page elements
- **Scroll Animations**: Content reveals as user scrolls down the page
- **GSAP Animations**: Powered by the GreenSock Animation Platform

## Technologies Used

- **HTML5**: Modern semantic markup
- **CSS3**: Advanced styling with CSS variables, flexbox, and CSS animations
- **JavaScript**: Vanilla JS for interactive elements
- **GSAP**: GreenSock Animation Platform for smooth, performant animations
- **ScrollTrigger**: GSAP plugin for scroll-based animations
- **SVG**: Vector graphics for the galaxy background and spaceship

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Basic knowledge of HTML, CSS, and JavaScript

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/spaceyyy-explorer.git
```

2. Navigate to the project directory:
```bash
cd spaceyyy-explorer
```

3. Open `index.html` in your preferred browser, or use a local development server:
```bash
# Using Python
python -m http.server

# Using Node.js
npx serve
```

## Customization

### Modifying Colors
The color scheme is defined in CSS variables and can be easily modified:
```css
/* Example of color customization */
body {
    background: #0a0a2a; /* Change the background color */
}

.logo span {
    color: #64f4df; /* Change the accent color */
}
```

### Adding Planets
Add more planets by following this pattern:
```html
<div class="planet" id="planet3"></div>
```

And define its style in CSS:
```css
#planet3 {
    width: 120px;
    height: 120px;
    background: radial-gradient(circle at 30% 40%, #f4a261, #e76f51);
    box-shadow: 0 0 20px rgba(231, 111, 81, 0.5);
    right: 20%;
    bottom: 30%;
}
```

Then animate it in JavaScript:
```javascript
mainTimeline.to('#planet3', {
    opacity: 1,
    x: -20,
    duration: 1.2,
    ease: "power2.out",
    onComplete: () => {
        gsap.to('#planet3', {
            rotation: 360,
            duration: 35,
            repeat: -1,
            ease: "none"
        });
    }
}, "-=1");
```

## Project Structure

```
space-explorer/
│
├── index.html          # Main HTML file
├── styles/             # CSS files 
│   └── style.css       # Main stylesheet 
├── scripts/            # JavaScript files
│   └── main.js         # Main script file
├── assets/             # Media files
│   ├── images/         # Images and SVGs
│   └── audio/          # Audio files
└── README.md           # This file
```

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Future Enhancements

- Add more interactive elements and space objects
- Implement WebGL for more advanced 3D effects
- Create additional sections for space exploration content
- Add a contact form and social media integration
- Develop a mobile app version with enhanced features

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Space imagery inspired by NASA photographs
- Sound effects sourced from royalty-free libraries
- GSAP documentation and examples

## Contact

For any questions or suggestions, feel free to reach out at ealiyasshaji@tistcochin.edu.in or open an issue on GitHub.

---

Made with ❤️ and cosmic dust
