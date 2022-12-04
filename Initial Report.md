---
Title: "Initial Report"
subtitle: "Fred Barrett"
author: "Fred Barrett"
subject: "Microbial Fuel Cells"
keywords: "Power generation"

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

- General opener

## Wastewater in the UK

Reporting by @Conway2022 indicates that untreated sewage has been repeatedly released or dumped into rivers across the United Kingdom.
In total, it is believed that sewage was dumped more than 3000 times between 2017 and 2021. This is despite regulation controls by 
Ofwat, whose stated vision is "to make the greatest contribution possible to improving life through water" @Ofwat2014. According to the Environment Audit Committee 36% of this pollution stems from sewage and wastewater sources, @EAC2022. As a result, only 14% of rivers in England can claim to have good ecological status.

## A Potential Solution

A potential solution to this ecological problem is the introduction of new technology to current wastewater treatment techniques.
Microbial Fuel Cells (MFCs) have been around since the mid 19th Century, but the technology was not considered to be a viable source
of power generation, @Scott2016. They are considered desirable for wastewater treatment due to their ability to treat waste water whilst simultaneously generating electricity.

Recently, these cells gave undergone a revival in research and sources such as @Herrero-Hernande2013 claim that the technology
is now at a stage where it should be considered workable.

Figure \ref{} below shows a typical diagram of an MFC.

FIGURE HERE

The principal components of a Microbial Fuel Cell are an anode and a cathode, @Logan2008. These can be arranged in a variety of ways with multiple of either comprising the cell. In addition, a membrane can be included to separate anodic and cathodic liquids however these are not preferred as they increase the internal resistance of the cell, reducing electron transfer.  

## Key Parameters



- These are a mix of operational and fundamental e.g. temperature is an operational variable but material and architecture aren't
- Should mention all of these below but might be able to break it up

Table \ref{tab:parameters} below contains the key parameters for consideration when discussing Microbial Fuel Cells

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

Table: List of parameters
\label{tab:parameters}

POTENTIALLY TALK ABOUT POWER GENERATION HERE



# Motivation

- Avid hiker and canoer 
- I want to help this problem 
- I enjoy clean water
- I like modelling
    - Would previous experience be interesting/useful?


# Technical background 

- Here to provide technological context to the topic as a whole as well as the literature review
- Level of detail will be iterated depending on how the doc flows

## Power Generation 
- Polarisation and power curves are used to characterise MFC power generation
- Changing the external resistance provides variable voltage
- External resistance has to be used as low resistance in the cell is not enough for feasible power generation
- We don't want to increase internal resistance because the cell will perform significantly worse
- _Use a good example to illustrate to the reader_
- We can use polarisation curve to calculate current and plot current vs voltage or current density
- Generally split into three sections - middle is the most important as it shows internal resistance of cell
- Shows how well the MFC maintains a voltage as a function of current production
- Maximum power can be read off the top of the curve

## Feed COD 

The Chemical Oxygen Demand (COD) of wastewater is defined as the quantity of water necessary to oxidise the organic matter present in 
said water @Scimed2021. If water with a high COD is discharged then downstream organisms will face increased competition for oxygen which will affect the 
aquatic life present.

## COD Removal Efficiency 

For effective wastewater treatment a high COD removal efficiency is desirable to reduce downstream competition for oxygen. It is calculated as $\frac{COD_{Inlet}-COD_{Outlet}}{COD_{Inlet}} \times 100$. 

### Coulombic Efficiency

A related parameter is the Coulombic efficiency which is the fraction of electrons recovered as current versus that in the starting organic matter, @Logan2008. A desirable MFC will have a high COD removal efficiency and Coulombic efficiency to maximise both the power generated and the volume of wastewater that can be treated.

## Mixed vs pure culture 

