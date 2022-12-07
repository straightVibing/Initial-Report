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
nocite: |
    @Zhang1995

link-citations: true

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


Changes since last meeting: 29/11

- Source for high flowrates
- Source for cathodic chamber flooding
- Source for carbon cloth
- Moved previous writeup of archetechture to the beginning as I thought it made more sense there
- Source that MFCs are good for wastewater treatment that isnt logan
- Wrote up an introduction
- Brief writeup for key parameters
- Brief intro to technical section
- Oxidising agent writeup 
- Added MFC diagram 
- Updated cover page
- Expansion on mixed versus pure
- Added to experimental work writeup
- Added modelling assumptions
- power and polarisation curve writeup

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

Figure \ref{fig:ZH_Diagram} below shows a typical diagram of an MFC.

\begin{figure}[H]
  \includegraphics[width=\linewidth]{ZH_Diagram.png}
  \caption{Diagram of a Microbial Fuel Cell (Zhang and Halme, 1995)}
  \label{fig:ZH_Diagram}
\end{figure}


MFCs operate by oxidising organic components to release electrons and protons,@Yujin2019, which are then used for power generation.
The principal components of a Microbial Fuel Cell are an anode and a cathode, @Logan2008. These can be arranged in a variety of ways with multiple of either comprising the cell. In addition, a membrane can be included to separate anodic and cathodic liquids however these are not preferred as they increase the internal resistance of the cell, reducing electron transfer.  

## Key Parameters

The key operational and fundamental parameters that affect MFCs are shown below in Table \ref{tab:parameters}. Several of these have
been expanded within the Technical Background section of this proposal.

| Parameter | Notes |
| --------- | ----------------- |
| Feed COD | Variable |
| COD Removal Efficiency | Variable |
| Culture Purity | Variable |
| Biofilm | Variable |
| Architecture | Fixed |
| Material | Fixed |
| Oxidising agent | Fixed |
| Feed Flow rate | Variable |
| Temperature | Variable |

Table: List of parameters
\label{tab:parameters}

# Motivation


- Avid hiker and canoer 
- I want to help this problem 
- I enjoy clean water
- I like modelling



# Technical Context & Overview

This section has been designed to provide technical context to a reader who may be looking for some background on Microbial Fuel Cells
and concerns the key parameters mentioned earlier.

## Power Generation 

A typical circuit arrangement involves including a source of external resistance alongside the MFC, @Logan2008. It is essential to use an external source of resistance as the internal resistance inside the cell is not enough for feasible power generation and increasing it would rapidly decrease the performance of the cell. Alternating this external resistance within a circuit provides a variable voltage output.

This output can be used to plot a polarisation curve of the external resistance against the cell voltage which can be used to calculate
the current. From this the current density can be plotted against the cell voltage to produce a power curve. This power curve can generally be divided into three separate zones, referred to as the kinetic region, ohmic region and the mass-transfer region. 
This is because as the current density increases different factors hold more sway over the cell. The most important region is the ohmic
region as this shows the internal resistance of the cell, a key parameter to be minimised.

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
In addition, as stated by @Yujin2019 cells using pure cultures are useful to explain the complicated electron transfer mechanisms within MFCs.  

However, this comes at the cost of an increased cost to procure the bacteria, due to the inherent difficulty of fully separating bacterial strains, as well as the risk of contamination from wastewater. On the other hand, mixed cultures are better for overall functionality due to their reduced substrate specificity and resistance to shock load conditions. Therefore, the more feasible MFC designs for scale-up will contain mixed cultures.


## Biofilm

The biofilm of an MFC is the layers of bacteria that form on the anode. As the thickness of the biofilm increases the quantity of bacteria increases, this allows for an increased rate of electron release as the organic matter present is broken down. However, if the biofilm is too thick then there will be mass transport issues that will reduce the power output of the cell. As a result, according to @Logan2008, biofilms are generally a few millimetres thick.  

- NEEDS MORE DETAIL
- Comment on the fact that most implementations have basic implementation of what happens in a biofilm
- Either taken from literature or assumptions
- In-depth Analysis of biofilm is very rarely considered - mentioned later on
- Comment on that

- @Yujin2019
  - Mentions different types of electron transfer: direct and indirect
  - Would be good to have another source that concurs



## Architecture

- The previous work should go into the introduction section
- It makes the most sense when compared with the diagram from Zhang and Halme 
- What should go here is the stuff that appears in the literature review
- Half and full cell models and how they relate to single and double chamber MFCs


## Materials

For large scale reactors, practical and inexpensive materials are desirable. These must be suitable for the anode, cathode and, if one is used, a membrane. The cathode generally requires a catalyst and this is usually Pt although a non-precious metal alternative would be preferred. When decided on a construction, material, @Logan2008 suggests that it should have a surface area to volume ratio of 100 m$^2$ m$^3$ of reactor.

Common material options are carbon based and include: carbon foam, carbon felt, carbon cloth and carbon paper. These were all compared by @Mateo2018 were able to achieve a specific surface area of 7500 m$^2$/m$^{-2}$. As a result, the material used could vary depending on price fluctuations at the time of cell production. 

## Cathode oxidising agent

In an MFC the oxidised organic matter releases protons which are then reduced in the presence of a catalyst, @Scott2016. This is
typically oxygen as it is readily available. This results in MFCs producing water as a by-product.

## Flow rate

The flow rate of wastewater dictates the available COD for the cell. By increasing it, the cell will be in contact with more organic matter in a set period of time which as @Ieropoulos2010 states, is beneficial to treating wastewater. However, if the flow rate is too high then the cell may not be able to achieve the required levels of COD removal. This could necessitate the inclusion of further downstream treatment steps. Additionally, @Villaseñor2013 established that at high flow rates there is a risk of unoxidised matter entering the cathodic chamber, causing it to enter into anaerobic condition, stopping the MFC from working. 

