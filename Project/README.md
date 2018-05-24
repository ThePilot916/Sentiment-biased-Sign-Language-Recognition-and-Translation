# Sign Recognition and Translation

NLP_PROJECT 2018

01FB15ECS285 - Shreyas Miraj
01FB15ECS290 - Siddharth Ganesan

image_classifier.ipynb contains all of digital image processing code
  it consists of a multiclass classifier for the alphabets of ASL
  every image fed to the model outputs 5 most probable classes for the given image
  given a sequence of images, it'll form all possible word combinations
  this result is dumped to a file called img_class_output.txt which is further used by language_enhancer.ipynb

language_enhancer.ipynb contains all of NLP code to enhance the output of the raw image classifier model
  first selects all valid words from the list
  if none of them are valid then chooses the ones with the least minEditDistance across the nltk word corpus
  then applies spell correction on them
  this is the language enhanced list
  this list of outputs is further enhanced by enabling sentiment analysis by matching the input and output sentiments


If you want to train the model again then get rid of sign_detector.pkl.gz(this contains the saved model)

incase you want to use the saved model then skip the training part of the code and directly load the model from the available compressed file
