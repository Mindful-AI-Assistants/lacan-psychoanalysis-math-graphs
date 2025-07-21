<br>

## <p align="center"> [Lacan’s Graph of Desire — Mathematical Formalization \& Computational Psychoanalysis]()


<br>

https://github.com/user-attachments/assets/7380e439-6547-400b-8ef1-d03d2f9bf2e0

<br>

## Table of Contents

- [Overview](#overview)
- [Key Concepts](#key-concepts)
- [Recent Computational Formalization](#recent-computational-formalization)
- [Repository Structure](#repository-structure)
- [Installation](#installation)
- [Usage and Examples](#usage-and-examples)
- [Limits of Formalization: Gödel \& Lacan](#limits-of-formalization-g%C3%B6dels-incompleteness-theorems-and-lacanian-theory)
- Lacan’s Graph of Desire: A Comprehensive Visual Guide
- [References and Further Reading](#references-and-further-reading)
- [Contributing](#contributing)
- [License](#license)

<br>

## [Overview]():

This repository presents a detailed and interdisciplinary exploration of **Jacques Lacan's psychoanalytic theory**, with a focus on the **Graph of Desire** and associated *mathemes*—formal symbolic and topological models of unconscious subjectivity and desire.

By bridging psychoanalysis, formal mathematics, and computational modeling (including the Free Energy Principle), it provides theory, visualization, and simulation tools for researchers in **Humanistic AI, cognitive science, linguistics**, and psychoanalysis.


<br>

## [Key Concepts]()

- **Graph of Desire:** A structure showing how unconscious desire traverses and is shaped by language (the signifying chain), symbolic law (the Other), and internal division (the barred subject).
- **Mathemes:** Lacan’s formal logic of key psychoanalytic notions, like sexuation, subjectivity, and the structure of desire.
- **Symbolic Formalization:** Use of logic, topology, and graph theory to model the dynamics of the unconscious.

<br>


## [Recent Computational Formalization]()

A recent study ([Heins et al., 2025](https://doi.org/10.3389/fpsyg.2025.1574650)) **formalizes Lacanian psychoanalysis using the Free Energy Principle (FEP)**, providing computational simulations embodying concepts such as desire, the Other, and their dynamic relations.

<br>

### ⚡️ [Highlights]()

<br>

- Models the Real, Symbolic, and Imaginary (RSI) orders as interacting autonomous systems minimizing free energy.
- Simulates structures like the **Borromean knot**, **dyadic synchronization** (desire as metaphorical convergence), and **triadic collective behaviors** (the Other as emergent).
- Demonstrates that the subject’s desire is ultimately the *desire of the Other*, and that “the Other does not exist”; mirroring Gödelian incompleteness.

***This work connects psychoanalysis, computational neuroscience, and [Humanistic AI](), supporting the rigorous modeling of subjectivity and unconscious processes.***

<br>

## [Repository Structure]()

| Path | Contents |
| :-- | :-- |
| `/latex/` | LaTeX/TikZ code for Lacanian graphs |
| `/notebooks/` | Jupyter Notebooks for visualization and math |
| `/python/` | Python scripts for simulation |
| `/references/` | Papers and psychoanalytic bibliography |


<br>

## [Installation]()

[1](). Make sure you have Python 3.8+ and Jupyter Lab/Notebook installed.

[2](). Install required packages:

<br>

```bash
pip install matplotlib networkx sympy jupyterlab
```

<br>

[3](). Launch Jupyter and open the notebooks.

## Usage and Examples

This repository enables visualization and symbolic analysis of **Lacan’s Graph of Desire**:

<br>

## [Usage and Examples]()

This repository enables visualization and symbolic analysis of **Lacan’s Graph of Desire**:

<br>

- [**Graph visualization**]()
Use NetworkX and Matplotlib to plot nodes (barred subject, the Other, etc.) and edges (signifying chain, vector of desire).

<br>

- [**Horseshoe curve**]()
Plot the iconic *vector of desire* intersecting the signifying chain using Python.

<br>

- [**Mathemes with SymPy**]()
Generate and print symbolic formulas, e.g., Lacan's sexuation mathemes:
   
    - Masculine:  ∀x ¬Φ(x)
    - Feminine:  ¬∃x ¬Φ(x)

 <br>

- [**Computational psychoanalysis**]()
See notebooks simulating interactions inspired by the Free Energy Principle and Lacanian dynamics.

<br>


```python
%pip install networkx
%pip install sympy

#### Example: Visualizing the Graph of Desire

import matplotlib.pyplot as plt
import networkx as nx
import numpy as np
from sympy import symbols, Function
from sympy.logic.boolalg import Not
# ForAll and Exists are in sympy.logic.boolalg in newer versions, or use Function for custom logic

# 1. Graph construction
G = nx.DiGraph()
positions = {
    "$S$": (0, 0), "$S'$": (4, 0), "$A$": (1.8, 0),
    "$d$": (2.7, 0), "$\\$$": (2.25, 1.5), "$s(A)$": (2.1, 0.9)
}
for node in positions:
    G.add_node(node)
G.add_edge("$S$", "$S'$")
G.add_edge("$\\$$", "$d$")
G.add_edge("$\\$$", "$A$")
plt.figure(figsize=(8,5))
nx.draw_networkx_nodes(G, positions, node_size=700, node_color='lightblue')
nx.draw_networkx_labels(G, positions, font_size=12)
nx.draw_networkx_edges(G, positions, edgelist=[("$S$", "$S'$")], arrowstyle='-|>', arrowsize=20, edge_color='blue')
nx.draw_networkx_edges(G, positions, edgelist=[("$\\$$", "$d$"), ("$\\$$", "$A$")], style='dashed', edge_color='red', arrowstyle='-|>', arrowsize=15)
plt.axis('off')
plt.title('Simplified Lacan\'s Graph of Desire')
plt.show()

# 2. Curve of desire
t = np.linspace(0, np.pi, 200)
x = 2 + np.cos(t)
y = 1 + np.sin(t)
plt.plot([0,4], [0,0], color='blue', label='Signifying chain')
plt.plot(x, y, color='red', label='Vector of Desire')
plt.scatter([1.8, 2.7], [0, 0], color='black')
plt.text(1.8, -0.1, '$A$', fontsize=12, ha='center')
plt.text(2.7, -0.1, '$d$', fontsize=12, ha='center')
plt.text(2, 1.4, '$\\$$', fontsize=14, ha='center')
plt.title("Simplified Lacan's Graph of Desire")
plt.legend()
plt.axis('equal')
plt.axis('off')
plt.show()

# 3. Symbolic formulas (simplified representation)
x = symbols('x')
Phi = Function('Phi')

# Representing the formulas as strings since ForAll/Exists import issues
print("Masculine sexuation formula: ∀x ¬Φ(x)")
print("Feminine sexuation formula: ¬∃x ¬Φ(x)")
print("In symbolic form:")
print(f"Phi function: {Phi(x)}")
print(f"Not Phi: {Not(Phi(x))}")
```

<br>

## [Limits of Formalization: Gödel’s Incompleteness Theorems and Lacanian Theory]()

This repository not only formalizes Lacan’s psychoanalytic theory, but also acknowledges the [**limits of all formal systems**]() as demonstrated by [**Gödel’s incompleteness theorems**](). No [axiomatic model—whether]()  in mathematics, logic, or psychoanalysis—can be both complete and consistent. There will always be aspects of [reality]() (the “real” in Lacanian terms) that escape symbolic capture.

This parallel reinforces Lacan's insight that the unconscious and human subjectivity remain fundamentally open and incomplete, echoing the [**lack in the Other**]()  and the inherent boundaries of any modeling approach—critical for anyone working in [Humanistic AI]().


Below, I develop this parallel including the most relevant mathematical formalizations in LaTeX and its relation to Lacanian theory.

<br>

### [1](). Gödel and the limitations of formalization

Gödel proved that **no sufficiently powerful formal system** (such as basic arithmetic) can be both *complete* and *consistent*.

<br>

### - [**First Incompleteness Theorem**](): There exist true propositions in arithmetic that can never be proven within the formal system itself.

Mathematically, given a consistent and recursively enumerable formal system $F\$ that includes arithmetic, there is a statement $G_F\$ (called the Gödel sentence) such that:

<br>

$$
F \not\vdash G_F \quad \text{and} \quad F \not\vdash \neg G_F
$$

<br>

[That is](): neither $G_F\$ nor its negation can be proven in $F\$, rendering $F\$ incomplete.


<br><br>

### <p align="center">  ─── ⋅⋆ ─── ⋆⋅[✮]()⋅⋆ ─── ⋅⋆ ─── 

<br><br>


### - [**Second Incompleteness Theorem**](): The system $F\$ cannot prove its own consistency, formally expressed as:

<br>

$$
F \not\vdash \mathrm{Consis}(F)
$$

<br>

[Where](): $\mathrm{Consis}(F)$ is a formula within the system expressing the “non-contradiction” of $F\$.

<br>

### [2](). Conceptual translation to Lacan and psychoanalysis

The psychoanalytic subject’s experience, according to Lacan, is marked by a structure of *lack*, which he calls the **“Real”**; a domain resisting full symbolization by the **“Symbolic”** (language and its rules). This Real is precisely what escapes any complete and closed formalization.

- The **“Other”** (in Lacanian theory, the symbolic instance) contains a fundamental *lack*, a kind of **structural incompleteness** that prevents the subject from being perfectly represented or captured in totality.

- Just as Gödel shows that every formal system has inevitable limits (undemonstrable truths), the Lacanian subject experiences their unconscious as marked by an “excess” beyond the symbolic, not fully representable or accessible.

 
<br>






















<!--
<br>

 
## <p align="center"> [𝚿]() Lacan’s Graph of Desire — Mathematical Formalization and the Expression of the Unconscious in Psychoanalytic Theory


<br>

## Overview

This repository offers a deep exploration of **Jacques Lacan’s psychoanalytic theory**, focusing on the **Graph of Desire** and associated *mathemes*—formal symbolic and topological representations of unconscious subjectivity and desire.

By linking psychoanalysis with symbolic mathematics and computational frameworks such as the **Free Energy Principle (FEP)**, this project bridges psychoanalysis, linguistics, cognitive science, and **Humanistic Artificial Intelligence (AI)**.


<br>


## What’s Inside

- **LaTeX/TikZ visualizations** of Lacan’s key graphs, including the Graph of Desire, with elements such as the barred subject ($\$$), Other ($A$), and objet petit a ($a$).
- **Python Jupyter Notebooks** simulating Lacan-inspired dynamics using:
  - **NetworkX** — graph nodes and edges visualization
  - **Matplotlib** — plotting the vector of desire (horseshoe curve)
  - **SymPy** — symbolic logic to express Lacan’s sexuation mathemes
- Theoretical discussions on:
  - Alienation, truth, and transference
  - Embodiment and unconscious material formalization
  - Relationships between Lacanian theory and computational neuroscience
- Latest research insights formalizing Lacan’s psychoanalysis with the **Free Energy Principle** approach:
  - Modeling the **Real, Symbolic, Imaginary (RSI)** triad as autonomous, interacting units minimizing free energy
  - Formalizing **desire** as dyadic synchronization of symbolic orders
  - Modeling **the Other** as an emergent triadic collective dynamic
- Educational and research resources for linguists, psychoanalysts, AI researchers, and Humanistic AI data scientists.


  <br>

## Background on Lacan and Computational Psychoanalysis

**Jacques Lacan’s Graph of Desire** graphically illustrates the interaction between language (signifying chain), desire, and subjectivity, entwining:

- The **signifying chain** ($S \to S'$), representing linguistic structure
- The **vector of desire**, a horseshoe-shaped curve intersecting the chain
- The **barred subject** ($\$$), or the divided self mediated by language
- The **Other** ($A$), symbolic authority shaping subject formation
- The **objet petit a** ($a$), the elusive cause of desire perpetually sought

Recent computational work (e.g., Heins et al. 2025) embeds these concepts within the **Free Energy Principle (FEP)** framework, modeling living and cognitive systems as minimizing prediction error or "free energy."

<br>

This formalization reveals:

- Desire as **generalized synchronization** between subjects’ symbolic orders
- The **incompleteness and instability of the Other**, aligning with Lacan’s maxim “the Other does not exist”
- How intersubjectivity and unconscious drives can be simulated as dynamical systems


<br>


## Installation

1. Install Python 3.8+ (Anaconda recommended).  
2. Install dependencies:

   ```bash
   pip install matplotlib networkx sympy jupyterlab
   ```

3. Launch Jupyter Lab or Notebook:

   ```bash
   jupyter lab
   ```

4. Open and run notebooks in the `/notebooks` directory.

<br>

## Usage and Examples

### Visualizing Lacan’s Graph of Desire

- Directed graph of key Lacanian nodes and symbolic edges  
- Horseshoe-shaped vector of desire intersecting the signifying chain  
- Annotation of barred subject, Other, desire point

### Symbolic Formalization

- Logical symbolic formulas representing Lacan’s sexuation mathemes, e.g.:

  - Masculine sexuation: $$\forall x \neg \Phi(x)$$  
  - Feminine sexuation: $$\neg \exists x \neg \Phi(x)$$

### Computational Psychoanalytic Modeling

- Simulation scripts demonstrating basic dynamics inspired by Lacanian theory and FEP  
- Potential to extend with interactive widgets or agent-based models for deeper research


<br>


## Contributing

Contributions welcome from psychoanalysts, AI researchers, linguists, and data scientists! Please:

- Suggest new simulations or visualizations  
- Extend symbolic formalisms  
- Develop educational materials or case studies  

Submit issues or pull requests via GitHub.


##  Support

- For notebook files, detailed tutorials, or enhanced visualizations, please reach out.  

- Interested in Python notebooks simulating these dynamics or advanced Humanistic AI models? Just ask!


## Resources and References


- **Heins, R., et al. (2025).** *Formalizing Lacanian psychoanalysis through the free energy principle: computational simulations of desire, the Borromean knot, and the Other.* Frontiers in Psychology. [DOI:10.3389/fpsyg.2025.1574650](https://doi.org/10.3389/fpsyg.2025.1574650)  
  - [Texto completo](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2025.1574650/full)  
  - [Formato XML](https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2025.1574650/xml)  

- **Romanowicz, T., & Moncayo, J. (2015).** *Going beyond Castration in the Graph of Desire.* *The Letter*, Issue 58.  

- **Evans, D. (2022).** *Lacan.* In E. N. Zalta (Ed.), *The Stanford Encyclopedia of Philosophy* (Fall 2022 Edition). Stanford University.  
  - [Entrada completa](https://plato.stanford.edu/entries/lacan/)

- **Burham, C. (2022).** *Lacan and the Algorithm.* *CLCWeb: Comparative Literature and Culture*, 24(4), Article 2.  
  - [DOI:10.7771/1481-4374.4044](https://doi.org/10.7771/1481-4374.4044)

- **Stanford Encyclopedia of Philosophy:**  
  - [Entrada sobre Lacan](https://plato.stanford.edu/entries/lacan/)

- **Repositório de matemas lacanianos em TikZ:**  
  - [gjoncas / Lacan-Mathemes (GitHub)](https://github.com/gjoncas/Lacan-Mathemes)

- **Pré-publicação (arXiv):**  
  - [PDF: arXiv:2309.06707](https://arxiv.org/pdf/2309.06707.pdf)

- **PubMed Central (PMC):**  
  - [PMC12180394](https://pmc.ncbi.nlm.nih.gov/articles/PMC12180394/)

-->


<br>


## 💌 [Contact Me](mailto:fabicampanari@proton.me)

#### For any questions or suggestions, please feel free to reach out:


<br><br>



#### <p align="center">  🛸๋ My Contacts [Hub](https://linktr.ee/fabianacampanari)


<br>

### <p align="center"> <img src="https://github.com/user-attachments/assets/517fc573-7607-4c5d-82a7-38383cc0537d" />


<br><br><br>

<p align="center">  ────────────── 🔭⋆ ──────────────


<p align="center"> ➣➢➤ <a href="#top">Back to Top </a>

<b><br>

#

##### <p align="center">Copyright 2024 Mindful-AI-Assistants. Code released under the  [MIT license.]( https://github.com/Mindful-AI-Assistants/.github/blob/ad6948fdec771e022d49cd96f99024fcc7f1106a/LICENSE)







