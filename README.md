DS 202 Final Project
================

<!-- README.md is generated from README.Rmd. Please edit the README.Rmd file -->

This repository serves as a starter repo for your final project, and
this Rmd is supposed to serve as a starter file for your project report.

## Part I: Repo Structure

The structure sketched out below is an idea of what your repository
might look like. You can use it as a starting base and change according
to your needs. But think about the changes that you make!

    -- code
    |   |   -- any R scripts you need but don't want to include directly in the write-up
    -- data
    |   |   -- csv files (cleaned data)
    -- data-raw
    |   |   -- raw data files 
    |   |   -- data description files, origin
    |   |   -- Codebook
    -- final-project.Rmd
    -- images  # only images that are not created by the Rmd
    -- LICENSE
    -- README.md
    -- README.Rmd
    -- README_files # folder with files created during the knitting process

## Part II: Project report

# Consumer Spending in Iowa

Authors: Kylie Tauke, Jordyn Reimer, and Akshat Valse

## Abstract (TL;DR)

The data explored in this project details estimates on consumer spending
in the state of Iowa. We wanted to identify what consumers spend the
most on and how it has changed throughout the years. The data comes from
the U.S. Bureau of Economic Analysis.

ADD FINDINGS LATER

# Motivation

We wanted to examine consumer spending in Iowa. Not only were we curious
about the distribution of spending among different categories of goods,
but this is also valuable information for any business providing a good
or service.

At the end of the Intro, write a sentence describing what each of the
(result) sections is about, e.g. in section [Results 1](#results-1) we
show the relationship between XXX and YYY, section [Results
2](#results-2) also considers the effect of variable ZZZ. … Finally we
conclude with a quick summary of our findings and potential follow-up
work in section [Conclusions](#conclusions).

# Quick Data Summary

- The data was cleaned by standardizing column names, extracting
  simplified categories from text fields, splitting composite IDs into
  separate columns, converting data types (dates, numbers), normalizing
  units to millions, and removing duplicates.

What are the variables that you will be using in the main part of the
report? What are their ranges? You could include a table with variable
names, a short explanation, and (very broad) summary statistics.

- The primary variables that will be used will be consumption_category,
  reported_year, and value_millions. Some summaries and preliminary
  plots are provided below.

<!-- -->

    ##     row_id           fips_code           data_year    series_code       
    ##  Length:1296        Length:1296        Min.   :1997   Length:1296       
    ##  Class :character   Class :character   1st Qu.:2003   Class :character  
    ##  Mode  :character   Mode  :character   Median :2010   Mode  :character  
    ##                                        Mean   :2010                     
    ##                                        3rd Qu.:2017                     
    ##                                        Max.   :2023                     
    ##   frequency         variable_code        variable         consumption_category
    ##  Length:1296        Length:1296        Length:1296        Length:1296         
    ##  Class :character   Class :character   Class :character   Class :character    
    ##  Mode  :character   Mode  :character   Mode  :character   Mode  :character    
    ##                                                                               
    ##                                                                               
    ##                                                                               
    ##      value        variable_unit           date            reported_year 
    ##  Min.   :   297   Length:1296        Min.   :1997-12-31   Min.   :1997  
    ##  1st Qu.:  1905   Class :character   1st Qu.:2003-12-31   1st Qu.:2003  
    ##  Median :  3959   Mode  :character   Median :2010-12-31   Median :2010  
    ##  Mean   : 10928                      Mean   :2010-12-31   Mean   :2010  
    ##  3rd Qu.: 10263                      3rd Qu.:2017-12-31   3rd Qu.:2017  
    ##  Max.   :153400                      Max.   :2023-12-31   Max.   :2023  
    ##    prior_year     category         expenditure_type       unit          
    ##  Min.   :1996   Length:1296        Length:1296        Length:1296       
    ##  1st Qu.:2002   Class :character   Class :character   Class :character  
    ##  Median :2009   Mode  :character   Mode  :character   Mode  :character  
    ##  Mean   :2009                                                           
    ##  3rd Qu.:2016                                                           
    ##  Max.   :2022                                                           
    ##  value_millions    
    ##  Min.   :     0.0  
    ##  1st Qu.:     0.0  
    ##  Median :   428.8  
    ##  Mean   :  8248.7  
    ##  3rd Qu.:  6952.5  
    ##  Max.   :153399.7

![](README_files/figure-gfm/summaries-1.png)<!-- -->![](README_files/figure-gfm/summaries-2.png)<!-- -->

# Results

Each line of exploration is supposed to be featured in one of the
Results sections. Make sure to change to more interesting section
headers!

## Results 1

In your write-up, make sure to refer to all of the figures you create.
You can include a hyperlink to the [scatterplot](#fig:scatterplot) by
using the name of the code chunk (make sure, to give each code chunk a
different name). In your markdown document you can create this link
either by calling the function `chunkref` with the name of the code
chunk in quotes, i.e. [scatterplot](#fig:scatterplot) or by using the
markdown expression `[scatterplot](#fig:scatterplot)`. Similarly, we can
refer to the [2nd scatterplot](#fig:2nd%20scatterplot). Note that the
figure captions appear above the figures - this saves us from having to
scroll up after following the link.

<p>
<small><strong><a name='fig:scatterplot'>scatterplot</a></strong>: This
is the figure caption. Make sure to use the description we practised in
the homework: first sentence describes structure of the plot, second
sentence describes main finding, third sentence describes
outliers/follow-up.</small>
</p>

<figure>
<img src="README_files/figure-gfm/scatterplot-1.png"
alt="This is the figure caption. Make sure to use the description we practised in the homework: first sentence describes structure of the plot, second sentence describes main finding, third sentence describes outliers/follow-up." />
<figcaption aria-hidden="true">This is the figure caption. Make sure to
use the description we practised in the homework: first sentence
describes structure of the plot, second sentence describes main finding,
third sentence describes outliers/follow-up.</figcaption>
</figure>

<p>
<small><strong><a name='fig:2nd scatterplot'>2nd
scatterplot</a></strong>: This is the figure caption. Make sure to use
the description we practised in the homework: first sentence describes
structure of the plot, second sentence describes main finding, third
sentence describes outliers/follow-up.</small>
</p>

<figure>
<img src="README_files/figure-gfm/2nd%20scatterplot-1.png"
alt="This is the figure caption. Make sure to use the description we practised in the homework: first sentence describes structure of the plot, second sentence describes main finding, third sentence describes outliers/follow-up." />
<figcaption aria-hidden="true">This is the figure caption. Make sure to
use the description we practised in the homework: first sentence
describes structure of the plot, second sentence describes main finding,
third sentence describes outliers/follow-up.</figcaption>
</figure>

Additionally, you can also refer to different sections in your writeup
by using anchors (links) to section headers. Here, we are referring to
subsection [Results 3](#results-3). The code for that is `[Results 3]`.

## Results 2

## Results 3

…

# Conclusions

Give a quick summary of your work. Here is the place to be a bit
critical and discuss potential limitations. Add a sentence on what else
you would have liked to include in your data exploration if you had more
time or more members in your team.

## Data source

Where does the data come from, who owns the data? Where are all the
scripts that you need to clean the data?

## References

List all resources you used.
