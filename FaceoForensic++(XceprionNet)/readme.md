Deepfake detection using Xception Network
Deepfake detection by using Xception Network architecture was proposed by FaceForensic++ (https://arxiv.org/pdf/1901.08971.pdf). Our implementation is also based on the parameters and technique described in the FaceForensic++ paper. It is also considered as a benchmark to evaluate the performance of new detection techniques.

** Dataset:** The processed dataset could be downloaded from this link: https://seafile.idmt.fraunhofer.de/u/d/b639276d15b9423bb11f/ ** Step 1

Extract the frames from the videos using the file "Rename and Frame Extraction.ipynb" by only adding the path to the directory.
Step 2:

Follow the instructions in file "Data_Analysis.ipynb" to create the test, train, and cv directory with only the cropped faces from the frames extracted earlier.
Also, follow further instruction to label and store the data for further processing.
Step 3:

Follow instructions in file "Model Training.ipynb" to train the model for deepfake detection.
Step 4:

Follow the instructions in file "Test_Xception.ipynb" to evaluate the model's performance on the unseen video data.
