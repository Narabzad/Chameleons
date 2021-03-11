# MSMarco Chameleons: Challenging the MSMarco Leaderboard with Extremely Obstinate Queries

In this work we find that while rankers have witnessed an impresive improvement in the oeprformance during the recent years, there are still a significant number of queries that
cannot be addressed by any of the state of the art neural rankers. We refer to these queries as obstinate queries because of their difficulty.
This means that regardless of the neural ranker, these queries will not see any performance improvements and the increase in overall
performance reported by the ranker are due to improvements on another selected subset of queries. We believe that careful treatment on these queries will lead 
to the a more stable and consistent performance of neural rankers across all the queries.

We investigate the performance of SOTA rankers  on MSMARCO small dev set  which contains 6980 queries. We noticed no matter
which baseline method is considered, whether it be a traditional BM25 ranker or a complex neural ranker, there is a noticeable number
of queries for which the rankers are unable to return any reasonable ranking. Further there is a noticeable number of poorly performed queries that are in common acroos all the rankers. Table 1 illustrates the performance of  the 'difficult' queries qhich are among least 50% performance of each baseline and are in common in 4,5 and 6 of SOTA rankers  

**Table 1. : MAP Performance of  the rankers on 50% hardest queries of the Chameleon datasets.**
| Variations          | Dataset Name           | Number of Queries            |BM25   | DeepCT | DocT5Query | RepBert | ANCE   | TCT-Colbert |
|---------------------|------------------------|------------|-------|--------|------------|---------|--------|-------------|
| Common in  <br>**6** rankers | [Meller's <br> Chameleon](https://github.com/Narabzad/Chameleons/tree/master/datasets/Meller(common6))   |1693   |0.0066 <br>[(Run)](https://drive.google.com/file/d/1TfRPhLhP2KxTVqERRUQ7_WJz3Gxa1HaW/view?usp=sharing) | 0.0122 <br>[(Run)](https://drive.google.com/file/d/1iRiLPUn-q6e533mAOKakKavTVv7dH5nI/view?usp=sharing) | 0.0185 <br>[(Run)](https://drive.google.com/file/d/14OyXbW2_TY0EnoCdKynRS6FaY8mqHUBm/view?usp=sharing)    | 0.0212 <br>[(Run)](https://drive.google.com/file/d/1k-z09WlRVDG8INkkwydPGL16Yq5RfUDE/view?usp=sharing)  | 0.0286 <br>[(Run)](https://drive.google.com/file/d/19UjCOSMSE7xpLKT2sQX0IggzIOA-6uEV/view?usp=sharing) | 0.0267 <br>[(Run)](https://drive.google.com/file/d/1vTFyJ4LlhE-GnGXmC_d1t4yxKr7rt7Vt/view?usp=sharing)     |
| Common in  <br>**5** rankers | [Fischer's  <br>Chameleon](https://github.com/Narabzad/Chameleons/tree/master/datasets/Fischer(common5))|2473   |0.0215 <br>[(Run)](https://drive.google.com/file/d/1rj_MNACTIHUWl87dCRWkmPgwx1h2Rhq5/view?usp=sharing) | 0.0240 <br>[(Run)](https://drive.google.com/file/d/1b7LID4TSHIiBj-sK2kZRxE-y_TLpsB4h/view?usp=sharing) | 0.0403 <br>[(Run)](https://drive.google.com/file/d/1xx30IQWME8TkTrVbMeO8st9cXFL2fofl/view?usp=sharing)    | 0.0398 <br>[(Run)](https://drive.google.com/file/d/1pNxulAWG2fGbZ2bEFWwnqSnwuMXZtHHW/view?usp=sharing)  | 0.0546 <br>[(Run)](https://drive.google.com/file/d/15KON9hz2dFgd1pYy8nTtqAsWYSPBsBf7/view?usp=sharing) | 0.0462 <br>[(Run)](https://drive.google.com/file/d/1Wapdz0h2noJCRlPSIw2X425krl7wTlOq/view?usp=sharing)     |
| Common in  <br>**4** rankers | [Outstalet's <br> Chameleon](https://github.com/Narabzad/Chameleons/tree/master/datasets/Outstalet(common4))|3119  |0.0392 <br>[(Run)](https://drive.google.com/file/d/1manHBekmogC1gcpgQ2hrksjZNqXwV5PK/view?usp=sharing)| 0.0400 <br>[(Run)](https://drive.google.com/file/d/1GNsjimgEaF15FSKVv19xVVBG-Nbmkp1d/view?usp=sharing)| 0.0660 <br>[(Run)](https://drive.google.com/file/d/1FCFvWYFngrK6s9zXQ-hI8a0zBAuAT0Vn/view?usp=sharing)    | 0.0560 <br>[(Run)](https://drive.google.com/file/d/1MORyZyZYME9ZREvAEcGBjyeoDlqjcIc7/view?usp=sharing) | 0.0847 <br>[(Run)](https://drive.google.com/file/d/1Ag-gh3ti9MLpasLI8iwngsns7y6IxMf-/view?usp=sharing) | 0.0780  <br>[(Run)](https://drive.google.com/file/d/1-_KDsTRtrJAfw34UlJpxBNTJjPtXDsYJ/view?usp=sharing)    |

We made all the runs available in the [Chameleons Google drive](https://drive.google.com/drive/folders/1vj8YC6YcADiiS7DjqepDMC9F_uaRneJC?usp=sharing). 

## Query Reformulation
Furthermore, given the literature has reported that hard queries can often be due to issues such as vocabulary mismatch, and
hence can be improved through query reformulation, we report the performance of several strong query reformulation 
techniques on the MSMarco Chameleons dataset and show that such queries remain stubborn and do not report noticeable performance
improvements even after systematic reformulation.

The expanded queries can be found [here](https://github.com/Narabzad/Chameleons/tree/master/expanded%20Queries) which are implemented using [ReQue toolkit](https://github.com/hosseinfani/ReQue). 


<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky"></th>
    <th class="tg-0pky"></th>
    <th class="tg-c3ow" colspan="6"><span style="font-weight:bold">Map pn the 50% Outstalet's dataset</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0pky">Category</td>
    <td class="tg-0pky">query</td>
    <td class="tg-0pky">BM25</td>
    <td class="tg-0pky">DeepCT</td>
    <td class="tg-0pky">DocT5</td>
    <td class="tg-0pky">RepBert</td>
    <td class="tg-0pky">ANCE</td>
    <td class="tg-0pky">TCT-ColBert</td>
  </tr>
    <tr>
    <td class="tg-0pky" rowspan="5"><br><br><br>Psuedo-Relevance Feedbac<br></td>
  </tr>

  <tr>
    <td class="tg-0pky">Relevance feedback</td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">RM3</td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">Document clustering</td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">Term Clustering </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
  </tr>
  <tr>
 <tr>
    <td class="tg-0pky" rowspan="8"><br><br><br><br> External Sources<br></td>
  </tr>
 <tr>
    <td class="tg-0pky"> Neural Embeddings </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
   <tr>
    <td class="tg-0pky"> WikiPedia </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
   <tr>
    <td class="tg-0pky"> Thesaurus </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky"> Entity Linking</td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">Sense Disambigution</td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">ConceptNet</td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky"> WordNet </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
  </tr>
  <tr>
 <tr>
    <td class="tg-0pky" rowspan="5"><br><br> Supervised Approaches<br></td>
  </tr>

  <tr>
    <td class="tg-0pky"> ANMT (Seq2Seq)</td>
    <td class="tg-4yk9">  </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
  <tr>
    <td class="tg-0pky">ACG (Seq2Seq + Attention)</td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
    <td class="tg-0pky"> </td>
  </tr>
  <tr>
    <td class="tg-0pky"> HRED-qs</td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
    <td class="tg-4yk9"> </td>
  </tr>
</tbody>
</table>

