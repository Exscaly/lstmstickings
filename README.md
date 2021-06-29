# lstmstickings
Generating marimba stickings using LSTM neural nets

xmltoarray converts Music XML files (.mxl) to numpy arrays and enables stickings to be entered manually.
This notebook uses the music21 package which requires configuration with external music notation software such as MuseScore 3.0.

data_cleaning checks through the array dataset to identify errors in the xml/mxls and arrays. These are fixed by hand and re-saved.

pve_encoding applies pitch-vector encoding to the dataset, including the splitting of chords, key and octave transposition for transposable exercises, and octave transposition only for non-transposable exercises. 

ite_encoding applies interval transposition encoding to the dataset, including the splitting of chords, reversal of inputs in place of a bidirectional LSTM layer, and key transposition within one octave.

pve_model outlines the final data preparation, LSTM model compilation (with bidirectionality) and training, visualises the learning curves, then evaluates the model under sequence accuracy and note accuracy with strict and multiple-ground truth (MGT) approaches.

ite_model does the same, but without bidirectionality (as input reversal was implemented in ite_encoding).
