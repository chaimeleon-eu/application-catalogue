# privacypreserver

## Description
A data synthesizer and a privacy analyzer of tabular data.

## Usage
Copy the dataset.csv file and metadata.json file to a new working directory. And then test the synthesis performance with

**for synthesis**
`jobman submit -i privacypreserver -- --target synthesis --data_dir ~/persistent-home/privacypreserver/data.csv`

**for analysis**
`jobman submit -i privacypreserver -- --target analysis -s ~/persistent-home/privacypreserver/tvae.csv --metric ml_efficency --meta_dir ~/persistent-home/privacypreserver/metadata.json`

## Authors
Imperial

## Contact info
https://github.com/chaimeleon-eu/image_batch_non-imaging-aug/issues

## URL
Public dockerfile repository:
https://github.com/chaimeleon-eu/image_batch_non-imaging-aug/tree/ca857a3e5e1f94c2da146cab35d4caa75dad4333 

## License
https://github.com/chaimeleon-eu/image_batch_non-imaging-aug/tree/ca857a3e5e1f94c2da146cab35d4caa75dad4333?tab=readme-ov-file#license
