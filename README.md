# Real-Time Webcam Tools: ASCII Art & Particle Engine

This project contains two purely browser-based, high-performance visual applications that tap into your webcam locally using HTML5, Canvas, and JavaScript. 

There are no databases on the backend and no data is ever sent over the internet! Your privacy is completely safe.

## Files Included

1. **`index.html`** - The Real-Time ASCII Art web application.
2. **`particles.html`** - The Real-Time Particle Mirror application.

## Requirements

- **Python 3.x** (Used exclusively to run a local web server to serve the HTML pages, overcoming modern browser CORS/Webcam origin security policies).
- **A Webcam** connected to your device.
- **A Modern Web Browser** (Chrome or Safari recommended).

## How to Run

1. Open your terminal.
2. Navigate into the project folder (`ascii_face`).
3. Run Python's built-in HTTP server:
   ```bash
   python3 -m http.server 8000
   ```
4. Open your browser and go to one of the following addresses:
   - For ASCII Map: [http://localhost:8000/index.html](http://localhost:8000/index.html)
   - For Particle Engine: [http://localhost:8000/particles.html](http://localhost:8000/particles.html)
5. When prompted by your browser, **allow camera access**.

## How to Use

### The ASCII App
The ASCII app translates your camera's luminance mappings into 1s and 0s perfectly filling the window.
- **Font Size**: Changes the density/size of the rendering. 
- **Contrast**: Adjusts how intensely dark shadows pop against light settings.
- **Gain**: Use this to increase brightness if you are in a dark room.

### The Particles App
The Particle Engine tracks bright elements of your camera mapping them natively to Canvas vectors at 60 Frames Per Second.
- **Density**: Controls the number of active particle dots allocated to your video target (WARNING: higher values require a faster CPU).
- **Size**: Increases the radius of every individual particle dot.
- **Speed**: Physics lerp coefficient determining how fast dots travel to assemble your form. 
- **Scatter Button**: Explodes the structure currently mapped on-screen.

*Note: In both applications, you can independently jump between Green Matrix, Ghost White, or Evil Red color themes.*
