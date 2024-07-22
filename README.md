# Transformer-Mass-Reconstruction

Developed a transformer encoder network, inspired by the Particle Transformer for Jet Tagging paper (https://arxiv.org/abs/2202.03772), for diHiggs invariant mass reconstruction.

The transformer takes the 4-vectors (pt,eta,phi,mass) of the leading order final state products of a 4W->HH->3lep+2jet+met decay and produces the invariant mass of the diHiggs system. 

Improvements to be made:

- Take all the final state products, not just the leading order (implement variable input lengths)
- Use the full training dataset and develop a generator to load the events temporarily for each epoch/batch.


Workflow:

Data preprocessing/cleaning:

- Event 4 vector extraction, object selection
- Dataset merging and formatting
- 
