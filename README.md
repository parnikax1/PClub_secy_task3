# Task_2

Drive link for the dataset used = https://drive.google.com/file/d/1NT3Zfui2Q38e-cKEMDMBxRfKTfrSd80m/view?usp=drive_link
Approach for the dataset used - I first downloaded the dataset from UTK face. But while trying and testing with diferent models, i applied haar cascade once to the dataset which os.remove()-ed the files in which no faces were detected, due to which neraly 1800 images nearly deleted. Remaining ones, nearly 22k, are in this daatset
Approach for the problem- My basic approach for the rpoblem was to crop the bachground from the images, just get the faces and then preprocess the image, crop the lower hald and train my model on the upper half for better accuarcy on the masked images. While scrolling through some documents, i came across haarcascade which did this for me but was a bit slow in my case. but when i tried to redetect the images with other model, things collapased, the details of which i have given in failed_code.ipynb along with the folder containing such cropped images. So lastly, i found the dnn res10 model which preprocessed the images for me and then i extracted the coordinated of the face box and ultimately' got the cropped face, which was then furthered cropped to remove the lower hald and then basic Sequential was trained on these images. after training the model, i defined functions for preprocessing and extracting features of our target images and finally predicted the gender using the CNN model above. Then to finally get the testing accuracy, I labelled a masked dataset which i found online of 151 images and calculated the testing accuracy by taking a artio of the images predicted accurately to total number of images.
Drive link for testing data-https://drive.google.com/file/d/1D3BHDzYwaQtdJ4dpLKmAPuM7CI_ao6Gk/view?usp=drive_link
Drive link for cropped image folder- https://drive.google.com/file/d/1ziq6h4SSME3Tanox71YSJ20u-qXzc_9X/view?usp=drive_link

![Screenshot 2024-05-23 225549](https://github.com/parnikax1/Task_2/assets/152218569/737a440d-e592-444a-a28a-4176e8c6c74a)
![Screenshot 2024-05-23 225536](https://github.com/parnikax1/Task_2/assets/152218569/b2de5123-f0a7-4f5b-8043-228538c40d80)
![Screenshot 2024-05-23 225505](https://github.com/parnikax1/Task_2/assets/152218569/f3ed90bc-e319-4dad-9298-b55ff654e42b)
![Screenshot 2024-05-23 225449](https://github.com/parnikax1/Task_2/assets/152218569/a623980b-3c68-4ab8-a514-15dac71bba5c)
![Screenshot 2024-05-23 225436](https://github.com/parnikax1/Task_2/assets/152218569/bc83fa07-fb78-484a-a7bd-be62f80d88cc)




