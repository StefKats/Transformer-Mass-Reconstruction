# Transformer-Mass-Reconstruction

Developed a transformer encoder network, inspired by the Particle Transformer for Jet Tagging paper (https://arxiv.org/abs/2202.03772), for diHiggs invariant mass reconstruction. This work develops a manual tensorflow implementation of the attention mask that was originally implemented with built-in Pytorch functions. The original transformer is used for jet classification, we adapt this for the task of mass regression by performing an ablation study. 

The transformer takes the 4-vectors (pt,eta,phi,mass) of the leading order final state products of a 4W->HH->3lep+2jet+met decay and produces the invariant mass of the diHiggs system. 

Improvements to be made:

- Take all the final state products, not just the leading order (implement variable input lengths)
- Use the full training dataset and develop a generator to load the events temporarily for each epoch/batch.
- The feasibility of discovering new physics can be explored by testing the mass reco on a new physics sample generated by modifying the EFT parameters and looking for resonances in the HH invariant mass distribution or shifts in the overall shape. 

**Workflow:**

Data preprocessing/cleaning:

- Event 4 vector extraction, object selection
- Dataset merging and formatting

Transformer ablation study/optimisation:

- 3 lepton mass reco (optimise the attention block)
- 3 lepton + 2 jet + met reco (optimise the attention blocks in series)
- HH invariant mass reco (obtain final results, optimise the proposed improvements)

  <em> The results of the three sub-studies motivate the architecture of the transformer encoder. </em>

Comparison with simple deep neural network:

- Benchmark results obtained with a simple network approach
- Best transformer model is compared with the benchmark in terms of the reconstruction metrics (average mass difference between truth and reco across the HH mass range)




