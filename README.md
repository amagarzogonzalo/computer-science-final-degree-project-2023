# Contextual Bandits: Foundations and Applications

Source code for the Bachelor's thesis *Bandidos Contextuales: Fundamentos y
Aplicaciones* (English title: *Contextual Bandits: Foundations and
Applications*), submitted at the Facultad de Informática, Universidad
Complutense de Madrid, course 2022/2023.

| | |
| --- | --- |
| **Authors** | Iván Hernández Roldán, Alejandro Magarzo Gonzalo |
| **Advisor** | Miguel Palomino Tarjuelo |
| **Department** | Sistemas Informáticos y de Computación |
| **Degrees** | B.Sc. Computer Engineering · B.Sc. Computer Engineering & Business Administration |
| **Year** | 2023 |
| **DOI / Handle** | [20.500.14352/87700](https://hdl.handle.net/20.500.14352/87700) |
| **Full text** | [Docta Complutense](https://docta.ucm.es/entities/publication/bf07715f-16a9-4e9a-b781-765332ff5abe) |

The thesis starts from multi-armed bandits and the exploration–exploitation
dilemma, covers stochastic and adversarial bandits, and then develops contextual
bandits: algorithms, regret analysis, and two applied systems (a trading bot and
a movie recommender). Each directory here matches a chapter of the thesis.

## Repository layout

| Directory | Thesis section | What it implements |
| --- | --- | --- |
| `section6.1` | 6.1 | First contextual bandits with few contexts, using UCB instances |
| `section6.2` | 6.2 | Lipschitzian contextual bandits via discretization + UCB |
| `section7` | 7 | Contextual game: Hedge, GPMW and cGPMW on a network, with RVM regression and k-shortest-path routines |
| `section8` | 8 | Trading bot driven by Exp4, with market experts and exploration/learning-rate analysis |
| `section9` | 9 | Movie recommender driven by Exp4, combining ε-greedy, a neural network as a contextual bandit and neighbourhood collaborative filtering |

Most of the code is Python in Jupyter notebooks; section 7 also contains C++
graph code (`dijkstra`, `YenTopKShortestPaths`, simulation and network code).

## Running

The notebooks were written for a 2023 Python/Jupyter environment and are kept
as submitted. Each directory is self-contained; open its `.ipynb` files from
that directory. Third-party imports across the project are `numpy`, `pandas`,
`matplotlib`, `seaborn`, `scipy`, `scikit-learn`, `networkx`, `keras`,
`tensorflow` and `yfinance`.

Section 7 is a C++/Visual Studio project: it needs Eigen and dlib (see
`section7/Readme.txt`) plus the bundled Sioux Falls network files. Its Python
scripts generate the figures.

## Citation

```bibtex
@misc{hernandezroldan2023bandidos,
  title        = {Bandidos Contextuales: Fundamentos y Aplicaciones},
  author       = {Hern{\'a}ndez Rold{\'a}n, Iv{\'a}n and Magarzo Gonzalo, Alejandro},
  year         = {2023},
  howpublished = {Bachelor's thesis, Facultad de Inform{\'a}tica, Universidad Complutense de Madrid},
  url          = {https://hdl.handle.net/20.500.14352/87700}
}
```

## License

No license is declared. The code is published for reference; contact the
authors before reusing it.
