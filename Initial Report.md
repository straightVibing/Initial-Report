---
Title: "Initial Report"
subtitle: "Fred Barrett"
geometry:

- top = 20mm
- left = 20mm
- right = 20mm
documentclass: article

bibliography: Dissertation_References.bib

fontsize: 12pt
header-includes: |
        \usepackage{float}
        \floatstyle{ruled}
        \newfloat{eq}{thp}{lop}
        \floatname{eq}{Equation}
        \restylefloat{eq}
        \renewcommand{\sfdefault}{ua1}
        \renewcommand{\familydefault}{\sfdefault}
        \usepackage{float}
        \floatstyle{plain}
        \newfloat{eq}{thp}{lop}
        \floatname{eq}{Equation}
        \restylefloat{eq}
        \usepackage{graphicx}
        \usepackage{fancyhdr}
        \pagestyle{fancy}
        \fancyhead[L]{Initial Report}
        \fancyhead[R]{Fred Barrett}
        \usepackage{hyperref}
        \usepackage{amsmath}
        \usepackage{wrapfig}
        \usepackage{lipsum}
        \usepackage{blindtext}
        \usepackage{pdfpages}
---

\includepdf[pages=-,scale=1.1]{CoverPage.pdf}

\tableofcontents

# Abstract 

- May not be necessary
- A summary of the initial report 

# Introduction

- Wastewater in the UK
- How bad is it and evidence
- Establish clear problem
- Bring up MFCs
- Description and discussion of major design parameters
    - Mention key ones here: biofilm thickness, flow rate, temperature, architecture, COD, 
    - When mention these very be brief so that you can then expand in the background and literature review
    - A table could be a coherent way show them
- Get/make a diagram to illustrate how the key component
    - Draw.io or similar should be fine
    - REMEMBER TO MENTION THAT THE MEMBRANE IS AN OPTIONAL STEP


TABLE OF OPERATIONAL PARAMETERS

| Parameter | Fixed or Variable |
| --------- | ----------------- |
| Feed COD | Variable |
| Feed Flow rate | Variable |
| Temperature | BOTH |
| Architecture | Fixed |
| Material | Fixed |
| Oxidising agent | Fixed |
| Culture Purity | Not sure |
| Biofilm thickness | Variable |
| COD Removal Efficiency | Operational |

POTENTIALLY TALK ABOUT POWER GENERATION HERE



# Motivation

- I want to help this problem 
- I enjoy clean water
- I like modelling
    - Would previous experience be interesting/useful?


# Background 

A broad overview of Microbial Fuel Cells is provided by a textbook on the subject by @Logan2008. 

## Power Generation 
- Polarisation and power curves are used to characterise MFC power generation
- Changing the external resistance provides variable voltage
- _Use a good example to illustrate to the reader_
- We can use polarisation curve to calculate current and plot current vs voltage or current density
- Generally split into three sections - middle is the most important as it shows internal resistance of cell
- Shows how well the MFC maintains a voltage as a function of current production
- Maximum power can be read off the top of the curve
- External resistance has to be used as low resistance in the cell is not enough for feasible power generation
- We don't want to increase internal resistance because the cell will perform significantly worse

## Mixed vs pure culture 
- From: Jadhav + Ghangrekar 2020
- Mixed cultures are better for overall functionality
    - Higher specific power 
    - Resistance against shock load conditions
    - Reduced substrate specificity 
    - Lower Coulombic efficiency
- Pure have increased power output and Coulombic efficiency
    - Increased cost
    -  Risk of contamination
    - Difficult to isolate a single strain 

## Cathode oxidising agent

## Architecture

## Materials

- Need practical and cheap options for large scale reactors
- Main components are anode,cathode and potentially a membrane
    - Membrane is optional as it adds to the internal resistance
    - Generally used to separate anodic and cathodic liquids
- Cathode requires a catalyst - ideally find a non precious metal 
    - Current is carbon based with a Pt catalyst @Logan2008
- Ideal ratio is 100 m$^2$ of surface area per m$^3$ of reactor @Logan2008
- Common option is carbon cloth
- Cheap and porous
- Good for bacteria to grow on
## Biofilm

- Layers of bacteria that form on the anode 
- Increasing bacteria increases electron release
- If biofilm is too thick then there are mass transport issues
- _How do we control it?_
- Will generally be a few millimetres thick @Logan2008

## Temperature
- Process is fundamentally biological 
- Therefore bacteria is affected by temperature 
- Higher temperatures generally correlate with larger power output
- USE THIS SECTION TO LINK TO INTRODUCTION/MOTIVATIONS LATER

## COD Removal Efficiency 

- Tied to Coulombic efficiency
    - Definition of CE (Logan 2008): Fraction of electrons recovered as current vs that in the starting organic matter
- We want it to be high so that the cell is efficient and doesn't require large flow rates to be effective 
- We also want it to be high so that it can actually treat the wastewater
    - Or at least, high enough that if further treatment steps are necessary they aren't too expensive,toxic or difficult to implement


## Flow rate

- More flow means higher COD available in set time
- Also increases shear stress on the cell 
- Too high and the cell may not be able to achieve required level of COD removal
- We want this high so we can deal with plenty of wastewater
- _Get source on average UK individual production of wastewater and typical treatment plant values_
- If each cell can deal with a high flow rate then we need less per unit volume, reducing costs, materials and maintenance 

