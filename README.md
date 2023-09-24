![text representation](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_sl0zFWi7_DNe07lXtdYC3KJ-J5OS4AnJTEUUtKJYRGkEmBtHFA2Wc2p58q5trmP8pN8&usqp=CAU)
# Text-Representation
NLP techniques apply "machines" to process natural language used by human.
  
We need to translate human langage to machine language!
  
- What human generate:  
![human](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-uaUgkTjRfpvxNGQfFtXq1aJ1FFdM8ZmdBtk0IK3b5AgphbrIBpE0V3yzpqUdDrT6su4&usqp=CAU)

- What machine can read:  
![machine](https://miro.medium.com/v2/resize:fit:960/1*_kbFlq2YypdZUZbdkwjq0g.jpeg)


[Note] This is an essential step for further text processing tasks, such as sentiment analysis, text similairty, clustering, etc. 

 - # Text representation
   - **One-hot encoding**
     ![one-hot encoding](https://cdn-images-1.medium.com/v2/resize:fit:1600/1*0kkqYg0mGpyvqvrMam2k2A.png)
     **What is one-hot encoding**
     - One-hot encoding is a technique used for representing categorical variables as vectors.
     - Size of the vector is 'n', where 'n' is the total number of categories in the data.
     - Each vector has a single '1' at the position corresponding to the category, and '0' everywhere else.
    
     **How to obtain one-hot encoding representation**  
      - For example, when we have a list of numbers 2,4,1,3,3,2,5  
         There are 5 unique numbers (categories) in this data, we can represent each of them as:  
         1: [1,0,0,0,0]  
         2: [0,1,0,0,0]  
         3: [0,0,1,0,0]  
         4: [0,0,0,1,0]  
         5: [0,0,0,0,1]  
       
         The original series of numbers can be represent as the following sequence of vectors:  
         2: [0,1,0,0,0]  
         4: [0,0,0,1,0]  
         1: [1,0,0,0,0]  
         3: [0,0,1,0,0]  
         3: [0,0,1,0,0]  
         2: [0,1,0,0,0]  
         5: [0,0,0,0,1]  
       
     - We can apply this method to represent words where we represent each word from a given vocabulary as a vector.
       Vocabulary:  'can','you','a'   
       word to one-hot representation:  
       can: [1,0,0,0]   
       you: [0,1,0,0]  
       a: [0,0,1,0]  

       We can represent the sentence "can you can a can" with the following sequence of vectors:  
       can: [1,0,0,0]  
       you: [0,1,0,0]  
       can: [1,0,0,0]  
       a: [0,0,1,0]  
       can: [1,0,0,0]  

     **Pros & Cons**   
       - Pros:  
           - Simplicity (straightforward to understand and implement)  
           - Effectiveness for categorical data  
           - Compatibility (many machine learning algorithms require numerical input)  
       - Cons:  
           - High dimensionality (if there are 10,000 words in our vocabulart, we need to represent each word as a 10000-D vector, which will multiply subsequent computational load)  
           - Sparse matrix (lots of zeros)  
           - Incapable of capturing inter-word relationship (for example the words 'good' and 'great' will be just two words with 1 in different positions)
           - Cannot handle new categories (fixed vocabulary size)  


     **Applications in Business Research (Basic but not widely-used)**
     - Examples:
       - Cui Y, Davis AM. Tax-induced inequalities in the sharing economy. Management Science. 2022 Oct;68(10):7202-20.  
  

   - **Bag-of-Words (BOW)**
     ![bag-of-words](https://miro.medium.com/v2/resize:fit:1200/1*3K9GIOVLNu0cRvQap_KaRg.png)
     
     **What is bag-of-words**
     - Bag-of-Words (BoW) is a popular way to represent text data in machine learning.
     - It's called a "bag" of words because the structure of the text (e.g., the order of words) is discarded. 
     - It only considers whether known words occur in the text, not where they occur.

     **How to obtain bag-of-words representation**
     - For example, when we have three hotel online reviews:
       - Review 1: "the experience is amazing and the food i had is fantastic"
       - Review 2: "i had fantastic hotel experience"
     - The vocabulary contains: 'the', 'experience', 'is', 'amazing', 'and', 'food', 'i', 'had', 'fantastic', 'hotel'.
       - Review 1: 'the' - 2, 'experience' - 1, 'is' - 2, 'amazing' - 1, 'and' - 1, 'food' - 1, 'i' - 1, 'had' - 1, 'fantastic' - 2, 'hotel' - 0;
       - Review 2: 'the' - 0, 'experience' - 1, 'is' - 0, 'amazing' - 0, 'and' - 0, 'food' - 0, 'i' - 1, 'had' - 1, 'fantastic' - 1, 'hotel' - 1;
       - Note: the number indicates the frequency of each word
         
     **Pros & Cons**
     - Pros:
       - Easy to understand and implement
     - Cons:
       - High dimensionality (same as one-hot-encoding, vector dimension is decided by the vocabulary size)
       - Order information loss (because it treats all words equivalently regardless of their order)
       - Sparse matrix (lots of zeros)
  
     **Note:** A typical topic model - Latent Dirichlet Allocation (LDA) - processes documents as a bag of words becuase its inferrence is based on word co-occurance while ignoring word order  
   
     **Applications in Business Research (Popular before 2017)**
     - Examples:
       - Mankad S, Han HS, Goh J, Gavirneni S. Understanding online hotel reviews through automated text analysis. Service Science. 2016 Jun;8(2):124-38.
       - Eliashberg J, Hui SK, Zhang ZJ. From story line to box office: A new approach for green-lighting movie scripts. Management Science. 2007 Jun;53(6):881-93.  
         
 
   - **Term Frequency-Inverse Document Frequency (TF-IDF)**
     
     **Applications in Business Research (Popular before 2017)**
     - Examples:
       - Xiang Z, Du Q, Ma Y, Fan W. A comparative analysis of major online review platforms: Implications for social media analytics in hospitality and tourism. Tourism Management. 2017 Feb 1;58:51-65.
       - 
      
         
   - **Word Embedding**
     - Word2Vec
     - GloVe
     - FastText
       
   - **Document embedding**
     - Word embedding aggregation
     - Doc2Vec

   - **Transformers-based embedding**

   - **Topic modeling**

     
