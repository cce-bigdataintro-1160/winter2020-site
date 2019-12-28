* [Insurance Claim](https://www.kaggle.com/easonlai/sample-insurance-claim-prediction-dataset)
* [Heart Disease at UCI](https://www.kaggle.com/ronitf/heart-disease-uci)
* [Top spotify tracks of 2018(not "prepared")](https://www.kaggle.com/nadintamer/top-spotify-tracks-of-2018)
* [Titanic Challenge(not "prepared")](https://www.kaggle.com/c/titanic/data)

1. Choose one of the datasets above and explore the dataset webpage, read the documentation and author's proposal
2. Load the dataset using pandas
3. Print the dataframe statistical summaries looking for:
  * Relevant variables
  * The dimensions of the dataset
  * Variables with empty values
  * Variables to be cleaned, corrected or enhanced
4. Ask at least one question you can answer by using the dataframe filtering through predicate like:
`df_name[df_name['Age'] > 30]`. For example, using the Spotify dataset try to find the 10 most `danceable` songs.
5. Use the method `df['my_column'].value_counts()` on a categorical column.
6. Check the correlation of the variables in your dataset!
7. Plot everything you need in order to understand this dataset and its correlations. You can use all the techniques we learned in the previous classes. Make sure to do plots with 2+ dimensions at the same time.
8. Finally, choose a variable to be used as target and run your classification or regression.
9. Check if your score is acceptable and try to optimize by chainging your algorithm, hyperparameters, data split or selecting your features!
