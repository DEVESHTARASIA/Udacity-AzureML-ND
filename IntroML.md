### Data Science Process is as follows:
1. Collect Data - Quering Databases, Retrieving Files, calling web services, or scraping webpages
2. Prepare Data - [Pre-process](https://www.geeksforgeeks.org/data-preprocessing-in-data-mining/) data to be suitable for model training and testing
3. Train Model - [Feature Vectorization](https://machinelearningmastery.com/prepare-text-data-machine-learning-scikit-learn/), [Feature Scaling](https://towardsdatascience.com/all-about-feature-scaling-bcc0ad75cb35), Tuning/Choosing with various [metrics](https://towardsdatascience.com/20-popular-machine-learning-metrics-part-1-classification-regression-evaluation-metrics-1ca3e282a2ce)
, preparing the pipeline 
4. Evaluate Model - Final Test on validation database 
5. Deploy Model - Part of DevOps, training, evaluation and deployment scripts are combined for respective build
5. Retraing the model with fresh data to suit the data environment needs. An iterative step

### Types of Data
- Numerical
- Text
- Time-series(includes speech)
- Categorical
- Image
- *Tabular Data(multiple objects(rows) with multiple features(columns))*

*It's all numerical in the end. The model works with numbers, so others are transformed to numerical*

### Scaling Data/Features
Scaling data means transforming it so that the values fit within some range or scale, such as 0–100 or 0–1. Algorithm doesn't understand units. It doesn't understand that 10A can be a lot but 10m can be very less.

__Why scaling data helps:__
* The output of the algorithm is not affected
* Can help speed up training as the algorithms need to handle numbers less than the given range

__When to Scale data:__
Rule of thumb is too scale it whenever algorithm uses distance(similarities) or assumes normality. For ex, you need to scale in k-means neighbours(euclidean distance based), but not required in [tree based model](https://www.quora.com/Decision-Tree-based-models-dont-require-scaling-How-does-scaling-impact-the-predictions-of-decision-tree-based-models).

![When to scale](https://i.stack.imgur.com/OKOsB.png)

__Ways to scale data:__(Done over each feature)
* *Standardization* rescales data to have mean = 0 and variance = 1

    x' = (𝑥 − 𝜇)/𝜎 
* *Min-max Normalization* rescales data to range [0,1]
    
    x' = (x-x<sub>min</sub>)/(x<sub>max</sub>-x<sub>min</sub>)
* *Scaling to unit length*
  x' = x/||x||

### Converting to Numeric Data
