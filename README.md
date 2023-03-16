## Sentinel-data-download
This repository is dedicated to download sentinel data using API.

## The repository includes:
1. download_sentineldata.ipynb
2. requirements.txt

## Setting-up a virtual environment
1. Create a virtual conda environment using 'conda create -n LPL'.
2. Activate the virtual environment using 'conda activate LPL'.
3. Install all the dependencies using requirements.txt 'pip install -r requirements.txt'.

- main.py: This script is use to create the weekly folder inside the SAR folder and copy/create the AOI geojson inside it based on the user input and after that all the scripts in the GIS folder will be called one by one via providing the relevant input variables to run each script.
    - The sequence of ruuning the script is:
            1. data_acquisition.py
            2. data_preprocessing.py
            (Note: the inference script will be running after data_preprocessing.py)
            3. AIS_extract.py
            (Note: the ais data will be aquired manually after AIS_extract.py)
            4. post_processing.py
    
    - Script requirements other than relevant libraries
    - The inputs for this script:
        1. Define all the relevent folders name which will be used to call/store the data while executing the script
        2. Define parameters for calling the main function defined inside the main.py script
            * test
