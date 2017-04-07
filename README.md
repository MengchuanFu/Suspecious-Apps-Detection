# Suspecious-Apps-Detection
With the rapid adoption of smartphones, tablets, and mobile apps, they are increasingly becoming part of children’s daily life for amusement and education. In order to help parents determine age-appropriate mobile apps for their children, iOS apps come with maturity ratings that are similar to the movie and video game industry. Such maturity ratings examine the existence and intensity of mature themes such as mature content, violence, offensive language, sexual content, and drug usage within each app. However, movie and video game industries have official rating organizations such as the Motion Picture Association of America (MPAA) and Entertainment Software Rating Board (ESRB), which set standards for film rating systems – mobile apps do not. Instead of having standard rating rules across platforms, each mobile platform establishes or adopts its own rating policy and rating strategy. iOS’s policy provides four different maturity-rating levels based on the suitable age of audience: “4+,” “9+,” “12+,” and “17+.” The rating systems classify types of objectionable content into four maturity levels. According to our best knowledge, little systematic research has conducted to analyze the problems with apps’ maturity rating policy and their implementation for children’s protection. Thus, the risks associated with content inappropriateness is unknown. This project develops mechanisms to compare, analyze and verify the maturity ratings of mobile apps and in-app advertisements, and investigates the possible reasons behind the inaccurate ratings.
<br /><br />Dataset Overview:
44840 Apps data with titile, description and maturity rating<br />
Crawled from Apple App Store
<br /><br />Suspecious Apps Detection - 10 Nearest Neighbor Approach.ipynb verified the possibility of using k-nn method in the maturity rating research and found suspicious apps for the use of future Mturk survey

1. Import the data, examine the shape and distribution
2. Data preprocessing: regular expression, lowercase, remove stop words
3. Randomly selection
4. Count the amount of overlapes words on descriptions for each pair of Apps among our selected dataset
5. For each app, select top 10 apps that have max overlaps words on description
6. Predict true maturity rating for each app by "top 10 apps" ratings (Majority Voting)
7. Further analysis
