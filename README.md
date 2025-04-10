# Computer-Graphics
# Atom Simulation - OpenGL Visualization

This project is an educational visualization tool that simulates the atomic structure of the first ten elements of the periodic table (Hydrogen to Neon) using OpenGL and GLUT. It provides an interactive graphical representation of atoms based on the Bohr model, allowing users to visualize the nucleus and orbiting electrons with animation.

## Features

* **Visual Representation:** Displays the nucleus and electron orbits for Hydrogen to Neon.
* **Interactive Controls:**
    * Right-click menu for element selection.
    * Start/stop electron animation.
    * Full-screen toggle (F10).
    * Keyboard controls for animation and exit.
* **Bohr Model Simulation:** Illustrates electron orbits and placements according to the Bohr model.
* **Educational Tool:** Helps visualize atomic structures for introductory chemistry and physics.

## Implementation Details

This project leverages OpenGL and GLUT for graphical rendering and user interaction. Key OpenGL functions used include:

* **Window and Projection Setup:**
    * `glutInit`, `glutCreateWindow`, `gluOrtho2D`
* **Drawing Primitives:**
    * `glBegin(GL_POINTS)`, `glBegin(GL_POLYGON)`, `glEnd`, `glVertex2i`, `glVertex2f`
* **Color and Text Rendering:**
    * `glClearColor`, `glColor3f`, `glRasterPos3f`, `glutBitmapCharacter`
* **Transformation and Animation:**
    * `glPushMatrix`, `glRotatef`, `glPopMatrix`, `glutIdleFunc`
* **Event Handling:**
    * `glutDisplayFunc`, `glutMouseFunc`, `glutKeyboardFunc`, `glutSpecialFunc`
* **Menu System:**
    * `glutCreateMenu`, `glutAddMenuEntry`, `glutAddSubMenu`, `glutAttachMenu`, `glutDetachMenu`
* **Buffer Management:**
    * `glClear`, `glutSwapBuffers`

### Core Drawing Logic

* **Nucleus:** Drawn as a blue filled circle using `GL_POLYGON`.
* **Electron Orbits:** Drawn as red circles using `GL_POINTS`.
* **Electrons:** Drawn as white filled circles using `GL_POLYGON`.
* **Text:** Displayed using `glutBitmapCharacter` for element names and labels.

### Element Visualization Strategy

The program visualizes elements by:

* Drawing the nucleus as a central blue circle.
* Drawing one orbit (radius 400) for the first electron shell (K shell).
* Drawing a second orbit (radius 600) for the second electron shell (L shell).
* Placing electrons at specific positions based on the Bohr model.
* Animating electrons using rotation transformations.

## Getting Started

### Prerequisites

* OpenGL and GLUT libraries installed.
* A C/C++ compiler (e.g., GCC).

### Compilation

1.  Clone the repository:

    ```bash
    git clone [repository URL]
    ```

2.  Compile the code (example using GCC):

    ```bash
    g++ main.cpp -o atom -lGL -lglut -lm
    ```

3.  Run the executable:

    ```bash
    ./atom
    ```

## Usage

* **Element Selection:** Right-click to open the menu and select an element.
* **Start/Stop Animation:** Use the menu or press the spacebar (start) and 's' (stop).
* **Full Screen:** Press F10.
* **Exit:** Press 'q' or 'Q'.

## Limitations

* Currently supports only the first ten elements (Hydrogen to Neon).
* Uses a simplified Bohr model, which does not accurately represent electron behavior for larger atoms.
* Electron orbital shapes are not accurately represented.
* The red color of the orbits is outside of the normal 0-1 range.

## Future Improvements

* Extend support to include more elements.
* Implement more accurate electron configuration representation.
* Incorporate 3D visualization for d and f orbitals.
* Improve animation and interactivity.
* Fix the color range of the orbits.
* Implement better orbit radius scaling.

## Author

* [Your Name(s)] - [Your GitHub Profile(s)]

## License

This project is [License Type] - see the [LICENSE.md](LICENSE.md) file for details.
