# Tiny-AI-in-Jupyter-Notebooks
A tiny AI trained on project Guttenberg books. It's designed to be easily configurable to run on anything from consumer graphics cards to proprietary server GPUs

TODO:

1. Add support for parallel processing in order to train bigger models on much larger datasets
   
2. Make sure it automatically detects whether it is running on a GPU or a TPU in order to make
   the code truly a plug and play experience as you will just set the training parameters
   in the initial cells and then add more training datasets. Afterwards just run every cell
   from the top down to the second from the bottom cell. You will be notified about the progress in real time
   with a sample text output with training progress every few epochs.
   E.G. set it to generate 600 tokens worth of text every 5 epochs.
