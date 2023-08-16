---
layout: tutorial_hands_on

title: Coastal Water Dynamics
zenodo_link: ''
questions:
- Which biological questions are addressed by the tutorial?
- Which bioinformatics techniques are important to know for this type of data?
objectives:
- The learning objectives are the goals of the tutorial
- They will be informed by your audience and will communicate to them and to yourself
  what you should focus on during the course
- They are single sentences describing what a learner should be able to do once they
  have completed the tutorial
- You can use Bloom's Taxonomy to write effective learning objectives
time_estimation: 3H
key_points:
- The take-home messages
- They will appear at the end of the tutorial
contributors:
- marie59
- contributor2

---


# Introduction

The Earth and Environmental Dynamics study is a huge complex topic, according to the Earth system under analysis and the specific objectives under consideration. [FAIR-EASE](https://fairease.eu/) planned to include in this effort three different Pilots, each one focusing on different Earth systems, each one having specific goals to achieve.

This tutorial deals with Coastal Water Dynamics (CWD) Pilot, and focuses on the coastal marine environment near river estuaries, where important processes, such as the evolution of plankton blooms or the transport and fate of nutrients, carbon and contaminants, critically depend on many factors, including river discharge, ocean circulation, meteorological conditions as well as biogeochemical processes. 
Specifically, the proposed demonstrator will focus on the Po river discharging into the Northern Adriatic.


> <details-title>State of the art</details-title>
> The Northern Adriatic has been monitored well over decades and numerous research activities covering all fields of environmental science are ongoing (Umgiesser et al, 2022; Ricci et al, 2022; Bonaldo et al, 2019).
{: .details}

> <details-title>Specific data resources</details-title>
> Due to economic (fisheries, tourism), environmental (carbon cycle, pollutants, plastic) and scientific reasons, coastal regions, such as the Northern Adriatic, are usually well monitored.
> As a result, many diverse datasets, sometimes reaching back more than 100 years, exist an are publicly available. This includes data, sometimes daily observations, from dense station networks recording river discharge, as well as meteorological and oceanographic conditions.
> In addition, there are now more than three decades of data from satellite sensors measuring physical and biological properties of ocean surface waters, and a wide range of physical and biogeochemical numerical models, re-analysis and gridding systems producing nearly continuous sea state estimates in space and time.
{: .details}


> <agenda-title></agenda-title>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}

# Which data and why 

The training here proposed focuses on the coastal marine environment near river estuaries, in particular the Po river discharging into the Northern Adriatic.
The aim is to facilitate seamless access to multidisciplinary environmental datasets and to provide new ways of connecting and correlating data with specific attention to the Po river estuary in the Northern Adriatic sea.


## Get data

> <hands-on-title> Data Upload </hands-on-title>
>
> 1. Create a new history for this tutorial and give it a name (example: “CWD tutorial”) for you to find it again later if needed.
>
>    {% snippet faqs/galaxy/histories_create_new.md box_type="none" %}
>
> 2. Import the files from [Zenodo]({{ page.zenodo_link }}) or from
>    the shared data library (`GTN - Material` -> `{{ page.topic_name }}`
>     -> `{{ page.title }}`):
>
>    ```
>    
>    ```
>    ***TODO***: *Add the files by the ones on Zenodo here (if not added)*
>
>    ***TODO***: *Remove the useless files (if added)*
>
>
>     > <tip-title>Importing data from your computer</tip-title>
>     >
>     > * Open the Galaxy Upload Manager {% icon galaxy-upload %}
>     > * Select **Choose local files**
>     > * Browse in your computer and get the downloaded zip folder
>     >
>     > * Press **Start**
>     {: .tip}
>
>    {% snippet faqs/galaxy/datasets_import_via_link.md %}
>
>    {% snippet faqs/galaxy/datasets_import_from_data_library.md %}
>
> 3. Rename the datasets
> 4. Check that the datatype
>
>    {% snippet faqs/galaxy/datasets_change_datatype.md datatype="datatypes" %}
>
> 5. Add to each database a tag corresponding to ...
>
>    {% snippet faqs/galaxy/datasets_add_tag.md %}
>
{: .hands_on}

