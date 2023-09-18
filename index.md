# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly from 3 to 4 PM ET. All talks by external speakers are **public** and can be attended via Zoom (email [Immanuel Trummer](https://itrummer.github.io/)/[Sainyam Galhotra](https://sainyamgalhotra.com) for the link). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLNBDQderXUGp-zvSkzHh1sT2YJ2M-fxx4). The seminar is organized by the [Cornell Database Group](https://cornelldb.github.io/dbgrouphp/).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|9/5|[Nikolaos Tziavelis](https://ntzia.github.io/), _Northeastern University_ | Efficient Ranked Access over Joins \[[Details](#talk-by-nikolaos-tziaveliss)\]
|9/12|[Immanuel Trummer](www.itrummer.org), _Cornell University_ | Approximate Query Processing|
|9/19|[Neha Makhija](https://nehamakhija.github.io/), _Northeastern University_  | An Unified Approach For Reverse Data Management 
|9/26|[Lin Ma](https://linmagit.github.io/), _University of Michigan_ | 
|10/03|[Ana Klimovic](https://anakli.inf.ethz.ch/), _ETH_ |
|10/10| No talk: Fall break
|10/17|[Michael Jungmair](https://db.in.tum.de/~jungmair/), _TUM_ |
|10/24|
|10/31|
|11/7|[Lei Cao](https://www2.cs.arizona.edu/~caolei/), _University of Arizona_ |
|11/14|
|11/21|[Alvin Cheung](https://people.eecs.berkeley.edu/~akcheung/), _UC Berkeley_ |
|11/28|


# Talk Details

## Talk by Nikolaos Tziavelis


### Abstract
Join queries over multiple tables with many-to-many relationships (e.g., in graph analytics) can produce a huge output that is infeasible to compute. However, users may have particular preferences over the answers in the output, and may be interested in accessing only a small subset according to that ranking; either to retrieve the most important answers or the quantiles for a statistics summary. We show that for many such queries, access patterns, and ranking functions over the answers, ranked access can be performed efficiently, without first computing the output of the join. This is captured theoretically by non-trivial complexity guarantees and shown in practice with significant performance improvements over typical implementations in state-of-the-art database management systems (DBMSs) that sort the join output. Besides addressing fundamental questions regarding the limits of query processing, this work opens up unexplored possibilities for the design of DBMSs. We clearly demonstrate how existing systems fall short in handling ranking over joins efficiently, with our algorithms outperforming them by orders of magnitude.

Project Website: https://northeastern-datalab.github.io/anyk/

### Bio
Nikolaos (Nikos) Tziavelis is a 5th year PhD candidate at Northeastern University, advised by Mirek Riedewald and Wolfgang Gatterbauer, and before that, he received a Diploma in Electrical and Computer Engineering from the National Technical University of Athens. His research interests lie in novel algorithms for query processing, efficient data representations, and distributed computing. His work has been awarded with  a Google PhD fellowship, a VLDB 2023 PhD Workshop Best Paper Award, and a PODS 2021 “Best of” recognition.
https://ntzia.github.io/

## Talk by Neha Makhija

Title: An Unified Approach For Reverse Data Management

### Abstract: 
Reverse data management generalizes problems that perform actions on the input data, on behalf of desired outcomes in the output data - including problems such as view maintenance, deletion propagation, and interventions for fairness. A long-open question is determining those conjunctive queries (CQs) for which these problems can be solved in guaranteed PTIME. We focus on the problem of resilience, a key algorithmic problem that underlies the various forms of reverse data management. It asks "What is the minimal number of tuples to delete from a database in order to remove all answers from a query?"

We discuss a novel approach for solving reverse data management problems: instead of creating dedicated algorithms for easy (PTIME) and hard (NP-complete) cases, we suggest using a unified algorithm that is guaranteed to terminate in PTIME for all easy cases. Our algorithm is also unified in that it can solve both previously studied restrictions (e.g., self-join-free CQs under set semantics that allow a PTIME solution) and new cases (e.g., all CQs under set or bag semantics). Our approach opens up the door to new variants and new fine-grained analysis: 1) It also works under bag semantics and we give the first dichotomy result for bags semantics in the problem space. 2) We give a more fine-grained analysis of the complexity of causal responsibility. 3) We recover easy instances for generally hard queries, such as instances with read-once provenance and instances that become easy because of Functional Dependencies in the data. 4) We solve an open conjecture from PODS 2020 regarding an unified hardness criterion, and use it to automatically find hardness proofs for queries whose complexity were previously unknown. 5) Experiments confirm that our results indeed predict the asymptotic running times, and that our universal ILP encoding is at times even faster to solve for the PTIME cases than a prior proposed dedicated flow algorithm.


Related Paper: 
A Unified Approach for Resilience and Causal Responsibility with Integer Linear Programming (ILP) and LP Relaxations. N Makhija, W Gatterbauer - arXiv preprint arXiv:2212.08898, 2022 (https://arxiv.org/abs/2212.08898) [To appear SIGMOD 2024]

Project Page: https://northeastern-datalab.github.io/unified-reverse-data-management/ 
