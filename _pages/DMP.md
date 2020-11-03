---
title: "iEco Lab DMP Quick Guide"
date: "Last Updated: November 11, 2020"
permalink: /DMP/
header: 
   image: "/images/iecolab_logo_v2_1_banner_v1_0.png"
output:
  html_document:
    toc: TRUE
    toc_depth: 2
---

This is a quick guide for the iEco Lab Data Management Plan. For the full Data Management plan visit the lab's [website](https://www.iecolab.org/) (full data management plant under construction)

<br>

“_The goal is to turn data into information, and information into insight_.” – Carly Fiorina

“_It is a capital mistake to theorize before one has data_.” – Sherlock Holmes

“_Without data, you are just another person with an opinion_.” – W. Edwards Deming

“_Data is a precious thing and will last longer than the systems themselves_.” – Sir Tim Berners-Lee

<br>

***

# Purpose

Data management is project management, and a data management plan (DMP) is used to standardize data formatting, naming, organization and storing so that data are accessible, understandable and reproducible. Data are any information collected or created pertaining to a research project (e.g. data tables, analysis scripts, figures, manuscripts, and reference libraries). 

The definition of a research project depends on the individual project. Research projects are defined by project leads in collaboration with a PI(s) . An easy guideline to follow is to use the data to define what is a project and what is a subproject. For instance, if you are using data that will be incorporated into many papers, then you would not want a project for each individual paper because then you would have multiple copies of data and keeping good data management practices across all copies would be difficult. In that case each paper would be a subproject under a larger project as defined by the data.

<br>

***

# Updating

The DMP is reviewed regularly because each time a new project is started, the DMP should be referenced. It is updated based on input from iEcoLab team members who are actively managing and creating research projects. All iEcoLab members are encouraged to read this document and discuss with their PI(s) if they prefer to follow a different DMP for one project.

<br>

***

# Sections

## Filesystem

In this section, guidelines for how to organize, name, and document your files in a directory are outlined.

### File Organization:

* **Each project should have a separate folder with at least four subfolders: ‘data’, ‘manuscripts’, ‘references’, and a R project folder**

<br>

### File Naming:

* **File names should be easy to understand, give information about the data, and be consistent**

<br>

The iEco Lab file naming convention is:

\<Project Name\>\_\<Data Type\>\_\<Author Initials\>\_\<Version\>

Naming Conventions for other file types are in the below table.

| File Type | Convention |
| ----------- | ----------- |
| Base Naming Convention | \<Project Name\>\_\<Data Type\>\_\<Author Initials\>\_\<Version\> |
| Audio-Visual Files | \<Project Name\>\_\<Data Type\>\_\<Date\>\_\<Version\> |
| Spatial Data | \<Project Name\>\_\<Data Type\>\_\<Projection\>\_\<Version\> |

<br>

### File Documentation:

* **Documentation files describe the data by stating their authors, methods, editing, and attributes**

* **The documentation files include Readme, Changelog, and Metadata files**

  + Readme - Describes the data

  + Changelog - Describes any changes you made to the various data versions

  + Metadata - Describes the data in each column of the data table

* **Documentation files should be save as text files**

  + The Metadata can be saved as a CSV

<br>

Naming Conventions for these types of files are:

| Document Type | Naming Convention |
| ----------- | ----------- |
| Meta Data	| \<Data File Name\>\_METADATA
| Readme Files | \<Project Name\>\_(0)\_README
| Project Changelog Files	| \<Project Name\>\_(0)\_CHANGELOG
| Individual Changelog Files | \<Data File Name\>\_CHANGELOG
| Individual Readme Files	| \<Data File Name\>\_README

<br>

### Version Control:

* **Data version control should be done manually by adding the version at the end of the filename**

* **At least three versions of the data are required: raw, v0, and final**

<br>

***

## Data

### Data Collection:

In this section, guidelines for how field and laboratory data should be collected are described. These guidelines are not for the actual methods and techniques of generating the data but rather how to get data from the field to a data file on a computer. 

