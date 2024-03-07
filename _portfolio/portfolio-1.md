---
title: "Disaster Modeling"
excerpt: "I am exploring how to create data-driven reduced order models for massive, agent-based systems of disaster in an urban area."
collection: portfolio
---

There is a disaster in an urban area. What happens to the people living there and the critical infrastructures in the city? 

  * Given simulations from an agent-based system that describes the behaviors of millions of agents and critical infrastructures, I am developing a data-driven reduced order model (ROM) that captures the important dynamics of the simulations. We want to **quickly and efficiently** predict what happens both to the agents and to the infrastructures under a set of initial conditions.
  * In tandem, I am developing my own simulation model, based on basic assumptions on agent behavior (e.g. people get their resources from their closest infrastructures) and infrastructures (e.g. all infrastructures can either be considered simple ODEs with mechanisms for refill and depletion OR binary variables that are on/off). The model is intended to be simple, quick, modular, and easily extendable. The end goal is to compare the outputs of the original ABS, the ROM, and my simulation model. 
