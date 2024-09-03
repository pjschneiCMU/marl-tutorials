# Multi-Agent Reinforcement Learning (MARL)

> [!WARNING]
> Under development!

This repository aims to provide tutorials on multi-agent reinforcement learning (MARL). Before diving into the modeling of multiple agents interacting through the Markov decision process (MDP) framework (introduced by Shapley in 1953), we first cover the basics of game theory and other fundamental concepts.

> [!NOTE]
> Currently, the repository has a strong focus on game theory, which may eventually be moved to a separate GitHub repository.

### Game Theory Literature

#### Key Questions for Modeling a Problem via Game Theory

- How many players are involved?
_The number of players defines the game’s structure (e.g., two-player vs. multi-player) and influences the complexity of the analysis._
- Are the actions available finite or infinite?
> Determining whether the action space is finite or infinite affects the strategies players can adopt and the mathematical tools used for analysis.
- Does the game evolve with simultaneous moves or sequential moves?
> Identifying whether players act simultaneously or in sequence helps classify the game (e.g., normal-form vs. extensive-form) and influences strategy formulation.
- Is the game static or dynamic?
> A static game is played once, while a dynamic game unfolds over multiple periods. Dynamic games often require more complex strategies, like backward induction.
- Is there complete or incomplete information?
> Assessing whether players have full knowledge of the game's structure and payoffs is vital. Incomplete information often leads to Bayesian or signaling games.
- Do players have private information (asymmetric information)?
> If some players have private information, the game involves asymmetric information, leading to scenarios like adverse selection or moral hazard.
- Are players cooperating or competing?
> Understanding whether players work together (cooperative games) or compete (non-cooperative games) influences the modeling approach and solution concepts.
- What is the payoff structure?
> Analyzing how payoffs are determined—whether zero-sum, positive-sum, or involving externalities—is crucial for understanding incentives and outcomes.
- Are players rational, and what level of rationality is assumed?
> Assuming players act in their best interest, the level of rationality (e.g., bounded or perfect) assumed in the model can significantly affect predictions.
- Is the game repeated, and how does repetition affect strategies?
> In repeated games, strategies may evolve based on past interactions, potentially leading to cooperation in repeated settings (e.g., folk theorem).
- How are equilibria defined, and which equilibrium concepts are applicable?
> Identifying the appropriate equilibrium concept (e.g., Nash, subgame perfect, Bayesian) is essential for predicting outcomes.

#### Simultaneous-move Games
Normal-form Games (Strategic-form Games)
- Von Neumann, J., & Morgenstern, O. (1944). Theory of games and economic behavior. Princeton University Press.
> This book laid the foundation for normal-form games, introducing the basic structure for analyzing strategic interactions where players make decisions simultaneously.

