# Module_14_Challenge
In this challenge I combined my algorithmic trading skills with my skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.

## Establish a Baseline Performance
In this section, I simply ran the provided starter code for this challenge in order to establish a baseline performance for the trading algorithm. The results were as follows:

Classification Report:

![image](https://github.com/tjohnce55/Module_14_Challenge/assets/144564878/8b5e1ba4-6d5f-447d-b057-fcc5a2437761)

![baseline_returns_plot](https://github.com/tjohnce55/Module_14_Challenge/assets/144564878/98118039-7d01-472b-a4fa-6dc02a668946)

## Tune the Baseline Trading Algorithm
Step 1: Tune the training algorithm by adjusting the size of the training dataset.
What impact resulted from increasing or decreasing the training window?
Increasing the training window from 3 months to 6 months improved the accuracy of the model slightly, from 0.55 to 0.57. I also tried decreasing the training window from 3 months to both 1 and 2 months, but this did not seem to have an impact on the accuracy of the model. As I move on to the next step in tuning my model I will keep the training window at 6 months.

Step 2: Tune the trading algorithm by adjusting the SMA input features.
What impact resulted from increasing or decreasing either or both of the SMA windows?
Both increasing and decreasing the short SMA window seemed to have a negative impact on the accuracy of the model. The only adjustment to the SMA windows that seemed to improve the accuracy slightly was to increase the long window from 100 to 150, therefore I will keep 150 as the long window.

The results of the tuned trading algorithm were as follows:

Classification Report:

![image](https://github.com/tjohnce55/Module_14_Challenge/assets/144564878/e78220b8-138e-4599-a447-e22774a505b1)

![tuned_algo_returns_plot](https://github.com/tjohnce55/Module_14_Challenge/assets/144564878/d99647de-2daa-4bd0-a3bf-0e94b1535fed)

## Evaluate a New Machine Learning Classifier
In this step I backtested the new model to evaluate its performance. I used the Decision Tree Classifier in this step. The results of using this classifier to fit the data were as follows:

![decision_tree_classifier_returns_plot](https://github.com/tjohnce55/Module_14_Challenge/assets/144564878/b5c650db-b272-4472-bdae-8114af217533)

## Conclusion
Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?
In conclusion, all three models ended up outperforming the actual cumulative returns over the time period analyzed. The new model that used the Decision Tree Classifier to fit the data and the tuned trading algorithm both performed better than the baseline model. The new model reached a higher cumulative return compared to the tuned trading alorithm, but due to a drop in the cumulative return of the new model at the end of the time period analyzed, the tuned trading algorithm finished with a slightly higher cumulative return than the new model. Therefore I would give the edge to the tuned trading algorithm as the best performing out of the three models.
