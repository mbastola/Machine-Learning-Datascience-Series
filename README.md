# Machine Learning & Data Science Experiment Series

This repository is to stay current with fundamental concepts in Machine Learning, where I implement algorithms from at times from scratch, but mainly using sklearn and other libraries, and explore their practical applications. Each folder represents a self-contained project focused on a specific area of ML.

## Project Structure

The repository is organized into the following main categories:

```
Machine-Learning-Datascience-Series/
├── Gaussian-Mixture-Models/
├── Hypothesis-Testing/
├── Hypothesis-Testing-II-Gaussian-Mixtures/
├── Hypothesis-Testing-III-Bayesian-Methods/
├── Reinforcement-Learning/
│   ├── a-star/
│   ├── min-max/
│   ├── mdp/
│   ├── monte-carlo/
│   └── q-learning/
├── docker-compose.yml
└── requirements.txt
```

---

## Experiment Summaries

### 1. Hypothesis Testing

A series on statistical hypothesis testing, from classical frequentist methods to modern Bayesian approaches.

*   **[Hypothesis-Testing](./Hypothesis-Testing/)**: Implements an A/B test from scratch in NumPy and validates the results against SciPy's `ttest_ind`. This project serves as a foundational exercise in hypothesis testing, covering both two-sided and one-sided tests.

*   **Hypothesis-Testing-II-Gaussian-Mixtures**: Analyzes the daily returns of Google's stock price. It compares the fit of a standard Normal distribution, a Student's t-distribution (to capture heavy tails), and finally a Gaussian Mixture Model (GMM), demonstrating how GMMs can approximate complex, real-world distributions.

*   **Hypothesis-Testing-III-Bayesian-Methods**: Reformulates the A/B testing problem as a Multi-Armed Bandit (MAB). This project implements and compares several algorithms for solving the explore-exploit dilemma: Epsilon-Greedy, Optimistic Initial Values, UCB1, and Bayesian Thompson Sampling. It highlights the efficiency of Bayesian methods in converging to the optimal choice while minimizing regret.

### 2. Gaussian Mixture Models

*   **Gaussian-Mixture-Models**: A deep dive into GMMs, featuring a from-scratch implementation using the Expectation-Maximization (EM) algorithm. The project contrasts the performance of GMM against K-Means on various non-linear synthetic datasets, showcasing GMM's flexibility in handling clusters of different shapes and variances. It also explores how GMMs can be used as generative models.

### 3. Reinforcement Learning

This section covers a wide range of RL concepts, from foundational search algorithms and MDPs to model-free learning.

*   **mdp**: Solves the `FrozenLake-v1` environment using model-based dynamic programming. It deconstructs the environment into its core Markov Decision Process (MDP) components (States, Actions, Transitions, Rewards) and implements both **Value Iteration** and **Policy Iteration** to find the optimal policy.

*   **q-learning**: Tackles the same `FrozenLake-v1` environment but without prior knowledge of its dynamics (model-free). It implements and compares two cornerstone Temporal-Difference (TD) learning algorithms: **SARSA (on-policy)** and **Q-Learning (off-policy)**, analyzing the trade-offs between their conservative and aggressive learning styles.

*   **monte-carlo**: Explores another class of model-free learning through **On-Policy First-Visit Monte Carlo Control**. Unlike TD methods, this algorithm learns only from complete episodes. The project highlights the unbiased nature but high variance of MC methods.

*   **a-star**: A comparative analysis of fundamental pathfinding algorithms. It implements **A* (informed search)**, **Breadth-First Search (BFS)**, and **Depth-First Search (DFS)** to solve grid-based mazes, evaluating them on path optimality, speed, and search efficiency.

*   **min-max**: Delves into game-playing AI by implementing the **Min-Max algorithm with Alpha-Beta Pruning** for a chess engine. This project explores the core concepts of evaluation functions, search depth, and the computational trade-offs involved in building a classical game AI.

## Getting Started

To run these experiments, you can use the provided Docker environment.

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd Machine-Learning-Datascience-Series
    ```

2.  **Build and run the Docker container:**
    This will start a Jupyter Lab server.
    ```bash
    docker-compose up --build
    ```

3.  **Access Jupyter Lab:**
    Open your browser and navigate to the URL provided in the terminal output (usually `http://127.0.0.1:8888/lab`). You will see a token for authentication.

You can then navigate to the respective project folders and run the notebooks or Python scripts.

---

