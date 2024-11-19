---
name: "📦 Request for addition of a new application"
about: "Do you want your application to be added in the catalogue?"
title: 'Add application: '
labels: 'add-application'
assignees: ''

---

<!-- Please replace the example content for each section and remove the comments like this. -->

# my-application  <!-- replace here with your application image name, please use lowercase letters, numbers and hyphens -->

## Description
<!-- Replace here with a description of the image/application, the utilities, the tools or features included. -->
This is a tool to do something a dataset...

## Usage
<!-- Replace here with the parameters accepted, those which the user can put after the "--" in the `jobman submit` command 
     (they will be appended to the `ENTRYPOINT` of your image). -->

`jobman submit -i my-application -- <INPUT_DIR> <OUTPUT_DIR>`
  
The application accepts 2 parameters:
 - The input path of a DICOM directory
 - The output directory where harmonized image will be saved.
 
Example:  
  ```
    jobman submit -i my-application -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ ~/persistent-home/results/
  ```
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job.

<!-- It is recommended to add a usage example, as you can see. 
     For that usage examples take into account that...
      - In the arguments where the user set the path for **image inputs** you should use the path of a dataset (`/home/chaimeleon/datasets/<dataset-id>` or just `~/datasets/<dataset-id>`).  
      - In the arguments where the user set the path for **output results**, you should use a directory within the persistent home (`/home/chaimeleon/persistent-home/results`or just `~/persistent-home/results`).  
-->

## Authors
James Gordon   <!-- You can put here your name, nick and/or your organization -->

## Contact info
<!-- Replace here with an email address or publicly accessible contact form to allow the user report issues or request missing documentation required for usage. -->
james@email.com
https://github.com/chaimeleon-eu/workstation-images/issues

## License
https://github.com/chaimeleon-eu/workstation-images/blob/main/LICENSE  <!-- You should put here a link to the public license document of your application (if any). -->

<!-- If it is a custom license and the repository is private you can copy the license text. 
     Otherwise you shouldn't do it, just put the link to not make this text too long (it will be included as output of `jobman image-details`). -->

## URL
<!-- Replace here with the link to the public or private repository where you put the Dockerfile and all the dependecies available for us to build the image. -->
Public dockerfile repository:
https://github.com/chaimeleon-eu/workstation-images/tree/main/ubuntu-python


