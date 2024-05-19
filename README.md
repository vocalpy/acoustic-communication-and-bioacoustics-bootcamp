# acoustic-communication-and-bioacoustics-bootcamp
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

A bootcamp on acoustic communication and bioacoustics in Python,
presented at the Gordon Research Seminar Neural Mechanisms of Acoustic Communication 2024
by [Tessa Rhinehart](https://www.tessarhinehart.com/) and [David Nicholson](https://nicholdav.info/about.html).

Slides are here:
https://docs.google.com/presentation/d/1dhQCF-IdN4owf4hiC94sKMef_nvhpXVIvNpYK8wOEuY/edit?usp=sharing

## Prerequisites

### This code

The first thing you'll need is the Jupyter notebooks we will run during the bootcamp.

You can download the code by clicking on the "Code" button on the upper right,
and then clicking the "Download ZIP" panel in the pop-out that appears.

<img src="https://github.com/vocalpy/acoustic-communication-and-bioacoustics-bootcamp/blob/main/docs/images/download-github.png?raw=true" width=300 alt="image-of-code-button-with-download-panel">

(The button appears blue in light mode and green in dark mode -- either way it should be in the upper right of this page.)


Your browser will download a zip file that you should unzip in whatever location is convenient for you on your computer,
e.g., `~\Users\You\documents\code`.

Alternatively, if you are familiar with the version control tool `git`,
you can use it to `clone` the repository, e.g.,

```console
git clone https://github.com/vocalpy/acoustic-communication-and-bioacoustics-bootcamp.git
```

### A package manager

You will also need a [package manager](https://the-turing-way.netlify.app/reproducible-research/renv/renv-package), that can install other software libraries. We will use the conda package manager that is installed for you with the Anaconda distribution (https://docs.anaconda.com/anaconda/install/).

### A terminal program (AKA "the shell")

We will work with conda and Python through the terminal, also known as the shell (because it's a "shell" around the core operating system).

On macOS, you can use the built-in Terminal application or alternatives like iTerm2. If you install Anaconda, then conda will be available to you through the terminal. The built-in terminal will also work on Linux.

If you are on Windows and using Anaconda and the conda package manager, you will want to install and run vak through the Anaconda prompt, that can be accessed as shown in the video below.
https://www.youtube.com/watch?v=UAUO_K-bRMs

We will only use the shell to start up Jupyter Lab, and we will show you how to do so.[^1]

## Set-up

First we will create a [virtual environment](https://realpython.com/python-virtual-environments-a-primer/) to work in.
This helps us make sure we all have a similar [computational environment](https://the-turing-way.netlify.app/reproducible-research/renv). Conda can also [create environments](https://the-turing-way.netlify.app/reproducible-research/renv/renv-package),
so we will use conda.

### 1. Create virtual environment and install packages

0. Install the Anaconda distribution on your computer: https://docs.anaconda.com/anaconda/install/
1. In the terminal, create a conda environment.

(On most operating systems, you can copy and paste the following into the terminal -- you don't have to type it out!)

```console
conda create -n acabb-env "python=3.11" jupyterlab "vocalpy>=0.9.0" scikit-learn umap-learn hdbscan "seaborn>=0.13" -c conda-forge
```

After you create the virtual environment, you need to `activate` it.
This means you will be using the libraries you installed, and any other libraries you install will be added to the environment.

```console
conda activate acabb-env
```

You will know the environment is activated because your prompt in the terminal will change--usually the name of the
environment appears in parentheses, like so:
```console
(acabb-env) $
```

(or on Windows)

```console
(acabb-env) C:\>
```

Finally you will want to `pip install` three more packages into the virtual environment:
```console
pip install "opensoundscape>=0.10.1" tensorflow timm
```

([Pip](https://pip.pypa.io/en/stable/) is another package manager, that installs packages from the [Python Package Index](https://pypi.org/) (AKA PyPI).
We need to use pip to install because Google does not make conda packages for tensorflow,
and there is not yet a conda package for opensoundscape.
It's beyond the scope of this bootcamp, but
for purposes of scientific reproducibility you generally
want to avoid using pip in a conda environment,
and if you have to, you should use pip "last", after installing as much as you can with conda.
See [this blog post from 2018](https://www.anaconda.com/blog/understanding-conda-and-pip).
For even more nuance, see [this post from Itamar Turner-Trauring](https://pythonspeed.com/articles/conda-vs-pip/).
There are ongoing efforts to [make the two work better together](https://conda.io/projects/conda/en/latest/user-guide/configuration/pip-interoperability.html), including newer tools like [pixi](https://prefix.dev/blog/pixi_a_fast_conda_alternative).
)

### 2. Download data

Download the data here and place it in the `./data` folder: https://drive.google.com/drive/folders/1s1tS6obMyZ3xIaLqqP_aAmAx7eCcZxbh?usp=drive_link

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

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/DiaLiao"><img src="https://avatars.githubusercontent.com/u/10343894?v=4?s=100" width="100px;" alt="DiaLiao"/><br /><sub><b>DiaLiao</b></sub></a><br /><a href="https://github.com/vocalpy/acoustic-communication-and-bioacoustics-bootcamp/commits?author=DiaLiao" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/nickjourjine"><img src="https://avatars.githubusercontent.com/u/56172893?v=4?s=100" width="100px;" alt="Nick Jourjine"/><br /><sub><b>Nick Jourjine</b></sub></a><br /><a href="https://github.com/vocalpy/acoustic-communication-and-bioacoustics-bootcamp/commits?author=nickjourjine" title="Documentation">📖</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
