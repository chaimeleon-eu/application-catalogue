# mri_harmonization

## Description
AI based tool that performs intensity harmonization in MRI images, and resolution enhancing to CT images.

## Usage

`jobman submit -i mri_harmonization -- <INPUT_DIR> <OUTPUT_DIR> <MODEL>`
  
The application accepts 3 parameters:
 - The path to the input directory with DICOM files
 - The output directory where harmonized image will be saved.
 - The model to use (options: `prostate`, `breast`, `rectum`, `lung`)
 
Example:  
  ```
    jobman submit -i mri_harmonization -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/patient01/ \
                                          ~/persistent-home/results_hamonization/ \
                                          prostate
  ```
If you want to accelerate the process with a GPU, you must use the proper tag in the image (`:latest-cuda`) and add a resource flavor with GPU (for example `-r small-gpu`):  
  ```
    jobman submit -i mri_harmonization:latest-cuda -r small-gpu -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ \
                                                                   ~/persistent-home/results_harmonization/ \
                                                                   prostate
  ``` 
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
QUIBIM

## Contact info
??

## URL
Private\* dockerfile repository:
https://github.com/chaimeleon-eu/image_batch_mri_harmonization/tree/development  
\* You will see error 404 if you don't have permissions to access.

## License
None
