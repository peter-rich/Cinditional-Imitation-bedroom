# Conditional object to the scene.
## Zhanfu Yang

## Dataset:
### Visual Genome
Run the following script to download and unpack the relevant parts of the Visual Genome dataset:

`bash scripts/download_vg.sh`

After downloading the Visual Genome dataset, we need to preprocess it. This will split the data into train / val / test splits, consolidate all scene graphs into HDF5 files, and apply several heuristics to clean the data. In particular we ignore images that are too small, and only consider object and attribute categories that appear some number of times in the training set; we also igmore objects that are too small, and set minimum and maximum values on the number of objects and relationships that appear per image.

`python scripts/preprocess_vg.py`
### Train:
`bash run.sh`

## Cinditional-Imitation-bedroom
