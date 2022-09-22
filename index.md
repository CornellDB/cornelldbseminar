# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly on Tuesdays from 3 to 4 PM ET. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRhWH5G7GJdKKirILbO56Mmv). The seminar is organized by the [Cornell Database Group](https://itrummer.github.io/dbgrouphp/).

Talk details and recordings from Spring 2022 can be found [here](/cornelldbseminar/spring22.html).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|8/23|Immanuel Trummer, _Cornell University_|Intro|
|8/30|||
|9/6|||
|9/13|Immanuel Trummer, _Cornell University_||
|9/20|Immanuel Trummer, _Cornell University_||
|9/27|Aecio Santos, _New York University_|Sketching Methods for Efficient Correlated Dataset Search \[[Details](#talk-by-aecio-santos)\]|
|10/4|Hung Ngo, _RelationalAI_|Query Optimization for Worst-case Optimal Joins|
|10/11|(Break)||
|10/18|Ippokratis Pandis, _Amazon_|Reinventing Amazon Redshift|
|10/25|Raul Castro Fernandez, _University of Chicago_|Data Pricing|
|11/1|Subarna Chatterjee, _Harvard University_|Self-Designing Key Value Stores|
|11/8|Arun Kumar, _University of California San Diego_|TBD|
|11/15|Arnab Nandi, _Ohio State University_|TBD|
|11/22|_MongoDB_||
|11/29|Matthias Boehm, _TU Berlin_||

# Talk Details

## Talk by Aecio Santos

### Abstract

Dataset search is emerging as a critical capability in both research and industry: it has spurred many novel applications such as data augmentation for enriching data analyses and improving machine learning models. In this talk, we present our recent work that explores a new class of dataset search queries that uncovers data relationships in large table collections. In particular, we focus on join-correlation queries: given an input query table, find the top-k tables that are both joinable with it and contain columns strongly correlated with a column in the query table. Unfortunately, a naïve approach to evaluate these queries, which first finds joinable tables and then explicitly materializes joins and computes correlations between the query and all discovered tables, is prohibitively expensive. To solve this problem, we 1) present novel data sketching methods that enable the construction of an index for a large number of tables and that provide accurate estimates for join-correlation queries, and 2) explore different indexing and scoring strategies that effectively retrieve and rank the query results based on how well the columns are correlated with the query.

### Bio

Aécio Santos is a Research Engineer in the Visualization, Imaging, and Data Analysis (VIDA) group at New York University (NYU). He received a Master's Degree in Computer Science from the Federal University of Minas Gerais (in Brazil) and is currently a part-time Ph.D. candidate at New York University under the supervision of Prof. Juliana Freire. Over the years, he has worked, both in academia and industry, on a wide range of problems related to web crawling, news recommendation and classification, automated machine learning, and dataset search. He has served as a reviewer and has published papers at multiple premier data management and information retrieval conferences and journals such as VLDB, SIGMOD, WWW, WSDM, SIGIR, and CIKM.
