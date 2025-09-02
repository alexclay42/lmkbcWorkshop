# lmkbcWorkshop
Code for our submission to the KBC - LM 2025 Workshop

## File Structure

### experiments.ipynb
This file outlines the different com.onents with brief explanations before each section.  
The components can be run with the following function calls 
initialTriple() generates the initial batch of triples, with given data and parameters indicating what example type, whether to add LLM generated information, or relation guides, and the sampling type to use for generation.  
faster_check() is the regeneration portion (named as it was a faster version of the original function) which accepts the parameters for generation type, data (expected to be from the intial generation format), and whether positive or negative examples are being used.
confidence_new() is the judge function, translate_check() handles the translation filter, and consensus() is as it is named.
format_preds() handles formatting the data into the file for evaluation.

If the notebook doesn't render, it should still work if downloaded.

### evalexperiments.ipynb
This file handles the recall and precision calculations for each relation by calling the evaluation file on each of the prediction files generated from the experiments.

### evaluate.ipynb
This file was adapted from the challenge, with precision defaulting to 0 in the absence of a prediction.

### workshopData
This folder houses all of the prediction files from each experiment generated from the format function, as well as the original train and validation data from the challenge. The hundredsample file contains the stratified samle of the train dataset used for the experiments.


