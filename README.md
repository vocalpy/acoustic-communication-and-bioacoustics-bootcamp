# acoustic-communication-and-bioacoustics-bootcamp

A bootcamp on acoustic communication and bioacoustics in Python,
presented at the Gordon Research Seminar Neural Mechanisms of Acoustic Communication 2024
by [Tessa Rhinehart](https://www.tessarhinehart.com/) and [David Nicholson](https://nicholdav.info/about.html).

## Prerequisites

### A package manager

First you need a [package manager](https://the-turing-way.netlify.app/reproducible-research/renv/renv-package), that can install other software libraries. We will use the conda package manager that is installed for you with the Anaconda distribution (https://docs.anaconda.com/anaconda/install/).

### A terminal program (AKA "the shell")

We will work with conda and Python through the terminal, also known as the shell (because it's a "shell" around the core operating system).

On macOS, you can use the built-in Terminal application or alternatives like iTerm2. If you install Anaconda, then conda will be available to you through the terminal. The built-in terminal will also work on Linux.

If you are on Windows and using Anaconda and the conda package manager, you will want to install and run vak through the Anaconda prompt, that can be accessed as shown in the video below.

If you are not yet familiar with working in the shell, we suggest you work through
[this lesson](https://swcarpentry.github.io/shell-novice/) from [the Carpentries](https://carpentries.org/).
Videos are available of instructors leading these lessons on-line, for example
[this one](https://www.youtube.com/watch?v=ifgeZ9n7MpA&list=PLE9Qrf4CJnRGiT9L9VbyYHDnVFQnrIfaR).

## Set-up

First we will create a [virtual environment]() to work in.
This helps us make sure we all have a similar [computational environment](https://the-turing-way.netlify.app/reproducible-research/renv).

0. Install the Anaconda distribution on your computer (see link above)
1. In the terminal, create a conda environment.

(On most operating systems, you can copy and paste the following into the terminal -- you don't have to type it out!)

```console
conda create -n acabb-env python=3.10 jupyterlab jupytext numpy librosa vocalpy -c conda-forge
```

## Getting started

After setting up, you will activate the virtual environment, and then start Jupyter to run the notebooks.

```console
conda activate acabb-env
jupyter lab
```
