# DICOM Viewer

**Digital Imaging and Communications in Medicine (DICOM)** is an internationally recognised standard for the communication and managment of medical
imaging information and related data. DICOM standard is used in several imaging modalities, such as radiography, CT, MRI...

DICOM files contain pixel information, as well as a lot of metadata about the method used to acquire the image, its orientation, study and patient information, amongst others. Allowing users to combine imaging and non-imaging data. For this reason, DICOM files are a great source of information in the field of medical imaging and image analysis and research.

This mini-app allows users to interactively visualise and explore 3D DICOM volume utilising *oro.dicom* and *oro.nifti* packages. These are to read DICOM files, display volums and extract DICOM metadata. Information about these packages can be found here: https://cran.r-project.org/web/packages/oro.dicom/index.html.
The sample DICOM images displayed are from MRIs (source: https://www.osirix-viewer.com/resources/dicom-image-library/, the library is called BRAINIX).

For more information about this app you can read the dedicated blog post at http://www.aridhia.com/blog/interactively-visualising-dicom-volumes-and-header-data/.

## About the app

You can select the patinet file to display using the dropdown menu on the left. Then, you can change the orientation of the image using the sliders below.
The image will be displayed in the middle of the screen, you can change the view plane by clicking on the Axial', 'Sagittal' or 'Coronal' tabs just above the image.
Under the image a table with the file information will be displayed. 
On the left-side of the screen, you will see the orthogonal position of your current view. 

The button on the bottom of the page to "Extract DICOM headers to database" only works if you are using the app within a workspace, and you have a dataset called "image_analysis_findings" in your database.

### Using your DICOM files

To use other DICOM files in the app, you can place the new folder inside the 'dicom_images' directory:

- Data
  - dicom_images
    - new_image_set
      - image1.dcm
      - image2.dcm
      - ...


### Checkout and run

You can clone this repository by using the command:

```clone
git clone https://github.com/aridhia/demo-dicom-viewer
```
Open the .Rproj file in RStudio and run `runApp()` to run the app. 

### Deploying to the workspace

1. Create a new mini-app in the workspace called "dicom-viewer" and delete the folder created for it
2. Download this GitHub repo as a .ZIP file, or zip all the files
3. Upload the .ZIP file to the workspace and unzip it inside a folder called "dicom-viewer"
4. Run the `dependencies.R` script to install all the packages required by the app
5. Run the app in your workspace

For more information visit https://knowledgebase.aridhia.io/article/how-to-upload-your-mini-app/


