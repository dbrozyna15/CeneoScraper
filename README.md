# CeneoScraper

# Stage 1 -- extraction of all components for single opinion 
# 1. extraciotn of single web page content
# 2. analysis of single opinion stucture
|Component|CSS selector|Variable name|Data type|
|---------|------------|-------------|---------|
|Opinion|div.user-post__card|opinion|
|ID|["data-entry-id"]|opinion_id|
|Author||span.user-post__author-name|author|
|Recommendation|span.user-post__author-recomendation > em|recommendation|
|Star rating|span.user-post__score-count|stars|
|Content|div.user-post__text|content|
|Adventages|div.review-feature__col:has(> div[class$="positives"]) > div.review-feature__item|pros|
|Disadventages|div.review-feature__col:has(> div[class$="negatives"]) > div.review-feature__item|cons|
|Purchase verification|div.review-pz|verified|
|Post date|span.user-post__published > time:nth-child(1)["datetime"]||post_date|
|Purchase date|span.user-post__published > time:nth-child(2)["datetime"]|purchase_date|
|Usefulness count|span[id^="votes-yes"]|usefulness|
|Uselessness count|span[id^="votes-no"]|uselessness|

# 3. extraction of single opinion components