# Machine learning-based Language classification of multilingual content written in Bengali.

**Problem Statement**

The exponential growth of social media provides platforms for empowering freedom of expression and individual voices. In social media, users express their expression using different languages, such as Bengali and English. But many users use the Bengali alphabet to express other languages such as Bengali, Chakma, Marma, Chittagonian, Sylheti Etc. So classifying the different lingual contents written in the Bengali alphabet is a challenging task. As far as we know, substantial progress has yet to be made in organizing the multilingual content written in the Bengali alphabet. This project applies modern machine learning models to classify the multilingual contents in the written Bengali alphabet.   


**Dataset**

We gathered multilingual content written in the Bengali alphabet from social media platforms.  Currently, our dataset has around 1000 content, with four content types representing Bengali, Chittagonian, Sylheti and Chakma languages, respectively. It contains 250 Bengali content, 250 Chittagonian content, 250 Sylheti content and 250 Chakma content. We will increase the number of contents in the dataset. 

![dataset](https://user-images.githubusercontent.com/116121494/213540770-77fb9142-d444-41e6-bf10-aa4fc87468ac.png)


**Sample of dataset**

![Screenshot (97)](https://user-images.githubusercontent.com/116121494/213538914-55bc6dab-1612-4703-abe3-a568e1e035f5.png)

**Approach**

We implement machine learning approaches for classifying the contents according to their language. The raw contents contain special characters, e.g., @, #, - Etc., punctuations. At the time of preprocessing, we have to remove these special characters and punctuation. Multilingual contents written in the Bengali alphabet have many unique words. For example ‘Where are you going?’ represent  in Bengali “আপনি কোথায় যাচ্ছেন?”, in Chittagonian ‘অঁনে হঁডে যাইতালাইজ্ঞুন?’, in Chakma ‘তুই হুদু ঝোড়?’ and in Sylheti ’ আপনে কই যাইতা?’. There is some common word such as 'আমি', 'তুমি', 'ভাত' Etc. We also have to remove those common words from the dataset. We need a list of words and the frequency with which they appeared in each content. This can be done by preprocessed the content. Then we have to extract the features from the contents. Using those extracted features we can train the machine learning models. 


![model2](https://user-images.githubusercontent.com/116121494/213540081-bcec5d82-f6ff-4aa1-ab65-4065d9484529.png)


**For classifying the contents according to their language we used the following steps:**

Step 1: Collect the various contents by writing them in Bengali alphabet. We collect the contents from different social media, newspaper, article Etc. The contents are different from each other and consists of a large number of unique words.

Step 2: Removed special characters, punctuation, stop words, and frequent terms from the content. For collecting the actual feature from the content, we removed the special characters, punctuation, stop words, and frequent terms from the content. 

Step 3: We utilized tokenizer to tokenize the data after deleting superfluous components. In this step we use tokenization to separate the individual word from content.

Step 4: We now have a list of terms and the frequency with which they appeared in each piece of content. The feature was then extracted from the material using tf-idf. Full form of if-idf is Term Frequency Inverse Document Frequency. 

Step 5: We then divided the dataset into 80% for training and 20% for testing. 

Step 6: We then trained a variety of machine learning models to categorize the contents. 
*Machine Leaning Models used:*
•	Logistic Regression
•	Decision Tree
•	Random Forest
•	Multinomial Naive Bayes
•	K-Nearest Neighbor
•	Linear Support Vector Machine
•	RBF Support Vector Machine

Step 7: We used a test dataset to assess the machine learning models. We plot confusion matrix for each model. Then we calculate precision, recall, accuracy, F1-score for each model. We evaluated our machine learning approaches using different test contents from our created dataset. In this case, machine learning models performed well for the Unigram feature. 

Step 8: Using the evaluated findings, we selected the best machine learning model. The Logistic Regression model outperformed the other machine learning models for Unigram features. Using the classifier model, we examined a variety of contents written in Bengali. We achieved 98% accuracy using the Logistic Regression with Unigram feature.

![Screenshot (99)](https://user-images.githubusercontent.com/116121494/213541212-b4625ddf-8134-42db-839d-601b10891057.png)


Step 9: We then used the Logistic Regression model to forecast the unlabeled content.

**Input Content:**

1. একটা ভাল খবর এবং, একটা ভাল উদাহরণ, কি ভাবে সঠিক সরকারি নীতির সাহায্যে দেশী বিনিয়োগিরা একটা শিল্পকে এগিয়ে নিতে পারেন। 
2. যে জাগাত নিজো লেঘালোই বানান সুধোম থিক গরিহ্ ন পারিয় সে জাগাত বাংলা/রোমান লেঘালোই কি পারিবং? কি দঝা ভিলি! এধক বঝরেও নেই একখান দোল বানান সুধোম
3. আই আইলে অঙ্ককা গর। আগর ডইল্লা দেইন নো ফার, আই তো বুঝির বেয়াগ্গিন। মানা গইল্লে আর নো আইস্সুম হন দিন হন দিন, মানা গইল্লে আর নো আইস্সুম হন দিন হন দিন| 
4. আউসে মাইরে দিছলায় লাই খেলার মোটা ফুসকুনি। তাইন আরও দূর গিয়া, হফার থাকি ছিঁইড়া আনতা মুরগাঝুঁট ফুল। তানরে দিসলায় ঝন ঝন ঝন কইরা বাজে এমন ফিতলর হান্ডি বাসন। 

**Output Content:**

![Screenshot (96)](https://user-images.githubusercontent.com/116121494/213541830-267f9c5e-4c2c-462f-9096-b69fde5470d9.png)



**Conclusion**
This project has been conducted to offer an approach for classifying multilingual content writing in the Bengali alphabet. With the experiment's findings, we could classify the original language of content writing as Bengali alphabets. With all of the conclusions of this experiment, it is possible to infer that the approach is an efficient and accurate method for classifying the contents written in Bengali alphabets. 

