# 3D Rubik’s Cube Simulator (Web-Based)

## Overview
This project is a fully interactive 3D Rubik’s Cube simulator built using HTML, CSS, and Vanilla JavaScript.
It allows users to dynamically generate Rubik’s Cubes of any size from 2×2 up to 100×100, rotate the cube in 3D space, perform standard cube moves, apply lane-based rotations, shuffle the cube, and track the exact path of moves used to scramble the cube.

The simulator focuses on logical cube behavior, accurate face rotations, and a clean interactive UI—making it useful for learning cube algorithms, visualization, and algorithm tracing.

## Key Features
- Dynamic Cube Size
  - Supports cube sizes from 2 to 100
  - Automatically adjusts face grids and valid lane ranges

- 3D Cube Rotation
  - Click-and-drag mouse interaction
  - Smooth X/Y axis rotations using CSS 3D transforms

- Standard Rubik’s Cube Moves
  - Supports:
   ```
     R, R′, L, L′, U, U′, D, D′, F, F′, B, B′
   ```
  - Works for outer and inner lanes
- Lane-Based Moves
  - Users can enter a lane number
  - Valid lanes are calculated automatically (odd/even cube sizes)
  - Buttons dynamically update (e.g., R2, U′1)

- Shuffle Function
  - Random number of random moves
  - Random lane selection for large cubes
  - Tracks shuffle moves accurately

- Move Counter
  - Counts all user and shuffle moves
  - Updates in real time

- Path to Solve
  - Displays the exact sequence of moves
  - Includes lane numbers
  - Helps in replaying or reversing scrambles

- Clean & Responsive UI
  - Modern dark theme
  - Responsive layout for different screen sizes
 
## Tech Stack

| Technology                         | Purpose                   |
| ---------------------------------- | ------------------------- |
| HTML5                              | Structure                 |
| CSS3                               | Styling & 3D transforms   |
| JavaScript (Vanilla)               | Cube logic & interactions |
| CSS Grid                           | Face layout               |
| CSS `transform-style: preserve-3d` | 3D rendering              |


## How to Run the Project
1. **Clone the Repository**
  ```
    git clone https://github.com/your-username/3d-rubiks-cube.git
    cd 3d-rubiks-cube
  ```
2. **Open in Browser**
   Simply open the HTML file:
   ```
     index.html
   ```
  - No server
  - No dependencies
  - Works offline

## How to Use
1. Enter Cube Size (2–100)
2. Click Generate Cube
3. Drag mouse to rotate the cube in 3D
4. Click Play
5. Enter a Lane Number
6. Use move buttons(R, U′, F, etc.)
7. Click Shuffle to randomize
8. Click Path to Solve to view move history

## Lane Number Rules
- Odd-sized cube (e.g., 3×3):
    ```
      Lane range: 0 → ⌊N/2⌋
    ```
- Even-sized cube (e.g., 4×4):
    ```
      Lane range: 0 → (N/2 − 1)
    ```
The system automatically validates lane input.

## Internal Logic Highlights
- Each face is a 2D matrix
- Face rotations use matrix transpose + reversal
- Adjacent face strips are rotated in correct order
- Inner layers rotate without affecting face centers
- Move tracking wraps every rotation function

## Project Structure

```
.
3d-rubiks-cube/
│
├── index.html                        
└── README.md        
```

## Conclusion
The 3D Rubik’s Cube Simulator (Web-Based) demonstrates how complex 3D puzzles can be effectively modeled using standard web technologies. With support for dynamic cube sizes, lane-based rotations, and all standard cube moves, the project emphasizes accurate logical behavior beyond simple visualization.

Matrix-based transformations ensure precise face and layer rotations, while features like move tracking, shuffle history, and path-to-solve visualization make it valuable for learning and analyzing cube algorithms. Overall, the project showcases the power of HTML, CSS 3D transforms, and Vanilla JavaScript for building interactive, browser-based applications and provides a strong foundation for future enhancements.



