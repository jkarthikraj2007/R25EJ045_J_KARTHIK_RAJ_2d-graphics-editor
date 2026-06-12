Portfolio Website
A single-page personal portfolio built with plain HTML and CSS, styled as a developer terminal/code-editor theme.

Live Demo
https://jkarthikraj2007.github.io/

Features
Terminal-style hero section introducing me and my focus areas
Projects section with descriptions, tech tags, and links to source/live demos
Skills section grouped by languages, tools/frameworks, and domains
Education and certifications
Fully responsive, dark-themed design


Tech Stack


HTML5
CSS3 (custom properties, flexbox, grid)
Google Fonts (JetBrains Mono, Inter)


Running Locally


Clone this repository


bash   git clone https://github.com/jkarthikraj2007/jkarthikraj2007.github.io.git


Open index.html in any browser


Deployment
Hosted via GitHub Pages, deployed from the main branch root.

Author
J Karthik Raj

# 2D Graphics Editor (ASCII Art using `*` and `_`)

A simple command-line 2D graphics editor written in C that lets you draw, manage, and display basic shapes — lines, rectangles, circles, and triangles — on a character-based canvas.

## Features

- **Draw primitives**: line, rectangle, circle, triangle
- **Object management**: add, delete, and modify shapes
- **2D character array** as the canvas/picture buffer
- **Menu-driven interface** for interaction
- Display the rendered picture on screen

## Canvas Representation

The picture is stored internally as a 2D `char` array (`canvas[ROWS][COLS]`). Each cell represents one character position on screen. Shapes are drawn by setting cells to a chosen character (e.g., `*` or `_`).

Coordinate convention:
- `x` → row index (0 to ROWS-1)
- `y` → column index (0 to COLS-1)

## File Structure

```
2d-graphics-editor/
├── editor.c       # Main source code
├── README.md      # This file
├── LICENSE        # License file
└── .gitignore     # Ignored files (binaries, IDE configs)
```

## How to Compile and Run

```bash
gcc editor.c -o editor
./editor
```

## Menu Options

```
1. Add Line
2. Add Rectangle
3. Add Circle
4. Add Triangle
5. Delete Object
6. Modify Object
7. List Objects
8. Display Picture
9. Exit
```

## Usage Examples

| Shape     | Input Format                          | Example            |
|-----------|----------------------------------------|---------------------|
| Line      | `x1 y1 x2 y2 char`                     | `5 5 5 30 *`        |
| Rectangle | `x y width height char`                | `2 5 10 8 *`        |
| Circle    | `xc yc radius char`                    | `12 30 5 *`         |
| Triangle  | `x1 y1 x2 y2 x3 y3 char`               | `2 2 10 2 6 10 *`   |

### Sample Workflow

1. Choose `1` to add a line, enter `5 5 5 30 *`
2. Choose `3` to add a circle, enter `12 30 5 *`
3. Choose `8` to display the picture
4. Choose `7` to list all objects with their indices
5. Choose `6` to modify an object by index
6. Choose `5` to delete an object by index
7. Choose `9` to exit

## Implementation Details

- **Line drawing**: Supports horizontal, vertical, and diagonal lines (DDA algorithm for diagonals)
- **Circle drawing**: Midpoint circle algorithm for efficient point calculation
- **Rectangle**: Composed of four lines forming a closed boundary
- **Triangle**: Composed of three lines connecting the given vertices
- **Objects**: Stored in a struct array with an `active` flag, enabling soft deletion and modification

## Possible Future Enhancements

- Fill support for shapes (solid rendering)
- ncurses-based interactive menu and live drawing
- Save/load picture to/from file
- Undo/redo functionality

## Author

J Karthik Raj

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
Email: rajkarthik622@gmail.com
LinkedIn: j-karthik-raj
GitHub: jkarthikraj2007
