# gctaf
Global Cross-Time Attention Fusion for Enhanced Solar Flare Prediction from Multivariate Time Series

Multivariate time series classification is increasingly investigated in space weather research as a means to predict intense solar flare events, which can cause widespread disruptions across modern technological systems. Magnetic field measurements of solar active regions are converted into structured multivariate time series, enabling predictive modeling across segmented observation windows. However, the inherently imbalanced nature of solar flare occurrences, where intense flares are rare compared to minor flare events, presents a significant barrier to effective learning. Conventional classification models frequently succumb to bias toward the majority class, undermining their ability to generalize in operational forecasting scenarios. To address these limitations, we propose a novel Global Cross-Time Attention Fusion (GCTAF) architecture, a transformer-based model that introduces learnable global temporal tokens to enhance long-range temporal modeling. Unlike traditional self-attention mechanisms that rely solely on local interactions within time series, GCTAF injects a set of cross-attentive global tokens that summarize salient temporal patterns across the entire sequence. These tokens are refined through cross-attention with the input sequence and fused back into the temporal representation, enabling the model to identify globally significant, non-contiguous time points that are critical for flare prediction. This mechanism functions as a dynamic, attention-driven temporal summarizer that augments the model’s capacity to capture discriminative flare-related dynamics. We evaluate our approach on the benchmark solar flare dataset and show that GCTAF effectively detects intense flares and improves predictive performance, demonstrating that refining transformer-based architectures presents a high-potential alternative for performing solar flare prediction tasks.

# Content Details

* <code> src/ </code> The details for each notebook file are as follows:
  - <code>CTAF_H02.ipynb</code>: This module is a step-by-step guide to our experiments in a single notebook file.

* <code> DATA </code> in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells).
  

# Execution Details 
* To view our modules, experiments, and results in a single file, contrex_module.ipynb file is sufficient.
* Since SWAN-SF is a large dataset, we do not include the preprocessed dataset in DATA\Preprocessed-SWANSF-main, if you need to train the components and start the experiments from scratch, don't hesitate to contact us!
* Original SWAN-SF data comes from: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EBCFKM,
we use the preprocessed version as discussed in our paper.
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2
