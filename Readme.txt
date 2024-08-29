Our project consists of three Jupyter Notebooks: 1) Resizing, 2) Resizing-Normalization, and 3) Resizing-Augmentation-Normalization. 
The purpose of creating these notebooks is to enhance modularity, organization, collaboration, and reproducibility within the project, 
while also facilitating experimentation and code reuse.

To run this code successfully, follow these steps:

1. Install Required Libraries:

pip install numpy
pip install pandas
pip install matplotlib
pip install opencv-python
pip install scikit-learn
pip install tensorflow
pip install imgaug

2. Prepare the Data:

Ensure you have the required CSV files (images-1.csv, images-2.csv, and images-3.csv) 
and images in a folder named images.

3. Run the Entire Code Block:
Execute the entire script in your Python environment like Jupyter Notebook or VSCode. Ensure your working directory contains the CSV files and the images folder.


******* Tips *******


- You can run the entire code blocks of "Resizing" Jupyter Notebook but there are some code block
  will take time to run the block are:

Code Block                                         Time                 
-------------------------------------------------  --------
Image Loading                                      3m-4m   

         
Resizing                                           2m-3m     
    
   
Model Execution                                    86m-88m    
  
       
Classification metrics                             15s-15.5s   

             
Model Testing                                      4m-5m          


===========================================================================================================================================


-Be advised the entire code blocks in the "Resizing-Normalization" and "Resizing-Augmentation-Normalization" Jupyter Notebooks. 
 However, please be aware that some errors might be encountered depending on the device specifications, particularly in RAM.


- To avoid the following errors:
  
  1. Keras crashes
  
  2. MemoryError (ex: MemoryError: Unable to allocate 32.67 GiB for an array with shape (71235, 100, 100, 3) and  data type float32)
  
  3. Window pop out with message ("Application Error Click Ok to Terminate the Program)

  4. Session Crash Open New Session



- Waiting a few minutes on some specific blocks which I am going to mention them below for each Notebook.


 
* Resizing-Normalization 

Code Block                                           Time       Note   
-------------------------------------------------    --------   ----------
Image Loading                                        3m-4m     

                          
Resizing                                             2m-3m


Convert the list of images to a numpy array          2m-3m      wait a few minutes after run   


Calculate mean and standard deviation                2m-3m      wait a few minutes after run 
 
 
Normalize images                                     3m-4m      wait a few minutes after run 
 
                  
Model Execution                                      92m-93m             

              
Classification metrics                               15.5s-16s    

                             
Model Testing                                        5m-5.5m     


===========================================================================================================================================


* Resizing-Augmentation-Normalization


Code Block                                                   Time           Note                
-------------------------------------------------            --------       -------
Image Loading                                                3m-4m     
                     
   
Resizing                                                     2m-3m  


Convert the list of images to a numpy array                  2m-3m          wait a few minutes after run

 
Augmentation pipeline usage with a batch size of 100         8m-9m          wait a few minutes after run (at least 5 minutes) batch size used to avoid 
                                                                            MemoryError which is variable depending on the RAM available


Calculate mean and standard deviation                        2m-3m          wait a few minutes after run


Normalize images usage with a batch size of 50               4m-5m          wait a few minutes after run (at least 5 minutes) batch size used to avoid 
                                                                            MemoryError which is variable depending on the RAM available  
            
Model Execution                                              92m-93m   

                      
Classification metrics                                       15.5s-16s  

                             
Model Testing                                                5m-5.5m  
                     

===========================================================================================================================================


***** Note *****

The previous batch numbers and the runtime depend on the device which been used for this project which could be vary from device to 
another especially the batch size could be modified depend on the RAM.

The following are the laptop specs on which the project was run:


Processor       Intel Core i7-6700HQ CPU @ 2.60 GHz (8 CPUs) 

GPU             NVIDIA GeForce GTX 960M VRAM (2 GB)

SSD             Kingston A400 M.2 SATA SSD (480GB — up to 500MB/s read and 450MB/s write)

Memory          16 GB RAM

OS              Windows 11 Home













