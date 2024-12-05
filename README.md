# Women-Safety

About the Project: Women's Safety Reddit Sentiment and Topic Analysis

This project analyzes Reddit posts from the subreddit r/India focusing on the topic of women's safety. It leverages text processing, sentiment analysis, and topic modeling to gain insights into public discourse surrounding the issue. Below is a breakdown of the main objectives and methodologies used in the project:

Objectives:

    1. Sentiment Analysis: Analyze the sentiment of Reddit posts related to women’s safety to determine whether the community’s overall sentiment is positive, negative, or neutral.
    2. Topic Modeling: Use Latent Dirichlet Allocation (LDA) to discover the dominant topics being discussed in relation to women’s safety, based on Reddit posts.
    3. Data Visualization: Provide visual insights into sentiment distribution and trends across different topics.

Methodology:

    1. Data Collection:
    The data was collected using the praw (Python Reddit API Wrapper) library to access the r/India subreddit. A search was conducted with the query "women safety," gathering the first 100 posts related to the topic. For each post, the following information was retrieved:
        Post title
        Post content
        Post score (upvotes/downvotes)
        Creation timestamp (date)

    2. Data Cleaning:
    The content of each post was cleaned by:
        Removing URLs, hashtags, mentions, and special characters.
        Converting text to lowercase.
        Removing stopwords using NLTK's list of English stopwords.

    3. Sentiment Analysis:
    Using the VADER (Valence Aware Dictionary and sEntiment Reasoner) tool from NLTK, sentiment scores for each cleaned post were computed. Based on the compound score, posts were classified as:
        Positive (compound > 0.05)
        Negative (compound < -0.05)
        Neutral (compound between -0.05 and 0.05)

    4. Topic Modeling:
    To extract themes from the posts, the Latent Dirichlet Allocation (LDA) algorithm was applied. The data was first vectorized using CountVectorizer to convert the text into a document-term matrix. LDA was then used to identify the top 5 topics within the posts, with the top words for each topic displayed.

    Data Visualization:
    Several visualizations were created to summarize the findings:
        Sentiment Distribution: A bar plot showing the distribution of posts across different sentiment categories.
        Topic Visualization: The LDA topics were displayed with their top words to provide an understanding of the major themes discussed in the posts.
        Sentiment Trends Across Topics: A stacked bar chart showing how sentiment varies across different topics identified by LDA.

Technologies Used:

    1. Python: Primary programming language for the project.
    2. Pandas: For data manipulation and cleaning.
    3. NLTK: For text processing and sentiment analysis.
    4. Scikit-learn: For vectorization and topic modeling (LDA).
    5. Matplotlib and Seaborn: For creating visualizations.
    6. pyLDAvis: For interactive visualizations of topics from LDA.

Key Insights:

    1. The analysis reveals how Reddit users perceive women’s safety, with insights into positive, negative, and neutral sentiments.
    2. The topic modeling allows a deeper understanding of what specific aspects of women’s safety are being discussed (e.g., legal issues, societal concerns, personal safety stories).
    3. The sentiment trends across different topics provide insights into the emotional response associated with various discussions.
    
![Untitled](https://github.com/user-attachments/assets/e9769d3e-e07c-405b-878c-e85ec43f92f6)

![Untitled-1](https://github.com/user-attachments/assets/5f0dd630-b865-4a56-b44b-eefec17b5f80)

Future Enhancements:

    1. Expanded Dataset: The analysis could be extended to cover more Reddit posts over a longer period to capture changing trends.
    2. Geographic Analysis: Incorporating location data (e.g., through post metadata) to analyze sentiment by region.
    3. User Analysis: Analyzing the sentiment and topics based on user demographics or post history to see if certain groups show distinct patterns of behavior.
