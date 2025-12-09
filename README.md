# MPRM_achaemenid
Multi-factor, Probabilistic Route Modelling (MPRM) algorithm to generate cost surfaces for use in least-cost analysis. 
Adapted for modelling the Achaemenid Royal Road across the Achaemenid Empire (c. 550-330 BC).

Based on the original code and paper:
> Petrie, Cameron A., Friederike K. Jürcke, Toby C. Wilkinson, Hector A. Orengo (submitted). *Over the hills and far 
> away: modelling mobility and connectivity across the Iranian Plateau in late prehistory (c. 10,000-2000 BC) using 
> multi-factor probabilistic corridors*. 
> submitted to Journal of Archaeological Research
> 

> 
> Original code repository: https://github.com/fjuercke/2025_MPRM_Petrie_etal_JAR

## Contents

This repository contains:

- [MPRM_costsurface](MPRM_costsurface): JavaScript code for implementation in Google Earth Engine (GEE).
- [reservoir_instructions](reservoir_instructions): Instructions for loading the reservoir data into your GEE assets.

## How to run the code in your browser

The code has been developed for implementation in Google Earth Engine's (c) JavaScript API 
by H.A. Orengo, T.C. Wilkinson and F.K. Jürcke. The changes made to the original code to adapt it for modellling the
Achaemenid Royal Road have been made by F.K. Jürcke with input from D. Salaris.

The changes include:
- use of a critical slope formula to account for wheeled vehicle movement

To run the code: 
1) Ingest the reservoir data into your GEE assets. Please see the [instructions](reservoir_instructions).
2) Copy the code contained in file [MPRM_costsurface](/code/MPRM_costsurface) into the Google Earth Engine code editor.
3) Adjust line 190 in the code, which calls the reservoir data, to where the reservoir data is in your asset manager. 
4) Press 'Run'. 

All further instructions are contained in the JavaScript Code. 

The code presented here is an iteration of the MPRM model. A version of the algorithm that integrates additional 
factors and convolutions of those factors is under further development, and will be presented 
in a separate paper where the additional parameters are used to consider movement across longer 
distances and different environments and landscapes (Orengo et al. n.d.). The repository can be found here:

https://github.com/horengo/Multitemporal-and-multifactor-probailistic-corridor-networks