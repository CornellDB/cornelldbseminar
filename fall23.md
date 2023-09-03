# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly from 3 to 4 PM ET. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRiTnsNRm0ojyXIbPVVe1iqi). The seminar is organized by the [Cornell Database Group](https://cornelldb.github.io/dbgrouphp/).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|2/7|Manos Athanassoulis, _Boston University_ | (A Prelude to) Building Robust LSM-based Key-Value Stores \[[Details](#talk-by-manos-athanassoulis)\] \[[Video](https://t.co/ywgitHApbY)\]|
|2/14|Rolando Garcia Sanchez, _UC Berkeley_ | FLOR: Managing the Infinite Virtual Metadata of Model Training \[[Details](#talk-by-rolando-garcia-sanchez)\] \[[Video](https://youtu.be/gAhqAHnJme0)\]|
|2/21| Immanuel Trummer, _Cornell University_| Towards Tuning Tools that "Read" the Manual \[[Details](#talk-by-immanuel-trummer)\] \[[Video](https://youtu.be/rICyXhjyqp8)\]|
|2/28| (Break) | |
|3/7|Carsten Binnig, _TU Darmstadt_ | Learned DBMS Components 2.0: From Workload-Driven to Zero-Shot Learning \[[Details](#talk-by-carsten-binnig)\] \[[Video](https://youtu.be/7Ws_Ms4wVcc)\]|
|3/14|Ibrahim Sabek, _MIT_ | LSched: A Workload-Aware Learned Query Scheduler for Analytical Database Systems \[[Details](#talk-by-ibrahim-sabek)\] \[[Video](https://youtu.be/uiMdErKz_rk)\]|
|3/21|Volker Markl, _TU Berlin_ | Mosaics of Big Data: Database Systems and Information Management – Trends and a Vision \[[Details](#talk-by-volker-markl)\] \[[Video](https://youtu.be/Y0qq1Di-Qvc)\]|
|3/28|Davide Mottin, _Aarhus University_ | Cleaning Knowledge Graphs with Little Effort \[[Details](#talk-by-davide-mottin)\] \[[Video](https://youtu.be/l1O9EFmAXaM)\]|
|4/4|(Break)| |
|4/11|Laurel Orr, _Stanford University_ | Incremental Entity Embedding Maintenance in Foundation Model Ecosystems \[[Details](#talk-by-laurel-orr)\] \[[Video](https://youtu.be/IgKz5Rnjnvk)\] |
|4/18|Angelos-Christos Anadiotis, _Ecole Polytechnique_| Pursue of Conflicts of Interest Across Heterogeneous Data \[[Details](#talk-by-angelos-christos-anadiotis)\] \[[Video](https://youtu.be/Qwc68qj4bK8)\] |
|4/25|Eugene Wu, _Columbia University_| Systems for Human Data Interaction \[[Details](#talk-by-eugene-wu)\] \[[Video](https://youtu.be/85AtsmN2Sm4)\] |
|5/2|Roger Waleffe, _University of Wisconsin-Madison_| Training Graph Neural Networks over Billion-Scale Graphs on a Single Machine \[[Details](#talk-by-roger-waleffe)\] \[[Video](https://youtu.be/BVDQauRb4gQ)\]|
|5/9|Joe Hellerstein, _UC Berkeley_| A Programmable Cloud: CALM Foundations and Open Challenges \[[Details](#talk-by-joe-hellerstein)\] \[[Video](https://youtu.be/HqyaFLcT3HQ)\]|

# Talk Details

## Talk by Nikolaos Tziavelis


### Abstract
Join queries over multiple tables with many-to-many relationships (e.g., in graph analytics) can produce a huge output that is infeasible to compute. However, users may have particular preferences over the answers in the output, and may be interested in accessing only a small subset according to that ranking; either to retrieve the most important answers or the quantiles for a statistics summary. We show that for many such queries, access patterns, and ranking functions over the answers, ranked access can be performed efficiently, without first computing the output of the join. This is captured theoretically by non-trivial complexity guarantees and shown in practice with significant performance improvements over typical implementations in state-of-the-art database management systems (DBMSs) that sort the join output. Besides addressing fundamental questions regarding the limits of query processing, this work opens up unexplored possibilities for the design of DBMSs. We clearly demonstrate how existing systems fall short in handling ranking over joins efficiently, with our algorithms outperforming them by orders of magnitude.

Project Website: https://northeastern-datalab.github.io/anyk/

### Bio
Nikolaos (Nikos) Tziavelis is a 5th year PhD candidate at Northeastern University, advised by Mirek Riedewald and Wolfgang Gatterbauer, and before that, he received a Diploma in Electrical and Computer Engineering from the National Technical University of Athens. His research interests lie in novel algorithms for query processing, efficient data representations, and distributed computing. His work has been awarded with  a Google PhD fellowship, a VLDB 2023 PhD Workshop Best Paper Award, and a PODS 2021 “Best of” recognition.
https://ntzia.github.io/

