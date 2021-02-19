# asr-jupyter
Explaining the content:

***
`asr.ipynb` is the file in which the entire recognition pipeline is implemented (MFCC + DTW + Recognition). However, this implementation relies heavily on pre-built methods. So in order to expand the process related to MFCC, two other codes were developed to implement MFCC from scratch
***
`mfcc_implementation` tries to reproduce the MFCC from [python_speech_features repository](https://github.com/jameslyons/python_speech_features).
***
`alt_mfcc` tries to implement it the way it is taught in [this Youtube playlist](https://youtube.com/playlist?list=PL-wATfeyAMNqIee7cH3q1bh4QJFAaeNv0), which is based on librosa.
***
There is some divergence in the results given by the MFCC methods in different libraries, as stated here: https://stackoverflow.com/questions/60492462/mfcc-python-completely-different-result-from-librosa-vs-python-speech-features
***
The current challenge now is to link these implementations with the `asr.ipynb` code and get a good recognition rate. As an example, running `asr.ipynb` using librosa built-in MFCC gives an accuracy of around 60%, as with other methods, this accuracy drops to around 20%.