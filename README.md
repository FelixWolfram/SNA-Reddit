# Reddit Hyperlink Network Analysis

Social Network Analysis of cross-community interactions on Reddit, examining how subreddits connect through hyperlinks over a 2.5-year period (Jan 2014 – Apr 2017).

## Research Question

Which subreddits hold the greatest importance for thematic networking, and how do communities shape the structure of the Reddit hyperlink network?

## Data

- **331,899 directed edges** between subreddits, each labeled with sentiment (-1 / +1)
- Filtered to largest connected component: ~55,864 nodes
- Source: [Stanford SNAP Reddit Hyperlink Dataset](http://snap.stanford.edu/data/soc-RedditHyperlinks.html)

## Method

- Graph construction (directed + undirected) in R
- Community detection via Louvain algorithm
- Network metrics: density, degree distribution, betweenness centrality, clustering coefficient
- Sentiment analysis of inter-community links

## Key Findings

- The network shows **Small-World properties**: average path length of ~3.9 despite low density
- **18 dominant communities** cover ~80% of the network (Pareto distribution)
- `r/askreddit` acts as central generalist hub — highest degree, but lower internal density
- `r/nfl` shows exceptionally high internal density with strong interconnection
- Negative interactions concentrate at interfaces between diverse communities, not within homogeneous ones

## Files

| File                               | Description                          |
| ---------------------------------- | ------------------------------------ |
| `Reddit_Network_Felix_Wolfram.Rmd` | R Markdown source with full analysis |
| `Reddit_Network_Felix_Wolfram.pdf` | Rendered report                      |
| `references.bib`                   | Bibliography                         |

## Tools

R, igraph, ggplot2, tidyverse