## Maintenance 

- How does one maintain a cell?
- Important consideration for both lab and industrial scale

## Temperature

As the processes inside an MFC are fundamentally biological in nature the cell is affected by temperature. A higher temperature correlates with a larger power output as lower temperatures slow down the growth and reproduction of bacteria. 

- Cold temperatures considered by @Dai2022

# Wastewater Treatment

A potential configuration for a domestic Wastewater Treatment Plant (WWTP) was considered by @Logan2008 and is shown below in Figure \ref{fig:WWTP_Diagram}.

\begin{figure}[H]
  \includegraphics[width=\linewidth]{WWTP_Diagram.png}
  \caption{Process flow train for a domestic wastewater treatment plant (Logan,2008)}
  \label{fig:WWTP_Diagram}
\end{figure}

First the wastewater is screened to remove large pieces of debris that may have entered upstream. The wastewater's flow is then measured and recorded. This allows for comparison with past data to determine any anomalous flow that may enter the system as a result of flooding or similar events. The wastewater then undergoes grit removal to prevent gritty particles such as coffee grinds 
or bones from damaging pumps. Typically, this will involve a hydraulic residence time (HRT) of between 1-20 minutes. Following this, the wastewater will be tested for either its biochemical oxygen demand (BOD) or its chemical oxygen demand (COD). The BOD takes 5 days and shows what material can be biologically removed, whilst the rapid COD test provides an assessment of all organic matter present.  

Some biological material present as particulates is then removed in the primary clarifier, usually by collecting solids that accumulate at the bottom of the tank in a process with an HRT between 1-3 hours. Once this has been done the biological material will have been reduced to around 200 mg L$^{-1}$ and the water will be ready for the wastewater treatment. It is proposed that this step will be done by a system based on MFCs to take advantage of the electricity generation and other related benefits over current systems. Finally, the wastewater goes a chlorination stage to kill of any remaining bacteria and then a dechlorination stage to prevent harm coming to aquatic life located where the water is released. 

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

Further work has been done testing the ability of MFCs to directly treat wastewater discharge at its source. @Harewood2017 and @Wen2009 have both investigated the potential of 
these cells to treat brewery wastewater whilst @Rahman2018 considered the treatment of sugar beet processing wastewater. These experiments were able to produce power in addition
to dealing with the industrial waste created, highlighting the feasibility of treating wastewater at the source. 

@Wen2009 used a single air-cathode MFC using carbon fibre as the anode material whilst @Harewood2017 used a dual chamber setup which most notably contained a chitosan/polymalic acid-citric acid membrane. This was designed to introduce multiple charged groups to increase mass transport through the cell. These two studies saw very different maximum
densities with @Wen2009 achieving a a density of 264 mW/m$^2$ whilst @Harewood2017 achieved a density of 3022.39 mW/m$^2$. It is worth noting that the former used a COD of
626.58 mg/L whilst the latter had a COD of 3228 mg/L an increase of 525%. Whilst this goes some way to explaining the large difference in power densities a further explanation
is that the technology surrounding MFCs has improved since the initial experiment conducted by @Wen2009. 


## Modelling Work

- methodologies 
- approaches
- equations
- assumptions
- Aim for a 1/2 a page more
- Pick out interesting points at the end of modelling work
- Link to objectives section

The large amount of experimental work provides plenty of data to validate new and existing MFC models. One such example 
is a model developed by @Oliveira2013 that could correctly predict how the substrate concentration and temperature affected the cells biofilm thickness and performance. As part of this the 
temperature considered by model was adjusted between the values of 20$^{\circ}$C, 30$^{\circ}$C and 40$^{\circ}$C. 
The key takeaway from this is that there are models accurate and reliable models available that allow for adjustment
of the temperature. Therefore, this model could potentially be adapted to investigate MFC performance at lower temperatures as part of the proposed project

Other potential models that could be used as the basis for the project include those considered by @Pinto2010 and @Zheng2010. Both of these were able to successfully predict MFC behaviour and performance when compared to 
experimental data despite being based on different principles. @Pinto2010 developed a half-cell model based 
on the anode whilst @Zheng2010 developed a model based on the cathode. This was unusual as the anodic step is generally considered to be reaction limiting. The existence and accuracy of these models demonstrates that there is good degree of flexibility available when initially building and then refining a model. As a result, the final model considered by the project may differ significantly from the one considered initially. 

It is notable that @Pinto2010 and another model by @Littfinski2022 used similar assumptions concerning the biofilm formation and retention. In both cases the expected changes to
the biofilm were not computed by the model directly but were instead taken from a different and specific biofilm model designed to model biofilm growth on an anode. This is a 
fairly common practice among MFC models, @Ortiz-Martínez2015, and is done due to the difficulty of integrating a more complete simulation of the biofilm's growth within an MFC
model. Other notable assumptions include a fixed cathode potential as mentioned by @Xia2018 which is used for single chamber, half cell models concerning the anode. Additionally, some models such as those by @Zhang1995 assumed that the mass transport through the cell was rapid to be discounted. This assumption was made as this model was one
of the very first models created to model MFC performance and is very rarely used today, @Ortiz-Martínez2015. A further assumption, made by @Littfinski2022 and @Wang2011 is to
neglect the substrate consumption gradient within the cell and instead assume a fixed value. 

# Objectives 

- As bullet points with sentence underneath for justification
- Link to end of modelling review


# Project Schedule 

- Gantt Chart
    - Detailed
    - Coursework dates
    - Term dates
    - Supervisor meetings?
    - Clear stages 
- Previous modelling experience

# References

\footnotesize