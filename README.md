
This repository explains the various scenarios to train your own models using the Azure AI Infrastructure (e.g., GPUs, Storage, etc.)


Pre-requisites:
It might be beneficial to clear some questions, such as: 
a. The GenAI use case. How is the training done now or the choice for a specific infrastructure, e.g., GPU, storage, scheduling, etc. 
b. How large the models are, e.g., number of parameters (million, billion, trillion?)
c. Confirm the compute capacity, GPU type, GPU memory, region and the SKU type.
d. The libraries and software packages in use for training, e.g., Pytorch, CUDA versions
e. Requirements for storage:
  (i)	Storage capacity – Size of checkpoints and how often.  
  (ii)	Throughput requirements
  (iii)	IOPS
  (iv)	How much is the active data for this workload. Active data is defined as the amount of input, output and intermediate (e.g., checkpoint) data created on the current project/job. 
f. Preferred way of training models using AI Infra, e.g., using SLURM, AKS or Open-Source Kubernetes.
g. What is done after training? How the models are used after training, e.g., inferencing ? Can Azure help to manage the models?
h. Plan for Resiliency -- Business Continuity Disaster Recovery. 

Distributed training on AI Infra can cater different scenarios. GPU infrastructure on Azure can be leveraged for distributed training in one or more of the following ways:
a.	Using SLURM (or similar) scheduler for distributed training using CUDA packages and/or MPI libraries. 
b.	Using Kubernetes cluster for distributed training, e.g., Azure Kubernetes Services (AKS)
c.	Using Kubernetes cluster for distributed training without AKS, e.g., Open-Source Kubernetes. 
