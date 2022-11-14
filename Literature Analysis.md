---
Title: "Literature Analysis "
subtitle: "Fred Barrett"
geometry:

- top = 20mm
- left = 20mm
- right = 20mm
documentclass: article


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

## Review

### Developments in microbial fuel cell modelling

- "Interest has significantly increased in recent decades"
- MFC modelling tends to be neglected
- Introduces the comprehensive type of models
- Anode based 
- Cathode based
- Mentioned parameters that are important:
    - Biofilm thickness
    - Fuel flow rate and concentration
    - Temperature (mentions experimental ranging from 15-40 degrees C)

### Models for Microbial Fuel Cells: A critical review

- Different models make different assumptions:
    - Full vs half cell models
    - Mechanism vs Application based
        - Mechanism: Focus on key reaction processes: substrate utilisation, voltage and current, biofilm formation etc
        - Application: Focus on electrical models to aide understanding of how MFCs will function as electrical devices
    - Mine will be mechanism based 
- Doesn't mention models that considered temperature as their primary parameter
- Therefore my research has a USP

## Experimental Work

### Power generation from wastewater using single chamber microbial fuel cells (MFCs) with platinum-free cathodes and pre-colonized anodes

- Operated for 26 weeks
- We don't want biofilm growth on cathode due to increased proton transfer resistance
- Colonized with wastewater - University of Connecticut wastewater treatment plant
    - Potential flow basis for my model
- Operated at 30 degrees

### Continuous electricity production from artificial wastewater using a mediator-less microbial fuel cell

- Mediator is used to separate out cathodic and anodic fluids
- Anode volume of 20 ml
    - scale-up issues 
- Best result obtained at 35 degrees
    - Not realistic for UK expect for heatwaves
- Power stably generated over 2 years
    - Viability for larger scale deployment if individual cells don't require frequent maintenance

### Electricity generation of single-chamber microbial fuel cells at low temperatures

- Main source of comparison with my model at present
- 4-30 degrees C
- States that initially operating MFCs at 30 degrees allows them to provide reasonable power generation at lower temperatures
- Evidence for feasibility of project 

## Modelling

### A 1D mathematical model for a microbial fuel cell

- Model correctly predicted how substrate concentration and temperature affect biofilm thickness and cell performance
    - Therefore project is feasible 
- Modelled temp ranges of 20,30 and 40 degrees
    - Varying temperature is a possibility of these models
- Since lower temperatures not considered, research maintains a niche

### A two-population bio-electrochemical model of a microbial fuel cell

- "Energy from organic waste cannot be recovered using traditional methods"
- This is because it has a complex composition and is usually very dilute
- Model based on anode and focuses on bio-chemical reactions there
    - Therefore, assumes cathode reaction rate is non-limiting
- Demonstrates influence of organic load and external resistance on the MFC power output and long term performance
    - Experiments from 35 - 60 days
    - Adjusted influent acetate concentration between 275 - 2550 mg-S L-1
    - External resistance set between ~10-25 ohms above Rint as well as 5 ohms (below Rint)
- Validated with experimental results
    - Plots of simulated vs measured results show the models follows the patterns of behavior of MFCs
    - Results look pretty good based off graphical comparisons

### Modelling and simulation of two-chamber microbial fuel cell

- "Modelling remain scarce" 
- Claims cathodic reaction is the rate limiting step 
- Flow has an effect on power
- Artificial wastewater
- Useful for scale-up
- Claims reducing feed flow could increase power


### A generalized whole-cell model for wastewater-fed microbial fuel cells

- Mentions a lit review that found COD removal efficiency can be between 5-99% depending on operating conditions.
- Experimental work featured municipal wastewater
- Whole cell model so anode and cathode
- Model assesses after the startup phase of 32 days

### Electricity generation and modelling of microbial fuel cell from continuous beer brewery wastewater

- COD removal efficiency of 40-43% classed as good enough for wastewater treatment
- Low flow-rates considered in experimental work
- Most detailed wastewater description
- Cell operated between 20-28 degrees C
