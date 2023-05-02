Download Link: https://assignmentchef.com/product/solved-cpsc1021-lab-10-c-classes-and-ppm-images
<br>
You were introduced to working with PPM files in lab 4. Lab 4 used 2 structs; 1 to represent the header of a ppm and 1 for the pixels of a ppm image.

In today’s lab, you are going to implement two classes, Header and Pixel both of which will represent ppm images. You are then going to write 4 driver files. Each of which will read in a ppm file, flip it horizontally, and write it back out. Each driver will store the pixels using different methods (1D Array, 2D Array, 1D Vector and a 2D Vector.)

<h1>Lab Objectives</h1>

<ul>

 <li>Practice with classes</li>

 <li>Image processing and manipulation</li>

 <li>Using vectors</li>

 <li>Using 2D vectors</li>

 <li>Working with dynamically allocated memory (1D and 2D)</li>

</ul>

<h1>Lab Instructions</h1>

I have provided you with header.hpp and pixel.hpp. You will implement the functions provided in each .hpp file. While I realize you may or may not use all of the functions, for practice you are still required to implement all of the functions provided in the .hpp files. You will then create 4 driver files named vec1DDriver.cpp, vec2DDriver.cpp, array1DDriver.cpp, and array2DDriver.cpp. As you probably have discerned, each of the driver files will use a different storage method for the image you will read.

What each driver should do:

Basically, each driver will read in a ppm image, flip the image horizontally and write it to the output file.

Create the input and output file stream. Each will be provided through command line arguments.

Allocate the space for the image. You can determine the amount of space needed from the information you read from the header. Read the pixels from the input image, flip the image horizontally and write them back out.

The horizontal flip function is not part of either class it should be implemented as an independent function in functions.h and functions.cpp. Below is the prototype for the horizontal flip function for the array2DDriver.cpp file. The prototype will change for each of the 4 driver.cpp files.

void HFlip(Header, Pixel**);

The <strong>HFlip</strong> function will iterate through all pixels providing the necessary code to flip an image horizontally. As an example, suppose I have a 3X3 image.  The <strong>Original</strong> matrix below represents the image with the pixels numbered 1-9.  Upon completion of the <strong>HFlip </strong>function the pixels should be in the order displayed by the <strong>Horizontally Flipped </strong>matrix<strong>. </strong>

Original                                      Horizontally Flipped

1          2          3                           3           2          1

4          5          6                           6           5          4

7          8          9                           9            8         7




You are also required to make sure you check that all input files open successfully. If they do not open successfully you should print a message and exit the program. You should check that the appropriate number of command line arguments are passed to the command line. If not print a message and exit the program. Rather than checking these in the main, you are required to create a function for each of these tasks.  These functions are to be implemented in the functions.cpp and the prototypes should be placed in the functions.hpp file.

Additional information:

<strong>Vector of vectors (multidimensional):</strong>

There are several examples of how to create multidimensional vectors online.  I have given you several links to look at:

<a href="https://www.geeksforgeeks.org/2d-vector-in-cpp-with-user-defined-size/">https://www.geeksforgeeks.org/2d-vector-in-cpp-with-user-defined-size/ </a><a href="https://stackoverflow.com/questions/823562/multi-dimensional-vector">https://stackoverflow.com/questions/823562/multi-dimensional-vector </a><a href="https://www.codeproject.com/Questions/456547/How-to-use-Multidimensional-vector-in-Cplusplus">https://www.codeproject.com/Questions/456547/How-to-use-Multidimensional-vector-in</a><a href="https://www.codeproject.com/Questions/456547/How-to-use-Multidimensional-vector-in-Cplusplus">Cplusplus</a>

Here is an example of a 2D vector I used to practiced with.

<table width="693">

 <tbody>

  <tr>

   <td width="693">vector&lt; vector&lt;int&gt; &gt; test;This is an empty vector of vectors of type <strong>int</strong> called <strong>test.</strong>I used resize to create memory for the 2D vector:Since you know the exact size of  the 2D vector using resize is more efficient than using Push_back().test.resize(10, vector&lt;int&gt;(5));I now have a 2D vector called test that is a 10 X 5 vector (10 rows, 5 cols). You can access the vectors using array notation or by using the safer function <strong>at()</strong>. I could have initialized each of the elements to a value when calling resize.</td>

  </tr>

 </tbody>

</table>