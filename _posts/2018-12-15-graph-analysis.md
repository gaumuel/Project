---
title: "Graph Analysis"
bg: white
color: black
fa-icon: search
---

## Graph Analysis on Panama and Paradise Papers

Both datasets are comprised of similar structure as explained in the introduction. Thus, we can do a graph analysis on both of them with almost the same methods. 

From the graph analysis, we discovered that the highest page-rank nodes are mostly addresses. This is actually quite logical as an address serves as a contact postal address, thus a lot of intermediaries which help clients to set up an offshore company, can not change the address and most of the times same addresses are being used.  Therefore a lot of entities get linked to a similar address one way or the other.

![country distribution](img/page_rank_paradise_single.png "pagerank single")

Another interesting thing that was noticed, is the fact that the top 10 with the highest degree are mostly intermediaries. As mentioned in the introduction intermediaries serve as a middleman that helps a client to set up an offshore entity, therefore we can easily correlate why would they rank on top 10 of the highest degree nodes.  Most of the intermediaries are based outside onshire jurisdictions and sometimes they are subject to different laws, thus making it very difficult to influence them, especially the big banks and trust companies.


![country distribution](img/paradise_papers_degree.png "pagerank single")