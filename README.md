<p align="center">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/samowola_logo.png" width="300">
</p>

## About the project

A building permit is one of the first steps to be taken when deciding to erect a building. 
This is a formality that everyone must go through. Despite severe penalties, many people decide to erect the building 
without permission.

Let's see what the statistics say.

<p align="center">
<img src="https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/raw/main/img/legalisations.png" width="300">
</p>

_Source: Main Construction Supervision Office_ [[1]](http://www.gunb.gov.pl/)

Are these numbers impressive? Let's take a closer look at the problem.

In 2011, aerial photos were taken in Gliwice (Poland), with the help of which the legal analysis of the buildings was 
conducted. The results are shocking - 1374 discrepancies were detected, of which 454 were removed and 473 objects were 
modified [2]. The lowest cost of legalizing a building is PLN 2,500, so the profit for the commune from the regulation 
of discrepancies is huge. If we subtract the modifications and removed objects and take into account the lowest cost of 
legalization, it can be quickly recalculated that PLN 1,117,500 was received in the budget of Gliwice. If we calculate 
it according to the price list from 2017 [3], then for this amount it is possible to build a pavement with a length of 
about 4.5 km.

The results of this project clearly show that the number of abnormalities detected and the official data are only a 
fraction of the reality. The main reason for this is the high cost of aerial / satellite imagery and manual image 
analysis. Technical limitations and the lack of digital competences of officials additionally make it difficult to 
supervise the legality of construction sites and system errors.

This is where our Detector comes in.

## Solution

The process of detecting inconsistencies is automated through machine learning. The input data is the Land and Building 
Registry, orthophotomap images or satellite photos. The algorithm uses a trained model of neural networks to indicate 
(segment) building objects, verifies their existence in the official database, and then marks any deviations with the 
given parameters.

[Want to find out about the details of the illegal building detection process?](https://github.com/DataWorkshop-Foundation/olsztyn-project-samowola/blob/main/results.md)


## Disclaimer 

Machine learning (ML) algorithms are a great solution and can replace us in many tedious and boring jobs. 
However, they are not free from imperfections. It is similar with the algorithm used here. 
For this reason, it can be seen, for example, that the model does not detect all buildings or occasionally indicates a 
building, though it wasn't there at all. Although we are constantly trying to improve the quality of the ML model, 
we will never be able to guarantee 100% effectiveness.

It is worth noting that not all discrepancies between the records and the actual state mean breaking the law. They may 
be due to administrative negligence, but should nevertheless be clarified.
