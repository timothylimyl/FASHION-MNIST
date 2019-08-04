# FASHION-MNIST & MNIST

Fashion MNIST is a dataset containing 60,000 examples for the training set and 10,000 examples for the testing set.
The idea for the Fashion MNIST dataset is to serve as a replacement to the original MNIST dataset which is widely used for benchmarking machine learning algorithms.

Replacing MNIST is a good idea because the MNIST datasets is already to easily solved with the current Deep Learning algorithms. According to the Kaggle leaderboard, someone has already achieved 99.7% accuracy with MNIST.
Besides that, I personally also feel that MNIST does not really serve as a good benchmark for computer vision tasks that seeks to identify objects as handwritten digits comparitively have way less distinct features than real-world objects.

## My Model

I have tried many different CNN Architecture to get as high of a testing accuracy as I can. 
Most of my time was spent comparing different network architecture and edited the network parameters to potentially give me the highest accuracy.
What I found was that reaching approximately 91-93% accuracy was pretty easy with CNN, you can do it with 200k parameters but trying to reach 94% accuracy required a lot more parameters. My final decision after testing numerous CNN

- CNN Layer 1 and 2 with 128 filters of 3x3
- CNN layer 3 with 256 filters of 3x3
- FC Layer of size 256
- Dropout of 50% was used
- Batch Normalization after every activation function

**Total Parameters - 23123131**

Note- Everytime I try reducing the FC layers, the accuracy will definitely drop below 94%. As I was tuning the parameters, my main goal was to try to have as less parameters as possible
but the accuracy could never hit 94% whenever I tried increasing the max pooling filter size or reducing size of FC.

## Results

Running with my final CNN Architecture 3 times to get an average of the testing accuracy for both the Fashion MNIST and MNIST datasets-


| Test | Testing Accuracy (Fashion MNIST)  |  Testing Accuracy (MNIST)  |
| :---         |     :---:      |          ---: |
| 1 | git status     | git status    |
| 2    | git diff       | git diff      |
| 3    | git diff       | git diff      |
| Average   | git diff       | git diff      |

## Extra idea

  Targeted Data augmentation to add extra specific data that will boost performance. 
  
  Majority of the mislabelled data was caused by the T-Shirt (Label 0) and Shirt (Label 1) as I predicted.
  T-shirt and shirt images looks very alike especially on 28x28 sized images, I believe that even humans will find a hard time        differentiating between the T-shirts and Shirts in this dataset.
  On further inspection, differentiate between Shirt and T-Shirt can actually be very easy once the focus is on the buttons.
  
  I believe that once the deep CNN is able to extract out more distinct features to differentiate T-Shirt from Shirt, the accuracy for the     Fashion MNIST will be above 95% and be the top algorithm in the benchmark.
  
  Every test that I did, the mislabels are always of such proportion with most mislabels coming from T-Shirt (0) and Shirt (6). Example from my results-
  
 ![Mislabels](https://user-images.githubusercontent.com/49274721/62420175-48f5d000-b6d1-11e9-9e10-8f7d9206b0d5.PNG)
 
 ![Mislabels2](https://user-images.githubusercontent.com/49274721/62420212-ee10a880-b6d1-11e9-857d-899a8f4ddac1.PNG)
 
 The total mislabels from T-Shirt and Shirt is averages around
 
 
 
  
