# Kaggle Machine Learning and Data Science Survey 2020

An exploratory look at Kaggle's 2020 Machine Learning and Data Science Survey, in a Jupyter notebook using pandas and Plotly.

This is an early learning project from March 2021. It is a first pass at the data rather than a finished analysis.

## What the notebook does

The main notebook, `survey_data/survey2020.ipynb`:

- loads the survey responses and drops the first row, which holds the question text, leaving 20,036 responses across 355 columns
- groups the multi-part question columns (for example `Q7_Part_1` to `Q7_OTHER`) under their question number
- plots the age distribution of respondents (Q1)
- counts the programming languages respondents use on a regular basis (Q7)
- splits respondents by current role (Q5) and counts education levels (Q4), for everyone and for data engineers
- builds two interactive Plotly bar charts, each with two dropdown menus, so two groups (all respondents or a single role) can be compared side by side: one chart for education level and one for programming languages, each shown as a share of the group

`survey_data/notes.ipynb` is a short list of questions planned for later (gender differences, skills by role, pay differences by skills, opportunities from higher education, and which questions were most often left blank). Those are not explored in this repo.

The charts are stored as interactive Plotly output, which GitHub's notebook preview does not display (at about 11 MB, the notebook may also be too large for GitHub to preview at all). Open the notebook in Jupyter to see them.

## Data

`survey_data/kaggle_survey_2020_responses.csv` is Kaggle's public survey dataset. Kaggle's methodology and answer-choice documents are in `survey_data/supplementary_data/`.

According to the methodology document, the survey "received 20,036 usable responses from participants in 171 different countries and territories", and "The survey data was released under a CC 2.0 license: https://creativecommons.org/licenses/by/2.0/". The data is Kaggle's; this repo adds only the notebooks.

## Running it

You need Python 3 (the notebook was last run on Python 3.8.5) with pandas, NumPy, Plotly and Jupyter.

```bash
pip install pandas numpy plotly notebook
cd survey_data
jupyter notebook survey2020.ipynb
```

The notebook reads the CSV by a relative path, so start Jupyter from the `survey_data` folder.

## Repository layout

```
survey_data/
  survey2020.ipynb                  Main analysis notebook
  notes.ipynb                       Planned questions, not yet explored
  kaggle_survey_2020_responses.csv  Kaggle survey responses (about 25 MB)
  supplementary_data/               Kaggle's methodology and answer-choice PDFs
```

## Author

Daniel Olliver, [danielolliver.com](https://danielolliver.com/)
