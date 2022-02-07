# Digit Discriminator and Generator Network
One of the fun projects I was doing during my AI class. The objective is to use **PyTorch** to create a discriminator to recongize input digit and a generator network to print digits.
First time learning and using pytorch, so much fun! 
## The Discriminator:
For our discriminator, we chose digit 1. The architecture of our discriminator consists of one input layer from 784 to 512 with the LeakyReLU function applied to it,
and one hidden layer from 512 to 256 with LeakyReLU function as well, and finally an output player from 256 to 1 with the Sigmoid function applied to it. We originally had no
hidden layer in our architecture. After we added one, we found that we got much better loss results, at the cost of processing speed. We set Adam’s learning rate to 0.01.
In our validation set we consistently achieved a <strong>99% accuracy, and above 98% in precision, recall. </strong> 

## The Generator Network:

For the generator network, It is the opposite of the discriminator. I have the input layer from 100 to 512 with the LeakyReLU function, and 512 to 256 for the hidden
layers with the LeakyReLU function, for the output layer is 512 to 784. Initially, I have the loops for n,n1,n2 is 5,10, and 15 with a learning rate of 0.001.
I slowly decreased the learning rate and increased the iterations, and I finalized with n,n1,n2 as 15, 30, 40. The finalized learning rate for discriminator 0.001 and 0.0001 for
the generator.
Initially, I did not use a hidden layer and the images of the digit look bigger, After I added the hidden layer the digit looks smaller and cleaner. It takes me approximately 3
hours to make it look decent. The code still works after I changed the digit, The below is what the digit looks
like and also the difference of images of digits produced with the hidden layer and without the hidden layer.
### Some of generated digits and processes:
![image](https://user-images.githubusercontent.com/71905429/152282143-6e58c5e8-c64d-4dc5-a2cf-8e9e24651aac.png)


