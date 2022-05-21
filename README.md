# Image-Compression-using-Principal-Component-Analysis

## Why did I choose this project ?
While glancing through the algorithms in CLRS, I came across Huffman encoding algorithm and found it to be quite intriguing. Exploring it's wide range of applications, I was led to an image compression aspect of it white seemed quite interesting. However, Further research and a conversation with the professor revealed that PCA works for relatively a wide range of datasets as compared to Huffman encoding algorithm and PCA. This is how I came up with this project idea.

## What is the problem ? 
When it comes to humongous amount of data storage especially in the form of images, compression of these images becomes almost inevitable in order to optimize the tradeoff between storage and image quality. Also, For machine learning algorithms that need images of decent quality as an input, image compresssion can improve the running time of the algorithm drastically. Image compression can be associated to saving a lot of memory space. The compression of photographs, technical drawings, artworks, digital art etc can find variety of applications in various fields. These compressed images can be sent, downloaded and uploaded in lesser time and makes the overall process efficient.

## How is the problem solved ?
There are many algorithms that can be used for image compression namely, Huffman Encoding, Run Length Encoding(RLE) etc. However, These algorithms are applicable to only specific types of datasets. On the other hand, Principal Component Analysis (PCA) can be used on a wide range of datasets. Thus, PCA seems to be a reasonable choice fro image compression. 

## What does the code do ?
- The code firstly reads an image with the help of Python Imaging Library (PIL).
- This image is converted into grayscale for the ease of computation by eliminating the 3 channel representation.
- This grayscale representation is typecasted into np.array for further matrix operations.
- This matrix (image_matrix) is passed on to a function named pca which involves the steps for principal component analysis : 
  - The rows in the image_matrix are centralized by subtracting the mean matrix from the image_matrix.
  - The covariance of the transpose of this centered_matrix calculated. 
  - The eigen values for this covariance_matrix are calculated and rearraged in descending order.
  - The eigen vectors corresponding to this eigen values are also calculated.
- The pca function returs the eigen values, eigen vectors, covariance_matrix and the centered_matrix.
- These values are passed on to the function named comress_img which follows the steps below :
  -   The cummulative contribution rate for each eigen value is calculated.
  -   Reconstruct the image using dot product of eigen vector and covariance matrix.
- The images have been reconstructed using 1,3,5,10,20,30 and 40% components.

## How to install dependencies and run the code ?
You may need to install the following dependencies to run the code : <br>
`!pip install scipy` <br>
`!pip install matplotlib` <br>
`!pip install numpy` <br>
`!pip install PIL` <br>

## Results



