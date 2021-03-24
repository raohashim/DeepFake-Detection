

## Capsule forensic
The Capsule network is used in conjunction with VGG-19 to detect the manipulation in the faces. Our implementation is based on [https://arxiv.org/pdf/1810.11215.pdf](https://arxiv.org/pdf/1810.11215.pdf). 

** Dataset:**
The processed dataset could be downloaded from this link: [https://seafile.idmt.fraunhofer.de/u/d/b639276d15b9423bb11f/](https://seafile.idmt.fraunhofer.de/u/d/b639276d15b9423bb11f/)
The processed database must be stored with the label "0_" as a prefix for the real images and else (e.g., 1_ , 2_....) for all fake directories.

**Step 1:**
 - Extract the frames from the videos using the file `"Rename and Frame Extraction.ipynb"` by only adding the directory path.

**Step 2:**
 - Follow the instructions in file `" Data_Analysis.ipynb"` to create the test, train, and cv directory with only the cropped faces from the frames extracted earlier.
 - Add manually "0_" to the folder with real images and "1_", "2_", and "3_" to directories with fake images.


**Step 3:**
 - To train the model, the database must be organized as told earlier.
 -  Afterwards, the parameters of the training file (`"train_binary_ffpp.py"`) must be changed accordingly, such as the path of the dataset (where the train, test, and validation directories are located), checkpoints (where the model and its checkpoints will be saved), dropout value and many other. Parameters detail could be seen in the corresponding source code.
 - We have trained three different capsule network variants using **5%, 10%, and 20%** dropouts. Our training files, checkpoints, and dataset could be found in their corresponding directories directory. 
 - The evaluation results of the models could be found in the file `"CapsuleNet.ipynb"`.
 
 **Step 5:**

 - To evaluate the model on an unseen Dataset or test dataset, use the file `"test_binary_ffpp.py"`.
 - Change the parameters such as saved checkpoint directory path, and test data path.
