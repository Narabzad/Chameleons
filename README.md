# Chameleons
This repository contains the dataset related to ''MSMarco Chameleons: Challenging the MSMarco Leaderboard with Extremely Obstinate Queries'' resource paper.

In this work we find that while rankers have witnessed an impresive improvement in the oeprformance during the recent years, there are still a significant number of queries that
cannot be addressed by any of the state of the art neural rankers. We refer to these queries as obstinate queries because of their difficulty.
This means that regardless of the neural ranker, these queries will not see any performance improvements and the increase in overall
performance reported by the ranker are due to improvements on another selected subset of queries.We belive that careful treatintmenr on these queries will lead 
to the stable and consistent performance of neural rankers.

Further, we show the performance of SOTA rankers  on MSMARCO small dev set which contains 6980 queries in Table 1.




**Table 1. : MAP Performance of  the rankers on 50% hardest queries of the Chameleon datasets.**
| Variations          | Dataset Name          | Queries             |BM25   | DeepCT | DocT5Query | RepBert | ANCE   | TCT-Colbert |
|---------------------|-----------------------|---------------------|-------|--------|------------|---------|--------|-------------|
| Common in 6 rankers | Meller's <br> Chameleon    | Meller's queries    |0.0066 <br>(Run) | 0.0122 <br>(Run) | 0.0185 <br>(Run)    | 0.0212 <br>(Run)  | 0.0286 <br>(Run) | 0.0267 <br>(Run)     |
| Common in 5 rankers | Fischer's  <br>Chameleon   | Fischer's queries   |0.0215 <br>(Run) | 0.0240 <br>(Run) | 0.0403 <br>(Run)    | 0.0398 <br>(Run)  | 0.0546 <br>(Run) | 0.0462 <br>(Run)     |
| Common in 4 rankers | Outstalet's <br> Chameleon | Outstalet's queries |0.0392 <br>(Run)| 0.0400 <br>(Run)| 0.0660 <br>(Run)    | 0.0560 <br>(Run) | 0.0847 <br>(Run) | 0.0780  <br>(Run)    |

We made all these runs available in the [Chameleons Google drive](https://drive.google.com/drive/folders/1vj8YC6YcADiiS7DjqepDMC9F_uaRneJC?usp=sharing). 

