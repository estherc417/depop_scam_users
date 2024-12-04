# Depop Scam Users Detection Using Neural Networks and Machine Learning

#### This project uses a variety of machine learning models, neural networks, and clustering techniques to identify scam users and listings from the secondhand E-commerce platform Depop.

### Dataset
The dataset includes:

User metadata: logged-in time, number of sold or bought items, etc.
Post descriptions: text content analyzed for scam-like word usage using NLP techniques.
Behavioral data: posting frequency, interactions, and reviews.

User dataset was split into three groups through annotation for purpose of analysis: 

Real users: users that were verified to be authentic 
New users: a subset of real users that shared similar characteristics with scam users (lack of reviews, no sold or bought items)
Fake users: users that would post fake listings using photos that weren't their own 

All personal and sensitive data is omitted to comply with privacy policies.

### Models and Techniques 
Scraping: developed a Depop user's username Cloudscraper as well as scraping product and user variables using open-source Github code (credits below) 

Tree-based models: OHE for categorical features, bag-of-words feature for 1000 most common words, 

&emsp; Random Forest model: reduced variance, model accuracy was 99.5%
  
&emsp; Decision Tree model: less overfitting, fastest compile and run time, model accuracy was 99.6%
  
&emsp; Gradient Boosting (XGBoost) model: minimized loss, better accuracy than RF, model accuracy was 99.7%
  
Sentence Embedding NN model: specifically to differentiate new and scam users, utilized pretrained RoBERTa model for NN with ReLU activation and adam optimization. Product descriptions embedded on a sentence-level used as input variables. Highest accuracy at 99.9%. 

### Credits
Code was adapted from Github user gertje823 for scraping product and user variables https://github.com/Gertje823/Vinted-Scraper/tree/main. 
Project credits and collaboration: Zekai Hu, Bofei Xu, Kylie Ren, Serena Bai

### P.S. 
Some files were unable to be adapted to Github as a result of being developed over Google Colab. Please email estherchoi4@berkeley.edu for more access. 