Due to the biological nature of MFCs, the purity of bacterial species used on the anode is a parameter for optimisation as considered by @Jadhav2020. Pure cultures tend to produce an increased power output and Coulombic efficiency compared to mixed cultures.
However, this comes at the cost of an increased cost to procure the bacteria, due to the inherent difficulty of fully separating bacterial strains, as well as the risk of contamination from wastewater. On the other hand, mixed cultures are better for overall functionality due to their reduced substrate specificity and resistance to shock load conditions. Therefore, the more feasible MFC designs for scale-up will contain mixed cultures.

## Biofilm

The biofilm of an MFC is the layers of bacteria that form on the anode. As the thickness of the biofilm increases the quantity of bacteria increases, this allows for an increased rate of electron release as the organic matter present is broken down. However, if the biofilm is too thick then there will be mass transport issues that will reduce the power output of the cell. As a result, according to @Logan2008, biofilms are generally a few millimetres thick.  

## Architecture

- The previous work should go into the introduction section
- It makes the most sense when compared with the diagram from Zhang and Halme 
- What should go here is the stuff that appears in the literature review
- Half and full cell models and how they relate to chamber MFCs


## Materials

For large scale reactors, practical and inexpensive materials are desirable. These must be suitable for the anode, cathode and, if one is used, a membrane. The cathode generally requires a catalyst and this is usually Pt although a non-precious metal alternative would be preferred. When decided on a construction, material, @Logan2008 suggests that it should have a surface area to volume ratio of 100 m$^2$ m$^3$ of reactor.

Common material options are carbon based and include: carbon foam, carbon felt, carbon cloth and carbon paper. These were all compared by @Mateo2018 were able to achieve a specific surface area of 7500 m$^2$/m$^{-2}$. As a result, the material used could vary depending on price fluctuations at the time of cell production. 

## Cathode oxidising agent

- @Scott2016
- The oxidant is reduced by a catalyst
- In MFCs this produces water
- Since we're dealing with protons, oxygen is a natural choice of catalyst

## Flow rate

The flow rate of wastewater dictates the available COD for the cell. By increasing it, the cell will be in contact with more organic matter in a set period of time which as @Ieropoulos2010 states, is beneficial to treating wastewater. However, if the flow rate is too high then the cell may not be able to achieve the required levels of COD removal. This could necessitate the inclusion of further downstream treatment steps. Additionally, @Villaseñor2013 established that at high flow rates there is a risk of unoxidised matter entering the cathodic chamber, causing it to enter into anaerobic condition, stopping the MFC from working. 

## Maintenance 

- How does one maintain a cell?
- Important consideration for both lab and industrial scale

## Temperature

As the processes inside a MFC are fundamentally biological in nature the cell is affected by temperature. A higher temperature correlates with a larger power output as lower temperatures slow down the growth and reproduction of bacteria. 

# Wastewater Treatment

A potential configuration for a domestic Wastewater Treatment Plant (WWTP) was considered by @Logan2008 and is shown below in Figure \ref{fig:WWTP_Diagram}.

\begin{figure}[H]
  \includegraphics[width=\linewidth]{WWTP_Diagram.png}
  \caption{Process flow train for a domestic wastewater treatment plant (Logan,2008)}
  \label{fig:WWTP_Diagram}
\end{figure}

First the wastewater is screened to remove large pieces of debris that may have entered upstream. The wastewater's flow is then measured and recorded. This allows for comparison with past data to determine any anomalous flow that may enter the system as a result of flooding or similar events. The wastewater then undergoes grit removal to prevent gritty particles such as coffee grinds 
or bones from damaging pumps. Typically, this will involve a hydraulic residence time (HRT) of between 1-20 minutes. Following this, the wastewater will be tested for either its biochemical oxygen demand (BOD) or its chemical oxygen demand (COD). The BOD takes 5 days and shows what material can be biologically removed, whilst the rapid COD test provides an assessment of all organic matter present.  

Some biological material present as particulates is then removed in the primary clarifier, usually by collecting solids that accumulate at the bottom of the tank in a process with a HRT between 1-3 hours. Once this has been done the biological material will have been reduced to around 200 mg L$^{-1}$ and the water will be ready for the wastewater treatment. It is proposed that this step will be done by a system based on MFCs to take advantage of the electricity generation and other related benefits over current systems. Finally, the wastewater goes a chlorination stage to kill of any remaining bacteria and then a dechlorination stage to prevent harm coming to aquatic life located where the water is released. 

