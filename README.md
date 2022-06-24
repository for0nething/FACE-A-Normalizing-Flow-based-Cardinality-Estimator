# FACE
This is a pytorch implementation for the VLDB 2022 paper [FACE: A Normalizing Flow based Cardinality Estimator](http://www.vldb.org/pvldb/vol15/p72-li.pdf) [[**Citation**]](#citation)


<p align="center">
    <br>
    <img src="framework.png" width="450"/>
<p>

# Quick Start



## Folder Structure

    .
    ├── torchquadMy     # Modified pytorch implementation of adaptive importance sampling
    ├── utils           # A wrapper for datasets used to generate query, oracle results, etc.
    ├── data            # A directory for storing data. Downloaded data can be stored here
    ├── train           # Codes for training normalizing flow models
    ├── evaluate        # Evaluate trained models on real-world datasets for cardinality estimation
    ├── environment.yml # Used to build conda environment
    └── README.md               

The normalizing flow models are built based on [nflows](https://pypi.org/project/nflows/). 
The adaptive importance sampling codes are modified from [torchquad](https://github.com/esa/torchquad).


## Quick Start
The real-world datasets can be downloaded from [dataset link](https://cloud.tsinghua.edu.cn/d/96132c6b279e4097baaa/).
- **Step 1:** Build conda environment with `conda env create -f environment.yml`
- **Step 2:** Switch to the installed environment by `conda activate testenv`
- **Step 3:** Install modified torchquad by `cd ./torchquadMy`, and then `pip install .`
- **Step 4:** After properly setting the paths of datasets, models, etc, 
you can use the notebook files under `train` and `evaluate` directories to conduct experiments.


## Usage




**Notes:** 
- Before running the codes, make sure the path variables in the codes are set properly. 
We have added some comments to hint before some path variables, but may not have covered all of them.
- Current codes may be incompatible with machines that do not have GPUs.
- 

## License

The project is available under the [MIT](LICENSE) license.



## Citation
If our work is helpful to you, please cite our paper:
```bibtex
@article{DBLP:journals/pvldb/WangCLL21,
  author    = {Jiayi Wang and
               Chengliang Chai and
               Jiabin Liu and
               Guoliang Li},
  title     = {{FACE:} {A} Normalizing Flow based Cardinality Estimator},
  journal   = {Proc. {VLDB} Endow.},
  volume    = {15},
  number    = {1},
  pages     = {72--84},
  year      = {2021},
  url       = {http://www.vldb.org/pvldb/vol15/p72-li.pdf},
  doi       = {10.14778/3485450.3485458},
  timestamp = {Thu, 21 Apr 2022 17:09:21 +0200},
  biburl    = {https://dblp.org/rec/journals/pvldb/WangCLL21.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```