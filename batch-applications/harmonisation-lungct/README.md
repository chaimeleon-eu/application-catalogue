# harmonisation-lungct

## Description
Lung CT harmonisation that harmonises low-resolution CT scans to high-resolution CT scans

## Usage

`jobman submit -i harmonisation_lungct -- python3 sr_model.py -i <INPUT_DIR> -o <OUTPUT_DIR> -g|-1`
  
The application accepts 3 parameters:
 - The path to the input directory with DICOM files
 - The output directory where harmonized image will be saved.
 - Wheter to use GPU (`-g`) or CPU (`-1`)
 
Example:  
  ```
    jobman submit -i harmonisation-lungct -- python3 sr_model.py\
                                             -i ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/patient01/ \
                                             -o ~/persistent-home/results_harmonisation/ \
                                             -1
  ```
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job. 

## Authors
Imperial

## Contact info
??

## URL
Private\* dockerfile repository:
https://github.com/chaimeleon-eu/image_batch_lungCT_harmonisation  
\* You will see error 404 if you don't have permissions to access.

## License
https://github.com/chaimeleon-eu/application-catalogue/blob/main/batch-applications/harmonisation-lungct/LICENSE.md
