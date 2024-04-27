# PROJECT TITLE 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT
This project focuses on analyzing and organizing YouTube channels into distinct groups, or clusters, based on their content and audience engagement. By examining things like the language used, types of videos, and viewer interactions, the model categorizes channels to help understand what types of content are popular and how they align with viewer preferences. This information can be used by marketers to tailor their strategies, by content creators to enhance their videos, and by analysts to understand trends in the digital media landscape. Essentially, it’s about making sense of vast amounts of YouTube data to help optimize online video content strategies.

## DATA
The data for this project comprises a comprehensive dataset of YouTube channels, originally sourced from Kaggle (original data owner Nidula Elgiriyewithana).
This dataset includes key metrics such as video views, number of uploads, and basic channel information. 
To enrich the data and provide deeper insights into the content, additional information such as channel descriptions and primary languages was appended using advanced language models. Specifically, descriptions were generated and refined with the assistance of language models like ChatGPT-4, Google Gemini, and META LLMA 2, ensuring a robust and nuanced understanding of each channel's focus and audience engagement. 
This integration of structured channel data with dynamically generated text data allows for a sophisticated analysis of YouTube content strategies across diverse linguistic and cultural contexts.


## MODEL 
The model deployed in this project combines machine learning techniques like clustering and classification to analyze and categorize YouTube channels. 
I used K-Means clustering to identify distinct groups of channels based on similarities in their content descriptions and viewer metrics.
This method is ideal for segmenting large datasets into manageable groups that share common characteristics, making it easier to understand overarching trends and niche content areas.

For predicting the category of channels based on their subscriber counts, a RandomForestClassifier is employed. 
This model was chosen for its robustness and effectiveness in handling diverse datasets with a mix of numerical and categorical data.
RandomForest is particularly advantageous due to its ability to manage overfitting, making it reliable for our purposes where the accuracy of prediction is key. 
The combination of these models provides a comprehensive approach to understanding YouTube channels, aiding in strategic decision-making for content creators and marketers alike.
The model is created in a Jupyter environment.
For more detailed technical information, performance metrics, and in-depth analysis, please see the full **model card** included with this project documentation.

## HYPERPARAMETER OPTIMSATION 

In this project, hyperparameter optimization was essential to ensure the best performance of our machine learning models, particularly the RandomForestClassifier. 
The main hyperparameters optimized for the RandomForestClassifier model include:

Number of Trees (n_estimators): The number of trees in the forest.
Maximum Depth of Trees (max_depth): Controls the maximum depth of each tree. 
Minimum Samples Split (min_samples_split): The minimum number of samples required to split an internal node.
Minimum Samples Leaf (min_samples_leaf): The minimum number of samples required to be at a leaf node. 


For the K-Means clustering used in data segmentation, the main hyperparameter was the Number of Clusters (k).
The Herarchiral Method was used here to identify the optimal k value 

Optimization Methodology
For hyperparameter tuning, I employed GridSearchCV, which systematically constructs and evaluates a model for each combination of algorithm parameters specified in a grid. .
The process involved:
Defining a parameter grid for RandomForest parameters such as n_estimators, max_depth, min_samples_split, and min_samples_leaf.
Running GridSearchCV with cross-validation to ensure that the model's performance estimates are reliable and the model does not just perform well on a subset of the data.
This structured approach to hyperparameter tuning helps in refining the models to achieve higher accuracy and efficiency, enabling more precise predictions and better clustering outcomes.
For more detailed technical information, performance metrics, and in-depth analysis, please see the full **model card** included with this project documentation.


## RESULTS
The analysis of YouTube channels through clustering and classification techniques has yielded insightful results, summarized as follows:

Clustering Results
- Five distinct topics were identified, shedding light on the diverse content types prevalent on YouTube, from gaming and vlogging to music and educational content. Notable overlaps in content themes indicate the multifaceted nature of YouTube channels.

Classification Results
- The RandomForestClassifier demonstrated a solid performance, achieving a cross-validation score of 81.01% and an independent test score of 79.49%. The model effectively categorized channels into 'Popular', 'Influential', and 'Elite' based on various metrics, although the precision for 'Elite' channels was found to be lower, suggesting room for improvement.

Continuous Improvement
- The findings suggest potential enhancements in model precision through the integration of more comprehensive datasets, which could refine the predictions and reduce misclassification rates.

For a detailed breakdown of each topic, the specific words associated with each cluster, and a more thorough analysis of the RandomForestClassifier’s performance, including the confusion matrix, please refer to the MODEL CARD. This document provides extensive details on the methodologies used, the data analyzed, and the in-depth results obtained from this study.
This revised section:
