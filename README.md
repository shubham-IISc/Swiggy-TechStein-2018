# Swiggy-TechStein-2018
**Swiggy TechStein Open Hackathon 2018**

Present day swiggy reccomendations are restaurand based. But food items available in any recommended restaurant is so diverse that it does not look like a recommendation from perspective of user's taste.

For example, if I like chinese food, I would like to be recommended more variety in chinese food from those restaurants which have been liked by many users having similar taste like me.

Developing a food recommendation engine has been challenging given the sparsity issues. We wanted to leverage large datasets available with swiggy to build a fast and an efficient model.

With no ratings data provided, we wanted to do collaboration filtering with implicit feedback but also utilizing the information about number of times given user has ordered that particular item in some way. We experimented with several models like user-user similarity based, SVD++ (generated similar recommendations for all users when we considered number of times user has ordered as explicit feedback) and finally came across the following paper **Hu, Koren et al "Collaborative Filtering for Implicit Feedback Datasets"**. Paper describes that implicit user observations should be transformed into two paired magnitudes: preferences and confidence levels.  In other words, for each user-item pair, we derive from the input data an estimate to whether the user would order or not order the item (“preference”) and couple this estimate with a number of times user will order("confidence"). 

We finally went on implementing this suggested ALS model and obtained AUC-ROC score of .85 while predicting if user would order an item or not for the test set. Also training time for 100 iterations is less than a minute even with more than 1 million order-id's provided in the training set. All the recommendations are generated at run-time with negligible latency requirement.

Details about the dataset and results of preprocessing to feed into our model has been shown in the presentation as well as in jupyter notebook codes. Following are some of the screenshots of the interface developed by us:

**NOTE**:Each item-id mentioned along with a image is unique to a restaurant and an item. Exact name of restaurant and item corresponding to given item-id were not disclosed to us by swiggy.



login page
![swiggy login-1](https://user-images.githubusercontent.com/32159487/42841529-feafad94-8a27-11e8-88cc-90a15a49bed4.png)
recommendation for different users
![10014484 html-1](https://user-images.githubusercontent.com/32159487/42841611-3eeddd36-8a28-11e8-87ca-8926ee62c05f.png)


![10006285 html-1](https://user-images.githubusercontent.com/32159487/42841646-57769654-8a28-11e8-8a5b-135082547a26.png)


![10001756 html-1](https://user-images.githubusercontent.com/32159487/42841662-6d36e85e-8a28-11e8-963b-ee534ed1e205.png)


![10001491 html-1](https://user-images.githubusercontent.com/32159487/42841699-868858f6-8a28-11e8-8d0f-8e6e0751a392.png)