<br>

#### Field Data Collection:

* **Data should be recorded with dark pen and never erased or scratched out**

<br>

#### Lab Data Collection

* **Data collected in the lab should kept together and recorded in dark ink**

<br>

Key points in keeping a Lab Notebook:

1.	Neat and legible handwriting in dark ink; not pencil if able

2.	Procedure/Study title and purpose clearly stated

3.	Methods described clearly and succinctly, with errors and steps taken to correct them

4.	Calculations performed neatly showing intermediate steps

5.	Errors crossed out with a single line, initialed, and briefly explained

6.	All pages dated at the top and numbered at the bottom

<br>

#### Data Transcription

* **Digitize and back up data within a week after collection**

* **If multiple people are transcribing data, then they should each be working with separate spreadsheets**

  + This different spreadsheets are then compiled by the Data Manager

<br>

#### Quality Control During Transcription

* **Spreadsheets should resemble field data sheets as much as possible**

  + The spreadsheets are then formatted by the Data Manager
  
* **Use column rules or data entry forms for transcription quality control**

<br>

#### Data Mining

* **Work from master source list and compile and backup regularly**

<br>

### Data Formatting

This section is aimed at providing guidelines for how to build and format data tables so that they are easily manipulated, edited, analyzed, and most importantly understood. In addition, we will discuss the proper formatting of other types of data as well such as spatial and audio-visual data. The formatting outlined in this section should be done before the final version of the data.

<br>

#### Data Tables
* **Data tables should be saved as CSV files and be in long format**

* **Column headers are required, should be consistent, and easy to understand**

* **All text should be formatted consistently with dates in the YYYY-MM-DD format**

* **All cells should have values and if a value is missing then an NA should be entered**

<br>

#### Spatial Data

* **Spatial data should be a CSV, shapefile, GeoTIFF, or netCDF file depending on the data type**

<br>

#### Audio-Visual Data

<br>

* **Avoid proprietary formats and include data information in the recording or picture file**

<br>

### Data Backup:

* **Data should be backed-up weekly using the 3-2-1 strategy**

* **Data should ideally be backed up weekly and at least monthly**

<br>

### Data Storage and Sharing 

* **Final data storage should be on an online data repository**

* **Data sharing permissions is determined by the project lead and the PI(s)**

<br>

## Reference Libraries 

* **Reference libraries should be created through Zotero. Contact Dr. Matthew R. Helmus for Zotero access**

* If you cannot use Zotero then you should add a 'references' folder and follow the following naming convention.

\<Author(s)\>\_\<Year\>["Brief Description"]

<br>

## Project Packaging

When organizing your analyses for a research project, it's important to maximize two aspects: reproducibility and ease of sharing. This will make the life of your collaborators, and crucially the life of "future you", much easier. R packages provide a great tool to create collaborative and reproducible code. An R package bundles together the data your project requires, custom-made functions that can be used throughout your code, vignettes that describe your analyses step-by-step, and a thorough documentation that helps you and others to reproduce your analyses in the future. In practice, creating an R package boils down to 1) organizing your project folders and files in a clever and consistent way, and 2) documenting thoroughly your steps and the tools you use.

Guidelines for creating a project package can be found [HERE](workflow.rmd)

<br>

# Further Resources 

* Borer, E.T., Seabloom, E.W., Jones, M.B. and Schildhauer, M., 2009. Some simple guidelines for effective data management. The Bulletin of the Ecological Society of America, 90(2), pp.205-214. [LINK](https://esajournals.onlinelibrary.wiley.com/doi/full/10.1890/0012-9623-90.2.205)

* Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L. and Teal, T.K., 2017. Good enough practices in scientific computing. PLoS computational biology, 13(6). [LINK](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)

* [Guide to Reproducible Code](https://www.britishecologicalsociety.org/wp-content/uploads/2017/12/guide-to-reproducible-code.pdf)

* [Stanford Guide to the Best Data Management Practices](https://library.stanford.edu/research/data-management-services/data-best-practices)
