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

   NOTE!
   The default settings require approximately 90 GB of GPU VRAM. In order to train it on
   a consumer level graphics card with 16GB down to possibly even 4 GB of VRAM apply these settings:
   SEQ_LENGTH = 1024
   BATCH_SIZE = 16

   GEN_LENGTH = 600
   TEMPERATURE = 0.7
   TOP_P = 0.89
   TOP_K = 70

   Note: If the training cell still tries to allocate more VRAM than you have available try decreasing FF_DIM = 1024
   and possibly set EMBED_DIM = 512 NUM_HEADS = 4 and NUM_LAYERS = 4. Always keep the VOCAB_SIZE at 16384!
   
