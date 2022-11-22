Instructions for using the checkpoint for inference:

Basic Setup (One time activity)

1. Clone the DYGIE++ repository from: https://github.com/dwadden/dygiepp. This repositiory is managed by Wadden et al., authors of the paper Entity, Relation, and Event Extraction with Contextualized Span Representations (https://www.aclweb.org/anthology/D19-1585.pdf).

git clone https://github.com/dwadden/dygiepp.git

2. Navigate to the root of repo in your system and use the following commands to setup the conda environment:

conda create --name dygiepp python=3.7
pip install -r requirements.txt
conda develop .   # Adds DyGIE to your PYTHONPATH

Running Inference on Radiology Reports

3. Activate the conda environment: 

conda activate dygiepp

3. Copy the inference.py file to the root of the cloned repo where you have the dygie folder

4. Run the inference.py file using the command:

python3 inference.py --model_path <path to file in model_checkpoint ending in tar.gz> --data_path <path to folder with reports> --out_path <path to file where to save result ending in .json> --cuda_device <optional id>
