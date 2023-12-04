# Automatically Generated Exploded View Animations in VR: A Deep Learning Approach

<!---Official PyTorch implementation of "AssemblyNet: A Point Cloud Dataset and Benchmark for Predicting Part Directions in an Exploded Layout," accepted at WACV 2024.

AssemblyNet is a novel point cloud dataset for the prediction of part directions used in the automatic generation of exploded view animations. We benchmarked the dataset on four well-known point cloud based methods as well as two novel methods using a two-path approach with two different backbones.-->

For further information, please contact [Jesper Gaarsdal](mailto:gaarsdal.jesper@gmail.com).

<!---<img src='./figures/task-overview.png' width=800>-->

## Abstract
Exploded view animations are widely used in the understanding of complex mechanical assemblies in fields such as manufacturing, education, and engineering. Even today, the creation of these animations is largely a manual process that demands extensive expertise. In this paper, we introduce a novel tool for creating exploded view animations within a virtual reality (VR) environment, offering an automated human-in-the-loop process allowing users to adjust and refine the final animation. Our approach combines the principles of traditional assembly-by-disassembly with modern machine learning techniques to predict the order and direction of part disassembly, thereby automating the generation of exploded layouts. The core of our methodology is a novel point cloud classification network, PointDAN, for predicting the disassembly sequence of parts from 3D assemblies. Another key contribution of this work is the development of a public point cloud dataset, facilitating the training of models to predict whether a part can be disassembled from its assembly. We report the performance of our trained networks, along with the performance of the full assembly-by-disassembly process by evaluating the final animations and comparing the results with a previous method. Furthermore, we report on an expert user study including participants spanning various industries. This study demonstrates the industrial applicability and potential of the animation tool. Our findings show that the integration of assembly-by-disassembly and machine learning not only streamlines and simplifies the automatic creation of exploded layouts but also has the potential to create highly accurate animations. Implementing the tool and generating the animations within VR opens up new opportunities for interactive and immersive visualization, paving the way for innovative educational and engineering applications. To further support research and development in this domain, a project page containing the dataset and code will be made available upon acceptance of the manuscript.

## Dataset

<!---The AssemblyNet dataset contains both 512-point and 1024-point point clouds of mixed industrial assemblies and LEGO models.
It includes annotations for both classification and regression of 5420 samples. Each sample consists of two point clouds in separate files, one of the specific part and one of its subassembly.
The classification uses 26 categories representing 26 world space directions, while regression uses the world space direction as X, Y, and Z values.

The dataset is published on Zenodo: [https://doi.org/10.5281/zenodo.10069220](https://doi.org/10.5281/zenodo.10069220)-->

### Benchmarked Model Architectures

<!---The four state-of-the-art models used in our benchmarks are:

* [DGCNN](https://liuziwei7.github.io/projects/DGCNN)
* [PointNet](https://stanford.edu/~rqi/pointnet/)
* [PointNet++](https://stanford.edu/~rqi/pointnet2/)
* [SimpleView](https://github.com/princeton-vl/SimpleView)

We also designed and tested a novel two-path approach, using either DGCNN or PointNet++ as the backbone:

* [2P-DGCNN](./models/2p-dgcnn.py)
* [2P-PointNet2](./models/2p-pointnet2.py)-->

## Requirements

<!---Requirements can be found in the [requirements.txt file](./requirements.txt).-->

## Citation
<!---If you find this dataset and our work useful for your research, please consider citing the paper:

	@InProceedings{Gaarsdal2024AssemblyNet,
	  title={AssemblyNet: A Point Cloud Dataset and Benchmark for Predicting Part Directions in an Exploded Layout},
	  author={Gaarsdal, Jesper and Haurum, Joakim Bruslund and Wolff, Sune and Madsen, Claus Brøndgaard},
	  booktitle={Proceedings of the IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
	  month={January},
      year={2024}
	}-->

## License
[MIT License](./LICENSE).