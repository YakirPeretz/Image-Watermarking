# Image-Watermarking
Design and Verification of Image Watermarking component

Digital design of Watermarking component(peripherial to the CPU):
The CPU send the primary image and the wathetermarking image,pixel by pixel to, the component,using the APB bus protocol to communicate.
In addition, the CPU send a few parameters to my design: Block size(which the images divided to), the size of the images and parameters for calculations.
The images and the parameters saved in a register bank in my design.
After the CPU send a start bit, the component start tthe calculation for each pixel(there is an equations for each pixel for watermarking the image on the primary image),block by block,
and send it as an output.

Verification(System Verilog):
First, we had a Golden Model, a matlab code, which the design needed to get the same results as the golden model.
The verfication environment:
A stimulus file read the primary image and the watermarking image and send them to our design( the stimulus acts like the CPU here).
Using a checker(SVA) We checked that the APB bus protocol and the design works correctly.
In addittion, We compare the results from the design with the results of the Golden model.
With a functional coverage we checked that we covered all the design features.
