# CeneoScraper

# Stage 1 - extraction of all components for single opinion 
1. extraciotn of single web page content
2. analysis of single opinion stucture
|Component|CSS selector|Variable name|Data type
|---------------------|---------------------------------------------------------------------------------|--------------|---------
|Opinion              |div.js_product-review                                                            |opinion       |dict
|ID                   |["data-entry-id"]                                                                |opinion_id    |str
|Author               |span.user-post__author-name                                                      |author        |str
|Recommendation       |span.user-post__author-recomendation > em                                        |recommendation|bool
|Star rating          |span.user-post__score-count                                                      |stars         |float
|Content              |div.user-post__text                                                              |content       |str
|Adventages           |div.review-feature__col:has(> div[class$="positives"]) > div.review-feature__item|pros          |list(str)
|Disadventages        |div.review-feature__col:has(> div[class$="negatives"]) > div.review-feature__item|cons          |list(str)
|Purchase verification|div.review-pz                                                                    |verified      |bool
|Post date            |span.user-post__published > time:nth-child(1)["datetime"]                        |post_date     |str
|Purchase date        |span.user-post__published > time:nth-child(2)["datetime"]                        |purchase_date |str
|Usefulness count     |span[id^="votes-yes"]                                                            |usefulness    |int
|Uselessness count    |span[id^="votes-no"]                                                             |uselessness   |int

## Stage 2 - extraction of single opinion components
## Stage 3 - transformation of extracted data to given data types