# WIDS Midterm Submission Report
This is a character-level Bigram Language Model is built from scratch. The goal of this model is to predict the next character based only on the current character. It does not use any past context or memory. Due to this limitation, the generated text does not create meaningful sentences. Instead, it appears as broken or random English, which is the expected outcome of a Bigram model.


The program first reads a text file and collects all unique characters so the model knows what symbols it can work with.
Each character is converted into a numerical form because neural networks can only process numbers.
The full text is split into training data and validation data so the model can be trained and also checked for overfitting.
During training, small random chunks of text are selected where the input is a sequence of characters and the target is the same sequence shifted by one character.
The model uses a single lookup table that directly maps a current character to the probability of the next character.
There are no hidden layers or memory units, which means the model only learns character-to-character relationships.
A loss function is used to measure how wrong the model’s predictions are, and an optimizer updates the model to reduce this error.
The training loop repeats this process thousands of times so the character transition probabilities improve.
After training, the model generates text by starting from a single character and repeatedly predicting and appending the next character.
The final generated text is printed and appears as broken English, which confirms that the bigram model is functioning correctly.
