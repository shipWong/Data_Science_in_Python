# Helicopter Prison Break — Finding the Prison Escape Patterns

## Introduction
In this project, we analyse the [dataset of helicopter escapes](https://en.wikipedia.org/wiki/List_of_helicopter_prison_escapes) (1971 - 2020) obtained from Wikipedia to find the patterns of helicopter prison breaks. The result of our analysis is based on the dataset being analysed at that very moment; therefore, the conclusion can differ from the most updated data on the Wikipedia article.

We use basic Python techniques to analyse the data and Matplotlib to visualise some results. We find the patterns based on years, countries and escapees.

The original dataset contains six self-explainable columns as below:
- `Date`
- `Prison name`
- `Country`
- `Succeeded`
- `Escapee(s)`
- `Details`

### The goal of the project

This project aims to answer the questions below:
- Which year showed the maximum number of helicopter prison break attempts?
- Which countries demonstrated the highest amount of helicopter prison break attempts?
- Which countries recorded the greatest chance of success for helicopter prison breaks?
- How did the number of escapees affect success?
- Which escapees have done it more than once?

### Summary of results
- Years **1986, 2001, 2007 and 2009** showed the highest occurrence of helicopter prison break attempts, i.e. three attempts.
- **France** has the highest number of helicopter prison escape attempts between 1971 to 2020, i.e. **15 times**.
- We **could not statistically draw any conclusion about the countries with the highest success rate** for helicopter prison breaks due to the low number of prison break attempts demonstrated by the countries with a 100% success rate.
- The **longer the names of the escapees** the **higher** the chance of prison break **success**.
- The escapees from France, **Michel Vaujour** and **Pascal Payet**, have done prison breaks **twice** respectively.
