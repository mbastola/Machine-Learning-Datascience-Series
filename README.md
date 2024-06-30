# Machine Learning & Data Science Experiments

This repository is to stay current with fundamental concepts in Machine Learning, where I implement algorithms from at times from scratch, but mainly using sklearn and other libraries, and explore their practical applications. Each folder represents a self-contained project focused on a specific area of ML.

## Project Structure

The repository is organized into the following main categories:

```
Machine-Learning-Datascience-Series/
├── Gaussian-Mixture-Models/
├── Hypothesis-Testing/
├── Hypothesis-Testing-II-Gaussian-Mixtures/
├── Hypothesis-Testing-III-Bayesian-Methods/
├── K-Means/
├── KNN/
├── Linear-Regression/
├── Logistic-Regression/
├── NLP/
├── Reinforcement-Learning/
│   ├── a-star/
│   ├── expectimax/
│   ├── mdp/
│   ├── min-max/
│   ├── monte-carlo/
│   └── q-learning/
├── SVM/
│   ├── facial-expressions/
│   └── iris-dataset/
├── Trees/
├── docker-compose.yml
├── Dockerfile
└── requirements.txt
```

---

## Experiment Summaries

### 1. Hypothesis Testing

A series on statistical hypothesis testing, from classical frequentist methods to modern Bayesian approaches.

*   **Hypothesis-Testing**: Implements an A/B test from scratch in NumPy and validates the results against SciPy's `ttest_ind`. This project serves as a foundational exercise in hypothesis testing, covering both two-sided and one-sided tests.

*   **Hypothesis-Testing-II-Gaussian-Mixtures**: Analyzes the daily returns of Google's stock price. It compares the fit of a standard Normal distribution, a Student's t-distribution (to capture heavy tails), and finally a Gaussian Mixture Model (GMM), demonstrating how GMMs can approximate complex, real-world distributions.

*   **Hypothesis-Testing-III-Bayesian-Methods**: Reformulates the A/B testing problem as a Multi-Armed Bandit (MAB). This project implements and compares several algorithms for solving the explore-exploit dilemma: Epsilon-Greedy, Optimistic Initial Values, UCB1, and Bayesian Thompson Sampling. It highlights the efficiency of Bayesian methods in converging to the optimal choice while minimizing regret.

### 2. Supervised Learning and NLP

*   **Linear-Regression**: Builds a linear regression model for an e-commerce customer dataset, using customer behavior features such as session length, app usage, website usage, and membership length to predict yearly amount spent. The project includes exploratory plots, model evaluation, coefficient interpretation, and residual analysis.

*   **Logistic-Regression**: Applies logistic regression to advertising data to predict whether a user clicked on an ad. It explores demographic and usage features such as age, area income, daily internet usage, and time spent on site before training and evaluating a binary classifier.

*   **KNN**: Implements K-Nearest Neighbors classification on a synthetic feature dataset. The project standardizes input features, evaluates the initial classifier, searches for a better `k` value using error-rate analysis, and retrains the model with the selected neighborhood size.

*   **Trees**: Compares Decision Trees and Random Forests on LendingClub loan data to classify whether borrowers fully paid back their loans. It covers categorical feature handling, train-test evaluation, and side-by-side performance comparisons between a single tree and an ensemble model.

*   **SVM**: Contains Support Vector Machine experiments across two datasets: `iris-dataset`, which classifies Iris flower species and tunes SVM parameters with GridSearch, and `facial-expressions`, which applies SVM with PCA-based dimensionality reduction to classify facial expressions.

*   **NLP**: Uses the Yelp review dataset to compare text classification workflows. It builds scikit-learn pipelines with CountVectorizer, TF-IDF, Multinomial Naive Bayes, and Random Forests to evaluate how different feature extraction and model choices affect review classification.

### 3. Clustering and Mixture Models

*   **K-Means**: Introduces unsupervised learning with K-Means clustering on college data. The project clusters institutions using numerical features, compares predicted clusters against the known private/public label for evaluation, and visualizes cluster behavior across key variables.

*   **Gaussian-Mixture-Models**: A deep dive into GMMs, featuring a from-scratch implementation using the Expectation-Maximization (EM) algorithm. The project contrasts the performance of GMM against K-Means on various non-linear synthetic datasets, showcasing GMM's flexibility in handling clusters of different shapes and variances. It also explores how GMMs can be used as generative models.

### 4. Reinforcement Learning

This section covers a wide range of RL concepts, from foundational search algorithms and MDPs to model-free learning.

*   **mdp**: Solves the `FrozenLake-v1` environment using model-based dynamic programming. It deconstructs the environment into its core Markov Decision Process (MDP) components (States, Actions, Transitions, Rewards) and implements both **Value Iteration** and **Policy Iteration** to find the optimal policy.

*   **q-learning**: Tackles the same `FrozenLake-v1` environment but without prior knowledge of its dynamics (model-free). It implements and compares two cornerstone Temporal-Difference (TD) learning algorithms: **SARSA (on-policy)** and **Q-Learning (off-policy)**, analyzing the trade-offs between their conservative and aggressive learning styles.

*   **monte-carlo**: Explores another class of model-free learning through **On-Policy First-Visit Monte Carlo Control**. Unlike TD methods, this algorithm learns only from complete episodes. The project highlights the unbiased nature but high variance of MC methods.

*   **a-star**: A comparative analysis of fundamental pathfinding algorithms. It implements **A* (informed search)**, **Breadth-First Search (BFS)**, and **Depth-First Search (DFS)** to solve grid-based mazes, evaluating them on path optimality, speed, and search efficiency.

*   **min-max**: Delves into game-playing AI by implementing the **Min-Max algorithm with Alpha-Beta Pruning** for a chess engine. This project explores the core concepts of evaluation functions, search depth, and the computational trade-offs involved in building a classical game AI.

*   **expectimax**: Extends the chess-search experiments with the **Expectimax algorithm**, modeling uncertain or stochastic opponent behavior. It reuses the board evaluation concepts from the Min-Max project while comparing deterministic adversarial search with expectation-based decision making.

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
