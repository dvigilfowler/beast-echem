---
layout: page
title: Thrust 3
description: "Thrust 3: BEAST-DB and machine-learned acceleration"
permalink: /thrust3/
---

# Thrust 3: BEAST-DB and machine-learned acceleration

<p style="text-align: center;">
<img alt="Thrust3" src="/images/Thrust3.jpg"/>
</p>

Towards our ultimate goal of improving computed reaction energetics using accurate calculations of electrocatalyst electronic structure and charge-state, we are leveraging the first-principles electrochemistry calculations described in Thrusts 1 and 2 to achieve beyond-DFT accuracy at the cost of DFT using machine learning (ML).
To do this, we are building an open database of grand canoncial DFT (GC-DFT) calculations and beyond-DFT properties (using GC-RPA/GW) for a representative subset of systems - BEAST DB. We are training ML models that input structural and electronic features from GC-DFT to predict beyond-DFT GC-RPA/GW quality reaction energetics.
These electronic features include the extent of wavefunction localization, bond orders, and projected density of states (PDOS).
We are developing open-source scripts to extract these properties automatically from, e.g. JDFTx and BerkeleyGW output files, and provide the information required for our proposed electrochemical database. 

For each electrochemical system considered, we are modeling the most relevant catalyst facets, solvents and electrolytes, electrolyte concentrations, and potentials to construct a database of maximal interest to experimental and theoretical electrochemists.
After initial testing of proposed ML approaches with our database and refining its schema, we will expand it with further contributions from the community to expand the space of catalysts and conditions in our database. We will determine where the predictions for our delta learning ML models' predictions are accurate and where new beyond-DFT calculations are necessary using our recently developed domain of applicability (DA) approach to assess ML model reliability.
Moreover, because of the computational cost of beyond-DFT GC-RPA/GW calculations, we will leverage our DA approach as an active learning scheme to train accurate ML models with relatively small datasets, which is typically the key bottleneck in the construction of accurate ML models.

At present, BEAST DB contains 80 unique bulk compositions, 120 surface facets, and over 3000 adsorbate (i.e., surface with bound molecule) calculations providing information on many important electrochemical reactions including the hydrogen evolution reaction (HER), the CO<sub>2</sub> reduction reaction (CO<sub>2</sub>R), the nitrogen reduction reaction (NRR), the oxygen evolution reaction (OER), the oxygen reduction reaction (ORR) and the partial methane oxidization reaction (pMOR) to methanol.
Materials classes include d-block metals, metal oxides, 2D chalcogenides, single-atom alloys (SAAs), 2D metal-nitrogen-carbon surfaces (MNCs), and multinary Chevrel phase (CP) chalcogenides.
Properties of electrocatalyst systems are studied as a function of bias, including adsorption energies (Eads), converged structure geometries, orbital-projected density of states (pDOS), surface-adsorbate pDOS overlap and Bader charge distributions.