## Webcam and Jupyter notebook demo

This folder contains a simple webcam demo where you can perform real-time SGG. First, make sure that you have downloaded or trained a model in SGDet mode, currently only sgdet is supported for demo. 
To run the demo you'll need to:

1. Install the codebase, refer to [INSTALL.md](../INSTALL.md)
2. Train a SGDet model and save the results files in the ```./checkpoints/``` folder
3. Get the path to the config file used for training, for instance `./configs/VG150/baseline/e2e_relation_X_101_32_8_FPN_1x.yaml`
4. Get the path of the dict file with class names, it should be under ```./datasets/vg/``` and be named something like ```VG-SGG-dicts.json```
5. Get the path of your trained weights, for instance `./checkpoints/upload_causal_motif_sgdet/model_0028000.pth`

You can run the demo as follows:

```
conda activate scene_graph_benchmark
python webcam_demo.py --classes PATH_TO_CLASSES_DICT_FILE.json --config YOUR_CONFIG_FILE_HERE.yml --weights YOUR_WEIGHTS_FILE.pth
```