## Maintenance 

- How does one maintain a cell?
- Important consideration for both lab and industrial scale

# Literature Review

A potential configuration for a domestic Wastewater Treatment Plant (WWTP) was considered by @Logan2008 and is shown below in Figure \ref{fig:WWTP_Diagram}.

\begin{figure}[H]
  \includegraphics[width=\linewidth]{WWTP_Diagram.png}
  \caption{Process flow train for a domestic wastewater treatment plant (Logan,2008)}
  \label{fig:WWTP_Diagram}
\end{figure}

First the wastewater is screened to remove large pieces of debris that may have entered upstream. The wastewater's flow is then measured and recorded. This allows for comparison with past data to determine any anomalous flow that may enter the system as 
as result of flooding or similar events. The wastewater then undergoes grit removal to prevent gritty particles such as coffee grinds 
or bones from damaging pumps. Typically this will involve a hydraulic residence time (HRT) of between 1-20 minutes. Following this, the wastewater will be tested for either its biochemical oxygen demand (BOD) or its chemical oxygen demand (COD). The BOD takes 5 days and shows what material can be biologically removed, whilst the rapid COD test provides an assessment of all organic matter present.  

Some of the biological material present as particulates is then removed in the primary clarifier, usually by collecting solids that accumulate at the bottom of the tank in a process with a HRT between 1-3 hours. Once this has been done the biological material will have been reduced to around 200 mg L$^{-1}$ and the water will be ready for the wastewater treatment. It is proposed that this step will be done by a system based on MFCs to take advantage of the electricity generation and other related benefits over current systems. Finally the wastewater goes a chlorination stage to kill of any remaining bacteria and then a dechlorination stage to prevent harm coming to aquatic life located where the water is released. 

Within recent years interest in MFCs has increased. This is made clear by review papers considering the current state of modelling work such as those by @Ortiz-Martínez2015 and @Xia2018. These papers are very useful as they provide a broad overview into the technical work in key areas such as potential cell architecture, key parameters to consider and common model assumptions.

For instance, comprehensive models that seek to model all major processes such as the mass diffusion and substrate consumption can be either half cell models that consider the activity around the anode or full cell models that consider both the anode and cathode. Whilst the reaction around the anode is generally considered the limiting stage within the cell, the model for this proposed project will be a full model to provide as much insight into the internal processes of the cell when supplied with a low temperature feed. As a result, the model will be able to produce outputs relating to the biofilm thickness, fuel flow rate and concentration in addition to the electricity generation for comparison to experimental data. 

The experimental work around MFCs has been studied for longer than the modelling aspect and as a result there are plenty of papers available that provide experimental data for comparison with the results from a model. For this project, the main papers considered for this proposal focused on long term operation of MFCs. @Santoro2012 operated a cell for 26 weeks, operated at 30$^{\circ}$C whilst @Moon2006 were able to operate multiple cells for 2 years over a range of temperatures. These results illustrate the operational viability of MFCs as successful long term operation reduces the need for maintenance or replacement of cells. This in turn allows MFC systems to be operated for longer resulting in reliable wastewater treatment.

However, the temperatures considered by both of these papers are not reflective of typical temperatures of UK wastewater _Access Database evidence_. Therefore, the is scope for research into the performance of MFCs at lower temperatures to determine potential power outputs and thus potential feasibility. 

To provide experimental data for direct comparison with the proposed model the work done by @Cheng2011 has been considered.
This research involved testing the power output of MFCs between 4-30$^{\circ}$C having initialised them at 15$^{\circ}$C or 30$^{\circ}$C prior. This research suggests that cells initialised at higher temperatures produce reasonable 
quantities of power and could be used within a WWTP in the UK. This is an important fact to establish prior to any modelling work as it demonstrates that operation of these cells at lower temperatures is possible and therefore 
time spent modelling them is not being wasted. 

The large amount of experimental work provides plenty of data to validate new and existing MFC models. One such example 
is a model  developed by @Oliveira2013 that could correctly predict how the substrate concentration and temperature affected the cells biofilm thickness and performance. As part of this the 
temperature considered by model was adjusted between the values of 20$^{\circ}$C, 30$^{\circ}$C and 40$^{\circ}$C. 
The key takeaway from this is that there are models accurate and reliable models available that allow for adjustment
of the temperature. Therefore, this model could potentially be adapted to investigate MFC performance at lower temperatures as part of the proposed project

Other potential models that could be used as the basis for the project include those considered by @Pinto2010 and @Zheng2010. Both of these were able to successfully predict MFC behaviour and performance when compared to 
experimental data despite being based on different principles. @Pinto2010 developed a half-cell model based 
on the anode whilst @Zheng2010 developed a model based on the cathode. This was unusual as the anodic step is generally considered to be reaction limiting. The existence and accuracy of these models demonstrates that there is good degree of flexibility available when initially building and then refining a model. As a result, the final model considered by the project may differ significantly from the one considered initially. 

# Objectives 

- MAKE THESE "SMART" 
- MORE SPECIFIC AND DETAILED THAN THE ONES IN THE LITERATURE ANALYSIS

# References