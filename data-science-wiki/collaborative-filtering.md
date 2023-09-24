### Created by @jl33-ai 👦🏻

In this notebook, we will be exploring the essence of collaborative filtering, a technique used in recommendation systems. 

We'll break this down into the following sections:
1. [Introduction to Collaborative Filtering](#intro)
2. [Types of Collaborative Filtering](#types)
    - [Memory-Based Collaborative Filtering](#membased)
    - [Model-Based Collaborative Filtering](#modelbased)
3. [Pros and Cons of Collaborative Filtering](#proscons)
4. [Applications of Collaborative Filtering](#applications)
5. [Conclusion](#conclusion)
   
## Introduction to Collaborative Filtering <a name="intro"></a> 🎓
Collaborative Filtering (CF) is a recommendation technique which is based on the idea of user preference prediction. CF algorithms predict a user's interest by collecting preferences from numerous users. In other words, if a person A has the same decision as a person B on an issue, A is more likely to have B's opinion on a different issue than that of a randomly chosen person.

## Types of Collaborative Filtering <a name="types"></a> 📚
### Memory-Based Collaborative Filtering <a name="membased"></a>
Memory-based methods use the memory of previous users interactions to compute users' preferences. On the basis of similarity between items or users, we can make these calculations. This approach can be divided into two main sections:
* `User-User Collaborative Filtering`: Here we find look-alike users based on similarity and recommend items that first user's look-alike has chosen in the past.
    > Example: Netflix recommending movies based on the similarity in the behaviour of users.

* `Item-Item Collaborative Filtering`: This approach find items that are similar to the items that user has rated and recommend the most similar items.
   > Example: Amazon's "People who bought this, also bought this" recommendations.

### Model-Based Collaborative Filtering <a name="modelbased"></a>
Model-based methods are based on matrix factorization and are capable of dealing with scalability and sparsity than memory-based models. Model-based CF methods are based on machine learning and data mining techniques. The goal of Model-based Collaborative Filtering is to model the user-item interaction and they don't require maintaining a complete history of item-user interactions like in memory-based approach.

> Example: Predicting a customer's next purchase at a supermarket.

## Pros and Cons of Collaborative Filtering <a name="proscons"></a> 🔝🔚
### Pros:
* Does not need to understand item content. It merely finds patterns in user-item interaction history.
* Can handle numerous items since it's not based on item descriptions.
* Capable of recommending items to users with unique tastes.
* Effectively recommends complex items such as movies without requiring an understanding of item context.

### Cons:
* CF suffers from cold start problem, i.e. it can't handle new items or users.
* Popular items can often overshadow lesser known items, creating a bias.
* Incapable of recommending items not seen in interactions history.

## Applications of Collaborative Filtering <a name="applications"></a> 🛠️
Collaborative Filtering is pervasive in online services where personalized recommendations add tremendous value. Few examples are:
* Recommender systems (like youtube, netflix etc.)
* Social Media (friend recommendations)
* E-commerce (product recommendations)

## Conclusion <a name="conclusion"></a> ✍️

Collaborative Filtering is an essential component of effective recommendation systems, that makes recommendations based on the wisdom of the crowd. Both memory-based and model-based collaborative filtering have their unique strengths and weaknesses and a hybrid approach can be used to develop more robust recommendation systems. 
