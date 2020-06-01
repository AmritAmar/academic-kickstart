---
title: Games2Anime
summary: A recommendation system for CS 4300 (Language and Information).
tags:
- Cornell
- AI
- Game Design
date: "2020-05-08"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Center

links:
url_code: "http://games2anime.herokuapp.com/"
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#slides: example
---

[Games2Anime is a website that recommends Anime based on Steam Games.](http://games2anime.herokuapp.com/)

Due to current world events (COVID-19), there is a greater demand for online entertainment. Steam recently reached a record high for concurrent users and more people than ever are consuming online entertainment. However, there are only so many games on Steam and many gamers may seek to broaden their horizons by trying something new, like Japanese animation (anime). However, it can be difficult to narrow what anime to watch due to its wide variety of genres and styles.

Thus, the goal of our application is to recommend anime to people based on their Steam gaming preferences. By giving our system a game title from Steam, it will return a list of recommended anime based on the similarity in reviews and game description. Each recommendation displays general details and a similarity rating, along with a link to its [MyAnimeList](https://myanimelist.net/) page.

It works by comparing Steam Game Descriptions and Anime User Reviews to give you a list of Anime recommendations.

Games2Anime gets a list of all Anime with a MAL rating of 7.0 or above. We then remove any sequels/related movies from the list (to ensure we don't recommend more than 1 show from a particular series on a search). We get the top 20 reviews for each anime in our list (sorted by most helpful reviews first). We then combine all the reviews and use a fancy tool called [TfidfVectorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html) that converts a collection of raw documents to a matrix of TF-IDF features. We then perform dimensionality reduction using singular value decomposition ([svds](https://docs.scipy.org/doc/scipy/reference/generated/scipy.sparse.linalg.svds.html)) to get a matrices of words in reviews and anime based on words. We these structures, we can find similar anime to words using cosine similarity.

We then get a list of all Steam Games and their descriptions. Based on the game input, we go through each word in the game's description and get the top anime to that word and build up a ranking based on how often an anime shows up across the entire description. After normalizing and sorting the scores, we return the top 5 anime recommendations based on the game.

Because we are heavily reliant on keyword matching, some keywords get over weighted and thus we have to manually decrease the weight of certain keywords. This is ongoing so some search results are not great, yet.

This was a fun final project for CS 4300! I learnt a lot about information retrieval methods and systems along the way and found my next show. I hope it finds your next show as well!