Bayesian Games
- Harsanyi, J. C. (1967). [Games with incomplete information played by “Bayesian” players, I–III Part I. The basic model](https://doi.org/10.1287/mnsc.14.3.159). _Management Science_, 14(3), 159-182.
> Harsanyi’s work introduced Bayesian games, which extend normal-form games to situations of incomplete information, allowing players to form beliefs about unknown factors.

Potential Games
- Monderer, D., & Shapley, L. S. (1996). [Potential games](https://doi.org/10.1006/game.1996.0044). _Games and Economic Behavior_, 14(1), 124-143.
> This paper defines potential games, a class of games where the incentive structure can be captured by a potential function, simplifying the analysis of equilibria.

Robust Games
- Aghassi, M., & Bertsimas, D. (2006). [Robust game theory](https://doi.org/10.1007/s10107-005-0686-0). _Mathematical Programming_, 107(1), 231-273.
> This work extends game theory to account for uncertainty and robustness, providing tools for decision-making in uncertain environments.

#### Sequential-move Games

Stackelberg Games
- Stackelberg, H. V. (1934). [Marktform und Gleichgewicht](https://doi.org/10.1007/978-3-642-12586-7).
> Stackelberg introduced a model where leaders move first and followers react, which is fundamental in analyzing competitive markets and leadership dynamics in sequential games.

Extensive-form Games
- Von Neumann, J., & Morgenstern, O. (1944). Theory of games and economic behavior. Princeton University Press.
> This book also introduced extensive-form games, providing a framework for analyzing games where the order of moves and the information available at each decision point are crucial.

#### Games Involving Both Simultaneous and Sequential Moves
Stochastic Games (Markov Games)
- Shapley, L. S. (1953). [Stochastic games](https://doi.org/10.1073/pnas.39.10.1095). _Proceedings of the National Academy of Sciences_, 39(10), 1095-1100.
> Shapley’s work introduced stochastic games, which generalize Markov decision processes to multi-player settings with both simultaneous and sequential moves.
- M. L. Littman. (1994). [Markov games as a framework for multi-agent reinforcement learning](https://doi.org/10.1016/B978-1-55860-335-6.50027-1). In _Proceedings of the 11th International Conference on Machine Learning (ICML)_ (pp. 157-163).
> Littman introduced Minimax-Q learning and extended the concept of stochastic games into the realm of multi-agent reinforcement learning, emphasizing their application in AI and dynamic environments.

#### Special Forms
Evolutionary Game Theory
- Smith, J. M., & Price, G. R. (1973). [The logic of animal conflict](https://doi.org/10.1038/246015a0). _Nature_, 246(5427), 15-18.
> This paper introduced the concept of evolutionary stable strategies, a cornerstone of evolutionary game theory.

Repeated Games
- Fudenberg, D., & Maskin, E. (1986). [The folk theorem in repeated games with discounting or with incomplete information](https://doi.org/10.2307/1911307). _Econometrica_, 54(3), 533–554.
> This work is key in the theory of repeated games, explaining how cooperation can be sustained over time in strategic settings.

Cooperative Games
- Shapley, L. S. (1953). [A value for n-person games](https://doi.org/10.1515/9781400881970-018). In _Contributions to the Theory of Games_ (pp. 307-317).
> Shapley introduced the Shapley value, a solution concept in cooperative game theory that is widely used in economics and political science.

### Surveys and Literature Reviews
- Busoniu, L., Babuska, R., & De Schutter, B. (2008). [A comprehensive survey of multiagent reinforcement learning](https://doi.org/10.1109/TSMCC.2007.913919). _IEEE Transactions on Systems, Man, and Cybernetics, Part C (Applications and Reviews)_, 38(2), 156-172.
- Zhang, K., Yang, Z., & Başar, T. (2021). [Multi-agent reinforcement learning: A selective overview of theories and algorithms](https://doi.org/10.1007/978-3-030-60990-0_12). In _Handbook of Reinforcement Learning and Control_ (pp. 321-384). Springer, Cham.

### Algorithms
- Lowe, R., Wu, Y. I., Tamar, A., Harb, J., Pieter Abbeel, O., & Mordatch, I. (2017). [Multi-agent actor-critic for mixed cooperative-competitive environments](https://papers.nips.cc/paper_files/paper/2017/hash/68a9750337a418a86fe06c1991a1d64c-Abstract.html). _Advances in Neural Information Processing Systems_, 30.
> MADDPG
- Iqbal, S. & Sha, F.. (2019). [Actor-attention-critic for multi-agent reinforcement learning](https://proceedings.mlr.press/v97/iqbal19a.html). In _Proceedings of the 36th International Conference on Machine Learning (ICML)_ (pp. 2961-2970).

### Cooperative setting
- Yu, C., Velu, A., Vinitsky, E., Gao, J., Wang, Y., Bayen, A., & Wu, Y. (2022). [The surprising effectiveness of ppo in cooperative multi-agent games](https://proceedings.neurips.cc/paper_files/paper/2022/hash/9c1535a02f0ce079433344e14d910597-Abstract-Datasets_and_Benchmarks.html). _Advances in Neural Information Processing Systems_, 35, 24611-24624.

### Competitive setting
- Bansal, T., Pachocki, J., Sidor, S., Sutskever, I., & Mordatch, I. (2018). [Emergent complexity via multi-agent competition](https://openreview.net/pdf?id=Sy0GnUxCb). In _Proceedings of the 6th International Conference on Learning Representations (ICLR)_. [\[Code\]](https://github.com/openai/multiagent-competition)
- Al-Shedivat, M., Bansal, T., Burda, Y., Sutskever, I., Mordatch, I., & Abbeel, P. (2018). [Continuous adaptation via meta-learning in nonstationary and competitive environments](https://openreview.net/pdf?id=Sk2u1g-0-). In _Proceedings of the 6th International Conference on Learning Representations (ICLR)_. [\[Code\]](https://github.com/openai/robosumo)

### Learning strategies
- Bengio, Y., Louradour, J., Collobert, R., & Weston, J. (2009). [Curriculum learning](https://doi.org/10.1145/1553374.1553380). In _Proceedings of the 26th International Conference on Machine Learning (ICML)_ (pp. 41-48).

### Learning zero-sum games
- Loftin, R., Saha, A., Devlin, S., & Hofmann, K. (2021). [Strategically efficient exploration in competitive multi-agent reinforcement learning](https://proceedings.mlr.press/v161/loftin21a.html). In _Uncertainty in Artificial Intelligence_ (pp. 1587-1596).
- Chen, J., Xu, Z., Li, Y., Yu, C., Song, J., Yang, H., Fang, F., Wang, Y., & Wu, Y. (2024). [Accelerate multi-agent reinforcement learning in zero-sum games with subgame curriculum learning](https://doi.org/10.1609/aaai.v38i10.29011). In _Proceedings of the AAAI Conference on Artificial Intelligence_, 38(10), 11320-11328.

### TBD
- Fudenberg, D., & Levine, D. K. (1998). [_The theory of learning in games_](https://mitpress.mit.edu/9780262529242/the-theory-of-learning-in-games/) (Vol. 2). MIT Press, Cambridge, MA.
- Hofbauer, J., & Sandholm, W. H. (2002). [On the global convergence of stochastic fictitious play](https://doi.org/10.1111/j.1468-0262.2002.00440.x). _Econometrica_, 70(6), 2265-2294.
- Hu, J., & Wellman, M. P. (2003). [Nash Q-learning for general-sum stochastic games](https://www.jmlr.org/papers/volume4/hu03a/hu03a.pdf). _Journal of Machine Learning Research_, 4, 1039-1069.
- Daskalakis, C., Foster, D. J., & Golowich, N. (2020). [Independent policy gradient methods for competitive reinforcement learning](https://dl.acm.org/doi/pdf/10.5555/3495724.3496188). _Advances in Neural Information Processing Systems_, 33, 5527-5540.
- Leslie, D. S., Perkins, S., & Xu, Z. (2020). [Best-response dynamics in zero-sum stochastic games](https://doi.org/10.1016/j.jet.2020.105095). _Journal of Economic Theory_, 189, 105095.
- Sayin, M. O., Parise, F., & Ozdaglar, A. (2022). [Fictitious play in zero-sum stochastic games](https://doi.org/10.1137/21M1426675). _SIAM Journal on Control and Optimization_, 60(4), 2095-2114.

There are multiple GitHub repositories providing literature resources purely focused on recent advancements in MARL research.
- [MARL-Papers](https://github.com/LantaoYu/MARL-Papers)
- [MARL-papers-with-code](https://github.com/TimeBreaker/MARL-papers-with-code)
