# Mercado Libre Data Challenge 2019

Here is the code I used to achieve the #11th place during the training phase and #12th when the final scores were calculated. The final leaderboard can be checked [here](https://ml-challenge.mercadolibre.com/final_results) (username nmacian).

## Challenge assets
The official site for the challenge is [here](https://ml-challenge.mercadolibre.com/) and the rules are [here](https://ml-challenge.mercadolibre.com/rules).

The training and test datasets can be downloaded from [here](https://ml-challenge.mercadolibre.com/downloads).

The remaining assests needed to run my code can be found [here](https://ml-challenge.mercadolibre.com/workshop).

The model I built was based in the one provided by Mercado Libre. The original Colab can be visited [here](https://colab.research.google.com/drive/1YW5PlZdA26WpdJ87DiudCq8FVExgiR6v#scrollTo=hBd-gvH_RHEh). I cleaned the data and tuned hyperparameters to achieve a 0.9048 score (compared to the 0.875 obtained in the original model).

## Coding environment

During almost all the competition time I used Google Colab as my coding environment, where GPU usage is quite limited. It wasn't until the last 2 days of the challenge that I managed to run on Google Cloud, but I didn't have much time those final days to continue improving the model result. 

## Data cleaning and subsampling
As I didn't have access to more powerful processing until the end, I had to subsample the original data to almost half of its original size. The cleaning function and subsampling strategies can be found in "Sampling_Spanish" and "Sampling_Portuguese" notebooks.

## Model
The given model uses a Fastai library.

I made two different models to classify Spanish and Portuguese titles. At the end I joined the results.

In order to run the model you need to download the vocabulary language model provided by Mercado Libre. After cleaning and sampling the data you can run the two models and obtain the two submission files that need to be combined.

## Merge results

The notebook "JoinResults" takes the two inputs and takes the Spanish titles classified by the Spanish model and the Portuguese titles classified by the other model. Then it sorts the results and gives the expected format.


## Next steps

As I didn't have much time to use Google Cloud, here is what I would have done:
- Train two vocabulary databunches after cleaning the data, one for each language.
- Train the two models with all the available data.

My guess is that the overall performance would improve and get a higher result.

## License
[MIT](https://choosealicense.com/licenses/mit/)