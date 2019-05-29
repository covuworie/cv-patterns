# Consonant-vowel patterns of short words in English

## Description

Have you ever wondered what are the possible [consonant (C) and vowel (V) patterns](https://www.spellzone.com/unit08/page5.cfm) of short words in the English language? Furthermore, with what frequency do these patterns occur? As an example, for four letter words, it is clear that the pattern **VVVV** is impossible and intuitively we would expect that the pattern **CVCC** (e.g. *blab*, *drew*, *shut*, *chew*, *walk*, etc.) is far more common than the pattern **VVVC** (e.g. *aeon* and *eaux* are the only possibilities).

The aim of this repository is to find out the answers to the above questions for short words from three to six characters in length. We will use words from [All Scrabble Words](http://www.allscrabblewords.com) as our corpus.

## Environment

An **environment** for *computational reproducibility* of this project can be setup by following these simple steps:

1. Download and install `python 3.7.3 (64-bit)` (any 3.7.x version should be ok) for your operating system from [python.org](https://www.python.org/downloads/) or [anaconda](https://www.anaconda.com/download/).
Make sure to check the option "Add python 3.7 to PATH" during installation.

2. Download and install the latest version (any version should be ok) of [git-scm](https://git-scm.com/downloads) for your operating system.

3. Clone the [github](https://github.com/) repository:

```
git clone https://github.com/covuworie/cv-patterns.git
```

4. Use [pipenv](https://pipenv.readthedocs.io/en/latest/) to spawn a shell with the [virtualenv](https://virtualenv.pypa.io/en/latest/) activated (this will also load the .env environment variables):

```
pipenv shell
```

5. Install all packages from the [Pipfile](https://github.com/pypa/pipfile) (both *develop* and *default* packages):

```
pipenv install --dev
```

6. Launch the [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) application in your default browser:

```
jupyter lab
```

## Notebooks

Notebooks are located under the *notebooks* directory. The individual notebooks of the projects can be run interactively in *JupyterLab*. Or if you prefer, there is the [run-all notebook](nobel_physics_prizes/notebooks/run-all.ipynb), which allows one to run all the notebooks sequentially in a non-interactive manner. This is useful for reproducing the output results of the entire study without having to interact with the individual notebooks.

The outputs of the individual notebooks are located in HTML files under the *notebooks/html_output* directory and can be viewed in a web browser. They are produced after a notebook has been run by issuing the following command in a terminal from the *notebooks* directory:

```
jupyter nbconvert --to html --output-dir=html mynotebook.ipynb
```

The actual notebooks only contain source code and markdown narrative as the output is cleaned after running them by issuing the following commands in a terminal from the *notebooks* directory:

```
jupyter nbconvert --to notebook --ClearOutputPreprocessor.enabled=True mynotebook.ipynb

mv mynotebook.nbconvert.ipynb nbconvert.ipynb
```

Cleaning the output allows for better source control of notebooks as the diff outputs only contain code and markdown narrative changes. If output diffs are desired then the diffs between the versions of html files can be examined.
