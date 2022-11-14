# Text Mining Assignment 

* Create a Python notebook with a function called parse() <br>
* The function should accept 3 parameters: <br> 
  * input_path: the path to the   'amazonreviews.csv' file that we also used in class. <br>
  * index1: the row number that corresponds to a specific review in the given csv (first row would have index1=0) <br>
  * index2: the row number that corresponds to another specific review in the given csv <br>
* The function should return a list of all nouns for which the review at index1 expresses the opposite opinion than the review at index2. <br>
* You should compute the opinion that a review expresses on a noun as follows: <br>
  * Let P be the number of positive words that appear in the same sentence as the noun in the review <br>
  * Let N be the number of negative words that appear in the same sentence as the noun in the review <br>
  * If P>N, then the opinion of the review on the noun is positive. <br>
  * If P<N, then the opinion of the review on the noun is negative <br>
  * If P==N, then the opinion of the review on the noun is neutral. <br>

Example: <br>
suppose that review 1 says: "I really like this product, the quality is perfect. However, the price is unreasonable" <br>
suppose that review 2 says: "This product has a great price." <br>

review 1 has 2 sentences and 3 nouns: <br>

  * I really like this product, the quality is perfect. <br>     
  * However, the price of the product is unreasonable <br>   
  
product: [2,1]: (2 positives, 1 negative) <br>
quality: [2,0]: (2 positives, 0 negatives) <br>
price: [0,1]: (0 positives, 1 negative) <br>

 

review 2 has 1 sentence and 2 nouns: <br>

  * This product has a great price  <br>

product: [1,0]: (1 positive, 0 negatives) <br>
price: [1,0] : (1 positive,  0 negatives) <br>

 
The nouns 'product' and 'price' appear in both reviews. <br>

The overall opinion for 'product' in review 1 is: positive <br>

The overall opinion for 'product' in review 2 is: positive. <br>

The overall opinion for 'price in review 1 is: negative <br>

The overall opinion for 'price in review 2 is: positive <br>

__In this case, the two reviews express an opposite opinion for the attribute 'price'. The first review expresses a negative opinion and the second review expresses a positive opinion.__ <br>

Your function should return ['price'] <br>
