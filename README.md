# SPIP V3.24
Root Tracing Algorithm 

# Steps for the Root Tracing
1. Press the File Button and select Image Sequence.
	1. Choose the first Image in the Image Sequence.
2. After selecting the first Image in the Image Sequence, press the "Draw Reference Region Button" and select the region by dragging the mouse to the desired reference region.
	1. Once the Reference Region is done, Click the "Confirm Reference Region" button. ( the Image Sequence Path should appear on the Reference Region Box and the user should be able to change between plates) .
3. After selecting and confirming the Reference region for each Plate(s), start the stabilization process by clicking the "Stabilize Images (All Plate(s))"
4. Once the Stabilization is done, continue by drawing the seeds region by selecting the "Draw Seeds Region" button, and use the mouse to create an area of interest. 
	1. To add or remove seeds, click the "Add Seed" or "Remove Seed".
	2. Once, every seed is located in the current plate, click "Confirm Seeds Locations" button and the Image Sequence Path should be added to "Place(s) Ready For Tracing" box.
5. Once every seed in all plates are located, start the Tracing Root process by pressing "Trace Roots (All Plates)"

Afterevery step is done, there should be a Stats, EigenAngle, Hessian, Imgs_Stabilized, Mark, and MarkColor Folder under the Plate's folder. 
# Optional

There is an option to see visualy the pixel moves per frame on any root on any Plate, to do this, press "Select Root" and type in the number of the root to be displayed. 

# Notes

1. If there is already an  Imgs_Stabilized folder under the Plate Path, Root Tracing can be done without doing steps 1 and 2
2. Even though some steps can be performed without others, the program best operates if each steps is done in order on each Plate. 

# Stopping Any Process

If you already drew the reference region, and by accident pressed the button again, just clicked in any point on the screen, and it would cancel the useer input. 

If the "Add Seed" or "Remove Seed" button is selected and want to cancel the process, just pressed the stop button that is below "Remove Seed". The same process apply for cancelling Stabilization and Tracing. 

# Common Errors

Array Out Of Bounds Error: when the user uses the get Rectangle function from either "Draw Reference Region" or "Add Seeds Region" and the selected area is outside from the picture frame, it would generate a "Array Out Of Bounds Error".

Mask Error: This error occurs when adding the seed region, and each seed's response from the Second Derivate is less than 2, it would not be able to detect the seed. Hence, producing a "Mask To small Error". Since this error is due to data, to fix this, a clearer plate should be provided. 




