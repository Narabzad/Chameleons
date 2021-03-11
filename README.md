# Chameleons
This repository contains the dataset related to ''MSMarco Chameleons: Challenging the MSMarco Leaderboard with Extremely Obstinate Queries'' resource paper.

In this work we find that while rankers have witnessed an impresive improvement in the oeprformance during the recent years, there are still a significant number of queries that
cannot be addressed by any of the state of the art neural rankers. We refer to these queries as obstinate queries because of their difficulty.
This means that regardless of the neural ranker, these queries will not see any performance improvements and the increase in overall
performance reported by the ranker are due to improvements on another selected subset of queries.We belive that careful treatintmenr on these queries will lead 
to the stable and consistent performance of neural rankers.

Further, we show the performance of SOTA rankers  on MSMARCO small dev set which contains 6980 queries in Table 1.




**Table 1. : MAP Performance of  the rankers on 50% hardest queries of the Chameleon datasets.**
| Variations          | Dataset Name          | BM25   | DeepCT | DocT5Query | RepBert | ANCE   | TCT-Colbert |
|---------------------|-----------------------|--------|--------|------------|---------|--------|-------------|
| Common in 6 rankers | Meller's Chameleon    | 0.0066 <br>(Q, R ) | 0.0122 | 0.0185     | 0.0212  | 0.0286 | 0.0267      |
| Common in 5 rankers | Fischer's Chameleon   | 0.0215 | 0.0240 | 0.0403     | 0.0398  | 0.0546 | 0.0462      |
| Common in 4 rankers | Outstalet's Chameleon | 0.0392 | 0.0400 | 0.0660     | 0.0560  | 0.0847 | 0.0780      |

We made all these runs available in the [Chameleons Google drive](https://drive.google.com/drive/folders/1vj8YC6YcADiiS7DjqepDMC9F_uaRneJC?usp=sharing). 

