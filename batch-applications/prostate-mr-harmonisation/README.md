# prostate-mr-harmonisation

## Description
This is a tool for Prostate MR harmonisation that harmonises MR scans to the given reference MR images.

## Usage

`jobman submit -i prostate-mr-harmonisation -r medium-gpu -- -i <INPUT_DIR> -o <OUTPUT_DIR> -r <INPUT_REF_NPZ>`
  
The application accepts 3 parameters:
 - The input path of a folder that contains nii.gz/mha/png/jpg files.
 - The output directory where harmonized image will be saved.
 - The reference .npz file for harmonisation (should be 3 stacked slices from the reference scan).
 
Example:  
  ```
    jobman submit -i prostate-mr-harmonisation -r medium-gpu -- \
        -i ~/persistent-shared-folder/apps/prostate-mr-harmonisation/examples/ \
        -o ~/persistent-home/results_hamonization/ \
        -r ~/persistent-shared-folder/apps/prostate-mr-harmonisation/examples/ref.npz
  ```
Note the output directory path should be any within the persistent-home, 
which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
Yang Nan Imperial College London

## Contact info
nandayanger@gmail.com
https://github.com/chaimeleon-eu/image_batch_ProstateMR_harm_IC/issues

## URL
Private\* dockerfile repository:  
https://github.com/chaimeleon-eu/image_batch_ProstateMR_harm_IC  
\* You will see error 404 if you don't have permission to access.

## License
https://github.com/chaimeleon-eu/application-catalogue/blob/main/batch-applications/prostate-mr-harmonisation/LICENSE.md
