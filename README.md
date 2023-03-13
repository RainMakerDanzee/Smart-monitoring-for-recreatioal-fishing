# Smart-monitoring-for-recreatioal-fishing
The mission for this project was to collect many images of fish, label the quality of  each image, and train an AI model to identify the species of fish in an image using  this new dataset. 
We collected a total of 2,040 images. We found the most effective method was  taking screenshots from Facebook fishing groups and other online forums. In this  report, we explain how we did this and have further discussion on other methods,  including web scraping and manual photography. 
With this dataset, I have created a Jupyter Notebook for  training and evaluating an AI model based on MobileNetV2. To integrate Labelbox,  we had to fork the repository on Github to create a patch, and then compile this  custom Labelbox python package in the notebook. With this patch, the python  script can download directly from the Labelbox server using the API key. This process  is slow but effective, usually taking 5 minutes. 
We used Google Colab setup with a graphics card to run this notebook in the  cloud as it does not require heavy compute and can be completed in less than half  an hour. The performance of this AI model was measured at 87.76% accuracy when  identifying 14 different species. 
This Jupyter notebook is fully automated and will allow you to present your work  as an effective proof of concept achieving a solid level of performance. More data  can easily be collected. It is recommended that the project now is ready to move forward into real world testing and data collection using cameras at fish cleaning tables. Fine tuning is still needed and this small project needs further optimization to yield accurate results. 



The test images were used to evaluate the performance of the artificial  intelligence model. Our key metric is accuracy which measure the proportion of  predictions the model made correctly. 
Model Evaluation Statistics 
Species count: 14
Test Loss: 0.44057
Test Accuracy: 87.76%



Here we note that across 14 species, our model predicted 87.76% of the unseen  testing data correctly. We consider this to be a success. 
Loss during training of the model represents how much the model is changing.  This loss is expected to reduce as the model becomes more accurate. This training  loss reducing to close to zero, representing diminishing returns from further training  after 3 epochs.


