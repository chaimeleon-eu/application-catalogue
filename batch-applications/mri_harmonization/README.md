# mri_image_intensity_harmonization

## Description
AI based tool that performs intensity harmonization in MRI images.

## Usage

`jobman submit -i mri_image_intensity_harmonization -- <INPUT_PATH> <OUTPUT_DIR> <MODEL> <INPUT_TYPE>`
  
The application accepts 4 parameters:
 - The path to the input file or directory with DICOM files
 - The output directory where harmonized Dicom files will be saved.
 - The model to use (options: `prostate`)
 - The type of input (options: `volume`, `series`)
 
Example:  
  ```
    jobman submit -i mri_image_intensity_harmonization -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/patient01/ \
                                          ~/persistent-home/results_hamonization/ \
                                          prostate series
  ```
If you want to accelerate the process with a GPU, you must use the proper tag in the image (`:latest-cuda`) and add a resource flavor with GPU (for example `-r small-gpu`):  
  ```
    jobman submit -i mri_image_intensity_harmonization:latest-cuda -r small-gpu -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ \
                                                                   ~/persistent-home/results_harmonization/ \
                                                                   prostate series
  ``` 
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
QUIBIM

## Contact info
xavierrafael@quibim.com
anajimenez@quibim.com

## URL
Private\* dockerfile repository:
https://github.com/chaimeleon-eu/image_batch_mri_harmonization/tree/development  
\* You will see error 404 if you don't have permissions to access.

## License
None
