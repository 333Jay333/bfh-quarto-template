# README
---
This project offers a Quarto document template following the formatting requirements from the Bern University of Applied Sciences, School of Health Professions.

## Features

The project structure is designed to facilitate the creation of reproducible research. The main feature is a template for outputting a PDF file following the formatting requirements for written documents at the Bern University of Applied Sciences, School of Health Professions. In addition, a second template for outputting a Word document is also available. However, this does not match all the formatting requirements and is therefore mainly meant to facilitate collaboration with Word users.

## Usage

The templates are located in the [template](templates/) folder.

### PDF template
For exporting to pdf, copy the YAML header from [pdf-template.qmd](templates/pdf-template/pdf-template.qmd) into your own Quarto document.

Next, you will need to include the following files in the same folder that your Quarto document is located in:

- [apa.csl](templates/pdf-template/apa.csl)
- [header.tex](templates/pdf-template/header.tex)
- [references.bib](templates/pdf-template/references.bib)
- [remove_title.lua](templates/pdf-template/remove_title.lua)
- [titlepage.tex](templates/pdf-template/titlepage.tex)

Adjust the information in the placeholders at the top of [titlepage.tex](templates/pdf-template/titlepage.tex) according to your needs. If more detailed changes are needed, these can be added by commenting/uncommenting lines of the file. 

Once you have successfully set up your Quarto document and all the required files are in place, you can render your document and will receive a PDF file following the formatting guidelines.

### Word template

For exporting to pdf, copy the YAML header from [word-template.qmd](templates/word-template/word-template.qmd) into your own Quarto document.

Next, you will need to include the following files in the same folder that your Quarto document is located in:

- [apa.csl](templates/pdf-template/apa.csl)
- [reference.docx](templates/pdf-template/reference.docx)
- [references.bib](templates/pdf-template/references.bib)

### File structure

The project comes with a prepared file structure for research reproducibility. Feel free to adjust it according to your project's needs.

Below, a possible workflow is described:

1. Raw data (ideally in a `.csv` format) is imported into the [raw_data](raw_data/) folder
2. Inside the [scripts](scripts/) folder, the user creates an R script to clean the data and exports the results into the [clean_data](clean_data/) folder
3. The user creates a Quarto document for preparing his manuscript. At a later stage, different versions of the manuscript can be saved in the [manuscripts](manuscripts/) folder.
4. If needed, the user can export his plots and tables into the provided folders for easy access and further usage in research dissemination.

What advantages does such a file structure offer?

- Data analysis can easily be repeated: in case of a data entry error or more available data, the raw data can be replaced at a later stage. If variables were correctly used in the manuscript, all values will be updated accordingly, plots and tables can be redrawn and the user can save hours of painstaking work manually correcting every value in his manuscript.
- Product documentation: the whole process from data analysis to manuscript creation is clearly documented, allowing easy and accurate reproducibility of all steps of research.

## License
                        GNU GENERAL PUBLIC LICENSE
                          Version 3, 29 June 2007
     
     Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
     Everyone is permitted to copy and distribute verbatim copies
     of this license document, but changing it is not allowed.
