---
Title: "Literature Review"
subtitle: "Fred Barrett"
geometry:

- top = 20mm
- left = 20mm
- right = 20mm
documentclass: article

bibliography: Dissertation_References.bib

fontsize: 10pt
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
        \fancyhead[L]{Literature Analysis}
        \fancyhead[R]{Fred Barrett}
        \usepackage{hyperref}
        \usepackage{amsmath}
        \usepackage{wrapfig}
        \usepackage{lipsum}
        \usepackage{blindtext}
---

# Introduction/Motivations/Objectives/Context

- Wastewater in the UK
- How bad is it and evidence
- Establish clear problem
- Bring up MFCs
- Description and discussion of major design parameters
    - A table could be a coherent way show them
- Can use diagram from Zheng and Halme 1995 for visualisation 

# Aims

- Assess currently available literature on MFCs 
- Present a clear and logical narrative
- High quality critical analysis 
- Set the project within a wider context


# The Plan

- Literature read in preparation for dissertation
- Covers a range of key topics
    - Background and context:
        - Expand my knowledge 
        - Provide information for the reader
            - Strike a balance between this analysis and the critical review
    - Review papers:
        - What is the current situation in the research community
        - Work that has been done
        - Suggested areas of future work
    - Experimental work:
        - Detailed information on current capabilities
        - Results that can be used for comparison to test model viability
        - Helps define what our models should be looking for
    - Modelling Papers
        - Specific work relevant to my project
        - What are the assumptions and why?
        - Parameters that were considered and why?

## Background

### Microbial fuel cells

A possible arrangement for a Wastewater Treatment Plant (WWTP) was considered by @Logan2008. This consisted of STEAL FROM THE BOOK. 

@Logan2008


- Most of the information I've learned from this will go in the beginning 
    - Key parameters, general design etc
- Proposes how an MFC based Wastewater Treatment Plant would function
    - Evidence for intro/motivations of research 
    - Approximately 200 mg L$^{-1}$ of organic matter in fluid 
        - Possible value for model parameter
- Concept of normalising power by surface area and volume
    - A way to assess performance of model and provide comparison
        - Highest is 0.115 kW m$^3$ 
- Minimise Rint
- Energy efficiency ranges from 2%-50%



Within recent years interest in MFCs has increased. This is made clear by review papers considering the current state of
modelling work such as those by @Ortiz-Martínez2015 and @Xia2018. These papers are very useful as they provide a broad
overview into the technical work in key areas such as potential cell architecture, key parameters to consider and common
model assumptions.

For instance, comprehensive models that seek to model all major processes such as the mass diffusion and substrate 
consumption can be either half cell models that consider the activity around the anode or full cell models that consider both the anode and cathode. Whilst the reaction around the anode is generally considered the limiting stage within the cell, the model for this proposed project will be a full model to provide as much insight into the internal processes of the cell when supplied with a low temperature feed. As a result, the model will be able to produce outputs relating to 
the biofilm thickness, fuel flow rate and concentration in addition to the electricity generation for comparison to 
experimental data. 

The experimental work around MFCs has been studied for longer than the modelling aspect and as a result there are plenty
of papers available that provide experimental data for comparison with the results from a model. For this project, the main papers considered for this proposal focused on long term operation of MFCs.
@Santoro2012 operated a cell for 26 weeks, operated at 30$^{\circ}$C whilst @Moon2006 were able to operate multiple cells for 2 years over a range of temperatures. These results illustrate the operational viability of MFCs 
as successful long term operation reduces the need for maintenance or replacement of cells. This is important
because if MFCs are used as part of a WWTP then they may not be readily accessible. REWORD

However, the temperatures considered by both of these papers are not reflective of typical temperatures of UK wastewater SOURCE. Therefore, the is scope for research into the performance of MFCs at lower temperatures to determine potential
power outputs and thus potential feasibility. 

To provide experimental data for direct comparison with the proposed model the work done by @Cheng2011 has been considered.
This research involved testing the power output of MFCs between 4-30$^{\circ}$C having initialised them at 15$^{\circ}$C or 30$^{\circ}$C prior. This research suggests that cells initialised at higher temperatures produce reasonable 
quantities of power and could be used within a WWTP in the UK. This is an important fact to establish prior to any modelling work as it demonstrates that operation of these cells at lower temperatures is possible and therefore 
time spent modelling them is not being wasted. 

The large amount of experimental work provides plenty of data to validate new and existing MFC models. One such example 
is a 1D WHAT DOES THIS MEAN model  developed by @Oliveira2013 that could correctly predict how the substrate concentration and temperature affected the cells biofilm thickness and performance. As part of this the 
temperature considered by model was adjusted between the values of 20$^{\circ}$C, 30$^{\circ}$C and 40$^{\circ}$C. 
The key takeaway from this is that there are models accurate and reliable models available that allow for adjustment
of the temperature. Therefore, this model could potentially be adapted to investigate MFC performance at lower temperatures as part of the proposed project

Other potential models that could be used as the basis for the project include those considered by @Pinto2010 and @Zheng2010. Both of these were able to successfully predict MFC behaviour and performance when compared to 
experimental data despite being based on different principles. @Pinto2010 developed a half-cell model based 
on the anode whilst @Zheng2010 developed a model based on the cathode. This was unusual as the anodic step is generally considered to be reaction limiting. The existence and accuracy of these models demonstrates that there is good degree of flexibility available when initially building and then refining a model. As a result, the final model considered by the project may differ significantly from the one considered initially. 

# References