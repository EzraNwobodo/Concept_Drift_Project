# Detecting Concept Drift using Spectral Embedding 
This report is on a novel method of detecting a phenomenon called "concept drift" called unfolded adjacency spectral embedding (UASE), which was introduced by [A. Jones and P. Rubin-Delanchy](https://arxiv.org/abs/2007.10455) as a method of embedding complex graphs. Using UASE for this purpose is heavily inspired by two papers by I. Gallagher et al.([1](https://proceedings.neurips.cc/paper/2021/hash/5446f217e9504bc593ad9dcf2ec88dda-Abstract.html),[2](https://arxiv.org/abs/1910.05534)). The first uses UASE in the context of a dynamic latent position model, a sequence of unweighted graphs, and the second uses it for a single weighted graph (the specifics are discussed in Section 4). The aim here is to model the relationship between features or covariates changing over time as a weighted dynamic latent position model, a sequence of weighted graphs, and combine the results of those two papers. Obtaining useful insights and properties from this model involves defining a new class of model called a weighted multilayer random dot product graph, which is some weighted extension of the multilayer random dot product graph defined in the [A. Jones and P. Rubin-Delanchy paper](https://arxiv.org/abs/2007.10455).
We first explain what concept drift is, why it’s important, and what problems this method aims to solve (Section 1). We then describe the method itself (Section 2) and apply it to a toy model to illustrate its properties (Section 3) before going into detail on the theory behind model and proving some important properties (Section 4).
