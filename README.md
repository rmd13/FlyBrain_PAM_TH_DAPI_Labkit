# FlyBrain_PAM_TH_DAPI_Labkit
Predict the dopaminergic neuron's cell bodies in the PAM cluster of Drosophila brain stained with anti-TH antibody.

# link to the code
https://github.com/rmd13/FlyBrain_PAM_TH_DAPI_Labkit

# Materials required:
1. Z-stack tif files of Drosophila brain PAM cluster image on anti-Tyrosine Hydroxylase(TH) channel, with a image size x=512, y=512, z between 10 and 25, with an interval of 0.34 um. The PAM cluster from one half of brain was freely rotated and zoomed when necessary to fit the entire PAM cluster into the image region. Avoid overexposure.
2. Matlab (Mathwork).
3. Fiji/Imagej<https://imagej.net/software/fiji/downloads>, with labkit<https://imagej.net/imagej-wiki-static/Labkit> installed.
4. A computer with dedicated high-end GPU, such as Quadro P6000.

# Installation guide
operating system:Windows 8/10+
programing language: Matlab
software: Matlab(2014~now), Fiji and Labkit (if not included)
dependencies: no
typical install time on a current computer: 1~3 hours.

# demo with example data (typical run time: 5~10 minnutes)
1. Run the Fiji and open one TH stack (can use the demo TH-stack), then import the image into the Labkit.
2. Clear the pre-defined classes by clickling the delete/Remove button on left.
3. Load the "57C10.eGFP.IR-day32-PAM-TH-add5.classifier" into the Labkit using menu "load classifier".
4. Click "Batch" menu, and input the folder path that contains all the TH channel z-stacks (can use the demo TH-stack) only, also create an empty output folder and specify it.
5. Start run batch.
6. After step 5, then open "Correct_Labkit_TH.m" in Matlab.
   Edit the "labkit_output_folder" to the output folder from step 4.
   Create another empty output folder, specify it by edit "labkit_output_correct_folder".
7. Run the "Correct_Labkit_TH.m" in Matlab. You will get corrected mask z-stack.

# License
MIT license
Copyright <2024> 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
