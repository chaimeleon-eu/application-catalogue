# deepfakes-detector

## Description
The tool helps users to identify tampered images inside or uploaded to the CHAIMELEON repository.
It can identify the following forms of tampering: adversarial noise, copy move and AI based editing, aka Deepfakes.
The developed tool uses a Deep Neural Network (DNN) to detect these manipulations.
This tool employs a technique called inpainting, and the model is trained in an unsupervised manner on a specific modality and body region (e.g. CT scans of the lungs). We provide two pretrained models and the user can train his/her own. The pretrained models are trained on chest MRI or lung CT scans. 
To use the tool, the user points the target model to an area of interest within the image (e.g. a tumor or a noisy area) and gets a score indicating whether the area has been manipulated or not.

## Usage
This tool provide two seperate capabilities:
- Training of DeepFakes detection models
- Inference using pretrained/user provided models

### Training
The tool is based on an inpainting DNN, hence to train new models, the user must provide training data in the form of DICOM(.dcm) files.
We recommend selecting just slices containing areas of interest(e.g. tumors) for the training set.


### Inference
For inference the user must provide a path to a trained detection DNN, and a test folder containig: (1) folders with .dcm files and (2) a csv file with regions to check in the following format: | filename(.dcm) | X | Y |.

### File structure
The folder structure should be:
```
datasets
+──train
|   |   p1
│   │     file011.dcm 
│   │     file012.dcm
|   |     ...
|   |   p2
|   |     ...
│   |  ...
+──test
|   |   p1
│   │     file011.dcm 
│   │     file012.dcm
|   |   p2
|   |     ...
|   |  ...
|   |   test.csv
```

### Run Examples
Train example:
```
jobman submit -i deepfakes-detector -- -mode Train \
                                       -model_path ~/persistent-home/deepfakes-detector/models/my_model.ckpt \
                                       -data_path ~/persistent-home/deepfakes-detector/train \
                                       -epochs 100 -batch_size 64 -num_workers 6
```

Test example:
```
jobman submit -i deepfakes-detector -- -mode Test \
                                       -model_path './app/models/<Modality>_InPainting.ckpt' \
                                       -data_path ~/persistent-home/deepfakes-detector/test 
```
For pretrained models replace \<Modality\> with CT or MRI.  
For user models put the path to the model (e.g. "~/persistent-home/deepfakes-detector/models/my_model.ckpt").

## Authors
BGU

## Contact info
??

## URL
Private\* dockerfile repository:
https://github.com/chaimeleon-eu/image_batch_deepfakesdetector  
\* You will see error 404 if you don't have permissions to access.

## License
None
