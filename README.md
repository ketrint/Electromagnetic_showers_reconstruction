## Reconstruction of 3D Shower Structures for Neutrino Experiments

#### Authors: [V. Belavin] (vbelavin@hse.ru), [E. Trofimova] (etrofimova@hse.ru), [A. Ustyuzhanin] (austyuzhanin@hse.ru)

### Overview

This directory contains code necessary to run the Electromagnetic Showers (EM) Reconstruction algorithm that is devided into the following parts:
1) Graph Construction;
2) Edge Classification;
3) Showers Clusterization;
4) Parameters Reconstruction.

#### Experimental Data

X, Y, Z coordinates and the direction of the EM Showers base-tracks. 

The showers are generated using FairShip framework. 

Data for graph generation is located here: https://gitlab.com/SchattenGenie/shower_generation/blob/master/data/mcdata_taue2.root

#### Results

The algorithm detects ~ 86% of Showers and assess the coordinates and direction of base-tracks with ~ 75% accuracy.

Clusters Examples:
![Clusters Examples](./docs/Clusters_Example.png)

### Running the code

training_classifier.py predicts the probability of edge to connect vertices of one shower. The probability will be then used as edge weight for proposed clusterization algorithm in clustering.py.
