# NBA Win Probability Model: Extending Stern (1994)

Stern (1994) presents a formula that can be used to calculate win probability using time and lead as inputs. This project expands on Stern (1994) by incorporating pregame betting spreads, testing model assumptions, and developing meaningful coaching insight.

## Notebooks

### VariabilityAnalysis.ipynb
Variability Analysis uses play-by-play data from multiple seasons to calculate the variability at multiple points of the game using a maximum likelihood algorithm. It then uses that data to make a graph to visualize the change in variability. In the graph, the points appear relatively close together, indicating a small change in variability over time. To further demonstrate that fixed variability is a safe assumption, the Brier score was calculated with varying variability and with fixed variability to evaluate the improvement. There was just a 0.51% increase in Brier Score, confirming Stern's (1994) variability assumption.

### StrategicAnalysis.ipynb
Strategic Analysis combines two data sets to get pregame betting spreads and quarter leads for multiple NBA seasons. It then uses Stern’s (1994) original equation to calculate the win probability and generate figures. The figures create a visual representation of the points needed to maintain a 95% win probability, the increase in relative win probability of different lead changes, and at what time teams cross the 95% win probability threshold with multiple leads. These graphs shine light on when coaches should rest their best players by highlighting the most important moments to score during the game, depending on the situation. It also calculates the Brier Score using multiple seasons as tests to demonstrate consistent improvement.

## Datasets Required

- **NBA Matches 1949-2024** — [Kaggle](https://www.kaggle.com/datasets/joybiswas389/nba-matches-results-1949-2024)
- **NBA Odds Data 2008-2023** — [Kaggle](https://www.kaggle.com/datasets/christophertreasure/nba-odds-data)
- **NBA Play-by-Play Data 2020-2025** — [GitHub (shufinskiy/nba_data)](https://github.com/shufinskiy/nba_data)

## How to Run

1. Open the notebooks in [Google Colab](https://colab.research.google.com/)
2. Install required libraries: `pandas`, `numpy`, `scipy`, `matplotlib`, `kagglehub`
3. For VariabilityAnalysis.ipynb, manually upload the play-by-play `.tar.xz` files from the CDN NBA repository
4. Run all cells in order

## Paper

The full research paper is included in the `paper/` folder.

## References

Stern, Hal S. 1994. "A Brownian Motion Model for the Progress of Sports Scores." *Journal of the American Statistical Association* 89 (427): 1128-1134.
