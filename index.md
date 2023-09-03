# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly from 3 to 4 PM ET. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRiTnsNRm0ojyXIbPVVe1iqi). The seminar is organized by the [Cornell Database Group](https://cornelldb.github.io/dbgrouphp/).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|9/5|Nikolaos Tziavelis, _Northeastern University_ | Efficient Ranked Access over Joins \[[Details](#talk-by-nikolaos-tziaveliss)\]
|9/12|
|9/19|
|9/26|Lin Ma, _University of Michigan_ | 
|10/03|Ana Klimovic , _ETH_|
|10/10| No talk: Fall break
|10/17|Michael Jungmair
|10/24|
|10/31|
|11/7|Lei Cao
|11/14|
|11/21|Alvin Cheung
|11/28|


# Talk Details

## Talk by Nikolaos Tziavelis


### Abstract
Join queries over multiple tables with many-to-many relationships (e.g., in graph analytics) can produce a huge output that is infeasible to compute. However, users may have particular preferences over the answers in the output, and may be interested in accessing only a small subset according to that ranking; either to retrieve the most important answers or the quantiles for a statistics summary. We show that for many such queries, access patterns, and ranking functions over the answers, ranked access can be performed efficiently, without first computing the output of the join. This is captured theoretically by non-trivial complexity guarantees and shown in practice with significant performance improvements over typical implementations in state-of-the-art database management systems (DBMSs) that sort the join output. Besides addressing fundamental questions regarding the limits of query processing, this work opens up unexplored possibilities for the design of DBMSs. We clearly demonstrate how existing systems fall short in handling ranking over joins efficiently, with our algorithms outperforming them by orders of magnitude.

Project Website: https://northeastern-datalab.github.io/anyk/

### Bio
Nikolaos (Nikos) Tziavelis is a 5th year PhD candidate at Northeastern University, advised by Mirek Riedewald and Wolfgang Gatterbauer, and before that, he received a Diploma in Electrical and Computer Engineering from the National Technical University of Athens. His research interests lie in novel algorithms for query processing, efficient data representations, and distributed computing. His work has been awarded with  a Google PhD fellowship, a VLDB 2023 PhD Workshop Best Paper Award, and a PODS 2021 “Best of” recognition.
https://ntzia.github.io/

