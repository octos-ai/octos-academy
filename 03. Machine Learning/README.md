# Classical Machine Learning

Vamos usar o _all-time classic_ [Machine Learning do Andrew Ng](https://www.coursera.org/learn/machine-learning) que tem um total de 18h de vídeo de aula (descontando o módulo de _Octave/Matlab_). Os exercícios serão feitos também em _Python_ (ao invés do original _Octave/Matlab_), contribuindo para o fortalecimento da proficiência.

Esse módulo é mais longo do que o [Data Handling](../Data%20Handling/README.md) e estimamos uma carga horário 48h para que o termine por completo. Ao fim, já terá uma base legal em ML e conseguirá fazer análises interessantes (aka _Data Science_) usando esse conhecimento combinado com a lib do Pandas.

Ainda estamos avaliando se haverá um mini-projeto de _Data Science_ depois.

![](machinelearning.jpg)

## Python Programming Assignments

This repositry contains the python versions of the programming assignments for the [Machine Learning online class](https://www.coursera.org/learn/machine-learning) taught by Professor Andrew Ng. This is perhaps the most popular introductory online machine learning class. In addition to being popular, it is also one of the best Machine learning classes any interested student can take to get started with machine learning. An unfortunate aspect of this class is that the programming assignments are in MATLAB or OCTAVE, probably because this class was made before python became the go-to language in machine learning.

The Python machine learning ecosystem has grown exponentially in the past few years, and is still gaining momentum. I suspect that many students who want to get started with their machine learning journey would like to start it with Python also. It is for those reasons I have decided to re-write all the programming assignments in Python, so students can get acquainted with its ecosystem from the start of their learning journey.

These assignments work seamlessly with the class and do not require any of the materials published in the MATLAB assignments. Here are some new and useful features for these sets of assignments:

- The assignments use [Jupyter Notebook](http://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/what_is_jupyter.html), which provides an intuitive flow easier than the original MATLAB/OCTAVE assignments.
- The original assignment instructions have been completely re-written and the parts which used to reference MATLAB/OCTAVE functionality have been changed to reference its `python` counterpart.
- The re-written instructions are now embedded within the Jupyter Notebook along with the `python` starter code. For each assignment, all work is done solely within the notebook.
- The `python` assignments can be submitted for grading. They were tested to work perfectly well with the original Coursera grader that is currently used to grade the MATLAB/OCTAVE versions of the assignments.
- After each part of a given assignment, the Jupyter Notebook contains a cell which prompts the user for submitting the current part of the assignment for grading.

Each assignment is contained in a separate folder. Each folder contains two files:

- The assignment `jupyter` notebook, which has a `.ipynb` extension. All the code which you need to write will be written within this notebook.
- A python module `utils.py` which contains some helper functions needed for the assignment. Functions within the `utils` module are called from the python notebook. You do not need to modify or add any code to this file.

### Requirements

These assignments has been tested and developed using the following libraries:

    - python==3.6.4
    - numpy==1.13.3
    - scipy==1.0.0
    - matplotlib==2.1.2
    - jupyter==1.0.0
    - jupyter-client==5.0.1

We recommend using at least these versions of the required libraries or later. Python 2 is not supported.

Create a new python environment with all the requirements using the following command:

    conda env create -f environment.yml

After the new environment is setup, activate it using (windows)

    activate machine_learning

or if you are on a linux machine

    source activate machine_learning

Now we have our python environment all set up, we can start working on the assignments. To do so, navigate to the directory where the assignments were installed, and launch the jupyter notebook from the terminal using the command

    jupyter notebook

This should automatically open a tab in the default browser.

## Caveats and tips

- In many of the exercises, the regularization parameter $\lambda$ is denoted as the variable name `lambda_`, notice the underscore at the end of the name. This is because `lambda` is a reserved python keyword, and should never be used as a variable name.

- In `numpy`, the function `dot` is used to perform matrix multiplication. The operation '\*' only does element-by-element multiplication (unlike MATLAB). If you are using python version 3.5+, the operator '@' is the new matrix multiplication, and it is equivalent to the `dot` function.

## Agradecimentos

- Professor Andrew Ng e equipe do curso da Stanford Machine Learning no Coursera.

- [Gerges Dib](https://github.com/dibgerge) pelos exercícios em Python.
