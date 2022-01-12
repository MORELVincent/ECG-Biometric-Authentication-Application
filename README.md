# ECG-Biometric-Authentication-Application
This application uses transer learning methods in order to recognize patients using electrocardiogram images

The application is the result of a three-month internship realised by Morgane Nadeau and Vincent Morel
in Lodz, Poland.
This program requires Python version 3.7.

Its purpose is to train a model from raw electrocardiogram signals in a specific format : .csv files. 
A sample is given in the folder (ECG_PTB_Database_CSV), and its folder hierarchy has to remain the same
for the program to function.

The whole database can be found on github following this link : 
https://github.com/MORELVincent/ECG-Biometric-Authentication-Application


The program is divided in two specific parts :

	- Training part :

This part gives you the accuracy of our model with a given database, lead and number of epochs.
The hierarchy of the database folder has to be very specific, it must contains a list of patient
named patientXXX to patientXXX, and each patient must has a list of sessions named 0 to n (with
n a positive integer). The sessions have a list of CSV files containing the lead to be used, they
are simply named after the lead they refer to.

In the Result folder should appear the database with the given lead, as well as their 
representation in 2D images. 

Finally you will be able to see the accuracy of your model, and you may want to save it.

The training part can become very long if you plan to launch the code on your CPU, thus, if you
can use your GPU to run it, you may want to do it.

	- Predict part :

The predict part allows you to chose a saved model and to test your images in order to check 
if the model has been trained properly. You may chose an image that has been created on the 
Result\Person_dataset\test_data_files folder, which contains the data that has not been
trained on the algorithm.



