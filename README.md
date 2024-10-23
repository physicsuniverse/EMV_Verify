## Overview

This repository contains a Mathematica notebook (`for_data.ipynb`) that solves the perturbation equation in the context of Einstein-Maxwell-Vector (EMV) black hole models. Specifically, it performs symbolic computations, transforms equations into their more standard forms (such as hypergeometric functions), and visualizes the results.

Key aspects include:

- Analytical solutions derived for the perturbation equation.
- Transformations into different coordinate systems (such as Boyer-Lindquist and isotropic coordinates).
- Specific boundary conditions to determine the upper boundary of the existence domain for the EMV model.
- Visualizations of numerical solutions.

This repository accompanies the paper *"Spontaneous Vectorization in the Einstein-Maxwell-Vector Model"* on arXiv available at [arXiv:2410.16920](https://arxiv.org/abs/2410.16920).

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
  
- **Solving the Perturbation Equation and Compare**:  
  Includes symbolic transformations and simplifications of Einstein-Maxwell-Vector model perturbation equations. The key step is to transform the perturbation equation through a change of coordinates to obtain the standard hypergeometric equation, thereby achieving an analytical solution to the perturbation equation. This section also demonstrates that the perturbation equation in the Boyer-Lindquist coordinate system can be transformed into the isotropic coordinate system's perturbation equation through a coordinate change, and both can be converted into a consistent standard hypergeometric equation through their respective transformations. Finally, it compares the shapes of the solutions to the perturbation equations in the two coordinate systems and the phenomenon of multiple branch solutions.
- **The upper boundary of the domain of existence  in the $(q-\alpha )$ space**:
  The perturbative analytical solution obtained in the previous chapter is used to impose asymptotically flat boundary conditions at infinity, yielding the required parameters. For a given $ \alpha  $, there are multiple $ q $ (dimensionless charges) values that satisfy our boundary conditions, with the smallest $q$  being the nodal-free solution primarily discussed in our article. By continuously varying the value of $ \alpha  $, a perfect boundary line for the domain of existence of the EMV model can be determined.
- **Numerical Solutions and Plots**:  
  This notebook provides a visualization of a set of numerical solutions $B_t(z), h(z)$ with the same parameter $ a=10 $ but different charges $ Q $. These numerical solutions are obtained using the numerical strategy described in the [article](https://doi.org/10.1103/PhysRevD.103.044004), facilitating validation by the reader.

---

## Further Reading

Some of the results in this notebook were computed to verify or extend existing research in the black hole physics literature. Certain findings challenge or provide refinements on previously published results such as those found in:

> [Spontaneous vectorization of electrically charged black holes](https://doi.org/10.1103/PhysRevD.103.044004)

You may also refer to this GitHub repository for a comprehensive derivation of the domain of existence for nodeless vector-regular black holes.

For citation or referencing, a footnote indicates potential discrepancies in the existing literature and refers to the full derivation provided in this repository.

---

## Contribution

This repository is a work-in-progress. If you wish to contribute:

1. Fork the repository.
2. Make changes or improvements.
3. Submit a pull request for review.

---

## Citation  

**Guang-Zai Ye**, **Chong-Ye Chen**, **GuoYang Fu**, **Chao Niu**, **Cheng-Yong Zhang**, **Peng Liu** (2024). *Spontaneous Vectorization in the Einstein-Maxwell-Vector Model*. [arXiv:2410.16920](https://arxiv.org/abs/2410.16920) [gr-qc]. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
