# Music Artist Recommendation System

## Overview

This project implements a hybrid music recommendation engine using the Last.fm HetRec 2011 dataset. The goal is to generate personalized artist recommendations by combining multiple recommendation techniques and leveraging both user listening behavior and artist metadata.

The system integrates three complementary recommendation approaches:

* Item-Based Collaborative Filtering
* User-Based Collaborative Filtering
* Content-Based Filtering

By combining these methods, the model can provide more accurate and diverse music recommendations compared to using a single recommendation technique.

---

## Project Objective

Music streaming platforms rely heavily on recommendation systems to improve user experience and engagement. This project simulates a real-world recommendation engine capable of suggesting new artists based on:

* Listening history
* Similar users' preferences
* Artist genre and tag information

The system helps users discover artists they are likely to enjoy while exploring new music beyond their existing playlists.

---

## Dataset

The project uses the Last.fm HetRec 2011 dataset, which contains:

* User listening records
* Artist information
* User-generated tags
* Social network relationships
* Artist popularity data

Required dataset files:

data/
├── artists.dat
├── user_artists.dat
├── tags.dat
├── user_taggedartists.dat
├── user_taggedartists-timestamps.dat
└── user_friends.dat

The dataset provides a realistic environment for building and evaluating recommendation algorithms.

---

## Recommendation Approaches

### 1. Item-Based Collaborative Filtering

This method recommends artists that are frequently listened to together.

If users who enjoy Metallica also frequently listen to Megadeth and Anthrax, the model learns these relationships and recommends similar artists.

Example:

Metallica →

* Megadeth
* Anthrax
* Hellyeah
* Armored Saint

This approach focuses on artist-to-artist similarity derived from listening behavior.

---

### 2. User-Based Collaborative Filtering

This method identifies users with similar music preferences.

The recommendation engine:

1. Finds users whose listening habits resemble the target user.
2. Identifies artists enjoyed by those similar users.
3. Recommends artists not yet discovered by the target user.

This approach captures community-driven preferences and hidden listening patterns.

---

### 3. Content-Based Filtering

Content-based recommendations are generated using artist tags, genres, and descriptive metadata.

Examples of tags include:

* Rock
* Alternative
* Pop
* Metal
* Indie
* Electronic

Artists sharing similar tag profiles receive higher similarity scores.

Cosine Similarity is used to measure the closeness between artists based on their tag vectors.

---

## Similarity Calculation

The system uses Cosine Similarity to measure relationships between users and artists.

Higher scores indicate stronger similarity.

Example:

Metallica Playlist:

* Megadeth (0.86)
* Anthrax (0.84)
* Hellyeah (0.83)

Radiohead Playlist:

* Placebo (0.91)
* Muse (0.89)
* Coldplay (0.88)

Britney Spears Playlist:

* Christina Aguilera (0.87)
* Gwen Stefani (0.87)
* Lady Gaga (0.86)

These recommendations demonstrate how the model captures genre, audience, and listening-pattern similarities.

---

## Sample Results

### Metal / Thrash Metal Recommendations

Input Artist:
Metallica

Recommended Artists:

* Megadeth
* Anthrax
* Armored Saint
* Hellyeah

The model successfully identifies artists from the same metal ecosystem and listening community.

---

### Alternative Rock Recommendations

Input Artist:
Radiohead

Recommended Artists:

* Placebo
* Muse
* Coldplay
* Weezer
* Beck

The recommendations capture alternative and indie rock characteristics associated with Radiohead listeners.

---

### Pop Music Recommendations

Input Artist:
Britney Spears

Recommended Artists:

* Christina Aguilera
* Gwen Stefani
* Lady Gaga
* Madonna
* Hilary Duff

The system groups artists with similar fan bases and musical styles.

---

### Indie Folk Recommendations

Input Artist:
Beirut

Recommended Artists:

* Sufjan Stevens
* Iron & Wine
* Bright Eyes
* Devendra Banhart
* M. Ward

These recommendations demonstrate successful genre-aware discovery within the indie folk community.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Cosine Similarity
* Recommendation Systems
* Collaborative Filtering
* Content-Based Filtering

---

## Business Applications

Recommendation systems similar to this project are widely used by:

* Spotify
* YouTube Music
* Apple Music
* Netflix
* Amazon

Applications include:

* Personalized content recommendations
* User engagement optimization
* Customer retention
* Product recommendation engines
* Content discovery systems

---

## Key Learning Outcomes

Through this project:

* Implemented multiple recommendation algorithms.
* Built a hybrid recommendation architecture.
* Worked with real-world user interaction data.
* Applied similarity-based machine learning techniques.
* Evaluated recommendation quality through practical examples.

This project demonstrates skills in Machine Learning, Data Science, Recommender Systems, Data Processing, and User Behavior Analytics.

