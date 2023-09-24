### Created by @jl33-ai 👦🏻

---

**Content-Based Filtering** is an important concept in recommendation systems which recommend items by comparing the content of the items, such as genre, director, description, actors, etc., for a movie recommendation system. Recommendations are made based on the similarity between them.

---

## Topics 📚

---

- [Algorithm](#algorithm)
- [Implementation Example in Python](#implementation-example-in-python)
- [Advantages and Disadvantages](#advantages-and-disadvantages)
- [Conclusion](#conclusion)

---

## Algorithm

---

Content-Based Filtering uses item features to recommend other items that are similar to what the user likes, based on their previous actions or explicit feedback. For instance, if a user has watched `Lord of the Rings`, the system can recommend `The Hobbit` because both of them belong to the `Fantasy` genre.

The steps in Content-Based Filtering are:

1. **Represent each item in terms of a set of descriptors or terms**. For example, a movie could be represented by a vector of genres, directors, main actors, etc.
2. **Develop a user profile which models the user's preferences based on the item's characteristics**. This could be binary (user likes or dislikes item), or on a scale (user likes item to a certain degree). 

---

## Implementation Example in Python

---

```python
# Import required libraries
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity

# Create content
content = ["This movie is about a group of superheroes.", "A horror story with ghosts.", "A romantic drama set in New York."]

# Create TF-IDF Matrix
tfidfvec = TfidfVectorizer(stop_words='english')
content_matrix = tfidfvec.fit_transform(content)

# Calculate Cosine Similarity
cosine_sim = cosine_similarity(content_matrix, content_matrix)

# Top recommendations
recommendations = cosine_sim.argsort()[:,::-1]
top_2_recommendations = recommendations[0, 1:3]
```
This example recommends two content pieces at a time. Pass in a user's previously liked items, and using TF-IDF, it will return items with the highest cosine similarity.

---

## Advantages and Disadvantages

---

Advantages 🎉:

- No need for data on other users, thus no cold-start or sparsity problems.
- Can recommend to users with unique tastes.
- Can recommend new & unpopular items.
- Can provide explanations for recommended items by listing content-features that caused the recommendation.

Disadvantages 😱:

- Finding the appropriate features is hard.
- Does not recommend items outside a user's content profile.
- Unable to exploit quality judgments of other users.

---

## Conclusion

---

Content-Based Filtering offers personalized recommendations based on a user's past behavior and can work effectively with detailed user profiles. Although it isn't perfect, it's an essential technique in recommendation systems. 

---

Created by @jl33-ai 👦🏻
