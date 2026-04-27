# Encoder-Decoder Assignment Package


## Assignment Topic
Review, implementation, and comparative analysis of encoder-decoder models:
1. Without attention
2. With attention

The notebook uses a synthetic sequence task (digit-sequence reversal) to compare both models under similar training settings.

## What the Notebook Does
1. Creates synthetic training, validation, and test datasets.
2. Builds vocabulary with special tokens (`<pad>`, `<sos>`, `<eos>`).
3. Implements baseline seq2seq model (no attention).
4. Implements seq2seq model with Bahdanau attention.
5. Trains both models.
6. Computes exact-match test accuracy.
7. Plots training and validation losses for comparison.
8. Shows qualitative sample predictions.

## Requirements
Install Python packages if needed:
- torch
- numpy
- matplotlib
- jupyter

Example install command:

```bash
pip install torch numpy matplotlib jupyter
```

## How to Run
1. Open `encoder_decoder_attention_comparison.ipynb` in VS Code or Jupyter.
2. Select a Python kernel.
3. Run cells from top to bottom.
4. Wait for both training sections to complete.
5. Read the final metrics and sample outputs.

## Expected Outcome
should observe that the attention-based model typically:
- Achieves better exact-match accuracy.
- Handles longer sequences more reliably.
- Shows improved output quality over the baseline model.

## How to Use for Submission
1. Run the notebook completely.
2. Copy key results (loss curves and accuracies).
3. Fill the blank result sections in `Assignment_Documentation.doc`.
4. Add screenshots/plots from the notebook if required by your instructor.


