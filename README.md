# Replication of Suk and Mudita's 2023 Experiment on Donation Collection Methods

This is the documentation of a replication effort of Dr. Kwanho Suk and Dr. Triza Mudita's study, *Effects of donation collection methods on donation amount: Nudging donation for the cause and overhead.* I and three others replicate the second experiment described in this article, which found that participants donate more money to a hypothetical charity when asked to donate to a charity's overhead expenses first and advertised cause second, as opposed to the other way around. However, oue results failed to find this same effect, indicating a more complicated relationship.

## Project Overview

This repository documenting the entirety of the replication effort consists of a few major components, listed below.

### Data

This is the data that we collected. All of it is fully anonymized with no risk of Personalliy Identifiable Information (PII) leaking. I include data that was used during our first and second pilot studies in [pilotdata_a.csv](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/data/pilotdata_a.csv) and [pilotdata_b.csv](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/data/pilotdata_b.csv). Our raw sample data that was used for our calculations is included in [sampledata.csv](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/data/sampledata.csv), and our cleaned sample data that was edited to be remove JSON formatting, in order to be more legible, and filtered based on comprehension checks, so that only serious responses are used, is included in [filteredsampledata.csv](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/data/filteredsampledata.csv).

### Original Paper

The [original 2023 paper](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/original_paper.pdf) by Dr. Suk and Dr. Mudita is included for reference. You can also find it on [Wiley online library](https://onlinelibrary.wiley.com/doi/abs/10.1002/mar.21781). We specifically replicated **Study 2** from the original paper.

### Website

We utilized a custom website to host the survey that was used to collect our data. This website was hosted on the popular crowdworking website, Prolific, where we worked with online participants to get our results. To review our methodology, you can view the [.html code](https://github.com/willdemelo/Replication_Study_Suk2023/blob/main/website/index.html), or take the survey yourself [here](https://willdemelo.github.io/Replication_Study_Suk2023/website/). Notable features of this website include the usage of jsPysch plugins to create our questions and general infrastructure, restrictions we placed on participants' answering (for instance, that they must answer to move forward, and cannot put in the wrong kind of answer) as well as the datapipe that takes raw data from the survey and sends it to our public repository at the [Open Science Framework](https://osf.io/jzx7e/).

## Resources
- **Editor Used:** RStudio
- **R Version:** R 4.4.1

### Quarto
  This writeup was produced as a Quarto Markdown (.qmd) file, which allows for greater ease of rendering and publishing documents produced in RStudio.

### tidyverse
  tidyverse has essential libraries that form the backbone of this project's infrastructure, especially concerning loading the data (readr), data organization (dplyr, tidyr, stringr, tibble) and visualization (ggplot2).

### jsonlite
  jsonlite helps with removing the JSON formatting from our raw data. Because this data was transferred from our custom survey website to our OSF repository, and then loaded into R, the raw data is in JSON format, which must be removed for the analysis to progress.

## Bibliography
  Suk, K., & Mudita, T. (2023). Effects of donation collection methods on donation amount: Nudging donation for the cause and overhead. Psychology & Marketing, 40, 690–706. [https://doi.org/10.1002/mar.21781](https://doi.org/10.1002/mar.21781)
