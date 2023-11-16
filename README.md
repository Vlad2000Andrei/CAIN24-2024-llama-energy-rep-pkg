# Energy Efficiency Analysis of LLaMA-Generated Code
This repository is a companion page for the following thesis / publication:
> *Anonymous Authors*. 2023. Energy Efficiency Analysis of LLaMA-Generated Code. CAIN24.

It contains all the material required for replicating the study, including:
 - Scripts for generating code using CodeLLama.
 - Scripts for generating inputs for the code.
 - Scripts for generating running the experiment using Experiment Runner.

## How to cite us
The scientific article describing design, execution, and main results of this study is available [TODO](https://www.google.com).<br> 
If this study is helping your research, consider to cite it is as follows, thanks!

```
@article{,
  title={Energy Efficiency Analysis of LLaMA-Generated Code},
  author={Vlad-Andrei Cursaru and Laura Duits and Joel Milligan and Damla Ural and Berta Rodriguez-Sanchez and Vincenzo Stoico and Ivano Malavolta},
  journal={CAIN}
  volume={???},
  pages={???},
  year={2024},
  publisher={???}
}
```

## Quick start

Instructions on how to set up the execution environment and perform the experiment are available under [src/README.md](src/README.md).

## Repository Structure
This is the root directory of the repository. The directory is structured as follows:

```
    root-directory
    ㄴ src
    |  ㄴ energy
    |  |  ㄴ human
    |  |  ㄴ llama
    |  |  ㄴ utils
    |  ㄴ experiment_runner
    |  ㄴ models
    |  ㄴ Data Analysis
    ㄴ data
```  

The contents of the folders are:
* The [src](src/) folder contains the scripts for running the experiment and analysing the data, as well as a [README](src/README.md) file explaining how to use them.
    * The [energy](src/energy/) folder contains scripts for creating the benchmark inputs and the [RunnerConfig.py](src/energy/RunnerConfig.py) file used by experiment runner for executing the experiment. It also contains subfolders.
        * The [human](src/energy/human/) folder contains the code to be benchmarked for the human implementations of the algorithms.
        * The [llama](src/energy/llama/) folder contains the code to be benchmarked for the Llama implementations of the algorithms.
        * The [utils](src/energy/utils/) contains a script for compiling C++ versions of the algorithms.
    * The [experiment_runner](src/experiment_runner/) folder is where the Experiment Runner tool should be downloaded.
    * The [models](src/models/) folder is where the CodeLlama model should be downloaded.
    * The [server](src/server/) folder contains the HTTP Flask server used to facilitate communication between the Raspberry Pi and the Monsoon.
* The [data](data/) folder contains information on how to access the data generated by the experiments.


## Replication package naming convention
The final name of this repository, as appearing in the published article, should be formatted according to the following naming convention:
`CAIN24-2024-llama-energy-rep-pkg`

For example, the repository of a research published at the International conference on ICT for Sustainability (ICT4S) in 2022, which investigates cloud tactics would be named `ICT4S-2022-cloud-tactics-rep-pkg`

## Preferred repository license
As general indication, we suggest to use:
* [MIT license](https://opensource.org/licenses/MIT) for code-based repositories, and 
* [Creative Commons Attribution 4.0	(CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) for text-based repository (papers, docts, etc.).

For more information on how to add a license to your replication package, refer to the [official GitHUb documentation](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository).
