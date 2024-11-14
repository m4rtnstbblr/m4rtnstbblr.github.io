---
layout: page
title: Python Geography Game
description: Application Development
img: assets/img/py_game.jpg
importance: 3
category: work
related_publications: false
---

This project focuses on creating a geography quiz application that tests users on capital cities by showing either a country or a city. Users are required to submit the corresponding capital or country, with the quiz running for 10 rounds. At the end, a score out of 10 is displayed, with options to replay or exit.

---

### Implementation Details

- **Technologies Used**:

  - `geopandas` and `pandas` for data handling.
  - `matplotlib` for map visualization.
  - `tkinter` for the GUI.

- **Data**:

  - Two shapefiles (one for world cities and another for countries) are utilized.
  - Random city questions are generated from the data.

- **Functionality**:

  - Users are shown a city or country and must enter the corresponding capital or country in a text box.
  - Upon submitting an answer, a map is displayed:
    - The correct country is highlighted in yellow.
    - The user’s selected country is marked in blue if correct or in red if incorrect.
  - The application has an input field for answers, a submit button, a next question button, and an end game button.

  ***

## Challenges and Improvements

- **Challenges**:

  - The new question window sometimes opens in the background.
  - Occasional map stretching issues.
  - Answers require exact spelling, so minor typos result in incorrect answers.

- **Suggested Improvements**:
  - Additional game modes, such as identifying a country based on a map view.
  - Varying difficulty levels, with options based on different shapefiles and user knowledge.
  - Packaging the application into an executable for easier deployment.

---

**Full documentation:**

<iframe src="/assets/pdf/FinalProject_Documentation_Stobbelaar.pdf" width="100%" height="600px" style="border: none;">
    <a href="/assets/pdf/FinalProject_Documentation_Stobbelaar.pdf">Download PDF</a>.
</iframe>
