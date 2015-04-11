# Deformation
Affine Tranformations using MLS

This is an implementation in Processing of affine transformations using the method proposed on:
http://faculty.cs.tamu.edu/schaefer/research/mls.pdf

So basically you can add, remove and traslate control points and drag them to generate their new positions.
There are some predefined deformations than can be used pressing the numbers.

This predifened deformations are:
  -Random
  -Scaling Width
  -Scaling Height
  -Horizontal splines in three different positions: Top, middle and Bottom. Here, basically some control points are
   added in a horizontal line at the top, the middle or the left of the shape. Then there are randomly added other points 
   that will be the images of the control points and then an interpolation of that points using hermite splines generates 
   some other images to make a smooth change.
   An additional option can be used pressing the key 'r' and in this case top and bottom methods will create a reflexion
   of the calculated spline at the top (if the method is bottom) or the bottom (if the option is top) of the shape.
  -Vertical spline: same idea as before but modifing the width of the shape.
  -Combination: Mix scaling and splines methods.
  
It's important to know that the proposed method, do a preprocessing of the image (Basically a threshold) to consider
only the outter contour of it. 