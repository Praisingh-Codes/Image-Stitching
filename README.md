## <div align="justify">Title - An Advanced Panorama Stitching Framework with Cylindrical Projection, Multi-Blend Strategies, and Homography Caching </div>

##  Introduction

<div align="justify">
Panorama stitching is a fundamental task in computer vision that enables the creation of wide-angle composite images by aligning and blending multiple overlapping photographs. While traditional stitching approaches often face challenges such as parallax distortion, exposure differences, and seam visibility, advanced techniques are required to produce seamless, high-quality results. This project introduces an advanced panorama stitching framework that integrates cylindrical projection to minimize perspective distortion, multiple blending strategies (direct, feather, and multiband) to enhance visual smoothness, and a homography caching mechanism for efficient re-use of transformation matrices. The framework is further equipped with a Gradio-powered user interface, allowing users to interactively upload images, select blending options, toggle cylindrical projection, and visualize intermediate artifacts such as feature matches, inlier correspondences, and blending results. By combining robust feature detection, flexible blending pipelines, and modern visualization tools, this system provides both researchers and practitioners with a powerful and practical solution for building high-quality panoramic images.
</div>

##  Structure 

├── samples/  # Sample input images for panorama stitching 

├── gradio test samples/  # Test images for Gradio interface demo 

├── stitching_&_creating_panorama_code.ipynb  # Main Jupyter notebook with code & UI

├── requirement.txt # Required Python libraries for the project

## Setup Instructions

1. Clone the Repository

    Terminal - Command - Git Clone 

    https://github.com/Praisingh-Codes/Image-Stitching.git

    cd Image-Stitching


2. Create Virtual Environment

   Terminal - Command
   
   python -m venv venv
   
   source venv/bin/activate 
   
   (On Windows: venv\Scripts\activate)


3. Install Dependencies
   
   Terminal - Command
    
   pip install -r requirements.txt


4. Prepare Input Images

   Place your image set in the samples/ directory.

   samples/

      ├── img1.jpg

      ├── img2.jpg

      ├── img3.jpg
      
      ...

      Images should have overlapping regions for effective feature matching. For wide panoramas, keep focal length metadata (EXIF) if possible.


5. Run the Jupyter Notebook
   
   Launch the notebook environment:
   
   jupyter notebook

   Open stitching_&_creating_panorama_code.ipynb in Jupyter Notebook and run the cells.


6. Use the Gradio Interfac
   
   Run the last cell in the notebook to launch the Gradio web app:
   
   - Upload 2–8 images with overlapping regions.

   - Select blend type: direct, feather, or multiband.

   - Toggle cylindrical projection and adjust focal length if needed.

   - Optionally load a saved homography cache (JSON) for faster recomputation.

   View outputs:

   - Final panorama

   - Gallery of visual artifacts (SIFT features, matches, intermediate blends)

   - Downloadable homography cache

   <div align="justify">
   The Gradio interface provides an interactive way to experiment with different stitching strategies while showcasing internal visualizations (matches, projections, blending levels). It ensures both transparency of the pipeline and flexibility for users to generate professional-quality panoramas. </div>

## Conclusion

<div align="justify">
This project presents a robust and advanced panorama stitching framework that combines classical computer vision techniques with modern usability features. By employing SIFT feature extraction, KNN and BF matching, RANSAC-based homography estimation, and multiple blending strategies such as direct, feather, and multiband, the system achieves seamless panoramic reconstruction even in complex scenarios. The integration of cylindrical projection enhances wide-angle stitching performance, while the inclusion of homography caching significantly reduces redundant computations, improving efficiency. Furthermore, the Gradio-powered interface enables users to interactively select blending strategies, visualize intermediate outputs such as feature matches and inliers, and generate high-quality panoramas with ease. Overall, this work demonstrates how the synergy of algorithmic rigor and user-centric design can deliver a flexible, efficient, and professional-grade panorama stitching solution.
</div>
