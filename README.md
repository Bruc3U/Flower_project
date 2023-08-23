# 🍁 Image Recognition Project 

![japanese_red_maple (42)](https://github.com/Bruc3U/Flower_project/assets/142362478/72a4528d-3fe2-4ff9-9723-eec00942e300)

# Tool Used
- Google Cloud (ML, Bigquery)
- Excel
- Python (seaborn, pandas)


## Objective

In the midst of machine learning development, PictureThis a plant recognition app, sparked our interest.<br>
Developed by the private company Glority, which was founded in 2009, their new app PictureThis allows users to take a photo of any plant and get an accurate result.<br>

PictureThis allows users to recognize plant species and also to have an analysis of the plant’s health, through pictures.<br> 
The app will let you know the current health state of your plant as well as recommendations on how to treat the condition. 
Since this kind of technology can be quite expensive to develop our question will be to test a similar version on Google Cloud’s platform.<br>

With a budget of 50 USD, our goal will be to create an accurate version of the app. We will only focus on the plant recognition techniques and leave the other features for a future project.<br>
Being able to create a more cost-effective version of the technology could be useful for smaller structures that do not have the resources to hire a dedicated team on such a project. 


## About the dataset

Our project will feature 3 different species of maple trees: [Acer palmatum](https://github.com/Bruc3U/Flower_project/blob/main/acer_palmatum%20(44).JPG) (regular maple tree), [Japanese maple](https://github.com/Bruc3U/Flower_project/blob/main/japanese_maple%20(11).JPG), and the [Japanese red maple](https://github.com/Bruc3U/Flower_project/blob/main/japanese_red_maple%20(17).JPG).<br> 
Most of the pictures were taken at the Dallas Botanical Garden.<br>

Our training dataset is composed of 300 pictures (100 pictures per plant species), 80% of those pictures will be ‘live’ pictures, and the remaining 20% will be online pictures.<br> 
Our train and test dataset will have both high-quality pictures (80% taken from a Sony Camera, 21Mp) and regular-quality pictures (20% taken from an iPhone 11,12Mp). Since the app can also accept saved pictures.<br>

On another note, the raw data was collected on a sunny day, with normal exposure, since our time and budget are restricted, capturing accuracy with different lighting will be part of another endeavor.<br>
Our project will focus on standard cases, which means that our pictures will feature only the top part of the leaf, the app does not support other sides and asks for a clear, well-lighted picture. <br>

The obvious limitation of our dataset is the number and variety of pictures.<br>
Machine learning performs better on larger datasets with a lot of examples to ‘learn’ better. We will be accepting differences in accuracy.<br>

 The test data set is composed of 20 randomly selected pictures from a 100-picture pool. Those pictures will appear in 12 and 21 Mega Pixel, some will have hands or shadows to try to ‘trick’ the prediction software. 
 

| Species | Population (out of 20) | Low Quality | Hands | 
|---|---|---|---|
| Acer Palmatum | 11 | 4 | 1 |
| Japanese Maple | 6 | 2 | 3 |
| Japanese Red Maple | 3 | 0 | 1 | 

# I/Data Wrangling: 

Once the pictures were taken the only ‘cleaning’ step was to convert most of the files into a similar extension such as JPG and rename the files to have a better classification.<br>
A CSV file was also created to have a proper path to the data (required by Google Cloud). 

After gathering and cleaning the data, we finally fed it to the Google Machine Learning API. 

# II/ Analysis:

We can observe that the overall accuracy for Google Cloud was 75% whereas the PictureThis app is 100%.<br> 
Google Cloud’s predictions were given with the number of percentages predictions for each species, when the software had more than 50% accuracy in one column it would count as a correct prediction.

The app did not have any trouble differentiating the 3 species despite changes in quality. The result was fast and accurate.<br>
Whereas the Google Cloud model suffered from a lack of accuracy on certain models. It could be explained by the similarity of the two species. Indeed, the Japanese maple and the red maple are really similar in terms of leaf shape. 

| Plant type | Accuracy | Total population |
|---|---|---|
| Acer Palmatum | 100% | 55% |
| Japanese Maple | 66% | 30% |
| Japanese Red Maple | 33% | 15% | 

| Plant type | % of hands | % of low-quality pictures (Iphone) |
|---|---|---|
| Acer Palmatum | 9% | 36% |
| Japanese Maple | 50% | 33% |
| Japanese Red Maple | 33% | 0% | 

As we can also observe, the overall picture quality did not influence the model’s outcome nor did the hands present in the backgrounds. Half of the Japanese Maple folder was with Hands and more than 1/3 were lower quality, still, it outperformed the Japanese Red Maple. 


# Conclusion

Despite its lack of overall accuracy, Google Cloud’s platform seems to be a reliable form of prediction. Limitations were accepted due to the lack of raw data but for a 10-hour project, the results were more than acceptable. 
The app PictureThis is a fantastic tool and incredibly precise but for a small business, it’s a heavy price to pay.
Google's platform offers affordability and reliability for a cheap price, more importantly, it widens access to high-tech processes for an unspecialized workforce. This project was conducted without major coding or major AI knowledge. The only challenging part was to find proper raw data and clean it according to Google Cloud’s rules. 









