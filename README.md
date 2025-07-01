# 🎬 Genre-Based Movie Recommendation System

A content-based movie recommendation system built using a dataset of **Telugu-language films**, designed to help users discover movies based on their preferred genres. This project leverages NLP, TF-IDF vectorization, cosine similarity, and a simple interactive GUI using Tkinter.

---

## 📌 Project Overview

This project aims to solve the problem of movie discovery within the context of **Telugu cinema**, which is often underrepresented in global datasets. Instead of relying on collaborative filtering, it uses **content-based filtering** — focusing on the `Genre` and `Overview` fields of movies to recommend similar ones.

---

## 🎯 Objective

- Recommend top-N movies that are similar in genre to a given movie.
- Provide an intuitive GUI for testing recommendations.
- Focus on **Telugu movies** with support for genre-specific filtering and content-based suggestions.

---

## 🧠 Why Genre-Based Filtering?

- Genres are a natural and intuitive grouping for movie preferences.
- Enables recommendations for lesser-known or new movies, as long as genre info is available.
- Avoids cold-start problems associated with user-based systems.

---

## 🔍 Approach

### 1. Data Preprocessing & Cleaning
- Handled missing values in `Year`, `Certificate`, `Genre`, and `Overview`.
- Cleaned irrelevant columns (`Unnamed: 0`) and converted datatypes.
- Normalized `Runtime`, removed or imputed unknowns.
- Ensured consistency in certificate labels.

### 2. Exploratory Data Analysis (EDA)
- Plotted distributions of runtime, year, certificate types, genre counts.
- Analyzed outliers and trends in rating and runtime.

### 3. Feature Engineering
- Transformed multi-label `Genre` into string corpus.
- Cleaned and tokenized the `Overview` text.
- Used `TF-IDF Vectorizer` for both `Genre` and `Overview` fields.

### 4. Model & Recommendation Logic
- Calculated **cosine similarity** for:
  - Overview vectors (for thematic similarity)
  - Genre vectors (for categorical similarity)
- Defined two primary recommendation modes:
  - **Genre-based Top-N** recommendations.
  - **You May Also Like** — based on overview similarity + rating.

---

## 🖥️ GUI (Tkinter-based)

A lightweight graphical interface built with Python's `tkinter`, which allows users to:
- Select a genre from a dropdown.
- View Top-10 recommended Telugu movies.
- Click on a movie to see:
  - Overview, Certificate, Runtime, Rating.
- Also see **"You May Also Like"** suggestions based on thematic content.

---

## 🔧 Tech Stack

| Tool/Library      | Purpose                                      |
|-------------------|----------------------------------------------|
| `pandas`          | Data manipulation                            |
| `numpy`           | Numeric computations                         |
| `matplotlib`, `seaborn` | Visualizations                       |
| `sklearn`         | TF-IDF vectorization, cosine similarity      |
| `tkinter`         | GUI development                              |
| `Counter`, `re`   | Text preprocessing                           |

---

## 📊 Sample Dataset Snapshot

| Movie                          | Year | Genre               | Rating | Overview             |
|-------------------------------|------|---------------------|--------|-----------------------|
| Bahubali: The Beginning       | 2015 | Action, Drama       | 8.1    | A legendary warrior...|
| Baahubali 2: The Conclusion   | 2017 | Action, Drama       | 8.2    | Shiva, the son of...  |
| 1 - Nenokkadine               | 2014 | Action, Thriller    | 8.1    | A rock star struggles...|

---

