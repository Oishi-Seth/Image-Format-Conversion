# Image-Format-Conversion

Source format: 		24-bit BMP
Destination format: 	Uncompressed GIF

Limitations:
1. Converts only those images whose number of distinct colours doesn't exceed 128.
2. Converts only those images whose width is a multiple of 4.


There are three important .c files here:
1. bmp.c :- 
This file reads in the essential details of a bmp image, including the pixels' colour data.

2. gif.c :-
This file stores the pixels' colors into a global colour table, which is then used for writing colour data of pixels into a GIF file.
It also writes in essential details required for defining the GIF file.

3. main.c :- 
This file calls functions new_BMP and new_GIF. 

Other files are:
1. format.h is the header file containing the structs of BMP and GIF, function prototypes and includes some standard .h files .
2. makefile is for code compilation.



Commands for running the file:
1. $ make my_project :- For making the OUT file
2. $ ./my_project "source_image_name".bmp "output_image_name".gif  :- For getting the image output
3. $ make clean  :- For removing the .o files



CODE INSPIRED BY:
1) https://en.wikipedia.org/wiki/GIF#Uncompressed_GIF
2) https://elcharolin.wordpress.com/2018/11/28/read-and-write-bmp-files-in-c-c/
3) http://giflib.sourceforge.net/whatsinagif/bits_and_bytes.html
