# CHAIMELEON Application Catalogue

This is the catalogue of available applications in CHAIMELEON platform.

There are two types of applications:
 - Batch applications (non-interactive) launched as k8s batch jobs.  
   If you still don't know how to launch one of these, see [here](https://github.com/chaimeleon-eu/workstation-images/blob/main/usage-guide.md#jobman-client-tool).
 - Interactive applications launched as k8s deployments/services.  
   If you still don't know how to launch one of these, see [here](https://github.com/chaimeleon-eu/workstation-images/blob/main/usage-guide.md#workstation-usage-guide).


## Batch applications
The user can launch batch jobs from any desktop in the platform.
The available docker images with applications to launch are listed with the command `jobman images` in your desktop.

| Image name (link to description)                                                               | Author                         | Dockerfile  |
|:-----------------------------------------------------------------------------------------------|:-------------------------------|:------------|
| [ubuntu-python](batch-applications/ubuntu-python/README.md)                                    | UPV                            | Public      |
| [ubuntu-python-tensorflow](batch-applications/ubuntu-python-tensorflow/README.md)              | UPV                            | Public      |
| [ubuntu-python-pytorch](batch-applications/ubuntu-python-pytorch/README.md)                    | UPV                            | Public      |
| [mri_harmonization](batch-applications/mri_harmonization/README.md)                            | Quibim                         | Private     |
| [Deepfakes Detector](https://github.com/chaimeleon-eu/image_batch_deepfakesdetector) (private repository) from BGU
| [Lung CT Harmonisation](https://github.com/chaimeleon-eu/image_batch_lungCT_harmonisation) (private repository) from Imperial
| [Non-imaging Data Augmentation](https://github.com/chaimeleon-eu/image_batch_non-imaging-aug) from Imperial
| [SHAP Explainability Radiomics](https://github.com/chaimeleon-eu/image_batch_shap_explainability_radiomics) from University of Maastricht

### Testing
| Image name (link to description)                                                               | Author                         | Dockerfile  |
|:-----------------------------------------------------------------------------------------------|:-------------------------------|:------------|
| [dicom-file-integrity-checker](batch-applications/dicom-file-integrity-checker/README.md)      | IIS La Fe                      | Private     |
| [trace4harmonization](batch-applications/trace4harmonization/README.md)                        | DeepTrace Technologies         | Public      |
| [t2w-prostate-segmentation-tool](batch-applications/t2w-prostate-segmentation-tool/README.md)  | Quibim                         | Private     |
| [mammography-density-segmenter](batch-applications/mammography-density-segmenter/README.md)    | ITI                            | Private     |



## Interactive applications
These applications appear in the catalog of applications to deploy.

| Helm chart name (link to description)                  | Author               | Dockerfile, helm chart |
|:-------------------------------------------------------|:---------------------|:-----------------------|
| [desktop-tensorflow](desktop-tensorflow/README.md)     | UPV                  | Public                 |
| [jupyter-tensorflow](jupyter-tensorflow/README.md)     | UPV                  | Public                 |
| [desktop-pytorch](desktop-pytorch/README.md)           | UPV                  | Public                 |
| [jupyter-pytorch](jupyter-pytorch/README.md)           | UPV                  | Public                 |
| [chaimeleon-superset](chaimeleon-superset/README.md)   | Bahia Software       | Public                 |(https://github.com/chaimeleon-eu/helm-chart-superset)
| [analytic-engine](analytic-engine/README.md)           | Bahia Software       | Private                |(https://github.com/chaimeleon-eu/analytical-engine)


## Request to add or update an application
For new applications please read the 
[developer guide](https://github.com/chaimeleon-eu/workstation-images/tree/main?tab=readme-ov-file#how-to-integrate-your-application-in-chaimeleon-platform).

To request the addition or update of an application choose one of the following ways:
 - Open an issue by selecting one of the provided categories from the [issue page](https://github.com/chaimeleon-eu/application-catalogue/issues/new/choose) 
   and fill in the requested information.
 - [Fork](https://github.com/chaimeleon-eu/application-catalogue/fork) this repository,  
   add a new subdirectory in `batch-applications` or in `interactive-applications` with the name of the image for your application,  
   add a `README.md` file (use the [template](.github/ISSUE_TEMPLATE/01_add-new-application.md) or simply take it from other application as an example) 
   and submit a pull request with your addition. 

