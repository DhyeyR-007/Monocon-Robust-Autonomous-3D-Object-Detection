# Monocon_NA565

THis is out final project submission for ROB 535: Self-Driving cars




**Setup**

# [Step 1]: Create new conda environment and activate.
#           Set [ENV_NAME] freely to any name you want. (Please exclude the brackets.)
conda create --name [ENV_NAME] python=3.8
conda activate [ENV_NAME]

# [Step 2]: Clone this repository and change directory.
git clone https://github.com/2gunsu/monocon-pytorch
cd monocon-pytorch

# [Step 3]: See https://pytorch.org/get-started/locally/ and install pytorch for your environment.
#           We have tested on version 1.11.0.
#           It is recommended to install version 1.7.0 or higher.

# [Step 4]: Install some packages using 'requirements.txt' in the repository.
#           The version of numpy must be 1.22.4.
pip install -r requirements.txt

# [Step 5]
conda install cudatoolkit



**Train, Eval, and Test **(Training, evaluation and testing are to be followed according to this repository "https://github.com/minghanz/monocon_na565") <br />
cd monocon_na565 <br />
python train.py <br />

python test.py  --config_file       [FILL]      # Config file (.yaml file)
                --checkpoint_file   [FILL]      # Checkpoint file (.pth file)
                --gpu_id            [Optional]  # Index of GPU to use for testing (Default: 0)
                --evaluate                      # Perform evaluation (Quantitative Results)
<br />
python test.py  --config_file       [FILL]      # Config file (.yaml file)
                --checkpoint_file   [FILL]      # Checkpoint file (.pth file)
                --visualize                     # Perform visualization (Qualitative Results)
                --gpu_id            [Optional]  # Index of GPU to use for testing (Default: 0)
                --save_dir          [FILL]      # Path where visualization results will be saved to



**Monocon_NA565**
├── DevKit
│   ├── ExamplePrediction.txt
│   ├── FinalData
│   │   ├── Test
│   │   ├── Train
│   │   └── Val
│   ├── ImageSets
│   │   ├── test.txt
│   │   ├── train.txt
│   │   ├── trainval.txt
│   │   └── val.txt
│   ├── merger.py
│   ├── readme.txt
│   ├── ToKITTITest.ipynb
│   └── ToKITTITrain.ipynb
├── monocon_na565
│   ├── CFG_OUTPUT_DIR
│   │   ├── checkpoints
│   │   │   └── epoch_171.pth
│   │   ├── config.yaml
│   │   └── tf_logs
│   │       ├── events.out.tfevents.1702246751.ROB-IGMR-ETUDEU.12728.0
│   │       └── events.out.tfevents.1702246979.ROB-IGMR-ETUDEU.13754.0
│   ├── config
│   │   └── monocon_configs.py
│   ├── dataset
│   │   ├── base_dataset.py
│   │   ├── ImageSets_final_prj
│   │   │   ├── test.txt
│   │   │   ├── train.txt
│   │   │   ├── trainval.txt
│   │   │   └── val.txt
│   │   ├── kitti_raw_dataset.py
│   │   ├── monocon_dataset.py
│   │   ├── testing
│   │   │   ├── calib
│   │   │   └── image_2
│   │   └── training
│   │       ├── calib
│   │       ├── image_2
│   │       └── label_2
│   ├── engine
│   │   ├── base_engine.py
│   │   ├── kitti_eval
│   │   │   ├── eval.py
│   │   │   ├── __init__.py
│   │   │   ├── __pycache__
│   │   │   │   ├── eval.cpython-311.pyc
│   │   │   │   ├── __init__.cpython-311.pyc
│   │   │   │   └── rotate_iou.cpython-311.pyc
│   │   │   └── rotate_iou.py
│   │   ├── monocon_engine.py
│   │   └── __pycache__
│   │       ├── base_engine.cpython-311.pyc
│   │       └── monocon_engine.cpython-311.pyc
│   ├── losses
│   │   ├── cross_entropy_loss.py
│   │   ├── depth_loss.py
│   │   ├── dim_loss.py
│   │   ├── focal_loss.py
│   │   ├── __init__.py
│   │   ├── l1_loss.py
│   │   └── utils.py
│   ├── model
│   │   ├── backbone
│   │   │   ├── dla_neck.py
│   │   │   ├── dla.py
│   │   │   ├── __init__.py
│   │   │   └── __pycache__
│   │   │       ├── dla.cpython-311.pyc
│   │   │       ├── dla_neck.cpython-311.pyc
│   │   │       └── __init__.cpython-311.pyc
│   │   ├── dense_heads
│   │   │   ├── __init__.py
│   │   │   ├── monocon_heads.py
│   │   │   └── __pycache__
│   │   │       ├── __init__.cpython-311.pyc
│   │   │       └── monocon_heads.cpython-311.pyc
│   │   ├── detector
│   │   │   ├── __init__.py
│   │   │   ├── monocon_detector.py
│   │   │   └── __pycache__
│   │   │       ├── __init__.cpython-311.pyc
│   │   │       └── monocon_detector.cpython-311.pyc
│   │   ├── __init__.py
│   │   ├── norm
│   │   │   ├── attentive_norm.py
│   │   │   ├── __init__.py
│   │   │   └── __pycache__
│   │   │       ├── attentive_norm.cpython-311.pyc
│   │   │       └── __init__.cpython-311.pyc
│   │   └── __pycache__
│   │       └── __init__.cpython-311.pyc
│   ├── solver
│   │   ├── cyclic_scheduler.py
│   │   └── __init__.py
│   ├── test.py
│   ├── test_raw.py
│   ├── train.py
│   ├── transforms
│   │   ├── base_transforms.py
│   │   ├── default_transforms.py
│   │   ├── geo_aware_transforms.py
│   │   └── __init__.py
│   └── utils
│       ├── data_classes.py
│       ├── decorators.py
│       ├── engine_utils.py
│       ├── geometry_ops.py
│       ├── kitti_convert_utils.py
│       ├── target_generator.py
│       ├── tensor_ops.py
│       └── visualizer.py
├── navarch565
│   └── CFG_OUTPUT_DIR
│       ├── config.yaml
│       └── tf_logs
├── output_dir
│   ├── checkpoints
│   ├── config.yaml
│   └── tf_logs
│       └── events.out.tfevents.1702246335.ROB-IGMR-ETUDEU.9852.0
├── pretrained-20231210T223435Z-001
│   └── pretrained
│       ├── best.pth
│       └── config.yaml
└── test.html

