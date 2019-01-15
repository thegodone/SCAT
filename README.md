# SCAT: encoding robust representation for graph generation

This work proposes a graph generation model that uses a recent adaptation of Mallat’s scattering transform to graphs. The proposed model is naturally composed of an encoder and a decoder. The encoder is a Gaussianized graph scattering transform, which is robust to signal and graph manipulation. The decoder is a simple fully connected network that is adapted to specific tasks, such as link prediction, signal generation on graphs and full graph and signal generation.

## Getting Started

This repository demonstates the implementation of the experiments described in [1]. The codes can be used for implementing the following models:
- Link prediction (SCAT-S, SCAT-D)
```
python trainCora.py -s S [S/D] -d cora [cora/citeseer/pubmed]
```
- Signal generation on graph (SCAT-SW, SCAT-DW, SCAT-SN, SCAT-DN)
```
python trainFashion.py -s S [S/D] -g W [W/N]
```
- Graph and signal generation (SCAT-SW, SCAT-DW, SCAT-SN, SCAT-DN)
```
python -W ignore trainFashion.py -s S [S/D] -g W [W/N]
```

The graph scattering functions in [scat.py](scat.py) have wider uses. We encourage using them in variant graph tasks, e.g. [2].

### Prerequisites

* Python >= 3.6
* Tensorflow >= 1.2.0
* RDKit
* networkx
* scipy, numpy, scikit-learn

## Citation
```
[1] Zou, D., & Lerman, G. (2019). Encoding Robust Representation for Graph Generation. Submitted to The International Joint Conference on Neural Networks (IJCNN) 2019.
[2] Zou, D., & Lerman, G. (2018). Graph Convolutional Neural Networks via Scattering. arXiv preprint arXiv:1804.00099.
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

We borrowed data and codes from various repositories we cited in [1].
