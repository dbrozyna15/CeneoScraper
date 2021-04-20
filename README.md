# CeneoScraper

# Stage 1 - extraction of all components for single opinion 
1. extraciotn of single web page content
2. analysis of single opinion stucture
| Component | CSS selector | Variable name | Data type
|---------------------|-----------------------------------------------------------------------------------|----------------|----------
| Opinion              | div.js_product-review                                                             | opinion        | dict
| ID                   | ["data-entry-id"]                                                                 | opinion_id     | str
| Author               | span.user-post__author-name                                                       | author         | str
| Recommendation       | span.user-post__author-recomendation > em                                         | recommendation | bool
| Star rating          | span.user-post__score-count                                                       | stars          | float
| Content              | div.user-post__text                                                               | content        | str
| Adventages           | div.review-feature__col:has(> div[class$="positives"]) > div.review-feature__item | pros           | list(str)
| Disadventages        | div.review-feature__col:has(> div[class$="negatives"]) > div.review-feature__item | cons           | list(str)
| Purchase verification| div.review-pz                                                                     | verified       | bool
| Post date            | span.user-post__published > time:nth-child(1)["datetime"]                         | post_date      | str
| Purchase date        | span.user-post__published > time:nth-child(2)["datetime"]                         | purchase_date  | str
| Usefulness count     | span[id^="votes-yes"]                                                             | usefulness     | int
| Uselessness count    | span[id^="votes-no"]                                                              | uselessness    | int

## Stage 2 - extraction of single opinion components
1. definition of dictionary to store all components of single opinion
2. definition of dictionary for opinions' dictionaries storing
3. implementation of loop traversing through all opinions from single page

## Stage 3 - transformation of extracted data to given data types
1. implementation of loop traversing through consecutive pages with opinions
2. loading extracted opinions to .json file
3. parametrization of product id and reading product id from standard input

## Stage 4 - code refactoring