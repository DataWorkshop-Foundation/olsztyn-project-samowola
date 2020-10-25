
<p align="center">
<a href="https://raw.githubusercontent.com/DataWorkshop-Foundation/olsztyn-project-samowola/main/about/project_workflow_pl.pdf">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/samowola_workflow.png" width="90%">
</a>
</p>

## Project tasks

<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/nr_1.png" width="50px">

**[Gathering and pre-processing of data.](https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/blob/main/about/notebooks/1_gathering_data.ipynb)**

* We have developed an original - and more importantly, automated - method of acquisition and preparation of training data. 
* Using publicly available resources, we have collected
[RGB photos](https://www.geoportal.gov.pl/dane/ortofotomapa) for over 50,000 locations.
* Using the [Land and Buildings Register](https://pl.wikipedia.org/wiki/Ewidencja_grunt%C3%B3w_i_budynk%C3%B3w) and 
some image transformations, a binary mask was prepared for each location, delineating the area of all registered buildings.  
    
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/nr_2.png" width="50px">

**[Development of a building segmentation model.](https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/blob/main/about/notebooks/2_building_unet_model.ipynb)** 

* We conducted a series of experiments, during which we checked approx. 30 architectures, parameters and variants of 
deep neural network training.
* We validated all models, which allowed us to choose the best - convolutional encoder-decoder 
([U-NET](https://en.wikipedia.org/wiki/U-Net)) model, with the [F1](https://en.wikipedia.org/wiki/F1_score) measure 
result over 0.78.
 
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/nr_3.png" width="50px">

**Preparation of the model API and the demo version of the system.**

* The final model was compressed using 
[Tensorflow Lite](https://www.tensorflow.org/lite/convert), which allowed to reduce the amount of memory needed for 
prediction by 1/3.
* A sample of the possibilities along with the visualization of the results is presented by a simple demo-application 
prepared with the use of [Plotly](https://plotly.com/) and [Dash](https://plotly.com/dash/) libraries.

**Importantly, only free tools and data sources were used in the process of creating the project.**

## Examples

Below, we present some examples of our model predictions - both those we are proud of and other that we still have to 
work on. ;)

<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_001.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_002.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_003.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_004.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_005.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_006.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_007.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_008.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_009.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_010.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_011.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_012.png">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/example_plots/example_013.png">

