# UOVH-Hackathon-Prototype

This repo contains the prototype of the application with which my team (FarAhead) joined the **University Open Virtual Hackathon 2020** of West Malysia.
It's a simple ML application which is a proposed a solution to the presented problem statement which was the absence of product traceability in the largest manufacturer of rubber gloves which is a Malaysian company. The solution is a basic visual inspection tool where gloves on production lines are classified into good gloves and defective ones, this is using a pretrained MobileNet SSD model that we trained using Tensorflow object detection API and the converted to Intel OpenVino format and using a custom dataset of 2 classes  which are normal gloves and defective ones (The dataset can be found in another repo linked in the colab notebook along with helper scripts and instructions from the original blog post I used to apply this)
The rules of the hackathon implied that we use Intel OpenVino toolkit for the inference process and we have used their API and built a very simple GUI around it. We ended up came out as a finalist in the Hackathon and brought back a consolation 
Prize. 

The repo consists of: 
1-the gloves detection and classification model we trained in `gloves_model/` 
2- The python script which is a modified version of one of the demos that Intel OpenVino toolkit provides which is basically the Inference Engine  API along with added simple GUI in `obj_detection_demo_ssd_async.py` 
3- The Jupyter notebook which should run on Google Colab which you can use to produce a Tensorflow custom object detection model that can be then used by OpenVino model optimizer to get the .xml and .bin files in `Tensorflow_Custom_Object_Detection.ipynb`

To run the python script, you need to have Intel OpenVino toolkit installed and then move the .py file into the clone this repo in the `C:\Program Files (x86)\IntelSWTools\openvino_2020.4.287\deployment_tools\open_model_zoo\demos\python_demos` directory and the cd into the folder and run `python obj_detection_demo_ssd_async.py`
