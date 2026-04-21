# Metadata Spreadsheet Columns
[metadata spreadsheet](./metadata_with_absa_scores_and_trust.csv)

|column name|description|
|--|--|
|`id`|unique identifier for a `note_id`-`medicine_name` pair|
|`note_id`|anonymized unique identifier for a post, which can be used to link to the content and title in [the corpus](./absa/parsed_cleaned_posts.parquet)|
|`search_keyword`|the keyword used to search for the post|
|`poster`|the anonymized username of the poster|
|`created_year`|the year the post was created|
|`created_utc`|the UTC timestamp of when the post was created|
|`source`|where the post was scraped (Weibo or Reddit)|
|`language`|the target language of the post (Chinese for Weibo, English for Reddit), *not* the actual language of the post|
|`ups`|number of upvotes/likes|
|`downs`|number of downvotes (Reddit only)|
|`shared_count`|number of shares (Weibo only)|
|`comments_count`|number of comments (Weibo only)|
|`medicine_matches`|comma-separated string of all medicine names (including common variations) matching the post|
|`medicine_name`|one of the medicine names (could be a variation) matching the post|
|`medicine_uname`|unified name of `medicine_name`, Chinese for Weibo and English for Reddit|
|`medicine_en_uname`|English unified name of `medicine_name`|
|`medicine_category`|condition category of `medicine_name` (one of "diabetes", "flu", or "eczema")|
|`medicine_type`|type of `medicine_name` ("tcm" or "ebm")|
|`condition_mentioned`|whether `medicine_category` is mentioned in the post|
|`content_language`|identified language of the content|
|`content_language_confidence`|confidence score of the identified content language|
|`title_language`|identified language of the title|
|`title_language_confidence`|confidence score of the identified title language|
|`related`|whether the post is related to the medicine|
|`related_proba`|confidence score of the relatedness|
|`trust`|trust category of the post (one of "trust", "neutral", or "distrust")|
|`score`|ABSA sentiment score of the post|
|`sentiment`|sentiment category of the post (one of "positive", "neutral", or "negative")|
<br><br><br>
[back](../README.md)