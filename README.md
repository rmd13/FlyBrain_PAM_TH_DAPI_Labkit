# FlyBrain_PAM_TH_DAPI_Labkit
Predict the dopaminergic neuron's cell bodies in the PAM cluster of Drosophila brain stained with anti-TH antibody.

# Materials required:
1. Z-stack tif files of Drosophila brain PAM cluster image on anti-Tyrosine Hydroxylase(TH) channel, with a image size x=512, y=512, z between 10 and 25, with an interval of 0.34 um. The PAM cluster from one half of brain was freely rotated and zoomed when necessary to fit the entire PAM cluster into the image region. Avoid overexposure.
2. Matlab (Mathwork).
3. Fiji/Imagej[https://imagej.net/software/fiji/downloads], with labkit[https://imagej.net/imagej-wiki-static/Labkit] installed.
4. A computer with dedicated high-end GPU, such as Quadro P6000.

# Installation and demo
1. Run the Fiji and open one TH stack (can use the demo TH-stack), then import the image into the Labkit.
2. Clear the pre-defined classes by clickling the delete/Remove button on left.
3. Load the "57C10.eGFP.IR-day32-PAM-TH-add5.classifier" into the Labkit using menu "load classifier".
4. Click "Batch" menu, and input the folder path that contains all the TH channel z-stacks (can use the demo TH-stack) only, also create an empty output folder and specify it.
5. Start run batch.
6. After step 5, then open "Correct_Labkit_TH.m" in Matlab.
   Edit the "labkit_output_folder" to the output folder from step 4.
   Create another empty output folder, specify it by edit "labkit_output_correct_folder".
7. Run the "Correct_Labkit_TH.m" in Matlab. You will get corrected mask z-stack.

