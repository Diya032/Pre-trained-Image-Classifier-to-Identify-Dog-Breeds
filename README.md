# Pre-trained-Image-Classifier-to-Identify-Dog-Breeds

## Project Outline
* Time your program
  * Use Time Module to compute program runtime
* Get program Inputs from the user
  * Use command line arguments to get user inputs
* Create Pet Images Labels
  * Use the pet images filenames to create labels
  * Store the pet image labels in a data structure (e.g. dictionary)
* Create Classifier Labels and Compare Labels
  * Use the Classifier function to classify the images and create the classifier labels
  * Compare Classifier Labels to Pet Image Labels
  * Store Pet Labels, Classifier Labels, and their comparison in a complex data structure (e.g. dictionary of lists)
* Classifying Labels as "Dogs" or "Not Dogs"
  * Classify all Labels as "Dogs" or "Not Dogs" using the dognames.txt file
  * Store new classifications in the complex data structure (e.g. dictionary of lists)
* Calculate the Results
  * Use Labels and their classifications to determine how well the algorithm worked on classifying images
* Print the Results

## Uploaded Images Specifications
* Must be in jpeg format with extension jpg
* Approximately square in shape (their height and width are approximately the same number of pixels).
* Dog Image - named Dog_01.jpg. Make sure you know the breed of dog that the image is of.
* Pet or Animal Image that's not a dog - named Animal_Name_01.jpg , where Animal_Name is the name of the animal in the picture. This name is formatted such that if 
  more than one word makes up the animal name those words are separated by an underbar ( _ ).
  For example:
  Image of a Black Bear is named Black_bear_01.jpg
  Image of a Frog is named Frog_01.jpg

* An image of something that's not an animal - named Object_Name_01.jpg, where Object_Name is the name of the object in the picture. (Similar naming for multiple     words as above)
* Create a fourth Image of a Dog using Dog_01.jpg (Dog_02 by either horizontally flipping or rotating by 180 degrees(upside down position of dog))

## Running Models for classification
* For Uploaded photos
  ''' shell
  sh run_models_batch_uploaded.sh
  '''

* For Photos present already
  ##  Code from run_models_batch.sh 
  * python check_images.py --dir pet_images/ --arch resnet  --dogfile dognames.txt
     > resnet_pet-images.txt
  * python check_images.py --dir pet_images/ --arch alexnet  --dogfile dognames.txt  
     > alexnet_pet-images.txt
  * python check_images.py --dir pet_images/ --arch vgg  --dogfile dognames.txt 
     > vgg_pet-images.txt
