# Swiggy-TechStein-2018
Swiggy TechStein Open Hackathon 2018

Present day swiggy reccomendations are restaurand based. But food items available in any reccomended restaurant is so diverse that it does not look like a reccomendation from viewpoint of user's taste.
For example, if I like chinese food, I would like to be recommended more variety in chinese food from those restaurants which have been liked by many users having similar taste like me.
Developing a food recommendation engine has been challenging given the sparsity isues. We wanted to leverage large datasets available with swiggy to build a fast and efficient model.
With no ratings data provided, we wanted to do collaboration filtering with implicit feedback being number of times user has ordered that particular item. We experimented with several models like user-user similarity based, SVD++ and finally came across the following paper Hu, Koren et al "Collaborative Filtering for Implicit Feedback Datasets". Paper describes that implicit user observations should be transformed into two paired magnitudes: preferences and confidence levels.  In other words, for each
user-item pair, we derive from the input data an estimate to whether the user would like or dislike the item (“preference”) and couple this estimate with a confidence level.


we built a dish based food recommendation rather than restaurant based recommendation system. 

some recommendation based on previous order

login page
![swiggy login-1](https://user-images.githubusercontent.com/32159487/42841529-feafad94-8a27-11e8-88cc-90a15a49bed4.png)
recommendation for different users
![10014484 html-1](https://user-images.githubusercontent.com/32159487/42841611-3eeddd36-8a28-11e8-87ca-8926ee62c05f.png)


![10006285 html-1](https://user-images.githubusercontent.com/32159487/42841646-57769654-8a28-11e8-8a5b-135082547a26.png)


![10001756 html-1](https://user-images.githubusercontent.com/32159487/42841662-6d36e85e-8a28-11e8-963b-ee534ed1e205.png)


![10001491 html-1](https://user-images.githubusercontent.com/32159487/42841699-868858f6-8a28-11e8-8d0f-8e6e0751a392.png)
