# hpc-matlab-run-command

[![Cuedo HPC Official](https://img.shields.io/static/v1?label=Cuedo%20HPC&message=official&color=blue&style=for-the-badge 'Badge with title Cuedo HPC Official')](https://cuedo.com.au)

This repository contains a [GitHub Action](https://github.com/features/actions) that can be used on hosted runners in the Cuedo HPC Datacenter.

The use of this software requires the runner to be hosted in the Cuedo Datacenter, a Cuedo HPC license key, and the correct licensing to be installed on the runner for any MATLAB products used.

## Examples

Use Cuedo HPC to run the commands in a file named myscript.m in the root of your repository.

```
name: Run MATLAB script on Cuedo HPC
on: [push]
jobs:
  my-job:
    name: Run MATLAB Script
    runs-on: [self-hosted, cuedo-hpc]
    steps:
      - name: Check out repository
        uses: actions/checkout@v3
      - name: Run script
        uses: cuedo-hpc/hpc-matlab-run-command@v1
        with:
          command: myscript
```
