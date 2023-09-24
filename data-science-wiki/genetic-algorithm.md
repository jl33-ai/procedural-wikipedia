
### Created by @jl33-ai 👦🏻

The Genetic Algorithm is a search heuristic that mimics the process of natural selection. This algorithm reflects the process of natural evolution, such as selection, crossover or mating and mutation.

## 🏷️ Tags:
- `#Genetic-Algorithm`
- `#AI`
- `#Machine-Learning`
- `#Search-Heuristic`
- `#Natural-Evolution`

## 📝 Contents:
1. [Introduction](#intro)
2. [Principles](#principles)
3. [Pseudocode](#pseudo)
4. [Example](#example)
5. [Applications](#app)
6. [Advantages and Disadvantages](#adv)
7. [Conclusion](#conclusion)

<a name="intro"></a>
## ✨ Introduction 
- Genetic Algorithms are commonly used to generate high-quality solutions for optimization problems and search problems.
- They use bio-inspired operators such as mutation, crossover, and selection.

<a name="principles"></a>
## 📚 Principles
- __Fitness Function__: The function we want to optimize and it provides a measurement of how well each individual in the population is suited to the task.
- __Selection__: Selected according to their fitness, the higher the fitness, the higher the chance of being selected.
- __Crossover (recombination)__: Parent chromosomes produce offspring for the next generation.
- __Mutation__: This step helps to maintain genetic diversity from one generation to the next. It alters one or more gene values in a chromosome.

<a name="pseudo"></a>
## 📜 Pseudocode
```plaintext
1. Create a population
2. Determine fitness of population
3. Until convergence repeat:
   a. Select parents from population
   b. Crossover and generate new population
   c. Perform mutation on new population
   d. Calculate fitness for new population
```

<a name="example"></a>
## 📔 Example
Let's take an example of the "Hello World" problem. We want to reach the target string starting from a random string.

```python
import random
import string

def create_individual(length, chrom_set):
    return [random.choice(chrom_set) for _ in range(length)]

def compute_fitness(individual, target):
    return sum(indi_gene == target_gene for indi_gene, target_gene in zip(individual, target))

# An example of Genetic Algorithm usage
target = list("Hello, World!")
chrom_set = list(string.ascii_letters + string.punctuation + ' ')
pop_size, gen_limit = 100, 1000

# Initialization
population = [create_individual(len(target), chrom_set) for _ in range(pop_size)]

for generation in range(gen_limit):
    pop_fitness = [(compute_fitness(individual, target), individual) for individual in population]
    if max(pop_fitness)[0] == len(target): break
    # Selection, Crossover and Mutation
    # ...
```

<a name="app"></a>
## 🕹️ Applications
- Machine Learning
- Data Science Optimization
- Artificial Intelligence
- Gaming

<a name="adv"></a>
## 📈 Advantages and Disadvantages
- __Advantages__:
    - Optimizes both continuous and discrete functions.
    - Provides near-optimal solutions for large and complex problems.
- __Disadvantages__:
    - Computationally expensive.
    - Not suitable for simple problems.

<a name="conclusion"></a>
## 🎯 Conclusion