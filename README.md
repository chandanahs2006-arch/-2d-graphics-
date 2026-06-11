# MiniProject 2D Graphics Editor

A simple C console application that lets you draw basic shapes on an ASCII canvas.

## Features

- Add objects: line, rectangle, circle, triangle
- Delete objects by index
- Modify existing objects
- Render the canvas as ASCII art in the console
- List active objects

## Project Structure

- `miniproject.c` - main source file containing the editor logic and rendering code

## Canvas

- Width: 80 characters
- Height: 24 lines
- Empty pixel: `_`
- Drawn pixel: `*`

## Build Instructions

Use a standard C compiler like `gcc`.

```sh
gcc miniproject.c -o miniproject -lm
```

> The `-lm` flag is required because the code uses `sqrt()` from the math library.

## Run Instructions

```sh
./miniproject
```

On Windows PowerShell:

```powershell
.
```

## Usage

The program displays a menu with options:

1. Add object
2. Delete object
3. Modify object
4. Display picture
5. List objects
0. Exit

When adding or modifying shapes, follow the prompts for coordinates and radius.

### Shape input formats

- Line: `x1 y1 x2 y2`
- Rectangle: `x1 y1 x2 y2` (top-left and bottom-right corners)
- Circle: `x y radius`
- Triangle: `x1 y1 x2 y2 x3 y3`

## Notes

- Coordinates are based on the canvas grid and should stay within the 80x24 bounds.
- Shapes are drawn using ASCII characters and may appear approximate for circles.
- Deleted objects remain in the object buffer but are marked inactive.
