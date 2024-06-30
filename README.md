# Spooky-Author-Identification
The competition dataset contains text from works of fiction written by spooky authors of the public domain: Edgar Allan Poe, HP Lovecraft and Mary Shelley. The data was prepared by chunking larger texts into sentences using CoreNLP's MaxEnt sentence tokenizer, so you may notice the odd non-sentence here and there.

## Objective is to accurately identify the author of the sentences in the test set.

File descriptions
train.csv - the training set
test.csv - the test set
sample_submission.csv - a sample submission file in the correct format
Data fields
id - a unique identifier for each sentence
text - some text written by one of the authors
author - the author of the sentence (EAP: Edgar Allan Poe, HPL: HP Lovecraft; MWS: Mary Wollstonecraft Shelley)


## To Import the dataset in your system you can go through the below ways

Step 1: Install the Kaggle API
Ensure you have the Kaggle API installed. You can install it using pip:
`!pip install kaggle`


Step 2: Set Up Kaggle API Credentials
Go to Kaggle's website.
Log in to your account.
Go to "My Account" by clicking on your profile picture.
Scroll down to the "API" section and click on "Create New API Token". This will download a kaggle.json file containing your API credentials.


Step 3: Place the kaggle.json File
Move the kaggle.json file to a directory named .kaggle in your home directory. You can do this in a Jupyter notebook with the following commands:

```
import os
import shutil

#Ensure the .kaggle directory exists
os.makedirs(os.path.expanduser('~/.kaggle'), exist_ok=True)

#Move the kaggle.json file to the .kaggle directory
shutil.move('path_to_downloaded_kaggle.json', os.path.expanduser('~/.kaggle/kaggle.json'))

#Set the permissions of the file to ensure it's not readable by others
os.chmod(os.path.expanduser('~/.kaggle/kaggle.json'), 0o600)
```

Replace `'path_to_downloaded_kaggle.json'` with the path where your kaggle.json file is located.


