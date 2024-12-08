# Article Management System

Welcome to the **Article Management System**! This system allows you to efficiently manage authors, magazines, and articles. With features for associating authors with their works, tracking contributors, and exploring articles across various categories, it’s the perfect tool for organizing articles across different magazines and topics.

---

## Overview

The **Article Management System** is composed of three primary classes:

- **Article**: Represents an article written by an author and published in a magazine.
- **Author**: Represents an author, enabling them to write articles and associate them with different magazines.
- **Magazine**: Represents a magazine that publishes articles, tracks contributors, and manages topics.

---

## Key Features

### Article Class
- Articles are linked to both **authors** and **magazines**.
- Title validation ensures article titles are between 5 and 50 characters.
- Tracks all articles ever created and links them to their respective authors and magazines.

### Author Class
- Authors can be associated with multiple articles.
- Authors can query all articles they've written.
- Authors can retrieve all magazines they have contributed to, as well as the topics they write about.

### Magazine Class
- Each magazine stores its name, category, and the articles it has published.
- Tracks the authors who have contributed to the magazine.
- Retrieves all article titles published in the magazine.
- Identifies top contributors (authors who have contributed more than two articles).
- Class method to identify the magazine with the most articles published.

---

## Classes

### `Article`

Represents an article written by an **Author** and published in a **Magazine**.

#### Attributes:
- `author`: The author of the article (instance of `Author` class).
- `magazine`: The magazine where the article is published (instance of `Magazine` class).
- `title`: The title of the article (string between 5 and 50 characters).

#### Methods:
- `__init__(self, author, magazine, title)`: Initializes a new article, linking it to an author and magazine.
- `title`: Property to retrieve the article's title (immutable).

---

### `Author`

Represents an author who writes articles and publishes them in different magazines.

#### Attributes:
- `name`: The name of the author (non-empty string).
- `_articles`: A private list of articles the author has written.

#### Methods:
- `__init__(self, name)`: Initializes an author with a name.
- `articles()`: Returns a list of articles written by the author.
- `magazines()`: Returns a list of unique magazines the author has written for.
- `add_article(magazine, title)`: Adds a new article to a specific magazine.
- `topic_areas()`: Returns a list of unique topic areas (categories) based on the magazines the author contributes to.

---

### `Magazine`

Represents a magazine that publishes articles and tracks contributors.

#### Attributes:
- `name`: The name of the magazine (2 to 16 characters).
- `category`: The category of the magazine (non-empty string).
- `_articles`: A private list of articles published in the magazine.

#### Methods:
- `__init__(self, name, category)`: Initializes a new magazine.
- `name`: Property to retrieve the magazine's name (immutable).
- `category`: Property to retrieve or set the magazine's category (immutable).
- `articles()`: Returns a list of articles published in the magazine.
- `contributors()`: Returns a list of authors who have contributed to the magazine.
- `article_titles()`: Returns a list of article titles published in the magazine.
- `contributing_authors()`: Returns a list of authors who have contributed more than two articles to the magazine.
- `top_publisher()`: Class method to return the magazine with the most articles.

---

## Installation

### 1. Clone the repository:
Clone the repository to your local machine using the following command:

```bash
git clone git@github.com:aliabdi1/python-non-sqlalchemy-code-challenge-articles.git
