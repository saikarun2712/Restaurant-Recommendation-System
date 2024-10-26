
# Restaurant Recommendation System

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [Data Analysis and Filtering](#data-analysis-and-filtering)
- [Recommendation Approach](#recommendation-approach)
- [Limitations and Future Enhancements](#limitations-and-future-enhancements)
- [References](#references)

---

## Project Overview
The Restaurant Recommendation System helps users navigate the diverse culinary landscape of Arizona, specifically within a 15-mile radius of Tucson. It provides personalized dining suggestions based on past reviews, restaurant ratings, and user preferences, while also supporting local businesses in reaching relevant customer segments.

## Problem Statement
With the rise in dining options, choosing the right restaurant has become overwhelming. Restaurant owners face similar challenges in attracting the right customers amid high competition. This project aims to bridge this gap by connecting users with local restaurants that align with their unique preferences, enhancing the dining experience and supporting local business growth.

## Proposed Solution
The **Restaurant Recommendation System** utilizes:
- **Restaurant Ratings**
- **User Reviews**
- **Geolocation Filtering**

By analyzing user dining history and restaurant data, the system generates customized recommendations that align closely with user preferences, facilitating a more satisfying dining experience.

---

## Data Analysis and Filtering

### Exploratory Data Analysis (EDA)
Our data analysis focused on:
1. **Target Area:** Tucson, AZ, for its high density of restaurants.
2. **Data Filtering:** Reviews from 2005 to 2022, focusing on open restaurants with ratings of 3 or above.
3. **Cuisine Classification:** Grouped by American, Mexican, Italian, Chinese, and Japanese cuisines, further divided by meal type (e.g., breakfast, coffee, nightlife).

### Topic Modeling with LDA
Key topics identified:
- **Cuisine Flavor:** Food types and flavors.
- **Beverage and Atmosphere:** Nightlife experience.
- **Service Quality:** Restaurant ambiance and service.
- **Specialized Options:** Breakfast and Mexican cuisine.
- **Wait Times and Service Experience:** General wait time feedback.

---

## Recommendation Approach

### Content-Based Recommender System
Our system adopts a content-based approach, where:
- **User Profiles:** Created from reviews and user preferences.
- **Restaurant Features:** Represented as “bags of words” for similarity analysis.
- **Similarity Matching:** Cosine similarity identifies restaurants aligning with the user’s profile, creating personalized recommendations based on prior dining experiences.

### Implementation Steps
1. **Key Phrase Extraction:** Reviews undergo text preprocessing (stop word removal, lemmatization) to focus on meaningful keywords.
2. **Profile Matching:** User profiles are matched with a pre-processed restaurant feature matrix, ranking restaurants by similarity.

---

## Limitations and Future Enhancements

### Current Limitations
- **Misspelled Searches:** Limited accuracy when user input contains errors.
- **Preference Blind Spots:** Current model does not factor in cuisine preferences or budget constraints.
- **Limited New User Recommendations:** Challenges in offering accurate suggestions for inactive or new users.

### Future Enhancements
1. **User-Centric Enhancements:** Prompt users for unique IDs and preferred cuisines to personalize recommendations further.
2. **Collaborative Filtering for New Users:** Uses similar user profiles to generate recommendations when no dining history exists.
3. **Location-Based Suggestions:** Offers highly rated nearby restaurant suggestions for users with no prior history.
4. **Model Refinement:** Use BERT for topic modeling and integrate sentiment and polarity scoring for a comprehensive recommendation “Superscore.”

---

## References
- [Yelp Dataset Documentation](https://www.yelp.com/dataset)
- [BERT for Topic Modeling](https://github.com/google-research/bert)

By delivering tailored recommendations, our system provides restaurants with a competitive advantage, helping them meet specific customer demands and drive growth in a crowded market.
