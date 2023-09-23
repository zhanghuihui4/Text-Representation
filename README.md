![text representation](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT_sl0zFWi7_DNe07lXtdYC3KJ-J5OS4AnJTEUUtKJYRGkEmBtHFA2Wc2p58q5trmP8pN8&usqp=CAU)
# Text-Representation
NLP techniques apply "machines" to process natural language used by human.
  
We need to translate human langage to machine language!
  
- What human generate:  
![human](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-uaUgkTjRfpvxNGQfFtXq1aJ1FFdM8ZmdBtk0IK3b5AgphbrIBpE0V3yzpqUdDrT6su4&usqp=CAU)

- What machine can read:  
![machine](https://miro.medium.com/v2/resize:fit:960/1*_kbFlq2YypdZUZbdkwjq0g.jpeg)


[Note] This is an essential step for further text processing tasks, such as sentiment analysis, text similairty, clustering, etc. 

 - # Word representation
   - **One-hot encoding**
     - One-hot encoding is a technique used for representing categorical variables as vectors.
     - Size of the vector is 'n', where 'n' is the total number of categories in the data.
     - Each vector has a single '1' at the position corresponding to the category, and '0' everywhere else.
       
       For example, when we have a list of numbers 2,4,1,3,3,2,5  
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
    
   - **Bag-of-Words (BOW)**
   - **Term Frequency-Inverse Document Frequency (TF-IDF)**
   - **Word Embedding**
     - Word2Vec
     - GloVe
     - FastText
   - **Transformers-based embedding**

 - # Document representation
   - **Bag-of-Words (BOW)**
   - **Term Frequency-Inverse Document Frequency (TF-IDF)**
   - **Topic modeling**
   - **Document embedding**
     - Word embedding aggregation
     - Doc2Vec
   - **Transformers-based embedding**
     
