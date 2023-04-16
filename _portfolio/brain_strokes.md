---
title: "Brain criticality and strokes"
excerpt: "Study of the problem of the brain's critical behavior in the case of a brain injury such as a stroke."
collection: portfolio
---

Short summary of the article [*How do strokes affect the brain's critical state? Structural and functional aspects of the loss of connectome integrity*](/publication/2023-03-30-paper5)

The codes for numerical simulation of brain activity, the Ising lattice dynamics, as well as cluster size calculations were prepared by me (JJ) and Jacek Grela. The codes are written in python are available [here](https://github.com/grelade/critical-stroke) alongside jupyter notebooks showing example usecases.

### Criticality of the brain
The criticality provides optimal functioning of the healthy brain, hence neurological dysfunctions might be associated with its loss, which opens this area of study to clinical applications. Assessing whether a critical phase transition occurs, however, has been challenging in similar contexts.

In study for a cohort of stroke patients [1] the presence and severity of the stroke reportedly were related to a loss of critical behavior in the brain. The state-of-the-art analysis of a brain’s cortex activity model dynamics has been based on the time-averaged sizes of the largest clusters. However, calculation of additional criticality-aware quantities for the patients cohort, beyond the usual second-largest cluster size, and a comparison with an artificial system with known criticality status reveals an inconsistency. The criticality status of the stroke-affected brain becomes unclear due to an ambiguous behavior of the second-largest cluster size. Explaining this crucial observation is our main motivation.

### Artificial strokes
<p align = "center">
<img src = "/files/brain_strokes/figure_1.png">
</p>
<p align = "center">
Figure 1. Comparison of real and artificial strokes
</p>
In our work introduce a model of a stroke-like modification of a healthy connectome. The Hagmann et al.’s connectome [2] serves as the base connectivity matrix representing the healthy brain. An artificial stroke changes the connectivity between a particular brain’s subsystem, called resting state network (RSN), with the rest of the brain. To this end, we randomly select a fixed fraction of nodes of the RSN and completely remove connections to their neighbors not belonging to the same RSN. This way, the internal structure of the RSN remains unchanged, while effectively decreasing the connection of the RSN with the rest of the brain. The proposed minimal model of a stroke recreates the behavior of second largest cluster observed for stroke patients, cf. Figure 1 above. Furthermore, we perform the comparison using graph-theoretic methods. The connectome integrity is probed by the graph modularity. Despite the limiting assumptions, the artificial stroke model recreates quite well the overall loss of connectome integrity observed in patient’s cohort.

Finally, we perform a detailed study for the second-largest cluster in the Ising model. We combine the insights from connectome integrity study with the Ising model, a paradigmatic case with known criticality status. Ising spins act as the neuron nodes, and the usual two-dimensional grid takes the role of the connectome. The stroke-induced loss of integrity is taken to an edge case where the connectome is completely divided into subsystems, thus modeling a severe artificial stroke. We recreate an anomalous lack-of-peak in the second-largest cluster size and describe the underlying mechanism as a competition within the hierarchy of subsystem-wide clusters. The results presented refer to neurobiological data; however, the conclusions reached apply to a broad class of complex systems for which a critical state is identified.

Bibliography:
1. Rocha, R. P. et al. Recovery of neural dynamics criticality in personalized whole-brain models of stroke. Nature Communications 13 (1), 3683648 (2022).
2. Hagmann, P. et al. Mapping the structural core of human cerebral cortex. PLoS Biology 6, e159 (2008)