# experiment name
Use this template to generate evidence for opportunities, vechicles, and products.

## Report
Describe where to find the most current report and give a brief synopsis of the results. For example
+ **Purpose:** Determine how much of *this* is required for *that* to become *those*.
+ **Synopsis:** 5 units of *this* is required for *that* to become *those*.
+ **Location:** `docs/report.pdf`
+ **Reproduce:** `src/some_script_that_reproduces_report_data_and_figs`

## Reproduction
Before you begin make sure you have the `<experiment_name>` environment activated. Refer to
the `Setup` section for instructions on how to do this.

Describe the steps required to reproduce the experiment and generate all relevant data.
Be as explicit as possible.
It would be best if all these instructions are codified in an executatble script.

## Setup
+ Follow directions to download miniconda installer for [Windows](https://conda.io/docs/user-guide/install/windows.html), [MacOS](https://conda.io/docs/user-guide/install/macos.html), or [Linux](https://conda.io/docs/user-guide/install/linux.html).
Run the installer script, e.g. for MacOS open a terminal and run:
```
bash Miniconda3-latest-MacOSX-x86_64.sh
```
which will open an installer screen that will walk you through installation.
+ Double check conda is updated.
```
conda update -n base conda
```
+ Create a virtual environment named '<experiment_name>'
```
conda create --file requirements.txt -c conda-forge -n <experiment_name>
```
When prompted new packages will be installed, procceed by pressing `y`.
+ Activate `<experiment_name>` virtual environment
```
conda activate <experiment_name>
```
+ Update virtual environment (when necessary)
```
conda env update -n <experiment_name> -f requirements.txt
```
+ Integration testing (for devs)- Check for code style and run tests
```
./integration.sh
```
+ To deactivate environment, use
```
conda deactivate
```
+ To remove an environment, use
```
conda env remove -n <experiment_name>
```
