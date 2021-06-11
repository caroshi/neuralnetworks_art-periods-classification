# Classifying Art Periods with Neural Networks
Caroline Shi

## Abstract
There are certain stylistic indicators such as color palette, brushstroke, and subject matter that suggest a certain art period to the human eye. Using a neural network model, I explore the capabilities of my model and its ability to distinguish art periods based off of these indicators in each work. Starting off as a two class classification problem, I eventually expand to a five class model to parse out the strengths and weaknesses of applying neural networks to art and which art periods are more easily classified than others. 

## Design 
The goal of this project was to build an neural network model that classified art periods for paintings. I started off with a binary classification of Impressionism and Post-Impressionism paintings with 1,000 images per class. This model proved to be difficult and gave very poor metrics with little improvement with continual tuning-- I think due to the similarities in style with the two art periods, a basic CNN model had a hard time classifiying the two. I moved onto a new binary model with Surrealism and Neo-Classicism, initially using CNN, that gave me a train accuracy score of 0.838 and val score of 0.720. Image augmentation with both models made my model perform significantly worse, I believe due to the fact that classifiying paintings is so reliant on minute details and texture of the canvas. Applying a MobileNet model with dropout and no augmentation gave me a balanced model with 1.0 and 0.925 accuracy for train and val respectively. 

I moved onto a 3 class model, incorporating Impressionism paintings back into the fold, with 1,000 images per class. Applying a tuned CNN model gave me a baseline score of 0.967 and 0.646 accuracy, indicating a lot of overfitting. Adding in more data for a total of 2,000 per class in addition to using VGG16 with feature extraction brought my val score up to 0.805. 

Lastly, I tried a 5 class model, incorporating Romanticism and Expressionism paintings. I purposely chose two art periods that would have some stylistic overlaps with my existing art periods to see how well my model would be able to handle the similarities. Apparently, it could not handle it well, with an accuracy of 0.561. With some fine tuning and additional data, I think the model will be able to perform better. 

## Data
Kaggle has a comprehensive dataset of ~100,000 images of paintings ranging from the Renaissance to Cubism. In order to maintain a balanced dataset, I grabbed 2,000 image per class for a total of five art periods. In addition to the images, the dataset includes a corresponding csv file of tabular data including: 

1. Artist
2. Date
3. Title 
4. Style (this is where I can grab the work's art period)
5. Genre (this pertains more to the work's subject matter)
5. Pixels, x-axis
6. Pixels, y-axis


## Algorithms
* _Modelling_
	* Tried CNN with parameter, tuning, image augmentation
	* Tried MobileNet, VGG16 with feature extraction and parameter tuning 
		
* _Visualizing Data_
	* Used Matplotlib to create visualizations looking at model accuracy

## Tools
* OS, Pathlib for pulling my images and organizing into directories 
* Numpy, Pandas for EDA
* Matplotlib for data visualization
* Keras/Tensorflower for modelling and analysis
* Google Colab for cloud computing 

