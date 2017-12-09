# BvS
**Dawn of AI**  
An Image classifier to identify whether the given image is Batman or Superman.  

<p align="center">
<img src="/media/giphy.gif" alt="bvs" width="600" height="400">
</p>  

## Building a simple Neural Network:

**Step 1:** Prepare the image data & preprocess it.

Firstly, we will have to collect huge amount of data to get atleast a significant amount of accuracy. I've collected 300 images from google. While it cannot be considered as decent data at all, it is enough to demonstrate the process.

<p align="center">
<img src="/media/image_collection.png" alt="All bat" width="650" height="300">
</p>

These Images may come of as different resolutions and formats. We don't need higher resolution images. So, we convert all of them into a standard 30 * 30 resolution in .jpg format.

A simple program to do this can be found [**here**](https://github.com/perseus784/BvS/blob/master/image_process.py).  
Input -> Folder containing collection of images.  

<p align="center">
<img src="/media/convert.png" alt="Conversion" width="650" height="300">
</p>

**Step 2:** Convert Images into Data matrices.  

Our program cannot directly take image inputs. So, we need to convert it into a format which it understands.  
*Numbers!*. Yes, it can handle numbers better than us (Unless you are an asian).  
It is done [**here**](https://github.com/perseus784/BvS/blob/master/data_prep.py).  
<p align="center">
<img src="/media/club.png" alt="Conversion to table" width="900" height="350">
</p>  
 
**Step 3:** Create a Neural Network Tensorflow graph.  
Okay, this is gonna be long but interesting. Lets begin!  

A Neural Network is a Bio-inspired mathematical model based on how our brains work.  
---
***How do we learn?*** It was a mystery for millions of years ever since we were conscious. Our brains consist of billions of neurons. These neurons communicate to each other by Synapses. By recent advancements, it is found that whenever we learn new stuff these synapses between these neurons gets strong. *Thus, we learn!*  
<p align="center">
<img src="/media/brain-cell-neuron.gif" alt="neuron" width="500" height="350">
</p>  
This process is inspired and applied in machine learning. While in early periods there was neither enough data nor the processing power to do the math. Luckily, we are in the golden age of Information.  
Firstly, we create a simple perceptron. A rudimentary model without any complexities. It has,  
<p align="center">
<img src="/media/perc.png" alt="neuron" width="600" height="300">
</p>  

    Inputs -> x1, x2, x3.
    Weights -> w1, w2, w3.
    Formatted Output -> y.
    Weights are nothing but likeablity of that respective input to be chosen.
    Weight is high for an input branch which gives max. output.
    Bias will give a basic shift to the output, it avoids nullification of a cell.
An analogy:  
Inputs are from our senses or previous neurons.  
Weights are the synapes that connects the neurons.  
Function cells are neuron cells. 

    Each Neuron cell has the functional equation,  
     Y= Wx+ b
    Where Y is output,
          W is Weight,
          b is bias.  
The whole thing can be represented mathematically as,  
<p align="center">
<img src="/media/Perceptron.jpg" alt="Perceptron" width="1000" height="600">
</p>  

*Here comes Deep Neural Networks:*  
If we add more layers in a neural network to make it more accurate and handle larger data, it's a deep neural network.  
It works the same way as shown above except it has more layers of it's repeated selfs.  
<p align="center">
<img src="/media/neural_network.jpg" alt="DNN" width="700" height="350">
</p>  

Ahh Ahh, not so fast. We have to add more things to make it smarter.  
We give some inputs to the network we've built and it gives us some output back, Simple right!.
Now the network has no kind of huiding or rewarding system to go towards the right direction.
The predicted output is compared with the actual output, from that loss is calculated.
This loss should be reduced. A cost function is defined and it has to be minimized using various methods.  


**Step 4:** Train the model using the data matrices.


**Step 5:** Test the model that was created with a new set of data.
