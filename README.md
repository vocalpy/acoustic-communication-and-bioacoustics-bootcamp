# acoustic-communication-and-bioacoustics-bootcamp

A bootcamp on acoustic communication and bioacoustics in Python,
presented at the Gordon Research Seminar Neural Mechanisms of Acoustic Communication 2024
by [Tessa Rhinehart](https://www.tessarhinehart.com/) and [David Nicholson](https://nicholdav.info/about.html).

## Prerequisites

### This code

The first thing you'll need is the Jupyter notebooks we will run during the bootcamp.
You can download the code by clicking on the blue "Code" button on the upper right,
and then clicking the "Download zip" panel in the pop-out that appears.
Your browser will download a zip file that you should unzip in whatever location is convenient for you on your computer,
e.g., `~\Users\You\documents\code`.

If you are familiar with the version control tool `git`, you can use it to `clone` the repository, e.g.,

```console
git clone https://github.com/vocalpy/acoustic-communication-and-bioacoustics-bootcamp.git
```

### A package manager

You will also need a [package manager](https://the-turing-way.netlify.app/reproducible-research/renv/renv-package), that can install other software libraries. We will use the conda package manager that is installed for you with the Anaconda distribution (https://docs.anaconda.com/anaconda/install/).

### A terminal program (AKA "the shell")

We will work with conda and Python through the terminal, also known as the shell (because it's a "shell" around the core operating system).

On macOS, you can use the built-in Terminal application or alternatives like iTerm2. If you install Anaconda, then conda will be available to you through the terminal. The built-in terminal will also work on Linux.

If you are on Windows and using Anaconda and the conda package manager, you will want to install and run vak through the Anaconda prompt, that can be accessed as shown in the video below.

We will only use the shell to start up Jupyter Lab, and we will show you how to do so.[^1]

## Set-up

First we will create a [virtual environment]() to work in.
This helps us make sure we all have a similar [computational environment](https://the-turing-way.netlify.app/reproducible-research/renv).

0. Install the Anaconda distribution on your computer (see link above)
1. In the terminal, create a conda environment.

(On most operating systems, you can copy and paste the following into the terminal -- you don't have to type it out!)

```console
conda create -n acabb-env "python=3.11" jupyterlab "vocalpy>=0.8.2" -c conda-forge
pip install "opensoundscape>=0.10.0"
```

2. Download the data here and place it in the `./data` folder: https://drive.google.com/drive/folders/1s1tS6obMyZ3xIaLqqP_aAmAx7eCcZxbh?usp=drive_link

You should end up with a folder structure like this:
```console
.
└── acoustic-communication-and-bioacoustics-bootcamp/
    ├── data/
    │   ├── Nicholson-Queen-Sober-2017-bfsongrepo-subset
    │   ├── Merino-Recalde-Wytham-Great-Tit-Dataset-2023-subset
    │   ├── Jourjine-et-al-2023-two-pup-calls-subset
    │   └── Elie-Theunissen-2016-zebra-finch-song-library-subset
    ├── code/
    │   ├── 00-data-prep.ipynb
    │   ├── 01-segmentation.ipynb
    │   └── ...
    ├── .gitignore
    ├── LICENSE
    └── README
```

## Getting started

After setting up, you will activate the virtual environment in the shell, and then start Jupyter to run the notebooks.

```console
conda activate acabb-env
jupyter lab
```

[^1]: However, if you are not yet familiar with working in the shell, we recommend that (at some point!) you work through
[this lesson](https://swcarpentry.github.io/shell-novice/) from [the Carpentries](https://carpentries.org/).
Videos are available of instructors leading these lessons on-line, for example
[this one](https://www.youtube.com/watch?v=ifgeZ9n7MpA&list=PLE9Qrf4CJnRGiT9L9VbyYHDnVFQnrIfaR).
You don't need to know all that for this bootcamp, though.