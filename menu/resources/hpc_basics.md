---
layout: page
title: "HPC basics"
permalink: /resources/hpcbasics
---

HPC systems provide a significant amount of computational resources for running advanced applications that require parallel processing. MPI and OpenMP are commonly used parallel programming frameworks for utilizing these resources, while nodes and CPUs are the building blocks of the HPC system. To utilize an HPC system, one can typically submit jobs to a scheduler using a job submission script.

Here's an example job submission script using the Slurm job scheduler:

```
#!/bin/bash
#SBATCH --job-name=myjob # Job name
#SBATCH --nodes=2 # Number of nodes
#SBATCH --ntasks-per-node=4 # Number of tasks (processes) per node
#SBATCH --mem-per-cpu=2G # Memory per CPU
#SBATCH --time=00:30:00 # Time limit in HH:MM:SS format

# Load any required modules
module load mymodule

# Change to the directory where the job will be run
cd $SLURM_SUBMIT_DIR

# Run the job
mpirun myprogram inputfile > outputfile
```

This script requests 2 nodes, each with 4 tasks (processes), and a total memory of 8 GB (2 GB per CPU). It also sets a time limit of 30 minutes for the job to complete. The module load command is used to load any required software modules, and the cd command changes to the directory where the job will be run. Finally, the mpirun command is used to run the myprogram executable, with inputfile as the input file and outputfile as the output file.

When this script is submitted to the Slurm scheduler using the sbatch command, Slurm will schedule the job to run on 2 nodes, with 4 tasks (processes) per node, and will allocate a total of 8 GB of memory to the job. The job will be given a unique ID by Slurm, which can be used to check the status of the job and view its output. Once the job completes, the output will be written to the specified output file.

You can find more information on FSU Jena's HPC clusters in the wiki for [ARA](https://wiki.uni-jena.de/pages/viewpage.action?pageId=22453005) and [Draco](https://wiki.uni-jena.de/pages/viewpage.action?pageId=22453002) (the wiki is in german only, [contact me](/contact) for any questions).