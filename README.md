Hermite Bezier Curve
====================
## Bresenham's Circle Drawing Algorithm
Bresenham's Circle Algorithm is an algorithm for drawing circles in a discrete coordinate space such as a pixel grid. It is an efficient algorithm that utilizes the symmetry of a circle and the principle of rasterization to draw a circle without floating-point calculations. The algorithm starts at the top of the circle and moves around it in a clockwise direction, plotting points in each of the octants (or eighths) of the circle simultaneously. This is done using only integer addition, subtraction, and bit shifting, which are very efficient operations on a computer.

# Bresenham's Line Drawing Algorithm
Bresenham's Line Algorithm is another efficient incremental scan conversion algorithm, which is used to draw lines in a bitmap image. The algorithm determines which pixels should be plotted in order to form a close approximation to a straight line between two given points. It is particularly useful for drawing lines on low-resolution devices, where the steepness of the line could result in uneven stepping along the pixel grid. This algorithm also uses only integer addition, subtraction, and bit shifting to calculate the pixels to draw, avoiding the need for floating-point arithmetic.

Cubic polynomial splines are extensively used in computer graphics and geometric modeling to obtain smooth and continuous curves that are easy to compute and can accurately model complex shapes.

## Bresenham Algorithms Implementation

This Java implementation provides methods to draw lines and circles using Bresenham's algorithms on a pixel grid.

## Bresenham's Circle Drawing Algorithm

The `Bresenham` class contains a method `bresenhamCircle` that implements Bresenham's Circle Drawing Algorithm. This method takes the center coordinates `(x, y)`, the `radius` of the circle, and the RGB color values `r`, `g`, `b` to draw the circle on the image.

### Usage

```java
// Create a Bresenham object with image width, height, and background color
Bresenham bresenham = new Bresenham(width, height, red, green, blue);

// Draw a circle at (xCenter, yCenter) with a specified radius and color
bresenham.bresenhamCircle(xCenter, yCenter, radius, red, green, blue);

// Write the image to a file
bresenham.write("circle.png");

