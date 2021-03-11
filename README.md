# Chameleons
This repository contains the dataset related to ''MSMarco Chameleons: Challenging the MSMarco Leaderboard with Extremely Obstinate Queries'' resource paper.

In this work we find that while rankers have witnessed an impresive improvement in the oeprformance during the recent years, there are still a significant number of queries that
cannot be addressed by any of the state of the art neural rankers. We refer to these queries as obstinate queries because of their difficulty.
This means that regardless of the neural ranker, these queries will not see any performance improvements and the increase in overall
performance reported by the ranker are due to improvements on another selected subset of queries. We believe that careful treatment on these queries will lead 
to the a more stable and consistent performance of neural rankers across all the queries.

We investigate the performance of SOTA rankers  on MSMARCO small dev set  which contains 6980 queries. We noticed no matter
which baseline method is considered, whether it be a traditional BM25 ranker or a complex neural ranker, there is a noticeable number
of queries for which the rankers are unable to return any reasonable ranking. Further there is a noticeable number of poorly performed queries that are in common acroos all the rankers. Table 1 illustrates the performance of  the 'difficult' queries qhich are among least 50% performance of each baseline and are in common in 4,5 and 6 of SOTA rankers  

**Table 1. : MAP Performance of  the rankers on 50% hardest queries of the Chameleon datasets.**
| Variations          | Dataset Name          | Queries             |BM25   | DeepCT | DocT5Query | RepBert | ANCE   | TCT-Colbert |
|---------------------|-----------------------|---------------------|-------|--------|------------|---------|--------|-------------|
| Common in  <br>**6** rankers | Meller's <br> Chameleon    | [Meller's queries](https://github.com/Narabzad/Chameleons/tree/master/datasets/Meller(common6)) <br>(1693)   |0.0066 <br>(Run) | 0.0122 <br>(Run) | 0.0185 <br>(Run)    | 0.0212 <br>(Run)  | 0.0286 <br>(Run) | 0.0267 <br>(Run)     |
| Common in  <br>**5** rankers | Fischer's  <br>Chameleon   | [Fischer's queries](https://github.com/Narabzad/Chameleons/tree/master/datasets/Fischer(common5))<br>(2473)    |0.0215 <br>(Run) | 0.0240 <br>(Run) | 0.0403 <br>(Run)    | 0.0398 <br>(Run)  | 0.0546 <br>(Run) | 0.0462 <br>(Run)     |
| Common in  <br>**4** rankers | Outstalet's <br> Chameleon | [Outstalet's queries](https://github.com/Narabzad/Chameleons/tree/master/datasets/Outstalet(common4))<br>(3119)  |0.0392 <br>[(Run)](https://drive.google.com/file/d/1manHBekmogC1gcpgQ2hrksjZNqXwV5PK/view?usp=sharing)| 0.0400 <br>[(Run)](https://drive.google.com/file/d/1GNsjimgEaF15FSKVv19xVVBG-Nbmkp1d/view?usp=sharing)| 0.0660 <br>[(Run)](https://drive.google.com/file/d/1FCFvWYFngrK6s9zXQ-hI8a0zBAuAT0Vn/view?usp=sharing)    | 0.0560 <br>[(Run)](https://drive.google.com/file/d/1MORyZyZYME9ZREvAEcGBjyeoDlqjcIc7/view?usp=sharing) | 0.0847 <br>[(Run)](https://drive.google.com/file/d/1Ag-gh3ti9MLpasLI8iwngsns7y6IxMf-/view?usp=sharing) | 0.0780  <br>[(Run)](https://drive.google.com/file/d/1-_KDsTRtrJAfw34UlJpxBNTJjPtXDsYJ/view?usp=sharing)    |

We made all the runs available in the [Chameleons Google drive](https://drive.google.com/drive/folders/1vj8YC6YcADiiS7DjqepDMC9F_uaRneJC?usp=sharing). 

Furthermore, given the literature has reported that hard queries can often be due to issues such as vocabulary mismatch, and
hence can be improved through query reformulation, we report the performance of several strong query reformulation 
techniques on the MSMarco Chameleons dataset and show that such queries remain stubborn and do not report noticeable performance
improvements even after systematic reformulation.
The expanded queries can be found [here](https://github.com/Narabzad/Chameleons/tree/master/expanded%20Queries).
