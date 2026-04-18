# UNCC-Applied-Machine_Learning
UNCC Spring 2026 ITCS-5154-051 Applied Machine Learning

## To set up environment to run code in this repository
conda env create -f mena_environment_test.yml

## Steps to set up and run code from Mena paper
Run notebook "get_cropharvest_data.ipynb"
python data_creation.py -d data -c kenya -o selected_data
python train_multiview.py -s config/project_config_MV.yaml
python evaluate_predictions.py -s config/evaluation_MV.yaml
python train_singleview.py -s config/project_config_SV.yaml
python evaluate_predictions.py -s config/evaluation_SV.yaml
