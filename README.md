# EMV_Verify

# README.md for `for_data.ipynb`

## Overview

This repository contains a Mathematica notebook (`for_data.ipynb`) that solves the perturbation equation in the context of Einstein-Maxwell-Vector (EMV) black hole models. Specifically, it performs symbolic computations, transforms equations into their more standard forms (such as hypergeometric functions), and visualizes the results.

Key aspects include:

- Analytical and numerical solutions derived for the perturbation equation.
- Transformations into different coordinate systems (such as Boyer-Lindquist and isotropic coordinates).
- Numerical root-finding to determine parameters governing the solutions.
- Visualizations of solutions such as the electromagnetic mode as a function of `z`.

This repository accompanies the paper *"Spontaneous Vectorization in the Einstein-Maxwell-Vector Model"* on arXiv available at [arxiv:2410.xxxxx](https://arxiv.org/abs/2410.xxxxx).

The notebook also includes a comparison between the solutions and those described in existing research papers.

**Note**: This project relies on Wolfram Mathematica, or a Wolfram Engine is required for the execution of the code.


---

## Prerequisites

### 1. Jupyter Notebook (or VSCode Jupyter Extension)
To run the `.ipynb` notebook, you need Jupyter installed. You can either:

- Install Jupyter Notebook:
  ```bash
  pip install notebook
  ```
  
- Or use it in **VSCode** with the Jupyter extension.

### 2. Wolfram Mathematica / Wolfram Engine
For symbolic computations, this project requires **Wolfram Mathematica** or the free **Wolfram Engine**.

- Install **Wolfram Engine**:  
  Download from [here](https://www.wolfram.com/engine/).

- Install **Wolfram Jupyter Kernel**:  
  You can either use `wolframscript` or Wolfram Language directly:

#### Method 1: Using `wolframscript`
1. Clone the repository:
   ```bash
   git clone https://github.com/WolframResearch/WolframLanguageForJupyter.git
   ```
2. Configure Jupyter:
   - On macOS/Linux:
     ```bash
     ./configure-jupyter.wls add
     ```
   - On Windows:
     ```bash
     .\configure-jupyter.wls add
     ```

#### Method 2: Using Wolfram Language
1. Download the paclet from [Releases](https://github.com/WolframResearch/WolframLanguageForJupyter/releases).
2. In Wolfram Language:
   ```wolfram
   PacletInstall["WolframLanguageForJupyter-x.y.z.paclet"]
   Needs["WolframLanguageForJupyter`"]
   ConfigureJupyter["Add"]
   ```

For additional configuration, refer to the official [Wolfram Jupyter documentation](https://github.com/WolframResearch/WolframLanguageForJupyter).

---

## How to Use

1. **Clone the Repository**  
   First, clone the repository to your local machine

2. **Open the Notebook**  

   Starting the Jupyter interface:
   ```
   jupyter notebook for_data.ipynb
   ```
   or if you're using JupyterLab:
   ```
   jupyter lab for_data.ipynb
   ```

3. **Execute the Cells**  
   If you have installed everything successfully, you can execute each cell in sequence within `for_data.ipynb`. This involves solving perturbation equations, performing numerical root-finding, and generating plots.

---

## Structure of the Notebook

- **Useful Functions**:  
  This block evaluates a set of utility functions (`org`, `org2` etc.) to simplify symbolic expressions. These utilize assumptions about parameters such as `r`, `M`, `Q`, `x`, and `q`, which relate to black hole definitions.
  
- **Solving the Perturbation Equation**:  
  Includes symbolic transformations and simplifications of Einstein-Maxwell-Vector model perturbation equations. Key steps involve converting equations into their hypergeometric form and solving for specific boundary conditions.

- **Coordinate Transformations**:  
  The notebook transforms the perturbation equation into Boyer-Lindquist and isotropic coordinates, providing analytical solutions for both systems.

- **Numerical Solutions and Plots**:  
  The notebook uses the solutions derived to numerically determine roots and boundary values. Additionally, plots of the solutions such as `Bt(z)` and various boundary functions, are made to visualize the solutions.

In certain sections, comprehensive derivations are provided related to the equations and models pulled from literature, particularly related to the domain of existence of vector regular black holes. For more details on the boundary of `q - α` space explored numerically, you can reference the equation derivations included.

---

## Results

The solutions produced through symbolic manipulation and numerical root-finding can be visualized in several forms, including comparisons between the perturbation equation in Boyer-Lindquist coordinates and isotropic coordinates.

Notably:

- **Boundary Conditions**:  
  Numerical solutions satisfying boundary conditions for electromagnetic perturbation modes ($ Bt(z) $) and hypergeometric constraint verifications.
  
- **Plots**:  
  Solutions for specific values of the parameters ($α = 10, q = {0.83759, 0.976911}$) are plotted across $ z $, visualizing the behavior of the perturbation function.

- **Domain of Existence**:  
  The notebook numerically solves and plots the upper boundary of the domain of existence in the $(q-\alpha)$ space by solving the transcendental hypergeometric equation derived.

---

## Citation and Further Reading

Some of the results in this notebook were computed to verify or extend existing research in the black hole physics literature. Certain findings challenge or provide refinements on previously published results such as those found in:

> Oliveira:2020dru

You may also refer to this GitHub repository for a comprehensive derivation of the domain of existence for nodeless vector-regular black holes.

For citation or referencing, a footnote indicates potential discrepancies in the existing literature and refers to the full derivation provided in this repository.

---

## Contribution

This repository is a work-in-progress. If you wish to contribute:

1. Fork the repository.
2. Make changes or improvements.
3. Submit a pull request for review.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
