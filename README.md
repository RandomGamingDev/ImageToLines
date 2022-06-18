### ImageToLines

This is a program that converts your image to a series of lines (and sometimes dots).

The way that this works is quite simple.<br/>
The program just takes the image and loops over each pixel, for which it samples all 9 surrounding pixels (including the pixel it's iterating over), and it calculates the average difference/contrast, for which it then places a pixel if there's enough contrast, and doesn't place a pixel if there isn't enough.

To start you want to compile the program using cargo build.<br/>
Then you want to create the files img_name.txt, pixel_drawing_settings.txt.<br/>
You can then plop in your image.<br/>
Write the filepath to your image in img_name.txt.<br/>
Then write the contrast setting (what minimum contrast is required to draw a pixel) in pixel_drawing_settings.txt (there are currently no other settings that can be modified in pixel_drawing_settings.txt, but modifying the executable is easy enough).<br/>
After that you can run the program and you should have your image in output.jpeg!<br/>

Btw, this uses the CPU rather than the GPU. The speed is still good enough, where even a high quality images don't take that long to generate.
