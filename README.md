# A Method for Fine-Grained Aircraft Recognition Base on Web-Supervised Network

Introduction
------------
This is the source code for our paper **A Method for Fine-Grained Aircraft Recognition Base on Web-Supervised Network**

Installation
------------
After creating a virtual environment of python 3.7, run `pip install -r requirements.txt` to install all dependencies

How to use
------------
The code is currently tested only on GPU
* **Data Preparation**
    - Download data into project root directory and uncompress them using
        ```
        wget https://wsnfg-sh.oss-cn-shanghai.aliyuncs.com/web-aircraft.tar.gz
        tar -xvf web-aircraft.tar.gz
        ```

* **Source Code**

    - If you want to train the whole network from begining using source code on the web fine-grained dataset, please follow subsequent steps
    
      - Choose a dataset, create soft link to dataset by
       ```
       ln -s web-aircraft aircraft
       ```  
      - Modify `CUDA_VISIBLE_DEVICES` to proper cuda device id in  ``` run_train_resnet.sh```
      - Modify `data` to the dataset you want to use in  ``` run_train_resnet.sh```
      
      - Activate virtual environment(e.g. conda) and then run the script
       ```
       bash run_train_resnet.sh
       ```
    - We recommend you use Resnet-50 model, because it has better performance.  


