This is a one-page application displaying a 3D ring model. The model is downloaded for free from:

https://www.cgtrader.com/free-3d-print-models/jewelry/rings/jewelry-diamond-ring-model-rg89

Page Generation:
The page is generated using AI. As it has to open local files, a web server is needed to deliver the page and the files. It is a temporary http server delivered by using Python:

python -m http.server 8000

Run the above command from the directory where the page and the files are located. View the page by opening the following URL:

http://localhost:8000/

Model Correction and Optimization:
The 3dm file is downloaded and opened in Rhino. The diamonds model is exported and opened in Blender to fix face normal direction by Mesh -> Normal -> Recalculate Outside. The ring model is exported as obj and imported in ZBrush. It is converted into DynaMesh and smoothed to remove hard edges. It is then decimated and exported back to Blender. Both models are compressed and exported as glb files in Blender. 

The respository is deployed to Github pages and can be viewed in the following URL:

https://jmmychow.github.io/ring/
