# Latent state energy profile

*Exercises from The Carpentries workshop on reusable, reproducible research code at Erasmus
University Rotterdam (December 2024), which I attended as a participant.*

This code is meant to apply the approach from this preprint: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10401920/
It aims at exploiting the energy profile inferred from the Langevin dynamics of a latent state to
quantitatively reproduce the stochastic behaviour of the recorded neurons given as input to the
model. We plan to apply this tool to a spatial memory and decision-making task of rats in a maze
with electrophysiological recordings from 3 areas of the cortex.

# Warnings

The code was meant to work with a previous version of neuralflow (in particular neuralflow 2.0)
that now seems to not be available. The final plots are preliminary.

# Contents

- `scripts/reusable_code_example.ipynb`: the worked example (load spike rasters, fit the latent
  Langevin model with neuralflow, plot the results).
- `scripts/poster_bar_plots_flexible_model_inference.ipynb`: summary plots of the inferred models.
- `scripts/reusable_code-test.ipynb`: exercise notebook for the workshop.
- `data/poster_data/`: the example spike rasters the notebooks read (about 880 MB). To keep the
  repository light they are no longer tracked, but they are still in its history. Restore them
  with:

  ```bash
  git checkout 8e4d5c64ea927acc890b120ba20046b05509fe66 -- data/poster_data
  git restore --staged data/poster_data
  ```

# Setup

Download the repository, open a terminal inside the folder and install the dependencies:

```bash
pip install -r requirements.txt
```

Then open `scripts/reusable_code_example.ipynb` in the IDE you prefer (for example VS Code) and run
all the cells.

# License

[Apache License 2.0](LICENSE).
