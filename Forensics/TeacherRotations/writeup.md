# Writeup

We are provided with an excel file, and on analyzing the actual data in the file, there doesn't seem to have any useful information. But the question makes numerous allusions to "rotation", and its importance. On searching online, for steganography involving rotation and excel, we are led to [this](https://www.researchgate.net/publication/49942013_Steganography_in_Ms_Excel_Document_using_Text-rotation_Technique)

So, now we understand that the data is encoded in the rotation of the text fields. But, if we try and get the data as is, by getting the rotation of each cell, we would get a garbage answer. We turn to the question again, which tells us that this "secret plan" can only work if the cells are sorted in a profitable way, i.e, by their salary. 

  This can be achieved with a program that can read an excel file. We sort all the data here based on the salary field, to get [this](SolnStuff/created.xlsx) file. 

  Now, that we have sorted the file, we need to read the data encoded. It can be accomplished in multiple ways. We are currently using [this](SolnStuff/decode.py) python script to get the data. If you read the first email field provided, we also get to know that the data is ASCII encoded.

Hence, we can get all the data, split it and decode it accordingly to get the final answer.

## Running the script
![decode.py run](SolnStuff/script_run.png)