# Literature Review

- GO BACK AND MENTION PARAMETERS CONSIDERED EARLIER

Within recent years interest in MFCs has increased. This is made clear by review papers considering the current state of modelling work such as those by @Ortiz-Martínez2015 and @Xia2018. These papers are very useful as they provide a broad overview into the technical work in key areas such as potential cell architecture, key parameters to consider and common model assumptions.

For instance, comprehensive models that seek to model all major processes such as the mass diffusion and substrate consumption can be either half cell models that consider the activity around the anode or full cell models that consider both the anode and cathode. Whilst the reaction around the anode is generally considered the limiting stage within the cell, the model for this proposed project will be a full model to provide as much insight into the internal processes of the cell when supplied with a low temperature feed. As a result, the model will be able to produce outputs relating to the biofilm thickness, fuel flow rate and concentration in addition to the electricity generation for comparison to experimental data. 

## Experimental Work

The experimental work concerning MFCs has been studied for longer than the modelling aspect and as a result there are plenty of papers available that provide experimental data for comparison with the results from a model. For this project, the main papers considered for this proposal focused on long term operation of MFCs. @Santoro2012 operated a cell for 26 weeks, operated at 30$^{\circ}$C whilst @Moon2006 were able to operate multiple cells for 2 years over a range of temperatures. These results illustrate the operational viability of MFCs as successful long term operation reduces the need for maintenance or replacement of cells. This in turn allows MFC systems to be operated for longer resulting in reliable wastewater treatment.

However, the temperatures considered by both of these papers are not reflective of typical temperatures of UK wastewater _Access Database evidence_. Therefore, the is scope for research into the performance of MFCs at lower temperatures to determine potential power outputs and thus potential feasibility. 

To provide experimental data for direct comparison with the proposed model the work done by @Cheng2011 has been considered.
The research involved testing the power output of MFCs between 4-30$^{\circ}$C having initialised them at 15$^{\circ}$C or 30$^{\circ}$C prior. This research suggests that cells initialised at higher temperatures produce reasonable 
quantities of power and could be used within a WWTP in the UK. This is an important fact to establish prior to any modelling work as it demonstrates that operation of these cells at lower temperatures is possible and therefore 
time spent modelling them is not being wasted. 

## Modelling Work

The large amount of experimental work provides plenty of data to validate new and existing MFC models. One such example 
is a model developed by @Oliveira2013 that could correctly predict how the substrate concentration and temperature affected the cells biofilm thickness and performance. As part of this the 
temperature considered by model was adjusted between the values of 20$^{\circ}$C, 30$^{\circ}$C and 40$^{\circ}$C. 
The key takeaway from this is that there are models accurate and reliable models available that allow for adjustment
of the temperature. Therefore, this model could potentially be adapted to investigate MFC performance at lower temperatures as part of the proposed project

Other potential models that could be used as the basis for the project include those considered by @Pinto2010 and @Zheng2010. Both of these were able to successfully predict MFC behaviour and performance when compared to 
experimental data despite being based on different principles. @Pinto2010 developed a half-cell model based 
on the anode whilst @Zheng2010 developed a model based on the cathode. This was unusual as the anodic step is generally considered to be reaction limiting. The existence and accuracy of these models demonstrates that there is good degree of flexibility available when initially building and then refining a model. As a result, the final model considered by the project may differ significantly from the one considered initially. 

# Objectives 

- MAKE THESE "SMART" 
- MORE SPECIFIC AND DETAILED THAN THE ONES IN THE LITERATURE ANALYSIS

# Project Schedule 

- Gantt Chart
    - Detailed
    - Coursework dates
    - Term dates
    - Supervisor meetings?
    - Clear stages 
- Previous modelling experience

# References