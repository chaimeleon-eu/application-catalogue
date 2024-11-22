# analytic-engine

## Description
Application to assist in the selection of Artificial Intelligence (AI) training / testing datasets.  
It allows the user to do statistics analysis and establish correlations between the different data variables of datasets.

All those services will be deployed:
* **trino-plugin** (aka trino): special instance of trino which offers an SQL access to the Chaimeleon datasets.
* **ai-layer-microservice** (aka ws): web Service to requests analytical jobs and retrieve results.
* **db**: postgres instance for the ws, where requests and their relative information is persist.
* **queue**: Queue to analytical jobs requests (a rabbitmq container which exchange messages, analytical requests, from ws to worker.
* **mongo**: nosql database for query and result management.
* **ai-layer-worker** (aka worker): analytical jobs worker.
* **ai-layer-frontend**: analytical engine's frontend.

## Usage
https://github.com/chaimeleon-eu/workstation-images/blob/main/usage-guide.md#workstation-usage-guide

Read carefully the "Installation Notes" after deploy because there are important points about usage.

## Authors
Bahia Software

## Contact info
??

## URL
Private\* helm chart:
https://github.com/chaimeleon-eu/helm-chart-analytical-engine

Private\* dockerfile repository:
https://github.com/chaimeleon-eu/analytical-engine

\* You will see error 404 if you don't have permissions to access.

## License
None
