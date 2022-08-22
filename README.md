# About me
Hi there,
I'm Jason and I'm interested in Data Science and Computational Biology. 
I studied bioinformatics at the University of Queensland and, more recently, a masters of Data Science at LMU in Munich. 
I'm particularly interested in incorporating thermodynamics into metabolic models and hybrid modelling, that is, the synthesis of ML and mechanistic models to hopefully combine the rigidity, specificty and interpretability of mechanistic models with the accuracy of ML models. 
I'm currently working on a new statistical model for improving the covariance estimates of the [group contribution](http://dx.doi.org/10.1529/biophysj.107.124784) (and [component contribution](https://doi.org/10.1371/journal.pcbi.1003098)) methods. 
# Projects
Unfortunately, my current projects are still private until we get closer to publishing, but I have a handful here that might be interesting.

## Improving seedling detection with height data
[In this project](https://github.com/JasonJooste/seedlings_height) I was tasked with integrating height data into an existing Faster-RCNN object detection network to detect conifer seedlings from drone imagery. Interestingly, it turned out that if you introduced the height data directly as a fourth image channel, the performance of  the network decreased. However, pooling the height data and incorporating it after the backbone and before the region proposal network improved performance. It goes to show that it's important to think about how to incorporate new information when using transfer learning. 

## Generative Bayesian model of metabolic fluxes and thermodynamics
[In this project](https://github.com/biosustain/gtfa) I wanted to integrate thermodynamics into steady-state flux sampling for my master's thesis. The requirement that the fluxes are steady-state introduces a number of constraints into the model that need to be adressed. I solved this by making explicit the linear relations between the models parameters and removing superfluous parameters. This project also involved improving existing estimates of formation energy covariance to address prediction collinearity. 

## Metabolic model matching and inconsistency detection
[In this project](https://github.com/JasonJooste/model_match) I wanted to match two cobra-formatted metabolic models and check their overlap. Unfortunately, they didn't share the same identifiers for the reactions and metabolites but some of the external idenfiers matched. Luckily, reactions can be uniquely identified by the stoichiometry of their substrates and substrates can be identified if they're present in known reactions, so it is possible to iteratively match the idenifiers of the two models. This script matches the two models as well as possible and outputs any inconguencies discovered. 


<!--## Small RNA mapping
This was a project during my bachelors, where the goal was to map small RNA sequences (sRNAs) to a larger sequence. Because we knew these sequences were strictly less than 32 characters in length and only encoded four characters, they could be encoded as a single 64 bit integer and stored in a hash table. The sequence could then be rapidly checked by simply bit shifting the new characters on to the existing sequence which would then be checked against the table in very few operations. As someone who doesn't work with C very often it was a good chance to grok memory allocation and pointers. 
--> 
