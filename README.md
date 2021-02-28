# lstmstickings
Generating marimba stickings using LSTM neural nets

xmltoarray converts Music XML files (.mxl) to numpy arrays and enables stickings to be entered manually.
This notebook uses the music21 package which requires configuration with external music notation software such as MuseScore 3.0.

dataprep_runmodels loads the numpy arrays, prepares the data, and builds, trains, and evaluates the models through grid-search over hyperparameter configurations.
