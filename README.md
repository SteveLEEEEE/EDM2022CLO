# Dataset and source code for [Classification of Learning Objective](./Classification_of_Learning_Objectives_preprint.pdf) (EDM2022)
For EDM2022 paper "Automatic Classification of Learning Objectives Based on Bloom’s Taxonomy"

## 1. How the Dataset was Collected
We collected 21,380 learning objectives publicly available from 5,558 courses provided by the 10 faculties at an Australian university in 2021. To collect the data, we developed a web scraper using Python to automatically parse the content of the available course web pages to obtain learning objectives of a course. 


## 2. Files in the Dataset
The [data](./data/sample_full.csv) contains textual learning objectives as well as the humanly annotated labels in binary format for different Bloom's taxonomy levels. We also generate the [LIWC features](<./data/LIWC2015 Results (Learning_outcome.csv).csv>) using LIWC2015 for the machine learning experiments in our project.