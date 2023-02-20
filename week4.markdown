---
layout: page
title: Week 4
permalink: /week-4/
---

## Week 4

Tried a lot of different models.

baseline models for trying to predict price movement for the next hour. All done with dataset_draft1, which has stock movement indicators
on the daily basis.

LSTM
	30 lag hours - accuracy 50%
	100 lag hours - accuracy 50%
	
SVM (though not really)
	30 lag hours - accuracy 50%

Random Forest (1000 estimators)
	30 lag hours - accuracy 50%
	100 lag hours - accuracy 50%

Probably not a problem with not enough data, as we had 40000 rows, just more that there’s too much noise and not enough features
that explain random movements. It might not be enough data if we decide to lag all the features, as that leads to a sqaure matrix... but
not sure. Other experiments indicate that accuracy with my current dataset using random forest can give 68% accuracy, if it's looking at prediction for the price movement of next day.

