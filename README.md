# QUIZ-8
zlai0110
# Peace Dove Animation Project

This project aims to create a peace dove animation styled like old silent films, emulating the visual effects of early film cinema. The following content includes the inspiration, technical implementation, and related code for the project.

## Inspiration

The visual inspiration for this project primarily comes from the following aspects:

### Artistic Style References

1. **Georges Méliès' "A Trip to the Moon"** - Famous for its stop-motion animation and multiple exposure techniques, this film provides the core visual inspiration for our project.
2. **Early 20th-century silent films** - The distinctive black and white tones, frame rates, and visual effects of this era significantly influence the animation style of the peace dove.
3. **Artwork References**:
   - [Georges Méliès style image](https://pic1.zhimg.com/ecf7064ff3571941430e4c447df52850_r.jpg?source=1940ef5c) - This image showcases typical visual characteristics of early cinema.
   - [Early animation style example](https://th.bing.com/th/id/R.44b790d21ab012cf4afa3fa19824f85d?rik=522lO%2bQdKUrpEA&riu=http%3a%2f%2fwww.animationkolkata.com%2fblog%2fwp-content%2fuploads%2f2017%2f01%2fvZ1H1J5Nt3obIVx3tRZRWsquRKL.jpg) - An image displaying animation techniques from the early 20th century.

### Technical References

- **p5.js** - A JavaScript library well-suited for rapid development of visual art projects. [p5.js Official Website](https://p5js.org/)
- **Old animation techniques** - Such as stop-motion animation and multiple exposures, which will be simulated in our code implementation.
- **OpenProcessing Example** - Provides a technical example of animation implementation, reference link at [OpenProcessing Sketch](https://openprocessing.org/sketch/743533).

## Technical Implementation

This project is implemented using p5.js, simulating the visual effects of old film cinema through programming methods.

### Core Features

- **Stop-motion Animation**: Simulates the flying animation of the peace dove.
- **Multiple Exposure Effects**: Creates visual effects of ghosting or double exposures on the screen to enhance the retro feel.

### Code Example

```javascript
// Preload frames of the peace dove animation
function preload() {
  for (let i = 0; i < totalFrames; i++) {
    doveFrames[i] = loadImage('path_to_dove_frame_' + i + '.png');
  }
}

// Set up the canvas and frame rate
function setup() {
  createCanvas(800, 600);
  frameRate(10); // Control the frame rate
}

// Draw and update frames
function draw() {
  background(255, 255, 255, opacity); // Background processing for multiple exposures
  image(doveFrames[currentFrame], 50, 50); // Draw the peace dove
  currentFrame = (currentFrame + 1) % totalFrames; // Update frame index
}
