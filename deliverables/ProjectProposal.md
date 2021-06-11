# Deep Learning Project Proposal 

## Question: 
There are certain stylistic indicators such as color palette, brushstroke, and subject matter that suggest a certain art period and provenance. As an art history enthusiast, I would like to see if it is possible to build a neural network model that predicts the art period and style of a painting based off of these indicators in each work. Starting off as a two class classification problem with Impressionist and Post-Impressionist works, I would like to expand my model to a multi class predictor if possible. Time allowing, it would be interesting to build another model that classifies the work's subject matter (abstract, portrait, landscape, etc.)

## Data: 
Kaggle has a comprehensive dataset of ~100,000 images of paintings ranging from the Renaissance to Cubism. I will initally grab only Impressionist and Post-Impressionist works for a total of ~2,000 per class. In addition to the images, the dataset includes a corresponding csv file of tabular data including: 

1. Artist
2. Date
3. Title 
4. Style (this is where I can grab the work's art period)
5. Genre (this pertains more to the work's subject matter)
5. Pixels, x-axis
6. Pixels, y-axis

## Tools:
* Numpy, Pandas for processing data, EDA
* Keras for modelling and analysis
* Matplotlib, Tableau for visualization
* Google Cloud for data storage

## MVP:
I plan to have a two class classification model running with my parameters tuned for optimal accuracy. Ideally, I will have expanded my model to multiple genres. 