# Three tools for a complete Coastal Dynamics study

With the aim of supporting users in the exploitation of multiple, heterogeneous datasets, the Coastal Dynamics Pilot will significantly extend and enhance the capabilities of two existing well-proven, operational services: 
- ODV for on-line interactive analysis and visualization of environmental data;
- DIVAnd for intelligent spatial and temporal gridding of oceanographic data;
- SOURCE a new proposed web service based on the software tool, for the intercomparison of model results with time series observations of essential ocean variables (EOV).

***TODO***![ADD image](../../images/image_name "Legend of the image very detail (for blind people to be read to)")

The idea is to keep the theory description before quite simple to focus more on the practical part.

***TODO***: *Consider adding a detail box to expand the theory*

> <details-title> More details about the theory </details-title>
>
> But to describe more details, it is possible to use the detail boxes which are expandable
>
{: .details}

A big step can have several subsections or sub steps:


## **Interactive Source Notebooks**

SOURCE will create outputs in netCDF format that can be used in both DIVAnd and webODV for the multidisciplinary analysis of different data types.

> <hands-on-title> Sea Observations Utility for Reprocessing, Calibration and Evaluation</hands-on-title>
>
> 1. {% tool [Interactive Source Notebooks](interactive_tool_source) %} with the following parameters:
>    - *"Do you already have a notebook?"*: `Start with a fresh notebook`
>    - {% icon param-file %} *"Include data into the environment"*: `output` (Input dataset)
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}
***TODO***![ADD image](../../images/image_name "Legend of the image very detail (for blind people to be read to)")

## **ODV**

In addition to the data analysis and visualization services, ODV will also be used to prepare, combine and subset datasets, creating as output a set of netCDF files. 

> <hands-on-title>Ocean Data Viewer</hands-on-title>
>
> 1. {% tool [ODV](interactive_tool_odv) %} with the following parameters:
>    - {% icon param-file %} *"Netcdf file"*: `jupyter_notebook` (output of **Interactive DIVAnd Notebooks** {% icon tool %})
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}
***TODO***![ADD image](../../images/image_name "Legend of the image very detail (for blind people to be read to)")

## **Interactive DIVAnd Notebooks**

The netCDF files recovered from ODV will then be read by DIVAnd for the preparation of gridded products, also written as netCDF files.

> <hands-on-title>Data-Interpolating Variational Analysis in n dimensions</hands-on-title>
>
> 1. {% tool [Interactive DIVAnd Notebooks](interactive_tool_divand) %} with the following parameters:
>    - *"Do you already have a notebook?"*: `Start with a fresh notebook`
>    - {% icon param-file %} *"Include data into the environment"*: `jupyter_notebook` (output of **Interactive Source Notebooks** {% icon tool %})
>
>    ***TODO***: *Check parameter descriptions*
>
>    ***TODO***: *Consider adding a comment or tip box*
>
>    > <comment-title> short description </comment-title>
>    >
>    > A comment about the tool or something else. This box can also be in the main text
>    {: .comment}
>
{: .hands_on}

***TODO***: *Consider adding a question to test the learners understanding of the previous exercise*

> <question-title></question-title>
>
> 1. Question1?
> 2. Question2?
>
> > <solution-title></solution-title>
> >
> > 1. Answer for question1
> > 2. Answer for question2
> >
> {: .solution}
>
{: .question}
***TODO***![ADD image](../../images/image_name "Legend of the image very detail (for blind people to be read to)")

## Re-arrange

To create the template, each step of the workflow had its own subsection.

***TODO***: *Re-arrange the generated subsections into sections or other subsections.
Consider merging some hands-on boxes to have a meaningful flow of the analyses*

# Conclusion

Sum up the tutorial and the key takeaways here. We encourage adding an overview image of the
pipeline used.
