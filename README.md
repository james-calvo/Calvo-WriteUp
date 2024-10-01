# Image Convolution Performance Comparison: Serial vs Parallel Implementation
This repository contains Python code for comparing the performance of serial and parallel implementations of the Gaussian blur image convolution algorithm. The experiments are conducted on a dataset of 100 images, consisting of 50 images of dogs and 50 images of cats. The goal of this project is to evaluate the efficiency of both approaches in terms of processing time and demonstrate the conditions under which parallel processing may or may not provide speedup over serial processing.

**Purpose**
The primary objective of this project is to measure and compare the time taken to apply the Gaussian blur filter in both serial and parallel contexts. While parallel processing is typically expected to speed up computation by leveraging multiple CPU cores, this experiment explores whether it is effective for smaller datasets and relatively simple image processing tasks.

**Overview**
The code applies the Gaussian blur filter to each image in the dataset in two ways:

Serial Implementation: Processes each image one after another on a single CPU core.
Parallel Implementation: Splits each image into smaller parts and processes these parts simultaneously using multiple CPU cores.
The results are captured, and the total processing times for both approaches are compared. The code also calculates the speedup of the parallel approach relative to the serial approach, with performance metrics presented for different batch sizes of images (10, 25, 50, 75, 100).

**Key Features**
Gaussian Blur Filter: A commonly used image convolution algorithm for smoothing and noise reduction.
Performance Measurement: The elapsed time for both serial and parallel processing is recorded for various batch sizes.
Speedup Calculation: The code calculates the speedup achieved by the parallel implementation over the serial one.
Dynamic Batch Processing: Images are processed in batches of 10, 25, 50, 75, and 100 to evaluate performance under different dataset sizes.
Results
In this experiment, the parallel approach did not achieve a significant speedup over the serial approach due to the overhead associated with splitting images, managing multiple processes, and CPU synchronization. The serial implementation was generally faster, particularly for smaller datasets.

Speedup (Serial/Parallel) for Different Batch Sizes:
10 Images: 0.0365
25 Images: 0.0209
50 Images: 0.0148
75 Images: 0.0138
100 Images: 0.0129

**Requirements**
Python 3.x
Google Colab (Optional for GPU/TPU testing)
Libraries:
OpenCV (cv2)
NumPy
Matplotlib
Multiprocessing
Pandas

**How to Run**
Clone the repository to your local machine or open the notebook in Google Colab.
Ensure all the required libraries are installed.
Replace the image dataset path with the correct path where your images are stored.
Run the script and observe the performance comparison between the serial and parallel implementations.
